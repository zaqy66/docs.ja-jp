---
title: 機械学習のタスク - ML.NET
description: ML.NET でサポートされる機械学習のさまざまなタスクと、関連する学習器について説明します。
ms.custom: seodec18
ms.date: 11/29/2018
author: jralexander
ms.openlocfilehash: 4b333fb8c954c94ed84033d9858a496f591f2169
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53126589"
---
# <a name="machine-learning-tasks-in-mlnet"></a><span data-ttu-id="bfd98-103">ML.NET での機械学習のタスク</span><span class="sxs-lookup"><span data-stu-id="bfd98-103">Machine learning tasks in ML.NET</span></span>

<span data-ttu-id="bfd98-104">機械学習モデルを構築する場合は、データを使用して実現したい目的を最初に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfd98-104">When building a machine learning model, you first need to define what you are hoping to achieve with your data.</span></span> <span data-ttu-id="bfd98-105">その後で、状況に適した機械学習のタスクを選択できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-105">Afterwards, you can pick the right machine learning task for your situation.</span></span> <span data-ttu-id="bfd98-106">選択可能な機械学習のさまざまなタスクといくつかの一般的なユース ケースについて以下で説明します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-106">The following list describes the different machine learning tasks that you can choose from and some common use cases.</span></span>

> [!NOTE]
> <span data-ttu-id="bfd98-107">ML.NET は現在プレビュー段階です。</span><span class="sxs-lookup"><span data-stu-id="bfd98-107">ML.NET is currently in Preview.</span></span> <span data-ttu-id="bfd98-108">現時点では、機械学習のタスクがすべてサポートされているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="bfd98-108">Not all machine learning tasks are currently supported.</span></span> <span data-ttu-id="bfd98-109">特定のタスクに対するご要望を送信するには、[dotnet/machinelearning リポジトリ](https://github.com/dotnet/machinelearning/issues)で問題をオープンしてください。</span><span class="sxs-lookup"><span data-stu-id="bfd98-109">To submit a request for a certain task, open an issue in the [dotnet/machinelearning repository](https://github.com/dotnet/machinelearning/issues).</span></span>

## <a name="binary-classification"></a><span data-ttu-id="bfd98-110">二項分類</span><span class="sxs-lookup"><span data-stu-id="bfd98-110">Binary classification</span></span>

<span data-ttu-id="bfd98-111">データのインスタンスが 2 つのうちのどちらのクラス (カテゴリ) に属しているかを予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="bfd98-111">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict which of two classes (categories) an instance of data belongs to.</span></span> <span data-ttu-id="bfd98-112">分類アルゴリズムの入力はラベル付けされた一連のサンプルであり、各ラベルは整数 0 または 1 です。</span><span class="sxs-lookup"><span data-stu-id="bfd98-112">The input of a classification algorithm is a set of labeled examples, where each label is an integer of either 0 or 1.</span></span> <span data-ttu-id="bfd98-113">二項分類アルゴリズムの出力は分類子であり、ラベルのない新しいインスタンスのクラスを予測するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-113">The output of a binary classification algorithm is a classifier, which you can use to predict the class of new unlabeled instances.</span></span> <span data-ttu-id="bfd98-114">二項分類のシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-114">Examples of binary classification scenarios include:</span></span>

* <span data-ttu-id="bfd98-115">[Twitter コメントのセンチメントが "肯定的" か "否定的" かを理解する](../tutorials/sentiment-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="bfd98-115">[Understanding sentiment of Twitter comments](../tutorials/sentiment-analysis.md) as either "positive" or "negative".</span></span>
* <span data-ttu-id="bfd98-116">患者が特定の病気であるかどうかを診断する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-116">Diagnosing whether a patient has a certain disease or not.</span></span>
* <span data-ttu-id="bfd98-117">電子メールを "スパム" としてマークするかどうかを決定する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-117">Making a decision to mark an email as "spam" or not.</span></span>
* <span data-ttu-id="bfd98-118">写真に犬または果物が含まれているかどうかを決定する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-118">Determining if a photo contains a dog or fruit.</span></span>

<span data-ttu-id="bfd98-119">詳しくは、Wikipedia の[二項分類](https://en.wikipedia.org/wiki/Binary_classification)の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfd98-119">For more information, see the [Binary classification](https://en.wikipedia.org/wiki/Binary_classification) article on Wikipedia.</span></span>

<span data-ttu-id="bfd98-120">二項分類で推奨される学習器:</span><span class="sxs-lookup"><span data-stu-id="bfd98-120">Recommended learners for binary classification:</span></span>

* <span data-ttu-id="bfd98-121">AveragedPerceptronTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-121">AveragedPerceptronTrainer</span></span>
* <span data-ttu-id="bfd98-122">StochasticGradientDescentClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-122">StochasticGradientDescentClassificationTrainer</span></span>
* <span data-ttu-id="bfd98-123">LightGbmBinaryTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-123">LightGbmBinaryTrainer</span></span>
* <span data-ttu-id="bfd98-124">FastTreeBinaryClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-124">FastTreeBinaryClassificationTrainer</span></span>
* <span data-ttu-id="bfd98-125">SymSgdClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-125">SymSgdClassificationTrainer</span></span>

### <a name="binary-classification-learners"></a><span data-ttu-id="bfd98-126">二項分類学習器</span><span class="sxs-lookup"><span data-stu-id="bfd98-126">Binary Classification Learners</span></span>

<span data-ttu-id="bfd98-127">二項分類タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-127">The following learners are available for binary classification tasks:</span></span>

* [<span data-ttu-id="bfd98-128">AveragedPerceptronTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-128">AveragedPerceptronTrainer</span></span>](xref:Microsoft.ML.Trainers.Online.AveragedPerceptronTrainer)
* [<span data-ttu-id="bfd98-129">BinaryClassificationGamTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-129">BinaryClassificationGamTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.BinaryClassificationGamTrainer)
* [<span data-ttu-id="bfd98-130">FastForestClassification</span><span class="sxs-lookup"><span data-stu-id="bfd98-130">FastForestClassification</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastForestClassification)
* [<span data-ttu-id="bfd98-131">FastTreeBinaryClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-131">FastTreeBinaryClassificationTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer)
* [<span data-ttu-id="bfd98-132">FieldAwareFactorizationMachineTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-132">FieldAwareFactorizationMachineTrainer</span></span>](xref:Microsoft.ML.Runtime.FactorizationMachine.FieldAwareFactorizationMachineTrainer)
* [<span data-ttu-id="bfd98-133">LightGbmBinaryTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-133">LightGbmBinaryTrainer</span></span>](xref:Microsoft.ML.Runtime.LightGBM.LightGbmBinaryTrainer)
* [<span data-ttu-id="bfd98-134">LinearSvm</span><span class="sxs-lookup"><span data-stu-id="bfd98-134">LinearSvm</span></span>](xref:Microsoft.ML.Trainers.Online.LinearSvm)
* [<span data-ttu-id="bfd98-135">PriorTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-135">PriorTrainer</span></span>](xref:Microsoft.ML.Trainers.PriorTrainer)
* [<span data-ttu-id="bfd98-136">RandomTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-136">RandomTrainer</span></span>](xref:Microsoft.ML.Trainers.RandomTrainer)
* [<span data-ttu-id="bfd98-137">StochasticGradientDescentClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-137">StochasticGradientDescentClassificationTrainer</span></span>](xref:Microsoft.ML.Trainers.StochasticGradientDescentClassificationTrainer)
* [<span data-ttu-id="bfd98-138">SymSgdClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-138">SymSgdClassificationTrainer</span></span>](xref:Microsoft.ML.Trainers.SymSgd.SymSgdClassificationTrainer)

## <a name="multiclass-classification"></a><span data-ttu-id="bfd98-139">多クラス分類</span><span class="sxs-lookup"><span data-stu-id="bfd98-139">Multiclass classification</span></span>

<span data-ttu-id="bfd98-140">データのインスタンスのクラス (カテゴリ) を予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="bfd98-140">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict the class (category) of an instance of data.</span></span> <span data-ttu-id="bfd98-141">分類アルゴリズムの入力は、ラベル付けされた一連のサンプルです。</span><span class="sxs-lookup"><span data-stu-id="bfd98-141">The input of a classification algorithm is a set of labeled examples.</span></span> <span data-ttu-id="bfd98-142">各ラベルは、通常、テキストとして開始されます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-142">Each label normally starts as text.</span></span> <span data-ttu-id="bfd98-143">その後、TermTransform を経由してキー (数値) 型に変換されます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-143">It is then run through the TermTransform, which converts it to the Key (numeric) type.</span></span> <span data-ttu-id="bfd98-144">分類アルゴリズムの出力は分類子であり、ラベルのない新しいインスタンスのクラスを予測するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-144">The output of a classification algorithm is a classifier, which you can use to predict the class of new unlabeled instances.</span></span> <span data-ttu-id="bfd98-145">多クラス分類のシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-145">Examples of multi-class classification scenarios include:</span></span>

* <span data-ttu-id="bfd98-146">"シベリアン ハスキー"、"ゴールデン レトリバー"、"プードル" などの犬種を特定する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-146">Determining the breed of a dog as a "Siberian Husky", "Golden Retriever", "Poodle", etc.</span></span>
* <span data-ttu-id="bfd98-147">映画のレビューが "肯定的"、"中立"、"否定的" のどれかを理解する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-147">Understanding movie reviews as "positive", "neutral", or "negative".</span></span>
* <span data-ttu-id="bfd98-148">ホテルのレビューを "立地"、"価格"、"清潔さ" などに分類する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-148">Categorizing hotel reviews as "location", "price", "cleanliness", etc.</span></span>

<span data-ttu-id="bfd98-149">詳しくは、Wikipedia の[多クラス分類](https://en.wikipedia.org/wiki/Multiclass_classification)の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfd98-149">For more information, see the [Multiclass classification](https://en.wikipedia.org/wiki/Multiclass_classification) article on Wikipedia.</span></span>

<span data-ttu-id="bfd98-150">多クラスで推奨される学習器:</span><span class="sxs-lookup"><span data-stu-id="bfd98-150">Recommended learners for Multi-class:</span></span>

* <span data-ttu-id="bfd98-151">OVA-AveragedPerceptronTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-151">OVA-AveragedPerceptronTrainer</span></span>
* <span data-ttu-id="bfd98-152">SdcaMultiClassTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-152">SdcaMultiClassTrainer</span></span>
* <span data-ttu-id="bfd98-153">LightGbmMulticlassTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-153">LightGbmMulticlassTrainer</span></span>
* <span data-ttu-id="bfd98-154">OVA-FastTreeBinaryClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-154">OVA-FastTreeBinaryClassificationTrainer</span></span>

>[!NOTE]
><span data-ttu-id="bfd98-155">OVA と PKPD では、多クラス データセットに対して機能するように[二項分類学習器](#binary-classification)がアップグレードされています。</span><span class="sxs-lookup"><span data-stu-id="bfd98-155">OVA and PKPD upgrades any [binary classification learner](#binary-classification) to act on multiclass datasets.</span></span> <span data-ttu-id="bfd98-156">詳細については、[Wikipedia] (https://en.wikipedia.org/wiki/Multiclass_classification#One-vs.-rest)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfd98-156">More information on [Wikipedia] (https://en.wikipedia.org/wiki/Multiclass_classification#One-vs.-rest).</span></span>

### <a name="multiclass-classification-learners"></a><span data-ttu-id="bfd98-157">多クラス分類学習器</span><span class="sxs-lookup"><span data-stu-id="bfd98-157">Multiclass Classification Learners</span></span>

<span data-ttu-id="bfd98-158">多クラス分類タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-158">The following learners are available for multiclass classification tasks:</span></span>

* [<span data-ttu-id="bfd98-159">LightGbmMulticlassTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-159">LightGbmMulticlassTrainer</span></span>](xref:Microsoft.ML.Runtime.LightGBM.LightGbmMulticlassTrainer)
* [<span data-ttu-id="bfd98-160">MetaMulticlassTrainer<TTransformer,TModel></span><span class="sxs-lookup"><span data-stu-id="bfd98-160">MetaMulticlassTrainer<TTransformer,TModel></span></span>](xref:Microsoft.ML.Runtime.Learners.MetaMulticlassTrainer%602)
* [<span data-ttu-id="bfd98-161">MultiClassClassificationTrainers</span><span class="sxs-lookup"><span data-stu-id="bfd98-161">MultiClassClassificationTrainers</span></span>](xref:Microsoft.ML.Trainers.MultiClassClassificationTrainers)
* [<span data-ttu-id="bfd98-162">MultiClassNaiveBayesTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-162">MultiClassNaiveBayesTrainer</span></span>](xref:Microsoft.ML.Trainers.MultiClassNaiveBayesTrainer)
* [<span data-ttu-id="bfd98-163">Ova</span><span class="sxs-lookup"><span data-stu-id="bfd98-163">Ova</span></span>](xref:Microsoft.ML.Trainers.Ova)
* [<span data-ttu-id="bfd98-164">Pkpd</span><span class="sxs-lookup"><span data-stu-id="bfd98-164">Pkpd</span></span>](xref:Microsoft.ML.Trainers.Pkpd)
* [<span data-ttu-id="bfd98-165">SdcaMultiClassTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-165">SdcaMultiClassTrainer</span></span>](xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer)

## <a name="regression"></a><span data-ttu-id="bfd98-166">回帰</span><span class="sxs-lookup"><span data-stu-id="bfd98-166">Regression</span></span>

<span data-ttu-id="bfd98-167">関連する一連の特徴からラベルの値を予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="bfd98-167">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict the value of the label from a set of related features.</span></span> <span data-ttu-id="bfd98-168">ラベルには任意の実際の値を使用できます。分類タスクのように有限の値のセットから取得するものではありません。</span><span class="sxs-lookup"><span data-stu-id="bfd98-168">The label can be of any real value and is not from a finite set of values as in classification tasks.</span></span> <span data-ttu-id="bfd98-169">回帰アルゴリズムでは、ラベルに関連する特徴におけるラベルの依存関係をモデル化して、特徴の値が変化するとラベルがどのように変化するかを判断します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-169">Regression algorithms model the dependency of the label on its related features to determine how the label will change as the values of the features are varied.</span></span> <span data-ttu-id="bfd98-170">回帰アルゴリズムの入力は、既知の値のラベルが付いた一連のサンプルです。</span><span class="sxs-lookup"><span data-stu-id="bfd98-170">The input of a regression algorithm is a set of examples with labels of known values.</span></span> <span data-ttu-id="bfd98-171">回帰アルゴリズムの出力は関数であり、新しい入力特徴のセットのラベル値を予測するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-171">The output of a regression algorithm is a function, which you can use to predict the label value for any new set of input features.</span></span> <span data-ttu-id="bfd98-172">回帰のシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-172">Examples of regression scenarios include:</span></span>

* <span data-ttu-id="bfd98-173">住宅の属性 (寝室数、立地、規模など) に基づいて住宅価格を予測する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-173">Predicting house prices based on house attributes such as number of bedrooms, location, or size.</span></span>
* <span data-ttu-id="bfd98-174">履歴データと現在の市場動向に基づいて将来の株価を予測する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-174">Predicting future stock prices based on historical data and current market trends.</span></span>
* <span data-ttu-id="bfd98-175">広告予算に基づいて製品の売り上げを予測する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-175">Predicting sales of a product based on advertising budgets.</span></span>

<span data-ttu-id="bfd98-176">回帰で推奨される学習器:</span><span class="sxs-lookup"><span data-stu-id="bfd98-176">Recommended learners for regression:</span></span>

* <span data-ttu-id="bfd98-177">FastTreeTweedieTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-177">FastTreeTweedieTrainer</span></span> 
* <span data-ttu-id="bfd98-178">LightGbmRegressorTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-178">LightGbmRegressorTrainer</span></span> 
* <span data-ttu-id="bfd98-179">SdcaRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-179">SdcaRegressionTrainer</span></span> 
* <span data-ttu-id="bfd98-180">FastTreeRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-180">FastTreeRegressionTrainer</span></span>

### <a name="regression-learners"></a><span data-ttu-id="bfd98-181">回帰学習器</span><span class="sxs-lookup"><span data-stu-id="bfd98-181">Regression Learners</span></span>

<span data-ttu-id="bfd98-182">回帰タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-182">The following learners are available for regression tasks:</span></span>

* [<span data-ttu-id="bfd98-183">FastTreeRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-183">FastTreeRegressionTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeRegressionTrainer)
* [<span data-ttu-id="bfd98-184">FastTreeRegressionFastTreeTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-184">FastTreeRegressionFastTreeTrainer</span></span>](xref:Microsoft.ML.Runtime.FastTreeRegressionFastTreeTrainer)
* [<span data-ttu-id="bfd98-185">FastTreeTweedieRegressionFastTreeTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-185">FastTreeTweedieRegressionFastTreeTrainer</span></span>](xref:Microsoft.ML.Runtime.FastTreeTweedieRegressionFastTreeTrainer)
* [<span data-ttu-id="bfd98-186">FastTreeTweedieTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-186">FastTreeTweedieTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeTweedieTrainer)
* [<span data-ttu-id="bfd98-187">LightGbmRegressorTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-187">LightGbmRegressorTrainer</span></span>](xref:Microsoft.ML.Runtime.LightGBM.LightGbmRegressorTrainer)
* [<span data-ttu-id="bfd98-188">LogisticRegression</span><span class="sxs-lookup"><span data-stu-id="bfd98-188">LogisticRegression</span></span>](xref:Microsoft.ML.Runtime.Learners.LogisticRegression)
* [<span data-ttu-id="bfd98-189">OlsLinearRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-189">OlsLinearRegressionTrainer</span></span>](xref:Microsoft.ML.Trainers.HalLearners.OlsLinearRegressionTrainer)
* [<span data-ttu-id="bfd98-190">OnlineGradientDescentTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-190">OnlineGradientDescentTrainer</span></span>](xref:Microsoft.ML.Trainers.Online.OnlineGradientDescentTrainer)
* [<span data-ttu-id="bfd98-191">PoissonRegression</span><span class="sxs-lookup"><span data-stu-id="bfd98-191">PoissonRegression</span></span>](xref:Microsoft.ML.Trainers.PoissonRegression)
* [<span data-ttu-id="bfd98-192">RegressionGamTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-192">RegressionGamTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.RegressionGamTrainer)
* [<span data-ttu-id="bfd98-193">SdcaRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-193">SdcaRegressionTrainer</span></span>](xref:Microsoft.ML.Trainers.SdcaRegressionTrainer)
* [<span data-ttu-id="bfd98-194">FastTree.SingleTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-194">FastTree.SingleTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.SingleTrainer)
* [<span data-ttu-id="bfd98-195">LightGBM.SingleTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-195">LightGBM.SingleTrainer</span></span>](xref:Microsoft.ML.Runtime.LightGBM.SingleTrainer)

## <a name="clustering"></a><span data-ttu-id="bfd98-196">クラスタリング</span><span class="sxs-lookup"><span data-stu-id="bfd98-196">Clustering</span></span>

<span data-ttu-id="bfd98-197">データのインスタンスを、同様の特性を持つクラスタにグループ化するために使用する[教師なし機械学習](glossary.md#unsupervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="bfd98-197">An [unsupervised machine learning](glossary.md#unsupervised-machine-learning) task that is used to group instances of data into clusters that contain similar characteristics.</span></span> <span data-ttu-id="bfd98-198">また、閲覧や単純な観測では論理的に導き出せない可能性のあるデータ セットにおける関係をクラスタリングを使用して識別することもできます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-198">Clustering can also be used to identify relationships in a dataset that you might not logically derive by browsing or simple observation.</span></span> <span data-ttu-id="bfd98-199">クラスタリング アルゴリズムの入力と出力は、選択した方法によって異なります。</span><span class="sxs-lookup"><span data-stu-id="bfd98-199">The inputs and outputs of a clustering algorithm depends on the methodology chosen.</span></span> <span data-ttu-id="bfd98-200">分布、重心、結合性、または密度に基づくアプローチを利用できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-200">You can take a distribution, centroid, connectivity, or density-based approach.</span></span> <span data-ttu-id="bfd98-201">現在、ML.NET では、K 平均法によるクラスタリングを使用した重心に基づくアプローチをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bfd98-201">ML.NET currently supports a centroid-based approach using K-Means clustering.</span></span> <span data-ttu-id="bfd98-202">クラスタリングのシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-202">Examples of clustering scenarios include:</span></span>

* <span data-ttu-id="bfd98-203">ホテル選択の傾向と特性に基づいてホテルの宿泊客のセグメントを理解する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-203">Understanding segments of hotel guests based on habits and characteristics of hotel choices.</span></span>
* <span data-ttu-id="bfd98-204">対象を絞った広告キャンペーンの構築に役立つ顧客セグメントと統計データを特定する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-204">Identifying customer segments and demographics to help build targeted advertising campaigns.</span></span>
* <span data-ttu-id="bfd98-205">製造メトリックに基づいてインベントリを分類する。</span><span class="sxs-lookup"><span data-stu-id="bfd98-205">Categorizing inventory based on manufacturing metrics.</span></span>

### <a name="clustering-learners"></a><span data-ttu-id="bfd98-206">クラスタリング学習器</span><span class="sxs-lookup"><span data-stu-id="bfd98-206">Clustering Learners</span></span>

<span data-ttu-id="bfd98-207">クラスタリング タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-207">The following learners are available for clustering tasks:</span></span>

* [<span data-ttu-id="bfd98-208">KMeansPlusPlusTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-208">KMeansPlusPlusTrainer</span></span>](xref:Microsoft.ML.Trainers.KMeans.KMeansPlusPlusTrainer)

## <a name="anomaly-detection"></a><span data-ttu-id="bfd98-209">異常検出</span><span class="sxs-lookup"><span data-stu-id="bfd98-209">Anomaly detection</span></span>

<span data-ttu-id="bfd98-210">このタスクでは、主成分分析 (PCA) を使用して、異常検出モデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-210">This task creates an anomaly detection model by using Principal Component Analysis (PCA).</span></span> <span data-ttu-id="bfd98-211">PCA に基づく異常分析は、有効なトランザクションなどの 1 つのクラスからトレーニング データを簡単に取得できるが、対象とする異常の十分なサンプルを取得するのが難しいシナリオでモデルを構築するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-211">PCA-Based Anomaly Detection helps you build a model in scenarios where it is easy to obtain training data from one class, such as valid transactions, but difficult to obtain sufficient samples of the targeted anomalies.</span></span>

<span data-ttu-id="bfd98-212">機械学習における確立された手法である PCA は、データの内部構造を明らかにし、データの分散を説明するために、調査データ分析で頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-212">An established technique in machine learning, PCA is frequently used in exploratory data analysis because it reveals the inner structure of the data and explains the variance in the data.</span></span> <span data-ttu-id="bfd98-213">PCA は、複数の変数が含まれるデータを分析することで機能します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-213">PCA works by analyzing data that contains multiple variables.</span></span> <span data-ttu-id="bfd98-214">変数の相関を探し、結果内の差異を最も捕らえている値の合成を決定します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-214">It looks for correlations among the variables and determines the combination of values that best captures differences in outcomes.</span></span> <span data-ttu-id="bfd98-215">これらの合成されたフィーチャー値を使用して、主成分と呼ばれる、よりコンパクトなフィーチャー空間が作成されます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-215">These combined feature values are used to create a more compact feature space called the principal components.</span></span>

<span data-ttu-id="bfd98-216">異常検出には、機械学習における多くの重要なタスクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="bfd98-216">Anomaly detection encompasses many important tasks in machine learning:</span></span>

* <span data-ttu-id="bfd98-217">不正な可能性があるトランザクションを識別します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-217">Identifying transactions that are potentially fraudulent.</span></span>
* <span data-ttu-id="bfd98-218">ネットワークへの侵入が発生していることを示唆するパターンを学習します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-218">Learning patterns that indicate that a network intrusion has occurred.</span></span>
* <span data-ttu-id="bfd98-219">患者の異常なクラスターを検出します。</span><span class="sxs-lookup"><span data-stu-id="bfd98-219">Finding abnormal clusters of patients.</span></span>
* <span data-ttu-id="bfd98-220">システムに入力された値をチェックします。</span><span class="sxs-lookup"><span data-stu-id="bfd98-220">Checking values entered into a system.</span></span>

<span data-ttu-id="bfd98-221">異常とは定義上はまれに発生するイベントであるため、モデル化するために使用する代表的なデータ サンプルを収集するのは困難です。</span><span class="sxs-lookup"><span data-stu-id="bfd98-221">Because anomalies are rare events by definition, it can be difficult to collect a representative sample of data to use for modeling.</span></span> <span data-ttu-id="bfd98-222">このカテゴリに含まれるアルゴリズムは、不均衡なデータセットの使用によるモデルの構築とトレーニングという主要な課題に対処するように特別に設計されています。</span><span class="sxs-lookup"><span data-stu-id="bfd98-222">The algorithms included in this category have been especially designed to address the core challenges of building and training models by using imbalanced data sets.</span></span>

### <a name="anomaly-detection-learners"></a><span data-ttu-id="bfd98-223">異常検出学習器</span><span class="sxs-lookup"><span data-stu-id="bfd98-223">Anomaly detection learners</span></span>

<span data-ttu-id="bfd98-224">異常検出タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-224">The following learners are available for anomaly detection tasks:</span></span>

* [<span data-ttu-id="bfd98-225">RandomizedPcaTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-225">RandomizedPcaTrainer</span></span>](xref:Microsoft.ML.Trainers.PCA.RandomizedPcaTrainer)

## <a name="ranking"></a><span data-ttu-id="bfd98-226">ランキング</span><span class="sxs-lookup"><span data-stu-id="bfd98-226">Ranking</span></span>

<span data-ttu-id="bfd98-227">ランキング タスクでは、ラベル付きのサンプルのセットからランカーが構築されます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-227">A ranking task constructs a ranker from a set of labeled examples.</span></span> <span data-ttu-id="bfd98-228">この例のセットは、特定の条件を使用してスコア付けできるインスタンス グループで構成されています。</span><span class="sxs-lookup"><span data-stu-id="bfd98-228">This example set consists of instance groups that can be scored with a given criteria.</span></span> <span data-ttu-id="bfd98-229">順位付けのラベルは、インスタンスごとに {0、1、2、3, 4} です。</span><span class="sxs-lookup"><span data-stu-id="bfd98-229">The ranking labels are { 0, 1, 2, 3, 4 } for each instance.</span></span>  <span data-ttu-id="bfd98-230">各インスタンスのスコアが不明である新しいインスタンス グループをランク付けするように、ランカーがトレーニングされます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-230">The ranker is trained to rank new instance groups with unknown scores for each instance.</span></span> <span data-ttu-id="bfd98-231">ML.NET のランキング学習器は、[機械が学習したランキング](https://en.wikipedia.org/wiki/Learning_to_rank)に基づいています。</span><span class="sxs-lookup"><span data-stu-id="bfd98-231">ML.NET ranking learners are [machine learned ranking](https://en.wikipedia.org/wiki/Learning_to_rank) based.</span></span>

### <a name="ranking-learners"></a><span data-ttu-id="bfd98-232">ランキング学習器</span><span class="sxs-lookup"><span data-stu-id="bfd98-232">Ranking learners</span></span>

<span data-ttu-id="bfd98-233">ランキング タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-233">The following learners are available for ranking tasks:</span></span>

* [<span data-ttu-id="bfd98-234">FastTreeRankingFastTreeTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-234">FastTreeRankingFastTreeTrainer</span></span>](xref:Microsoft.ML.Runtime.FastTreeRankingFastTreeTrainer)
* [<span data-ttu-id="bfd98-235">FastTreeRankingTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-235">FastTreeRankingTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeRankingTrainer)
* [<span data-ttu-id="bfd98-236">LightGbmRankingTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-236">LightGbmRankingTrainer</span></span>](xref:Microsoft.ML.Runtime.LightGBM.LightGbmRankingTrainer)

## <a name="recommendation"></a><span data-ttu-id="bfd98-237">レコメンデーション</span><span class="sxs-lookup"><span data-stu-id="bfd98-237">Recommendation</span></span>

<span data-ttu-id="bfd98-238">レコメンデーション タスクによって、推奨される製品やサービスの一覧を作成できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-238">A recommendation task enables producing a list of recommended products or services.</span></span> <span data-ttu-id="bfd98-239">ML.NET では、カタログ内に製品のレーティングの履歴データがある場合は、レコメンデーション用の[協調フィルタリング](https://en.wikipedia.org/wiki/Collaborative_filtering) アルゴリズムである[行列因子分解 (MF)](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-239">ML.NET uses [Matrix factorization (MF)](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29), a [collaborative filtering](https://en.wikipedia.org/wiki/Collaborative_filtering) algorithm for recommendations when you have historical product rating data in your catalog.</span></span> <span data-ttu-id="bfd98-240">たとえば、ユーザーによる映画の採点の履歴データがあるときに、そのユーザーが次に見たいと思う映画を推薦できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-240">For example, you have historical movie rating data for your users and want to recommend  other movies they are likely to watch next.</span></span>

### <a name="recommendation-learners"></a><span data-ttu-id="bfd98-241">レコメンデーション学習機</span><span class="sxs-lookup"><span data-stu-id="bfd98-241">Recommendation learners</span></span>

<span data-ttu-id="bfd98-242">レコメンデーション タスクでは、次の学習器を利用できます。</span><span class="sxs-lookup"><span data-stu-id="bfd98-242">The following learners are available for recommendation tasks:</span></span>

* [<span data-ttu-id="bfd98-243">MatrixFactorizationTrainer</span><span class="sxs-lookup"><span data-stu-id="bfd98-243">MatrixFactorizationTrainer</span></span>](xref:Microsoft.ML.Trainers.MatrixFactorizationTrainer)
* [<span data-ttu-id="bfd98-244">MatrixFactorizationPredictionTransformer</span><span class="sxs-lookup"><span data-stu-id="bfd98-244">MatrixFactorizationPredictionTransformer</span></span>](xref:Microsoft.ML.Trainers.Recommender.MatrixFactorizationPredictionTransformer)
