---
title: Visual Studio Tools for Windows 上の Docker
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: cd140c12ef4a0187cce096e013937d5c98cd4b39
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47170796"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a><span data-ttu-id="82a91-103">Visual Studio Tools for Docker (Windows で Visual Studio) を使用</span><span class="sxs-lookup"><span data-stu-id="82a91-103">Using Visual Studio Tools for Docker (Visual Studio on Windows)</span></span>

<span data-ttu-id="82a91-104">Visual Studio Tools for Docker 開発者のワークフローは、Visual Studio Code と Docker CLI を (同じ Docker CLI に基づきます) を使用してに似ています。</span><span class="sxs-lookup"><span data-stu-id="82a91-104">The Visual Studio Tools for Docker developer workflow is similar to using Visual Studio Code and Docker CLI (it is based on the same Docker CLI).</span></span> <span data-ttu-id="82a91-105">Visual Studio Tools の Docker を開始するのにはいっそう簡単に、プロセスを簡略化され、ビルドで生産性の向上が提供、実行、およびタスクを構成します。</span><span class="sxs-lookup"><span data-stu-id="82a91-105">Visual Studio Tools for Docker makes it even easier to get started, simplifies the process, and provides greater productivity for the build, run, and compose tasks.</span></span> <span data-ttu-id="82a91-106">実行し、デバッグのような単純なアクションを使用して、コンテナー **F5**と**Ctrl**+**F5**します。</span><span class="sxs-lookup"><span data-stu-id="82a91-106">Execute and debug your containers via simple actions like **F5** and **Ctrl**+**F5**.</span></span>

> [!NOTE]
> <span data-ttu-id="82a91-107">この記事は、Windows 上の Visual Studio と Visual Studio for mac。</span><span class="sxs-lookup"><span data-stu-id="82a91-107">This article applies to Visual Studio on Windows, and not Visual Studio for Mac.</span></span>

## <a name="configure-your-local-environment"></a><span data-ttu-id="82a91-108">ローカル環境を構成します。</span><span class="sxs-lookup"><span data-stu-id="82a91-108">Configure your local environment</span></span>

<span data-ttu-id="82a91-109">Docker for Windows の最新バージョン ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/))、簡単なセットアップでは、Docker アプリケーションの開発が容易にします。</span><span class="sxs-lookup"><span data-stu-id="82a91-109">With the latest versions of Docker for Windows ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)), the straightforward setup makes it easy to develop Docker applications.</span></span>

<span data-ttu-id="82a91-110">Visual Studio 2017 では、docker のサポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="82a91-110">Docker support is included in Visual Studio 2017.</span></span> <span data-ttu-id="82a91-111">ここで Visual Studio 2017 をダウンロードします。 [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)</span><span class="sxs-lookup"><span data-stu-id="82a91-111">Download Visual Studio 2017 here: [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)</span></span>

## <a name="use-docker-tools-in-visual-studio-2017"></a><span data-ttu-id="82a91-112">Visual Studio 2017 での Docker ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="82a91-112">Use Docker Tools in Visual Studio 2017</span></span>

<span data-ttu-id="82a91-113">Docker のサポートをプロジェクトに追加することの 2 つのレベルがあります。</span><span class="sxs-lookup"><span data-stu-id="82a91-113">There are two levels of Docker support you can add to a project.</span></span> <span data-ttu-id="82a91-114">.NET Core web アプリのプロジェクトに追加できます、 *Dockerfile*に Docker サポートを有効にすると、プロジェクト ファイル。</span><span class="sxs-lookup"><span data-stu-id="82a91-114">In .NET Core web app projects, you can just add a *Dockerfile* file to the project by enabling Docker support.</span></span> <span data-ttu-id="82a91-115">次のレベルはコンテナー オーケストレーター サポートは、追加、 *Dockerfile* (まだ存在しない) 場合は、プロジェクトに、 *docker compose.yml*ソリューション レベルでのファイル。</span><span class="sxs-lookup"><span data-stu-id="82a91-115">The next level is container orchestrator support, which adds a *Dockerfile* to the project (if it doesn't already exist) and a *docker-compose.yml* file at the solution level.</span></span>

<span data-ttu-id="82a91-116">**追加** > **Docker サポート**と**追加** > **コンテナー オーケストレーター サポート**コマンドは、web アプリ プロジェクトのプロジェクト ノードの右クリック メニュー (またはコンテキスト メニュー) にある**ソリューション エクスプ ローラー**図 4-26 に示すようにします。</span><span class="sxs-lookup"><span data-stu-id="82a91-116">The **Add** > **Docker Support** and **Add** > **Container Orchestrator Support** commands are located on the right-click menu (or context menu) of the project node for a web app project in **Solution Explorer**, as shown in Figure 4-26:</span></span>

![Visual Studio での Docker サポート メニュー オプションを追加します。](media/add-docker-support-menu.png)

<span data-ttu-id="82a91-118">図 4-26: Visual Studio 2017 のプロジェクトに Docker サポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="82a91-118">Figure 4-26: Adding Docker support to a Visual Studio 2017 project</span></span>

### <a name="add-docker-support"></a><span data-ttu-id="82a91-119">Docker サポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="82a91-119">Add Docker support</span></span>

<span data-ttu-id="82a91-120">選択して、既存の .NET Core web アプリ プロジェクトに Docker サポートを追加する**追加** > **Docker サポート**で**ソリューション エクスプ ローラー**します。</span><span class="sxs-lookup"><span data-stu-id="82a91-120">You can add Docker support to an existing .NET Core web app project by selecting **Add** > **Docker Support** in **Solution Explorer**.</span></span> <span data-ttu-id="82a91-121">選択して、プロジェクトの作成時に Docker サポートを有効することも**Docker サポートを有効にする**で、**新しい ASP.NET Core Web アプリケーション**クリックした後に表示されたダイアログ ボックス**ok**で、**新しいプロジェクト** ダイアログ ボックスで、図 4-27 に示すようにします。</span><span class="sxs-lookup"><span data-stu-id="82a91-121">You can also enable Docker support during project creation by selecting **Enable Docker Support** in the **New ASP.NET Core Web Application** dialog box that opens after you click **OK** in the **New Project** dialog box, as shown in Figure 4-27.</span></span>

![Visual Studio での新しい ASP.NET Core web アプリの Docker サポートを有効にします。](./media/enable-docker-support-visual-studio.png)

<span data-ttu-id="82a91-123">図 4-27: Visual Studio 2017 でプロジェクトの作成時に Docker サポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="82a91-123">Figure 4-27: Enable Docker support during project creation in Visual Studio 2017</span></span>

<span data-ttu-id="82a91-124">Docker サポートを有効にすると、Visual Studio の追加、 *Dockerfile*ファイルをプロジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="82a91-124">When you add or enable Docker support, Visual Studio adds a *Dockerfile* file to the project.</span></span>

> [!NOTE]
> <span data-ttu-id="82a91-125">図 4-28 に示すように .NET Framework web アプリ プロジェクト (いない .NET Core web アプリのプロジェクト) のプロジェクトの作成時に Docker Compose のサポートが有効、コンテナー オーケストレーター サポートも追加されます。</span><span class="sxs-lookup"><span data-stu-id="82a91-125">When you enable Docker Compose support during project creation for a .NET Framework web app project (not a .NET Core web app project) as shown in Figure 4-28, container orchestrator support is also added.</span></span>
>
> ![Docker を有効にする .NET Framework web アプリ プロジェクトのサポートの構成](media/enable-docker-compose-support.png)

> <span data-ttu-id="82a91-127">図 4-28: Visual Studio 2017 で .NET Framework web アプリ プロジェクトでの Docker Compose のサポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="82a91-127">Figure 4-28: Enabling Docker Compose support on a .NET Framework web app project in Visual Studio 2017</span></span>

### <a name="add-container-orchestrator-support"></a><span data-ttu-id="82a91-128">コンテナー オーケストレーター サポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="82a91-128">Add container orchestrator support</span></span>

<span data-ttu-id="82a91-129">複数のコンテナー ソリューションを作成する場合は、コンテナー オーケストレーター サポートをプロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="82a91-129">When you want to compose a multicontainer solution, add container orchestrator support to your projects.</span></span> <span data-ttu-id="82a91-130">コンテナー オーケストレーター サポートを追加すると Visual Studio が追加されます、 *Dockerfile* (まだ存在しない) 場合は、プロジェクトと、グローバルに*docker compose.yml*ソリューション レベルでのファイル。</span><span class="sxs-lookup"><span data-stu-id="82a91-130">When you add container orchestrator support, Visual Studio adds a *Dockerfile* to the project (if it doesn't already exist) and a global *docker-compose.yml* file at the solution level.</span></span> <span data-ttu-id="82a91-131">これにより、実行およびで同じ定義している場合、コンテナー (ソリューション全体) のグループを同時にデバッグ*docker compose.yml*ファイル。</span><span class="sxs-lookup"><span data-stu-id="82a91-131">This lets you run and debug a group of containers (a whole solution) at the same time if they're defined in the same *docker-compose.yml* file.</span></span> <span data-ttu-id="82a91-132">場合*docker compose.yml*が既に存在する Visual Studio に必要な構成コードの行を追加するだけです。</span><span class="sxs-lookup"><span data-stu-id="82a91-132">If *docker-compose.yml* already exists, Visual Studio just adds the required lines of configuration code to it.</span></span>

<span data-ttu-id="82a91-133">プロジェクトに追加の Dockerfile を参照してくださいコンテナー オーケストレーションのサポートをプロジェクトに追加した後、 **docker compose**でソリューションに追加されたフォルダー**ソリューション エクスプ ローラー**図 4-29 に示すように。</span><span class="sxs-lookup"><span data-stu-id="82a91-133">After you add container orchestration support to your project, you see a Dockerfile added to the project and a **docker-compose** folder added to the solution in **Solution Explorer**, as shown in Figure 4-29:</span></span>

![Visual Studio でソリューション エクスプ ローラーでの docker ファイル](media/docker-support-solution-explorer.png)

<span data-ttu-id="82a91-135">Visual Studio 2017 でのソリューション エクスプ ローラーで、図 4-29: Docker ファイル</span><span class="sxs-lookup"><span data-stu-id="82a91-135">Figure 4-29: Docker files in Solution Explorer in Visual Studio 2017</span></span>

<span data-ttu-id="82a91-136">**詳細については:** サービスの実装と Visual Studio tools for Docker の使用の詳細については、次の記事を参照します。</span><span class="sxs-lookup"><span data-stu-id="82a91-136">**More information:** For further details on the services implementation and use of Visual Studio Tools for Docker, read the following articles:</span></span>

<span data-ttu-id="82a91-137">ビルド、デバッグ、更新、およびローカル Docker コンテナーでアプリを更新します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span><span class="sxs-lookup"><span data-stu-id="82a91-137">Build, debug, update, and refresh apps in a local Docker container: [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span></span>

<span data-ttu-id="82a91-138">コンテナー レジストリには、ASP.NET Core の Docker コンテナーを展開します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span><span class="sxs-lookup"><span data-stu-id="82a91-138">Deploy an ASP.NET Core Docker container to a container registry: [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="82a91-139">[前へ](docker-apps-inner-loop-workflow.md)
[次へ](set-up-windows-containers-with-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="82a91-139">[Previous](docker-apps-inner-loop-workflow.md)
[Next](set-up-windows-containers-with-powershell.md)</span></span>