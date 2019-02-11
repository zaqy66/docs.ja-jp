---
title: テキスト データに対するモデル トレーニングに特徴エンジニアリングを適用する - ML.NET
description: ML.NET でテキスト データに対するモデル トレーニングに特徴エンジニアリングを適用する方法について説明します
ms.date: 02/01/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 9c3e131a46ad02c60178aa60c45dcc95472e32c7
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2019
ms.locfileid: "55758392"
---
# <a name="apply-feature-engineering-for-machine-learning-model-training-on-textual-data-with-mlnet"></a><span data-ttu-id="31aa9-103">ML.NET でテキスト データに対する機械学習モデル トレーニングに特徴エンジニアリングを適用する</span><span class="sxs-lookup"><span data-stu-id="31aa9-103">Apply feature engineering for machine learning model training on textual data with ML.NET</span></span>

<span data-ttu-id="31aa9-104">すべての ML.NET `learners` は `float vector` 型の特徴を想定しているため、float 以外のデータはすべて `float` データ型に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31aa9-104">You need to convert any non float data to `float` data types since all ML.NET `learners` expect features as a `float vector`.</span></span>

<span data-ttu-id="31aa9-105">テキスト データについて学習するには、テキストの特徴を抽出する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31aa9-105">To learn on textual data, you need to extract text features.</span></span> <span data-ttu-id="31aa9-106">ML.NET には、基本的なテキストの特徴抽出メカニズムがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="31aa9-106">ML.NET has some basic text feature extraction mechanisms:</span></span>

- <span data-ttu-id="31aa9-107">`Text normalization` (句読点の削除、分音記号、小文字への切り替え)</span><span class="sxs-lookup"><span data-stu-id="31aa9-107">`Text normalization` (removing punctuation, diacritics, switching to lowercase etc.)</span></span>
- <span data-ttu-id="31aa9-108">`Separator-based tokenization`。</span><span class="sxs-lookup"><span data-stu-id="31aa9-108">`Separator-based tokenization`.</span></span>
- <span data-ttu-id="31aa9-109">`Stopword` 削除。</span><span class="sxs-lookup"><span data-stu-id="31aa9-109">`Stopword` removal.</span></span>
- <span data-ttu-id="31aa9-110">`Ngram` と `skip-gram` 抽出。</span><span class="sxs-lookup"><span data-stu-id="31aa9-110">`Ngram` and `skip-gram` extraction.</span></span>
- <span data-ttu-id="31aa9-111">`TF-IDF` 再スケーリング。</span><span class="sxs-lookup"><span data-stu-id="31aa9-111">`TF-IDF` rescaling.</span></span>
- <span data-ttu-id="31aa9-112">`Bag of words` 変換。</span><span class="sxs-lookup"><span data-stu-id="31aa9-112">`Bag of words` conversion.</span></span>

<span data-ttu-id="31aa9-113">[Wikipedia detox データセット](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv)を使用する ML.NET のテキストの特徴抽出メカニズムの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="31aa9-113">The following example demonstrates ML.NET text feature extraction mechanisms using the [Wikipedia detox dataset](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv):</span></span>

```console
Sentiment   SentimentText
1   Stop trolling, zapatancas, calling me a liar merely demonstartes that you arer Zapatancas. You may choose to chase every legitimate editor from this site and ignore me but I am an editor with a record that isnt 99% trolling and therefore my wishes are not to be completely ignored by a sockpuppet like yourself. The consensus is overwhelmingly against you and your trolling lover Zapatancas,  
1   ::::: Why are you threatening me? I'm not being disruptive, its you who is being disruptive.   
0   " *::Your POV and propaganda pushing is dully noted. However listing interesting facts in a netral and unacusitory tone is not POV. You seem to be confusing Censorship with POV monitoring. I see nothing POV expressed in the listing of intersting facts. If you want to contribute more facts or edit wording of the cited fact to make them sound more netral then go ahead. No need to CENSOR interesting factual information. "
0   ::::::::This is a gross exaggeration. Nobody is setting a kangaroo court. There was a simple addition concerning the airline. It is the only one disputed here.   
```

```csharp
// Define the reader: specify the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextReader(new[] 
    {
        new TextLoader.Column("IsToxic", DataKind.BL, 0),
        new TextLoader.Column("Message", DataKind.TX, 1),
    },
    hasHeader: true
);

// Read the data.
var data = reader.Read(dataPath);

// Inspect the message texts that are read from the file.
var messageTexts = data.GetColumn<string>(mlContext, "Message").Take(20).ToArray();

// Apply various kinds of text operations supported by ML.NET.
var pipeline =
    // One-stop shop to run the full text featurization.
    mlContext.Transforms.Text.FeaturizeText("TextFeatures", "Message")

    // Normalize the message for later transforms
    .Append(mlContext.Transforms.Text.NormalizeText("NormalizedMessage", "Message"))

    // NLP pipeline 1: bag of words.
    .Append(new WordBagEstimator(mlContext, "BagOfWords", "NormalizedMessage"))

    // NLP pipeline 2: bag of bigrams, using hashes instead of dictionary indices.
    .Append(new WordHashBagEstimator(mlContext, "BagOfBigrams","NormalizedMessage", 
                ngramLength: 2, allLengths: false))

    // NLP pipeline 3: bag of tri-character sequences with TF-IDF weighting.
    .Append(mlContext.Transforms.Text.TokenizeCharacters("MessageChars", "Message"))
    .Append(new NgramExtractingEstimator(mlContext, "BagOfTrichar", "MessageChars", 
                ngramLength: 3, weighting: NgramExtractingEstimator.WeightingCriteria.TfIdf))

    // NLP pipeline 4: word embeddings.
    .Append(mlContext.Transforms.Text.TokenizeWords("TokenizedMessage", "NormalizedMessage"))
    .Append(mlContext.Transforms.Text.ExtractWordEmbeddings("Embeddings", "TokenizedMessage",
                WordEmbeddingsExtractingTransformer.PretrainedModelKind.GloVeTwitter25D));

// Let's train our pipeline, and then apply it to the same data.
// Note that even on a small dataset of 70KB the pipeline above can take up to a minute to completely train.
var transformedData = pipeline.Fit(data).Transform(data);

// Inspect some columns of the resulting dataset.
var embeddings = transformedData.GetColumn<float[]>(mlContext, "Embeddings").Take(10).ToArray();
var unigrams = transformedData.GetColumn<float[]>(mlContext, "BagOfWords").Take(10).ToArray();
```
