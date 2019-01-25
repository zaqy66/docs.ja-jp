---
title: 機械学習のタスク - ML.NET
description: ML.NET でサポートされる機械学習のさまざまなタスクと、それらに関連するタスクについて説明します。
ms.custom: seodec18
ms.date: 01/15/2019
author: jralexander
ms.openlocfilehash: 02b454d18eca36c94c27ae15665af5df2ec87905
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54415703"
---
# <a name="machine-learning-tasks-in-mlnet"></a><span data-ttu-id="ce488-103">ML.NET での機械学習のタスク</span><span class="sxs-lookup"><span data-stu-id="ce488-103">Machine learning tasks in ML.NET</span></span>

<span data-ttu-id="ce488-104">機械学習モデルを構築する場合は、データを使用して実現したい目的を最初に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce488-104">When building a machine learning model, you first need to define what you are hoping to achieve with your data.</span></span> <span data-ttu-id="ce488-105">その後で、状況に適した機械学習のタスクを選択できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-105">Afterwards, you can pick the right machine learning task for your situation.</span></span> <span data-ttu-id="ce488-106">選択可能な機械学習のさまざまなタスクといくつかの一般的なユース ケースについて以下で説明します。</span><span class="sxs-lookup"><span data-stu-id="ce488-106">The following list describes the different machine learning tasks that you can choose from and some common use cases.</span></span>

> [!NOTE]
> <span data-ttu-id="ce488-107">ML.NET は現在プレビュー段階です。</span><span class="sxs-lookup"><span data-stu-id="ce488-107">ML.NET is currently in Preview.</span></span> <span data-ttu-id="ce488-108">現時点では、機械学習のタスクがすべてサポートされているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="ce488-108">Not all machine learning tasks are currently supported.</span></span> <span data-ttu-id="ce488-109">特定のタスクに対するご要望を送信するには、[dotnet/machinelearning リポジトリ](https://github.com/dotnet/machinelearning/issues)で問題をオープンしてください。</span><span class="sxs-lookup"><span data-stu-id="ce488-109">To submit a request for a certain task, open an issue in the [dotnet/machinelearning repository](https://github.com/dotnet/machinelearning/issues).</span></span>

## <a name="binary-classification"></a><span data-ttu-id="ce488-110">二項分類</span><span class="sxs-lookup"><span data-stu-id="ce488-110">Binary classification</span></span>

<span data-ttu-id="ce488-111">データのインスタンスが 2 つのうちのどちらのクラス (カテゴリ) に属しているかを予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="ce488-111">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict which of two classes (categories) an instance of data belongs to.</span></span> <span data-ttu-id="ce488-112">分類アルゴリズムの入力はラベル付けされた一連のサンプルであり、各ラベルは整数 0 または 1 です。</span><span class="sxs-lookup"><span data-stu-id="ce488-112">The input of a classification algorithm is a set of labeled examples, where each label is an integer of either 0 or 1.</span></span> <span data-ttu-id="ce488-113">二項分類アルゴリズムの出力は分類子であり、ラベルのない新しいインスタンスのクラスを予測するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-113">The output of a binary classification algorithm is a classifier, which you can use to predict the class of new unlabeled instances.</span></span> <span data-ttu-id="ce488-114">二項分類のシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ce488-114">Examples of binary classification scenarios include:</span></span>

* <span data-ttu-id="ce488-115">[Twitter コメントのセンチメントが "肯定的" か "否定的" かを理解する](../tutorials/sentiment-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="ce488-115">[Understanding sentiment of Twitter comments](../tutorials/sentiment-analysis.md) as either "positive" or "negative".</span></span>
* <span data-ttu-id="ce488-116">患者が特定の病気であるかどうかを診断する。</span><span class="sxs-lookup"><span data-stu-id="ce488-116">Diagnosing whether a patient has a certain disease or not.</span></span>
* <span data-ttu-id="ce488-117">電子メールを "スパム" としてマークするかどうかを決定する。</span><span class="sxs-lookup"><span data-stu-id="ce488-117">Making a decision to mark an email as "spam" or not.</span></span>
* <span data-ttu-id="ce488-118">写真に犬または果物が含まれているかどうかを決定する。</span><span class="sxs-lookup"><span data-stu-id="ce488-118">Determining if a photo contains a dog or fruit.</span></span>

<span data-ttu-id="ce488-119">詳しくは、Wikipedia の[二項分類](https://en.wikipedia.org/wiki/Binary_classification)の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce488-119">For more information, see the [Binary classification](https://en.wikipedia.org/wiki/Binary_classification) article on Wikipedia.</span></span>

<span data-ttu-id="ce488-120">二項分類で推奨される学習器:</span><span class="sxs-lookup"><span data-stu-id="ce488-120">Recommended learners for binary classification:</span></span>

* <span data-ttu-id="ce488-121">AveragedPerceptronTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-121">AveragedPerceptronTrainer</span></span>
* <span data-ttu-id="ce488-122">StochasticGradientDescentClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-122">StochasticGradientDescentClassificationTrainer</span></span>
* <span data-ttu-id="ce488-123">LightGbmBinaryTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-123">LightGbmBinaryTrainer</span></span>
* <span data-ttu-id="ce488-124">FastTreeBinaryClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-124">FastTreeBinaryClassificationTrainer</span></span>
* <span data-ttu-id="ce488-125">SymSgdClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-125">SymSgdClassificationTrainer</span></span>

### <a name="binary-classification-learners"></a><span data-ttu-id="ce488-126">二項分類学習器</span><span class="sxs-lookup"><span data-stu-id="ce488-126">Binary Classification Learners</span></span>

<span data-ttu-id="ce488-127">二項分類タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-127">The following learners are available for binary classification tasks:</span></span>

* [<span data-ttu-id="ce488-128">AveragedPerceptronTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-128">AveragedPerceptronTrainer</span></span>](xref:Microsoft.ML.Trainers.Online.AveragedPerceptronTrainer)
* [<span data-ttu-id="ce488-129">BinaryClassificationGamTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-129">BinaryClassificationGamTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.BinaryClassificationGamTrainer)
* [<span data-ttu-id="ce488-130">FastForestClassification</span><span class="sxs-lookup"><span data-stu-id="ce488-130">FastForestClassification</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastForestClassification)
* [<span data-ttu-id="ce488-131">FastTreeBinaryClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-131">FastTreeBinaryClassificationTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer)
* [<span data-ttu-id="ce488-132">FieldAwareFactorizationMachineTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-132">FieldAwareFactorizationMachineTrainer</span></span>](xref:Microsoft.ML.FactorizationMachine.FieldAwareFactorizationMachineTrainer)
* [<span data-ttu-id="ce488-133">LightGbmBinaryTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-133">LightGbmBinaryTrainer</span></span>](xref:Microsoft.ML.LightGBM.LightGbmBinaryTrainer)
* [<span data-ttu-id="ce488-134">LinearSvmTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-134">LinearSvmTrainer</span></span>](xref:Microsoft.ML.Trainers.Online.LinearSvmTrainer)
* [<span data-ttu-id="ce488-135">LogisticRegression</span><span class="sxs-lookup"><span data-stu-id="ce488-135">LogisticRegression</span></span>](xref:Microsoft.ML.Learners.LogisticRegression)
* [<span data-ttu-id="ce488-136">PriorTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-136">PriorTrainer</span></span>](xref:Microsoft.ML.Trainers.PriorTrainer)
* [<span data-ttu-id="ce488-137">RandomTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-137">RandomTrainer</span></span>](xref:Microsoft.ML.Trainers.RandomTrainer)
* [<span data-ttu-id="ce488-138">StochasticGradientDescentClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-138">StochasticGradientDescentClassificationTrainer</span></span>](xref:Microsoft.ML.Trainers.StochasticGradientDescentClassificationTrainer)
* [<span data-ttu-id="ce488-139">SymSgdClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-139">SymSgdClassificationTrainer</span></span>](xref:Microsoft.ML.Trainers.SymSgd.SymSgdClassificationTrainer)

## <a name="multiclass-classification"></a><span data-ttu-id="ce488-140">多クラス分類</span><span class="sxs-lookup"><span data-stu-id="ce488-140">Multiclass classification</span></span>

<span data-ttu-id="ce488-141">データのインスタンスのクラス (カテゴリ) を予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="ce488-141">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict the class (category) of an instance of data.</span></span> <span data-ttu-id="ce488-142">分類アルゴリズムの入力は、ラベル付けされた一連のサンプルです。</span><span class="sxs-lookup"><span data-stu-id="ce488-142">The input of a classification algorithm is a set of labeled examples.</span></span> <span data-ttu-id="ce488-143">各ラベルは、通常、テキストとして開始されます。</span><span class="sxs-lookup"><span data-stu-id="ce488-143">Each label normally starts as text.</span></span> <span data-ttu-id="ce488-144">その後、TermTransform を経由してキー (数値) 型に変換されます。</span><span class="sxs-lookup"><span data-stu-id="ce488-144">It is then run through the TermTransform, which converts it to the Key (numeric) type.</span></span> <span data-ttu-id="ce488-145">分類アルゴリズムの出力は分類子であり、ラベルのない新しいインスタンスのクラスを予測するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-145">The output of a classification algorithm is a classifier, which you can use to predict the class of new unlabeled instances.</span></span> <span data-ttu-id="ce488-146">多クラス分類のシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ce488-146">Examples of multi-class classification scenarios include:</span></span>

* <span data-ttu-id="ce488-147">"シベリアン ハスキー"、"ゴールデン レトリバー"、"プードル" などの犬種を特定する。</span><span class="sxs-lookup"><span data-stu-id="ce488-147">Determining the breed of a dog as a "Siberian Husky", "Golden Retriever", "Poodle", etc.</span></span>
* <span data-ttu-id="ce488-148">映画のレビューが "肯定的"、"中立"、"否定的" のどれかを理解する。</span><span class="sxs-lookup"><span data-stu-id="ce488-148">Understanding movie reviews as "positive", "neutral", or "negative".</span></span>
* <span data-ttu-id="ce488-149">ホテルのレビューを "立地"、"価格"、"清潔さ" などに分類する。</span><span class="sxs-lookup"><span data-stu-id="ce488-149">Categorizing hotel reviews as "location", "price", "cleanliness", etc.</span></span>

<span data-ttu-id="ce488-150">詳しくは、Wikipedia の[多クラス分類](https://en.wikipedia.org/wiki/Multiclass_classification)の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce488-150">For more information, see the [Multiclass classification](https://en.wikipedia.org/wiki/Multiclass_classification) article on Wikipedia.</span></span>

<span data-ttu-id="ce488-151">多クラスで推奨される学習器:</span><span class="sxs-lookup"><span data-stu-id="ce488-151">Recommended learners for Multi-class:</span></span>

* <span data-ttu-id="ce488-152">OVA-AveragedPerceptronTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-152">OVA-AveragedPerceptronTrainer</span></span>
* <span data-ttu-id="ce488-153">SdcaMultiClassTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-153">SdcaMultiClassTrainer</span></span>
* <span data-ttu-id="ce488-154">LightGbmMulticlassTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-154">LightGbmMulticlassTrainer</span></span>
* <span data-ttu-id="ce488-155">OVA-FastTreeBinaryClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-155">OVA-FastTreeBinaryClassificationTrainer</span></span>

>[!NOTE]
><span data-ttu-id="ce488-156">OVA と PKPD では、多クラス データセットに対して機能するように[二項分類学習器](#binary-classification)がアップグレードされています。</span><span class="sxs-lookup"><span data-stu-id="ce488-156">OVA and PKPD upgrades any [binary classification learner](#binary-classification) to act on multiclass datasets.</span></span> <span data-ttu-id="ce488-157">詳細については、[Wikipedia] (https://en.wikipedia.org/wiki/Multiclass_classification#One-vs.-rest)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce488-157">More information on [Wikipedia] (https://en.wikipedia.org/wiki/Multiclass_classification#One-vs.-rest).</span></span>

### <a name="multiclass-classification-learners"></a><span data-ttu-id="ce488-158">多クラス分類学習器</span><span class="sxs-lookup"><span data-stu-id="ce488-158">Multiclass Classification Learners</span></span>

<span data-ttu-id="ce488-159">多クラス分類タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-159">The following learners are available for multiclass classification tasks:</span></span>

* [<span data-ttu-id="ce488-160">LightGbmMulticlassTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-160">LightGbmMulticlassTrainer</span></span>](xref:Microsoft.ML.LightGBM.LightGbmMulticlassTrainer)
* [<span data-ttu-id="ce488-161">MetaMulticlassTrainer<TTransformer,TModel></span><span class="sxs-lookup"><span data-stu-id="ce488-161">MetaMulticlassTrainer<TTransformer,TModel></span></span>](xref:Microsoft.ML.Learners.MetaMulticlassTrainer%602)
* [<span data-ttu-id="ce488-162">MultiClassNaiveBayesTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-162">MultiClassNaiveBayesTrainer</span></span>](xref:Microsoft.ML.Trainers.MultiClassNaiveBayesTrainer)
* [<span data-ttu-id="ce488-163">Ova</span><span class="sxs-lookup"><span data-stu-id="ce488-163">Ova</span></span>](xref:Microsoft.ML.Trainers.Ova)
* [<span data-ttu-id="ce488-164">Pkpd</span><span class="sxs-lookup"><span data-stu-id="ce488-164">Pkpd</span></span>](xref:Microsoft.ML.Trainers.Pkpd)
* [<span data-ttu-id="ce488-165">SdcaMultiClassTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-165">SdcaMultiClassTrainer</span></span>](xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer)

## <a name="regression"></a><span data-ttu-id="ce488-166">回帰</span><span class="sxs-lookup"><span data-stu-id="ce488-166">Regression</span></span>

<span data-ttu-id="ce488-167">関連する一連の特徴からラベルの値を予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="ce488-167">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict the value of the label from a set of related features.</span></span> <span data-ttu-id="ce488-168">ラベルには任意の実際の値を使用できます。分類タスクのように有限の値のセットから取得するものではありません。</span><span class="sxs-lookup"><span data-stu-id="ce488-168">The label can be of any real value and is not from a finite set of values as in classification tasks.</span></span> <span data-ttu-id="ce488-169">回帰アルゴリズムでは、ラベルに関連する特徴におけるラベルの依存関係をモデル化して、特徴の値が変化するとラベルがどのように変化するかを判断します。</span><span class="sxs-lookup"><span data-stu-id="ce488-169">Regression algorithms model the dependency of the label on its related features to determine how the label will change as the values of the features are varied.</span></span> <span data-ttu-id="ce488-170">回帰アルゴリズムの入力は、既知の値のラベルが付いた一連のサンプルです。</span><span class="sxs-lookup"><span data-stu-id="ce488-170">The input of a regression algorithm is a set of examples with labels of known values.</span></span> <span data-ttu-id="ce488-171">回帰アルゴリズムの出力は関数であり、新しい入力特徴のセットのラベル値を予測するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-171">The output of a regression algorithm is a function, which you can use to predict the label value for any new set of input features.</span></span> <span data-ttu-id="ce488-172">回帰のシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ce488-172">Examples of regression scenarios include:</span></span>

* <span data-ttu-id="ce488-173">住宅の属性 (寝室数、立地、規模など) に基づいて住宅価格を予測する。</span><span class="sxs-lookup"><span data-stu-id="ce488-173">Predicting house prices based on house attributes such as number of bedrooms, location, or size.</span></span>
* <span data-ttu-id="ce488-174">履歴データと現在の市場動向に基づいて将来の株価を予測する。</span><span class="sxs-lookup"><span data-stu-id="ce488-174">Predicting future stock prices based on historical data and current market trends.</span></span>
* <span data-ttu-id="ce488-175">広告予算に基づいて製品の売り上げを予測する。</span><span class="sxs-lookup"><span data-stu-id="ce488-175">Predicting sales of a product based on advertising budgets.</span></span>

<span data-ttu-id="ce488-176">回帰で推奨される学習器:</span><span class="sxs-lookup"><span data-stu-id="ce488-176">Recommended learners for regression:</span></span>

* <span data-ttu-id="ce488-177">FastTreeTweedieTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-177">FastTreeTweedieTrainer</span></span> 
* <span data-ttu-id="ce488-178">LightGbmRegressorTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-178">LightGbmRegressorTrainer</span></span> 
* <span data-ttu-id="ce488-179">SdcaRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-179">SdcaRegressionTrainer</span></span> 
* <span data-ttu-id="ce488-180">FastTreeRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-180">FastTreeRegressionTrainer</span></span>

### <a name="regression-learners"></a><span data-ttu-id="ce488-181">回帰学習器</span><span class="sxs-lookup"><span data-stu-id="ce488-181">Regression Learners</span></span>

<span data-ttu-id="ce488-182">回帰タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-182">The following learners are available for regression tasks:</span></span>

* [<span data-ttu-id="ce488-183">FastTreeRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-183">FastTreeRegressionTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeRegressionTrainer)
* [<span data-ttu-id="ce488-184">FastTreeTweedieTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-184">FastTreeTweedieTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeTweedieTrainer)
* [<span data-ttu-id="ce488-185">LightGbmRegressorTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-185">LightGbmRegressorTrainer</span></span>](xref:Microsoft.ML.LightGBM.LightGbmRegressorTrainer)
* [<span data-ttu-id="ce488-186">OlsLinearRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-186">OlsLinearRegressionTrainer</span></span>](xref:Microsoft.ML.Trainers.HalLearners.OlsLinearRegressionTrainer)
* [<span data-ttu-id="ce488-187">OnlineGradientDescentTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-187">OnlineGradientDescentTrainer</span></span>](xref:Microsoft.ML.Trainers.Online.OnlineGradientDescentTrainer)
* [<span data-ttu-id="ce488-188">PoissonRegression</span><span class="sxs-lookup"><span data-stu-id="ce488-188">PoissonRegression</span></span>](xref:Microsoft.ML.Trainers.PoissonRegression)
* [<span data-ttu-id="ce488-189">RegressionGamTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-189">RegressionGamTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.RegressionGamTrainer)
* [<span data-ttu-id="ce488-190">SdcaRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-190">SdcaRegressionTrainer</span></span>](xref:Microsoft.ML.Trainers.SdcaRegressionTrainer)
* [<span data-ttu-id="ce488-191">FastTree.SingleTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-191">FastTree.SingleTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.SingleTrainer)
* [<span data-ttu-id="ce488-192">LightGBM.SingleTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-192">LightGBM.SingleTrainer</span></span>](xref:Microsoft.ML.LightGBM.SingleTrainer)

## <a name="clustering"></a><span data-ttu-id="ce488-193">クラスタリング</span><span class="sxs-lookup"><span data-stu-id="ce488-193">Clustering</span></span>

<span data-ttu-id="ce488-194">データのインスタンスを、同様の特性を持つクラスタにグループ化するために使用する[教師なし機械学習](glossary.md#unsupervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="ce488-194">An [unsupervised machine learning](glossary.md#unsupervised-machine-learning) task that is used to group instances of data into clusters that contain similar characteristics.</span></span> <span data-ttu-id="ce488-195">また、閲覧や単純な観測では論理的に導き出せない可能性のあるデータ セットにおける関係をクラスタリングを使用して識別することもできます。</span><span class="sxs-lookup"><span data-stu-id="ce488-195">Clustering can also be used to identify relationships in a dataset that you might not logically derive by browsing or simple observation.</span></span> <span data-ttu-id="ce488-196">クラスタリング アルゴリズムの入力と出力は、選択した方法によって異なります。</span><span class="sxs-lookup"><span data-stu-id="ce488-196">The inputs and outputs of a clustering algorithm depends on the methodology chosen.</span></span> <span data-ttu-id="ce488-197">分布、重心、結合性、または密度に基づくアプローチを利用できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-197">You can take a distribution, centroid, connectivity, or density-based approach.</span></span> <span data-ttu-id="ce488-198">現在、ML.NET では、K 平均法によるクラスタリングを使用した重心に基づくアプローチをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ce488-198">ML.NET currently supports a centroid-based approach using K-Means clustering.</span></span> <span data-ttu-id="ce488-199">クラスタリングのシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ce488-199">Examples of clustering scenarios include:</span></span>

* <span data-ttu-id="ce488-200">ホテル選択の傾向と特性に基づいてホテルの宿泊客のセグメントを理解する。</span><span class="sxs-lookup"><span data-stu-id="ce488-200">Understanding segments of hotel guests based on habits and characteristics of hotel choices.</span></span>
* <span data-ttu-id="ce488-201">対象を絞った広告キャンペーンの構築に役立つ顧客セグメントと統計データを特定する。</span><span class="sxs-lookup"><span data-stu-id="ce488-201">Identifying customer segments and demographics to help build targeted advertising campaigns.</span></span>
* <span data-ttu-id="ce488-202">製造メトリックに基づいてインベントリを分類する。</span><span class="sxs-lookup"><span data-stu-id="ce488-202">Categorizing inventory based on manufacturing metrics.</span></span>

### <a name="clustering-learners"></a><span data-ttu-id="ce488-203">クラスタリング学習器</span><span class="sxs-lookup"><span data-stu-id="ce488-203">Clustering Learners</span></span>

<span data-ttu-id="ce488-204">クラスタリング タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-204">The following learners are available for clustering tasks:</span></span>

* [<span data-ttu-id="ce488-205">KMeansPlusPlusTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-205">KMeansPlusPlusTrainer</span></span>](xref:Microsoft.ML.Trainers.KMeans.KMeansPlusPlusTrainer)

## <a name="anomaly-detection"></a><span data-ttu-id="ce488-206">異常検出</span><span class="sxs-lookup"><span data-stu-id="ce488-206">Anomaly detection</span></span>

<span data-ttu-id="ce488-207">このタスクでは、主成分分析 (PCA) を使用して、異常検出モデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="ce488-207">This task creates an anomaly detection model by using Principal Component Analysis (PCA).</span></span> <span data-ttu-id="ce488-208">PCA に基づく異常分析は、有効なトランザクションなどの 1 つのクラスからトレーニング データを簡単に取得できるが、対象とする異常の十分なサンプルを取得するのが難しいシナリオでモデルを構築するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ce488-208">PCA-Based Anomaly Detection helps you build a model in scenarios where it is easy to obtain training data from one class, such as valid transactions, but difficult to obtain sufficient samples of the targeted anomalies.</span></span>

<span data-ttu-id="ce488-209">機械学習における確立された手法である PCA は、データの内部構造を明らかにし、データの分散を説明するために、調査データ分析で頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ce488-209">An established technique in machine learning, PCA is frequently used in exploratory data analysis because it reveals the inner structure of the data and explains the variance in the data.</span></span> <span data-ttu-id="ce488-210">PCA は、複数の変数が含まれるデータを分析することで機能します。</span><span class="sxs-lookup"><span data-stu-id="ce488-210">PCA works by analyzing data that contains multiple variables.</span></span> <span data-ttu-id="ce488-211">変数の相関を探し、結果内の差異を最も捕らえている値の合成を決定します。</span><span class="sxs-lookup"><span data-stu-id="ce488-211">It looks for correlations among the variables and determines the combination of values that best captures differences in outcomes.</span></span> <span data-ttu-id="ce488-212">これらの合成されたフィーチャー値を使用して、主成分と呼ばれる、よりコンパクトなフィーチャー空間が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ce488-212">These combined feature values are used to create a more compact feature space called the principal components.</span></span>

<span data-ttu-id="ce488-213">異常検出には、機械学習における多くの重要なタスクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ce488-213">Anomaly detection encompasses many important tasks in machine learning:</span></span>

* <span data-ttu-id="ce488-214">不正な可能性があるトランザクションを識別します。</span><span class="sxs-lookup"><span data-stu-id="ce488-214">Identifying transactions that are potentially fraudulent.</span></span>
* <span data-ttu-id="ce488-215">ネットワークへの侵入が発生していることを示唆するパターンを学習します。</span><span class="sxs-lookup"><span data-stu-id="ce488-215">Learning patterns that indicate that a network intrusion has occurred.</span></span>
* <span data-ttu-id="ce488-216">患者の異常なクラスターを検出します。</span><span class="sxs-lookup"><span data-stu-id="ce488-216">Finding abnormal clusters of patients.</span></span>
* <span data-ttu-id="ce488-217">システムに入力された値をチェックします。</span><span class="sxs-lookup"><span data-stu-id="ce488-217">Checking values entered into a system.</span></span>

<span data-ttu-id="ce488-218">異常とは定義上はまれに発生するイベントであるため、モデル化するために使用する代表的なデータ サンプルを収集するのは困難です。</span><span class="sxs-lookup"><span data-stu-id="ce488-218">Because anomalies are rare events by definition, it can be difficult to collect a representative sample of data to use for modeling.</span></span> <span data-ttu-id="ce488-219">このカテゴリに含まれるアルゴリズムは、不均衡なデータセットの使用によるモデルの構築とトレーニングという主要な課題に対処するように特別に設計されています。</span><span class="sxs-lookup"><span data-stu-id="ce488-219">The algorithms included in this category have been especially designed to address the core challenges of building and training models by using imbalanced data sets.</span></span>

### <a name="anomaly-detection-learners"></a><span data-ttu-id="ce488-220">異常検出学習器</span><span class="sxs-lookup"><span data-stu-id="ce488-220">Anomaly detection learners</span></span>

<span data-ttu-id="ce488-221">異常検出タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-221">The following learners are available for anomaly detection tasks:</span></span>

* [<span data-ttu-id="ce488-222">RandomizedPcaTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-222">RandomizedPcaTrainer</span></span>](xref:Microsoft.ML.Trainers.PCA.RandomizedPcaTrainer)

## <a name="ranking"></a><span data-ttu-id="ce488-223">ランキング</span><span class="sxs-lookup"><span data-stu-id="ce488-223">Ranking</span></span>

<span data-ttu-id="ce488-224">ランキング タスクでは、ラベル付きのサンプルのセットからランカーが構築されます。</span><span class="sxs-lookup"><span data-stu-id="ce488-224">A ranking task constructs a ranker from a set of labeled examples.</span></span> <span data-ttu-id="ce488-225">この例のセットは、特定の条件を使用してスコア付けできるインスタンス グループで構成されています。</span><span class="sxs-lookup"><span data-stu-id="ce488-225">This example set consists of instance groups that can be scored with a given criteria.</span></span> <span data-ttu-id="ce488-226">順位付けのラベルは、インスタンスごとに {0、1、2、3, 4} です。</span><span class="sxs-lookup"><span data-stu-id="ce488-226">The ranking labels are { 0, 1, 2, 3, 4 } for each instance.</span></span>  <span data-ttu-id="ce488-227">各インスタンスのスコアが不明である新しいインスタンス グループをランク付けするように、ランカーがトレーニングされます。</span><span class="sxs-lookup"><span data-stu-id="ce488-227">The ranker is trained to rank new instance groups with unknown scores for each instance.</span></span> <span data-ttu-id="ce488-228">ML.NET のランキング学習器は、[機械が学習したランキング](https://en.wikipedia.org/wiki/Learning_to_rank)に基づいています。</span><span class="sxs-lookup"><span data-stu-id="ce488-228">ML.NET ranking learners are [machine learned ranking](https://en.wikipedia.org/wiki/Learning_to_rank) based.</span></span>

### <a name="ranking-learners"></a><span data-ttu-id="ce488-229">ランキング学習器</span><span class="sxs-lookup"><span data-stu-id="ce488-229">Ranking learners</span></span>

<span data-ttu-id="ce488-230">ランキング タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-230">The following learners are available for ranking tasks:</span></span>

* [<span data-ttu-id="ce488-231">FastTreeRankingTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-231">FastTreeRankingTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeRankingTrainer)
* [<span data-ttu-id="ce488-232">LightGbmRankingTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-232">LightGbmRankingTrainer</span></span>](xref:Microsoft.ML.LightGBM.LightGbmRankingTrainer)

## <a name="recommendation"></a><span data-ttu-id="ce488-233">推奨事項</span><span class="sxs-lookup"><span data-stu-id="ce488-233">Recommendation</span></span>

<span data-ttu-id="ce488-234">レコメンデーション タスクによって、推奨される製品やサービスの一覧を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-234">A recommendation task enables producing a list of recommended products or services.</span></span> <span data-ttu-id="ce488-235">ML.NET では、カタログ内に製品のレーティングの履歴データがある場合は、レコメンデーション用の[協調フィルタリング](https://en.wikipedia.org/wiki/Collaborative_filtering) アルゴリズムである[行列因子分解 (MF)](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ce488-235">ML.NET uses [Matrix factorization (MF)](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29), a [collaborative filtering](https://en.wikipedia.org/wiki/Collaborative_filtering) algorithm for recommendations when you have historical product rating data in your catalog.</span></span> <span data-ttu-id="ce488-236">たとえば、ユーザーによる映画の採点の履歴データがあるときに、そのユーザーが次に見たいと思う映画を推薦できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-236">For example, you have historical movie rating data for your users and want to recommend  other movies they are likely to watch next.</span></span>

### <a name="recommendation-learners"></a><span data-ttu-id="ce488-237">レコメンデーション学習機</span><span class="sxs-lookup"><span data-stu-id="ce488-237">Recommendation learners</span></span>

<span data-ttu-id="ce488-238">レコメンデーション タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="ce488-238">The following learners are available for recommendation tasks:</span></span>

* [<span data-ttu-id="ce488-239">MatrixFactorizationTrainer</span><span class="sxs-lookup"><span data-stu-id="ce488-239">MatrixFactorizationTrainer</span></span>](xref:Microsoft.ML.Trainers.MatrixFactorizationTrainer)
* [<span data-ttu-id="ce488-240">MatrixFactorizationPredictionTransformer</span><span class="sxs-lookup"><span data-stu-id="ce488-240">MatrixFactorizationPredictionTransformer</span></span>](xref:Microsoft.ML.Trainers.Recommender.MatrixFactorizationPredictionTransformer)
