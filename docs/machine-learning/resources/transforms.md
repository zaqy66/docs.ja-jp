---
title: データ変換
description: ML.NET でサポートされているさまざまなデータ変換について説明します。
ms.date: 08/08/2018
author: jralexander
ms.author: johalex
ms.openlocfilehash: 3c483f4a263052eb15435775a47f514893eee049
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2018
ms.locfileid: "43000865"
---
# <a name="data-transforms"></a><span data-ttu-id="2ac6a-103">データ変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-103">Data transforms</span></span>

<span data-ttu-id="2ac6a-104">次の表には、ML.NET でサポートされるすべてのデータ変換の情報が含まれています (データ変換の種類を選択すると、対応する表に移動します)。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-104">The following tables contain information about all of the data transforms supported in ML.NET (select the data transform type to navigate to the corresponding table):</span></span>

* [<span data-ttu-id="2ac6a-105">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="2ac6a-105">Categorical</span></span>](#categorical)
* [<span data-ttu-id="2ac6a-106">結合と分離</span><span class="sxs-lookup"><span data-stu-id="2ac6a-106">Combiners and segregators</span></span>](#combiners-and-segregators)
* [<span data-ttu-id="2ac6a-107">フィーチャーの選択</span><span class="sxs-lookup"><span data-stu-id="2ac6a-107">Feature selection</span></span>](#feature-selection)
* [<span data-ttu-id="2ac6a-108">フィーチャライザー</span><span class="sxs-lookup"><span data-stu-id="2ac6a-108">Featurizers</span></span>](#featurizers)
* [<span data-ttu-id="2ac6a-109">ラベルの解析</span><span class="sxs-lookup"><span data-stu-id="2ac6a-109">Label parsing</span></span>](#label-parsing)
* [<span data-ttu-id="2ac6a-110">欠損値</span><span class="sxs-lookup"><span data-stu-id="2ac6a-110">Missing Values</span></span>](#missing-values)
* [<span data-ttu-id="2ac6a-111">正規化</span><span class="sxs-lookup"><span data-stu-id="2ac6a-111">Normalization</span></span>](#normalization)
* [<span data-ttu-id="2ac6a-112">行フィルター</span><span class="sxs-lookup"><span data-stu-id="2ac6a-112">Row filters</span></span>](#row-filters)
* [<span data-ttu-id="2ac6a-113">スキーマ</span><span class="sxs-lookup"><span data-stu-id="2ac6a-113">Schema</span></span>](#schema)
* [<span data-ttu-id="2ac6a-114">テキスト処理と特徴付け</span><span class="sxs-lookup"><span data-stu-id="2ac6a-114">Text processing and featurization</span></span>](#text-processing-and-featurization)
* [<span data-ttu-id="2ac6a-115">その他</span><span class="sxs-lookup"><span data-stu-id="2ac6a-115">Miscellaneous</span></span>](#miscellaneous)

> [!NOTE]
> <span data-ttu-id="2ac6a-116">ML.NET は現在プレビュー段階です。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-116">ML.NET is currently in Preview.</span></span> <span data-ttu-id="2ac6a-117">現時点では、すべてのデータ変換がサポートされているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-117">Not all data transforms are currently supported.</span></span> <span data-ttu-id="2ac6a-118">特定の変換に対するご要望を送信するには、[dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues) GitHub リポジトリで問題をオープンしてください。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-118">To submit a request for a certain transform, open an issue in the [dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues) GitHub repository.</span></span>

## <a name="categorical"></a><span data-ttu-id="2ac6a-119">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="2ac6a-119">Categorical</span></span>

| <span data-ttu-id="2ac6a-120">変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-120">Transform</span></span> | <span data-ttu-id="2ac6a-121">定義</span><span class="sxs-lookup"><span data-stu-id="2ac6a-121">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CategoricalHashOneHotVectorizer> | <span data-ttu-id="2ac6a-122">ハッシュ ベースのエンコードを使用してカテゴリ変数をエンコードします。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-122">Encodes the categorical variable with hash-based encoding.</span></span> |
| <xref:Microsoft.ML.Transforms.CategoricalOneHotVectorizer> | <span data-ttu-id="2ac6a-123">用語の辞書に基づき、ワンホット エンコードを使用して、カテゴリ変数をエンコードします。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-123">Encodes the categorical variable with one-hot encoding based on a term dictionary.</span></span> |

## <a name="combiners-and-segregators"></a><span data-ttu-id="2ac6a-124">結合と分離</span><span class="sxs-lookup"><span data-stu-id="2ac6a-124">Combiners and segregators</span></span>

| <span data-ttu-id="2ac6a-125">変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-125">Transform</span></span> | <span data-ttu-id="2ac6a-126">定義</span><span class="sxs-lookup"><span data-stu-id="2ac6a-126">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CombinerByContiguousGroupId> | <span data-ttu-id="2ac6a-127">連続するグループ ID に基づいて、スカラー列の値をベクターにグループ化します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-127">Groups values of a scalar column into a vector based on a contiguous group ID.</span></span> |
| <xref:Microsoft.ML.Transforms.FeatureCombiner> | <span data-ttu-id="2ac6a-128">すべてのフィーチャーを 1 つのフィーチャーの列に結合します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-128">Combines all the features into one feature column.</span></span> |
| <xref:Microsoft.ML.Transforms.ManyHeterogeneousModelCombiner> | <span data-ttu-id="2ac6a-129">TransformModels のシーケンスと PredictorModel を 1 つの PredictorModel に結合します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-129">Combines a sequence of TransformModels and a PredictorModel into a single PredictorModel.</span></span> |
| <xref:Microsoft.ML.Transforms.ModelCombiner> | <span data-ttu-id="2ac6a-130">TransformModels のシーケンスを 1 つのモデルに結合します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-130">Combines a sequence of TransformModels into a single model.</span></span> |
| <xref:Microsoft.ML.Transforms.Segregator> | <span data-ttu-id="2ac6a-131">ベクター列をグループ解除して行のシーケンスにします。グループ化変換の逆です。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-131">Ungroups vector columns into sequences of rows; the inverse of Group transform.</span></span> |
| <xref:Microsoft.ML.Transforms.TwoHeterogeneousModelCombiner> | <span data-ttu-id="2ac6a-132">TransformModel と PredictorModel を 1 つの PredictorModel に結合します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-132">Combines a TransformModel and a PredictorModel into a single PredictorModel.</span></span> |

## <a name="feature-selection"></a><span data-ttu-id="2ac6a-133">フィーチャーの選択</span><span class="sxs-lookup"><span data-stu-id="2ac6a-133">Feature selection</span></span>

| <span data-ttu-id="2ac6a-134">変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-134">Transform</span></span> | <span data-ttu-id="2ac6a-135">定義</span><span class="sxs-lookup"><span data-stu-id="2ac6a-135">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.FeatureSelectorByCount> | <span data-ttu-id="2ac6a-136">既定値以外の値の数がしきい値以上のスロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-136">Selects the slots for which the count of non-default values is greater than or equal to a threshold.</span></span> |
| <xref:Microsoft.ML.Transforms.FeatureSelectorByMutualInformation> | <span data-ttu-id="2ac6a-137">ラベル列を持つ相互情報によって指定されたすべての列にわたって、最上位の k スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-137">Selects the top k slots across all specified columns ordered by their mutual information with the label column.</span></span> |

## <a name="featurizers"></a><span data-ttu-id="2ac6a-138">フィーチャライザー</span><span class="sxs-lookup"><span data-stu-id="2ac6a-138">Featurizers</span></span>

| <span data-ttu-id="2ac6a-139">変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-139">Transform</span></span> | <span data-ttu-id="2ac6a-140">定義</span><span class="sxs-lookup"><span data-stu-id="2ac6a-140">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.HashConverter> | <span data-ttu-id="2ac6a-141">列の値をハッシュに変換します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-141">Converts column values into hashes.</span></span> <span data-ttu-id="2ac6a-142">この変換では、数値とテキストの両方の入力と、単一値とベクター値の両方の列を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-142">This transform accepts both numeric and text inputs, both single and vector-valued columns.</span></span> |
| <xref:Microsoft.ML.Transforms.TreeLeafFeaturizer> | <span data-ttu-id="2ac6a-143">ツリー アンサンブルをトレーニングするか、ファイルから読み込んで、数値特徴ベクトルを 3 つの出力にマップします。1.</span><span class="sxs-lookup"><span data-stu-id="2ac6a-143">Trains a tree ensemble, or loads it from a file, then maps a numeric feature vector to three outputs: 1.</span></span> <span data-ttu-id="2ac6a-144">ツリー アンサンブルの個別のツリー出力を含むベクター。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-144">A vector containing the individual tree outputs of the tree ensemble.</span></span> <span data-ttu-id="2ac6a-145">2.</span><span class="sxs-lookup"><span data-stu-id="2ac6a-145">2.</span></span> <span data-ttu-id="2ac6a-146">ツリー アンサンブル内で特徴ベクトルが位置するリーフを示すベクター。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-146">A vector indicating the leaves that the feature vector falls on in the tree ensemble.</span></span> <span data-ttu-id="2ac6a-147">3.</span><span class="sxs-lookup"><span data-stu-id="2ac6a-147">3.</span></span> <span data-ttu-id="2ac6a-148">ツリー アンサンブル内で特徴ベクトルが位置するパスを示すベクター。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-148">A vector indicating the paths that the feature vector falls on in the tree ensemble.</span></span> <span data-ttu-id="2ac6a-149">モデル ファイルとトレーナーの両方が指定されている場合、ベクターではモデル ファイルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-149">If both a model file and a trainer are specified, the vector will use the model file.</span></span> <span data-ttu-id="2ac6a-150">どちらも指定されていない場合、ベクターによって既定の FastTree モデルがトレーニングされます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-150">If neither are specified, the vector will train a default FastTree model.</span></span> <span data-ttu-id="2ac6a-151">これでキー ラベルを処理するには、必要に応じて順序を変更したインデックスに対する回帰モデルをトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-151">This can handle key labels by training a regression model towards their optionally permuted indices.</span></span> |

## <a name="label-parsing"></a><span data-ttu-id="2ac6a-152">ラベルの解析</span><span class="sxs-lookup"><span data-stu-id="2ac6a-152">Label parsing</span></span>

| <span data-ttu-id="2ac6a-153">変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-153">Transform</span></span> | <span data-ttu-id="2ac6a-154">定義</span><span class="sxs-lookup"><span data-stu-id="2ac6a-154">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.Dictionarizer> | <span data-ttu-id="2ac6a-155">入力値 (単語、数字など) をディクショナリ内のインデックスに変換します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-155">Converts input values (words, numbers, etc.) to index in a dictionary.</span></span> |
| <xref:Microsoft.ML.Transforms.LabelColumnKeyBooleanConverter> | <span data-ttu-id="2ac6a-156">ラベルを分類に適したものにするため、キーまたはブール値 (必要な場合) に変換します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-156">Transforms the label to either key or bool (if needed) to make it suitable for classification.</span></span> |
| <xref:Microsoft.ML.Transforms.LabelIndicator> | <span data-ttu-id="2ac6a-157">OVA で使用される再マッパーにラベル付けします。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-157">Label remapper used by OVA.</span></span> |
| <xref:Microsoft.ML.Transforms.LabelToFloatConverter> | <span data-ttu-id="2ac6a-158">ラベルを回帰に最適なものにするため、float 型に変換します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-158">Transforms the label to float to make it suitable for regression.</span></span> |
| <xref:Microsoft.ML.Transforms.PredictedLabelColumnOriginalValueConverter> | <span data-ttu-id="2ac6a-159">予測されるラベル列が bool 型である場合を除き、元の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-159">Transforms a predicted label column to its original values, unless it is of type bool.</span></span> |

## <a name="missing-values"></a><span data-ttu-id="2ac6a-160">欠損値</span><span class="sxs-lookup"><span data-stu-id="2ac6a-160">Missing Values</span></span>

| <span data-ttu-id="2ac6a-161">変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-161">Transform</span></span> | <span data-ttu-id="2ac6a-162">定義</span><span class="sxs-lookup"><span data-stu-id="2ac6a-162">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.MissingValueHandler> | <span data-ttu-id="2ac6a-163">欠損値は、既定値または平均値/最小値/最大値 (テキスト以外の列の場合のみ) のいずれかで置き換えることで処理します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-163">Handle missing values by replacing them with either the default value or the mean/min/max value (for non-text columns only).</span></span> <span data-ttu-id="2ac6a-164">インジケーター列は、入力列の型が数値の場合には、必要に応じて連結できます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-164">An indicator column can optionally be concatenated, if the input column type is numeric.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValueIndicator> | <span data-ttu-id="2ac6a-165">入力列と同じ数のスロットを持つブール値出力列を作成します。この場合、入力列に値がない場合、出力値は true です。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-165">Create a boolean output column with the same number of slots as the input column, where the output value is true if the value in the input column is missing.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValuesDropper> | <span data-ttu-id="2ac6a-166">ベクター列から NA を削除します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-166">Removes NAs from vector columns.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValuesRowDropper> | <span data-ttu-id="2ac6a-167">欠損値を含む行を除外します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-167">Filters out rows that contain missing values.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValueSubstitutor> | <span data-ttu-id="2ac6a-168">入力列と同じ型とサイズの出力列を作成します。この場合、欠損値は既定値または平均値/最小値/最大値 (テキスト以外の列の場合のみ) のいずれかで置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-168">Create an output column of the same type and size of the input column, where missing values are replaced with either the default value or the mean/min/max value (for non-text columns only).</span></span> |

## <a name="normalization"></a><span data-ttu-id="2ac6a-169">正規化</span><span class="sxs-lookup"><span data-stu-id="2ac6a-169">Normalization</span></span>

| <span data-ttu-id="2ac6a-170">変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-170">Transform</span></span> | <span data-ttu-id="2ac6a-171">定義</span><span class="sxs-lookup"><span data-stu-id="2ac6a-171">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.BinNormalizer> | <span data-ttu-id="2ac6a-172">値が等密度のビンに割り当てられ、値がその bin_number / number_of_bins にマップされます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-172">The values are assigned into equidensity bins and a value is mapped to its bin_number / number_of_bins.</span></span> |
| <xref:Microsoft.ML.Transforms.ConditionalNormalizer> | <span data-ttu-id="2ac6a-173">必要な場合にのみ、列を正規化します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-173">Normalize the columns only if needed.</span></span> |
| <xref:Microsoft.ML.Transforms.GlobalContrastNormalizer> | <span data-ttu-id="2ac6a-174">入力値に対してグローバル コントラスト正規化を実行します。Y = (s \* X - M) / D。ここで、s はスケール、M は平均、D は L2 norm または標準偏差です。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-174">Performs a global contrast normalization on input values: Y = (s \* X - M) / D, where s is a scale, M is mean and D is either L2 norm or standard deviation.</span></span> | 
| <xref:Microsoft.ML.Transforms.LogMeanVarianceNormalizer> | <span data-ttu-id="2ac6a-175">データの対数の計算された平均と分散に基づいて、データを正規化します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-175">Normalizes the data based on the computed mean and variance of the logarithm of the data.</span></span> |
| <xref:Microsoft.ML.Transforms.LpNormalizer> | <span data-ttu-id="2ac6a-176">ベクター (行) を単位 norm (L2、L1 または LInf) に再スケーリングすることで、個別に正規化します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-176">Normalize vectors (rows) individually by rescaling them to the unit norm (L2, L1 or LInf).</span></span> <span data-ttu-id="2ac6a-177">ベクター X で、Y = (X - M) / D の演算を実行します。ここで、M は平均、D は L2 norm、L1 norm、または LInf norm のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-177">Performs the following operation on a vector X: Y = (X - M) / D, where M is mean and D is either the L2 norm, the L1 norm, or the LInf norm.</span></span> |
| <xref:Microsoft.ML.Transforms.MeanVarianceNormalizer> | <span data-ttu-id="2ac6a-178">データの計算された平均と分散に基づいて、データを正規化します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-178">Normalizes the data based on the computed mean and variance of the data.</span></span> |
| <xref:Microsoft.ML.Transforms.MinMaxNormalizer> | <span data-ttu-id="2ac6a-179">データの観察された最小値と最大値に基づいて、データを正規化します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-179">Normalizes the data based on the observed minimum and maximum values of the data.</span></span> |
| <xref:Microsoft.ML.Transforms.SupervisedBinNormalizer> | <span data-ttu-id="2ac6a-180"><xref:Microsoft.ML.Transforms.BinNormalizer> と似ていますが、等密度ではなく、ラベル列との相関関係に基づいてビンを計算します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-180">Similar to <xref:Microsoft.ML.Transforms.BinNormalizer>, but calculates bins based on correlation with the label column, not equidensity.</span></span> <span data-ttu-id="2ac6a-181">新しい値は bin_number / number_of_bins です。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-181">The new value is bin_number / number_of_bins.</span></span> |

## <a name="row-filters"></a><span data-ttu-id="2ac6a-182">行フィルター</span><span class="sxs-lookup"><span data-stu-id="2ac6a-182">Row Filters</span></span>

| <span data-ttu-id="2ac6a-183">変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-183">Transform</span></span> | <span data-ttu-id="2ac6a-184">定義</span><span class="sxs-lookup"><span data-stu-id="2ac6a-184">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.RowRangeFilter> | <span data-ttu-id="2ac6a-185">Single、Double または Key (連続) 型の列で dataview をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-185">Filters a dataview on a column of type Single, Double or Key (contiguous).</span></span> <span data-ttu-id="2ac6a-186">指定した最小/最大の範囲内に値を保持します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-186">Keeps the values that are in the specified min/max range.</span></span> <span data-ttu-id="2ac6a-187">NaNs は常に除外されます。入力が Key 型の場合、最小/最大は値の数の割合と見なされます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-187">NaNs are always filtered out. If the input is a Key type, the min/max are considered percentages of the number of values.</span></span> |
| <xref:Microsoft.ML.Transforms.RowSkipAndTakeFilter> | <span data-ttu-id="2ac6a-188">任意のオフセットで行のサブセットへの入力を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-188">Allows limiting input to a subset of rows at an optional offset.</span></span> <span data-ttu-id="2ac6a-189">データのページングを実装するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-189">Can be used to implement data paging.</span></span> |
| <xref:Microsoft.ML.Transforms.RowSkipFilter> | <span data-ttu-id="2ac6a-190">行の数をスキップすることで行のサブセットへの入力を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-190">Allows limiting input to a subset of rows by skipping a number of rows.</span></span> |
| <xref:Microsoft.ML.Transforms.RowTakeFilter> | <span data-ttu-id="2ac6a-191">最初の N 行を取得することで行のサブセットへの入力を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-191">Allows limiting input to a subset of rows by taking N first rows.</span></span> |

## <a name="schema"></a><span data-ttu-id="2ac6a-192">Schema</span><span class="sxs-lookup"><span data-stu-id="2ac6a-192">Schema</span></span>

| <span data-ttu-id="2ac6a-193">変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-193">Transform</span></span> | <span data-ttu-id="2ac6a-194">定義</span><span class="sxs-lookup"><span data-stu-id="2ac6a-194">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.ColumnConcatenator> | <span data-ttu-id="2ac6a-195">項目の種類が同じ 2 つの列を連結します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-195">Concatenates two columns of the same item type.</span></span> |
| <xref:Microsoft.ML.Transforms.ColumnCopier> | <span data-ttu-id="2ac6a-196">データセットから列を複製します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-196">Duplicates columns from the dataset.</span></span>|
| <xref:Microsoft.ML.Transforms.ColumnDropper> | <span data-ttu-id="2ac6a-197">データセットから列を削除します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-197">Drops columns from the dataset.</span></span> |
| <xref:Microsoft.ML.Transforms.ColumnSelector> | <span data-ttu-id="2ac6a-198">列のセットを選択し、それ以外のすべてを削除します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-198">Selects a set of columns, dropping all others.</span></span> |
| <xref:Microsoft.ML.Transforms.ColumnTypeConverter> | <span data-ttu-id="2ac6a-199">標準の変換を使用して、列を別の型に変換します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-199">Converts a column to a different type, using standard conversions.</span></span> |
| <xref:Microsoft.ML.Transforms.KeyToTextConverter> | <span data-ttu-id="2ac6a-200">KeyToValueTransform では、KeyValues メタデータを使用してキー インデックスを KeyValues メタデータ内の対応する値にマップします。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-200">KeyToValueTransform utilizes KeyValues metadata to map key indices to the corresponding values in the KeyValues metadata.</span></span> |
| <xref:Microsoft.ML.Transforms.NGramTranslator> | <span data-ttu-id="2ac6a-201">キーの指定のベクターで、n-gram のカウントのバッグ (長さ 1-n の連続する値のシーケンス) が生成されます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-201">Produces a bag of counts of ngrams (sequences of consecutive values of length 1-n) in a given vector of keys.</span></span> <span data-ttu-id="2ac6a-202">n-gram のディクショナリをビルドし、ディクショナリの ID をバッグのインデックスとして使用することでこれを行います。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-202">It does so by building a dictionary of ngrams and using the id in the dictionary as the index in the bag.</span></span> | 
| <xref:Microsoft.ML.Transforms.OptionalColumnCreator> | <span data-ttu-id="2ac6a-203">逆シリアル化にソース列が存在しない場合は、適切な型と既定値を持つ列を作成します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-203">If the source column does not exist after deserialization, create a column with the right type and default values.</span></span> |

## <a name="text-processing-and-featurization"></a><span data-ttu-id="2ac6a-204">テキスト処理と特徴付け</span><span class="sxs-lookup"><span data-stu-id="2ac6a-204">Text processing and featurization</span></span>

| <span data-ttu-id="2ac6a-205">変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-205">Transform</span></span> | <span data-ttu-id="2ac6a-206">定義</span><span class="sxs-lookup"><span data-stu-id="2ac6a-206">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CharacterTokenizer> | <span data-ttu-id="2ac6a-207">テキストが文字のシーケンスと見なされる文字指向のトークナイザー。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-207">Character-oriented tokenizer where text is considered a sequence of characters.</span></span> |
| <xref:Microsoft.ML.Transforms.TextFeaturizer> | <span data-ttu-id="2ac6a-208">テキスト ドキュメントのコレクションを数値特徴ベクトルにする変換。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-208">A transform that turns a collection of text documents into numerical feature vectors.</span></span> <span data-ttu-id="2ac6a-209">特徴ベクトルは、特定のトークン化されたテキストの (単語や文字) n-gram の正規化されたカウントです。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-209">The feature vectors are normalized counts of (word and/or character) ngrams in a given tokenized text.</span></span> |
| <xref:Microsoft.ML.Transforms.TextToKeyConverter> | <span data-ttu-id="2ac6a-210">入力値 (単語、数字など) をディクショナリ内のインデックスに変換します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-210">Converts input values (words, numbers, etc.) to index in a dictionary.</span></span> |
| <xref:Microsoft.ML.Transforms.WordEmbeddings> | <span data-ttu-id="2ac6a-211">事前にトレーニングされたモデルを使用して、テキスト トークンを数値ベクターに変える変換。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-211">A transform that converts vectors of text tokens into numeric vectors using a pre-trained model.</span></span> <span data-ttu-id="2ac6a-212">この手法の詳細については、Wikipedia の [Word embedding](https://en.wikipedia.org/wiki/Word_embedding) のページ (英語) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-212">For more information about the technique, see the [Word embedding](https://en.wikipedia.org/wiki/Word_embedding) Wikipedia page.</span></span> |
| <xref:Microsoft.ML.Transforms.WordTokenizer> | <span data-ttu-id="2ac6a-213">この変換への入力はテキストで、出力は元のテキスト内の単語 (トークン) を含む文字列のベクターです。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-213">The input to this transform is text, and the output is a vector of text containing the words (tokens) in the original text.</span></span> <span data-ttu-id="2ac6a-214">区切り記号は空白文字ですが、他の任意の文字 (または複数の文字) を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-214">The separator is space, but any other character (or multiple characters) can be specified.</span></span> |

## <a name="miscellaneous"></a><span data-ttu-id="2ac6a-215">その他</span><span class="sxs-lookup"><span data-stu-id="2ac6a-215">Miscellaneous</span></span>

| <span data-ttu-id="2ac6a-216">変換</span><span class="sxs-lookup"><span data-stu-id="2ac6a-216">Transform</span></span> | <span data-ttu-id="2ac6a-217">定義</span><span class="sxs-lookup"><span data-stu-id="2ac6a-217">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.ApproximateBootstrapSampler> | <span data-ttu-id="2ac6a-218">ブートストラップ サンプリングを概算します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-218">Approximate bootstrap sampling.</span></span> |
| <xref:Microsoft.ML.Transforms.BinaryPredictionScoreColumnsRenamer> | <span data-ttu-id="2ac6a-219">バイナリの予測の場合、PredictedLabel 列と Score 列の名前を、正のクラスの名前を含めるように変更します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-219">For binary prediction, renames the PredictedLabel and Score columns to include the name of the positive class.</span></span>|
| <xref:Microsoft.ML.Transforms.DataCache> | <span data-ttu-id="2ac6a-220">指定されたキャッシュ オプションを使用してキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-220">Caches using the specified cache option.</span></span> |
| <xref:Microsoft.ML.Transforms.DatasetScorer> | <span data-ttu-id="2ac6a-221">予測モデルを使用してデータセットをスコア付けします。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-221">Scores a dataset with a predictor model.</span></span> |
| <xref:Microsoft.ML.Transforms.DatasetTransformScorer> | <span data-ttu-id="2ac6a-222">変換モデルを使用してデータセットをスコア付けします。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-222">Scores a dataset with a transform model.</span></span> |
| <xref:Microsoft.ML.Transforms.NoOperation> | <span data-ttu-id="2ac6a-223">処理を行いません。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-223">Does nothing.</span></span> |
| <xref:Microsoft.ML.Transforms.RandomNumberGenerator> | <span data-ttu-id="2ac6a-224">生成された数字シーケンスを使用して列を追加します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-224">Adds a column with a generated number sequence.</span></span> |
| <xref:Microsoft.ML.Transforms.ScoreColumnSelector> | <span data-ttu-id="2ac6a-225">最後のスコア列と、引数で指定された追加の列のみを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-225">Selects only the last score columns and the extra columns specified in the arguments.</span></span> |
| <xref:Microsoft.ML.Transforms.Scorer> | <span data-ttu-id="2ac6a-226">予測モデルを変換モデルに変えます。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-226">Turns the predictor model into a transform model.</span></span> |
| <xref:Microsoft.ML.Transforms.SentimentAnalyzer> | <span data-ttu-id="2ac6a-227">事前にトレーニングされたセンチメント モデルを使用して、入力文字列をスコア付けします。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-227">Uses a pretrained sentiment model to score input strings.</span></span> |
| <xref:Microsoft.ML.Transforms.TrainTestDatasetSplitter> | <span data-ttu-id="2ac6a-228">データセットをトレーニングとテストのセットに分割します。</span><span class="sxs-lookup"><span data-stu-id="2ac6a-228">Splits the dataset into train and test sets.</span></span> |
