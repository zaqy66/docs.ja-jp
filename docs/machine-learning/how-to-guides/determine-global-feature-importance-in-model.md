---
title: ML.NET の Permutation Feature Importance を使ってモデルの特徴の重要度を判断する
description: ML.NET の Permutation Feature Importance を使ってモデルの特徴の重要度を理解する
ms.date: 02/01/2019
ms.custom: mvc,how-to
ms.openlocfilehash: a61e5dbbd544aa7df56291db9207343cb6f03e6e
ms.sourcegitcommit: facefcacd7ae2e5645e463bc841df213c505ffd4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2019
ms.locfileid: "55738813"
---
# <a name="determine-the-feature-importance-of-models-with-permutation-feature-importance-in-mlnet"></a><span data-ttu-id="d0061-103">ML.NET の Permutation Feature Importance を使ってモデルの特徴の重要度を判断する</span><span class="sxs-lookup"><span data-stu-id="d0061-103">Determine the feature importance of models with Permutation Feature Importance in ML.NET</span></span>

<span data-ttu-id="d0061-104">機械学習モデルを作成するとき、予測を作成するだけでは十分でないことがよくあります。</span><span class="sxs-lookup"><span data-stu-id="d0061-104">When creating machine learning models, it is often not enough to simply make predictions.</span></span> <span data-ttu-id="d0061-105">多くの場合、機械学習の開発者、意思決定者、およびモデルによって影響を受ける担当者は、機械学習モデルがどのように決定を行うか、またそのパフォーマンスにどの特徴が関係するかを理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0061-105">Often, machine learning developers, decision makers, and those affected by the models need to understand how machine learning models make decisions and which features contribute to their performance.</span></span> <span data-ttu-id="d0061-106">`Permutation Feature Importance` (PFI) はモデルについて説明するツールであり、機械学習開発者がモデルの特徴の重要性をよく理解できるように社内で使用されています。</span><span class="sxs-lookup"><span data-stu-id="d0061-106">`Permutation Feature Importance` (PFI) is a model explainability tool that is used internally at Microsoft to help machine learning developers better understand the feature importance of models.</span></span>

<span data-ttu-id="d0061-107">PFI は、トレーニングされた機械学習モデルの**グローバルな特徴の重要性**を判断する技術であり、Breiman 著[「Random Forests」論文、セクション 10](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf) から刺激を受けたものです。</span><span class="sxs-lookup"><span data-stu-id="d0061-107">PFI is a technique to determine **global feature importance** in a trained machine learning model, motivated by Breiman in the ["Random Forests" paper, section 10](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf).</span></span> <span data-ttu-id="d0061-108">PFI では、特徴の重要性を測定するために、"特徴の値がランダム\* 値に設定されたら、どのような影響がモデルに及ぼされるか?" と質問します。</span><span class="sxs-lookup"><span data-stu-id="d0061-108">PFI measures feature importance by asking the question, "What would the effect on the model be if the values for a feature were set to a random\* value?".</span></span> <span data-ttu-id="d0061-109">PFI 方法のメリットは、モデルに依存しない点です。評価することができるすべてのモデルに使用できます。また、特徴の重要性を計算するために、トレーニング セットだけでなく任意のデータセットを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d0061-109">The advantage of the PFI method is that it is model agnostic — it works with any model that can be evaluated — and it can use any dataset, not just the training set, to compute feature importance.</span></span> <span data-ttu-id="d0061-110">PFI を使用すると、このグラフのように特徴の重要性を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="d0061-110">You can use PFI like so to produce feature importances like this graph:</span></span>

![Permutation Feature Importance グラフ](./media/determine-global-feature-importance-in-model/pfi-graph.png)

```csharp
// Compute the feature importance using PFI
var permutationMetrics = mlContext.Regression.PermutationFeatureImportance(model.LastTransformer, model.Transform(data), "MedianHomeValue");

// Get the feature names from the training set
var featureNames =
    data.Schema.AsEnumerable()
    .Select(column => column.Name) // Get the column names
    .Where(name => name != "MedianHomeValue") // Drop the Label
    .ToArray();

// Write out the feature names and their importance to the model's Mean R-squared value
for (int i = 0; i < featureNames.Length;i++)
{
    Console.WriteLine($"{featureNames[i]}\t{permutationMetrics[i].RSquared.Mean:G4}");
}
```

<span data-ttu-id="d0061-112">モデルの特徴の重要性を分析する PFI の使用例については、[dotnet/machinelearning GitHub リポジトリ](https://github.com/dotnet/machinelearning/tree/master/docs/samples/Microsoft.ML.Samples/Dynamic/PermutationFeatureImportance)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d0061-112">For a sample using PFI to analyze the feature importance of a model, see [the dotnet/machinelearning GitHub repository](https://github.com/dotnet/machinelearning/tree/master/docs/samples/Microsoft.ML.Samples/Dynamic/PermutationFeatureImportance).</span></span>

<span data-ttu-id="d0061-113">/\* 厳密にはランダムではありませんが、サンプルのセット全体で順序が変更されます。</span><span class="sxs-lookup"><span data-stu-id="d0061-113">/\* Well, not random exactly, but permuted across the set of examples.</span></span>
