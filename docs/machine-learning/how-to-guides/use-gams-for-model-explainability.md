---
title: ML.NET でモデルの説明可能性のために一般化加法モデルと形状関数を使う
description: ML.NET でモデルの説明可能性のために一般化加法モデルと形状関数を使う
ms.date: 02/06/2019
ms.custom: mvc,how-to
ms.openlocfilehash: c6f30a8cc5c07d97c62ded065f1e18a4f0523617
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2019
ms.locfileid: "56093113"
---
# <a name="use-generalized-additive-models-and-shape-functions-for-model-explainability-in-mlnet"></a><span data-ttu-id="b8bc0-103">ML.NET でモデルの説明可能性のために一般化加法モデルと形状関数を使う</span><span class="sxs-lookup"><span data-stu-id="b8bc0-103">Use Generalized Additive Models and shape functions for model explainability in ML.NET</span></span>

<span data-ttu-id="b8bc0-104">機械学習モデルを作成するとき、予測を作成するだけでは十分でないことがよくあります。</span><span class="sxs-lookup"><span data-stu-id="b8bc0-104">When creating machine learning models, it is often not enough to simply make predictions.</span></span> <span data-ttu-id="b8bc0-105">多くの場合、機械学習の開発者、意思決定者、およびモデルによって影響を受ける担当者は、機械学習モデルがどのように決定を行うか、またそのパフォーマンスにどの特徴が関係するかを理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8bc0-105">Often, machine learning developers, decision makers, and those affected by the models need to understand how machine learning models make decisions and which features contribute to their performance.</span></span> <span data-ttu-id="b8bc0-106">**一般化加法モデル (GAM)** は、モデルについて説明するために社内で使用され、他の人が簡単に解釈できる高性能モデルを機械学習の開発者が作成する際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b8bc0-106">**Generalized Additive Models (GAMs)** are used internally at Microsoft for model explainability to help machine learning developers create high-capacity models that can be easily interpreted by others.</span></span>

<span data-ttu-id="b8bc0-107">GAM は、線形モデルである**解釈可能モデル**の一種です。ここでは、用語は、1 つの変数の "形状関数" と呼ばれる非線形関数です。</span><span class="sxs-lookup"><span data-stu-id="b8bc0-107">GAMs are a class of **interpretable models** that are linear models where the terms are nonlinear functions, called "shape functions" of a single variable.</span></span> <span data-ttu-id="b8bc0-108">線形モデルとして、これらは簡単に解釈されます。ただし、モデルは 1 つの重みではなく特徴の関数を学習するため、1 つの線形モデルよりも複雑な関係をモデル化することができます。</span><span class="sxs-lookup"><span data-stu-id="b8bc0-108">As linear models, they are easily interpreted but because the models learn functions of features instead of a single weight, they can model more complex relationships than a simple linear model.</span></span> <span data-ttu-id="b8bc0-109">結果として得られる GAM 予測器は、トレーニング セットで平均予測を表す用語と、平均予測からの偏差を表す形状関数をインターセプトします。</span><span class="sxs-lookup"><span data-stu-id="b8bc0-109">The resulting GAM predictor has an intercept term that represents the average prediction over the training set, and shape functions that represent the deviation from the average prediction.</span></span> <span data-ttu-id="b8bc0-110">形状関数を調べると、さまざまな値の特徴に対するモデルのレスポンスを目視で確認でき、コード例の最後で作成される次のグラフのように視覚化できます。</span><span class="sxs-lookup"><span data-stu-id="b8bc0-110">The shape functions can be inspected by eye to see the response of the model to different values of a feature, and visualized like the following graph that is created at the end of the code example.</span></span> <span data-ttu-id="b8bc0-111">ML.NET の GAM トレーナーは、ノンパラメトリック形状関数を学習するように、浅い勾配ブースティング木 (たとえば切り株) を使って実装されます。これは、Lou、Caruana、Gehrke 共著の「[Intelligible Models for Classification and Regression](https://www.cs.cornell.edu/~yinlou/papers/lou-kdd12.pdf)」(分類および回帰の明瞭なモデル) で説明されている方法に基づいています。</span><span class="sxs-lookup"><span data-stu-id="b8bc0-111">The GAM trainer in ML.NET is implemented using shallow gradient boosted trees (for example tree stumps) to learn nonparametric shape functions, and is based on the method described in [Intelligible Models for Classification and Regression](https://www.cs.cornell.edu/~yinlou/papers/lou-kdd12.pdf) by Lou, Caruana, and Gehrke.</span></span>

```csharp
// Train the Generalized Additive Model
var fitPipeline = pipeline.Fit(data);
var gamModel = fitPipeline.LastTransformer.Model;

// The intercept for Generalize Additive Models represent the average prediction for the training data
var intercept = gamModel.Intercept;
Console.WriteLine($"Average predicted cost: {intercept:0.00}");

// Get the column names from the training set
var columnNames = data.Schema.AsEnumerable()
    .Select(column => column.Name) // Get the column names
    .Where(name => name != "MedianHomeValue") // Drop the Label
    .ToArray();

// Get the index of a variable from the training data
var myFeatureIndex = columnNames.ToList().FindIndex(str => str.Equals("MyFeature"));

// The shape functions represent the deviation from the average prediction as a function of the feature value
// It is represented by a discrete set of bins
// First, get the array of bin upper bounds from the model for this feature
var myFeatureBins = gamModel.GetBinUpperBounds(myFeatureIndex);
// Then get the array of bin weights; these are the effect size for each bin
var myFeatureWeights = gamModel.GetBinEffects(myFeatureIndex);

// Write out the shape function for the feature (see the following figure for what this looks like)
for (int i = 0; i < myFeatureBins.Length; i++)
{
    Console.WriteLine($"x < {myFeatureBins[i]:0.00} => {myFeatureWeights[i]:0.000}");
}
```

![一般化加法モデルの形状関数のグラフ](./media/use-gams-for-model-explainability/gam-shape-function-graph.png)

<span data-ttu-id="b8bc0-113">GAM モデルのトレーニングや、結果の検査と解釈の方法の例については、[dotnet/machinelearning GitHub リポジトリ](https://github.com/dotnet/machinelearning/blob/master/docs/samples/Microsoft.ML.Samples/Dynamic/GeneralizedAdditiveModels.cs)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b8bc0-113">For a sample of how to train a GAM model and inspect and interpret the results, see [the dotnet/machinelearning GitHub repository](https://github.com/dotnet/machinelearning/blob/master/docs/samples/Microsoft.ML.Samples/Dynamic/GeneralizedAdditiveModels.cs).</span></span>
