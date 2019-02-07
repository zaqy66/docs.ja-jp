---
title: ML.NET でのモデル トレーニングに関する基本的な概念
description: この記事では、ML.NET での "*モデル トレーニング*" シナリオに関する基本概念について説明します。 よりシンプルなシナリオである "*既存モデルでの予測*" と関係のない概念も含まれます。
ms.date: 11/06/2018
ms.topic: overview
ms.custom: mvc
ms.openlocfilehash: cff833b45583bc752bb42616820a95ca6c5c6b12
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "55252441"
---
# <a name="basic-concepts-for-model-training-in-mlnet"></a><span data-ttu-id="dd19f-104">ML.NET でのモデル トレーニングに関する基本的な概念</span><span class="sxs-lookup"><span data-stu-id="dd19f-104">Basic concepts for model training in ML.NET</span></span>

<span data-ttu-id="dd19f-105">この記事では、ML.NET での "*モデル トレーニング*" シナリオに関する基本概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-105">This article explains the basic concepts covering *model training* scenarios in ML.NET.</span></span> <span data-ttu-id="dd19f-106">よりシンプルなシナリオである "*既存モデルでの予測*" と関係のない概念も含まれます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-106">Not all concepts are relevant to the more simple scenario of *prediction with existing model*.</span></span>

## <a name="model-training-concepts"></a><span data-ttu-id="dd19f-107">モデルのトレーニングの概念</span><span class="sxs-lookup"><span data-stu-id="dd19f-107">Model training concepts</span></span>

<span data-ttu-id="dd19f-108">このドキュメントでは、ML.NET でのモデルのトレーニングに関連する次の概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-108">This document covers the following concepts related to model training in ML.NET:</span></span>

- <span data-ttu-id="dd19f-109">`IDataView` インターフェイスとして表された "[*データ*](#data)"。</span><span class="sxs-lookup"><span data-stu-id="dd19f-109">[*Data*](#data) represented as an `IDataView` interface.</span></span>
  - <span data-ttu-id="dd19f-110">ML.NET では、データは SQL ビューに似ています。つまり、遅延評価で、不変で、カーソル可能で、異種で、スキーマ化されたデータセットです。</span><span class="sxs-lookup"><span data-stu-id="dd19f-110">In ML.NET, data is similar to a SQL view: It's a lazily evaluated, immutable, cursorable, heterogenous, schematized dataset.</span></span> 
  - <span data-ttu-id="dd19f-111">データ インターフェイスに関する優れたドキュメントとしては、「[IDataView Design Principles](https://github.com/dotnet/machinelearning/blob/master/docs/code/IDataViewDesignPrinciples.md)」(IDataView 設計原則) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="dd19f-111">An excellent document about the data interface is [IDataView Design Principles](https://github.com/dotnet/machinelearning/blob/master/docs/code/IDataViewDesignPrinciples.md).</span></span>
- <span data-ttu-id="dd19f-112">`ITransformer` インターフェイスとして表された "[*トランスフォーマー*](#transformer)"。</span><span class="sxs-lookup"><span data-stu-id="dd19f-112">[*Transformer*](#transformer) represented as `ITransformer` interface.</span></span>
  - <span data-ttu-id="dd19f-113">トランスフォーマーは、データを受け取り、データに対して何らかの作業を行い、変換された新しいデータを返すコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="dd19f-113">A transformer is a component that takes data, does some work on it, and returns new transformed data.</span></span>
  - <span data-ttu-id="dd19f-114">たとえば、機械学習モデルは特徴を受け取って予測を返すトランスフォーマーと考えることができます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-114">For example, you can think of a machine learning model as a transformer that takes features and returns predictions.</span></span>
  - <span data-ttu-id="dd19f-115">別の例としては、テキスト トークナイザーは 1 つのテキスト列を受け取り、テキストから抽出され個々の単語を含むベクトル列を出力します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-115">Another example, text tokenizer takes a single text column and output a vector column with individual words extracted out of the texts.</span></span>
- <span data-ttu-id="dd19f-116">`IDataReader<T>` インターフェイスとして表された "[*データ リーダー*](#data-reader)"。</span><span class="sxs-lookup"><span data-stu-id="dd19f-116">[*Data reader*](#data-reader) represented as an `IDataReader<T>` interface.</span></span>
  - <span data-ttu-id="dd19f-117">データ リーダーは、データを作成する ML.NET コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="dd19f-117">The data reader is ML.NET component to create data.</span></span> <span data-ttu-id="dd19f-118">`T` のインスタンスを受け取り、そのデータを返します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-118">It takes an instance of `T` and returns data out of it.</span></span> 
  - <span data-ttu-id="dd19f-119">たとえば、*TextLoader* は `IDataReader<FileSource>` です。</span><span class="sxs-lookup"><span data-stu-id="dd19f-119">For example, a *TextLoader* is an `IDataReader<FileSource>`.</span></span> <span data-ttu-id="dd19f-120">ファイル ソースを受け取って、データを生成します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-120">It takes the file source and produces data.</span></span> 
- <span data-ttu-id="dd19f-121">`IEstimator<T>` インターフェイスとして表された "[*エスティメーター*](#estimator)"。</span><span class="sxs-lookup"><span data-stu-id="dd19f-121">[*Estimator*](#estimator) represented as an `IEstimator<T>` interface.</span></span>
  - <span data-ttu-id="dd19f-122">これは、データから学習するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="dd19f-122">This is an object that learns from data.</span></span> <span data-ttu-id="dd19f-123">学習の結果は "*トランスフォーマー*" です。</span><span class="sxs-lookup"><span data-stu-id="dd19f-123">The result of the learning is a *transformer*.</span></span>
  - <span data-ttu-id="dd19f-124">機械学習の "*アルゴリズム*" は、データについて学習して機械学習の "*モデル*" を生成するエスティメーターと考えることができます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-124">You can think of a machine learning *algorithm* as an estimator that learns on data and produces a machine learning *model*.</span></span>
- <span data-ttu-id="dd19f-125">`PredictionFunction<TSrc, TDst>` クラスとして表された "[*予測関数*](#prediction-function)"。</span><span class="sxs-lookup"><span data-stu-id="dd19f-125">[*Prediction function*](#prediction-function) represented as a `PredictionFunction<TSrc, TDst>` class.</span></span>
  - <span data-ttu-id="dd19f-126">予測関数は、予測時などに 1 つの行に対してトランスフォーマーを適用するマシンと見なすことができます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-126">The prediction function can be seen as a machine that applies a transformer to one row, such as at prediction time.</span></span>

## <a name="data"></a><span data-ttu-id="dd19f-127">データ</span><span class="sxs-lookup"><span data-stu-id="dd19f-127">Data</span></span>

<span data-ttu-id="dd19f-128">ML.NET では、データは SQL ビューに似ています。つまり、遅延評価で、カーソル可能で、異種で、スキーマ化されたデータセットです。</span><span class="sxs-lookup"><span data-stu-id="dd19f-128">In ML.NET, data is similar to a SQL view: It's a lazily evaluated, cursorable, heterogenous, schematized dataset.</span></span>

- <span data-ttu-id="dd19f-129">データ ビューの列に関する情報を含む "*スキーマ*" (`ISchema` インターフェイスのインスタンス) を持っています。</span><span class="sxs-lookup"><span data-stu-id="dd19f-129">It has *Schema* (an instance of an `ISchema` interface) that contains the information about the data view's columns.</span></span>
  - <span data-ttu-id="dd19f-130">各列には、"*名前*"、"*型*"、および列に関連付けられた "*メタデータ*" の任意のセットがあります。</span><span class="sxs-lookup"><span data-stu-id="dd19f-130">Each column has a *Name*, a *Type*, and an arbitrary set of *metadata* associated with it.</span></span>
  - <span data-ttu-id="dd19f-131">列の "*メタデータ*" には、ベクトルの列のスロット名のような情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dd19f-131">The column's *metadata* contains information like slot names of a vector column and the like.</span></span> <span data-ttu-id="dd19f-132">メタデータ自体は、各列に固有の別の 1 つの行 "*データ*" として表されます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-132">The metadata itself is represented as another one-row *data* that is unique to each column.</span></span>
  - <span data-ttu-id="dd19f-133">データ ビューは "*カーソル*" のソースです。</span><span class="sxs-lookup"><span data-stu-id="dd19f-133">The data view is a source of *cursors*.</span></span> <span data-ttu-id="dd19f-134">SQL のカーソルを考えてください。カーソルは、一度に 1 行ずつデータを反復処理するオブジェクトであり、使用可能なデータを表します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-134">Think SQL cursors: A cursor is an object that iterates through the data, one row at a time, and presents the available data.</span></span>
  - <span data-ttu-id="dd19f-135">当然ながら、データには必要なだけいくつでもアクティブなカーソルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-135">Naturally, data can have as many active cursors over it as needed.</span></span> <span data-ttu-id="dd19f-136">データ自体は変更不可能であるため、カーソルは完全に独立しています。</span><span class="sxs-lookup"><span data-stu-id="dd19f-136">Since data itself is immutable, cursors are truly independent.</span></span>
  - <span data-ttu-id="dd19f-137">通常、カーソルは列のサブセットにのみアクセスします。効率化するため、ML.NET ではカーソルで必要な列の値のみが計算されます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-137">Cursors typically access only a subset of columns: For efficiency, ML.NET computes only the values of columns that are needed by the cursor.</span></span>

## <a name="transformer"></a><span data-ttu-id="dd19f-138">トランスフォーマー</span><span class="sxs-lookup"><span data-stu-id="dd19f-138">Transformer</span></span>

<span data-ttu-id="dd19f-139">トランスフォーマーは、データを受け取り、データに対して何らかの作業を行い、変換された新しいデータを返すコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="dd19f-139">A transformer is a component that takes data, does some work on it, and return new transformed data.</span></span>

<span data-ttu-id="dd19f-140">ML.NET のほとんどのトランスフォーマーは、多くの場合、一度に 1 つの "*入力列*" を処理して、"*出力列*" を生成します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-140">Most transformers in ML.NET tend to operate on one *input column* at a time, and produce the *output column*.</span></span> <span data-ttu-id="dd19f-141">たとえば、`new HashTransformer("foo", "bar")` は、"foo" 列から値を取得し、そのハッシュ値を計算して、"bar" 列に格納します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-141">For example, a `new HashTransformer("foo", "bar")` takes the values from column "foo", hash them, and put them into column "bar".</span></span> 

<span data-ttu-id="dd19f-142">また、入力列と出力列は同じ名前であることが一般的です。</span><span class="sxs-lookup"><span data-stu-id="dd19f-142">It's also common that the input and output column names are the same.</span></span> <span data-ttu-id="dd19f-143">この場合、古い列は新しい列で置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-143">In this case, the old column is replaced with the new one.</span></span> <span data-ttu-id="dd19f-144">たとえば、`new HashTransformer("foo")` は、"foo" 列から値を取得し、そのハッシュ値を計算して、"foo" 列に戻します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-144">For example, a `new HashTransformer("foo")` takes the values from column "foo", hash them, and put them back into "foo".</span></span> 

<span data-ttu-id="dd19f-145">もちろん、`Transform` が呼び出されると、すべてのトランスフォーマーは新しいデータ ビューを生成します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-145">Any transformer, of course, produces a new data view when `Transform` is called.</span></span> <span data-ttu-id="dd19f-146">データ ビューは不変であることを思い出してください。</span><span class="sxs-lookup"><span data-stu-id="dd19f-146">Remember, data views are immutable.</span></span>

<span data-ttu-id="dd19f-147">もう 1 つの重要な考慮事項は、データは遅延評価されるため、"*トランスフォーマーも遅延である*" ということです。</span><span class="sxs-lookup"><span data-stu-id="dd19f-147">Another important consideration is that, because data is lazily evaluated, *transformers are lazy too*.</span></span> <span data-ttu-id="dd19f-148">基本的に、次の呼び出しの後で</span><span class="sxs-lookup"><span data-stu-id="dd19f-148">Essentially, after you call</span></span>

```csharp
var newData = transformer.Transform(oldData)
```

<span data-ttu-id="dd19f-149">実際の計算は行われません。</span><span class="sxs-lookup"><span data-stu-id="dd19f-149">no actual computation happens.</span></span> <span data-ttu-id="dd19f-150">`newData` からカーソルを取得し、値の使用を開始した後でのみ、`newData` は `transformer` の変換ロジックを呼び出します (そしてその場合でも、対象の `transformer` が要求された列を生成するために必要な場合だけです)。</span><span class="sxs-lookup"><span data-stu-id="dd19f-150">Only after you get a cursor from `newData` and start consuming the value does `newData` invoke the `transformer` transformation logic (and even that only if `transformer` in question is needed to produce the requested columns).</span></span>

### <a name="transformer-chains"></a><span data-ttu-id="dd19f-151">トランスフォーマーのチェーン</span><span class="sxs-lookup"><span data-stu-id="dd19f-151">Transformer chains</span></span>

<span data-ttu-id="dd19f-152">トランスフォーマーの便利な性質は、"*トランスフォーマーのシーケンシャルな適用を別のトランスフォーマーで表すことができる*" というものです。</span><span class="sxs-lookup"><span data-stu-id="dd19f-152">A useful property of a transformer is that *you can phrase a sequential application of transformers as yet another transformer*:</span></span>

```csharp
var fullTransformer = transformer1.Append(transformer2).Append(transformer3);
```

<span data-ttu-id="dd19f-153">この性質は ML.NET でよく使用されます。通常、トレーニング済みの ML.NET モデルはトランスフォーマーのチェーンであり、これはすべての意図と目的に対する 1 つの "*トランスフォーマー*" です。</span><span class="sxs-lookup"><span data-stu-id="dd19f-153">This property is commonly used in ML.NET: typically, the trained ML.NET model is a chain of transformers, which is, for all intents and purposes, a *transformer*.</span></span> 

## <a name="data-reader"></a><span data-ttu-id="dd19f-154">データ リーダー</span><span class="sxs-lookup"><span data-stu-id="dd19f-154">Data reader</span></span>

<span data-ttu-id="dd19f-155">データ リーダーは、データを "作成する" ための ML.NET コンポーネントです。`T` のインスタンスを受け取り、そのデータを返します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-155">The data reader is ML.NET component to 'create' data: it takes an instance of `T` and returns data out of it.</span></span>

<span data-ttu-id="dd19f-156">注意すべき興味深い性質は、既存のデータ リーダーにトランスフォーマーをアタッチすることにより、データ リーダーを作成できることです。</span><span class="sxs-lookup"><span data-stu-id="dd19f-156">An interesting property to note is that you can create a data reader by attaching a transformer to an existing data reader.</span></span> <span data-ttu-id="dd19f-157">このようにして、トランスフォーマーの動作が組み込まれたリーダーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-157">This way you can have a reader with transformation behavior baked in:</span></span>

```c#
var newReader = reader.Append(transformer1).Append(transformer2)
```

<span data-ttu-id="dd19f-158">トランスフォーマーと似ているもう 1 つの点は、データは遅延評価されるため、"*リーダーも遅延である*" ことです。`dataReader.Read()` を呼び出した時点では、実際の "読み取り" はまったく (または最小限でしか) 行われません。結果のデータでカーソルが要求されたときにのみ、リーダーは処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-158">Another similarity to transformers is that, since data is lazily evaluated, *readers are lazy*: no (or minimal) actual 'reading' happens when you call `dataReader.Read()`: only when a cursor is requested on the resulting data does the reader begin to work.</span></span>

## <a name="estimator"></a><span data-ttu-id="dd19f-159">エスティメーター</span><span class="sxs-lookup"><span data-stu-id="dd19f-159">Estimator</span></span>

<span data-ttu-id="dd19f-160">"*エスティメーター*" は、データから学習するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="dd19f-160">The *estimator* is an object that learns from data.</span></span> <span data-ttu-id="dd19f-161">学習の結果は "*トランスフォーマー*" です。</span><span class="sxs-lookup"><span data-stu-id="dd19f-161">The result of the learning is a *transformer*.</span></span>

<span data-ttu-id="dd19f-162">ML.NET では、この特性を使用して、異なるエスティメーターを連結する学習パイプラインを作成します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-162">In ML.NET, use this property to create learning pipelines that chain together different estimators:</span></span>

```csharp
MLContext mlContext = new MLContext(seed: 0);

var pipeline = new CopyColumnsEstimator(mlContext, "FareAmount", "Label")
.Append(mlContextml.Transforms.Categorical.OneHotEncoding(mlContext, "VendorId"))
.Append(mlContextml.Transforms.Categorical.OneHotEncoding(mlContext, "RateCode"))
.Append(mlContextml.Transforms.Categorical.OneHotEncoding(mlContext, "PaymentType"))
.Append(new ColumnConcatenatingEstimator(mlContext, "Features", "VendorId", "RateCode", "PassengerCount", "TripTime", "TripDistance", "PaymentType"))
.Append(mlContext.Regression.Trainers.FastTree("Label", "Features"));

var model = pipeline.Fit(dataView);
```

<span data-ttu-id="dd19f-163">エスティメーターの 1 つの重要な特性は、"*エスティメーターは遅延ではなく一括である*" ということです。`Fit` のすべての呼び出しによって学習が発生し、その操作には時間がかかる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dd19f-163">One important property of estimators is that *estimators are eager, not lazy*: every call to `Fit` is causing learning to happen, which is potentially a time-consuming operation.</span></span>

## <a name="prediction-function"></a><span data-ttu-id="dd19f-164">予測関数</span><span class="sxs-lookup"><span data-stu-id="dd19f-164">Prediction function</span></span>

<span data-ttu-id="dd19f-165">予測関数は、1 つの行に対してトランスフォーマーを適用するマシンと見なすことができます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-165">The prediction function can be seen as a machine that applies a transformer to one row.</span></span>

<span data-ttu-id="dd19f-166">モデルを取得した後は (`Fit()` によってトレーニングされたか、またはどこかから読み込まれた "*トランスフォーマー*")、それを使用して、`model.Transform(data)` の通常の呼び出しで予測を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-166">Once you get the model (a *transformer* either trained via `Fit()`, or loaded from somewhere), you can use it to make predictions using the normal calls to `model.Transform(data)`.</span></span> <span data-ttu-id="dd19f-167">ただし、実際のシナリオでこのモデルを使用するときは、通常、予測に多くの例を使用しません。</span><span class="sxs-lookup"><span data-stu-id="dd19f-167">However, when you use this model in a real-life scenario, you often don't have many examples to predict on.</span></span> <span data-ttu-id="dd19f-168">代わりに、一度に 1 つの例を使用し、すぐに適切なタイミングで予測を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd19f-168">Instead, you have one example at a time, and you need to make timely predictions on them immediately.</span></span>

<span data-ttu-id="dd19f-169">もちろん、これをバッチ予測に軽減できます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-169">Of course, you can reduce this to the batch prediction:</span></span>

- <span data-ttu-id="dd19f-170">厳密に 1 つの行でデータ ビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-170">Create a data view with exactly one row.</span></span>
- <span data-ttu-id="dd19f-171">`model.Transform(data)` を呼び出して、予測されたデータ ビューを取得します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-171">Call `model.Transform(data)` to get the predicted data view.</span></span>
- <span data-ttu-id="dd19f-172">結果のデータに対するカーソルを取得します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-172">Get a cursor over the resulting data.</span></span>
- <span data-ttu-id="dd19f-173">カーソルを 1 ステップ進めて、最初の (そして唯一の) 行を取得します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-173">Advance the cursor one step to get to the first (and only) row.</span></span>
- <span data-ttu-id="dd19f-174">それから予測される値を抽出します。</span><span class="sxs-lookup"><span data-stu-id="dd19f-174">Extract the predicted values out of it.</span></span>

<span data-ttu-id="dd19f-175">前記のアルゴリズムは、次のように[スキーマの理解](https://github.com/dotnet/machinelearning/blob/master/docs/code/SchemaComprehension.md)と 2 つのユーザー定義オブジェクト `InputExample` と `OutputPrediction` を使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-175">The preceding algorithm can be implemented using the [schema comprehension](https://github.com/dotnet/machinelearning/blob/master/docs/code/SchemaComprehension.md), with two user-defined objects `InputExample` and `OutputPrediction` as follows:</span></span>

```c#
var inputData = env.CreateDataView(new InputExample[] { example });
var outputData = model.Transform(inputData);
var output = outputData.AsDynamic.AsEnumerable<OutputPrediction>(env, reuseRowObject: false).Single();
```

<span data-ttu-id="dd19f-176">ただし、これは面倒で、パフォーマンス コストがかかります。</span><span class="sxs-lookup"><span data-stu-id="dd19f-176">But this is cumbersome and incurs performance costs.</span></span> <span data-ttu-id="dd19f-177">代わりに、予測関数オブジェクトでは、拡張メソッド `MakePredictionFunction` により同じ処理が、ただしもっと速く便利に行われます。</span><span class="sxs-lookup"><span data-stu-id="dd19f-177">Instead, a prediction function object performs the same work, but faster and more convenient, via an extension method `MakePredictionFunction`:</span></span>

```c#
var predictionFunc = model.MakePredictionFunction<InputExample, OutputPrediction>(env);
var output = predictionFunc.Predict(example);
```

<span data-ttu-id="dd19f-178">予測関数は "*再入可能/スレッド セーフではありません*"。</span><span class="sxs-lookup"><span data-stu-id="dd19f-178">The prediction function is *not re-entrant / thread-safe*.</span></span> <span data-ttu-id="dd19f-179">複数のスレッドで同時に予測を実行する場合は、スレッドごとに予測関数が存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd19f-179">If you want to conduct predictions simultaneously with multiple threads, you need to have a prediction function per thread.</span></span>
