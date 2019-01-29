---
title: ML.NET を GitHub の問題の多クラス分類シナリオで使用する
description: GitHub の問題を分類し、それを特定の領域に割り当てるための多クラス分類シナリオで、ML.NET を使用する方法について説明します。
ms.date: 01/24/2019
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: 6f01357906fd4398f68dadfb35dbce816f4302c0
ms.sourcegitcommit: d9a0071d0fd490ae006c816f78a563b9946e269a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2019
ms.locfileid: "55066208"
---
# <a name="tutorial-use-mlnet-in-a-multiclass-classification-scenario-to-classify-github-issues"></a><span data-ttu-id="0e5ff-103">チュートリアル: ML.NET を、GitHub の問題を分類する多クラス分類シナリオで使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-103">Tutorial: Use ML.NET in a multiclass classification scenario to classify GitHub issues.</span></span>

<span data-ttu-id="0e5ff-104">このサンプル チュートリアルでは、Visual Studio 2017 で ML.NET を使用して、C# を使用する .NET Core コンソール アプリケーションから GitHub の問題を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-104">This sample tutorial illustrates using ML.NET to create a GitHub issue classifier via a .NET Core console application using C# in Visual Studio 2017.</span></span>

<span data-ttu-id="0e5ff-105">このチュートリアルでは、次の作業を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-105">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="0e5ff-106">問題を把握する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-106">Understand the problem</span></span>
> * <span data-ttu-id="0e5ff-107">適切な機械学習タスクを選択する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-107">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="0e5ff-108">データを準備する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-108">Prepare your data</span></span>
> * <span data-ttu-id="0e5ff-109">学習パイプラインを作成する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-109">Create the learning pipeline</span></span>
> * <span data-ttu-id="0e5ff-110">分類器を読み込む</span><span class="sxs-lookup"><span data-stu-id="0e5ff-110">Load a classifier</span></span>
> * <span data-ttu-id="0e5ff-111">モデルをトレーニングする</span><span class="sxs-lookup"><span data-stu-id="0e5ff-111">Train the model</span></span>
> * <span data-ttu-id="0e5ff-112">別のデータ セットを使用してモデルを評価する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-112">Evaluate the model with a different dataset</span></span>
> * <span data-ttu-id="0e5ff-113">モデルを使用してテスト データの結果の 1 つのインスタンスを予測する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-113">Predict a single instance of test data outcome with the model</span></span>
> * <span data-ttu-id="0e5ff-114">読み込んだモデルを使用してテスト データの結果を予測する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-114">Predict the test data outcomes with a loaded model</span></span>

> [!NOTE]
> <span data-ttu-id="0e5ff-115">このトピックは現在プレビュー中の ML.NET について述べており、内容が変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-115">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="0e5ff-116">詳細については、[ML.NET の概要](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-116">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

## <a name="github-issue-sample-overview"></a><span data-ttu-id="0e5ff-117">GitHub の問題のサンプルの概要</span><span class="sxs-lookup"><span data-stu-id="0e5ff-117">GitHub issue sample overview</span></span>

<span data-ttu-id="0e5ff-118">このサンプルは ML.NET を使用するコンソール アプリケーションであり、GitHub の問題の区分ラベルを分類および予測するモデルをトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-118">The sample is a console app that uses ML.NET to train a model that classifies and predicts the Area label for a GitHub issue.</span></span> <span data-ttu-id="0e5ff-119">また、高品質な分析のために、2 番目のデータ セットを使用してモデルを評価します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-119">It also evaluates the model with a second dataset for quality analysis.</span></span> <span data-ttu-id="0e5ff-120">問題のデータセットは、dotnet/corefx GitHub リポジトリにあります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-120">The issue datasets are from the dotnet/corefx GitHub repo.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0e5ff-121">必須コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e5ff-121">Prerequisites</span></span>

* <span data-ttu-id="0e5ff-122">[Visual Studio 2017 15.6 以降](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)が ".NET Core クロスプラット フォーム開発" とともにインストールされていること。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-122">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

* <span data-ttu-id="0e5ff-123">[Github の問題のタブ区切りのファイル (issues_train.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv)。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-123">The [Github issues tab separated file (issues_train.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv).</span></span>
* <span data-ttu-id="0e5ff-124">[Github の問題のテスト タブ区切りのファイル (issues_test.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv)。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-124">The [Github issues test tab separated file (issues_test.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv).</span></span>

## <a name="machine-learning-workflow"></a><span data-ttu-id="0e5ff-125">機械学習ワークフロー</span><span class="sxs-lookup"><span data-stu-id="0e5ff-125">Machine learning workflow</span></span>

<span data-ttu-id="0e5ff-126">このチュートリアルでは、プロセスを順序立てて進められるようにする機械学習ワークフローに従います。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-126">This tutorial follows a machine learning workflow that enables the process to move in an orderly fashion.</span></span>

<span data-ttu-id="0e5ff-127">このワークフローには次のフェーズがあります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-127">The workflow phases are as follows:</span></span>

1. <span data-ttu-id="0e5ff-128">**問題を把握する**</span><span class="sxs-lookup"><span data-stu-id="0e5ff-128">**Understand the problem**</span></span>
2. <span data-ttu-id="0e5ff-129">**データを準備する**</span><span class="sxs-lookup"><span data-stu-id="0e5ff-129">**Prepare your data**</span></span>
   * <span data-ttu-id="0e5ff-130">**データを読み込む**</span><span class="sxs-lookup"><span data-stu-id="0e5ff-130">**Load the data**</span></span>
   * <span data-ttu-id="0e5ff-131">**特徴を抽出する (データを変換する)**</span><span class="sxs-lookup"><span data-stu-id="0e5ff-131">**Extract features (Transform your data)**</span></span>
3. <span data-ttu-id="0e5ff-132">**ビルドしてトレーニングする**</span><span class="sxs-lookup"><span data-stu-id="0e5ff-132">**Build and train**</span></span> 
   * <span data-ttu-id="0e5ff-133">**モデルをトレーニングする**</span><span class="sxs-lookup"><span data-stu-id="0e5ff-133">**Train the model**</span></span>
   * <span data-ttu-id="0e5ff-134">**モデルを評価する**</span><span class="sxs-lookup"><span data-stu-id="0e5ff-134">**Evaluate the model**</span></span>
4. <span data-ttu-id="0e5ff-135">**実行**</span><span class="sxs-lookup"><span data-stu-id="0e5ff-135">**Run**</span></span>
   * <span data-ttu-id="0e5ff-136">**モデルの使用**</span><span class="sxs-lookup"><span data-stu-id="0e5ff-136">**Model consumption**</span></span>

### <a name="understand-the-problem"></a><span data-ttu-id="0e5ff-137">問題を把握する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-137">Understand the problem</span></span>

<span data-ttu-id="0e5ff-138">まず、問題を把握して、モデルのビルドおよびトレーニングに使用できるパーツに分ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-138">You first need to understand the problem, so you can break it down to parts that can support building and training the model.</span></span> <span data-ttu-id="0e5ff-139">問題を分けることで、結果の予測および評価ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-139">Breaking  down the problem allows you to predict and evaluate the results.</span></span>

<span data-ttu-id="0e5ff-140">このチュートリアルでの問題は、優先順位付けとスケジューリングを行うための正しいラベル付けのために、受け取った GitHub の問題がどの区分に属するかを理解することです。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-140">The problem for this tutorial is to understand what area incoming GitHub issues belong to in order to label them correctly for prioritization and scheduling.</span></span>

<span data-ttu-id="0e5ff-141">問題は次に分けることができます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-141">You can break down the problem to the following:</span></span>

* <span data-ttu-id="0e5ff-142">問題のタイトル テキスト</span><span class="sxs-lookup"><span data-stu-id="0e5ff-142">the issue title text</span></span>
* <span data-ttu-id="0e5ff-143">問題の説明テキスト</span><span class="sxs-lookup"><span data-stu-id="0e5ff-143">the issue description text</span></span>
* <span data-ttu-id="0e5ff-144">モデルのトレーニング データの区分値</span><span class="sxs-lookup"><span data-stu-id="0e5ff-144">an area value for the model training data</span></span>
* <span data-ttu-id="0e5ff-145">評価して操作で使用できる予測される区分値</span><span class="sxs-lookup"><span data-stu-id="0e5ff-145">a predicted area value that you can evaluate and then use operationally</span></span>

<span data-ttu-id="0e5ff-146">次に、区分を**決定**する必要があります。これは機械学習タスクを選択するときに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-146">You then need to **determine** the area, which helps you with the machine learning task selection.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="0e5ff-147">適切な機械学習タスクを選択する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-147">Select the appropriate machine learning task</span></span>

<span data-ttu-id="0e5ff-148">この問題に関してわかっていることは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-148">With this problem, you know the following facts:</span></span>

<span data-ttu-id="0e5ff-149">トレーニング データ:</span><span class="sxs-lookup"><span data-stu-id="0e5ff-149">Training data:</span></span>

<span data-ttu-id="0e5ff-150">GitHub の問題は、次の例のようないくつかの領域 (**区分**) にラベル分けできます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-150">GitHub issues can be labeled in several areas (**Area**) as in the following examples:</span></span>

* <span data-ttu-id="0e5ff-151">area-System.Numerics</span><span class="sxs-lookup"><span data-stu-id="0e5ff-151">area-System.Numerics</span></span>
* <span data-ttu-id="0e5ff-152">area-System.Xml</span><span class="sxs-lookup"><span data-stu-id="0e5ff-152">area-System.Xml</span></span>
* <span data-ttu-id="0e5ff-153">area-Infrastructure</span><span class="sxs-lookup"><span data-stu-id="0e5ff-153">area-Infrastructure</span></span>
* <span data-ttu-id="0e5ff-154">area-System.Linq</span><span class="sxs-lookup"><span data-stu-id="0e5ff-154">area-System.Linq</span></span>
* <span data-ttu-id="0e5ff-155">area-System.IO</span><span class="sxs-lookup"><span data-stu-id="0e5ff-155">area-System.IO</span></span>

<span data-ttu-id="0e5ff-156">次の例のように、新しい GitHub の問題の**区分**を予測します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-156">Predict the **Area** of a new GitHub Issue such as in the following examples:</span></span>

* <span data-ttu-id="0e5ff-157">Contract.Assert 対 Debug.Assert</span><span class="sxs-lookup"><span data-stu-id="0e5ff-157">Contract.Assert vs Debug.Assert</span></span>
* <span data-ttu-id="0e5ff-158">System.Xml のフィールドを読み取り専用にする</span><span class="sxs-lookup"><span data-stu-id="0e5ff-158">Make fields readonly in System.Xml</span></span>

<span data-ttu-id="0e5ff-159">このシナリオには、分類機械学習タスクが適しています。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-159">The classification machine learning task is best suited for this scenario.</span></span>

### <a name="about-the-classification-task"></a><span data-ttu-id="0e5ff-160">分類タスクについて</span><span class="sxs-lookup"><span data-stu-id="0e5ff-160">About the classification task</span></span>

<span data-ttu-id="0e5ff-161">分類とは、データを使用して項目またはデータ行のカテゴリ、型、クラスを**判断**する機械学習タスクです。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-161">Classification is a machine learning task that uses data to **determine** the category, type, or class of an item or row of data.</span></span> <span data-ttu-id="0e5ff-162">分類はたとえば、次のような目的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-162">For example, you can use classification to:</span></span>

* <span data-ttu-id="0e5ff-163">センチメントが肯定的か否定的かを判断する。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-163">Identify sentiment as positive or negative.</span></span>
* <span data-ttu-id="0e5ff-164">電子メールをスパム、迷惑メール、正常なメールに分類する。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-164">Classify email as spam, junk, or good.</span></span>
* <span data-ttu-id="0e5ff-165">患者の検体が癌性かどうかを判断する。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-165">Determine whether a patient's lab sample is cancerous.</span></span>
* <span data-ttu-id="0e5ff-166">顧客を販売キャンペーンへの反応性で分類する。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-166">Categorize customers by their propensity to respond to a sales campaign.</span></span>

<span data-ttu-id="0e5ff-167">多くの場合、分類タスクは次のいずれかの種類です。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-167">Classification tasks are frequently one of the following types:</span></span>

* <span data-ttu-id="0e5ff-168">バイナリ: A か B のいずれかである。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-168">Binary: either A or B.</span></span>
* <span data-ttu-id="0e5ff-169">多クラス: 1 つのモデルを使用して予測できるカテゴリが多数ある。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-169">Multiclass: multiple categories that can be predicted by using a single model.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="0e5ff-170">コンソール アプリケーションを作成する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-170">Create a console application</span></span>

### <a name="create-a-project"></a><span data-ttu-id="0e5ff-171">プロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-171">Create a project</span></span>

1. <span data-ttu-id="0e5ff-172">Visual Studio 2017 を開きます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-172">Open Visual Studio 2017.</span></span> <span data-ttu-id="0e5ff-173">**[ファイル]** > **[新規作成]** > **[プロジェクト]** をメニュー バーから選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-173">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="0e5ff-174">**[新しいプロジェクト]** ダイアログで、**[Visual C#]** ノードを選択し、**[.NET Core]** ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-174">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="0e5ff-175">次に、**[コンソール アプリ (.NET Core)]** プロジェクト テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-175">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="0e5ff-176">**[名前]** テキスト ボックスに「SentimentAnalysis」と入力し、**[OK]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-176">In the **Name** text box, type "SentimentAnalysis" and then select the **OK** button.</span></span>

2. <span data-ttu-id="0e5ff-177">プロジェクトに *Data* という名前のディレクトリを作成して、データ セット ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-177">Create a directory named *Data* in your project to save your data set files:</span></span>

    <span data-ttu-id="0e5ff-178">**ソリューション エクスプローラー**で、プロジェクトを右クリックし、**[追加]** > **[新しいフォルダー]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-178">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="0e5ff-179">「Data」と入力して Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-179">Type "Data" and hit Enter.</span></span>

3. <span data-ttu-id="0e5ff-180">**Microsoft.ML NuGet パッケージ**をインストールします。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-180">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="0e5ff-181">ソリューション エクスプローラーで、プロジェクトを右クリックし、**[NuGet パッケージの管理]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-181">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="0e5ff-182">[パッケージ ソース] として "nuget.org" を選択し、[参照] タブを選択して「**Microsoft.ML**」を検索します。一覧からそのパッケージを選択し、**[インストール]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-182">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="0e5ff-183">**[変更のプレビュー]** ダイアログの **[OK]** を選択します。表示されているパッケージのライセンス条項に同意する場合は、**[ライセンスの同意]** ダイアログの **[同意する]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-183">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

### <a name="prepare-your-data"></a><span data-ttu-id="0e5ff-184">データを準備する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-184">Prepare your data</span></span>

1. <span data-ttu-id="0e5ff-185">[issues_train.tsv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv) データ セットと [issues_test.tsv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv) データ セットをダウンロードして、それらを作成済みの *Data* フォルダーに保存します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-185">Download the [issues_train.tsv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv) and the [issues_test.tsv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv) data sets and save them to the *Data* folder previously created.</span></span> <span data-ttu-id="0e5ff-186">1 番目のデータ セットでは機械学習モデルをトレーニングし、2 番目のデータ セットはモデルの精度を評価するために使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-186">The first dataset trains the machine learning model and the second can be used to evaluate how accurate your model is.</span></span>

2. <span data-ttu-id="0e5ff-187">ソリューション エクスプローラーで、各 \*.tsv ファイルを右クリックし、**[プロパティ]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-187">In Solution Explorer, right-click each of the \*.tsv files and select **Properties**.</span></span> <span data-ttu-id="0e5ff-188">**[詳細設定]** で、**[出力ディレクトリにコピー]** の値を **[新しい場合はコピーする]** に変更します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-188">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

### <a name="create-classes-and-define-paths"></a><span data-ttu-id="0e5ff-189">クラスを作成してパスを定義する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-189">Create classes and define paths</span></span>

<span data-ttu-id="0e5ff-190">次に示す追加の `using` ステートメントを *Program.cs* ファイルの先頭に追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-190">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddUsings)]

<span data-ttu-id="0e5ff-191">最近ダウンロードしたファイルのパスを保存する 3 つのグローバル フィールドと、`TextLoader` のためのグローバル変数を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-191">You need to create three global fields to hold the paths to the recently downloaded files, and a global variable for the `TextLoader`:</span></span>

* <span data-ttu-id="0e5ff-192">`_trainDataPath` には、モデルのトレーニングに使用するデータ セットのパスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-192">`_trainDataPath` has the path to the dataset used to train the model.</span></span>
* <span data-ttu-id="0e5ff-193">`_testDataPath` には、モデルの評価に使用するデータ セットのパスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-193">`_testDataPath` has the path to the dataset used to evaluate the model.</span></span>
* <span data-ttu-id="0e5ff-194">`_modelPath` には、トレーニング済みのモデルを保存するパスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-194">`_modelPath` has the path where the trained model is saved.</span></span>
* <span data-ttu-id="0e5ff-195">`_mlContext` は処理コンテキストを提供する <xref:Microsoft.ML.MLContext> です。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-195">`_mlContext` is the <xref:Microsoft.ML.MLContext> that provides processing context.</span></span>
* <span data-ttu-id="0e5ff-196">`_trainingDataView` は、トレーニング データセットを処理するために使用される <xref:Microsoft.ML.Data.IDataView> です。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-196">`_trainingDataView` is the <xref:Microsoft.ML.Data.IDataView> used to process the training dataset.</span></span>
* <span data-ttu-id="0e5ff-197">`_predEngine` は、1 つの予測に使用される <xref:Microsoft.ML.PredictionEngine%602> です。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-197">`_predEngine` is the <xref:Microsoft.ML.PredictionEngine%602> used for single predictions.</span></span>
* <span data-ttu-id="0e5ff-198">`_reader` は、データセットの読み込みと変換に使用される <xref:Microsoft.ML.Data.TextLoader> です。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-198">`_reader` is the <xref:Microsoft.ML.Data.TextLoader> used to load and transform the datasets.</span></span>

<span data-ttu-id="0e5ff-199">`Main` メソッドのすぐ上にある行に次のコードを追加して、それらのパスとその他の変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-199">Add the following code to the line right above the `Main` method to specify those paths and the other variables:</span></span>

[!code-csharp[DeclareGlobalVariables](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DeclareGlobalVariables)]

<span data-ttu-id="0e5ff-200">入力データと予測のために、いくつかのクラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-200">You need to create some classes for your input data and predictions.</span></span> <span data-ttu-id="0e5ff-201">プロジェクトに新しいクラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-201">Add a new class to your project:</span></span>

1. <span data-ttu-id="0e5ff-202">**ソリューション エクスプローラー**で、プロジェクトを右クリックし、**[追加]** > **[新しい項目]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-202">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="0e5ff-203">**[新しい項目の追加]** ダイアログ ボックスで、**[クラス]** を選択し、**[名前]** フィールドを「*GitHubIssueData.cs*」に変更します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-203">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *GitHubIssueData.cs*.</span></span> <span data-ttu-id="0e5ff-204">次に、**[追加]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-204">Then, select the **Add** button.</span></span>

    <span data-ttu-id="0e5ff-205">コード エディターで *GitHubIssueData.cs* ファイルが開きます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-205">The *GitHubIssueData.cs* file opens in the code editor.</span></span> <span data-ttu-id="0e5ff-206">*GitHubIssueData.cs* の先頭に次の `using` ステートメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-206">Add the following `using` statement to the top of *GitHubIssueData.cs*:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/GitHubIssueClassification/GitHubIssueData.cs#AddUsings)]

<span data-ttu-id="0e5ff-207">既存のクラス定義を削除し、`GitHubIssue` と `IssuePrediction` の 2 つのクラスを含む次のコードを *GitHubIssueData.cs* ファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-207">Remove the existing class definition and add the following code, which has two classes `GitHubIssue` and `IssuePrediction`, to the *GitHubIssueData.cs* file:</span></span>

[!code-csharp[DeclareTypes](../../../samples/machine-learning/tutorials/GitHubIssueClassification/GitHubIssueData.cs#DeclareTypes)]

<span data-ttu-id="0e5ff-208">`GitHubIssue` は、入力データセット クラスで、次の <xref:System.String> フィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-208">`GitHubIssue` is the input dataset class and has the following <xref:System.String> fields:</span></span>

* <span data-ttu-id="0e5ff-209">`ID` には GitHub の問題の ID 値が含まれます</span><span class="sxs-lookup"><span data-stu-id="0e5ff-209">`ID` contains a value for the GitHub issue ID</span></span>
* <span data-ttu-id="0e5ff-210">`Area` には、`Area` ラベルの値が含まれます</span><span class="sxs-lookup"><span data-stu-id="0e5ff-210">`Area` contains a value for the `Area` label</span></span>
* <span data-ttu-id="0e5ff-211">`Title` には GitHub の問題のタイトルが含まれます</span><span class="sxs-lookup"><span data-stu-id="0e5ff-211">`Title` contains the GitHub issue title</span></span>
* <span data-ttu-id="0e5ff-212">`Description` には GitHub の問題の説明が含まれます</span><span class="sxs-lookup"><span data-stu-id="0e5ff-212">`Description` contains the GitHub issue description</span></span>

<span data-ttu-id="0e5ff-213">`IssuePrediction` は、モデルがトレーニングされた後に、予測に使用されるクラスです。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-213">`IssuePrediction` is the class used for prediction after the model has been trained.</span></span> <span data-ttu-id="0e5ff-214">これは、1 つの `string` (`Area`) と、`PredictedLabel` `ColumnName` 属性があります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-214">It has a single `string` (`Area`) and a `PredictedLabel` `ColumnName` attribute.</span></span> <span data-ttu-id="0e5ff-215">`Label` はモデルを作成してトレーニングするために使用され、2 番目のデータ セットでもモデルを評価するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-215">The `Label` is used to create and train the model, and it's also used with a second dataset to evaluate the model.</span></span> <span data-ttu-id="0e5ff-216">`PredictedLabel` は予測と評価の際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-216">The `PredictedLabel` is used during prediction and evaluation.</span></span> <span data-ttu-id="0e5ff-217">評価では、トレーニング データを含む入力、予測された値、およびモデルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-217">For evaluation, an input with training data, the predicted values, and the model are used.</span></span>

<span data-ttu-id="0e5ff-218">ML.NET を使用してモデルをビルドするときは、まず <xref:Microsoft.ML.MLContext> を作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-218">When building a model with ML.NET, you start by creating an <xref:Microsoft.ML.MLContext>.</span></span> <span data-ttu-id="0e5ff-219">これは、概念的には Entity Framework での `DbContext` の使用に相当します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-219">This is comparable conceptually to using `DbContext` in Entity Framework.</span></span> <span data-ttu-id="0e5ff-220">環境によって、例外の追跡とログ記録に使用できる ML ジョブのコンテキストが提供されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-220">The environment provides a context for your ML job that can be used for exception tracking and logging.</span></span>

### <a name="initialize-variables-in-main"></a><span data-ttu-id="0e5ff-221">Main で変数を初期化する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-221">Initialize variables in Main</span></span>

<span data-ttu-id="0e5ff-222">複数のトレーニング間で反復可能な決定論的結果を得るために、`_mlContext` グローバル変数をランダム シード (`seed: 0`) を使用して `MLContext` の新しいインスタンスで初期化します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-222">Initialize the `_mlContext` global variable  with a new instance of `MLContext` with a random seed (`seed: 0`) for repeatable/deterministic results across multiple trainings.</span></span>  <span data-ttu-id="0e5ff-223">`Main` メソッドの `Console.WriteLine("Hello World!")` 行を、次のコードで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-223">Replace the `Console.WriteLine("Hello World!")` line with the following code in the `Main` method:</span></span>

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreateMLContext)]

## <a name="load-the-data"></a><span data-ttu-id="0e5ff-224">データを読み込む</span><span class="sxs-lookup"><span data-stu-id="0e5ff-224">Load the data</span></span>

<span data-ttu-id="0e5ff-225">次いで、`_trainingDataView` <xref:Microsoft.ML.Data.IDataView> グローバル変数を初期化して、`_trainDataPath` パラメーターを使用してデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-225">Next, initialize the `_trainingDataView` <xref:Microsoft.ML.Data.IDataView> global variable and load the data with the `_trainDataPath` parameter.</span></span>

 <span data-ttu-id="0e5ff-226">`Transforms` の入力および出力として、`DataView` は基本的なデータ パイプラインの種類であり、`LINQ` の `IEnumerable` と同等です。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-226">As the input and output of `Transforms`, a `DataView` is the fundamental data pipeline type, comparable to `IEnumerable` for `LINQ`.</span></span>

<span data-ttu-id="0e5ff-227">ML.NET ではデータは `SQL view` に似ています。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-227">In ML.NET, data is similar to a `SQL view`.</span></span> <span data-ttu-id="0e5ff-228">つまり、遅延評価、体系的、異種です。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-228">It is lazily evaluated, schematized, and heterogenous.</span></span> <span data-ttu-id="0e5ff-229">オブジェクトはパイプラインの最初の部分であり、データを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-229">The object is the first part of the pipeline, and loads the data.</span></span> <span data-ttu-id="0e5ff-230">このチュートリアルでは、問題のタイトル、説明、および対応する区分 GitHub ラベルを使用してデータセットを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-230">For this tutorial, it loads a dataset with issue titles, descriptions, and corresponding area GitHub label.</span></span> <span data-ttu-id="0e5ff-231">モデルの作成とトレーニングには、`DataView` が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-231">The `DataView` is used to create and train the model.</span></span>

<span data-ttu-id="0e5ff-232">以前に作成した `GitHubIssue` データ モデルの種類がデータセット スキーマと一致するため、初期化、マッピング、およびデータセットの読み込みを 1 行のコードに組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-232">Since your previously created `GitHubIssue` data model type matches the dataset schema, you can combine the initialization, mapping, and dataset loading into one line of code.</span></span>

<span data-ttu-id="0e5ff-233">行の最初の部分 (`CreateTextReader<GitHubIssue>(hasHeader: true)`) では、`GitHubIssue` データ モデル型からデータセット スキーマを推論し、データセットのヘッダーを使用し、<xref:Microsoft.ML.Data.TextLoader> を作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-233">The first part of the line (`CreateTextReader<GitHubIssue>(hasHeader: true)`) creates a <xref:Microsoft.ML.Data.TextLoader> by inferencing the dataset schema from the `GitHubIssue` data model type and using the dataset header.</span></span>

<span data-ttu-id="0e5ff-234">データ スキーマは、`GitHubIssue` クラスを作成したときに既に定義しています。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-234">You defined the data schema previously when you created the `GitHubIssue` class.</span></span> <span data-ttu-id="0e5ff-235">スキーマでは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-235">For your schema:</span></span>

* <span data-ttu-id="0e5ff-236">最初の列 `ID` (GitHub 問題 ID)</span><span class="sxs-lookup"><span data-stu-id="0e5ff-236">the first column `ID` (GitHub Issue ID)</span></span>
* <span data-ttu-id="0e5ff-237">2 番目の列 `Area` (トレーニングの予測)</span><span class="sxs-lookup"><span data-stu-id="0e5ff-237">the second column `Area` (the prediction for training)</span></span>
* <span data-ttu-id="0e5ff-238">3 番目の列 `Title` (GitHub の問題のタイトル) は、`Area` の予測に使用される最初の[特徴](../resources/glossary.md##feature)です</span><span class="sxs-lookup"><span data-stu-id="0e5ff-238">the third column `Title` (GitHub issue title) is the first [feature](../resources/glossary.md##feature)  used for predicting the `Area`</span></span>
* <span data-ttu-id="0e5ff-239">第 4 列 `Description` は、`Area` の予測に使用される 2 番目の特徴です</span><span class="sxs-lookup"><span data-stu-id="0e5ff-239">the fourth column  `Description` is the second feature used for predicting the `Area`</span></span>

<span data-ttu-id="0e5ff-240">行の 2 番目の部分 (`.Read(_trainDataPath)`) では <xref:Microsoft.ML.Data.TextLoader.Read%2A> メソッドを使用して、`IDataView` (`_trainingDataView`) グローバル変数に `_trainDataPath` を使用してトレーニング用のテキスト ファイルを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-240">The second part of the line  (`.Read(_trainDataPath)`) uses <xref:Microsoft.ML.Data.TextLoader.Read%2A> method to load the training text file using `_trainDataPath` into the `IDataView` (`_trainingDataView`) global variable.</span></span>  

<span data-ttu-id="0e5ff-241">パイプラインで利用するために `_trainingDataView` グローバル変数を初期化して読み込むには、`mlContext` 初期化の後に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-241">To initialize and load the `_trainingDataView` global variable in order to use it for the pipeline, add the following code after the  `mlContext` initialization:</span></span>

[!code-csharp[LoadTrainData](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadTrainData)]


<span data-ttu-id="0e5ff-242">`Main` メソッドに次のコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-242">Add the following as the next line of code in the `Main` method:</span></span>

[!code-csharp[CallProcessData](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallProcessData)]

<span data-ttu-id="0e5ff-243">`ProcessData` メソッドは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-243">The `ProcessData` method executes the following tasks:</span></span>

* <span data-ttu-id="0e5ff-244">データを抽出して変換します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-244">Extracts and transforms the data.</span></span>
* <span data-ttu-id="0e5ff-245">処理パイプラインを返します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-245">Returns the processing pipeline.</span></span>

<span data-ttu-id="0e5ff-246">`Main` メソッドの直後に、次のコードを使用して `ProcessData` メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-246">Create the `ProcessData` method, just after the `Main` method, using the following code:</span></span>

```csharp
public static EstimatorChain<ITransformer> ProcessData()
{

}
```

## <a name="extract-and-transform-the-data"></a><span data-ttu-id="0e5ff-247">データを抽出して変換する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-247">Extract and transform the data</span></span>

<span data-ttu-id="0e5ff-248">データの前処理とクリーニングは、機械学習でデータ セットを効果的に使用する前に発生する重要なタスクです。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-248">Pre-processing and cleaning data are important tasks that occur before a dataset is used effectively for machine learning.</span></span> <span data-ttu-id="0e5ff-249">多くの場合、生データはノイズが多くて信頼性が低く、値が欠落している可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-249">Raw data is often noisy and unreliable, and may be missing values.</span></span> <span data-ttu-id="0e5ff-250">これらのモデル化タスクを行わずにデータを使用すると、誤解を招く結果が生じるおそれがあります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-250">Using data without these modeling tasks can produce misleading results.</span></span>

<span data-ttu-id="0e5ff-251">ML.NET の変換パイプラインによって、トレーニングまたはテストの前にデータに適用するカスタム変換セットが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-251">ML.NET's transform pipelines compose a custom set of transforms that are applied to your data before training or testing.</span></span> <span data-ttu-id="0e5ff-252">この変換の主な目的は、データの[特徴付け](../resources/glossary.md#feature-engineering)です。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-252">The transforms' primary purpose is data [featurization](../resources/glossary.md#feature-engineering).</span></span> <span data-ttu-id="0e5ff-253">機械学習アルゴリズムによって理解されるのは、[特徴付け](../resources/glossary.md#feature)されたデータです。したがって、次の手順では、テキスト データを ML アルゴリズムが認識できる形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-253">Machine learning algorithms understand [featurized](../resources/glossary.md#feature) data, so the next step is to transform our textual data into a format that our ML algorithms recognize.</span></span> <span data-ttu-id="0e5ff-254">その形式は、[数値ベクトル](../resources/glossary.md#numerical-feature-vector)です。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-254">That format is a [numeric vector](../resources/glossary.md#numerical-feature-vector).</span></span>

<span data-ttu-id="0e5ff-255">次の手順では、`GitHubIssue` クラス内で定義された名前によって列を参照します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-255">In the next steps, we refer to the columns by the names defined in the `GitHubIssue` class.</span></span>

<span data-ttu-id="0e5ff-256">モデルのトレーニングと評価が行われるとき、既定では、**Label** 列内の値が予測される適切な値と見なされます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-256">When the model is trained and evaluated, by default, the values in the **Label** column are considered as correct values to be predicted.</span></span> <span data-ttu-id="0e5ff-257">`GitHubIssue` の区分 GitHub ラベルを予測したいので、`Area` 列を **Label** 列にコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-257">As we want to predict the Area GitHub label for a `GitHubIssue`, copy the `Area` column into the **Label** column.</span></span> <span data-ttu-id="0e5ff-258">これを行うには、<xref:Microsoft.ML.ConversionsExtensionsCatalog.MapValueToKey%2A> 変換クラスのラッパーである `MLContext.Transforms.Conversion.MapValueToKey` を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-258">To do that, use the `MLContext.Transforms.Conversion.MapValueToKey`, which is a wrapper for the <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapValueToKey%2A> transformation class.</span></span>  <span data-ttu-id="0e5ff-259">`MapValueToKey` は、実質的にパイプラインになる <xref:Microsoft.ML.Data.EstimatorChain%601> を返します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-259">The `MapValueToKey` returns an <xref:Microsoft.ML.Data.EstimatorChain%601> that will effectively be a pipeline.</span></span> <span data-ttu-id="0e5ff-260">後でトレーナーを `EstimatorChain` に付加するときに、この `pipeline` を指定します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-260">Name this `pipeline` as you will then append the trainer to the `EstimatorChain`.</span></span> <span data-ttu-id="0e5ff-261">次のコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-261">Add this as the next line of code:</span></span>

[!code-csharp[MapValueToKey](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#MapValueToKey)]

<span data-ttu-id="0e5ff-262">このモデルをトレーニングするアルゴリズムには**数値**の特徴が必要なので、次では、呼び出された各 `TitleFeaturized` および `DescriptionFeaturized` に対して、テキスト (`Title` と `Description`) 列を数値ベクトルに特徴付ける `mlContext.Transforms.Text.FeaturizeText` を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-262">The algorithm that trains the model requires **numeric** features, so you have Next, call `mlContext.Transforms.Text.FeaturizeText` which featurizes the text (`Title` and `Description`) columns into a numeric vector for each called `TitleFeaturized` and `DescriptionFeaturized`.</span></span> <span data-ttu-id="0e5ff-263">特徴付けによって、各列内のさまざまな値に異なる数値が割り当てられ、機械学習のアルゴリズムで使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-263">Featurizing assigns different numeric key values to the different values in each of the columns and is used by the machine learning algorithm.</span></span>
<span data-ttu-id="0e5ff-264">次のコードを使用して、両列の特徴付けをパイプラインに追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-264">Append the featurization for both columns to the pipeline with the following code:</span></span>

[!code-csharp[FeaturizeText](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#FeaturizeText)]

<span data-ttu-id="0e5ff-265">データの準備の最後の手順では、`Concatenate` 変換クラスを使用して、すべての特徴列を **Features** 列に結合します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-265">The last step in data preparation combines all of the feature columns into the **Features** column using the `Concatenate` transformation class.</span></span> <span data-ttu-id="0e5ff-266">既定では、学習アルゴリズムは **Features** 列の特徴のみを処理します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-266">By default, a learning algorithm processes only features from the **Features** column.</span></span> <span data-ttu-id="0e5ff-267">次のコードを使用してパイプラインに、この変換を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-267">Append this transformation to the pipeline with the following code:</span></span>

[!code-csharp[Concatenate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Concatenate)]

 <span data-ttu-id="0e5ff-268">次に、DataView をキャッシュするために <xref:Microsoft.ML.Data.EstimatorChain`1.AppendCacheCheckpoint%2A> を追加します。つまり、次のコードでキャッシュを使用してデータが複数回反復されると、パフォーマンスが向上する場合があります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-268">Next, append a <xref:Microsoft.ML.Data.EstimatorChain`1.AppendCacheCheckpoint%2A> to cache the DataView so when you iterate over the data multiple times using the cache might get better performance, as with the following code</span></span>

[!code-csharp[AppendCache](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AppendCache)]

<span data-ttu-id="0e5ff-269">`ProcessData` メソッドの最後で、パイプラインが返されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-269">Return the pipeline at the end of the `ProcessData` method.</span></span>

[!code-csharp[ReturnPipeline](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#ReturnPipeline)]

<span data-ttu-id="0e5ff-270">この手順で前処理と特徴付けが処理されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-270">This step handles preprocessing/featurization.</span></span> <span data-ttu-id="0e5ff-271">ML.NET に用意されているその他のコンポーネントを使用すると、モデルでより良い結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-271">Using additional components available in ML.NET can enable better results with your model.</span></span>

## <a name="build-and-train-the-model"></a><span data-ttu-id="0e5ff-272">モデルを構築してトレーニングする</span><span class="sxs-lookup"><span data-stu-id="0e5ff-272">Build and train the model</span></span>

<span data-ttu-id="0e5ff-273">`Main` メソッドの次のコード行として、`BuildAndTrainModel` メソッドに次の呼び出しを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-273">Add the following call to the `BuildAndTrainModel`method as the next line of code in the `Main` method:</span></span>

[!code-csharp[CallBuildAndTrainModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallBuildAndTrainModel)]

<span data-ttu-id="0e5ff-274">`BuildAndTrainModel` メソッドは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-274">The `BuildAndTrainModel` method executes the following tasks:</span></span>

* <span data-ttu-id="0e5ff-275">トレーニング アルゴリズムのクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-275">Creates the training algorithm class.</span></span>
* <span data-ttu-id="0e5ff-276">モデルをトレーニングする。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-276">Trains the model.</span></span>
* <span data-ttu-id="0e5ff-277">トレーニング データに基づいて区分を予測します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-277">Predicts area based on training data.</span></span>
* <span data-ttu-id="0e5ff-278">モデルを `.zip` ファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-278">Saves the model to a `.zip` file.</span></span>
* <span data-ttu-id="0e5ff-279">モデルを返します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-279">Returns the model.</span></span>

<span data-ttu-id="0e5ff-280">`Main` メソッドの直後に、次のコードを使用して `BuildAndTrainModel` メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-280">Create the `BuildAndTrainModel` method, just after the `Main` method, using the following code:</span></span>

```csharp
public static void BuildAndTrainModel()
{

}
```

<span data-ttu-id="0e5ff-281">これでトレーニング データセット (`trainingDataView`) 用の `IDataView` と、ProcessData (`pipeline`) で作成された処理用パイプライン用の <xref:Microsoft.ML.Data.EstimatorChain%601> の 2 つのパラメーターが BuildAndTrainModel メソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-281">Notice that two parameters are passed into the BuildAndTrainModel method; an `IDataView` for the training dataset (`trainingDataView`), and a <xref:Microsoft.ML.Data.EstimatorChain%601> for the processing pipeline created in ProcessData (`pipeline`).</span></span>

 <span data-ttu-id="0e5ff-282">`BuildAndTrainModel` メソッドの最初の行として、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-282">Add the following code as the first line of the `BuildAndTrainModel` method:</span></span>

### <a name="choose-a-trainer-algorithm"></a><span data-ttu-id="0e5ff-283">トレーナー アルゴリズムを選択する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-283">Choose a trainer algorithm</span></span>

<span data-ttu-id="0e5ff-284">トレーナー アルゴリズムを追加するには、<xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer> オブジェクトを返す `mlContext.Transforms.Text.FeaturizeText` ラッパー メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-284">To add the trainer algorithm, call the `mlContext.Transforms.Text.FeaturizeText` wrapper method which returns a <xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer> object.</span></span> <span data-ttu-id="0e5ff-285">これは、このパイプラインで使用するデシジョン ツリーの学習器です。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-285">This is a decision tree learner you'll use in this pipeline.</span></span> <span data-ttu-id="0e5ff-286">`SdcaMultiClassTrainer` が `pipeline` に追加されます。これは、特徴付けされた `Title` と `Description` (`Features`) と `Label` 入力パラメーターを受け入れて、履歴データから学習します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-286">The `SdcaMultiClassTrainer` is appended to the `pipeline` and accepts the featurized `Title` and `Description` (`Features`) and the `Label` input parameters to learn from the historic data.</span></span>

<span data-ttu-id="0e5ff-287">`BuildAndTrainModel` メソッドに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-287">Add the following code to the `BuildAndTrainModel` method:</span></span>

[!code-csharp[SdcaMultiClassTrainer](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#SdcaMultiClassTrainer)]

<span data-ttu-id="0e5ff-288">これでトレーナー アルゴリズムが作成できたので、これを `pipeline` に追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-288">Now that you've created a trainer algorithm, append it to the `pipeline`.</span></span> <span data-ttu-id="0e5ff-289">元の読み取り可能な状態に戻すために、値にラベルもマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-289">You also need to map the label to the value to return to its original readable state.</span></span> <span data-ttu-id="0e5ff-290">これらの両アクションは、次のコードを使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-290">Do both of those actions with the following code:</span></span>

[!code-csharp[AddTrainer](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddTrainer)]

### <a name="train-the-model"></a><span data-ttu-id="0e5ff-291">モデルをトレーニングする</span><span class="sxs-lookup"><span data-stu-id="0e5ff-291">Train the model</span></span>

<span data-ttu-id="0e5ff-292">読み込まれて変換されたデータ セットに基づいて、モデル <xref:Microsoft.ML.Data.TransformerChain%601> をトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-292">You train the model, <xref:Microsoft.ML.Data.TransformerChain%601>, based on the dataset that has been loaded and transformed.</span></span> <span data-ttu-id="0e5ff-293">推定器が定義されたら、既に読み込まれたトレーニング データを提供しながら、<xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> を使用してモデルをトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-293">Once the estimator has been defined, you train your model using the <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> while providing the already loaded training data.</span></span> <span data-ttu-id="0e5ff-294">これにより、予測で使用されるモデルが返されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-294">This returns a model to use for predictions.</span></span> <span data-ttu-id="0e5ff-295">`trainingPipeline.Fit()` でパイプラインをトレーニングし、`DataView` に基づいて `Transformer` を返します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-295">`trainingPipeline.Fit()` trains the pipeline and returns a `Transformer` based on the `DataView` passed in.</span></span> <span data-ttu-id="0e5ff-296">これが行われるまで、実験は実行されません。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-296">The experiment is not executed until this happens.</span></span>

<span data-ttu-id="0e5ff-297">`BuildAndTrainModel` メソッドに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-297">Add the following code to the `BuildAndTrainModel` method:</span></span>

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#TrainModel)]

<span data-ttu-id="0e5ff-298">`model` は多数のデータ行を操作する `transformer` ですが、よくある運用シナリオとして個々の例に対する予測のニーズがあります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-298">While the `model` is a `transformer` that operates on many rows of data, a very common production scenario is a need for predictions on individual examples.</span></span> <span data-ttu-id="0e5ff-299"><xref:Microsoft.ML.PredictionEngine%602> は、`CreatePredictionEngine` メソッドから返されるラッパーです。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-299">The <xref:Microsoft.ML.PredictionEngine%602> is a wrapper that is returned from the `CreatePredictionEngine` method.</span></span> <span data-ttu-id="0e5ff-300">次の行を追加して、`PredictionEngine` を `BuildAndTrainModel` メソッドの次の行として作成しましょう。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-300">Let's add the following code to create the `PredictionEngine` as the next line in the `BuildAndTrainModel` Method:</span></span>

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine)]

<span data-ttu-id="0e5ff-301">GitHub の問題を追加して、`Predict` メソッドでトレーニングされたモデルの予測をテストします。これには `GitHubIssue` のインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-301">Add a GitHub issue to test the trained model's prediction in the `Predict` method by creating an instance of `GitHubIssue`:</span></span>

[!code-csharp[CreateTestIssue1](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreateTestIssue1)]

<span data-ttu-id="0e5ff-302">これを使用して、問題のデータの 1 インスタンスの `Area` レベルを予測できます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-302">You can use that to predict the `Area` label of a single instance of the issue data.</span></span> <span data-ttu-id="0e5ff-303">予測を取得するには、データに対して <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-303">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="0e5ff-304">入力データは文字列であり、モデルには、特徴付けが含まれることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-304">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="0e5ff-305">トレーニングと予測の間は、パイプラインが同期されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-305">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="0e5ff-306">予測のために前処理/特徴付けのコードを特別に記述する必要はなく、同じ API によってバッチと 1 回限りの予測の両方が処理されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-306">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Predict)]

### <a name="model-operationalization-prediction"></a><span data-ttu-id="0e5ff-307">モデルの運用化: 予測</span><span class="sxs-lookup"><span data-stu-id="0e5ff-307">Model operationalization: prediction</span></span>

<span data-ttu-id="0e5ff-308">結果を共有し、それに応じたアクションを実行するために、`GitHubIssue` および対応する `Area` ラベル予測を表示します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-308">Display `GitHubIssue` and corresponding `Area` label prediction in order to share the results and act on them accordingly.</span></span> <span data-ttu-id="0e5ff-309">これは運用化と呼ばれ、返されたデータを運用ポリシーとして使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-309">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="0e5ff-310">次の <xref:System.Console.WriteLine?displayProperty=nameWithType> コードを使用して、結果の表示を作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-310">Create a display for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[OutputPrediction](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#OutputPrediction)]

### <a name="save-and-return-the-model-trained-to-use-for-evaluation"></a><span data-ttu-id="0e5ff-311">評価に使用する、トレーニングされたモデルを保存して返す</span><span class="sxs-lookup"><span data-stu-id="0e5ff-311">Save and return the model trained to use for evaluation</span></span>

<span data-ttu-id="0e5ff-312">この時点で、既存または新規のどの .NET アプリケーションにも統合できる、型が <xref:Microsoft.ML.Data.TransformerChain%601> のモデルができました。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-312">At this point, you have a model of type <xref:Microsoft.ML.Data.TransformerChain%601> that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="0e5ff-313">トレーニングしたモデルを .zip ファイルに保存するには、`BuildAndTrainModel` の次の行で `SaveModelAsFile` メソッドを呼び出すために次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-313">To save your trained model to a .zip file, add the following code to call the `SaveModelAsFile` method as the next line in `BuildAndTrainModel`:</span></span>

[!code-csharp[CallSaveModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallSaveModel)]

<span data-ttu-id="0e5ff-314">`BuildAndTrainModel` メソッドの最後で、モデルを返します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-314">Return the model at the end of the `BuildAndTrainModel` method.</span></span>

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#ReturnModel)]

## <a name="save-the-model-as-azip-file"></a><span data-ttu-id="0e5ff-315">モデルを .zip ファイルとして保存する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-315">Save the model as a.zip file</span></span>

<span data-ttu-id="0e5ff-316">`BuildAndTrainModel` メソッドの直後に、次のコードを使用して `SaveModelAsFile` メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-316">Create the `SaveModelAsFile` method, just after the `BuildAndTrainModel` method, using the following code:</span></span>

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="0e5ff-317">`SaveModelAsFile` メソッドは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-317">The `SaveModelAsFile` method executes the following tasks:</span></span>

* <span data-ttu-id="0e5ff-318">モデルを .zip ファイルとして保存します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-318">Saves the model as a .zip file.</span></span>

<span data-ttu-id="0e5ff-319">次に、モデルを再利用して他のアプリケーションで使用できるようにモデルを保存するメソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-319">Next, create a method to save the model so that it can be reused and consumed in other applications.</span></span> <span data-ttu-id="0e5ff-320">`ITransformer` には <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> メソッドがあり、`_modelPath` グローバル フィールドと <xref:System.IO.Stream> を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-320">The `ITransformer` has a <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> method that takes in the `_modelPath` global field, and a <xref:System.IO.Stream>.</span></span> <span data-ttu-id="0e5ff-321">これを zip ファイルとして保存するには、`FileStream` を作成した直後に `SaveTo` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-321">To save this as a zip file, you'll create the `FileStream` immediately before calling the `SaveTo` method.</span></span> <span data-ttu-id="0e5ff-322">`SaveModelAsFile` メソッドに次のコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-322">Add the following code to the `SaveModelAsFile` method as the next line:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#SaveModel)]

<span data-ttu-id="0e5ff-323">`_modelPath` を使用してコンソール メッセージを記述することで、ファイルが書き込まれた場所も表示できるようになります。これには次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-323">You could also display where the file was written by writing a console message with the `_modelPath`, using the following code:</span></span>

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="evaluate-the-model"></a><span data-ttu-id="0e5ff-324">モデルを評価する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-324">Evaluate the model</span></span>

<span data-ttu-id="0e5ff-325">これでモデルの作成とトレーニングが完了したので、品質保証と検証のために、別のデータ セットを使用してモデルを評価します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-325">Now that you've created and trained the model, you need to evaluate it with a different dataset for quality assurance and validation.</span></span> <span data-ttu-id="0e5ff-326">`Evaluate` メソッドでは、`BuildAndTrainModel` で作成されたモデルが渡されて評価されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-326">In the `Evaluate` method, the model created in `BuildAndTrainModel` is passed in to be evaluated.</span></span> <span data-ttu-id="0e5ff-327">`BuildAndTrainModel` の直後に、次のコードに示すように `Evaluate` メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-327">Create the `Evaluate` method, just after `BuildAndTrainModel`, as in the following code:</span></span>

```csharp
public static void Evaluate()
{

}
```

<span data-ttu-id="0e5ff-328">`Evaluate` メソッドは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-328">The `Evaluate` method executes the following tasks:</span></span>

* <span data-ttu-id="0e5ff-329">テスト データ セットを読み込む。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-329">Loads the test dataset.</span></span>
* <span data-ttu-id="0e5ff-330">多クラス評価器を作成する。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-330">Creates the multiclass evaluator.</span></span>
* <span data-ttu-id="0e5ff-331">モデルを評価し、メトリックを作成する。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-331">Evaluates the model and create metrics.</span></span>
* <span data-ttu-id="0e5ff-332">メトリックを表示する。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-332">Displays the metrics.</span></span>

<span data-ttu-id="0e5ff-333">`BuildAndTrainModel` メソッドの呼び出しのすぐ下に、次のコードを使用して、`Main` メソッドからの新しいメソッドの呼び出しを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-333">Add a call to the new method from the `Main` method, right under the `BuildAndTrainModel` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallEvaluate)]

<span data-ttu-id="0e5ff-334">既にトレーニング データセットで行ったように、初期化、マッピング、テスト データの読み込みを 1 行のコードに結合できます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-334">As you did previously with the training dataset, you can combine the initialization, mapping, and test dataset loading into one line of code.</span></span> <span data-ttu-id="0e5ff-335">このデータ セットを品質チェックとして使用して、モデルを評価できます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-335">You can evaluate the model using this dataset as a quality check.</span></span> <span data-ttu-id="0e5ff-336">`Evaluate` メソッドに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-336">Add the following code to the `Evaluate` method:</span></span>

[!code-csharp[LoadTestDataset](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadTestDataset)]

<span data-ttu-id="0e5ff-337">`MulticlassClassificationContext.Evaluate` は、指定されたデータセットを使用してモデルの品質メトリックを計算する <xref:Microsoft.ML.MulticlassClassificationContext.Evaluate%2A> メソッドのラッパーです。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-337">The `MulticlassClassificationContext.Evaluate` is a wrapper for the <xref:Microsoft.ML.MulticlassClassificationContext.Evaluate%2A> method that computes the quality metrics for the model using the specified dataset.</span></span> <span data-ttu-id="0e5ff-338">これによって返される <xref:Microsoft.ML.Data.MultiClassClassifierMetrics> オブジェクトには、多クラス分類評価器によって計算されるメトリック全体が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-338">It returns a <xref:Microsoft.ML.Data.MultiClassClassifierMetrics> object that contains the overall metrics computed by multiclass classification evaluators.</span></span>
<span data-ttu-id="0e5ff-339">これらを表示してモデルの品質を判定するには、最初にメトリックを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-339">To display these to determine the quality of the model, you need to get the metrics first.</span></span>
<span data-ttu-id="0e5ff-340">特徴を入力し、予測を戻す、機械学習の `_trainedModel` グローバル変数 (変換器) の `Transform` メソッドの使用法に注目してください。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-340">Notice the use of the `Transform` method of the machine learning `_trainedModel` global variable (a transformer) to input the features and return predictions.</span></span> <span data-ttu-id="0e5ff-341">`Evaluate` メソッドに次のコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-341">Add the following code to the `Evaluate` method as the next line:</span></span>

[!code-csharp[Evaluate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Evaluate)]

<span data-ttu-id="0e5ff-342">多クラス分類では、次のメトリックが評価されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-342">The following metrics are evaluated for multiclass classification:</span></span>

* <span data-ttu-id="0e5ff-343">マイクロ精度: すべてのサンプルとクラスのペアが、精度メトリックに均等に作用します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-343">Micro Accuracy - Every sample-class pair contributes equally to the accuracy metric.</span></span>  <span data-ttu-id="0e5ff-344">マイクロ精度は可能な限り 1 に近づけます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-344">You want Micro Accuracy to be as close to 1 as possible.</span></span>

* <span data-ttu-id="0e5ff-345">マクロ精度: すべてのクラスが、精度メトリックに均等に作用します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-345">Macro Accuracy - Every class contributes equally to the accuracy metric.</span></span> <span data-ttu-id="0e5ff-346">少数派のクラスは、大規模なクラスと同じ重みが与えられています。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-346">Minority classes are given equal weight as the larger classes.</span></span> <span data-ttu-id="0e5ff-347">マクロ精度は可能な限り 1 に近づけます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-347">You want Macro Accuracy to be as close to 1 as possible.</span></span>

* <span data-ttu-id="0e5ff-348">対数損失: [対数損失](../resources/glossary.md#log-loss)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-348">Log-loss - see [Log Loss](../resources/glossary.md#log-loss).</span></span> <span data-ttu-id="0e5ff-349">対数損失は可能な限り 1 に近づけます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-349">You want Log-loss to be as close to zero as possible.</span></span>

* <span data-ttu-id="0e5ff-350">対数損失還元: 範囲は [-inf, 100] です。ここで、100 は完璧な予測で、0 は平均の予測です。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-350">Log-loss reduction - Ranges from [-inf, 100], where 100 is perfect predictions and 0 indicates mean predictions.</span></span> <span data-ttu-id="0e5ff-351">対数損失還元は可能な限り 1 に近づけます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-351">You want Log-loss reduction to be as close to zero as possible.</span></span>

### <a name="displaying-the-metrics-for-model-validation"></a><span data-ttu-id="0e5ff-352">モデル検証のためのメトリックを表示する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-352">Displaying the metrics for model validation</span></span>

<span data-ttu-id="0e5ff-353">次のコードを使用してメトリックを表示し、結果を共有し、それに対してアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-353">Use the following code to display the metrics, share the results, and then act on them:</span></span>

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DisplayMetrics)]

## <a name="predict-the-test-data-outcome-with-the-saved-model"></a><span data-ttu-id="0e5ff-354">保存したモデルを使用してテスト データの結果を予測する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-354">Predict the test data outcome with the saved model</span></span>

<span data-ttu-id="0e5ff-355">`Evaluate` メソッドの呼び出しのすぐ下に、次のコードを使用して、`Main` メソッドからの新しいメソッドの呼び出しを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-355">Add a call to the new method from the `Main` method, right under the `Evaluate` method call, using the following code:</span></span>

[!code-csharp[CallPredictIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallPredictIssue)]

<span data-ttu-id="0e5ff-356">`Evaluate` メソッドの直後に、次のコードを使用して `PredictIssue` メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-356">Create the `PredictIssue` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void PredictIssue()
{

}
```

<span data-ttu-id="0e5ff-357">`PredictIssue` メソッドは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-357">The `PredictIssue` method executes the following tasks:</span></span>

* <span data-ttu-id="0e5ff-358">テスト データの問題を 1 つ作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-358">Creates a single issue of test data.</span></span>
* <span data-ttu-id="0e5ff-359">テスト データに基づいて区分を予測します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-359">Predicts Area based on test data.</span></span>
* <span data-ttu-id="0e5ff-360">テスト データと予測をレポート用に結合する。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-360">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="0e5ff-361">予測された結果を表示する。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-361">Displays the predicted results.</span></span>

<span data-ttu-id="0e5ff-362">まず、次のコードを使用して、先ほど保存したモデルを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-362">First, load the model that you saved previously with the following code:</span></span>

[!code-csharp[LoadModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadModel)]

<span data-ttu-id="0e5ff-363">GitHub の問題を追加して、`Predict` メソッドでトレーニングされたモデルの予測をテストします。これには `GitHubIssue` のインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-363">Add a GitHub issue to test the trained model's prediction in the `Predict` method by creating an instance of `GitHubIssue`:</span></span>

[!code-csharp[AddTestIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddTestIssue)]

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine)]
  
<span data-ttu-id="0e5ff-364">これでモデルがあるので、それを使用して GitHub の問題データの 1 インスタンスの区分 GitHub ラベルを予測できます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-364">Now that you have a model, you can use that to predict the Area GitHub label of a single instance of the GitHub issue data.</span></span> <span data-ttu-id="0e5ff-365">予測を取得するには、データに対して <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-365">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="0e5ff-366">入力データは文字列であり、モデルには、特徴付けが含まれることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-366">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="0e5ff-367">トレーニングと予測の間は、パイプラインが同期されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-367">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="0e5ff-368">予測のために前処理/特徴付けのコードを特別に記述する必要はなく、同じ API によってバッチと 1 回限りの予測の両方が処理されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-368">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span> <span data-ttu-id="0e5ff-369">予測のために `PredictIssue` メソッドに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-369">Add the following code to the `PredictIssue` method for the predictions:</span></span>

[!code-csharp[PredictIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine)]

### <a name="model-operationalization-prediction"></a><span data-ttu-id="0e5ff-370">モデルの運用化: 予測</span><span class="sxs-lookup"><span data-stu-id="0e5ff-370">Model operationalization: prediction</span></span>

<span data-ttu-id="0e5ff-371">問題を分類し、それに応じて処理するために `Area` を表示します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-371">Display `Area` in order to categorize the issue and act on it accordingly.</span></span> <span data-ttu-id="0e5ff-372">これは運用化と呼ばれ、返されたデータを運用ポリシーとして使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-372">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="0e5ff-373">次の <xref:System.Console.WriteLine?displayProperty=nameWithType> コードを使用して、結果の表示を作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-373">Create a display for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[DisplayResults](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DisplayResults)]

## <a name="results"></a><span data-ttu-id="0e5ff-374">結果</span><span class="sxs-lookup"><span data-stu-id="0e5ff-374">Results</span></span>

<span data-ttu-id="0e5ff-375">結果は以下のようになるはずです。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-375">Your results should be similar to the following.</span></span> <span data-ttu-id="0e5ff-376">パイプラインが処理されると、メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-376">As the pipeline processes, it displays messages.</span></span> <span data-ttu-id="0e5ff-377">警告または処理メッセージが表示されることがありますが、</span><span class="sxs-lookup"><span data-stu-id="0e5ff-377">You may see warnings, or processing messages.</span></span> <span data-ttu-id="0e5ff-378">わかりやすくするために、それらは次の結果から削除してあります。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-378">These have been removed from the following results for clarity.</span></span>

```console
=============== Single Prediction just-trained-model - Result: area-System.Net ===============
The model is saved to C:\Users\johalex\dotnet-samples\samples\machine-learning\tutorials\GitHubIssueClassification\bin\Debug\netcoreapp2.0\..\..\..\Models\model.zip
*************************************************************************************************************
*       Metrics for Multi-class Classification model - Test Data
*------------------------------------------------------------------------------------------------------------
*       MicroAccuracy:    0.74
*       MacroAccuracy:    0.687
*       LogLoss:          .932
*       LogLossReduction: 63.852
*************************************************************************************************************
=============== Single Prediction - Result: area-System.Data ===============
```

<span data-ttu-id="0e5ff-379">おめでとうございます! </span><span class="sxs-lookup"><span data-stu-id="0e5ff-379">Congratulations!</span></span> <span data-ttu-id="0e5ff-380">これで、GitHub の問題用の区分ラベルを分類および予測するための機械学習モデルをビルドできました。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-380">You've now successfully built a machine learning model for classifying and predicting an Area label for a GitHub issue.</span></span> <span data-ttu-id="0e5ff-381">このチュートリアルのソース コードは [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification) リポジトリで確認できます。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-381">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification) repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0e5ff-382">次の手順</span><span class="sxs-lookup"><span data-stu-id="0e5ff-382">Next steps</span></span>

<span data-ttu-id="0e5ff-383">このチュートリアルでは、次の作業を行う方法を学びました。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-383">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="0e5ff-384">問題を把握する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-384">Understand the problem</span></span>
> * <span data-ttu-id="0e5ff-385">適切な機械学習タスクを選択する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-385">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="0e5ff-386">データを準備する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-386">Prepare your data</span></span>
> * <span data-ttu-id="0e5ff-387">学習パイプラインを作成する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-387">Create the learning pipeline</span></span>
> * <span data-ttu-id="0e5ff-388">分類器を読み込む</span><span class="sxs-lookup"><span data-stu-id="0e5ff-388">Load a classifier</span></span>
> * <span data-ttu-id="0e5ff-389">モデルをトレーニングする</span><span class="sxs-lookup"><span data-stu-id="0e5ff-389">Train the model</span></span>
> * <span data-ttu-id="0e5ff-390">別のデータ セットを使用してモデルを評価する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-390">Evaluate the model with a different dataset</span></span>
> * <span data-ttu-id="0e5ff-391">モデルを使用してテスト データの結果を予測する</span><span class="sxs-lookup"><span data-stu-id="0e5ff-391">Predict the test data outcomes with the model</span></span>

<span data-ttu-id="0e5ff-392">さらに詳しく学習するには、次のチュートリアルに進んでください。</span><span class="sxs-lookup"><span data-stu-id="0e5ff-392">Advance to the next tutorial to learn more</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="0e5ff-393">タクシー代予測</span><span class="sxs-lookup"><span data-stu-id="0e5ff-393">Taxi Fare Predictor</span></span>](taxi-fare.md)
