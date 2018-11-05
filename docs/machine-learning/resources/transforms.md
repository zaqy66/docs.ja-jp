---
title: データ変換
description: ML.NET でサポートされているさまざまなデータ変換について説明します。
ms.date: 10/16/2018
ms.openlocfilehash: 5df4598de6fcd08689d72c378f51d792860ef49c
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50187742"
---
# <a name="data-transforms"></a>データ変換

次の表には、ML.NET でサポートされるすべてのデータ変換の情報が含まれています (データ変換の種類を選択すると、対応する表に移動します)。

* [カテゴリ](#categorical)
* [結合と分離](#combiners-and-segregators)
* [フィーチャーの選択](#feature-selection)
* [フィーチャライザー](#featurizers)
* [ラベルの解析](#label-parsing)
* [欠損値](#missing-values)
* [正規化](#normalization)
* [行フィルター](#row-filters)
* [スキーマ](#schema)
* [テキスト処理と特徴付け](#text-processing-and-featurization)
* [その他](#miscellaneous)

> [!NOTE]
> ML.NET は現在プレビュー段階です。 現時点では、すべてのデータ変換がサポートされているわけではありません。 特定の変換に対するご要望を送信するには、[dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues) GitHub リポジトリで問題をオープンしてください。

## <a name="categorical"></a>カテゴリ

| 変換 | 定義 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.CategoricalHashOneHotVectorizer> | ハッシュ ベースのエンコードを使用してカテゴリ変数をエンコードします。 |
| <xref:Microsoft.ML.Legacy.Transforms.CategoricalOneHotVectorizer> | 用語の辞書に基づき、ワンホット エンコードを使用して、カテゴリ変数をエンコードします。 |

## <a name="combiners-and-segregators"></a>結合と分離

| 変換 | 定義 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.CombinerByContiguousGroupId> | 連続するグループ ID に基づいて、スカラー列の値をベクターにグループ化します。 |
| <xref:Microsoft.ML.Legacy.Transforms.FeatureCombiner> | すべてのフィーチャーを 1 つのフィーチャーの列に結合します。 |
| <xref:Microsoft.ML.Legacy.Transforms.ManyHeterogeneousModelCombiner> | TransformModels のシーケンスと PredictorModel を 1 つの PredictorModel に結合します。 |
| <xref:Microsoft.ML.Legacy.Transforms.ModelCombiner> | TransformModels のシーケンスを 1 つのモデルに結合します。 |
| <xref:Microsoft.ML.Legacy.Transforms.Segregator> | ベクター列をグループ解除して行のシーケンスにします。グループ化変換の逆です。 |
| <xref:Microsoft.ML.Legacy.Transforms.TwoHeterogeneousModelCombiner> | TransformModel と PredictorModel を 1 つの PredictorModel に結合します。 |

## <a name="feature-selection"></a>フィーチャーの選択

| 変換 | 定義 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.FeatureSelectorByCount> | 既定値以外の値の数がしきい値以上のスロットを選択します。 |
| <xref:Microsoft.ML.Legacy.Transforms.FeatureSelectorByMutualInformation> | ラベル列を持つ相互情報によって指定されたすべての列にわたって、最上位の k スロットを選択します。 |

## <a name="featurizers"></a>フィーチャライザー

| 変換 | 定義 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.HashConverter> | 列の値をハッシュに変換します。 この変換では、数値とテキストの両方の入力と、単一値とベクター値の両方の列を受け入れます。 |
| <xref:Microsoft.ML.Legacy.Transforms.TreeLeafFeaturizer> | ツリー アンサンブルをトレーニングするか、ファイルから読み込んで、数値特徴ベクトルを 3 つの出力にマップします。1. ツリー アンサンブルの個別のツリー出力を含むベクター。 2. ツリー アンサンブル内で特徴ベクトルが位置するリーフを示すベクター。 3. ツリー アンサンブル内で特徴ベクトルが位置するパスを示すベクター。 モデル ファイルとトレーナーの両方が指定されている場合、ベクターではモデル ファイルが使用されます。 どちらも指定されていない場合、ベクターによって既定の FastTree モデルがトレーニングされます。 これでキー ラベルを処理するには、必要に応じて順序を変更したインデックスに対する回帰モデルをトレーニングします。 |

## <a name="label-parsing"></a>ラベルの解析

| 変換 | 定義 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.Dictionarizer> | 入力値 (単語、数字など) をディクショナリ内のインデックスに変換します。 |
| <xref:Microsoft.ML.Legacy.Transforms.LabelColumnKeyBooleanConverter> | ラベルを分類に適したものにするため、キーまたはブール値 (必要な場合) に変換します。 |
| <xref:Microsoft.ML.Legacy.Transforms.LabelIndicator> | OVA で使用される再マッパーにラベル付けします。 |
| <xref:Microsoft.ML.Legacy.Transforms.LabelToFloatConverter> | ラベルを回帰に最適なものにするため、float 型に変換します。 |
| <xref:Microsoft.ML.Legacy.Transforms.PredictedLabelColumnOriginalValueConverter> | 予測されるラベル列が bool 型である場合を除き、元の値に変換します。 |

## <a name="missing-values"></a>欠損値

| 変換 | 定義 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValueHandler> | 欠損値は、既定値または平均値/最小値/最大値 (テキスト以外の列の場合のみ) のいずれかで置き換えることで処理します。 インジケーター列は、入力列の型が数値の場合には、必要に応じて連結できます。 |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValueIndicator> | 入力列と同じ数のスロットを持つブール値出力列を作成します。この場合、入力列に値がない場合、出力値は true です。 |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValuesDropper> | ベクター列から NA を削除します。 |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValuesRowDropper> | 欠損値を含む行を除外します。 |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValueSubstitutor> | 入力列と同じ型とサイズの出力列を作成します。この場合、欠損値は既定値または平均値/最小値/最大値 (テキスト以外の列の場合のみ) のいずれかで置き換えられます。 |

## <a name="normalization"></a>正規化

| 変換 | 定義 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.BinNormalizer> | 値が等密度のビンに割り当てられ、値がその bin_number / number_of_bins にマップされます。 |
| <xref:Microsoft.ML.Legacy.Transforms.ConditionalNormalizer> | 必要な場合にのみ、列を正規化します。 |
| <xref:Microsoft.ML.Legacy.Transforms.GlobalContrastNormalizer> | 入力値に対してグローバル コントラスト正規化を実行します。Y = (s * X - M) / D。ここで、s はスケール、M は平均、D は L2 norm または標準偏差です。 | 
| <xref:Microsoft.ML.Legacy.Transforms.LogMeanVarianceNormalizer> | データの対数の計算された平均と分散に基づいて、データを正規化します。 |
| <xref:Microsoft.ML.Legacy.Transforms.LpNormalizer> | ベクター (行) を単位 norm (L2、L1 または LInf) に再スケーリングすることで、個別に正規化します。 ベクター X で、Y = (X - M) / D の演算を実行します。ここで、M は平均、D は L2 norm、L1 norm、または LInf norm のいずれかです。 |
| <xref:Microsoft.ML.Legacy.Transforms.MeanVarianceNormalizer> | データの計算された平均と分散に基づいて、データを正規化します。 |
| <xref:Microsoft.ML.Legacy.Transforms.MinMaxNormalizer> | データの観察された最小値と最大値に基づいて、データを正規化します。 |

## <a name="row-filters"></a>行フィルター

| 変換 | 定義 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.RowRangeFilter> | Single、Double または Key (連続) 型の列で dataview をフィルター処理します。 指定した最小/最大の範囲内に値を保持します。 NaNs は常に除外されます。入力が Key 型の場合、最小/最大は値の数の割合と見なされます。 |
| <xref:Microsoft.ML.Legacy.Transforms.RowSkipAndTakeFilter> | 任意のオフセットで行のサブセットへの入力を制限することができます。 データのページングを実装するために使用できます。 |
| <xref:Microsoft.ML.Legacy.Transforms.RowSkipFilter> | 行の数をスキップすることで行のサブセットへの入力を制限することができます。 |
| <xref:Microsoft.ML.Legacy.Transforms.RowTakeFilter> | 最初の N 行を取得することで行のサブセットへの入力を制限することができます。 |

## <a name="schema"></a>Schema

| 変換 | 定義 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnConcatenator> | 項目の種類が同じ 2 つの列を連結します。 |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnCopier> | データセットから列を複製します。|
| <xref:Microsoft.ML.Legacy.Transforms.ColumnDropper> | データセットから列を削除します。 |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnSelector> | 列のセットを選択し、それ以外のすべてを削除します。 |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnTypeConverter> | 標準の変換を使用して、列を別の型に変換します。 |
| <xref:Microsoft.ML.Legacy.Transforms.KeyToTextConverter> | KeyToValueTransform では、KeyValues メタデータを使用してキー インデックスを KeyValues メタデータ内の対応する値にマップします。 |
| <xref:Microsoft.ML.Legacy.Transforms.NGramTranslator> | キーの指定のベクターで、n-gram のカウントのバッグ (長さ 1-n の連続する値のシーケンス) が生成されます。 n-gram のディクショナリをビルドし、ディクショナリの ID をバッグのインデックスとして使用することでこれを行います。 | 
| <xref:Microsoft.ML.Legacy.Transforms.OptionalColumnCreator> | 逆シリアル化にソース列が存在しない場合は、適切な型と既定値を持つ列を作成します。 |

## <a name="text-processing-and-featurization"></a>テキスト処理と特徴付け

| 変換 | 定義 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.CharacterTokenizer> | テキストが文字のシーケンスと見なされる文字指向のトークナイザー。 |
| <xref:Microsoft.ML.Legacy.Transforms.TextFeaturizer> | テキスト ドキュメントのコレクションを数値特徴ベクトルにする変換。 特徴ベクトルは、特定のトークン化されたテキストの (単語や文字) n-gram の正規化されたカウントです。 |
| <xref:Microsoft.ML.Legacy.Transforms.TextToKeyConverter> | 入力値 (単語、数字など) をディクショナリ内のインデックスに変換します。 |
| <xref:Microsoft.ML.Legacy.Transforms.WordEmbeddings> | 事前にトレーニングされたモデルを使用して、テキスト トークンを数値ベクターに変える変換。 この手法の詳細については、Wikipedia の [Word embedding](https://en.wikipedia.org/wiki/Word_embedding) のページ (英語) を参照してください。 |
| <xref:Microsoft.ML.Legacy.Transforms.WordTokenizer> | この変換への入力はテキストで、出力は元のテキスト内の単語 (トークン) を含む文字列のベクターです。 区切り記号は空白文字ですが、他の任意の文字 (または複数の文字) を指定することもできます。 |

## <a name="miscellaneous"></a>その他

| 変換 | 定義 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.ApproximateBootstrapSampler> | ブートストラップ サンプリングを概算します。 |
| <xref:Microsoft.ML.Legacy.Transforms.BinaryPredictionScoreColumnsRenamer> | バイナリの予測の場合、PredictedLabel 列と Score 列の名前を、正のクラスの名前を含めるように変更します。|
| <xref:Microsoft.ML.Legacy.Transforms.DataCache> | 指定されたキャッシュ オプションを使用してキャッシュします。 |
| <xref:Microsoft.ML.Legacy.Transforms.DatasetScorer> | 予測モデルを使用してデータセットをスコア付けします。 |
| <xref:Microsoft.ML.Legacy.Transforms.DatasetTransformScorer> | 変換モデルを使用してデータセットをスコア付けします。 |
| <xref:Microsoft.ML.Legacy.Transforms.NoOperation> | 処理を行いません。 |
| <xref:Microsoft.ML.Legacy.Transforms.RandomNumberGenerator> | 生成された数字シーケンスを使用して列を追加します。 |
| <xref:Microsoft.ML.Legacy.Transforms.ScoreColumnSelector> | 最後のスコア列と、引数で指定された追加の列のみを選択します。 |
| <xref:Microsoft.ML.Legacy.Transforms.Scorer> | 予測モデルを変換モデルに変えます。 |
| <xref:Microsoft.ML.Legacy.Transforms.SentimentAnalyzer> | 事前にトレーニングされたセンチメント モデルを使用して、入力文字列をスコア付けします。 |
| <xref:Microsoft.ML.Legacy.Transforms.TrainTestDatasetSplitter> | データセットをトレーニングとテストのセットに分割します。 |
