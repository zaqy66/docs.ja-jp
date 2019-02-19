---
title: 機械学習の用語集 - ML.NET
description: ML.NET でカスタム モデルをビルドする際に役立つ機械学習の重要な用語の用語集。
ms.custom: seodec18
ms.date: 12/20/2018
ms.openlocfilehash: 3dfa17e9264bf913465adb63ce0a90a9d196e617
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2019
ms.locfileid: "56092437"
---
# <a name="machine-learning-glossary-of-important-terms"></a><span data-ttu-id="16098-103">機械学習の重要な用語の用語集</span><span class="sxs-lookup"><span data-stu-id="16098-103">Machine learning glossary of important terms</span></span>

<span data-ttu-id="16098-104">ML.NET でカスタム モデルをビルドする際に役立つ機械学習の重要な用語を次に示します。</span><span class="sxs-lookup"><span data-stu-id="16098-104">The following list is a compilation of important machine learning terms that are useful as you build your custom models in ML.NET.</span></span>

## <a name="accuracy"></a><span data-ttu-id="16098-105">正確度</span><span class="sxs-lookup"><span data-stu-id="16098-105">Accuracy</span></span>

<span data-ttu-id="16098-106">[分類](#classification)における正確度は、正しく分類された項目の数をテスト セット内の項目の総数で割ったものです。</span><span class="sxs-lookup"><span data-stu-id="16098-106">In [classification](#classification), accuracy is the number of correctly classified items divided by the total number of items in the test set.</span></span> <span data-ttu-id="16098-107">0 (正確度が最も低い) ～ 1 (正確度が最も高い) の値になります。</span><span class="sxs-lookup"><span data-stu-id="16098-107">Ranges from 0 (least accurate) to 1 (most accurate).</span></span> <span data-ttu-id="16098-108">正確度は、モデル パフォーマンスの評価メトリックの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="16098-108">Accuracy is one of evaluation metrics of the model performance.</span></span> <span data-ttu-id="16098-109">[精度](#precision)、[再現率](#recall)、および [F 値](#f-score)と併せて考慮してください。</span><span class="sxs-lookup"><span data-stu-id="16098-109">Consider it in conjunction with [precision](#precision), [recall](#recall), and [F-score](#f-score).</span></span>

## <a name="area-under-the-curve-auc"></a><span data-ttu-id="16098-110">曲線下面積 (AUC)</span><span class="sxs-lookup"><span data-stu-id="16098-110">Area under the curve (AUC)</span></span>

<span data-ttu-id="16098-111">[二項分類](#binary-classification)における評価メトリックであり、偽陽性率 (x 軸上) に対する真陽性率 (y 軸上) を描画する曲線下面積の値です。</span><span class="sxs-lookup"><span data-stu-id="16098-111">In [binary classification](#binary-classification), an evaluation metric that is the value of the area under the curve that plots the true positives rate (on the y-axis) against the false positives rate (on the x-axis).</span></span> <span data-ttu-id="16098-112">0.5 (最低) ～ 1 (最高) の値になります。</span><span class="sxs-lookup"><span data-stu-id="16098-112">Ranges from 0.5 (worst) to 1 (best).</span></span> <span data-ttu-id="16098-113">ROC 曲線 (受信者操作特性曲線) 下面積とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="16098-113">Also known as the area under the ROC curve, i.e., receiver operating characteristic curve.</span></span> <span data-ttu-id="16098-114">詳しくは、Wikipedia の[受信者操作特性](https://en.wikipedia.org/wiki/Receiver_operating_characteristic)の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16098-114">For more information, see the [Receiver operating characteristic](https://en.wikipedia.org/wiki/Receiver_operating_characteristic) article on Wikipedia.</span></span>

## <a name="binary-classification"></a><span data-ttu-id="16098-115">二項分類</span><span class="sxs-lookup"><span data-stu-id="16098-115">Binary classification</span></span>

<span data-ttu-id="16098-116">[ラベル](#label)が 2 つのクラスのうちの 1 つである[分類](#classification)です。</span><span class="sxs-lookup"><span data-stu-id="16098-116">A [classification](#classification) case where the [label](#label) is only one out of two classes.</span></span> <span data-ttu-id="16098-117">詳細については、トピック「[機械学習のタスク](tasks.md)」のセクションの「[二項分類](tasks.md#binary-classification)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16098-117">For more information, see the [Binary classification](tasks.md#binary-classification) section of the [Machine learning tasks](tasks.md) topic.</span></span>

## <a name="classification"></a><span data-ttu-id="16098-118">分類</span><span class="sxs-lookup"><span data-stu-id="16098-118">Classification</span></span>

<span data-ttu-id="16098-119">データを使用してカテゴリを予測する際、[教師あり機械学習](#supervised-machine-learning)タスクが分類と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="16098-119">When the data is used to predict a category, [supervised machine learning](#supervised-machine-learning) task is called classification.</span></span> <span data-ttu-id="16098-120">[二項分類](#binary-classification)とは、2 つのカテゴリだけを予測する (たとえば、画像を猫または犬の写真として分類する) ことです。</span><span class="sxs-lookup"><span data-stu-id="16098-120">[Binary classification](#binary-classification) refers to predicting only two categories (for example, classifying an image as a picture of either a 'cat' or a 'dog').</span></span> <span data-ttu-id="16098-121">[多クラス分類](#multiclass-classification)とは、複数のカテゴリを予測する (たとえば、画像を特定の犬種の写真として分類する) ことです。</span><span class="sxs-lookup"><span data-stu-id="16098-121">[Multiclass classification](#multiclass-classification) refers to predicting multiple categories (for example, when classifying an image as a picture of a specific breed of dog).</span></span>

## <a name="coefficient-of-determination"></a><span data-ttu-id="16098-122">決定係数</span><span class="sxs-lookup"><span data-stu-id="16098-122">Coefficient of determination</span></span>

<span data-ttu-id="16098-123">[回帰](#regression)における評価メトリックであり、データがモデルにどの程度適合するかを示します。</span><span class="sxs-lookup"><span data-stu-id="16098-123">In [regression](#regression), an evaluation metric that indicates how well data fits a model.</span></span> <span data-ttu-id="16098-124">0 ～ 1 の値になります。</span><span class="sxs-lookup"><span data-stu-id="16098-124">Ranges from 0 to 1.</span></span> <span data-ttu-id="16098-125">値 0 は、データがランダムであるか、モデルに適合できないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="16098-125">A value of 0 means that the data is random or otherwise cannot be fit to the model.</span></span> <span data-ttu-id="16098-126">値 1 は、モデルがデータと完全に一致していることを意味します。</span><span class="sxs-lookup"><span data-stu-id="16098-126">A value of 1 means that the model exactly matches the data.</span></span> <span data-ttu-id="16098-127">多くの場合、これは r<sup>2</sup>、R<sup>2</sup>、または r の 2 乗と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="16098-127">This is often referred to as r<sup>2</sup>, R<sup>2</sup>, or r-squared.</span></span>

## <a name="feature"></a><span data-ttu-id="16098-128">機能</span><span class="sxs-lookup"><span data-stu-id="16098-128">Feature</span></span>

<span data-ttu-id="16098-129">測定対象となる事象の測定可能なプロパティです。通常は数 (倍精度) 値になります。</span><span class="sxs-lookup"><span data-stu-id="16098-129">A measurable property of the phenomenon being measured, typically a numeric (double) value.</span></span> <span data-ttu-id="16098-130">複数の特徴は**特徴ベクトル**と呼ばれ、通常は `double[]` として格納されます。</span><span class="sxs-lookup"><span data-stu-id="16098-130">Multiple features are referred to as a **Feature vector** and typically stored as `double[]`.</span></span> <span data-ttu-id="16098-131">特徴では、測定対象となる事象の重要な特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="16098-131">Features define the important characteristics of the phenomenon being measured.</span></span> <span data-ttu-id="16098-132">詳しくは、Wikipedia の[特徴](https://en.wikipedia.org/wiki/Feature_(machine_learning))の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16098-132">For more information, see the [Feature](https://en.wikipedia.org/wiki/Feature_(machine_learning)) article on Wikipedia.</span></span>

## <a name="feature-engineering"></a><span data-ttu-id="16098-133">特徴エンジニアリング</span><span class="sxs-lookup"><span data-stu-id="16098-133">Feature engineering</span></span>

<span data-ttu-id="16098-134">特徴エンジニアリングは、一連の[特徴](#feature)の定義、および使用可能な事象データから特徴ベクトルを生成する (特徴抽出) ソフトウェアの開発を含むプロセスです。</span><span class="sxs-lookup"><span data-stu-id="16098-134">Feature engineering is the process that involves defining a set of [features](#feature) and developing software that produces feature vectors from available phenomenon data, i.e., feature extraction.</span></span> <span data-ttu-id="16098-135">詳しくは、Wikipedia の[特徴エンジニアリング](https://en.wikipedia.org/wiki/Feature_engineering)の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16098-135">For more information, see the [Feature engineering](https://en.wikipedia.org/wiki/Feature_engineering) article on Wikipedia.</span></span>

## <a name="f-score"></a><span data-ttu-id="16098-136">F 値</span><span class="sxs-lookup"><span data-stu-id="16098-136">F-score</span></span>

<span data-ttu-id="16098-137">[分類](#classification)における評価メトリックであり、[精度](#precision)と[再現率](#recall)の調和平均を取ります。</span><span class="sxs-lookup"><span data-stu-id="16098-137">In [classification](#classification), an evaluation metric that balances [precision](#precision) and [recall](#recall).</span></span>

## <a name="hyperparameter"></a><span data-ttu-id="16098-138">ハイパーパラメーター</span><span class="sxs-lookup"><span data-stu-id="16098-138">Hyperparameter</span></span>

<span data-ttu-id="16098-139">機械学習アルゴリズムのパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="16098-139">A parameter of a machine learning algorithm.</span></span> <span data-ttu-id="16098-140">例として、デシジョン フォレストにおける学習するツリー数や勾配降下アルゴリズムにおけるステップ サイズなどがあります。</span><span class="sxs-lookup"><span data-stu-id="16098-140">Examples include the number of trees to learn in a decision forest or the step size in a gradient descent algorithm.</span></span> <span data-ttu-id="16098-141">*ハイパーパラメーター*の値は、モデルのトレーニング前に設定され、予測関数のパラメーターを検出するプロセスを管理します。例として、デシジョン ツリーにおける比較ポイントや線形回帰モデルにおける重みなどがあります。</span><span class="sxs-lookup"><span data-stu-id="16098-141">Values of *Hyperparameters* are set before training the model and govern the process of finding the parameters of the prediction function, for example, the comparison points in a decision tree or the weights in a linear regression model.</span></span> <span data-ttu-id="16098-142">詳しくは、Wikipedia の[ハイパーパラメーター](https://en.wikipedia.org/wiki/Hyperparameter_(machine_learning))の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16098-142">For more information, see the [Hyperparameter](https://en.wikipedia.org/wiki/Hyperparameter_(machine_learning)) article on Wikipedia.</span></span>

## <a name="label"></a><span data-ttu-id="16098-143">group1</span><span class="sxs-lookup"><span data-stu-id="16098-143">Label</span></span>

<span data-ttu-id="16098-144">機械学習モデルで予測される要素です。</span><span class="sxs-lookup"><span data-stu-id="16098-144">The element to be predicted with the machine learning model.</span></span> <span data-ttu-id="16098-145">たとえば、犬種や将来の株価などです。</span><span class="sxs-lookup"><span data-stu-id="16098-145">For example, the breed of dog or a future stock price.</span></span>

## <a name="log-loss"></a><span data-ttu-id="16098-146">対数損失</span><span class="sxs-lookup"><span data-stu-id="16098-146">Log loss</span></span>

<span data-ttu-id="16098-147">[分類](#classification)における評価メトリックであり、分類子の正確度を示します。</span><span class="sxs-lookup"><span data-stu-id="16098-147">In [classification](#classification), an evaluation metric that characterizes the accuracy of a classifier.</span></span> <span data-ttu-id="16098-148">対数損失が小さいほど、分類子の正確度が高くなります。</span><span class="sxs-lookup"><span data-stu-id="16098-148">The smaller log loss is, the more accurate a classifier is.</span></span>

## <a name="mean-absolute-error-mae"></a><span data-ttu-id="16098-149">平均絶対誤差 (MAE)</span><span class="sxs-lookup"><span data-stu-id="16098-149">Mean absolute error (MAE)</span></span>

<span data-ttu-id="16098-150">[回帰](#regression)における評価メトリックであり、すべてのモデルの誤差の平均です。モデルの誤差とは、予測された[ラベル](#label)値と正確なラベル値の間の距離です。</span><span class="sxs-lookup"><span data-stu-id="16098-150">In [regression](#regression), an evaluation metric that is the average of all the model errors, where model error is the distance between the predicted [label](#label) value and the correct label value.</span></span>

## <a name="model"></a><span data-ttu-id="16098-151">モデル</span><span class="sxs-lookup"><span data-stu-id="16098-151">Model</span></span>

<span data-ttu-id="16098-152">従来的に予測関数のパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="16098-152">Traditionally, the parameters for the prediction function.</span></span> <span data-ttu-id="16098-153">たとえば、線形回帰モデルにおける重みやデシジョン ツリーにおける分割ポイントなどがあります。</span><span class="sxs-lookup"><span data-stu-id="16098-153">For example, the weights in a linear regression model or the split points in a decision tree.</span></span> <span data-ttu-id="16098-154">ML.NET では、ドメイン オブジェクト (画像、テキストなど) の[ラベル](#label)の予測に必要なすべての情報がモデルに含まれます。</span><span class="sxs-lookup"><span data-stu-id="16098-154">In ML.NET, a model contains all the information necessary to predict the [label](#label) of a domain object (for example, image or text).</span></span> <span data-ttu-id="16098-155">つまり、ML.NET モデルには、必要な特徴付けのステップと予測関数のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="16098-155">This means that ML.NET models include the featurization steps necessary as well as the parameters for the prediction function.</span></span>

## <a name="multiclass-classification"></a><span data-ttu-id="16098-156">多クラス分類</span><span class="sxs-lookup"><span data-stu-id="16098-156">Multiclass classification</span></span>

<span data-ttu-id="16098-157">[ラベル](#label)が 3 つ以上のクラスのうちの 1 つである[分類](#classification)です。</span><span class="sxs-lookup"><span data-stu-id="16098-157">A [classification](#classification) case where the [label](#label) is one out of three or more classes.</span></span> <span data-ttu-id="16098-158">詳細については、トピック「[機械学習のタスク](tasks.md)」のセクション「[多クラス分類](tasks.md#multiclass-classification)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16098-158">For more information, see the [Multiclass classification](tasks.md#multiclass-classification) section of the [Machine learning tasks](tasks.md) topic.</span></span>

## <a name="n-gram"></a><span data-ttu-id="16098-159">N グラム</span><span class="sxs-lookup"><span data-stu-id="16098-159">N-gram</span></span>

<span data-ttu-id="16098-160">テキスト データの特徴抽出スキームです。N 個の単語のシーケンスが[特徴](#feature)値になります。</span><span class="sxs-lookup"><span data-stu-id="16098-160">A feature extraction scheme for text data: any sequence of N words turns into a [feature](#feature) value.</span></span>

## <a name="numerical-feature-vector"></a><span data-ttu-id="16098-161">数値特徴ベクトル</span><span class="sxs-lookup"><span data-stu-id="16098-161">Numerical feature vector</span></span>

<span data-ttu-id="16098-162">数値でのみ構成される[特徴](#feature)ベクトルです。</span><span class="sxs-lookup"><span data-stu-id="16098-162">A [feature](#feature) vector consisting only of numerical values.</span></span> <span data-ttu-id="16098-163">これは `double[]` に似ています。</span><span class="sxs-lookup"><span data-stu-id="16098-163">This is similar to `double[]`.</span></span>

## <a name="pipeline"></a><span data-ttu-id="16098-164">パイプライン</span><span class="sxs-lookup"><span data-stu-id="16098-164">Pipeline</span></span>

<span data-ttu-id="16098-165">モデルをデータ セットに適合させるために必要なすべての操作です。</span><span class="sxs-lookup"><span data-stu-id="16098-165">All of the operations needed to fit a model to a data set.</span></span> <span data-ttu-id="16098-166">パイプラインは、データのインポート、変換、特徴付け、および学習の各ステップで構成されます。</span><span class="sxs-lookup"><span data-stu-id="16098-166">A pipeline consists of data import, transformation, featurization, and learning steps.</span></span> <span data-ttu-id="16098-167">トレーニングが完了したパイプラインがモデルになります。</span><span class="sxs-lookup"><span data-stu-id="16098-167">Once a pipeline is trained, it turns into a model.</span></span>

## <a name="precision"></a><span data-ttu-id="16098-168">有効桁数</span><span class="sxs-lookup"><span data-stu-id="16098-168">Precision</span></span>

<span data-ttu-id="16098-169">[分類](#classification)におけるクラスの精度は、そのクラスに属していると正確に予測された項目の数を、クラスに属していると予測された項目の総数で割ったものです。</span><span class="sxs-lookup"><span data-stu-id="16098-169">In [classification](#classification), the precision for a class is the number of items correctly predicted as belonging to that class divided by the total number of items predicted as belonging to the class.</span></span>

## <a name="recall"></a><span data-ttu-id="16098-170">再現率</span><span class="sxs-lookup"><span data-stu-id="16098-170">Recall</span></span>

<span data-ttu-id="16098-171">[分類](#classification)におけるクラスの再現率は、そのクラスに属していると正確に予測された項目の数を、実際にクラスに属している項目の総数で割ったものです。</span><span class="sxs-lookup"><span data-stu-id="16098-171">In [classification](#classification), the recall for a class is the number of items correctly predicted as belonging to that class divided by the total number of items that actually belong to the class.</span></span>

## <a name="regression"></a><span data-ttu-id="16098-172">回帰</span><span class="sxs-lookup"><span data-stu-id="16098-172">Regression</span></span>

<span data-ttu-id="16098-173">出力が実際の値 (たとえば、倍精度) である[教師あり機械学習](#supervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="16098-173">A [supervised machine learning](#supervised-machine-learning) task where the output is a real value, for example, double.</span></span> <span data-ttu-id="16098-174">例として、株価の予測などがあります。</span><span class="sxs-lookup"><span data-stu-id="16098-174">Examples include predicting stock prices.</span></span> <span data-ttu-id="16098-175">詳細については、トピック「[機械学習のタスク](tasks.md)」のセクション「[回帰](tasks.md#regression)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16098-175">For more information, see the [Regression](tasks.md#regression) section of the [Machine learning tasks](tasks.md) topic.</span></span>

## <a name="relative-absolute-error"></a><span data-ttu-id="16098-176">相対絶対誤差</span><span class="sxs-lookup"><span data-stu-id="16098-176">Relative absolute error</span></span>

<span data-ttu-id="16098-177">[回帰](#regression)における評価メトリックであり、すべての絶対誤差の合計を、正確な[ラベル](#label)値とすべての正確なラベル値の平均との間の距離の合計で割ったものです。</span><span class="sxs-lookup"><span data-stu-id="16098-177">In [regression](#regression), an evaluation metric that is the sum of all absolute errors divided by the sum of distances between correct [label](#label) values and the average of all correct label values.</span></span>

## <a name="relative-squared-error"></a><span data-ttu-id="16098-178">相対平方誤差</span><span class="sxs-lookup"><span data-stu-id="16098-178">Relative squared error</span></span>

<span data-ttu-id="16098-179">[回帰](#regression)における評価メトリックであり、すべての平方絶対誤差の合計を、正確な[ラベル](#label)値とすべての正確なラベル値の平均との間の平方距離の合計で割ったものです。</span><span class="sxs-lookup"><span data-stu-id="16098-179">In [regression](#regression), an evaluation metric that is the sum of all squared absolute errors divided by the sum of squared distances between correct [label](#label) values and the average of all correct label values.</span></span>

## <a name="root-of-mean-squared-error-rmse"></a><span data-ttu-id="16098-180">平均平方誤差の平方根 (RMSE)</span><span class="sxs-lookup"><span data-stu-id="16098-180">Root of mean squared error (RMSE)</span></span>

<span data-ttu-id="16098-181">[回帰](#regression)における評価メトリックであり、誤差を 2 乗した値の平均値の平方根です。</span><span class="sxs-lookup"><span data-stu-id="16098-181">In [regression](#regression), an evaluation metric that is the square root of the average of the squares of the errors.</span></span>

## <a name="supervised-machine-learning"></a><span data-ttu-id="16098-182">教師あり機械学習</span><span class="sxs-lookup"><span data-stu-id="16098-182">Supervised machine learning</span></span>

<span data-ttu-id="16098-183">機械学習の 1 つの手法であり、目的となるモデルが未知のデータのラベルを予測します。</span><span class="sxs-lookup"><span data-stu-id="16098-183">A subclass of machine learning in which a desired model predicts the label for yet-unseen data.</span></span> <span data-ttu-id="16098-184">例として、分類、回帰、構造化予測などがあります。</span><span class="sxs-lookup"><span data-stu-id="16098-184">Examples include classification, regression, and structured prediction.</span></span> <span data-ttu-id="16098-185">詳しくは、Wikipedia の[教師あり学習](https://en.wikipedia.org/wiki/Supervised_learning)の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16098-185">For more information, see the  [Supervised learning](https://en.wikipedia.org/wiki/Supervised_learning) article on Wikipedia.</span></span>

## <a name="training"></a><span data-ttu-id="16098-186">トレーニング</span><span class="sxs-lookup"><span data-stu-id="16098-186">Training</span></span>

<span data-ttu-id="16098-187">特定のトレーニング データ セットの[モデル](#model)を識別するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="16098-187">The process of identifying a [model](#model) for a given training data set.</span></span> <span data-ttu-id="16098-188">線形モデルの場合、重みの検出を意味します。</span><span class="sxs-lookup"><span data-stu-id="16098-188">For a linear model, this means finding the weights.</span></span> <span data-ttu-id="16098-189">ツリーの場合、分割ポイントの識別が含まれます。</span><span class="sxs-lookup"><span data-stu-id="16098-189">For a tree, it involves the identifying the split points.</span></span>

## <a name="transform"></a><span data-ttu-id="16098-190">変換</span><span class="sxs-lookup"><span data-stu-id="16098-190">Transform</span></span>

<span data-ttu-id="16098-191">データを変換する[パイプライン](#pipeline) コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="16098-191">A [pipeline](#pipeline) component that transforms data.</span></span> <span data-ttu-id="16098-192">たとえば、数字のテキストからベクトルへの変換などです。</span><span class="sxs-lookup"><span data-stu-id="16098-192">For example, from text to vector of numbers.</span></span>

## <a name="unsupervised-machine-learning"></a><span data-ttu-id="16098-193">教師なし機械学習</span><span class="sxs-lookup"><span data-stu-id="16098-193">Unsupervised machine learning</span></span>

<span data-ttu-id="16098-194">機械学習の 1 つの手法であり、目的となるモデルがデータの隠された (潜在的な) 構造を検出します。</span><span class="sxs-lookup"><span data-stu-id="16098-194">A subclass of machine learning in which a desired model finds hidden (or latent) structure in data.</span></span> <span data-ttu-id="16098-195">例として、クラスタリング、トピック モデリング、次元削減などがあります。</span><span class="sxs-lookup"><span data-stu-id="16098-195">Examples include clustering, topic modeling, and dimensionality reduction.</span></span> <span data-ttu-id="16098-196">詳しくは、Wikipedia の[教師なし学習](https://en.wikipedia.org/wiki/Unsupervised_learning)の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16098-196">For more information, see the [Unsupervised learning](https://en.wikipedia.org/wiki/Unsupervised_learning) article on Wikipedia.</span></span>
