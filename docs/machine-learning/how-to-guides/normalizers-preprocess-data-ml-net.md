---
title: データ処理に使用するトレーニング データのノーマライザーによる前処理 - ML.NET
description: ML.NET で機械学習モデルの構築、トレーニング、スコア付けに使用するトレーニング データを、ノーマライザーを使用して前処理する方法について説明します
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: c8b959904705e996c97bdcd8b3444e754d14d046
ms.sourcegitcommit: 35316b768394e56087483cde93f854ba607b63bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2018
ms.locfileid: "52297619"
---
# <a name="preprocess-training-data-with-normalizers-to-use-in-data-processing---mlnet"></a><span data-ttu-id="95c6f-103">データ処理に使用するトレーニング データのノーマライザーによる前処理 - ML.NET</span><span class="sxs-lookup"><span data-stu-id="95c6f-103">Preprocess training data with normalizers to use in data processing - ML.NET</span></span>

<span data-ttu-id="95c6f-104">ML.NET には、多数の[パラメトリック アルゴリズムと非パラメトリック アルゴリズム](https://machinelearningmastery.com/parametric-and-nonparametric-machine-learning-algorithms/)が公開されています。</span><span class="sxs-lookup"><span data-stu-id="95c6f-104">ML.NET exposes a number of [parametric and non-parametric algorithms](https://machinelearningmastery.com/parametric-and-nonparametric-machine-learning-algorithms/).</span></span>

<span data-ttu-id="95c6f-105">線形モデルや他のパラメトリック モデルのトレーニング時にノーマライザーを**使用する**ことは重要ですが、どのノーマライザーを選択するかはそれほど**重要ではありません**。</span><span class="sxs-lookup"><span data-stu-id="95c6f-105">It's **not** as important which normalizer you choose as it is to **use** a normalizer when training linear or other parametric models.</span></span>

<span data-ttu-id="95c6f-106">ノーマライザーは常に ML.NET の学習パイプラインに直接含めてください。その目的は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="95c6f-106">Always include the normalizer directly in the ML.NET learning pipeline, so it:</span></span>

- <span data-ttu-id="95c6f-107">テスト データではなく、トレーニング データに対してのみトレーニングする。</span><span class="sxs-lookup"><span data-stu-id="95c6f-107">is only trained on the training data, and not on your test data,</span></span>
- <span data-ttu-id="95c6f-108">予測時に余計な前処理を行うことなく、すべての新しい受信データに正しく適用する。</span><span class="sxs-lookup"><span data-stu-id="95c6f-108">is correctly applied to all the new incoming data, without the need for extra pre-processing at prediction time.</span></span>

<span data-ttu-id="95c6f-109">次の例は、学習パイプラインの正規化方法を示すコード スニペットです。</span><span class="sxs-lookup"><span data-stu-id="95c6f-109">Here's a snippet of code that demonstrates normalization in learning pipelines.</span></span> <span data-ttu-id="95c6f-110">Iris データセットを前提としています。</span><span class="sxs-lookup"><span data-stu-id="95c6f-110">It assumes the Iris dataset:</span></span>

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Define the reader: specify the data columns and where to find them in the text file.
var reader = mlContext.Data.TextReader(new TextLoader.Arguments
{
    Column = new[] {
        // The four features of the Iris dataset will be grouped together as one Features column.
        new TextLoader.Column("Features", DataKind.R4, 0, 3),
        // Label: kind of iris.
        new TextLoader.Column("Label", DataKind.TX, 4),
    },
    // Default separator is tab, but the dataset has comma.
    Separator = ","
});

// Read the training data.
var trainData = reader.Read(dataPath);

// Apply all kinds of standard ML.NET normalization to the raw features.
var pipeline =
    mlContext.Transforms.Normalize(
        new NormalizingEstimator.MinMaxColumn("Features", "MinMaxNormalized", fixZero: true),
        new NormalizingEstimator.MeanVarColumn("Features", "MeanVarNormalized", fixZero: true),
        new NormalizingEstimator.BinningColumn("Features", "BinNormalized", numBins: 256));

// Let's train our pipeline of normalizers, and then apply it to the same data.
var normalizedData = pipeline.Fit(trainData).Transform(trainData);

// Inspect one column of the resulting dataset.
var meanVarValues = normalizedData.GetColumn<float[]>(mlContext, "MeanVarNormalized").ToArray();
```
