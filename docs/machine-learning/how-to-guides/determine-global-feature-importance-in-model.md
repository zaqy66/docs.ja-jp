---
title: ML.NET の Permutation Feature Importance を使ってモデルの特徴の重要度を判断する
description: ML.NET の Permutation Feature Importance を使ってモデルの特徴の重要度を理解する
ms.date: 12/04/2018
ms.custom: mvc,how-to
ms.openlocfilehash: ebad89aaee1155d7c116b8536307756227dced31
ms.sourcegitcommit: 75567a3cb437009db55949c6092f4e77ed1a9da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2019
ms.locfileid: "54307111"
---
# <a name="determine-the-feature-importance-of-models-with-permutation-feature-importance-in-mlnet"></a>ML.NET の Permutation Feature Importance を使ってモデルの特徴の重要度を判断する

機械学習モデルを作成するとき、予測を作成するだけでは十分でないことがよくあります。 多くの場合、機械学習の開発者、意思決定者、およびモデルによって影響を受ける担当者は、機械学習モデルがどのように決定を行うか、またそのパフォーマンスにどの特徴が関係するかを理解する必要があります。 `Permutation Feature Importance` (PFI) はモデルについて説明するツールであり、機械学習開発者がモデルの特徴の重要性をよく理解できるように社内で使用されています。

PFI は、トレーニングされた機械学習モデルの**グローバルな特徴の重要性**を判断する技術であり、Breiman 著[「Random Forests」論文、セクション 10](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf) から刺激を受けたものです。 PFI では、特徴の重要性を測定するために、"特徴の値がランダム* 値に設定されたら、どのような影響がモデルに及ぼされるか?" と質問します。 PFI 方法のメリットは、モデルに依存しない点です。評価することができるすべてのモデルに使用できます。また、特徴の重要性を計算するために、トレーニング セットだけでなく任意のデータセットを使用できます。 PFI を使用すると、このグラフのように特徴の重要性を示すことができます。

![Permutation Feature Importance グラフ](./media/determine-global-feature-importance-in-model/pfi-graph.png)

```csharp
// Compute the feature importance using PFI
var permutationMetrics = mlContext.Regression.PermutationFeatureImportance(model, data);
 
// Get the feature names from the training set
var featureNames = data.Schema.GetColumns()
                .Select(tuple => tuple.column.Name) // Get the column names
                .Where(name => name != labelName) // Drop the Label
                .ToArray();
 
// Write out the feature names and their importance to the model's R-squared value
for (int i = 0; i < featureNames.Length; i++)
  Console.WriteLine($"{featureNames[i]}\t{permutationMetrics[i].rSquared:G4}");
```

モデルの特徴の重要性を分析する PFI の使用例については、[dotnet/machinelearning GitHub リポジトリ](https://github.com/dotnet/machinelearning/tree/master/docs/samples/Microsoft.ML.Samples/Dynamic/PermutationFeatureImportance)をご覧ください。

/* 厳密にはランダムではありませんが、サンプルのセット全体で順序が変更されます。
