---
title: Visual Studio Tools for Docker (Windows で Visual Studio) を使用
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: af14c92ab27885deec878dc33e7b94035f43e65b
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2018
ms.locfileid: "46488952"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a><span data-ttu-id="16e4b-103">Visual Studio Tools for Docker (Windows で Visual Studio) を使用</span><span class="sxs-lookup"><span data-stu-id="16e4b-103">Using Visual Studio Tools for Docker (Visual Studio on Windows)</span></span>

<span data-ttu-id="16e4b-104">Visual Studio Code と Docker CLI を使用する場合は、Docker を Visual Studio Tools を使用する場合は、開発ワークフローをワークフローに似ています。</span><span class="sxs-lookup"><span data-stu-id="16e4b-104">The development workflow when using Visual Studio Tools for Docker is similar to the workflow when using Visual Studio Code and Docker CLI.</span></span> <span data-ttu-id="16e4b-105">実際には、同じの Docker CLI に基づきますが容易に開始、プロセスを簡略化、および生産性の向上を提供します、ビルドの実行、およびタスクを構成します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-105">In fact, it's based on the same Docker CLI, but it's easier to get started, simplifies the process, and provides greater productivity for the build, run, and compose tasks.</span></span> <span data-ttu-id="16e4b-106">実行し、f5 キーを押して、Visual Studio から ctrl キーを押しながら f5 キーなどの単純なアクションを使用してコンテナーをデバッグすることもできます。</span><span class="sxs-lookup"><span data-stu-id="16e4b-106">It's also able to execute and debug your containers via simple actions like F5 and Ctrl+F5 from Visual Studio.</span></span> <span data-ttu-id="16e4b-107">実行し、1 つのコンテナーをデバッグできることに加え、省略可能なコンテナー オーケストレーションのサポートは、実行し、コンテナー (ソリューション全体) のグループを同時にデバッグできます。</span><span class="sxs-lookup"><span data-stu-id="16e4b-107">With the optional container orchestration support, in addition to being able to run and debug a single container, you can run and debug a group of containers (a whole solution) at the same time.</span></span> <span data-ttu-id="16e4b-108">同じコンテナーを定義するだけ*docker compose.yml*ソリューション レベルでのファイル。</span><span class="sxs-lookup"><span data-stu-id="16e4b-108">Just define the containers in the same *docker-compose.yml* file at the solution level.</span></span>

## <a name="configuring-your-local-environment"></a><span data-ttu-id="16e4b-109">ローカル環境を構成します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-109">Configuring your local environment</span></span>

<span data-ttu-id="16e4b-110">Docker のサポートは、インストールされている .NET と .NET Core のワークロードのいずれかで Visual Studio 2017 に含まれます。</span><span class="sxs-lookup"><span data-stu-id="16e4b-110">Docker support is included in Visual Studio 2017 with any of the .NET and .NET Core workloads installed.</span></span> <span data-ttu-id="16e4b-111">Docker for Windows を個別にインストールします。</span><span class="sxs-lookup"><span data-stu-id="16e4b-111">Install Docker for Windows separately.</span></span>

<span data-ttu-id="16e4b-112">Docker for Windows の最新バージョンでは、これまでにアプリケーションを開発 Docker、次の参照で説明したように、セットアップは簡単なためより簡単になります。</span><span class="sxs-lookup"><span data-stu-id="16e4b-112">With the latest versions of Docker for Windows, it is easier than ever to develop Docker applications because the setup is straightforward, as explained in the following references.</span></span>

<span data-ttu-id="16e4b-113">**詳細情報:** Docker for Windows をインストールする方法の詳細については、するには<https://docs.docker.com/docker-for-windows/>します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-113">**More info:** To learn more about installing Docker for Windows, go to <https://docs.docker.com/docker-for-windows/>.</span></span>

<span data-ttu-id="16e4b-114">**詳細情報:** Visual Studio をインストールする方法の詳細についてを参照してください[ https://visualstudio.microsoft.com/downloads/](https://visualstudio.microsoft.com/downloads/)します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-114">**More info:** For instructions on installing Visual Studio, go to [https://visualstudio.microsoft.com/downloads/](https://visualstudio.microsoft.com/downloads/).</span></span>

<span data-ttu-id="16e4b-115">Visual Studio Tools for Docker をインストールする詳細を表示するには<http://aka.ms/vstoolsfordocker>と<https://docs.microsoft.com/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker>します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-115">To see more about installing Visual Studio Tools for Docker, go to <http://aka.ms/vstoolsfordocker> and <https://docs.microsoft.com/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker>.</span></span>

## <a name="using-docker-tools-in-visual-studio-2017"></a><span data-ttu-id="16e4b-116">Visual Studio 2017 での Docker ツールの使用</span><span class="sxs-lookup"><span data-stu-id="16e4b-116">Using Docker Tools in Visual Studio 2017</span></span>

<span data-ttu-id="16e4b-117">プロジェクトに Docker サポートを追加するときに (図 4-26 参照)、Visual Studio の追加、 *Dockerfile*をプロジェクトのルート。</span><span class="sxs-lookup"><span data-stu-id="16e4b-117">When adding Docker support to a project (see Figure 4-26), Visual Studio adds a *Dockerfile* to the project root.</span></span>

![Visual Studio 2017 プロジェクトでの Docker ソリューションのサポートの有効化](./media/image32.png)

<span data-ttu-id="16e4b-119">図 4-26: Visual Studio 2017 プロジェクトでの Docker ソリューションのサポートの有効化</span><span class="sxs-lookup"><span data-stu-id="16e4b-119">Figure 4-26: Turning on Docker Solution support in a Visual Studio 2017 project</span></span>

 <span data-ttu-id="16e4b-120">既定では Visual Studio 2017 バージョン 15.7 またはそれ以前で、Docker Compose を使用して、コンテナー オーケストレーションのサポートが追加されます。</span><span class="sxs-lookup"><span data-stu-id="16e4b-120">Container orchestration support, via Docker Compose, is added by default in Visual Studio 2017 versions 15.7 or earlier.</span></span> <span data-ttu-id="16e4b-121">コンテナー オーケストレーションのサポートは、Visual Studio 2017 バージョン 15.8 オプトイン機能または後で、どの場合 Docker Compose と Service Fabric がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="16e4b-121">Container orchestration support is an opt-in feature in Visual Studio 2017 versions 15.8 or later, in which case Docker Compose and Service Fabric are supported.</span></span>

<span data-ttu-id="16e4b-122">Visual Studio 15.8 およびそれ以降のバージョンを使用して、関連するコンテナーがあるソリューションで複数のプロジェクトのサポートを追加できます。</span><span class="sxs-lookup"><span data-stu-id="16e4b-122">With Visual Studio version 15.8 and later, you can add support for multiple projects in a solution that each have an associated container.</span></span> <span data-ttu-id="16e4b-123">ソリューションまたはプロジェクト ノードを右クリックして**ソリューション エクスプ ローラー**、選択**追加** > **コンテナー オーケストレーション サポート**します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-123">Right-click on the solution or project node in **Solution Explorer**, and choose **Add** > **Container Orchestration Support**.</span></span>  <span data-ttu-id="16e4b-124">クリックして**Docker Compose**または**Service Fabric**コンテナーを管理します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-124">Then choose **Docker Compose** or **Service Fabric** to manage the containers.</span></span>

<span data-ttu-id="16e4b-125">選択すると**Docker Compose**、Visual Studio でソリューションのサービス セクションを追加する*docker compose.yml*ファイル (または存在していない場合、ファイルが作成されます)。</span><span class="sxs-lookup"><span data-stu-id="16e4b-125">When you choose **Docker Compose**, Visual Studio adds a service section in your solution's *docker-compose.yml* files (or creates the files if they didn't exist).</span></span> <span data-ttu-id="16e4b-126">マルチ コンテナー ソリューションの作成を開始する簡単な方法開くことができます、 *docker compose.yml*ファイルし、その他の機能を更新します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-126">It's an easy way to begin composing your multi-container solution; you then can open the *docker-compose.yml* files and update them with additional features.</span></span>

<span data-ttu-id="16e4b-127">この操作は、必要な構成をコード行を追加します、 *docker compose.yml*ソリューション レベルで設定します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-127">This action adds the required configuration lines of code to a *docker-compose.yml* set at the solution level.</span></span>

<span data-ttu-id="16e4b-128">できます Docker サポートの Visual Studio 2017 では、ASP.NET Core プロジェクトを作成するときに図 4-27 に示すようにします。</span><span class="sxs-lookup"><span data-stu-id="16e4b-128">You also can turn on Docker support when creating an ASP.NET Core project in Visual Studio 2017, as shown in Figure 4-27.</span></span>

![プロジェクトを作成するときに Docker サポートの有効化](./media/image33.png)

<span data-ttu-id="16e4b-130">図 4-27: Docker のサポート、プロジェクトを作成するときにオン</span><span class="sxs-lookup"><span data-stu-id="16e4b-130">Figure 4-27: Turning on Docker support when creating a project</span></span>

<span data-ttu-id="16e4b-131">Visual Studio でソリューションに Docker サポートを追加した後も表示されますに新しいノード ツリー**ソリューション エクスプ ローラー**と、 *docker compose.yml*ファイル、図 4-28 に示すようにします。</span><span class="sxs-lookup"><span data-stu-id="16e4b-131">After you add Docker support to your solution in Visual Studio, you also will see a new node tree in **Solution Explorer** with the added *docker-compose.yml* files, as depicted in Figure 4-28.</span></span>

![docker compose.yml ファイルがソリューション エクスプ ローラーで表示されます。](./media/image34.PNG)

<span data-ttu-id="16e4b-133">図 4-28: docker compose.yml ファイルに表示されます**ソリューション エクスプ ローラー**</span><span class="sxs-lookup"><span data-stu-id="16e4b-133">Figure 4-28: docker-compose.yml files now display in **Solution Explorer**</span></span>

<span data-ttu-id="16e4b-134">1 つを使用して複数コンテナー アプリを展開する可能性があります*docker compose.yml*ファイルを実行する場合に`docker-compose up`ただし、Visual Studio 環境 (開発対によっての値をオーバーライドするために、それらのグループを追加します。運用環境) と実行 (リリース対デバッグ) を入力します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-134">You could deploy a multi-container app by using a single *docker-compose.yml* file when you run `docker-compose up`; however, Visual Studio adds a group of them, so you can override values depending on the environment (development versus production) and the execution type (release versus debug).</span></span> <span data-ttu-id="16e4b-135">この機能は以降の章で強化について説明します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-135">This capability is better explained in later chapters.</span></span>

<span data-ttu-id="16e4b-136">複数のコンテナーを管理するのに Docker Compose ではなく Service Fabric を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="16e4b-136">You can also use Service Fabric instead of Docker Compose to manage multiple containers.</span></span> <span data-ttu-id="16e4b-137">参照してください[チュートリアル: Azure Service Fabric への Windows コンテナーで .NET アプリケーションのデプロイ](https://docs.microsoft.com/azure/service-fabric/service-fabric-host-app-in-a-container)します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-137">See [Tutorial: Deploy a .NET application in a Windows container to Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-host-app-in-a-container).</span></span>

<span data-ttu-id="16e4b-138">**詳細情報:** サービスの実装と Visual Studio tools for Docker の使用の詳細については、次の記事を参照します。</span><span class="sxs-lookup"><span data-stu-id="16e4b-138">**More info:** For further details on the services implementation and use of Visual Studio Tools for Docker, read the following articles:</span></span>

<span data-ttu-id="16e4b-139">ビルド、デバッグ、更新、およびローカル Docker コンテナーでアプリを更新します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span><span class="sxs-lookup"><span data-stu-id="16e4b-139">Build, debug, update, and refresh apps in a local Docker container: [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span></span>

<span data-ttu-id="16e4b-140">コンテナー レジストリには、ASP.NET Core の Docker コンテナーを展開します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span><span class="sxs-lookup"><span data-stu-id="16e4b-140">Deploy an ASP.NET Core Docker container to a container registry: [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="16e4b-141">[前へ](docker-apps-inner-loop-workflow.md)
[次へ](set-up-windows-containers-with-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="16e4b-141">[Previous](docker-apps-inner-loop-workflow.md)
[Next](set-up-windows-containers-with-powershell.md)</span></span>
