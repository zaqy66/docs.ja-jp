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
# <a name="machine-learning-tasks-in-mlnet"></a>ML.NET での機械学習のタスク

機械学習モデルを構築する場合は、データを使用して実現したい目的を最初に定義する必要があります。 その後で、状況に適した機械学習のタスクを選択できます。 選択可能な機械学習のさまざまなタスクといくつかの一般的なユース ケースについて以下で説明します。

> [!NOTE]
> ML.NET は現在プレビュー段階です。 現時点では、機械学習のタスクがすべてサポートされているわけではありません。 特定のタスクに対するご要望を送信するには、[dotnet/machinelearning リポジトリ](https://github.com/dotnet/machinelearning/issues)で問題をオープンしてください。

## <a name="binary-classification"></a>二項分類

データのインスタンスが 2 つのうちのどちらのクラス (カテゴリ) に属しているかを予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。 分類アルゴリズムの入力はラベル付けされた一連のサンプルであり、各ラベルは整数 0 または 1 です。 二項分類アルゴリズムの出力は分類子であり、ラベルのない新しいインスタンスのクラスを予測するために使用できます。 二項分類のシナリオの例を次に示します。

* [Twitter コメントのセンチメントが "肯定的" か "否定的" かを理解する](../tutorials/sentiment-analysis.md)。
* 患者が特定の病気であるかどうかを診断する。
* 電子メールを "スパム" としてマークするかどうかを決定する。
* 写真に犬または果物が含まれているかどうかを決定する。

詳しくは、Wikipedia の[二項分類](https://en.wikipedia.org/wiki/Binary_classification)の記事を参照してください。

二項分類で推奨される学習器:

* AveragedPerceptronTrainer
* StochasticGradientDescentClassificationTrainer
* LightGbmBinaryTrainer
* FastTreeBinaryClassificationTrainer
* SymSgdClassificationTrainer

### <a name="binary-classification-learners"></a>二項分類学習器

二項分類タスクでは、次の学習器を利用できます。

* [AveragedPerceptronTrainer](xref:Microsoft.ML.Trainers.Online.AveragedPerceptronTrainer)
* [BinaryClassificationGamTrainer](xref:Microsoft.ML.Trainers.FastTree.BinaryClassificationGamTrainer)
* [FastForestClassification](xref:Microsoft.ML.Trainers.FastTree.FastForestClassification)
* [FastTreeBinaryClassificationTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer)
* [FieldAwareFactorizationMachineTrainer](xref:Microsoft.ML.Runtime.FactorizationMachine.FieldAwareFactorizationMachineTrainer)
* [LightGbmBinaryTrainer](xref:Microsoft.ML.Runtime.LightGBM.LightGbmBinaryTrainer)
* [LinearSvm](xref:Microsoft.ML.Trainers.Online.LinearSvm)
* [PriorTrainer](xref:Microsoft.ML.Trainers.PriorTrainer)
* [RandomTrainer](xref:Microsoft.ML.Trainers.RandomTrainer)
* [StochasticGradientDescentClassificationTrainer](xref:Microsoft.ML.Trainers.StochasticGradientDescentClassificationTrainer)
* [SymSgdClassificationTrainer](xref:Microsoft.ML.Trainers.SymSgd.SymSgdClassificationTrainer)

## <a name="multiclass-classification"></a>多クラス分類

データのインスタンスのクラス (カテゴリ) を予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。 分類アルゴリズムの入力は、ラベル付けされた一連のサンプルです。 各ラベルは、通常、テキストとして開始されます。 その後、TermTransform を経由してキー (数値) 型に変換されます。 分類アルゴリズムの出力は分類子であり、ラベルのない新しいインスタンスのクラスを予測するために使用できます。 多クラス分類のシナリオの例を次に示します。

* "シベリアン ハスキー"、"ゴールデン レトリバー"、"プードル" などの犬種を特定する。
* 映画のレビューが "肯定的"、"中立"、"否定的" のどれかを理解する。
* ホテルのレビューを "立地"、"価格"、"清潔さ" などに分類する。

詳しくは、Wikipedia の[多クラス分類](https://en.wikipedia.org/wiki/Multiclass_classification)の記事を参照してください。

多クラスで推奨される学習器:

* OVA-AveragedPerceptronTrainer
* SdcaMultiClassTrainer
* LightGbmMulticlassTrainer
* OVA-FastTreeBinaryClassificationTrainer

>[!NOTE]
>OVA と PKPD では、多クラス データセットに対して機能するように[二項分類学習器](#binary-classification)がアップグレードされています。 詳細については、[Wikipedia] (https://en.wikipedia.org/wiki/Multiclass_classification#One-vs.-rest)) を参照してください。

### <a name="multiclass-classification-learners"></a>多クラス分類学習器

多クラス分類タスクでは、次の学習器を利用できます。

* [LightGbmMulticlassTrainer](xref:Microsoft.ML.Runtime.LightGBM.LightGbmMulticlassTrainer)
* [MetaMulticlassTrainer<TTransformer,TModel>](xref:Microsoft.ML.Runtime.Learners.MetaMulticlassTrainer%602)
* [MultiClassClassificationTrainers](xref:Microsoft.ML.Trainers.MultiClassClassificationTrainers)
* [MultiClassNaiveBayesTrainer](xref:Microsoft.ML.Trainers.MultiClassNaiveBayesTrainer)
* [Ova](xref:Microsoft.ML.Trainers.Ova)
* [Pkpd](xref:Microsoft.ML.Trainers.Pkpd)
* [SdcaMultiClassTrainer](xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer)

## <a name="regression"></a>回帰

関連する一連の特徴からラベルの値を予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。 ラベルには任意の実際の値を使用できます。分類タスクのように有限の値のセットから取得するものではありません。 回帰アルゴリズムでは、ラベルに関連する特徴におけるラベルの依存関係をモデル化して、特徴の値が変化するとラベルがどのように変化するかを判断します。 回帰アルゴリズムの入力は、既知の値のラベルが付いた一連のサンプルです。 回帰アルゴリズムの出力は関数であり、新しい入力特徴のセットのラベル値を予測するために使用できます。 回帰のシナリオの例を次に示します。

* 住宅の属性 (寝室数、立地、規模など) に基づいて住宅価格を予測する。
* 履歴データと現在の市場動向に基づいて将来の株価を予測する。
* 広告予算に基づいて製品の売り上げを予測する。

回帰で推奨される学習器:

* FastTreeTweedieTrainer 
* LightGbmRegressorTrainer 
* SdcaRegressionTrainer 
* FastTreeRegressionTrainer

### <a name="regression-learners"></a>回帰学習器

回帰タスクでは、次の学習器を利用できます。

* [FastTreeRegressionTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeRegressionTrainer)
* [FastTreeRegressionFastTreeTrainer](xref:Microsoft.ML.Runtime.FastTreeRegressionFastTreeTrainer)
* [FastTreeTweedieRegressionFastTreeTrainer](xref:Microsoft.ML.Runtime.FastTreeTweedieRegressionFastTreeTrainer)
* [FastTreeTweedieTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeTweedieTrainer)
* [LightGbmRegressorTrainer](xref:Microsoft.ML.Runtime.LightGBM.LightGbmRegressorTrainer)
* [LogisticRegression](xref:Microsoft.ML.Runtime.Learners.LogisticRegression)
* [OlsLinearRegressionTrainer](xref:Microsoft.ML.Trainers.HalLearners.OlsLinearRegressionTrainer)
* [OnlineGradientDescentTrainer](xref:Microsoft.ML.Trainers.Online.OnlineGradientDescentTrainer)
* [PoissonRegression](xref:Microsoft.ML.Trainers.PoissonRegression)
* [RegressionGamTrainer](xref:Microsoft.ML.Trainers.FastTree.RegressionGamTrainer)
* [SdcaRegressionTrainer](xref:Microsoft.ML.Trainers.SdcaRegressionTrainer)
* [FastTree.SingleTrainer](xref:Microsoft.ML.Trainers.FastTree.SingleTrainer)
* [LightGBM.SingleTrainer](xref:Microsoft.ML.Runtime.LightGBM.SingleTrainer)

## <a name="clustering"></a>クラスタリング

データのインスタンスを、同様の特性を持つクラスタにグループ化するために使用する[教師なし機械学習](glossary.md#unsupervised-machine-learning)タスクです。 また、閲覧や単純な観測では論理的に導き出せない可能性のあるデータ セットにおける関係をクラスタリングを使用して識別することもできます。 クラスタリング アルゴリズムの入力と出力は、選択した方法によって異なります。 分布、重心、結合性、または密度に基づくアプローチを利用できます。 現在、ML.NET では、K 平均法によるクラスタリングを使用した重心に基づくアプローチをサポートしています。 クラスタリングのシナリオの例を次に示します。

* ホテル選択の傾向と特性に基づいてホテルの宿泊客のセグメントを理解する。
* 対象を絞った広告キャンペーンの構築に役立つ顧客セグメントと統計データを特定する。
* 製造メトリックに基づいてインベントリを分類する。

### <a name="clustering-learners"></a>クラスタリング学習器

クラスタリング タスクでは、次の学習器を利用できます。

* [KMeansPlusPlusTrainer](xref:Microsoft.ML.Trainers.KMeans.KMeansPlusPlusTrainer)

## <a name="anomaly-detection"></a>異常検出

このタスクでは、主成分分析 (PCA) を使用して、異常検出モデルを作成します。 PCA に基づく異常分析は、有効なトランザクションなどの 1 つのクラスからトレーニング データを簡単に取得できるが、対象とする異常の十分なサンプルを取得するのが難しいシナリオでモデルを構築するのに役立ちます。

機械学習における確立された手法である PCA は、データの内部構造を明らかにし、データの分散を説明するために、調査データ分析で頻繁に使用されます。 PCA は、複数の変数が含まれるデータを分析することで機能します。 変数の相関を探し、結果内の差異を最も捕らえている値の合成を決定します。 これらの合成されたフィーチャー値を使用して、主成分と呼ばれる、よりコンパクトなフィーチャー空間が作成されます。

異常検出には、機械学習における多くの重要なタスクが含まれています。

* 不正な可能性があるトランザクションを識別します。
* ネットワークへの侵入が発生していることを示唆するパターンを学習します。
* 患者の異常なクラスターを検出します。
* システムに入力された値をチェックします。

異常とは定義上はまれに発生するイベントであるため、モデル化するために使用する代表的なデータ サンプルを収集するのは困難です。 このカテゴリに含まれるアルゴリズムは、不均衡なデータセットの使用によるモデルの構築とトレーニングという主要な課題に対処するように特別に設計されています。

### <a name="anomaly-detection-learners"></a>異常検出学習器

異常検出タスクでは、次の学習器を利用できます。

* [RandomizedPcaTrainer](xref:Microsoft.ML.Trainers.PCA.RandomizedPcaTrainer)

## <a name="ranking"></a>ランキング

ランキング タスクでは、ラベル付きのサンプルのセットからランカーが構築されます。 この例のセットは、特定の条件を使用してスコア付けできるインスタンス グループで構成されています。 順位付けのラベルは、インスタンスごとに {0、1、2、3, 4} です。  各インスタンスのスコアが不明である新しいインスタンス グループをランク付けするように、ランカーがトレーニングされます。 ML.NET のランキング学習器は、[機械が学習したランキング](https://en.wikipedia.org/wiki/Learning_to_rank)に基づいています。

### <a name="ranking-learners"></a>ランキング学習器

ランキング タスクでは、次の学習器を利用できます。

* [FastTreeRankingFastTreeTrainer](xref:Microsoft.ML.Runtime.FastTreeRankingFastTreeTrainer)
* [FastTreeRankingTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeRankingTrainer)
* [LightGbmRankingTrainer](xref:Microsoft.ML.Runtime.LightGBM.LightGbmRankingTrainer)

## <a name="recommendation"></a>レコメンデーション

レコメンデーション タスクによって、推奨される製品やサービスの一覧を作成できます。 ML.NET では、カタログ内に製品のレーティングの履歴データがある場合は、レコメンデーション用の[協調フィルタリング](https://en.wikipedia.org/wiki/Collaborative_filtering) アルゴリズムである[行列因子分解 (MF)](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29) が使用されます。 たとえば、ユーザーによる映画の採点の履歴データがあるときに、そのユーザーが次に見たいと思う映画を推薦できます。

### <a name="recommendation-learners"></a>レコメンデーション学習機

レコメンデーション タスクでは、次の学習器を利用できます。

* [MatrixFactorizationTrainer](xref:Microsoft.ML.Trainers.MatrixFactorizationTrainer)
* [MatrixFactorizationPredictionTransformer](xref:Microsoft.ML.Trainers.Recommender.MatrixFactorizationPredictionTransformer)
