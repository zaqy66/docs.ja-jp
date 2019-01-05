---
title: 回帰ラーナーと ML.NET を使用してニューヨークのタクシー運賃を予測する
description: 回帰ラーナーと ML.NET を使用して運賃を予測する
author: aditidugar
ms.author: johalex
ms.date: 11/06/2018
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: 36da24f0cd2d2b9c4884101d97026307174f4130
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236350"
---
# <a name="tutorial-predict-new-york-taxi-fares-using-a-regression-learner-with-mlnet"></a><span data-ttu-id="714b9-103">チュートリアル: 回帰ラーナーと ML.NET を使用してニューヨークのタクシー運賃を予測する</span><span class="sxs-lookup"><span data-stu-id="714b9-103">Tutorial: Predict New York taxi fares using a regression learner with ML.NET</span></span>

> [!NOTE]
> <span data-ttu-id="714b9-104">このトピックは現在プレビュー中の ML.NET について述べており、内容が変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="714b9-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="714b9-105">詳しくは、[ML.NET の概要](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="714b9-105">For more information, see the [ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="714b9-106">このチュートリアルでは、ML.NET を使用して、ニューヨーク市のタクシー運賃を予測する[回帰モデル](../resources/glossary.md#regression)を構築する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="714b9-106">This tutorial illustrates how to use ML.NET to build a [regression model](../resources/glossary.md#regression) for predicting New York City taxi fares.</span></span>

<span data-ttu-id="714b9-107">このチュートリアルでは、次の作業を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="714b9-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="714b9-108">問題を把握する</span><span class="sxs-lookup"><span data-stu-id="714b9-108">Understand the problem</span></span>
> * <span data-ttu-id="714b9-109">適切な機械学習タスクを選択する</span><span class="sxs-lookup"><span data-stu-id="714b9-109">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="714b9-110">データを準備して理解する</span><span class="sxs-lookup"><span data-stu-id="714b9-110">Prepare and understand the data</span></span>
> * <span data-ttu-id="714b9-111">学習パイプラインを作成する</span><span class="sxs-lookup"><span data-stu-id="714b9-111">Create a learning pipeline</span></span>
> * <span data-ttu-id="714b9-112">データを読み込んで変換する</span><span class="sxs-lookup"><span data-stu-id="714b9-112">Load and transform the data</span></span>
> * <span data-ttu-id="714b9-113">学習アルゴリズムを選択する</span><span class="sxs-lookup"><span data-stu-id="714b9-113">Choose a learning algorithm</span></span>
> * <span data-ttu-id="714b9-114">モデルをトレーニングする</span><span class="sxs-lookup"><span data-stu-id="714b9-114">Train the model</span></span>
> * <span data-ttu-id="714b9-115">モデルを評価する</span><span class="sxs-lookup"><span data-stu-id="714b9-115">Evaluate the model</span></span>
> * <span data-ttu-id="714b9-116">モデルを使用して予測を行う</span><span class="sxs-lookup"><span data-stu-id="714b9-116">Use the model for predictions</span></span>

## <a name="prerequisites"></a><span data-ttu-id="714b9-117">必須コンポーネント</span><span class="sxs-lookup"><span data-stu-id="714b9-117">Prerequisites</span></span>

* <span data-ttu-id="714b9-118">[Visual Studio 2017 15.6 以降](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)が ".NET Core クロスプラット フォーム開発" とともにインストールされていること。</span><span class="sxs-lookup"><span data-stu-id="714b9-118">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

## <a name="understand-the-problem"></a><span data-ttu-id="714b9-119">問題を把握する</span><span class="sxs-lookup"><span data-stu-id="714b9-119">Understand the problem</span></span>

<span data-ttu-id="714b9-120">この問題の中心となるのは、ニューヨーク市のタクシー旅行の運賃の予測です。</span><span class="sxs-lookup"><span data-stu-id="714b9-120">This problem is about predicting the fare of a taxi trip in New York City.</span></span> <span data-ttu-id="714b9-121">一見すると、単に乗車距離に依存すると思われるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="714b9-121">At first glance, it may seem to depend simply on the distance traveled.</span></span> <span data-ttu-id="714b9-122">しかし、ニューヨークのタクシー会社は追加の乗客数や現金でなくクレジット カードによる支払いなど、その他の要因によって請求額を変えます。</span><span class="sxs-lookup"><span data-stu-id="714b9-122">However, taxi vendors in New York charge varying amounts for other factors such as additional passengers or paying with a credit card instead of cash.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="714b9-123">適切な機械学習タスクを選択する</span><span class="sxs-lookup"><span data-stu-id="714b9-123">Select the appropriate machine learning task</span></span>

<span data-ttu-id="714b9-124">データ セットの他の要因に基づき、実際の値である、価格値を予測します。</span><span class="sxs-lookup"><span data-stu-id="714b9-124">You want to predict the price value, which is a real value, based on the other factors in the data set.</span></span> <span data-ttu-id="714b9-125">それを行うには、[回帰](../resources/glossary.md#regression)機械学習タスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-125">To do that you choose a [regression](../resources/glossary.md#regression) machine learning task.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="714b9-126">コンソール アプリケーションを作成する</span><span class="sxs-lookup"><span data-stu-id="714b9-126">Create a console application</span></span>

1. <span data-ttu-id="714b9-127">Visual Studio 2017 を開きます。</span><span class="sxs-lookup"><span data-stu-id="714b9-127">Open Visual Studio 2017.</span></span> <span data-ttu-id="714b9-128">**[ファイル]** > **[新規作成]** > **[プロジェクト]** をメニュー バーから選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-128">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="714b9-129">**[新しいプロジェクト]** ダイアログで、**[Visual C#]** ノードを選択し、**[.NET Core]** ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-129">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="714b9-130">次に、**[コンソール アプリ (.NET Core)]** プロジェクト テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-130">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="714b9-131">**[名前]** テキスト ボックスに「TaxiFarePrediction」と入力し、**[OK]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-131">In the **Name** text box, type "TaxiFarePrediction" and then select the **OK** button.</span></span>

1. <span data-ttu-id="714b9-132">プロジェクトに *Data* という名前のディレクトリを作成して、データ セットとモデルのファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="714b9-132">Create a directory named *Data* in your project to store the data set and model files:</span></span>

    <span data-ttu-id="714b9-133">**ソリューション エクスプローラー**で、プロジェクトを右クリックし、**[追加]** > **[新しいフォルダー]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-133">In **Solution Explorer**, right-click the project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="714b9-134">「Data」と入力して Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="714b9-134">Type "Data" and hit Enter.</span></span>

1. <span data-ttu-id="714b9-135">**Microsoft.ML** NuGet パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="714b9-135">Install the **Microsoft.ML** NuGet Package:</span></span>

    <span data-ttu-id="714b9-136">**ソリューション エクスプローラー**で、プロジェクトを右クリックし、**[NuGet パッケージの管理]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-136">In **Solution Explorer**, right-click the project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="714b9-137">[パッケージ ソース] として "nuget.org" を選択し、**[参照]** タブを選択して「**Microsoft.ML**」を検索します。一覧からそのパッケージを選択し、**[インストール]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-137">Choose "nuget.org" as the Package source, select the **Browse** tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="714b9-138">**[変更のプレビュー]** ダイアログの **[OK]** を選択します。表示されているパッケージのライセンス条項に同意する場合は、**[ライセンスの同意]** ダイアログの **[同意する]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-138">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

## <a name="prepare-and-understand-the-data"></a><span data-ttu-id="714b9-139">データを準備して理解する</span><span class="sxs-lookup"><span data-stu-id="714b9-139">Prepare and understand the data</span></span>

1. <span data-ttu-id="714b9-140">[taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) データ セットと [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv) データ セットをダウンロードして、前の手順で作成済みの *Data* フォルダーに保存します。</span><span class="sxs-lookup"><span data-stu-id="714b9-140">Download the [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) and the [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv) data sets and save them to the *Data* folder you've created at the previous step.</span></span> <span data-ttu-id="714b9-141">これらのデータ セットを使用して、機械学習モデルをトレーニングし、モデルの正確度を評価します。</span><span class="sxs-lookup"><span data-stu-id="714b9-141">We use these data sets to train the machine learning model and then evaluate how accurate the model is.</span></span> <span data-ttu-id="714b9-142">これらのデータ セットは、[NYC TLC Taxi Trip データ セット](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml)から取得したものです。</span><span class="sxs-lookup"><span data-stu-id="714b9-142">These data sets are originally from the [NYC TLC Taxi Trip data set](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span></span>

1. <span data-ttu-id="714b9-143">**ソリューション エクスプローラー**で、各 \*.csv ファイルを右クリックし、**[プロパティ]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-143">In **Solution Explorer**, right-click each of the \*.csv files and select **Properties**.</span></span> <span data-ttu-id="714b9-144">**[詳細設定]** で、**[出力ディレクトリにコピー]** の値を **[新しい場合はコピーする]** に変更します。</span><span class="sxs-lookup"><span data-stu-id="714b9-144">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

1. <span data-ttu-id="714b9-145">**taxi-fare-train.csv** データ セットを開き、最初の行の列ヘッダーを確認します。</span><span class="sxs-lookup"><span data-stu-id="714b9-145">Open the **taxi-fare-train.csv** data set and look at column headers in the first row.</span></span> <span data-ttu-id="714b9-146">各列を確認してください。</span><span class="sxs-lookup"><span data-stu-id="714b9-146">Take a look at each of the columns.</span></span> <span data-ttu-id="714b9-147">データについて把握し、どの列が**特徴**で、どの列が**ラベル**であるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="714b9-147">Understand the data and decide which columns are **features** and which one is the **label**.</span></span>

<span data-ttu-id="714b9-148">**ラベル**は、予測する列の識別子です。</span><span class="sxs-lookup"><span data-stu-id="714b9-148">The **label** is the identifier of the column you want to predict.</span></span> <span data-ttu-id="714b9-149">識別された**特徴**は、ラベルを予測するために使用します。</span><span class="sxs-lookup"><span data-stu-id="714b9-149">The identified **features** are used to predict the label.</span></span>

<span data-ttu-id="714b9-150">提供されているデータ セットには、次の列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="714b9-150">The provided data set contains the following columns:</span></span>

* <span data-ttu-id="714b9-151">**vendor_id:** タクシー会社の ID は特徴です。</span><span class="sxs-lookup"><span data-stu-id="714b9-151">**vendor_id:** The ID of the taxi vendor is a feature.</span></span>
* <span data-ttu-id="714b9-152">**rate_code:** タクシー旅行のレートの種類は特徴です。</span><span class="sxs-lookup"><span data-stu-id="714b9-152">**rate_code:** The rate type of the taxi trip is a feature.</span></span>
* <span data-ttu-id="714b9-153">**passenger_count:** 旅行の乗客数は特徴です。</span><span class="sxs-lookup"><span data-stu-id="714b9-153">**passenger_count:** The number of passengers on the trip is a feature.</span></span>
* <span data-ttu-id="714b9-154">**trip_time_in_secs:** 旅行の所要時間です。</span><span class="sxs-lookup"><span data-stu-id="714b9-154">**trip_time_in_secs:** The amount of time the trip took.</span></span> <span data-ttu-id="714b9-155">旅行が終わる前に、旅行の運賃を予測したいと考えます。</span><span class="sxs-lookup"><span data-stu-id="714b9-155">You want to predict the fare of the trip before the trip is completed.</span></span> <span data-ttu-id="714b9-156">その時点では、旅行の所要時間はわかりません。</span><span class="sxs-lookup"><span data-stu-id="714b9-156">At that moment you don't know how long the trip would take.</span></span> <span data-ttu-id="714b9-157">したがって、旅行の所要時間は特徴ではなく、この列はモデルから除外します。</span><span class="sxs-lookup"><span data-stu-id="714b9-157">Thus, the trip time is not a feature and you'll exclude this column from the model.</span></span>
* <span data-ttu-id="714b9-158">**trip_distance:** 旅行距離は特徴です。</span><span class="sxs-lookup"><span data-stu-id="714b9-158">**trip_distance:** The distance of the trip is a feature.</span></span>
* <span data-ttu-id="714b9-159">**payment_type:** 支払い方法 (現金またはクレジット カード) は特徴です。</span><span class="sxs-lookup"><span data-stu-id="714b9-159">**payment_type:** The payment method (cash or credit card) is a feature.</span></span>
* <span data-ttu-id="714b9-160">**fare_amount:** 支払った合計タクシー運賃はラベルです。</span><span class="sxs-lookup"><span data-stu-id="714b9-160">**fare_amount:** The total taxi fare paid is the label.</span></span>

## <a name="create-data-classes"></a><span data-ttu-id="714b9-161">データ クラスを作成する</span><span class="sxs-lookup"><span data-stu-id="714b9-161">Create data classes</span></span>

<span data-ttu-id="714b9-162">入力データと予測のためのクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="714b9-162">Create classes for the input data and the predictions:</span></span>

1. <span data-ttu-id="714b9-163">**ソリューション エクスプローラー**で、プロジェクトを右クリックし、**[追加]** > **[新しい項目]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-163">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="714b9-164">**[新しい項目の追加]** ダイアログ ボックスで、**[クラス]** を選択し、**[名前]** フィールドを *TaxiTrip.cs* に変更します。</span><span class="sxs-lookup"><span data-stu-id="714b9-164">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TaxiTrip.cs*.</span></span> <span data-ttu-id="714b9-165">次に、**[追加]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-165">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="714b9-166">以下の `using` ディレクティブを新しいファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-166">Add the following `using` directives to the new file:</span></span>

   [!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#1 "Add necessary usings")]

<span data-ttu-id="714b9-167">既存のクラス定義を削除し、2 つのクラス `TaxiTrip` と `TaxiTripFarePrediction` を含む次のコードを *TaxiTrip.cs* ファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-167">Remove the existing class definition and add the following code, which has two classes `TaxiTrip` and `TaxiTripFarePrediction`, to the *TaxiTrip.cs* file:</span></span>

[!code-csharp[DefineTaxiTrip](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#2 "Define the taxi trip and fare predictions classes")]

<span data-ttu-id="714b9-168">`TaxiTrip` は入力データ クラスであり、各データ セット列の定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="714b9-168">`TaxiTrip` is the input data class and has definitions for each of the data set columns.</span></span> <span data-ttu-id="714b9-169"><xref:Microsoft.ML.Runtime.Api.ColumnAttribute> 属性を使用して、データ セット内のソース列のインデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="714b9-169">Use the <xref:Microsoft.ML.Runtime.Api.ColumnAttribute> attribute to specify the indices of the source columns in the data set.</span></span>

<span data-ttu-id="714b9-170">`TaxiTripFarePrediction` クラスは予測結果を表します。</span><span class="sxs-lookup"><span data-stu-id="714b9-170">The `TaxiTripFarePrediction` class represents predicted results.</span></span> <span data-ttu-id="714b9-171">このクラスには、`Score` <xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute> 属性が適用された 1 つの浮動小数点型フィールド `FareAmount` が含まれています。</span><span class="sxs-lookup"><span data-stu-id="714b9-171">It has a single float field, `FareAmount`, with a `Score` <xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute> attribute applied.</span></span> <span data-ttu-id="714b9-172">回帰タスクの場合、**Score** 列には、予測ラベル値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="714b9-172">In case of the regression task the **Score** column contains predicted label values.</span></span>

> [!NOTE]
> <span data-ttu-id="714b9-173">入力データと予測データのクラス内の浮動小数点値を表すには、`float` 型を使います。</span><span class="sxs-lookup"><span data-stu-id="714b9-173">Use the `float` type to represent floating-point values in the input and prediction data classes.</span></span>

## <a name="define-data-and-model-paths"></a><span data-ttu-id="714b9-174">データおよびモデルのパスを定義する</span><span class="sxs-lookup"><span data-stu-id="714b9-174">Define data and model paths</span></span>

<span data-ttu-id="714b9-175">次に示す追加の `using` ステートメントを *Program.cs* ファイルの先頭に追加します。[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#1 "Add necessary usings")]</span><span class="sxs-lookup"><span data-stu-id="714b9-175">Add the following additional `using` statements to the top of the *Program.cs* file: [!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#1 "Add necessary usings")]</span></span>

<span data-ttu-id="714b9-176">データ セットを含むファイルのパス、モデルを保存するファイルのパス、および `TextLoader` のグローバル変数を保持するための 3 つのフィールドを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="714b9-176">You need to create three fields to hold the paths to the files with data sets and the file to save the model, and a global variable for the `TextLoader`:</span></span>

* <span data-ttu-id="714b9-177">`_trainDataPath` には、モデルのトレーニングに使用するデータ セットがあるファイルへのパスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="714b9-177">`_trainDataPath` contains the path to the file with the data set used to train the model.</span></span>
* <span data-ttu-id="714b9-178">`_testDataPath` には、モデルの評価に使用するデータ セットがあるファイルへのパスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="714b9-178">`_testDataPath` contains the path to the file with the data set used to evaluate the model.</span></span>
* <span data-ttu-id="714b9-179">`_modelPath` には、トレーニング済みモデルが格納されるファイルへのパスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="714b9-179">`_modelPath` contains the path to the file where the trained model is stored.</span></span>
* <span data-ttu-id="714b9-180">`_textLoader` は、データセットの読み込みと変換に使用される <xref:Microsoft.ML.Runtime.Data.TextLoader> です。</span><span class="sxs-lookup"><span data-stu-id="714b9-180">`_textLoader` is the <xref:Microsoft.ML.Runtime.Data.TextLoader> used to load and transform the datasets.</span></span>

<span data-ttu-id="714b9-181">`Main` メソッドのすぐ上に次のコードを追加して、それらのパスと `_textLoader` 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="714b9-181">Add the following code right above the `Main` method to specify those paths and for the `_textLoader` variable:</span></span>

[!code-csharp[InitializePaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#2 "Define variables to store the data file paths")]

<span data-ttu-id="714b9-182">ML.NET を使用してモデルをビルドするときは、まず ML Context を作成します。</span><span class="sxs-lookup"><span data-stu-id="714b9-182">When building a model with ML.NET you start by creating an ML Context.</span></span> <span data-ttu-id="714b9-183">これは、概念的には Entity Framework での `DbContext` の使用に相当します。</span><span class="sxs-lookup"><span data-stu-id="714b9-183">This is comparable conceptually to using `DbContext` in Entity Framework.</span></span> <span data-ttu-id="714b9-184">環境によって、例外の追跡とログ記録に使用できる機械学習ジョブのコンテキストが提供されます。</span><span class="sxs-lookup"><span data-stu-id="714b9-184">The environment provides a context for your machine learning job that can be used for exception tracking and logging.</span></span>

### <a name="initialize-variables-in-main"></a><span data-ttu-id="714b9-185">Main で変数を初期化する</span><span class="sxs-lookup"><span data-stu-id="714b9-185">Initialize variables in Main</span></span>

<span data-ttu-id="714b9-186">`mlContext` という変数を作成し、`MLContext` の新しいインスタンスで初期化します。</span><span class="sxs-lookup"><span data-stu-id="714b9-186">Create a variable called `mlContext` and initialize it with a new instance of `MLContext`.</span></span>  <span data-ttu-id="714b9-187">`Main` メソッドの `Console.WriteLine("Hello World!")` 行を、次のコードで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="714b9-187">Replace the `Console.WriteLine("Hello World!")` line with the following code in the `Main` method:</span></span>

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#3 "Create the ML Context")]

<span data-ttu-id="714b9-188">次に、データ読み込みを設定するために、再利用できるように `_textLoader` グローバル変数を初期化します。</span><span class="sxs-lookup"><span data-stu-id="714b9-188">Next, to setup for data loading initialize the `_textLoader` global variable in order to reuse it.</span></span>  <span data-ttu-id="714b9-189">`TextReader` を使用していることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="714b9-189">Notice that we are using a `TextReader`.</span></span> <span data-ttu-id="714b9-190">`TextReader` を使用して `TextLoader` を作成するとき、必要なコンテキストと、カスタマイズを可能にする <xref:Microsoft.ML.Runtime.Data.TextLoader.Arguments> クラスを渡します。</span><span class="sxs-lookup"><span data-stu-id="714b9-190">When you create a `TextLoader` using a `TextReader`, you pass in the context needed and the <xref:Microsoft.ML.Runtime.Data.TextLoader.Arguments> class which enables customization.</span></span> <span data-ttu-id="714b9-191">すべての列名とそれらの型を含む <xref:Microsoft.ML.Runtime.Data.TextLoader.Column> オブジェクトの配列を `TextReader` に渡して、データ スキーマを指定します。</span><span class="sxs-lookup"><span data-stu-id="714b9-191">Specify the data schema by passing an array of <xref:Microsoft.ML.Runtime.Data.TextLoader.Column> objects to the `TextReader` containing all the column names and their types.</span></span> <span data-ttu-id="714b9-192">データ スキーマは、`TaxiTrip` クラスを作成したときに既に定義しています。</span><span class="sxs-lookup"><span data-stu-id="714b9-192">We defined the data schema previously when we created our `TaxiTrip` class.</span></span>

<span data-ttu-id="714b9-193">`TextReader` クラスは、完全に初期化された <xref:Microsoft.ML.Runtime.Data.TextLoader> を返します。</span><span class="sxs-lookup"><span data-stu-id="714b9-193">The `TextReader` class returns a fully initialized <xref:Microsoft.ML.Runtime.Data.TextLoader></span></span>  

<span data-ttu-id="714b9-194">必要なデータセットで再利用するために `_textLoader` グローバル変数を初期化するには、`mlContext` 初期化の後に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-194">To initialize the `_textLoader` global variable in order to reuse it for the needed datasets, add the following code after the  `mlContext` initialization:</span></span>

[!code-csharp[initTextLoader](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#4 "Initialize the TextLoader")]

<span data-ttu-id="714b9-195">`Main` メソッドに次のコード行を追加して、`Train` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="714b9-195">Add the following as the next line of code in the `Main` method to call the `Train` method:</span></span>

[!code-csharp[Train](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#5 "Train your model")]

<span data-ttu-id="714b9-196">`Train` メソッドは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="714b9-196">The `Train` method executes the following tasks:</span></span>

* <span data-ttu-id="714b9-197">データを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="714b9-197">Loads the data.</span></span>
* <span data-ttu-id="714b9-198">データを抽出して変換します。</span><span class="sxs-lookup"><span data-stu-id="714b9-198">Extracts and transforms the data.</span></span>
* <span data-ttu-id="714b9-199">モデルをトレーニングする。</span><span class="sxs-lookup"><span data-stu-id="714b9-199">Trains the model.</span></span>
* <span data-ttu-id="714b9-200">モデルを .zip ファイルとして保存します。</span><span class="sxs-lookup"><span data-stu-id="714b9-200">Saves the model as .zip file.</span></span>
* <span data-ttu-id="714b9-201">モデルを返します。</span><span class="sxs-lookup"><span data-stu-id="714b9-201">Returns the model.</span></span>

<span data-ttu-id="714b9-202">`Train` メソッドは、モデルをトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="714b9-202">The `Train` method trains the model.</span></span> <span data-ttu-id="714b9-203">次のコードを使用して、`Main` の直下にそのメソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="714b9-203">Create that method just below `Main`, using the following code:</span></span>

```csharp
public static ITransformer Train(MLContext mlContext, string dataPath)
{

}
```

<span data-ttu-id="714b9-204">`Train` メソッドに 2 つのパラメーターを渡します。つまり、コンテキスト (`mlContext`) には`MLContext`、データセット パス (`dataPath`) には文字列です。</span><span class="sxs-lookup"><span data-stu-id="714b9-204">We are passing two parameters into the `Train` method; an `MLContext` for the context (`mlContext`), and a string for the dataset path (`dataPath`).</span></span> <span data-ttu-id="714b9-205">このメソッドをデータセットの読み込みに再利用します。</span><span class="sxs-lookup"><span data-stu-id="714b9-205">We're going to reuse this method for loading datasets.</span></span>

## <a name="load-and-transform-data"></a><span data-ttu-id="714b9-206">データを読み込んで変換する</span><span class="sxs-lookup"><span data-stu-id="714b9-206">Load and transform data</span></span>

<span data-ttu-id="714b9-207">`_textLoader` グローバル変数と `dataPath` パラメーターを使用してデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="714b9-207">We'll load the data using the `_textLoader` global variable with the `dataPath` parameter.</span></span> <span data-ttu-id="714b9-208"><xref:Microsoft.ML.Runtime.Data.IDataView> が返されます。</span><span class="sxs-lookup"><span data-stu-id="714b9-208">It returns a <xref:Microsoft.ML.Runtime.Data.IDataView>.</span></span> <span data-ttu-id="714b9-209">Transforms の入力および出力として、`DataView` は基本的なデータ パイプラインの種類であり、`LINQ` の `IEnumerable` と同等です。</span><span class="sxs-lookup"><span data-stu-id="714b9-209">As the input and output of Transforms, a `DataView` is the fundamental data pipeline type, comparable to `IEnumerable` for `LINQ`.</span></span>

<span data-ttu-id="714b9-210">ML.NET ではデータは SQL ビューに似ています。</span><span class="sxs-lookup"><span data-stu-id="714b9-210">In ML.NET, data is similar to a SQL view.</span></span> <span data-ttu-id="714b9-211">つまり、遅延評価、体系的、異種です。</span><span class="sxs-lookup"><span data-stu-id="714b9-211">It is lazily evaluated, schematized, and heterogenous.</span></span> <span data-ttu-id="714b9-212">オブジェクトはパイプラインの最初の部分であり、データを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="714b9-212">The object is the first part of the pipeline, and loads the data.</span></span> <span data-ttu-id="714b9-213">このチュートリアルでは、料金の予測に役立つタクシーの運賃情報を含むデータセットを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="714b9-213">For this tutorial, it loads a dataset with taxi trip information useful to predict fares.</span></span> <span data-ttu-id="714b9-214">これを使用して、モデルを作成してトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="714b9-214">This is used to create the model, and train it.</span></span>

 <span data-ttu-id="714b9-215">`Train` メソッドの最初の行として、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-215">Add the following code as the first line of the `Train` method:</span></span>

[!code-csharp[LoadTrainData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#6 "loading training dataset")]

<span data-ttu-id="714b9-216">次の手順では、`TaxiTrip` クラス内で定義された名前によって列を参照します。</span><span class="sxs-lookup"><span data-stu-id="714b9-216">In the next steps we refer to the columns by the names defined in the `TaxiTrip` class.</span></span>

<span data-ttu-id="714b9-217">モデルのトレーニングと評価が行われるとき、既定では、**Label** 列内の値が予測される適切な値と見なされます。</span><span class="sxs-lookup"><span data-stu-id="714b9-217">When the model is trained and evaluated, by default, the values in the **Label** column are considered as correct values to be predicted.</span></span> <span data-ttu-id="714b9-218">タクシー旅行の運賃を予測したいので、`FareAmount` 列を **Label** 列にコピーします。</span><span class="sxs-lookup"><span data-stu-id="714b9-218">As we want to predict the taxi trip fare, copy the `FareAmount` column into the **Label** column.</span></span> <span data-ttu-id="714b9-219">これを行うには、`CopyColumnsEstimator` 変換クラスを使用して、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-219">To do that, use the `CopyColumnsEstimator` transformation class, and add the following code:</span></span>

[!code-csharp[CopyColumnsEstimator](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#7 "Use the CopyColumnsEstimator")]

<span data-ttu-id="714b9-220">モデルをトレーニングするアルゴリズムには、**数値**の特徴が必要であるため、カテゴリ データ (`VendorId`、`RateCode`、および `PaymentType`) 値を数字に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="714b9-220">The algorithm that trains the model requires **numeric** features, so you have to transform the categorical data (`VendorId`, `RateCode`, and `PaymentType`) values into numbers.</span></span> <span data-ttu-id="714b9-221">そのためには、`OneHotEncodingEstimator` 変換クラス (さまざまな数値キーの値をそれぞれ、各列内のさまざまな値に割り当てます) を使用し、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-221">To do that, use the `OneHotEncodingEstimator` transformation class, which assigns different numeric key values to the different values in each of the columns, and add the following code:</span></span>

[!code-csharp[OneHotEncodingEstimator](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#8 "Use the OneHotEncodingEstimator")]

<span data-ttu-id="714b9-222">データの準備の最後の手順では、`ColumnConcatenatingEstimator` 変換クラスを使用して、すべての特徴列を **Features** 列に結合します。</span><span class="sxs-lookup"><span data-stu-id="714b9-222">The last step in data preparation combines all of the feature columns into the **Features** column using the `ColumnConcatenatingEstimator` transformation class.</span></span> <span data-ttu-id="714b9-223">既定では、学習アルゴリズムは **Features** 列の特徴のみを処理します。</span><span class="sxs-lookup"><span data-stu-id="714b9-223">By default, a learning algorithm processes only features from the **Features** column.</span></span> <span data-ttu-id="714b9-224">次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-224">Add the following code:</span></span>

[!code-csharp[ColumnConcatenatingEstimator](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#9 "Use the ColumnConcatenatingEstimator")]

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="714b9-225">学習アルゴリズムを選択する</span><span class="sxs-lookup"><span data-stu-id="714b9-225">Choose a learning algorithm</span></span>

<span data-ttu-id="714b9-226">データをパイプラインに追加して正しい入力形式に変換したら、学習アルゴリズム (**ラーナー**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="714b9-226">After adding the data to the pipeline and transforming it into the correct input format, we select a learning algorithm (**learner**).</span></span> <span data-ttu-id="714b9-227">ラーナーはモデルをトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="714b9-227">The learner trains the model.</span></span> <span data-ttu-id="714b9-228">この問題に対しては**回帰タスク**を選択するので、`FastTreeRegressionTrainer` ラーナー (ML.NET によって提供される回帰ラーナーの 1 つ) を使用します。</span><span class="sxs-lookup"><span data-stu-id="714b9-228">We chose a **regression** task for this problem, so we use a `FastTreeRegressionTrainer` learner, which is one of the regression learners provided by ML.NET.</span></span>

<span data-ttu-id="714b9-229">`FastTreeRegressionTrainer` ラーナーは、勾配ブースティングを利用します。</span><span class="sxs-lookup"><span data-stu-id="714b9-229">The `FastTreeRegressionTrainer` learner utilizes gradient boosting.</span></span> <span data-ttu-id="714b9-230">勾配ブースティングは、回帰問題に対応する機械学習の手法です。</span><span class="sxs-lookup"><span data-stu-id="714b9-230">Gradient boosting is a machine learning technique for regression problems.</span></span> <span data-ttu-id="714b9-231">この手法では、それぞれの回帰ツリーを段階的に構築します。</span><span class="sxs-lookup"><span data-stu-id="714b9-231">It builds each regression tree in a step-wise fashion.</span></span> <span data-ttu-id="714b9-232">また、定義済みの損失関数を使用して、各ステップの誤差を測定し、次の段階で修正します。</span><span class="sxs-lookup"><span data-stu-id="714b9-232">It uses a pre-defined loss function to measure the error in each step and correct for it in the next.</span></span> <span data-ttu-id="714b9-233">結果は予測モデルですが、実際は弱い予測モデルの集合です。</span><span class="sxs-lookup"><span data-stu-id="714b9-233">The result is a prediction model that is actually an ensemble of weaker prediction models.</span></span> <span data-ttu-id="714b9-234">勾配ブースティングについて詳しくは、「[Boosted Decision Tree Regression](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression)」(ブーストされたデシジョン ツリー回帰) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="714b9-234">For more information about gradient boosting, see [Boosted Decision Tree Regression](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span></span>

<span data-ttu-id="714b9-235">`Train` メソッドに次のコードを追加して、前の手順で追加したデータ処理コードに `FastTreeRegressionTrainer` を追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-235">Add the following code into the `Train` method to add the `FastTreeRegressionTrainer` to the data processing code added in the previous step:</span></span>

[!code-csharp[FastTreeRegressionTrainer](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#10 "Add the FastTreeRegressionTrainer")]

## <a name="train-the-model"></a><span data-ttu-id="714b9-236">モデルをトレーニングする</span><span class="sxs-lookup"><span data-stu-id="714b9-236">Train the model</span></span>

<span data-ttu-id="714b9-237">最後の手順は、モデルのトレーニングです。</span><span class="sxs-lookup"><span data-stu-id="714b9-237">The final step is to train the model.</span></span> <span data-ttu-id="714b9-238">読み込まれて変換されたデータ セットに基づいて、モデル <xref:Microsoft.ML.Data.TransformerChain> をトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="714b9-238">We train the model, <xref:Microsoft.ML.Data.TransformerChain>, based on the dataset that has been loaded and transformed.</span></span> <span data-ttu-id="714b9-239">見積もり機能が定義されたら、既に読み込まれたトレーニング データを提供しながら、<xref:Microsoft.ML.Runtime.Data.EstimatorChain%601.Fit%2A> を使用してモデルをトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="714b9-239">Once the estimator has been defined, we train the model using the <xref:Microsoft.ML.Runtime.Data.EstimatorChain%601.Fit%2A> while providing the already loaded training data.</span></span> <span data-ttu-id="714b9-240">これにより、予測で使用されるモデルが返されます。</span><span class="sxs-lookup"><span data-stu-id="714b9-240">This returns a model to use for predictions.</span></span> <span data-ttu-id="714b9-241">`pipeline.Fit()` でパイプラインをトレーニングし、`DataView` に基づいて `Transformer` を返します。</span><span class="sxs-lookup"><span data-stu-id="714b9-241">`pipeline.Fit()` trains the pipeline and returns a `Transformer` based on the `DataView` passed in.</span></span> <span data-ttu-id="714b9-242">これが行われるまで、実験は実行されません。</span><span class="sxs-lookup"><span data-stu-id="714b9-242">The experiment is not executed until this happens.</span></span>

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#11 "Train the model")]

<span data-ttu-id="714b9-243">以上です。</span><span class="sxs-lookup"><span data-stu-id="714b9-243">And that's it!</span></span> <span data-ttu-id="714b9-244">これで機械学習モデルのトレーニングが終了し、ニューヨーク市のタクシー運賃を予測できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="714b9-244">You have successfully trained a machine learning model that can predict taxi fares in NYC.</span></span> <span data-ttu-id="714b9-245">それでは、モデルの正確度について理解してから、モデルを使用してタクシー運賃の値を予測する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="714b9-245">Now let's take a look to understand how accurate the model is and learn how to use it to predict taxi fare values.</span></span>

### <a name="save-the-model"></a><span data-ttu-id="714b9-246">モデルを保存する</span><span class="sxs-lookup"><span data-stu-id="714b9-246">Save the model</span></span>

<span data-ttu-id="714b9-247">この時点で、既存または新規のどの .NET アプリケーションにも統合できる、型が <xref:Microsoft.ML.Data.TransformerChain> のモデルができました。</span><span class="sxs-lookup"><span data-stu-id="714b9-247">At this point, you have a model of type <xref:Microsoft.ML.Data.TransformerChain> that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="714b9-248">モデルを .zip ファイルに保存するには、`Train` メソッドの終わりに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-248">To save the model to a .zip file, add the following code at the end of the `Train` method:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#12 "Save the model as a .zip file and return the model")]

## <a name="save-the-model-as-a-zip-file"></a><span data-ttu-id="714b9-249">モデルを .zip ファイルとして保存する</span><span class="sxs-lookup"><span data-stu-id="714b9-249">Save the model as a .zip file</span></span>

<span data-ttu-id="714b9-250">`Train` メソッドの直後に、次のコードを使用して `SaveModelAsFile` メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="714b9-250">Create the `SaveModelAsFile` method, just after the `Train` method, using the following code:</span></span>

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="714b9-251">`SaveModelAsFile` メソッドは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="714b9-251">The `SaveModelAsFile` method executes the following tasks:</span></span>

* <span data-ttu-id="714b9-252">モデルを .zip ファイルとして保存します。</span><span class="sxs-lookup"><span data-stu-id="714b9-252">Saves the model as a .zip file.</span></span>

<span data-ttu-id="714b9-253">他のアプリケーションで再利用し、使用できるように、モデルを保存するメソッドを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="714b9-253">We need to create a method to save the model so that it can be reused and consumed in other applications.</span></span> <span data-ttu-id="714b9-254">`ITransformer` には <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.Runtime.IHostEnvironment,System.IO.Stream)> メソッドがあり、`_modelPath` グローバル フィールドと <xref:System.IO.Stream> を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="714b9-254">The `ITransformer` has a <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.Runtime.IHostEnvironment,System.IO.Stream)> method that takes in the `_modelPath` global field, and a <xref:System.IO.Stream>.</span></span> <span data-ttu-id="714b9-255">これを zip ファイルとして保存するために、`FileStream` を作成した直後に `SaveTo` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="714b9-255">Since we want to save this as a zip file, we'll create the `FileStream` immediately before calling the `SaveTo` method.</span></span> <span data-ttu-id="714b9-256">`SaveModelAsFile` メソッドに次のコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-256">Add the following code to the `SaveModelAsFile` method as the next line:</span></span>

[!code-csharp[SaveToMethod](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#13 "Add the SaveTo Method")]

<span data-ttu-id="714b9-257">`_modelPath` を使用してコンソール メッセージを記述することで、ファイルが書き込まれた場所も表示できるようになります。これには次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="714b9-257">We could also display where the file was written by writing a console message with the `_modelPath`, using the following code:</span></span>

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="evaluate-the-model"></a><span data-ttu-id="714b9-258">モデルを評価する</span><span class="sxs-lookup"><span data-stu-id="714b9-258">Evaluate the model</span></span>

<span data-ttu-id="714b9-259">評価は、モデルがラベル値を適切に予測するかどうかを確認するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="714b9-259">Evaluation is the process of checking how well the model predicts label values.</span></span> <span data-ttu-id="714b9-260">モデルのトレーニング時に使用しなかったデータを適切に予測できるかどうかが重要になります。</span><span class="sxs-lookup"><span data-stu-id="714b9-260">It's important that the model makes good predictions on data that was not used to train the model.</span></span> <span data-ttu-id="714b9-261">そのための方法の 1 つとしては、このチュートリアルで行ったように、データをトレーニング用のデータ セットとテスト用のデータ セットに分けます。</span><span class="sxs-lookup"><span data-stu-id="714b9-261">One way to do this is to split the data into training and test data sets, as it's done in this tutorial.</span></span> <span data-ttu-id="714b9-262">トレーニング用データでのモデルのトレーニングは完了しているので、テスト用データでモデルが適切に機能するかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="714b9-262">Now that you've trained the model on the training data, you can see how well it performs on the test data.</span></span>

<span data-ttu-id="714b9-263">`Evaluate` メソッドはモデルを評価します。</span><span class="sxs-lookup"><span data-stu-id="714b9-263">The `Evaluate` method evaluates the model.</span></span> <span data-ttu-id="714b9-264">そのメソッドを作成するには、`Train` メソッドの下に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-264">To create that method, add the following code below the `Train` method:</span></span>

```csharp
private static void Evaluate(MLContext mlContext, ITransformer model)
{

}
```
<span data-ttu-id="714b9-265">`Evaluate` メソッドは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="714b9-265">The `Evaluate` method executes the following tasks:</span></span>

* <span data-ttu-id="714b9-266">テスト データ セットを読み込む。</span><span class="sxs-lookup"><span data-stu-id="714b9-266">Loads the test dataset.</span></span>
* <span data-ttu-id="714b9-267">回帰エバリュエーターを作成する。</span><span class="sxs-lookup"><span data-stu-id="714b9-267">Creates the regression evaluator.</span></span>
* <span data-ttu-id="714b9-268">モデルを評価し、メトリックを作成する。</span><span class="sxs-lookup"><span data-stu-id="714b9-268">Evaluates the model and creates metrics.</span></span>
* <span data-ttu-id="714b9-269">メトリックを表示する。</span><span class="sxs-lookup"><span data-stu-id="714b9-269">Displays the metrics.</span></span>

<span data-ttu-id="714b9-270">`Train` メソッドの呼び出しのすぐ下に、次のコードを使用して、`Main` メソッドからの新しいメソッドの呼び出しを追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-270">Add a call to the new method from the `Main` method, right under the `Train` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#14 "Call the Evaluate method")]

<span data-ttu-id="714b9-271">前に初期化した `_textLoader` グローバル変数と `_testDataPath` グローバル フィールドを使用して、テスト データセットを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="714b9-271">We'll load the test dataset using the previously initialized  `_textLoader` global variable with the `_testDataPath` global field.</span></span> <span data-ttu-id="714b9-272">このデータ セットを品質チェックとして使用して、モデルを評価できます。</span><span class="sxs-lookup"><span data-stu-id="714b9-272">You can evaluate the model using this dataset as a quality check.</span></span> <span data-ttu-id="714b9-273">`Evaluate` メソッドに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-273">Add the following code to the `Evaluate` method:</span></span>

[!code-csharp[LoadTestDataset](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#15 "Load the test dataset")]

<span data-ttu-id="714b9-274">次に、機械学習 `model` パラメーター (トランスフォーマー) を使用してフィーチャを入力し、予測を返します。</span><span class="sxs-lookup"><span data-stu-id="714b9-274">Next, we'll use the machine learning `model` parameter (a transformer) to input the features and return predictions.</span></span> <span data-ttu-id="714b9-275">`Evaluate` メソッドに次のコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-275">Add the following code to the `Evaluate` method as the next line:</span></span>

[!code-csharp[PredictWithTransformer](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#16 "Predict using the Transformer")]

<span data-ttu-id="714b9-276">`RegressionContext.Evaluate` メソッドは、指定されたデータセットを使用して `PredictionModel` の品質メトリックを計算します。</span><span class="sxs-lookup"><span data-stu-id="714b9-276">The `RegressionContext.Evaluate` method computes the quality metrics for the `PredictionModel` using the specified dataset.</span></span> <span data-ttu-id="714b9-277">これによって返される <xref:Microsoft.ML.Runtime.Data.RegressionEvaluator.Result> オブジェクトには、回帰エバリュエーターによって計算されるメトリック全体が含まれます。</span><span class="sxs-lookup"><span data-stu-id="714b9-277">It returns a <xref:Microsoft.ML.Runtime.Data.RegressionEvaluator.Result> object contains the overall metrics computed by regression evaluators.</span></span> <span data-ttu-id="714b9-278">これらを表示してモデルの品質を判定するには、最初にメトリックを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="714b9-278">To display these to determine the quality of the model, you need to get the metrics first.</span></span> <span data-ttu-id="714b9-279">`Evaluate` メソッドに次のコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-279">Add the following code as the next line in the `Evaluate` method:</span></span>

[!code-csharp[ComputeMetrics](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#17 "Compute Metrics")]

<span data-ttu-id="714b9-280">次のコードを追加してモデルを評価し、評価メトリックを生成します。</span><span class="sxs-lookup"><span data-stu-id="714b9-280">Add the following code to evaluate the model and produce the evaluation metrics:</span></span>

```csharp
Console.WriteLine();
Console.WriteLine($"*************************************************");
Console.WriteLine($"*       Model quality metrics evaluation         ");
Console.WriteLine($"*------------------------------------------------");
```

<span data-ttu-id="714b9-281">[RSquared](../resources/glossary.md#coefficient-of-determination) は回帰モデルのもう 1 つの評価メトリックです。</span><span class="sxs-lookup"><span data-stu-id="714b9-281">[RSquared](../resources/glossary.md#coefficient-of-determination) is another evaluation metric of the regression models.</span></span> <span data-ttu-id="714b9-282">RSquared は 0 から 1 までの値を取ります。</span><span class="sxs-lookup"><span data-stu-id="714b9-282">RSquared takes values between 0 and 1.</span></span> <span data-ttu-id="714b9-283">値が 1 に近づくほど、優れたモデルになります。</span><span class="sxs-lookup"><span data-stu-id="714b9-283">The closer its value is to 1, the better the model is.</span></span> <span data-ttu-id="714b9-284">次のコードを `Evaluate` メソッドに追加して、RSquared 値を表示します。</span><span class="sxs-lookup"><span data-stu-id="714b9-284">Add the following code into the `Evaluate` method to display the RSquared value:</span></span>

[!code-csharp[DisplayRSquared](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#18 "Display the RSquared metric.")]

<span data-ttu-id="714b9-285">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) は回帰モデルの評価メトリックの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="714b9-285">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) is one of the evaluation metrics of the regression model.</span></span> <span data-ttu-id="714b9-286">RMS が低いほど、優れたモデルになります。</span><span class="sxs-lookup"><span data-stu-id="714b9-286">The lower it is, the better the model is.</span></span> <span data-ttu-id="714b9-287">`Evaluate` メソッドに次のコードを追加することで、RMS 値を表示します。</span><span class="sxs-lookup"><span data-stu-id="714b9-287">Add the following code into the `Evaluate` method to display the RMS value:</span></span>

[!code-csharp[DisplayRMS](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#19 "Display the RMS metric.")]

## <a name="use-the-model-for-predictions"></a><span data-ttu-id="714b9-288">モデルを使用して予測を行う</span><span class="sxs-lookup"><span data-stu-id="714b9-288">Use the model for predictions</span></span>


## <a name="predict-the-test-data-outcome-with-the-model-and-a-single-comment"></a><span data-ttu-id="714b9-289">モデルと 1 つのコメントを使用してテスト データの結果を予測する</span><span class="sxs-lookup"><span data-stu-id="714b9-289">Predict the test data outcome with the model and a single comment</span></span>

<span data-ttu-id="714b9-290">`Evaluate` メソッドの直後に、次のコードを使用して `TestSinglePrediction` メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="714b9-290">Create the `TestSinglePrediction` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void TestSinglePrediction(MLContext mlContext)
{

}
```

<span data-ttu-id="714b9-291">`TestSinglePrediction` メソッドは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="714b9-291">The `TestSinglePrediction` method executes the following tasks:</span></span>

* <span data-ttu-id="714b9-292">テスト データの 1 つのコメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="714b9-292">Creates a single comment of test data.</span></span>
* <span data-ttu-id="714b9-293">テスト データに基づいて運賃合計を予測します。</span><span class="sxs-lookup"><span data-stu-id="714b9-293">Predicts fare amount based on test data.</span></span>
* <span data-ttu-id="714b9-294">テスト データと予測をレポート用に結合する。</span><span class="sxs-lookup"><span data-stu-id="714b9-294">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="714b9-295">予測された結果を表示する。</span><span class="sxs-lookup"><span data-stu-id="714b9-295">Displays the predicted results.</span></span>

<span data-ttu-id="714b9-296">`Evaluate` メソッドの呼び出しのすぐ下に、次のコードを使用して、`Main` メソッドからの新しいメソッドの呼び出しを追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-296">Add a call to the new method from the `Main` method, right under the `Evaluate` method call, using the following code:</span></span>

[!code-csharp[CallTestSinglePrediction](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#20 "Call the TestSinglePrediction method")]

<span data-ttu-id="714b9-297">保存した zip ファイルからモデルを読み込むために、`Load` メソッドを呼び出す直前に `FileStream` を作成します。</span><span class="sxs-lookup"><span data-stu-id="714b9-297">Since we want to load the model from the zip file we saved, we'll create the `FileStream` immediately before calling the `Load` method.</span></span> <span data-ttu-id="714b9-298">`TestSinglePrediction` メソッドに次のコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-298">Add the following code to the `TestSinglePrediction` method as the next line:</span></span>

[!code-csharp[LoadTheModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#21 "Load the model")]

<span data-ttu-id="714b9-299">`model` は多数のデータ行を操作する `transformer` ですが、よくある運用シナリオとして個々の例に対する予測のニーズがあります。</span><span class="sxs-lookup"><span data-stu-id="714b9-299">While the `model` is a `transformer` that operates on many rows of data, a very common production scenario is a need for predictions on individual examples.</span></span> <span data-ttu-id="714b9-300"><xref:Microsoft.ML.Runtime.Data.PredictionFunction%602> は、`MakePredictionFunction` メソッドから返されるラッパーです。</span><span class="sxs-lookup"><span data-stu-id="714b9-300">The <xref:Microsoft.ML.Runtime.Data.PredictionFunction%602> is a wrapper that is returned from the `MakePredictionFunction` method.</span></span> <span data-ttu-id="714b9-301">次の行を追加して、`PredictionFunction` を `Predict` メソッドの 1 行目として作成しましょう。</span><span class="sxs-lookup"><span data-stu-id="714b9-301">Let's add the following code to create the `PredictionFunction` as the first line in the `Predict` Method:</span></span>

[!code-csharp[MakePredictionFunction](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#22 "Create the PredictionFunction")]
  
<span data-ttu-id="714b9-302">このチュートリアルでは、このクラス内の 1 つのテスト用の旅行を使用します。</span><span class="sxs-lookup"><span data-stu-id="714b9-302">This tutorial uses one test trip within this class.</span></span> <span data-ttu-id="714b9-303">モデルを試行するために後で他のシナリオを追加できます。</span><span class="sxs-lookup"><span data-stu-id="714b9-303">Later you can add other scenarios to experiment with the model.</span></span> <span data-ttu-id="714b9-304">`TaxiTrip` のインスタンスを作成して、`Predict` メソッドでコストのトレーニング済みモデルの予測をテストするために、旅行を追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-304">Add a trip to test the trained model's prediction of cost in the `Predict` method by creating an instance of `TaxiTrip`:</span></span>

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#23 "Create test data for single prediction")]

 <span data-ttu-id="714b9-305">これを使用して、タクシー運賃データの 1 つのインスタンスに基づいて料金を予測することができます。</span><span class="sxs-lookup"><span data-stu-id="714b9-305">We can use that to predict the fare based on a single instance of the taxi trip data.</span></span> <span data-ttu-id="714b9-306">予測を取得するには、データに対して <xref:Microsoft.ML.Runtime.Data.PredictionFunction%602.Predict(%600)> を使用します。</span><span class="sxs-lookup"><span data-stu-id="714b9-306">To get a prediction, use <xref:Microsoft.ML.Runtime.Data.PredictionFunction%602.Predict(%600)> on the data.</span></span> <span data-ttu-id="714b9-307">入力データは文字列であり、モデルには、特徴付けが含まれることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="714b9-307">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="714b9-308">トレーニングと予測の間は、パイプラインが同期されます。</span><span class="sxs-lookup"><span data-stu-id="714b9-308">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="714b9-309">予測のために前処理/特徴付けのコードを特別に記述する必要はなく、同じ API によってバッチと 1 回限りの予測の両方が処理されます。</span><span class="sxs-lookup"><span data-stu-id="714b9-309">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#24 "Create a prediction of taxi fare")]

<span data-ttu-id="714b9-310">指定された旅行の予測運賃を表示するために、次のコードを `Main` メソッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="714b9-310">To display the predicted fare of the specified trip, add the following code into the `Main` method:</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#25 "Display the prediction.")]

<span data-ttu-id="714b9-311">プログラムを実行し、テスト ケースに対して予測されたタクシー運賃を確認します。</span><span class="sxs-lookup"><span data-stu-id="714b9-311">Run the program to see the predicted taxi fare for your test case.</span></span>

<span data-ttu-id="714b9-312">おめでとうございます! </span><span class="sxs-lookup"><span data-stu-id="714b9-312">Congratulations!</span></span> <span data-ttu-id="714b9-313">これで、タクシー旅行運賃を予測する機械学習モデルが正常に構築され、その正確度が評価され、このモデルを使用した予測が行われました。</span><span class="sxs-lookup"><span data-stu-id="714b9-313">You've now successfully built a machine learning model for predicting taxi trip fares, evaluated its accuracy, and used it to make predictions.</span></span> <span data-ttu-id="714b9-314">このチュートリアルのソース コードは、[dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction) GitHub リポジトリで確認できます。</span><span class="sxs-lookup"><span data-stu-id="714b9-314">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction) GitHub repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="714b9-315">次の手順</span><span class="sxs-lookup"><span data-stu-id="714b9-315">Next steps</span></span>

<span data-ttu-id="714b9-316">このチュートリアルでは、次の作業を行う方法を学びました。</span><span class="sxs-lookup"><span data-stu-id="714b9-316">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="714b9-317">問題を把握する</span><span class="sxs-lookup"><span data-stu-id="714b9-317">Understand the problem</span></span>
> * <span data-ttu-id="714b9-318">適切な機械学習タスクを選択する</span><span class="sxs-lookup"><span data-stu-id="714b9-318">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="714b9-319">データを準備して理解する</span><span class="sxs-lookup"><span data-stu-id="714b9-319">Prepare and understand the data</span></span>
> * <span data-ttu-id="714b9-320">学習パイプラインを作成する</span><span class="sxs-lookup"><span data-stu-id="714b9-320">Create a learning pipeline</span></span>
> * <span data-ttu-id="714b9-321">データを読み込んで変換する</span><span class="sxs-lookup"><span data-stu-id="714b9-321">Load and transform the data</span></span>
> * <span data-ttu-id="714b9-322">学習アルゴリズムを選択する</span><span class="sxs-lookup"><span data-stu-id="714b9-322">Choose a learning algorithm</span></span>
> * <span data-ttu-id="714b9-323">モデルをトレーニングする</span><span class="sxs-lookup"><span data-stu-id="714b9-323">Train the model</span></span>
> * <span data-ttu-id="714b9-324">モデルを評価する</span><span class="sxs-lookup"><span data-stu-id="714b9-324">Evaluate the model</span></span>
> * <span data-ttu-id="714b9-325">モデルを使用して予測を行う</span><span class="sxs-lookup"><span data-stu-id="714b9-325">Use the model for predictions</span></span>

<span data-ttu-id="714b9-326">さらに詳しく学習するには、次のチュートリアルに進んでください。</span><span class="sxs-lookup"><span data-stu-id="714b9-326">Advance to the next tutorial to learn more.</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="714b9-327">アヤメのクラスタリング</span><span class="sxs-lookup"><span data-stu-id="714b9-327">Iris clustering</span></span>](iris-clustering.md)
