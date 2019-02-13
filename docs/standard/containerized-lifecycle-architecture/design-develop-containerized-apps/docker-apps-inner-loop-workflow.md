---
title: Docker アプリの内部ループ開発ワークフロー
description: Docker アプリケーションの開発の「内部ループ」ワークフローをについて説明します。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 03eb4662e55551678105fa9ef25b42cc05c132a5
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219089"
---
# <a name="inner-loop-development-workflow-for-docker-apps"></a><span data-ttu-id="7e6b7-103">Docker アプリの内部ループ開発ワークフロー</span><span class="sxs-lookup"><span data-stu-id="7e6b7-103">Inner-loop development workflow for Docker apps</span></span>

<span data-ttu-id="7e6b7-104">サイクル全体の DevOps のまたがりメモリ割り当て、外側のループのワークフローをトリガーする前に、各開発者のコンピューターで、アプリ自体のコーディングや、好みの言語またはプラットフォームを使用してローカルでテストして (図 4-14) すべてが開始されます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-104">Before triggering the outer-loop workflow spanning the entire DevOps cycle, it all begins on each developer's machine, coding the app itself, using their preferred languages or platforms, and testing it locally (Figure 4-14).</span></span> <span data-ttu-id="7e6b7-105">すべてのケースでは非常に重要なポイントに共通どのような言語、フレームワーク、またはプラットフォームを選んでも。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-105">But in every case, you will have a very important point in common, no matter what language, framework, or platforms you choose.</span></span> <span data-ttu-id="7e6b7-106">この特定のワークフローで常に開発およびがローカルで Docker コンテナーをテストします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-106">In this specific workflow, you are always developing and testing Docker containers, but locally.</span></span>

![](./media/image18.png)

<span data-ttu-id="7e6b7-107">図 4-14:内部ループ開発コンテキスト</span><span class="sxs-lookup"><span data-stu-id="7e6b7-107">Figure 4-14: Inner-loop development context</span></span>

<span data-ttu-id="7e6b7-108">コンテナーまたは Docker イメージのインスタンスは、これらのコンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-108">The container or instance of a Docker image will contain these components:</span></span>

-   <span data-ttu-id="7e6b7-109">(たとえば、Linux ディストリビューションまたは Windows)、オペレーティング システムの選択</span><span class="sxs-lookup"><span data-stu-id="7e6b7-109">An operating system selection (for example, a Linux distribution or Windows)</span></span>

-   <span data-ttu-id="7e6b7-110">(たとえば、アプリ バイナリ) の開発者によって追加されたファイル</span><span class="sxs-lookup"><span data-stu-id="7e6b7-110">Files added by the developer (for example, app binaries)</span></span>

-   <span data-ttu-id="7e6b7-111">構成 (たとえば、環境の設定との依存関係)</span><span class="sxs-lookup"><span data-stu-id="7e6b7-111">Configuration (for example, environment settings and dependencies)</span></span>

-   <span data-ttu-id="7e6b7-112">Docker で実行するどのようなプロセスの手順</span><span class="sxs-lookup"><span data-stu-id="7e6b7-112">Instructions for what processes to run by Docker</span></span>

<span data-ttu-id="7e6b7-113">(次のセクションで説明されている) プロセスとして Docker を使用する内部ループ開発ワークフローを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-113">You can set up the inner-loop development workflow that utilizes Docker as the process (described in the next section).</span></span> <span data-ttu-id="7e6b7-114">環境を設定するには、最初の手順が含まれているがないことを考慮に入れてを 1 回だけ実行する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-114">Take into account that the initial steps to set up the environment is not included, because you need to do that just once.</span></span>

## <a name="building-a-single-app-within-a-docker-container-using-visual-studio-code-and-docker-cli"></a><span data-ttu-id="7e6b7-115">Visual Studio Code と Docker CLI を使用して、Docker コンテナー内の 1 つのアプリの構築</span><span class="sxs-lookup"><span data-stu-id="7e6b7-115">Building a single app within a Docker container using Visual Studio Code and Docker CLI</span></span>

<span data-ttu-id="7e6b7-116">アプリは、独自のサービスとその他のライブラリ (依存関係) から構成されます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-116">Apps are made up from your own services plus additional libraries (dependencies).</span></span>

<span data-ttu-id="7e6b7-117">図 4-15 では、通常は各手順の詳細な説明の後に、Docker アプリを構築するときに実行するために必要な基本手順を示します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-117">Figure 4-15 shows the basic steps that you usually need to carry out when building a Docker app, followed by detailed descriptions of each step.</span></span>

![](./media/image19.png)

<span data-ttu-id="7e6b7-118">図 4-15:Docker CLI を使用してコンテナー化された Docker アプリケーションのライフ サイクルの高度なワークフロー</span><span class="sxs-lookup"><span data-stu-id="7e6b7-118">Figure 4-15: High-level workflow for the life cycle for Docker containerized applications using Docker CLI</span></span>

### <a name="step-1-start-coding-in-visual-studio-code-and-create-your-initial-appservice-baseline"></a><span data-ttu-id="7e6b7-119">手順 1: Visual Studio Code でコーディングを開始し、アプリやサービスの初期ベースラインを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-119">Step 1: Start coding in Visual Studio Code and create your initial app/service baseline</span></span>

<span data-ttu-id="7e6b7-120">アプリケーションを開発する方法は、Docker を使用しないことを行う方法とよく似ています。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-120">The way you develop your application is pretty similar to the way you do it without Docker.</span></span> <span data-ttu-id="7e6b7-121">違いは、開発中に、展開しているアプリケーションまたは (Windows や Linux VM) など、ローカル環境で配置された Docker コンテナー内で実行されているサービスをテストします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-121">The difference is that while developing, you are deploying and testing your application or services running within Docker containers placed in your local environment (like a Linux VM or Windows).</span></span>

<span data-ttu-id="7e6b7-122">**ローカル環境の設定**</span><span class="sxs-lookup"><span data-stu-id="7e6b7-122">**Setting up your local environment**</span></span>

<span data-ttu-id="7e6b7-123">Mac および Windows 用 Docker の最新バージョンでは、これまでに、Docker アプリケーションの開発よりも簡単ですし、セットアップは簡単です。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-123">With the latest versions of Docker for Mac and Windows, it's easier than ever to develop Docker applications, and the setup is straightforward.</span></span>

<span data-ttu-id="7e6b7-124">**詳細については** Docker for Windows の設定手順についてを参照してください[ https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-124">**More info** For instructions on setting up Docker for Windows, go to [https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/).</span></span>

<span data-ttu-id="7e6b7-125">Docker for Mac の設定手順については、<https://docs.docker.com/docker-for-mac/>します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-125">For instructions on setting up Docker for Mac, go to <https://docs.docker.com/docker-for-mac/>.</span></span>

<span data-ttu-id="7e6b7-126">さらに、実際に Docker CLI を使用しているときにアプリケーションを開発することができるように、コード エディターが必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-126">In addition, you'll need a code editor so that you can actually develop your application while using Docker CLI.</span></span>

<span data-ttu-id="7e6b7-127">Microsoft は、Visual Studio Code では、軽量なコード エディターは、Mac、Windows、および Linux でサポートされ、IntelliSense を提供しますです[多くの言語サポート](https://code.visualstudio.com/docs/languages/overview)(JavaScript、.NET、Go、Java、Ruby、Python、およびほとんど最新の言語の)[デバッグ](https://code.visualstudio.com/Docs/editor/debugging)、 [Git との統合](https://code.visualstudio.com/Docs/editor/versioncontrol)と[拡張機能のサポート](https://code.visualstudio.com/docs/extensions/overview)します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-127">Microsoft provides Visual Studio Code, which is a lightweight code editor that is supported on Mac, Windows, and Linux, and provides IntelliSense with [support for many languages](https://code.visualstudio.com/docs/languages/overview) (JavaScript, .NET, Go, Java, Ruby, Python, and most modern languages), [debugging](https://code.visualstudio.com/Docs/editor/debugging), [integration with Git](https://code.visualstudio.com/Docs/editor/versioncontrol) and [extensions support](https://code.visualstudio.com/docs/extensions/overview).</span></span> <span data-ttu-id="7e6b7-128">このエディターは、Mac および Linux の開発者に最適です。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-128">This editor is a great fit for Mac and Linux developers.</span></span> <span data-ttu-id="7e6b7-129">Windows でもに完全な Visual Studio アプリケーションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-129">In Windows, you also can use the full Visual Studio application.</span></span>

<span data-ttu-id="7e6b7-130">**詳細については** Visual Studio for Windows、Mac、または Linux をインストールする方法の詳細についてを参照してください<https://code.visualstudio.com/docs/setup/setup-overview/>します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-130">**More info** For instructions on installing Visual Studio for Windows, Mac, or Linux, go to <https://code.visualstudio.com/docs/setup/setup-overview/>.</span></span>

<span data-ttu-id="7e6b7-131">Docker CLI を使用して、コード エディターを使用してコードを記述が Visual Studio Code を使用する場合、Dockerfile を作成することが容易と docker compose.yml ファイル ワークスペースでします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-131">You can work with Docker CLI and write your code using any code editor, but if you use Visual Studio Code, it makes it easy to author Dockerfile and docker-compose.yml files in your workspace.</span></span> <span data-ttu-id="7e6b7-132">さらに、メッセージの下に、Docker CLI を使用して、詳細な操作を実行できるスクリプトを表示する IDE から Visual Studio Code のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-132">Plus, you can run Visual Studio Code tasks from the IDE that will prompt scripts that can be running elaborated operations using Docker CLI underneath.</span></span>

<span data-ttu-id="7e6b7-133">Visual Studio Code は、インストールする必要があります拡張機能によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-133">Visual Studio Code is provided by an extension, which you'll need to install.</span></span> <span data-ttu-id="7e6b7-134">キーを押して Ctrl + Shift + P、これを行うには、入力**ext インストール**、拡張機能を実行します。Marketplace 拡張機能の一覧を表示する拡張機能のコマンドをインストールします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-134">To do so, Press Ctrl+Shift+P, type **ext install**, and then run the Extensions: Install Extension command to bring up the Marketplace extension list.</span></span> <span data-ttu-id="7e6b7-135">次に、入力**docker**結果をフィルター処理し、図 4-16 に示すように、Dockerfile と Docker Compose ファイル (yml) サポートの拡張機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-135">Next, type **docker** to filter the results, and then select the Dockerfile And Docker Compose File (yml) Support extension, as depicted in Figure 4-16.</span></span>

![](./media/image20.png)

<span data-ttu-id="7e6b7-136">図 4-16:Visual Studio Code での Docker 拡張機能のインストール</span><span class="sxs-lookup"><span data-stu-id="7e6b7-136">Figure 4-16: Installing the Docker Extension in Visual Studio Code</span></span>

### <a name="step-2-create-a-dockerfile-related-to-an-existing-image-plain-os-or-dev-environments-like-net-core-nodejs-and-ruby"></a><span data-ttu-id="7e6b7-137">手順 2: 既存のイメージ (プレーンな OS または .NET Core、Node.js、Ruby などの開発環境) に関連する DockerFile を作成します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-137">Step 2: Create a DockerFile related to an existing image (plain OS or dev environments like .NET Core, Node.js, and Ruby)</span></span>

<span data-ttu-id="7e6b7-138">カスタム イメージを構築およびデプロイするコンテナーごとに DockerFile が必要になります、そのため、1 つのカスタム サービスのアプリが構成されている場合は、DockerFile が 1 つを必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-138">You will need a DockerFile per custom image to be built and per container to be deployed, therefore, if your app is made up of a single custom service, you will need a single DockerFile.</span></span> <span data-ttu-id="7e6b7-139">アプリが (マイクロ サービス アーキテクチャ) のように複数のサービスで構成される場合、サービスごとの 1 つの Dockerfile が必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-139">But, if your app is composed of multiple services (as in a microservices architecture), you'll need one Dockerfile per service.</span></span>

<span data-ttu-id="7e6b7-140">DockerFile では、通常は、アプリまたはサービスのルート フォルダー内に配置され、Docker を設定して、そのアプリやサービスを実行する方法を認識できるように、必要なコマンドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-140">The DockerFile is usually placed within the root folder of your app or service and contains the required commands so that Docker knows how to set up and run that app or service.</span></span> <span data-ttu-id="7e6b7-141">DockerFile を作成し、コードと共にプロジェクトに追加 (.NET Core、node.js など)、または、環境に慣れていない場合、次のヒントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-141">You can create your DockerFile and add it to your project along with your code (node.js, .NET Core, etc.), or, if you are new to the environment, take a look at the following Tip.</span></span>

> [!TIP]
> <span data-ttu-id="7e6b7-142">というコマンド ライン ツールを使用する[yo docker](https://github.com/Microsoft/generator-docker)言語を選択して、必要な Docker 構成ファイルを追加で、プロジェクトからファイルをスキャフォールディングします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-142">You can use a command-line tool called [yo docker](https://github.com/Microsoft/generator-docker), which scaffolds files from your project in the language you choose and adds the required Docker configuration files.</span></span> <span data-ttu-id="7e6b7-143">基本的には、開発者の作業の開始を支援するために作成、適切な DockerFile、docker-compose.yml とその他の関連のスクリプトをビルドして Docker コンテナーを実行します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-143">Basically, to assist developers getting started, it creates the appropriate DockerFile, docker-compose.yml, and other associated scripts to build and run your Docker containers.</span></span> <span data-ttu-id="7e6b7-144">選択した開発言語と移行先コンテナーのホストを確認するいくつかの質問はこの yeoman ジェネレーターから求められます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-144">This yeoman generator will prompt you with a few questions, asking your selected development language and destination container host.</span></span>

![yo docker](./media/image21.png)

<span data-ttu-id="7e6b7-146">たとえば、図 4-17 を示しています、端末からの 2 つのスクリーン ショットでは、Windows と Mac では、どちらの場合も、実行されている yo docker で作業を既に構成されているサンプル コード プロジェクト (.NET Core では現在、Golang、およびサポートされている言語として Node.js を使用) が生成されます。Docker の先頭。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-146">For instance, Figure 4-17 shows two screenshots from the terminals in Windows and on a Mac, in both cases, running yo docker, which will generate the sample code projects (currently .NET Core, Golang, and Node.js as supported languages) already configured to work on top of Docker.</span></span>

![](./media/image22.PNG)  ![](./media/image23.png)

<span data-ttu-id="7e6b7-147">図 4-17: yo docker コマンド ツール (左) の Windows と Mac</span><span class="sxs-lookup"><span data-stu-id="7e6b7-147">Figure 4-17: yo docker command tool in Windows (left) and on a Mac</span></span>

<span data-ttu-id="7e6b7-148">図 4-18 では、docker を使用して yo をスキャフォールディングする場所に既存の .NET Core プロジェクトを用意した後例を示します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-148">Figure 4-18 presents an example using yo docker after you have an existing .NET Core project in place to be scaffolded.</span></span>

![](./media/image24.PNG)

<span data-ttu-id="7e6b7-149">図 4-18: yo の既存の .NET Core の docker プロジェクト実施中</span><span class="sxs-lookup"><span data-stu-id="7e6b7-149">Figure 4-18: yo docker with an existing .NET Core project in place</span></span>

<span data-ttu-id="7e6b7-150">DockerFile からは、(microsoft/dotnet:1.0.0-core"から"を使用して) などに使用する基本の Docker イメージを指定します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-150">From the DockerFile, you specify what base Docker image you'll be using (like using "FROM microsoft/dotnet:1.0.0-core").</span></span> <span data-ttu-id="7e6b7-151">通常、公式のリポジトリでから取得できる基本イメージ上にカスタム イメージをビルドは、 [Docker Hub レジストリ](https://hub.docker.com/)(など、 [.NET Core のイメージ](https://hub.docker.com/r/microsoft/dotnet/)1 つまたは[for Node.js](https://hub.docker.com/_/node/)).</span><span class="sxs-lookup"><span data-stu-id="7e6b7-151">You usually will build your custom image on top of a base image that you can get from any official repository at the [Docker Hub registry](https://hub.docker.com/) (like an [image for .NET Core](https://hub.docker.com/r/microsoft/dotnet/) or one [for Node.js](https://hub.docker.com/_/node/)).</span></span>

<span data-ttu-id="7e6b7-152">***オプション a:既存の公式 Docker イメージを使用して、***</span><span class="sxs-lookup"><span data-stu-id="7e6b7-152">***Option A: Use an existing official Docker image***</span></span>

<span data-ttu-id="7e6b7-153">バージョン番号を持つ言語のスタックの公式のリポジトリを使用してにより、同じ言語機能が (開発、テスト、および運用環境を含む) すべてのコンピューターで使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-153">Using an official repository of a language stack with a version number ensures that the same language features are available on all machines (including development, testing, and production).</span></span>

<span data-ttu-id="7e6b7-154">.NET Core コンテナーのサンプル DockerFile を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-154">Following is a sample DockerFile for a .NET Core container:</span></span>

```
# Base Docker image to use
FROM microsoft/aspnetcore:1.0.1\

# Set the Working Directory and files to be copied to the image
ARG source
WORKDIR /app
COPY ${source:-bin/Release/PublishOutput} .

# Configure the listening port to 80 (Internal/Secured port within Docker host)
EXPOSE 80

# Application entry point
ENTRYPOINT ["dotnet", "MyCustomMicroservice.dll"]
```

<span data-ttu-id="7e6b7-155">この場合は、Linux microsoft/aspnetcore:1.0.1 という名前の公式の ASP.NET Core Docker イメージのバージョン 1.0.1 以降を使用しては。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-155">In this case, it is using the version 1.0.1 of the official ASP.NET Core Docker image for Linux named microsoft/aspnetcore:1.0.1.</span></span> <span data-ttu-id="7e6b7-156">詳細についてを参照してください、 [ASP.NET Core Docker イメージ ページ](https://hub.docker.com/r/microsoft/aspnetcore/)と[.NET Core Docker イメージ ページ](https://hub.docker.com/r/microsoft/dotnet/)します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-156">For further details, consult the [ASP.NET Core Docker Image page](https://hub.docker.com/r/microsoft/aspnetcore/) and the [.NET Core Docker Image page](https://hub.docker.com/r/microsoft/dotnet/).</span></span> <span data-ttu-id="7e6b7-157">でしたするイメージを使用するもう 1 つ比較可能なノード: 4 のように、Node.js、またはその他の多くの事前構成済みイメージで提供されている開発言語の onbuild [Docker Hub](https://hub.docker.com/explore/)。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-157">You also could be using another comparable image like node:4-onbuild for Node.js, or many other preconfigured images for development languages, which are available at [Docker Hub](https://hub.docker.com/explore/).</span></span>

<span data-ttu-id="7e6b7-158">DockerFile では、(ポート 80) などの実行時に使用する TCP ポートをリッスンするように Docker に指示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-158">In the DockerFile, you also need to instruct Docker to listen to the TCP port that you will use at runtime (such as port 80).</span></span>

<span data-ttu-id="7e6b7-159">Docker は、アプリを実行する方法を認識できるように、DockerFile を使用している言語/フレームワークに応じてで追加できる構成の他の行があります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-159">There are other lines of configuration that you can add in the DockerFile depending on the language/framework you are using, so Docker knows how to run the app.</span></span> <span data-ttu-id="7e6b7-160">たとえば、必要があるのでは、ENTRYPOINT 行\["dotnet"、"MyCustomMicroservice.dll"\]をビルドして、サービスの実行方法によっては、複数のバリアントを設定できますが、.NET Core アプリを実行します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-160">For instance, you need the ENTRYPOINT line with \["dotnet", "MyCustomMicroservice.dll"\] to run a .NET Core app, although you can have multiple variants depending on the approach to build and run your service.</span></span> <span data-ttu-id="7e6b7-161">SDK と dotnet CLI をビルドして、.NET アプリの実行を使用している場合は、若干異なるがなります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-161">If you're using the SDK and dotnet CLI to build and run the .NET app, it would be slightly different.</span></span> <span data-ttu-id="7e6b7-162">一番下の行は、ENTRYPOINT 行と行が追加されるアプリケーション用に選択した言語とプラットフォームによって異なります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-162">The bottom line is that the ENTRYPOINT line plus additional lines will be different depending on the language/platform you choose for your application.</span></span>

<span data-ttu-id="7e6b7-163">**詳細については** .NET Core アプリケーション用の Docker イメージを構築する方法の詳細についてを参照してください<https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images>します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-163">**More info** For information about building Docker images for .NET Core applications, go to <https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images>.</span></span>

<span data-ttu-id="7e6b7-164">詳細については、独自のイメージを構築するには[ https://docs.docker.com/engine/\ チュートリアル/dockerimages/](https://docs.docker.com/engine/tutorials/dockerimages/)します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-164">To learn more about building your own images, go to [https://docs.docker.com/engine/\ tutorials/dockerimages/](https://docs.docker.com/engine/tutorials/dockerimages/).</span></span>

<span data-ttu-id="7e6b7-165">**マルチプラット フォームのイメージ リポジトリ**</span><span class="sxs-lookup"><span data-stu-id="7e6b7-165">**Multiplatform image repositories**</span></span>

<span data-ttu-id="7e6b7-166">Windows コンテナーより一般的になると、1 つのリポジトリは、Linux および Windows のイメージなどのプラットフォーム バリアントを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-166">As Windows containers become more prevalent, a single repository can contain platform variants, such as a Linux and Windows image.</span></span> <span data-ttu-id="7e6b7-167">これにより、複数のプラットフォームを対象に 1 つのリポジトリを使用する仕入先の Docker で新機能は、 [microsoft/aspdotnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) DockerHub レジストリでは使用できるリポジトリ。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-167">This is a new feature coming in Docker that makes it possible for vendors to use a single repository to cover multiple platforms, such as [microsoft/aspdotnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) repository, which is available at DockerHub registry.</span></span> <span data-ttu-id="7e6b7-168">ように、この機能は、アライブに関しては、Windows ホストからのこのイメージのプルをプルする、Windows バリアントは、Linux バリアントがプルは Linux ホストから同じイメージ名を取得します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-168">As the feature comes alive, pulling this image from a Windows host will pull the Windows variant, whereas pulling the same image name from a Linux host will pull the Linux variant.</span></span>

<span data-ttu-id="7e6b7-169">***オプション b:最初から基本イメージを作成します。***</span><span class="sxs-lookup"><span data-stu-id="7e6b7-169">***Option B: Create your base image from scratch***</span></span>

<span data-ttu-id="7e6b7-170">これで説明したように、最初から、独自の Docker 基本イメージを作成することができます[記事](https://docs.docker.com/engine/userguide/eng-image/baseimages/)Docker から。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-170">You can create your own Docker base image from scratch as explained in this [article](https://docs.docker.com/engine/userguide/eng-image/baseimages/) from Docker.</span></span> <span data-ttu-id="7e6b7-171">これはシナリオですが、Docker を使い始めたばかりの場合に適していない可能性がありますが、基本イメージの特定のビットを設定する場合は、行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-171">This is a scenario that is probably not best for you if you are just starting with Docker, but if you want to set the specific bits of your own base image, you can do it.</span></span>

### <a name="step-3-create-your-custom-docker-images-embedding-your-service-in-it"></a><span data-ttu-id="7e6b7-172">手順 3: これで、サービスを埋め込み、カスタム Docker イメージを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-172">Step 3: Create your custom Docker images embedding your service in it</span></span>

<span data-ttu-id="7e6b7-173">サービスごとにカスタム アプリを構成するには、関連するイメージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-173">For each custom service that comprises your app, you'll need to create a related image.</span></span> <span data-ttu-id="7e6b7-174">1 つのサービスまたは web アプリのアプリが構成されている場合は、1 つのイメージを必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-174">If your app is made up of a single service or web app, you'll need just a single image.</span></span>

> [!NOTE]
> <span data-ttu-id="7e6b7-175">「外側のループ DevOps ワークフロー」を考慮に入れて、イメージから作成されるビルド プロセスを自動化して、イメージはグローバル環境で作成できるように、Git リポジトリ (継続的インテグレーション) に、ソース コードをプッシュするたびに、ソース コードです。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-175">When taking into account the "outer-loop DevOps workflow," the images will be created by an automated build process whenever you push your source code to a Git repository (Continuous Integration) so the images will be created in that global environment from your source code.</span></span>

<span data-ttu-id="7e6b7-176">ただし、その外側のループのルートに、検討する前に、Docker アプリケーションが実際に正しく動作するソース管理システム (Git など) が正しく動作しないコードをプッシュしないようにすることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-176">But, before we consider going to that outer-loop route, we need to ensure that the Docker application is actually working properly so that they don't push code that might not work properly to the source control system (Git, etc.).</span></span>

<span data-ttu-id="7e6b7-177">したがって、各開発者をローカルでテストし、完全な機能をプッシュするか、ソース管理システムに変更するまでの開発を続ける全体の内側のループ処理を行う最初が必要です。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-177">Therefore, each developer first needs to do the entire inner-loop process to test locally and continue developing until they want to push a complete feature or change to the source control system.</span></span>

<span data-ttu-id="7e6b7-178">図 4-19 に示すよう、ローカル環境と DockerFile を使用して、イメージを作成する docker ビルド コマンドを使用することができます (を実行することも、docker-compose up をいくつかのコンテナー/サービスによって構成されたアプリケーションのビルド)。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-178">To create an image in your local environment and using the DockerFile, you can use the docker build command, as demonstrated in Figure 4-19 (you also can run docker-compose up --build for applications composed by several containers/services).</span></span>

![](./media/image25.png)

<span data-ttu-id="7e6b7-179">図 4-19:Docker のビルドを実行しています。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-179">Figure 4-19: Running docker build</span></span>

<span data-ttu-id="7e6b7-180">まずを作成して展開可能なフォルダー実行 dotnet を使用して、コマンドを発行し、docker のビルドを実行に必要な .NET ライブラリと、必要に応じて、docker を直接実行する代わりに、プロジェクトのフォルダーから構築できます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-180">Optionally, instead of directly running docker build from the project's folder, you first can generate a deployable folder with the .NET libraries needed by using the run dotnet publish command, and then run docker build.</span></span>

<span data-ttu-id="7e6b7-181">この例で、名前 cesardl/netcore から web api マイクロ サービスで Docker イメージを作成これ-docker: 最初 (: 特定のバージョンのように、タグを 1 つ目は)。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-181">In this example, this creates a Docker image with the name cesardl/netcore-webapi-microservice-docker:first (:first is a tag, like a specific version).</span></span> <span data-ttu-id="7e6b7-182">複数のコンテナーで、構成した Docker アプリケーションを作成する必要がある各カスタム イメージでは、この手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-182">You can take this step for each custom image you need to create for your composed Docker application with several containers.</span></span>

<span data-ttu-id="7e6b7-183">既存のイメージで見つかりますローカル リポジトリ (開発用コンピューター)、docker を使用してイメージのコマンドを図 4-20 に示すようにします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-183">You can find the existing images in your local repository (your development machine) by using the docker images command, as illustrated in Figure 4-20.</span></span>

![](./media/image26.png)

<span data-ttu-id="7e6b7-184">図 4-20:Docker イメージを使用して既存のイメージを表示します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-184">Figure 4-20: Viewing existing images using docker images</span></span>

### <a name="step-4-optional-define-your-services-in-docker-composeyml-when-building-a-composed-docker-app-with-multiple-services"></a><span data-ttu-id="7e6b7-185">手順 4: (省略可能)複数のサービスで構成された Docker アプリを構築するときに docker compose.yml で、サービスを定義します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-185">Step 4: (Optional) Define your services in docker-compose.yml when building a composed Docker app with multiple services</span></span>

<span data-ttu-id="7e6b7-186">Docker compose.yml ファイルを使用して、次のセクションの手順で説明されている展開コマンドを使用して、構成されたアプリケーションとしてデプロイに関連するサービスのセットを定義できます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-186">With the docker-compose.yml file you can define a set of related services to be deployed as a composed application with the deployment commands explained in the next step section.</span></span>

<span data-ttu-id="7e6b7-187">そのファイルでメインまたはルート ソリューション フォルダーを作成する必要があります。次の docker compose.yml ファイルに類似のコンテンツになります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-187">You need to create that file in your main or root solution folder; it should have a similar content to the following docker-compose.yml file:</span></span>

```yml
version: '2'
services:
  web:
    build: .
    ports:
     - "81:80"
    volumes:
     - .:/code
    depends_on:
     - redis
  redis:
    image: redis
```

<span data-ttu-id="7e6b7-188">このケースでこのファイルは 2 つのサービスを定義します。 web サービス (カスタム サービス) と、redis サービス (一般的なキャッシュ サービス)。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-188">In this particular case, this file defines two services: the web service (your custom service) and the redis service (a popular cache service).</span></span> <span data-ttu-id="7e6b7-189">各サービスは、各具象の Docker イメージを使用する必要があります、コンテナーとしてデプロイされます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-189">Each service will be deployed as a container, so we need to use a concrete Docker image for each.</span></span> <span data-ttu-id="7e6b7-190">この特定の web サービスのイメージは、以下を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-190">For this particular web service, the image will need to do the following:</span></span>

-   <span data-ttu-id="7e6b7-191">現在のディレクトリに DockerFile からビルドします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-191">Build from the DockerFile in the current directory</span></span>

-   <span data-ttu-id="7e6b7-192">公開されているポート 80 をコンテナー ホスト コンピューター上でポート 81 上での転送します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-192">Forward the exposed port 80 on the container to port 81 on the host machine</span></span>

-   <span data-ttu-id="7e6b7-193">イメージを再構築することがなく、コードを変更することができるので、コンテナー内で指定するホスト上のプロジェクト ディレクトリをマウントします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-193">Mount the project directory on the host to /code within the container, making it possible for you to modify the code without having to rebuild the image</span></span>

-   <span data-ttu-id="7e6b7-194">Redis サービスに web サービスをリンクします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-194">Link the web service to the redis service</span></span>

<span data-ttu-id="7e6b7-195">Redis サービスの使用、[最新のパブリック redis イメージ](https://hub.docker.com/_/redis/)Docker Hub レジストリからプルします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-195">The redis service uses the [latest public redis image](https://hub.docker.com/_/redis/) pulled from the Docker Hub registry.</span></span> <span data-ttu-id="7e6b7-196">[redis](https://redis.io/)はサーバー側アプリケーションでの非常に人気のあるキャッシュ システムです。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-196">[redis](https://redis.io/) is a very popular cache system for server-side applications.</span></span>

### <a name="step-5-build-and-run-your-docker-app"></a><span data-ttu-id="7e6b7-197">手順 5: ビルドして Docker アプリの実行</span><span class="sxs-lookup"><span data-stu-id="7e6b7-197">Step 5: Build and run your Docker app</span></span>

<span data-ttu-id="7e6b7-198">アプリに 1 つのコンテナーのみがある場合だけ、Docker ホスト (VM または物理サーバー) にデプロイして実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-198">If your app has only a single container, you just need to run it by deploying it to your Docker Host (VM or physical server).</span></span> <span data-ttu-id="7e6b7-199">ただし、複数のサービス、アプリが構成されている場合をする必要があります*組み立てること*もします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-199">However, if your app is made up of multiple services, you need to *compose it*, too.</span></span> <span data-ttu-id="7e6b7-200">さまざまなオプションを見てみましょう。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-200">Let's see the different options.</span></span>

<span data-ttu-id="7e6b7-201">***オプション a:1 つのコンテナーまたはサービスを実行します。***</span><span class="sxs-lookup"><span data-stu-id="7e6b7-201">***Option A: Run a single container or service***</span></span>

<span data-ttu-id="7e6b7-202">次に示すように docker run コマンドを使用して、Docker イメージを実行できます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-202">You can run the Docker image by using the docker run command, as shown here:</span></span>

```
docker run -t -d -p 80:5000
cesardl/netcore-webapi-microservice-docker:first
```

<span data-ttu-id="7e6b7-203">この配置のいます 要求をリダイレクトする内部ポート 5000 をポート 80 に送信されるに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-203">Note that for this particular deployment, we'll be redirecting requests sent to port 80 to the internal port 5000.</span></span> <span data-ttu-id="7e6b7-204">ここで、アプリケーションは外部ポート、ホスト レベル 80 でリッスンします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-204">Now, the application is listening on the external port 80 at the host level.</span></span>

<span data-ttu-id="7e6b7-205">***オプション b:構成して複数コンテナー アプリケーションの実行***</span><span class="sxs-lookup"><span data-stu-id="7e6b7-205">***Option B: Compose and run a multiple-container application***</span></span>

<span data-ttu-id="7e6b7-206">ほとんどのエンタープライズ シナリオでは、Docker アプリケーションを複数のサービスはから構成します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-206">In most enterprise scenarios, a Docker application will be composed of multiple services.</span></span> <span data-ttu-id="7e6b7-207">コマンドを実行するような場合、docker compose を (図 4-21)、以前作成した可能性があります、docker-compose.yml ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-207">For these cases, you can run the command docker-compose up (Figure 4-21), which will use the docker-compose.yml file that you might have created previously.</span></span> <span data-ttu-id="7e6b7-208">このコマンドを実行するには、すべての関連するコンテナーの構成済みのアプリケーションはデプロイします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-208">Running this command deploys a composed application with all of its related containers.</span></span>

![](./media/image27.png)

<span data-ttu-id="7e6b7-209">図 4-21:"、Docker-compose up"コマンドの実行結果</span><span class="sxs-lookup"><span data-stu-id="7e6b7-209">Figure 4-21: Results of running the "docker-compose up" command</span></span>

<span data-ttu-id="7e6b7-210">Docker を実行した後、compose をデプロイする必要が、アプリケーションとその関連コンテナー、Docker ホストに VM の表記で図 4-22 に示すようにします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-210">After you run docker-compose up, you deploy your application and its related container(s) into your Docker Host, as illustrated in Figure 4-22, in the VM representation.</span></span>

![](./media/image28.png)

<span data-ttu-id="7e6b7-211">図 4-22:Docker コンテナーが展開された VM</span><span class="sxs-lookup"><span data-stu-id="7e6b7-211">Figure 4-22: VM with Docker containers deployed</span></span>

<span data-ttu-id="7e6b7-212">注、docker-compose up および docker の実行は、開発環境で、コンテナーをテストするための十分に可能性がありますがないそれらを使用するすべての場合は、Docker クラスターの操作を想定しているし、Docker Swarm、Mesosphere DC/OS、または Kubernetes などのオーケストレータースケール アップできるようにするには。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-212">Note docker-compose up and docker run might be enough for testing your containers in your development environment, but you might not use them at all if you are expecting to work with Docker clusters and orchestrators like Docker Swarm, Mesosphere DC/OS, or Kubernetes in order to be able to scale up.</span></span> <span data-ttu-id="7e6b7-213">などのクラスターを使用している場合[Docker Swarm mode](https://docs.docker.com/engine/swarm/)デプロイし、した場合など、docker サービスを 1 つのサービスの作成やその他のコマンドでテストに必要な (可能で、Docker for Windows と Mac バージョン 1.12 以降)、複数のコンテナーから成るアプリを展開するには、docker を使用してバンドルの作成し、docker は、情報の記事で説明したように、スタックとして構成済みのアプリを展開することで、myBundleFile をデプロイ[分散アプリケーション バンドル](https://blog.docker.com/2016/06/docker-app-bundle/)Docker から。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-213">If you're using a cluster like [Docker Swarm mode](https://docs.docker.com/engine/swarm/) (available in Docker for Windows and Mac since version 1.12), you need to deploy and test with additional commands such as docker service create for single services, or when you're deploying an app composed of several containers, using docker compose bundle and docker deploy myBundleFile, by deploying the composed app as a stack, as explained in the article [Distributed Application Bundles](https://blog.docker.com/2016/06/docker-app-bundle/) from Docker.</span></span>

<span data-ttu-id="7e6b7-214">[DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/)と[Kubernetes](https://kubernetes.io/docs/user-guide/deployments/#creating-a-deployment)さまざまな展開コマンドと、スクリプトを使用します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-214">For [DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) and [Kubernetes](https://kubernetes.io/docs/user-guide/deployments/#creating-a-deployment) you would use different deployment commands and scripts, as well.</span></span>

### <a name="step-6-test-your-docker-application-locally-in-your-local-cd-vm"></a><span data-ttu-id="7e6b7-215">手順 6: (ローカル CD VM) では、ローカルで Docker アプリケーションをテストします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-215">Step 6: Test your Docker application (locally, in your local CD VM)</span></span>

<span data-ttu-id="7e6b7-216">この手順は、アプリの実行内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-216">This step will vary depending on what your app is doing.</span></span>

<span data-ttu-id="7e6b7-217">非常に単純な .NET Core Web API の"Hello World"を 1 つのコンテナーまたはサービスとしてデプロイされている場合、DockerFile で指定された TCP ポートを提供することで、サービスにアクセスするとだけです。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-217">In a very simple .NET Core Web API "Hello World" deployed as a single container or service, you'd just need to access the service by providing the TCP port specified in the DockerFile.</span></span>

<span data-ttu-id="7e6b7-218">サービスに移動する localhost が有効でない場合は、このコマンドを使用して、マシンの IP アドレスを検索します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-218">If localhost is not turned on, to navigate to your service, find the IP address for the machine by using this command:</span></span>

<span data-ttu-id="7e6b7-219">docker-machine ip *your-container-name*</span><span class="sxs-lookup"><span data-stu-id="7e6b7-219">docker-machine ip *your-container-name*</span></span>

<span data-ttu-id="7e6b7-220">Docker ホストでは、ブラウザーを開いて、そのサイトに移動します図 4-23 に示すようにアプリ/サービスを実行して、参照してください必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-220">On the Docker host, open a browser and navigate to that site; you should see your app/service running, as demonstrated in Figure 4-23.</span></span>

![](./media/image29.png)

<span data-ttu-id="7e6b7-221">図 4-23:Localhost を使用してローカルで Docker アプリケーションのテスト</span><span class="sxs-lookup"><span data-stu-id="7e6b7-221">Figure 4-23: Testing your Docker application locally using localhost</span></span>

<span data-ttu-id="7e6b7-222">前に説明したように、実行するには、docker で展開された方法であるためですはポート 80 が使用が内部的にはポート 5000 にリダイレクトされましたされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-222">Note that it is using port 80, but internally it was being redirected to port 5000, because that's how it was deployed with docker run, as explained earlier.</span></span>

<span data-ttu-id="7e6b7-223">これは、CURL を使用して、ターミナルから、テストできます。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-223">You can test this by using CURL from the terminal.</span></span> <span data-ttu-id="7e6b7-224">図 4-24 に示すように、Windows で Docker のインストールでは、既定の IP、10.0.75.1、です。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-224">In a Docker installation on Windows, the default IP is 10.0.75.1, as depicted in Figure 4-24.</span></span>

![](./media/image30.png)

<span data-ttu-id="7e6b7-225">図 4-24:CURL を使用してローカルの Docker アプリケーションのテスト</span><span class="sxs-lookup"><span data-stu-id="7e6b7-225">Figure 4-24: Testing a Docker application locally by using CURL</span></span>

<span data-ttu-id="7e6b7-226">**Docker で実行されているコンテナーのデバッグ**</span><span class="sxs-lookup"><span data-stu-id="7e6b7-226">**Debugging a container running on Docker**</span></span>

<span data-ttu-id="7e6b7-227">Visual Studio Code は、Node.js と .NET Core コンテナーなどの他のプラットフォームを使用している場合に、Docker のデバッグをサポートします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-227">Visual Studio Code supports debugging Docker if you're using Node.js and other platforms like .NET Core containers.</span></span>

<span data-ttu-id="7e6b7-228">デバッグすることもできます Docker で .NET Core コンテナー、Visual Studio を使用する場合、次のセクションで説明されているとします。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-228">You also can debug .NET Core containers in Docker when using Visual Studio, as described in the next section.</span></span>

<span data-ttu-id="7e6b7-229">**詳細情報:** Node.js の Docker コンテナーのデバッグに関する詳細については、するには<https://blog.docker.com/2016/07/live-debugging-docker/>と[https://blogs.msdn.microsoft.com/\ユーザー\_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/](https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/)します。</span><span class="sxs-lookup"><span data-stu-id="7e6b7-229">**More info:** To learn more about debugging Node.js Docker containers, go to <https://blog.docker.com/2016/07/live-debugging-docker/> and [https://blogs.msdn.microsoft.com/\ user\_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/](https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/).</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="7e6b7-230">[前へ](docker-apps-development-environment.md)
>[次へ](visual-studio-tools-for-docker.md)</span><span class="sxs-lookup"><span data-stu-id="7e6b7-230">[Previous](docker-apps-development-environment.md)
[Next](visual-studio-tools-for-docker.md)</span></span>