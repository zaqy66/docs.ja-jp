---
title: 機械学習モデルの品質を評価するメトリックを計算する - ML.NET
description: ML.NET を使用して機械学習モデルの品質を評価および検証するメトリックを計算する方法について説明します。
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: 6fd4dfab6104b4398918e42ed70584b04169a8c1
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149524"
---
# <a name="calculate-metrics-to-evaluate-machine-learning-model-quality---mlnet"></a><span data-ttu-id="82a22-103">機械学習モデルの品質を評価するメトリックを計算する - ML.NET</span><span class="sxs-lookup"><span data-stu-id="82a22-103">Calculate metrics to evaluate machine learning model quality - ML.NET</span></span>

<span data-ttu-id="82a22-104">モデルをトレーニングした後はどのように品質を評価すればよいでしょうか。</span><span class="sxs-lookup"><span data-stu-id="82a22-104">How do you evaluate quality after you train the model?</span></span> <span data-ttu-id="82a22-105">各機械学習タスクは品質評価用のメトリックを公開しています。</span><span class="sxs-lookup"><span data-stu-id="82a22-105">Each machine learning task exposes metrics for quality evaluation.</span></span>

<span data-ttu-id="82a22-106">次の例のように、タスクの対応する 'コンテキスト' を使用してモデルを評価することができます。</span><span class="sxs-lookup"><span data-stu-id="82a22-106">You can use the corresponding 'context' of the task to evaluate the model, as in the following example:</span></span>

```csharp
// Read the test dataset.
var testData = reader.Read(testDataPath);
// Calculate metrics of the model on the test data.
var metrics = mlContext.Regression.Evaluate(model.Transform(testData), label: "Target");
```