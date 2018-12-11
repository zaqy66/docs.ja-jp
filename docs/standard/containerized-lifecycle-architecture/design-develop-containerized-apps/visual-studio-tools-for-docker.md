---
title: Visual Studio Tools for Windows 上の Docker
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: 79e9b5cc9bac317a368583013abbc5124ef2c9ac
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53151214"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a><span data-ttu-id="aed11-103">Visual Studio Tools for Docker (Windows で Visual Studio) を使用</span><span class="sxs-lookup"><span data-stu-id="aed11-103">Using Visual Studio Tools for Docker (Visual Studio on Windows)</span></span>

<span data-ttu-id="aed11-104">Visual Studio Code と Docker CLI を使用する場合は、Visual Studio Tools for Docker 開発ワークフローをワークフローに似ています。</span><span class="sxs-lookup"><span data-stu-id="aed11-104">The Visual Studio Tools for Docker development workflow is similar to the workflow when using Visual Studio Code and Docker CLI.</span></span> <span data-ttu-id="aed11-105">実際には、同じの Docker CLI に基づきますが容易に開始、プロセスを簡略化、および生産性の向上を提供します、ビルドの実行、およびタスクを構成します。</span><span class="sxs-lookup"><span data-stu-id="aed11-105">In fact, it's based on the same Docker CLI, but it's easier to get started, simplifies the process, and provides greater productivity for the build, run, and compose tasks.</span></span> <span data-ttu-id="aed11-106">実行し、デバッグのような単純なアクションを使用して、コンテナー **F5**と**Ctrl**+**F5**します。</span><span class="sxs-lookup"><span data-stu-id="aed11-106">Execute and debug your containers via simple actions like **F5** and **Ctrl**+**F5**.</span></span> <span data-ttu-id="aed11-107">実行し、1 つのコンテナーをデバッグできることに加え、省略可能なコンテナー オーケストレーションのサポートは、実行し、コンテナー (ソリューション全体) のグループを同時にデバッグできます。</span><span class="sxs-lookup"><span data-stu-id="aed11-107">With the optional container orchestration support, in addition to being able to run and debug a single container, you can run and debug a group of containers (a whole solution) at the same time.</span></span>

> [!NOTE]
> <span data-ttu-id="aed11-108">この記事は、Windows 上の Visual Studio と Visual Studio for mac。</span><span class="sxs-lookup"><span data-stu-id="aed11-108">This article applies to Visual Studio on Windows, and not Visual Studio for Mac.</span></span>

## <a name="configure-your-local-environment"></a><span data-ttu-id="aed11-109">ローカル環境を構成します。</span><span class="sxs-lookup"><span data-stu-id="aed11-109">Configure your local environment</span></span>

<span data-ttu-id="aed11-110">Docker for Windows の最新バージョン ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/))、簡単なセットアップでは、Docker アプリケーションの開発が容易にします。</span><span class="sxs-lookup"><span data-stu-id="aed11-110">With the latest versions of Docker for Windows ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)), the straightforward setup makes it easy to develop Docker applications.</span></span>

<span data-ttu-id="aed11-111">Visual Studio 2017 では、docker のサポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="aed11-111">Docker support is included in Visual Studio 2017.</span></span> <span data-ttu-id="aed11-112">ここで Visual Studio 2017 をダウンロードします。 [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)</span><span class="sxs-lookup"><span data-stu-id="aed11-112">Download Visual Studio 2017 here: [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)</span></span>

## <a name="use-docker-tools-in-visual-studio-2017"></a><span data-ttu-id="aed11-113">Visual Studio 2017 での Docker ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="aed11-113">Use Docker Tools in Visual Studio 2017</span></span>

<span data-ttu-id="aed11-114">Docker のサポートをプロジェクトに追加することの 2 つのレベルがあります。</span><span class="sxs-lookup"><span data-stu-id="aed11-114">There are two levels of Docker support you can add to a project.</span></span> <span data-ttu-id="aed11-115">.NET Core web アプリのプロジェクトに追加できます、 *Dockerfile*に Docker サポートを有効にすると、プロジェクト ファイル。</span><span class="sxs-lookup"><span data-stu-id="aed11-115">In .NET Core web app projects, you can just add a *Dockerfile* file to the project by enabling Docker support.</span></span> <span data-ttu-id="aed11-116">次のレベルは、追加コンテナー オーケストレーションのサポート、 *Dockerfile* (まだ存在しない) 場合は、プロジェクトに、 *docker compose.yml*ソリューション レベルでのファイル。</span><span class="sxs-lookup"><span data-stu-id="aed11-116">The next level is container orchestration support, which adds a *Dockerfile* to the project (if it doesn't already exist) and a *docker-compose.yml* file at the solution level.</span></span> <span data-ttu-id="aed11-117">既定では Visual Studio 2017 バージョン 15.7 またはそれ以前で、Docker Compose を使用して、コンテナー オーケストレーションのサポートが追加されます。</span><span class="sxs-lookup"><span data-stu-id="aed11-117">Container orchestration support, via Docker Compose, is added by default in Visual Studio 2017 versions 15.7 or earlier.</span></span> <span data-ttu-id="aed11-118">コンテナー オーケストレーションのサポートは、Visual Studio 2017 バージョン 15.8 オプトイン機能または後で、どの場合 Docker Compose と Service Fabric がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="aed11-118">Container orchestration support is an opt-in feature in Visual Studio 2017 versions 15.8 or later, in which case Docker Compose and Service Fabric are supported.</span></span>

<span data-ttu-id="aed11-119">**追加** > **Docker サポート**と**追加** > **コンテナー オーケストレーション サポート**コマンドは、web アプリ プロジェクトのプロジェクト ノードの右クリック メニュー (またはコンテキスト メニュー) にある**ソリューション エクスプ ローラー**図 4-26 に示すようにします。</span><span class="sxs-lookup"><span data-stu-id="aed11-119">The **Add** > **Docker Support** and **Add** > **Container orchestration Support** commands are located on the right-click menu (or context menu) of the project node for a web app project in **Solution Explorer**, as shown in Figure 4-26:</span></span>

![Visual Studio での Docker サポート メニュー オプションを追加します。](media/add-docker-support-menu.png)

<span data-ttu-id="aed11-121">図 4-26:Visual Studio 2017 のプロジェクトに Docker サポートの追加</span><span class="sxs-lookup"><span data-stu-id="aed11-121">Figure 4-26: Adding Docker support to a Visual Studio 2017 project</span></span>

### <a name="add-docker-support"></a><span data-ttu-id="aed11-122">Docker サポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="aed11-122">Add Docker support</span></span>

<span data-ttu-id="aed11-123">選択して、既存の .NET Core web アプリ プロジェクトに Docker サポートを追加する**追加** > **Docker サポート**で**ソリューション エクスプ ローラー**します。</span><span class="sxs-lookup"><span data-stu-id="aed11-123">You can add Docker support to an existing .NET Core web app project by selecting **Add** > **Docker Support** in **Solution Explorer**.</span></span> <span data-ttu-id="aed11-124">選択して、プロジェクトの作成時に Docker サポートを有効することも**Docker サポートを有効にする**で、**新しい ASP.NET Core Web アプリケーション**クリックした後に表示されたダイアログ ボックス**ok**で、**新しいプロジェクト** ダイアログ ボックスで、図 4-27 に示すようにします。</span><span class="sxs-lookup"><span data-stu-id="aed11-124">You can also enable Docker support during project creation by selecting **Enable Docker Support** in the **New ASP.NET Core Web Application** dialog box that opens after you click **OK** in the **New Project** dialog box, as shown in Figure 4-27.</span></span>

![Visual Studio での新しい ASP.NET Core web アプリの Docker サポートを有効にします。](./media/enable-docker-support-visual-studio.png)

<span data-ttu-id="aed11-126">図 4-27:Visual Studio 2017 でプロジェクトの作成時に Docker サポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="aed11-126">Figure 4-27: Enable Docker support during project creation in Visual Studio 2017</span></span>

<span data-ttu-id="aed11-127">Docker サポートを有効にすると、Visual Studio の追加、 *Dockerfile*ファイルをプロジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="aed11-127">When you add or enable Docker support, Visual Studio adds a *Dockerfile* file to the project.</span></span>

> [!NOTE]
> <span data-ttu-id="aed11-128">図 4-28 に示すように .NET Framework web アプリ プロジェクト (いない .NET Core web アプリのプロジェクト) のプロジェクトの作成時に Docker Compose のサポートが有効、コンテナー オーケストレーションのサポートも追加されます。</span><span class="sxs-lookup"><span data-stu-id="aed11-128">When you enable Docker Compose support during project creation for a .NET Framework web app project (not a .NET Core web app project) as shown in Figure 4-28, container orchestration support is also added.</span></span>
>
> ![Docker を有効にする .NET Framework web アプリ プロジェクトのサポートの構成](media/enable-docker-compose-support.png)

> <span data-ttu-id="aed11-130">図 4-28:Visual Studio 2017 で .NET Framework web アプリ プロジェクトでの Docker Compose のサポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="aed11-130">Figure 4-28: Enabling Docker Compose support on a .NET Framework web app project in Visual Studio 2017</span></span>

### <a name="add-container-orchestration-support"></a><span data-ttu-id="aed11-131">コンテナー オーケストレーションのサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="aed11-131">Add container orchestration support</span></span>

<span data-ttu-id="aed11-132">複数のコンテナー ソリューションを作成する場合は、コンテナー オーケストレーションのサポートをプロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="aed11-132">When you want to compose a multicontainer solution, add container orchestration support to your projects.</span></span> <span data-ttu-id="aed11-133">これにより、実行およびで同じ定義している場合、コンテナー (ソリューション全体) のグループを同時にデバッグ*docker compose.yml*ファイル。</span><span class="sxs-lookup"><span data-stu-id="aed11-133">This lets you run and debug a group of containers (a whole solution) at the same time if they're defined in the same *docker-compose.yml* file.</span></span>

<span data-ttu-id="aed11-134">コンテナー オーケストレーションのサポートを追加するには、ソリューションまたはプロジェクトのノードを右クリックし**ソリューション エクスプ ローラー**、選択**追加** > **コンテナー オーケストレーション サポート**.</span><span class="sxs-lookup"><span data-stu-id="aed11-134">To add container orchestration support, right-click on the solution or project node in **Solution Explorer**, and choose **Add** > **Container Orchestration Support**.</span></span> <span data-ttu-id="aed11-135">クリックして**Docker Compose**または**Service Fabric**コンテナーを管理します。</span><span class="sxs-lookup"><span data-stu-id="aed11-135">Then choose **Docker Compose** or **Service Fabric** to manage the containers.</span></span>

<span data-ttu-id="aed11-136">プロジェクトに追加の Dockerfile を参照してくださいコンテナー オーケストレーションのサポートをプロジェクトに追加した後、 **docker compose**でソリューションに追加されたフォルダー**ソリューション エクスプ ローラー**図 4-29 に示すように。</span><span class="sxs-lookup"><span data-stu-id="aed11-136">After you add container orchestration support to your project, you see a Dockerfile added to the project and a **docker-compose** folder added to the solution in **Solution Explorer**, as shown in Figure 4-29:</span></span>

![Visual Studio でソリューション エクスプ ローラーでの docker ファイル](media/docker-support-solution-explorer.png)

<span data-ttu-id="aed11-138">図 4-29:Visual Studio 2017 でのソリューション エクスプ ローラーでの docker ファイル</span><span class="sxs-lookup"><span data-stu-id="aed11-138">Figure 4-29: Docker files in Solution Explorer in Visual Studio 2017</span></span>

<span data-ttu-id="aed11-139">場合*docker compose.yml*が既に存在する Visual Studio に必要な構成コードの行を追加するだけです。</span><span class="sxs-lookup"><span data-stu-id="aed11-139">If *docker-compose.yml* already exists, Visual Studio just adds the required lines of configuration code to it.</span></span>

## <a name="configure-docker-tools"></a><span data-ttu-id="aed11-140">Docker ツールを構成します。</span><span class="sxs-lookup"><span data-stu-id="aed11-140">Configure Docker tools</span></span>

<span data-ttu-id="aed11-141">メイン メニューで、次のように選択します。**ツール** > **オプション**、展開と**コンテナー ツール** > **設定**します。</span><span class="sxs-lookup"><span data-stu-id="aed11-141">From the main menu, choose **Tools** > **Options**, and expand **Container Tools** > **Settings**.</span></span> <span data-ttu-id="aed11-142">コンテナーのツールの設定が表示されます。</span><span class="sxs-lookup"><span data-stu-id="aed11-142">The container tools settings appear.</span></span>

![](./media/visual-studio-docker-tools-options.png)

<span data-ttu-id="aed11-143">図 4-30:Docker Tools のオプション</span><span class="sxs-lookup"><span data-stu-id="aed11-143">Figure 4-30: Docker Tools Options</span></span>

<span data-ttu-id="aed11-144">次の表は、これらのオプションを設定する方法を決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="aed11-144">The following table might help you decide how to set these options.</span></span>

| <span data-ttu-id="aed11-145">名前</span><span class="sxs-lookup"><span data-stu-id="aed11-145">Name</span></span> | <span data-ttu-id="aed11-146">既定の設定</span><span class="sxs-lookup"><span data-stu-id="aed11-146">Default Setting</span></span> | <span data-ttu-id="aed11-147">対象</span><span class="sxs-lookup"><span data-stu-id="aed11-147">Applies To</span></span> | <span data-ttu-id="aed11-148">説明</span><span class="sxs-lookup"><span data-stu-id="aed11-148">Description</span></span> |
| -----|:---------------:|:----------:| ----------- |
| <span data-ttu-id="aed11-149">プロジェクトの読み込みで必要な Docker イメージを自動的にプルします。</span><span class="sxs-lookup"><span data-stu-id="aed11-149">Automatically pull required Docker images on project load</span></span> | <span data-ttu-id="aed11-150">オン</span><span class="sxs-lookup"><span data-stu-id="aed11-150">On</span></span> | <span data-ttu-id="aed11-151">Docker Compose</span><span class="sxs-lookup"><span data-stu-id="aed11-151">Docker Compose</span></span> | <span data-ttu-id="aed11-152">パフォーマンス向上のためのプロジェクトを読み込むときに、Visual Studio は、イメージが既にダウンロードしてコードを実行する準備ができたら、ダウンロード処理中にまたは、バック グラウンドで Docker プルの操作が開始されます。</span><span class="sxs-lookup"><span data-stu-id="aed11-152">For increased performance, when loading projects, Visual Studio will start a Docker pull operation in the background so that when you are ready to run your code, the image is already downloaded or in the process of downloading.</span></span> <span data-ttu-id="aed11-153">プロジェクトをロードする場合だけ、コードを参照するには、これをオフにできます必要はありません、コンテナー イメージをダウンロードしないようにする場合。</span><span class="sxs-lookup"><span data-stu-id="aed11-153">If you're just loading projects and browsing code, you can turn this off to avoid downloading container images you don't need.</span></span> |
| <span data-ttu-id="aed11-154">コンテナーをバック グラウンドで自動的に開始します。</span><span class="sxs-lookup"><span data-stu-id="aed11-154">Automatically start containers in background</span></span> | <span data-ttu-id="aed11-155">オン</span><span class="sxs-lookup"><span data-stu-id="aed11-155">On</span></span> | <span data-ttu-id="aed11-156">Docker Compose</span><span class="sxs-lookup"><span data-stu-id="aed11-156">Docker Compose</span></span> | <span data-ttu-id="aed11-157">もう一度パフォーマンスを向上させる Visual Studio によりコンテナーとボリューム マウント ビルドおよびコンテナーを実行する場合に対応。</span><span class="sxs-lookup"><span data-stu-id="aed11-157">Again for increased performance, Visual Studio creates a container with volume mounts ready for when you build and run your container.</span></span> <span data-ttu-id="aed11-158">コンテナーが作成されたときを制御するには、これをオフにします。</span><span class="sxs-lookup"><span data-stu-id="aed11-158">If you want to control when your container is created, turn this off.</span></span> |
| <span data-ttu-id="aed11-159">自動的に強制終了のコンテナー ソリューションを閉じる</span><span class="sxs-lookup"><span data-stu-id="aed11-159">Automatically kill containers on solution close</span></span> | <span data-ttu-id="aed11-160">オン</span><span class="sxs-lookup"><span data-stu-id="aed11-160">On</span></span> | <span data-ttu-id="aed11-161">Docker Compose</span><span class="sxs-lookup"><span data-stu-id="aed11-161">Docker Compose</span></span> | <span data-ttu-id="aed11-162">コンテナー ソリューションを閉じるか、Visual Studio の終了後も引き続き実行に、ソリューションが希望される場合は、これをオフにします。</span><span class="sxs-lookup"><span data-stu-id="aed11-162">Turn this off if you would like containers for your solution to continue to run after closing the solution or closing Visual Studio.</span></span> |
| <span data-ttu-id="aed11-163">Localhost SSL 証明書を信頼する側は表示しません</span><span class="sxs-lookup"><span data-stu-id="aed11-163">Do not prompt for trusting localhost SSL certificate</span></span> | <span data-ttu-id="aed11-164">オフ</span><span class="sxs-lookup"><span data-stu-id="aed11-164">Off</span></span> | <span data-ttu-id="aed11-165">ASP.NET Core 2.1 プロジェクト</span><span class="sxs-lookup"><span data-stu-id="aed11-165">ASP.NET Core 2.1 projects</span></span> | <span data-ttu-id="aed11-166">Localhost SSL 証明書が信頼されていない場合は、Visual Studio は必要ない限り、このチェック ボックスをオンになって、プロジェクトを実行するたびと求められます。</span><span class="sxs-lookup"><span data-stu-id="aed11-166">If the localhost SSL certificate is not trusted, Visual Studio will prompt every time you run your project, unless this checkbox is checked.</span></span> |

> [!WARNING]
> <span data-ttu-id="aed11-167">Localhost SSL 証明書は信頼されず、プロンプトを抑制するボックスをチェックする場合は、アプリまたはサービスの実行時に HTTPS web 要求が失敗します。</span><span class="sxs-lookup"><span data-stu-id="aed11-167">If the localhost SSL certificate is not trusted, and you check the box to suppress prompting, then HTTPS web requests might fail at runtime in your app or service.</span></span> <span data-ttu-id="aed11-168">その場合は、オフにして、**を求めない** チェック ボックスは、プロジェクトを実行し、プロンプトでの信頼関係を示します。</span><span class="sxs-lookup"><span data-stu-id="aed11-168">In that case, uncheck the **Do not prompt** checkbox, run your project, and indicate trust at the prompt.</span></span>

<span data-ttu-id="aed11-169">**詳細については:** サービスの実装と Visual Studio tools for Docker の使用の詳細については、次の記事を参照します。</span><span class="sxs-lookup"><span data-stu-id="aed11-169">**More information:** For further details on the services implementation and use of Visual Studio Tools for Docker, read the following articles:</span></span>

<span data-ttu-id="aed11-170">ビルド、デバッグ、更新、およびローカル Docker コンテナーでアプリを更新します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span><span class="sxs-lookup"><span data-stu-id="aed11-170">Build, debug, update, and refresh apps in a local Docker container: [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span></span>

<span data-ttu-id="aed11-171">コンテナー レジストリには、ASP.NET Core の Docker コンテナーを展開します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span><span class="sxs-lookup"><span data-stu-id="aed11-171">Deploy an ASP.NET Core Docker container to a container registry: [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="aed11-172">[前へ](docker-apps-inner-loop-workflow.md)
>[次へ](set-up-windows-containers-with-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="aed11-172">[Previous](docker-apps-inner-loop-workflow.md)
[Next](set-up-windows-containers-with-powershell.md)</span></span>