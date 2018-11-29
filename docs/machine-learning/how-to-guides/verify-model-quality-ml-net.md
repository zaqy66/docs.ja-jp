---
title: 機械学習モデルの品質を評価するメトリックを計算する - ML.NET
description: ML.NET を使用して機械学習モデルの品質を評価および検証するメトリックを計算する方法について説明します。
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: 6fd4dfab6104b4398918e42ed70584b04169a8c1
ms.sourcegitcommit: 35316b768394e56087483cde93f854ba607b63bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2018
ms.locfileid: "52297569"
---
# <a name="calculate-metrics-to-evaluate-machine-learning-model-quality---mlnet"></a>機械学習モデルの品質を評価するメトリックを計算する - ML.NET

モデルをトレーニングした後はどのように品質を評価すればよいでしょうか。 各機械学習タスクは品質評価用のメトリックを公開しています。

次の例のように、タスクの対応する 'コンテキスト' を使用してモデルを評価することができます。

```csharp
// Read the test dataset.
var testData = reader.Read(testDataPath);
// Calculate metrics of the model on the test data.
var metrics = mlContext.Regression.Evaluate(model.Transform(testData), label: "Target");
```