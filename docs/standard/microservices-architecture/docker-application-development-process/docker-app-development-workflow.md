---
title: Docker アプリの開発ワークフロー
description: '.NET マイクロサービス: コンテナー化された .NET アプリケーションのアーキテクチャ | Docker アプリの開発ワークフロー'
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/05/2018
ms.openlocfilehash: 00cffde7e7eb548f755b60f64aa596210b570d07
ms.sourcegitcommit: 35316b768394e56087483cde93f854ba607b63bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2018
ms.locfileid: "52297518"
---
# <a name="development-workflow-for-docker-apps"></a><span data-ttu-id="f12d0-103">Docker アプリの開発ワークフロー</span><span class="sxs-lookup"><span data-stu-id="f12d0-103">Development workflow for Docker apps</span></span>

<span data-ttu-id="f12d0-104">アプリケーション開発のライフ サイクルは、各開発者のコンピューターから始まります。このとき、アプリケーションは、開発者の好みの言語で記述され、ローカルでテストされます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-104">The application development life cycle starts at each developer’s machine, where the developer codes the application using their preferred language and tests it locally.</span></span> <span data-ttu-id="f12d0-105">このワークフローでは、開発者が選択している言語、フレームワークおよびプラットフォームにかかわらず、常に Docker コンテナーはローカルで開発およびテストされます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-105">No matter which language, framework, and platform the developer chooses, with this workflow, the developer is always developing and testing Docker containers, but doing so locally.</span></span>

<span data-ttu-id="f12d0-106">各コンテナー (Docker イメージのインスタンス) には、次のコンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-106">Each container (an instance of a Docker image) includes the following components:</span></span>

- <span data-ttu-id="f12d0-107">選択したオペレーティング システム (例: Linux ディストリビューション、Windows Nano Server、または Windows Server Core)。</span><span class="sxs-lookup"><span data-stu-id="f12d0-107">An operating system selection (for example, a Linux distribution, Windows Nano Server, or Windows Server Core).</span></span>

- <span data-ttu-id="f12d0-108">開発者が追加したファイル (アプリケーションのバイナリなど)。</span><span class="sxs-lookup"><span data-stu-id="f12d0-108">Files added by the developer (application binaries, etc.).</span></span>

- <span data-ttu-id="f12d0-109">構成情報 (環境の設定および依存関係)。</span><span class="sxs-lookup"><span data-stu-id="f12d0-109">Configuration information (environment settings and dependencies).</span></span>

## <a name="workflow-for-developing-docker-container-based-applications"></a><span data-ttu-id="f12d0-110">Docker のコンテナー ベースのアプリケーションを開発するためのワークフロー</span><span class="sxs-lookup"><span data-stu-id="f12d0-110">Workflow for developing Docker container-based applications</span></span>

<span data-ttu-id="f12d0-111">このセクションでは、Docker のコンテナー ベースのアプリケーションの*内側のループ*の開発ワークフローについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-111">This section describes the *inner-loop* development workflow for Docker container-based applications.</span></span> <span data-ttu-id="f12d0-112">内側のループのワークフローとは、DevOps のより全体的なワークフローではなく、開発者のコンピューター上で実行される開発作業のみを意味しています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-112">The inner-loop workflow means it is not taking into account the broader DevOps workflow and just focuses on the development work done on the developer’s computer.</span></span> <span data-ttu-id="f12d0-113">環境を設定する初期手順は、一度のみ実行されるものなので含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f12d0-113">The initial steps to set up the environment are not included, since those are done only once.</span></span>

<span data-ttu-id="f12d0-114">アプリケーションは、自分のサービスと追加のライブラリ (依存関係) で構成されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-114">An application is composed of your own services plus additional libraries (dependencies).</span></span> <span data-ttu-id="f12d0-115">Docker アプリケーションを構築するときの基本手順を次の図 5-1 に示します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-115">The following are the basic steps you usually take when building a Docker application, as illustrated in Figure 5-1.</span></span>

![Docker のコンテナー化されたアプリケーションを開発するための詳細なワークフローの図](./media/image1.png)

<span data-ttu-id="f12d0-117">**図 5-1**</span><span class="sxs-lookup"><span data-stu-id="f12d0-117">**Figure 5-1.**</span></span> <span data-ttu-id="f12d0-118">Docker のコンテナー化されたアプリケーションを開発するための詳細なワークフロー</span><span class="sxs-lookup"><span data-stu-id="f12d0-118">Step-by-step workflow for developing Docker containerized apps</span></span>

<span data-ttu-id="f12d0-119">このガイドでは、すべての手順が詳細に記載されており、主要な各手順は、Visual Studio の環境を使用して説明しています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-119">In this guide, this whole process is detailed and every major step is explained by focusing on a Visual Studio environment.</span></span>

<span data-ttu-id="f12d0-120">エディターと CLI を使用する開発手法 (例: Visual Studio Code と macOS または Windows 上の Docker CLI) を使用する場合、Visual Studio を使用する場合よりも、通常はより詳細に全手順を把握している必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-120">When you are using an editor/CLI development approach (for example, Visual Studio Code plus Docker CLI on macOS or Windows), you need to know every step, generally in more detail than if you are using Visual Studio.</span></span> <span data-ttu-id="f12d0-121">CLI 環境での作業の詳細については、電子書籍「[Containerized Docker Application lifecycle with Microsoft Platforms and Tools](https://aka.ms/dockerlifecycleebook/)」 (Microsoft のプラットフォームおよびツールとコンテナー化された Docker アプリケーションのライフサイクル) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f12d0-121">For more information about working in a CLI environment, see the e-book [Containerized Docker Application lifecycle with Microsoft Platforms and Tools](https://aka.ms/dockerlifecycleebook/).</span></span>

<span data-ttu-id="f12d0-122">Visual Studio を使用している場合、これらの手順の多くは自動処理されるので、生産性が大幅に向上します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-122">When you're using Visual Studio, many of those steps are handled for you, which dramatically improves your productivity.</span></span> <span data-ttu-id="f12d0-123">これは、Visual Studio 2017 で、複数のコンテナー アプリケーションを対象としているとき特にそうです。</span><span class="sxs-lookup"><span data-stu-id="f12d0-123">This is especially true when you are using Visual Studio 2017 and targeting multi-container applications.</span></span> <span data-ttu-id="f12d0-124">たとえば、マウスを 1 回クリックするだけで、Visual Studio では、アプリケーションに適した構成で *Dockerfile* と *docker-compose.yml* ファイルをプロジェクトに追加できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-124">For instance, with just one mouse click, Visual Studio adds the *Dockerfile* and *docker-compose.yml* files to your projects with the configuration for your application.</span></span> <span data-ttu-id="f12d0-125">そのアプリケーションを Visual Studio で実行すると、Docker イメージが構築され、Docker で直接マルチコンテナー アプリケーションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-125">When you run the application in Visual Studio, it builds the Docker image and runs the multi-container application directly in Docker.</span></span> <span data-ttu-id="f12d0-126">一度に複数のコンテナーをデバッグすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-126">It even allows you to debug several containers at once.</span></span> <span data-ttu-id="f12d0-127">これらの機能により、開発の速度が向上します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-127">These features boost your development speed.</span></span>

<span data-ttu-id="f12d0-128">以下のガイダンスでは、Docker を使用する場合の内部的な処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-128">In the guidance that follows, we explain what's happening "under the covers" with Docker.</span></span>

![手順 1 - アプリのコーディングの図](./media/image2.png)

## <a name="step-1-start-coding-and-create-your-initial-application-or-service-baseline"></a><span data-ttu-id="f12d0-130">手順 1.</span><span class="sxs-lookup"><span data-stu-id="f12d0-130">Step 1.</span></span> <span data-ttu-id="f12d0-131">コーディングを開始して、初期アプリケーションまたはサービス ベースラインを作成します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-131">Start coding and create your initial application or service baseline</span></span>

<span data-ttu-id="f12d0-132">Docker アプリケーションの開発方法は、Docker を使用しないアプリケーションの開発方法と似ています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-132">Developing a Docker application is similar to the way you develop an application without Docker.</span></span> <span data-ttu-id="f12d0-133">違いは、Docker 用を開発している場合、ローカル環境で Docker コンテナー内で実行するアプリケーションまたはサービスを開発またはテストするということです。</span><span class="sxs-lookup"><span data-stu-id="f12d0-133">The difference is that while developing for Docker, you are deploying and testing your application or services running within Docker containers in your local environment.</span></span> <span data-ttu-id="f12d0-134">コンテナーには、Linux コンテナーまたは Windows コンテナーのいずれも使用できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-134">The container can be either a Linux container or a Windows container.</span></span>

### <a name="set-up-your-local-environment-with-visual-studio"></a><span data-ttu-id="f12d0-135">Visual Studio でのローカル環境のセットアップ</span><span class="sxs-lookup"><span data-stu-id="f12d0-135">Set up your local environment with Visual Studio</span></span>

<span data-ttu-id="f12d0-136">最初に、次の手順で説明する、Windows 用の [Docker Community Edition (CE)](https://www.docker.com/community-edition) がインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-136">To begin, make sure you have [Docker Community Edition (CE)](https://www.docker.com/community-edition) for Windows installed, as explained in the following instructions:</span></span>

<span data-ttu-id="f12d0-137">[Get started with Docker CE for Windows](https://docs.docker.com/docker-for-windows/) (Windows 用の Docker CE の概要)</span><span class="sxs-lookup"><span data-stu-id="f12d0-137">[Get started with Docker CE for Windows](https://docs.docker.com/docker-for-windows/)</span></span>

<span data-ttu-id="f12d0-138">さらに、図 5-2 に示すように、**.NET Core クロスプラットフォーム開発**ワークロードがインストールされた Visual Studio 2017 が必要です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-138">In addition, you need Visual Studio 2017 with the **.NET Core cross-platform development** workload installed, as shown in Figure 5-2.</span></span>

![](./media/image3.png)

<span data-ttu-id="f12d0-139">**図 5-2**</span><span class="sxs-lookup"><span data-stu-id="f12d0-139">**Figure 5-2**.</span></span> <span data-ttu-id="f12d0-140">Visual Studio 2017 のセットアップ時の **.NET Core と Docker** ワークロードの選択</span><span class="sxs-lookup"><span data-stu-id="f12d0-140">Selecting the **.NET Core and Docker** workload during Visual Studio 2017 setup</span></span>

<span data-ttu-id="f12d0-141">アプリケーションのコーディングは、アプリケーションで Docker を有効にし、Docker を展開してテストする前から、単純な .NET で開始することができます (コンテナーを使用する計画がある場合、通常は .NET Core)。</span><span class="sxs-lookup"><span data-stu-id="f12d0-141">You can start coding your application in plain .NET (usually in .NET Core if you are planning to use containers) even before enabling Docker in your application and deploying and testing in Docker.</span></span> <span data-ttu-id="f12d0-142">ただし、実際の環境となることに加え、問題が早く検出されるため、できるだけ早く Docker で作業を開始することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f12d0-142">However, it is recommended that you start working on Docker as soon as possible, because that will be the real environment and any issues can be discovered as soon as possible.</span></span> <span data-ttu-id="f12d0-143">Docker は、Visual Studio では、ほとんど透過的で、使用しやすくなっているため、このようにすることが推奨されます。この最良の例は、Visual Studio からのマルチコンテナー アプリケーションのデバッグです。</span><span class="sxs-lookup"><span data-stu-id="f12d0-143">This is encouraged because Visual Studio makes it so easy to work with Docker that it almost feels transparent — the best example when debugging multi-container applications from Visual Studio.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="f12d0-144">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="f12d0-144">Additional resources</span></span>

- <span data-ttu-id="f12d0-145">**Get started with Docker CE for Windows** (Windows 用の Docker CE の概要)</span><span class="sxs-lookup"><span data-stu-id="f12d0-145">**Get started with Docker CE for Windows**</span></span>

   [*https://docs.docker.com/docker-for-windows/*](https://docs.docker.com/docker-for-windows/)

- <span data-ttu-id="f12d0-146">**Visual Studio 2017**</span><span class="sxs-lookup"><span data-stu-id="f12d0-146">**Visual Studio 2017**</span></span>

   [*https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs*](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)

![手順 2 - Dockerfile の記述の図](./media/image4.png)

## <a name="step-2-create-a-dockerfile-related-to-an-existing-net-base-image"></a><span data-ttu-id="f12d0-148">手順 2.</span><span class="sxs-lookup"><span data-stu-id="f12d0-148">Step 2.</span></span> <span data-ttu-id="f12d0-149">既存の .NET 基本イメージに関連する Dockerfile を作成します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-149">Create a Dockerfile related to an existing .NET base image</span></span>

<span data-ttu-id="f12d0-150">Dockerfile は、構築するカスタム イメージごとに必要です。また、Visual Studio から自動的に展開する場合も、Docker CLI (docker run および docker-compose コマンド) を使用して手動で展開する場合も、展開するコンテナーごとに Dockerfile が必要です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-150">You need a Dockerfile for each custom image you want to build; you also need a Dockerfile for each container to be deployed, whether you deploy automatically from Visual Studio or manually using the Docker CLI (docker run and docker-compose commands).</span></span> <span data-ttu-id="f12d0-151">アプリケーションにカスタム サービスが 1 つ含まれている場合、Dockerfile が 1 つ必要です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-151">If your application contains a single custom service, you need a single Dockerfile.</span></span> <span data-ttu-id="f12d0-152">(マイクロサービス アーキテクチャの場合のように) アプリケーションに複数のサービスが含まれる場合、サービスごとに Dockerfile が 1 つ必要です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-152">If your application contains multiple services (as in a microservices architecture), you need one Dockerfile for each service.</span></span>

<span data-ttu-id="f12d0-153">Dockerfile は、アプリケーションまたはサービスのルート フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-153">The Dockerfile is placed in the root folder of your application or service.</span></span> <span data-ttu-id="f12d0-154">これには、コンテナーでアプリケーションまたはサービスを設定して実行する方法を Docker に指示するコマンドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-154">It contains the commands that tell Docker how to set up and run your application or service in a container.</span></span> <span data-ttu-id="f12d0-155">手動でコードに Dockerfile を作成し、.NET の依存関係と共にプロジェクトに追加できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-155">You can manually create a Dockerfile in code and add it to your project along with your .NET dependencies.</span></span>

<span data-ttu-id="f12d0-156">Visual Studio Tools for Docker では、わずか数回のクリックでこのタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-156">With Visual Studio Tools for Docker, this task requires only a few mouse clicks.</span></span> <span data-ttu-id="f12d0-157">Visual Studio 2017 で新しいプロジェクトを作成する場合、図 5-3 に示すように **[Docker サポートを有効にする]** というオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-157">When you create a new project in Visual Studio 2017, there's an option named **Enable Docker Support**, as shown in Figure 5-3.</span></span>

![Visual Studio 2017 で新しいプロジェクトを作成するときの Docker サポートの有効化](./media/image5.png)

<span data-ttu-id="f12d0-159">**図 5-3**</span><span class="sxs-lookup"><span data-stu-id="f12d0-159">**Figure 5-3**.</span></span> <span data-ttu-id="f12d0-160">Visual Studio 2017 で新しいプロジェクトを作成するときの Docker サポートの有効化</span><span class="sxs-lookup"><span data-stu-id="f12d0-160">Enabling Docker Support when creating a new project in Visual Studio 2017</span></span>

<span data-ttu-id="f12d0-161">また、図 5-4 に示すように、**ソリューション エクスプローラー**でプロジェクトを右クリックし、**[追加]** > **[Docker サポート]** を選択することで、既存の .NET Core Web アプリ プロジェクトに対して Docker サポートを有効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-161">You can also enable Docker support on an existing .NET Core web app project by right-clicking the project in **Solution Explorer** and selecting **Add** > **Docker Support**, as shown in Figure 5-4.</span></span>

![Visual Studio の Docker サポートの追加メニュー オプション](./media/add-docker-support.png)

<span data-ttu-id="f12d0-163">**図 5-4**</span><span class="sxs-lookup"><span data-stu-id="f12d0-163">**Figure 5-4**.</span></span> <span data-ttu-id="f12d0-164">既存の Visual Studio 2017 プロジェクトでの Docker サポートの有効化</span><span class="sxs-lookup"><span data-stu-id="f12d0-164">Enabling Docker support in an existing Visual Studio 2017 project</span></span>

<span data-ttu-id="f12d0-165">この操作で、必要な構成のプロジェクトに *Dockerfile* が追加され、.NET Core Web アプリ プロジェクトでのみ使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-165">This action adds a *Dockerfile* to the project with the required configuration, and is only available on .NET Core web app projects.</span></span>

<span data-ttu-id="f12d0-166">ソリューション全体に *docker-compose.yml* ファイルを追加するには、図 5-5 に示すように、**ソリューション エクスプローラー**でプロジェクトを右クリックし、**[追加]** > **[Container Orchestrator Support]\(コンテナー オーケストレーターのサポート\)** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f12d0-166">To add a *docker-compose.yml* file for the whole solution, right-click on the project in **Solution Explorer** and select **Add** > **Container Orchestrator Support**, as shown in Figure 5-5.</span></span>

![Visual Studio のコンテナー オーケストレーターのサポートの追加メニュー オプション](./media/add-container-orchestrator-support.png)

<span data-ttu-id="f12d0-168">**図 5-5**</span><span class="sxs-lookup"><span data-stu-id="f12d0-168">**Figure 5-5**.</span></span> <span data-ttu-id="f12d0-169">Visual Studio 2017 で既存のプロジェクトにコンテナー オーケストレーター サポートを追加する。</span><span class="sxs-lookup"><span data-stu-id="f12d0-169">Adding container orchestrator support to an existing project in Visual Studio 2017.</span></span>

<span data-ttu-id="f12d0-170">次のセクションでは、それらの各ファイルに書き込まれる情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-170">In the following sections, we describe the information that goes into each of those files.</span></span> <span data-ttu-id="f12d0-171">この作業は、Visual Studio が実行してくれますが、Dockerfile に何が書き込まれるかを理解しておくと便利です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-171">Visual Studio can do this work for you, but it is useful to understand what goes into a Dockerfile.</span></span>

### <a name="option-a-creating-a-project-using-an-existing-official-net-docker-image"></a><span data-ttu-id="f12d0-172">オプション A: 既存の公式の .NET Docker イメージを使用してプロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="f12d0-172">Option A: Creating a project using an existing official .NET Docker image</span></span>

<span data-ttu-id="f12d0-173">通常、公式のリポジトリである [Docker Hub](https://hub.docker.com/) レジストリから取得できる基本イメージ上にコンテナーのカスタム イメージをビルドします。</span><span class="sxs-lookup"><span data-stu-id="f12d0-173">You usually build a custom image for your container on top of a base image you can get from an official repository at the [Docker Hub](https://hub.docker.com/) registry.</span></span> <span data-ttu-id="f12d0-174">Visual Studio で Docker のサポートを有効にした場合、背後ではこれがまさに発生します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-174">That is precisely what happens under the covers when you enable Docker support in Visual Studio.</span></span> <span data-ttu-id="f12d0-175">Dockerfile では、既存の aspnetcore イメージを使用します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-175">The Dockerfile uses an existing aspnetcore image.</span></span>

<span data-ttu-id="f12d0-176">選択した OS とフレームワークによって、使用できる Docker イメージとリポジトリについては、既に説明しています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-176">Earlier we explained which Docker images and repos you can use, depending on the framework and OS you have chosen.</span></span> <span data-ttu-id="f12d0-177">たとえば、ASP.NET Core (Linux または Windows) を使用したい場合は、microsoft/aspnetcore:2.0 のイメージを使用します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-177">For instance, if you want to use ASP.NET Core (Linux or Windows), the image to use is microsoft/aspnetcore:2.0.</span></span> <span data-ttu-id="f12d0-178">この場合は、コンテナーに使用する基本の Docker イメージのみを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-178">Therefore, you just need to specify what base Docker image you will use for your container.</span></span> <span data-ttu-id="f12d0-179">これは、Dockerfile に FROM microsoft/aspnetcore:2.0 を追加することによって行います。</span><span class="sxs-lookup"><span data-stu-id="f12d0-179">You do that by adding FROM microsoft/aspnetcore:2.0 to your Dockerfile.</span></span> <span data-ttu-id="f12d0-180">これは Visual Studio によって自動的に実行されますが、バージョンを更新する場合は、この値を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-180">This is automatically performed by Visual Studio, but if you were to update the version, you update this value.</span></span>

<span data-ttu-id="f12d0-181">バージョン番号を使用して Docker Hub の公式の .NET イメージ リポジトリを使うと、同じ言語機能が (開発、テスト、および実稼働環境などの) すべてのコンピューターで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-181">Using an official .NET image repository from Docker Hub with a version number ensures that the same language features are available on all machines (including development, testing, and production).</span></span>

<span data-ttu-id="f12d0-182">次の例では、ASP.NET Core コンテナー用のサンプルの Dockerfile を示しています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-182">The following example shows a sample Dockerfile for an ASP.NET Core container.</span></span>

```Dockerfile
FROM microsoft/aspnetcore:2.0

ARG source

WORKDIR /app

EXPOSE 80

COPY ${source:-obj/Docker/publish} .

ENTRYPOINT ["dotnet", " MySingleContainerWebApp.dll "]
```

<span data-ttu-id="f12d0-183">この場合、コンテナーは、公式の ASP.NET Core Docker イメージ (Linux および Windows 用マルチアーチ) のバージョン 2.0 に基づいています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-183">In this case, the container is based on version 2.0 of the official ASP.NET Core Docker image (multi-arch for Linux and Windows).</span></span> <span data-ttu-id="f12d0-184">この設定は、`FROM microsoft/aspnetcore:2.0` です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-184">This is the setting `FROM microsoft/aspnetcore:2.0`.</span></span> <span data-ttu-id="f12d0-185">(この基本イメージの詳細については、「[ASP.NET Core Docker Image](https://hub.docker.com/r/microsoft/aspnetcore/)」 (ASP.NET Core Docker イメージ) ページと「[.NET Core Docker Image](https://hub.docker.com/r/microsoft/dotnet/)」 (.NET Core Docker イメージ) ページを参照してください)。Dockerfile では、実行時に使用する、リッスンする TCP ポートを、Docker に指示する必要があります (ここでは、EXPOSE 設定で構成したポート 80)。</span><span class="sxs-lookup"><span data-stu-id="f12d0-185">(For more information about this base image, see the [ASP.NET Core Docker Image](https://hub.docker.com/r/microsoft/aspnetcore/) page and the [.NET Core Docker Image](https://hub.docker.com/r/microsoft/dotnet/) page.) In the Dockerfile, you also need to instruct Docker to listen on the TCP port you will use at runtime (in this case, port 80, as configured with the EXPOSE setting).</span></span>

<span data-ttu-id="f12d0-186">使用している言語とフレームワークによっては、Dockerfile に別の構成設定を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-186">You can specify additional configuration settings in the Dockerfile, depending on the language and framework you are using.</span></span> <span data-ttu-id="f12d0-187">たとえば、\["dotnet", "MySingleContainerWebApp.dll"\] の ENTRYPOINT 行では、.NET Core アプリケーションを実行するよう Docker に指示しています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-187">For instance, the ENTRYPOINT line with \["dotnet", "MySingleContainerWebApp.dll"\] tells Docker to run a .NET Core application.</span></span> <span data-ttu-id="f12d0-188">SDK と .NET Core CLI (dotnet CLI) を使用して、.NET アプリケーションをビルドおよび実行している場合、設定はこれとは別になります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-188">If you are using the SDK and the .NET Core CLI (dotnet CLI) to build and run the .NET application, this setting would be different.</span></span> <span data-ttu-id="f12d0-189">つまり、アプリケーションに選択した言語とプラットフォームにより、ENTRYPOINT 行とその他の設定は別になります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-189">The bottom line is that the ENTRYPOINT line and other settings will be different depending on the language and platform you choose for your application.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="f12d0-190">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="f12d0-190">Additional resources</span></span>

- <span data-ttu-id="f12d0-191">**.NET Core アプリケーションの Docker イメージのビルド**</span><span class="sxs-lookup"><span data-stu-id="f12d0-191">**Building Docker Images for .NET Core Applications**</span></span>

   [*https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images*](../../../core/docker/building-net-docker-images.md)

- <span data-ttu-id="f12d0-192">**Build your own image (独自のイメージのビルド)**。</span><span class="sxs-lookup"><span data-stu-id="f12d0-192">**Build your own image**.</span></span> <span data-ttu-id="f12d0-193">Docker の公式なドキュメント内にあります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-193">In the official Docker documentation.</span></span>

   [*https://docs.docker.com/engine/tutorials/dockerimages/*](https://docs.docker.com/engine/tutorials/dockerimages/)

### <a name="using-multi-arch-image-repositories"></a><span data-ttu-id="f12d0-194">マルチアーキテクチャ イメージ リポジトリの使用</span><span class="sxs-lookup"><span data-stu-id="f12d0-194">Using multi-arch image repositories</span></span>

<span data-ttu-id="f12d0-195">単一のリポジトリには、Linux イメージや Windows イメージなどのプラットフォーム バリアントを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-195">A single repo can contain platform variants, such as a Linux image and a Windows image.</span></span> <span data-ttu-id="f12d0-196">この機能では、Microsoft (基本イメージの作成者) などのベンダーが、複数のプラットフォーム (つまり、Linux および Windows) に対応できるリポジトリを 1 つ作成できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-196">This feature allows vendors like Microsoft (base image creators) to create a single repo to cover multiple platforms (that is Linux and Windows).</span></span> <span data-ttu-id="f12d0-197">たとえば、Docker Hub レジストリにある [microsoft/dotnet](https://hub.docker.com/r/microsoft/aspnetcore/) リポジトリでは、同じリポジトリ名を使用して Linux および Windows Nano Server をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-197">For example, the [microsoft/dotnet](https://hub.docker.com/r/microsoft/aspnetcore/) repository available in the Docker Hub registry provides support for Linux and Windows Nano Server by using the same repo name.</span></span>

<span data-ttu-id="f12d0-198">タグを指定する場合、次の場合のように、明示的にプラットフォームを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-198">If you specify a tag, targeting a platform that is explicit like in the following cases:</span></span>

- <span data-ttu-id="f12d0-199">**microsoft/aspnetcore:2.0.0-jessie**</span><span class="sxs-lookup"><span data-stu-id="f12d0-199">**microsoft/aspnetcore:2.0.0-jessie**</span></span>

        .NET Core 2.0 runtime-only on Linux

- <span data-ttu-id="f12d0-200">**microsoft/aspnetcore:2.0.0-nanoserver**</span><span class="sxs-lookup"><span data-stu-id="f12d0-200">**microsoft/aspnetcore:2.0.0-nanoserver**</span></span>

        .NET Core 2.0 runtime-only on Windows Nano Server

<span data-ttu-id="f12d0-201">しかし、これは 2017 年の中ごろからのものであり、同じイメージ名を指定した場合、同じタグを使用した場合でも、次の例で示すように、(マルチアーキテクチャをサポートする aspnetcore イメージなどの) 新しいマルチアーキテクチャ イメージは、展開する Docker ホストの OS に応じて Linux または Windows バージョンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-201">But, and this is new since mid-2017, if you specify the same image name, even with the same tag, the new multi-arch images (like the aspnetcore image, which supports multi-arch) will use the Linux or Windows version depending on the Docker host OS you are deploying, as shown in the following example:</span></span>

- <span data-ttu-id="f12d0-202">**microsoft/aspnetcore:2.0**</span><span class="sxs-lookup"><span data-stu-id="f12d0-202">**microsoft/aspnetcore:2.0**</span></span>

        Multi-arch: .NET Core 2.0 runtime-only on Linux or Windows Nano Server depending on the Docker host OS

<span data-ttu-id="f12d0-203">この場合、Windows ホストからイメージをプルした場合、Windows バリアントがプルされ、同じイメージ名が Linux ホストからプルされた場合、Linux バリアントがプルされます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-203">This way, when you pull an image from a Windows host, it will pull the Windows variant, and pulling the same image name from a Linux host will pull the Linux variant.</span></span>

### <a name="option-b-creating-your-base-image-from-scratch"></a><span data-ttu-id="f12d0-204">オプション B: 一から基本イメージを作成する</span><span class="sxs-lookup"><span data-stu-id="f12d0-204">Option B: Creating your base image from scratch</span></span>

<span data-ttu-id="f12d0-205">独自の Docker 基本イメージを一から作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-205">You can create your own Docker base image from scratch.</span></span> <span data-ttu-id="f12d0-206">このシナリオは、Docker を初めて使用するユーザーには推奨されませんが、独自の基本イメージの特定のビットを設定したい場合にそれを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-206">This scenario is not recommended for someone who is starting with Docker, but if you want to set the specific bits of your own base image, you can do so.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="f12d0-207">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="f12d0-207">Additional resources</span></span>

- <span data-ttu-id="f12d0-208">**Multi-arch .NET Core images** (マルチアーキテクチャの .NET Core のイメージ)</span><span class="sxs-lookup"><span data-stu-id="f12d0-208">**Multi-arch .NET Core images**.</span></span>

   https://github.com/dotnet/announcements/issues/14

- <span data-ttu-id="f12d0-209">**Create a base image** (基本イメージを作成する)</span><span class="sxs-lookup"><span data-stu-id="f12d0-209">**Create a base image**.</span></span> <span data-ttu-id="f12d0-210">Docker の公式なドキュメントです。</span><span class="sxs-lookup"><span data-stu-id="f12d0-210">Official Docker documentation.</span></span>

   [*https://docs.docker.com/engine/userguide/eng-image/baseimages/*](https://docs.docker.com/engine/userguide/eng-image/baseimages/)

![手順 3 - イメージの作成の図](./media/image7.png)

## <a name="step-3-create-your-custom-docker-images-and-embed-your-application-or-service-in-them"></a><span data-ttu-id="f12d0-212">手順 3.</span><span class="sxs-lookup"><span data-stu-id="f12d0-212">Step 3.</span></span> <span data-ttu-id="f12d0-213">カスタマイズした Docker イメージを作成し、それにアプリケーションまたはサービスを埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-213">Create your custom Docker images and embed your application or service in them</span></span>

<span data-ttu-id="f12d0-214">アプリケーションの各サービスには、関連イメージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-214">For each service in your application, you need to create a related image.</span></span> <span data-ttu-id="f12d0-215">アプリケーションが 1 つのサービスまたは Web アプリケーションで構成されている場合、イメージは 1 つのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-215">If your application is made up of a single service or web application, you just need a single image.</span></span>

<span data-ttu-id="f12d0-216">Docker イメージは、Visual Studio で自動的に構築されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-216">The Docker images are built automatically for you in Visual Studio.</span></span> <span data-ttu-id="f12d0-217">次の手順は、エディター/CLI ワークフローにのみ必要であり、背後で何が起こっているのか説明するために示しています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-217">The following steps are only needed for the editor/CLI workflow and explained for clarity about what happens underneath.</span></span>

<span data-ttu-id="f12d0-218">開発者は、完全な機能をプッシュできるか、(GitHub などの) ソース管理システムに変更するまで、ローカルで開発およびテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-218">You, as developer, need to develop and test locally until you push a completed feature or change to your source control system (for example, to GitHub).</span></span> <span data-ttu-id="f12d0-219">つまり、Docker イメージを作成してローカルの Docker ホスト (Windows または Linux VM) にコンテナーを展開し、それらのローカルのコンテナーに対して実行、テスト、およびデバッグをする必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-219">This means that you need to create the Docker images and deploy containers to a local Docker host (Windows or Linux VM) and run, test, and debug against those local containers.</span></span>

<span data-ttu-id="f12d0-220">Docker CLI と Dockerfile を使用して、ローカルの環境にカスタム イメージを作成するには、図 5-5 のとおり、docker build コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-220">To create a custom image in your local environment by using Docker CLI and your Dockerfile, you can use the docker build command, as in Figure 5-5.</span></span>

![カスタム Docker イメージの作成](./media/image8.png)

<span data-ttu-id="f12d0-222">**図 5-5**</span><span class="sxs-lookup"><span data-stu-id="f12d0-222">**Figure 5-5**.</span></span> <span data-ttu-id="f12d0-223">カスタム Docker イメージの作成</span><span class="sxs-lookup"><span data-stu-id="f12d0-223">Creating a custom Docker image</span></span>

<span data-ttu-id="f12d0-224">必要に応じて、プロジェクト フォルダーから docker build を直接実行する代わりに、dotnet publish を実行して必要な .NET ライブラリとバイナリを使用して、展開可能なフォルダーをまず生成し、次いで docker build コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-224">Optionally, instead of directly running docker build from the project folder, you can first generate a deployable folder with the required .NET libraries and binaries by running dotnet publish, and then use the docker build command.</span></span>

<span data-ttu-id="f12d0-225">これにより、**cesardl/netcore-webapi-microservice-docker:first** という名前の Docker イメージが作成されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-225">This will create a Docker image with the name **cesardl/netcore-webapi-microservice-docker:first**.</span></span> <span data-ttu-id="f12d0-226">このとき、:first は特定のバージョンを表すタグです。</span><span class="sxs-lookup"><span data-stu-id="f12d0-226">In this case, :first is a tag representing a specific version.</span></span> <span data-ttu-id="f12d0-227">この手順は、構成した Docker アプリケーション用に作成する必要のある各カスタム イメージで繰り返します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-227">You can repeat this step for each custom image you need to create for your composed Docker application.</span></span>

<span data-ttu-id="f12d0-228">アプリケーションが複数のコンテナーで作成されている場合 (つまり、マルチコンテナー アプリケーションの場合)、docker-compose up ビルド コマンドでは、関連する docker-compose.yml ファイルで公開されているメタデータを使用して、1 つのコマンドですべての関連イメージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-228">When an application is made of multiple containers (that is, it is a multi-container application), you can also use the docker-compose up --build command to build all the related images with a single command by using the metadata exposed in the related docker-compose.yml files.</span></span>

<span data-ttu-id="f12d0-229">図 5-6 の docker images コマンドを使用すると、ローカル リポジトリの既存のイメージを検索できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-229">You can find the existing images in your local repository by using the docker images command, as shown in Figure 5-6.</span></span>

![docker images コマンドを使用した既存のイメージの表示](./media/image9.png)

<span data-ttu-id="f12d0-231">**図 5-6**</span><span class="sxs-lookup"><span data-stu-id="f12d0-231">**Figure 5-6.**</span></span> <span data-ttu-id="f12d0-232">docker images コマンドを使用した既存のイメージの表示</span><span class="sxs-lookup"><span data-stu-id="f12d0-232">Viewing existing images using the docker images command</span></span>

### <a name="creating-docker-images-with-visual-studio"></a><span data-ttu-id="f12d0-233">Visual Studio での Docker イメージの作成</span><span class="sxs-lookup"><span data-stu-id="f12d0-233">Creating Docker images with Visual Studio</span></span>

<span data-ttu-id="f12d0-234">Visual Studio を使用して、Docker のサポートでプロジェクトを作成する場合、イメージは明示的には作成されません。</span><span class="sxs-lookup"><span data-stu-id="f12d0-234">When you use Visual Studio to create a project with Docker support, you don't explicitly create an image.</span></span> <span data-ttu-id="f12d0-235">代わりに、**F5** キーを押し、Docker 化されたアプリケーションまたはサービスを実行することによって、イメージは作成されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-235">Instead, the image is created for you when you press **F5** to run the dockerized application or service.</span></span> <span data-ttu-id="f12d0-236">この手順は Visual Studio で自動的に実行されるので、処理内容を見ることはできませんが、内部の処理内容を知ることは重要です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-236">This step is automatic in Visual Studio and you won't see it happen, but it's important that you know what's going on underneath.</span></span>

![手順 4 - サービスの定義の図](./media/image10.png)

## <a name="step-4-define-your-services-in-docker-composeyml-when-building-a-multi-container-docker-application"></a><span data-ttu-id="f12d0-238">手順 4.</span><span class="sxs-lookup"><span data-stu-id="f12d0-238">Step 4.</span></span> <span data-ttu-id="f12d0-239">マルチ コンテナー Docker アプリケーションを構築するときの docker-compose.yml へのサービスの定義</span><span class="sxs-lookup"><span data-stu-id="f12d0-239">Define your services in docker-compose.yml when building a multi-container Docker application</span></span>

<span data-ttu-id="f12d0-240">[docker-compose.yml](https://docs.docker.com/compose/compose-file/) ファイルでは、展開用のコマンドを使用して構成済みのアプリケーションとして関連サービスのセットを定義できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-240">The [docker-compose.yml](https://docs.docker.com/compose/compose-file/) file lets you define a set of related services to be deployed as a composed application with deployment commands.</span></span>

<span data-ttu-id="f12d0-241">docker-compose.yml ファイルを使用する場合、メインまたはルート ソリューション フォルダーに、次の例と類似した内容でファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-241">To use a docker-compose.yml file, you need to create the file in your main or root solution folder, with content similar to that in the following example:</span></span>

```yml
version: '3'

services:

  webmvc:
    image: eshop/web
    environment:
      - CatalogUrl=http://catalog.api
      - OrderingUrl=http://ordering.api
    ports:
      - "80:80"
    depends_on:
      - catalog.api
      - ordering.api

  catalog.api:
    image: eshop/catalog.api
    environment:
      - ConnectionString=Server=sql.data;Database=CatalogDB;…
    ports:
      - "81:80"
    depends_on:
      - sql.data

  ordering.api:
    image: eshop/ordering.api
    environment:
      - ConnectionString=Server=sql.data;Database=OrderingDb;…
    ports:
      - "82:80"
    extra_hosts:
      - "CESARDLBOOKVHD:10.0.75.1"
    depends_on:
      - sql.data

  sql.data:
    image: mssql-server-linux:latest
    environment:
      - SA_PASSWORD=Pass@word
      - ACCEPT_EULA=Y
    ports:
      - "5433:1433"
```

<span data-ttu-id="f12d0-242">この docker-compose.yml ファイルは、簡略化され、結合されたバージョンです。</span><span class="sxs-lookup"><span data-stu-id="f12d0-242">This docker-compose.yml file is a simplified and merged version.</span></span> <span data-ttu-id="f12d0-243">これには、必ずある (カスタム イメージ名などの) 各コンテナー用の静的な構成データと、展開環境によっては異なる場合のある、接続文字列などの構成情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-243">It contains static configuration data for each container (like the name of the custom image), which always applies, plus configuration information that might depend on the deployment environment, like the connection string.</span></span> <span data-ttu-id="f12d0-244">後半のセクションでは、複数の docker-compose ファイルに docker-compose.yml 構成を分割し、環境と実行の種類 (デバッグまたはリリース) に応じて、値をオーバーライドする方法について学習します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-244">In later sections, you will learn how you can split the docker-compose.yml configuration into multiple docker-compose files and override values depending on the environment and execution type (debug or release).</span></span>

<span data-ttu-id="f12d0-245">docker-compose.yml ファイルの例では、webmvc サービス (Web アプリケーション)、2 つのマイクロサービス (catalog.api および ordering.api)、1 つのデータ ソース コンテナー、コンテナーとして実行される Linux 用 SQL Server の sql.data の 4 つのサービスが定義されています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-245">The docker-compose.yml file example defines four services: the webmvc service (a web application), two microservices (catalog.api and ordering.api), and one data source container, sql.data, based on SQL Server for Linux running as a container.</span></span> <span data-ttu-id="f12d0-246">各サービスはコンテナーとして展開されるので、それぞれに Docker イメージが必要です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-246">Each service is deployed as a container, so a Docker image is required for each.</span></span>

<span data-ttu-id="f12d0-247">docker-compose.yml ファイルでは、どのコンテナーが使用されているかのみでなく、それらがどのように個々に構成されるかが指定されています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-247">The docker-compose.yml file specifies not only what containers are being used, but how they are individually configured.</span></span> <span data-ttu-id="f12d0-248">たとえば、.yml ファイルの webmvc コンテナーの定義は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f12d0-248">For instance, the webmvc container definition in the .yml file:</span></span>

- <span data-ttu-id="f12d0-249">事前にビルドされている eshop/web:latest イメージが使用されています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-249">Uses a pre-built eshop/web:latest image.</span></span> <span data-ttu-id="f12d0-250">ただし、docker-compose の実行の一部として、docker-compose ファイルの build: セクションの追加構成を加え、イメージがビルドされるように構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-250">However, you could also configure the image to be built as part of the docker-compose execution with an additional configuration based on a build: section in the docker-compose file.</span></span>

- <span data-ttu-id="f12d0-251">2 つの環境変数 (CatalogUrl および OrderingUrl) を初期化します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-251">Initializes two environment variables (CatalogUrl and OrderingUrl).</span></span>

- <span data-ttu-id="f12d0-252">コンテナー上の公開されているポート 80 を、ホスト コンピューター上の外部ポート 80 に転送します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-252">Forwards the exposed port 80 on the container to the external port 80 on the host machine.</span></span>

- <span data-ttu-id="f12d0-253">depends\_on 設定を使用して、カタログと順序付けサービスに Web アプリをリンクします。</span><span class="sxs-lookup"><span data-stu-id="f12d0-253">Links the web app to the catalog and ordering service with the depends\_on setting.</span></span> <span data-ttu-id="f12d0-254">これにより、サービスは、それらのサービスが開始されるまで待機するようになります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-254">This causes the service to wait until those services are started.</span></span>

<span data-ttu-id="f12d0-255">docker-compose.yml ファイルについては、マイクロサービスとマルチコンテナー アプリを実装する方法について説明する後のセクションで、再確認します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-255">We will revisit the docker-compose.yml file in a later section when we cover how to implement microservices and multi-container apps.</span></span>

### <a name="working-with-docker-composeyml-in-visual-studio-2017"></a><span data-ttu-id="f12d0-256">Visual Studio 2017 での docker-compose.yml の操作</span><span class="sxs-lookup"><span data-stu-id="f12d0-256">Working with docker-compose.yml in Visual Studio 2017</span></span>

<span data-ttu-id="f12d0-257">図 5-7 に示すように、コンテナー オーケストレーターのサポートを Web アプリ プロジェクトに追加すると、Visual Studio によって docker-compose.yml ファイルを含むソリューション セクション (プロジェクト) がソリューションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-257">When you add container orchestrator support to a web app project, as shown in Figure 5-7, Visual Studio adds a service section (project) to the solution that contains a docker-compose.yml file.</span></span> <span data-ttu-id="f12d0-258">この方法で、マルチコンテナー ソリューションの作成を簡単に始めることができます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-258">This is an easy way to start composing a multiple-container solution.</span></span>

![Visual Studio のコンテナー オーケストレーターのサポートの追加メニュー項目](./media/add-container-orchestrator-support.png)

<span data-ttu-id="f12d0-260">**図 5-7**</span><span class="sxs-lookup"><span data-stu-id="f12d0-260">**Figure 5-7**.</span></span> <span data-ttu-id="f12d0-261">Visual Studio 2017 への ASP.NET Core プロジェクトの右クリックでの Docker サポートの追加</span><span class="sxs-lookup"><span data-stu-id="f12d0-261">Adding Docker support in Visual Studio 2017 by right-clicking an ASP.NET Core project</span></span>

<span data-ttu-id="f12d0-262">コンテナー オーケストレーターのサポートを追加すると、Docker ファイルが存在しない場合はプロジェクトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-262">Adding container orchestrator support adds the Dockerfile to your project (if it doesn't already exist).</span></span> <span data-ttu-id="f12d0-263">また、ソリューション レベルのグローバル docker-compose.yml ファイルに構成情報も追加されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-263">It also adds configuration information to a global docker-compose.yml file at the solution level.</span></span> <span data-ttu-id="f12d0-264">図 5-8 に示すように、docker-compose.yml ファイルを含む新しいプロジェクト ノード (*docker-compose.dcproj* プロジェクト ファイル) が**ソリューション エクスプローラー**に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-264">You'll see a new project node (the *docker-compose.dcproj* project file) in **Solution Explorer** that contains the docker-compose.yml file, as shown in Figure 5-8.</span></span>

![ソリューション エクスプローラーの docker-compose ノード](./media/docker-compose-files.png)

<span data-ttu-id="f12d0-266">**図 5-8**.</span><span class="sxs-lookup"><span data-stu-id="f12d0-266">**Figure 5-8**.</span></span> <span data-ttu-id="f12d0-267">Visual Studio 2017 のソリューション エクスプローラーに追加された **docker-compose** ツリー ノード</span><span class="sxs-lookup"><span data-stu-id="f12d0-267">The **docker-compose** tree node added in Visual Studio 2017 Solution Explorer</span></span>

<span data-ttu-id="f12d0-268">その後、docker-compose.yml ファイルを開き、追加機能で更新することができます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-268">You can then open the docker-compose.yml file and update it with additional features.</span></span>

<span data-ttu-id="f12d0-269">`docker-compose up` コマンドを使用すると、1 つの docker-compose.yml ファイルで、マルチコンテナー アプリケーションを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-269">You can deploy a multi-container application with a single docker-compose.yml file by using the `docker-compose up` command.</span></span>

![手順 5 - アプリの実行の図](./media/image12.png)

## <a name="step-5-build-and-run-your-docker-application"></a><span data-ttu-id="f12d0-271">手順 5.</span><span class="sxs-lookup"><span data-stu-id="f12d0-271">Step 5.</span></span> <span data-ttu-id="f12d0-272">Docker アプリケーションのビルドと実行</span><span class="sxs-lookup"><span data-stu-id="f12d0-272">Build and run your Docker application</span></span>

<span data-ttu-id="f12d0-273">アプリケーションにコンテナーが 1 つしかない場合、Docker ホスト (仮想マシンまたは物理サーバー) に展開して実行することができます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-273">If your application only has a single container, you can run it by deploying it to your Docker host (VM or physical server).</span></span> <span data-ttu-id="f12d0-274">ただし、アプリケーションに複数のサービスが含まれている場合、単一の CLI コマンド (docker-compose up) を使用するか、背後でそのコマンドを使用する Visual Studio を使用して、構成されたアプリケーションとして展開することができます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-274">However, if your application contains multiple services, you can deploy it as a composed application, either using a single CLI command (docker-compose up), or with Visual Studio, which will use that command under the covers.</span></span> <span data-ttu-id="f12d0-275">別のオプションを見てみましょう。</span><span class="sxs-lookup"><span data-stu-id="f12d0-275">Let’s look at the different options.</span></span>

### <a name="option-a-run-a-single-container-app"></a><span data-ttu-id="f12d0-276">オプション A: 単一コンテナー アプリを実行する</span><span class="sxs-lookup"><span data-stu-id="f12d0-276">Option A: Run a single-container app</span></span>

#### <a name="docker-cli"></a><span data-ttu-id="f12d0-277">Docker CLI</span><span class="sxs-lookup"><span data-stu-id="f12d0-277">Docker CLI</span></span>

<span data-ttu-id="f12d0-278">図 5-9 に示すように、docker run コマンドを使用して Docker コンテナーを実行できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-278">You can run a Docker container using the docker run command, as in Figure 5-9:</span></span>

```console
  docker run -t -d -p 80:5000 cesardl/netcore-webapi-microservice-docker:first
```

![docker run コマンドを使用した Docker コンテナーの実行](./media/image13.png)

<span data-ttu-id="f12d0-280">**図 5-9**</span><span class="sxs-lookup"><span data-stu-id="f12d0-280">**Figure 5-9**.</span></span> <span data-ttu-id="f12d0-281">docker run コマンドを使用した Docker コンテナーの実行</span><span class="sxs-lookup"><span data-stu-id="f12d0-281">Running a Docker container using the docker run command</span></span>

<span data-ttu-id="f12d0-282">この場合、このコマンドによって、コンテナーの内部ポート 5000 がホスト コンピューターのポート 80 にバインドされます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-282">In this case, the command binds the internal port 5000 of the container to port 80 of the host machine.</span></span> <span data-ttu-id="f12d0-283">つまり、ホストはポート 80 をリッスンし、コンテナーのポート 5000 に転送することを意味します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-283">This means that the host is listening on port 80 and forwarding to port 5000 on the container.</span></span>

#### <a name="visual-studio"></a><span data-ttu-id="f12d0-284">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f12d0-284">Visual Studio</span></span>

<span data-ttu-id="f12d0-285">コンテナー オーケストレーターのサポートを追加していない場合は、Visual Studio で **F5** キーを押して単一コンテナー アプリを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-285">If you haven't added container orchestrator support, you can also run a single container app in Visual Studio by pressing **F5**.</span></span> <span data-ttu-id="f12d0-286">コンテナーは、docker run を使用してローカルで実行されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-286">The container runs locally using docker run.</span></span>

### <a name="option-b-run-a-multi-container-app"></a><span data-ttu-id="f12d0-287">オプション B: マルチコンテナー アプリを実行する</span><span class="sxs-lookup"><span data-stu-id="f12d0-287">Option B: Run a multi-container app</span></span>

<span data-ttu-id="f12d0-288">多くのエンタープライズ シナリオでは、Docker アプリケーションは複数のサービスで構成されています。つまり、図 5-10 のようにマルチコンテナーのアプリケーションを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-288">In most enterprise scenarios, a Docker application will be composed of multiple services, which means you need to run a multi-container application, as shown in Figure 5-10.</span></span>

![Docker コンテナーが展開された VM の図](./media/image14.png)

<span data-ttu-id="f12d0-290">**図 5-10**</span><span class="sxs-lookup"><span data-stu-id="f12d0-290">**Figure 5-10**.</span></span> <span data-ttu-id="f12d0-291">Docker コンテナーが展開された VM</span><span class="sxs-lookup"><span data-stu-id="f12d0-291">VM with Docker containers deployed</span></span>

#### <a name="docker-cli"></a><span data-ttu-id="f12d0-292">Docker CLI</span><span class="sxs-lookup"><span data-stu-id="f12d0-292">Docker CLI</span></span>

<span data-ttu-id="f12d0-293">Docker CLI を使用してマルチコンテナー アプリケーションを実行するには、docker-compose up コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-293">To run a multi-container application with the Docker CLI, you can run the docker-compose up command.</span></span> <span data-ttu-id="f12d0-294">このコマンドでは、ソリューション レベルにある、マルチコンテナー アプリケーションを展開する docker compose.yml ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-294">This command uses the docker-compose.yml file that you have at the solution level to deploy a multi-container application.</span></span> <span data-ttu-id="f12d0-295">図 5-11 は、docker-compose.yml ファイルを含む、メインのプロジェクト ディレクトリからコマンドを実行した結果を示しています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-295">Figure 5-11 shows the results when running the command from your main project directory, which contains the docker-compose.yml file.</span></span>

![docker-compose up コマンドの実行結果の例](./media/image15.png)

<span data-ttu-id="f12d0-297">**図 5-11**</span><span class="sxs-lookup"><span data-stu-id="f12d0-297">**Figure 5-11**.</span></span> <span data-ttu-id="f12d0-298">docker-compose up コマンドの実行結果の例</span><span class="sxs-lookup"><span data-stu-id="f12d0-298">Example results when running the docker-compose up command</span></span>

<span data-ttu-id="f12d0-299">docker-compose up コマンドを実行すると、アプリケーションとその関連コンテナーが Docker ホストに展開されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-299">After the docker-compose up command runs, the application and its related containers are deployed into your Docker host.</span></span>

#### <a name="visual-studio"></a><span data-ttu-id="f12d0-300">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f12d0-300">Visual Studio</span></span>

<span data-ttu-id="f12d0-301">Visual Studio 2017 を使用したマルチコンテナー アプリケーションの実行は簡単です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-301">Running a multi-container application using Visual Studio 2017 is simple.</span></span> <span data-ttu-id="f12d0-302">マルチコンテナー アプリケーションを実行できるだけでなく、標準のブレークポイントを設定することで、そのすべてのコンテナーを Visual Studio から直接デバッグできるようになります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-302">Not only can you run the multi-container application, but you're able to debug all its containers directly from Visual Studio by setting regular breakpoints.</span></span>

<span data-ttu-id="f12d0-303">既に説明したとおり、ソリューション内のプロジェクトにコンテナー オーケストレーターのサポートを追加するたびに、そのプロジェクトは、グローバル (ソリューション レベル) docker-compose.yml ファイルに構成され、一度にソリューション全体を実行またはデバッグできるようになります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-303">As mentioned before, each time you add container orchestrator support to a project within a solution, that project is configured in the global (solution-level) docker-compose.yml file, which lets you run or debug the whole solution at once.</span></span> <span data-ttu-id="f12d0-304">Visual Studio では、Docker ソリューションのサポートが有効になっているプロジェクトごとに 1 つのコンテナーが起動され、内部のすべての手順をユーザーのために実行してくれます (dotnet publish、docker build など)。</span><span class="sxs-lookup"><span data-stu-id="f12d0-304">Visual Studio will start one container for each project that has Docker solution support enabled and perform all the internal steps for you (dotnet publish, docker build, etc.).</span></span>

<span data-ttu-id="f12d0-305">ここで重要な点は、図 5-12 に示すように、**F5** キー操作用に **Docker** コマンドが Visual Studio 2017 に追加されていることです。</span><span class="sxs-lookup"><span data-stu-id="f12d0-305">The important point here is that, as shown in Figure 5-12, in Visual Studio 2017 there's an additional **Docker** command for the **F5** key action.</span></span> <span data-ttu-id="f12d0-306">このオプションでは、ソリューション レベルで docker-compose.yml ファイルに定義されているすべてのコンテナーを実行して、マルチコンテナー アプリケーションを実行またはデバッグできます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-306">This option lets you run or debug a multi-container application by running all the containers that are defined in the docker-compose.yml files at the solution level.</span></span> <span data-ttu-id="f12d0-307">マルチコンテナー ソリューションをデバッグできるということは、異なるプロジェクト (コンテナー) にそれぞれブレークポイントを設定でき (いくつかブレークポイントを設定でき)、Visual Studio でデバッグする際、別のプロジェクトに定義され、別のコンテナーで実行されているブレークポイントで停止されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-307">The ability to debug multiple-container solutions means that you can set several breakpoints, each breakpoint in a different project (container), and while debugging from Visual Studio you will stop at breakpoints defined in different projects and running on different containers.</span></span>

![Visual Studio 2017 でのマルチコンテナー アプリの実行](./media/image16.png)

<span data-ttu-id="f12d0-309">**図 5-12**</span><span class="sxs-lookup"><span data-stu-id="f12d0-309">**Figure 5-12**.</span></span> <span data-ttu-id="f12d0-310">Visual Studio 2017 でのマルチコンテナー アプリの実行</span><span class="sxs-lookup"><span data-stu-id="f12d0-310">Running multi-container apps in Visual Studio 2017</span></span>

### <a name="additional-resources"></a><span data-ttu-id="f12d0-311">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="f12d0-311">Additional resources</span></span>

-  <span data-ttu-id="f12d0-312">**リモート Docker ホストに ASP.NET コンテナーを配置する**</span><span class="sxs-lookup"><span data-stu-id="f12d0-312">**Deploy an ASP.NET container to a remote Docker host**</span></span>

   [*https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker*](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)

### <a name="a-note-about-testing-and-deploying-with-orchestrators"></a><span data-ttu-id="f12d0-313">オーケストレーターを使用したテストと展開に関する注意事項</span><span class="sxs-lookup"><span data-stu-id="f12d0-313">A note about testing and deploying with orchestrators</span></span>

<span data-ttu-id="f12d0-314">開発環境でコンテナーをテストするには、docker-compose up および docker run コマンド (または Visual Studio でのコンテナーの実行およびデバッグ) で十分です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-314">The docker-compose up and docker run commands (or running and debugging the containers in Visual Studio) are adequate for testing containers in your development environment.</span></span> <span data-ttu-id="f12d0-315">ただし、Docker クラスター、Docker Swarm、Mesosphere DC/OS、Kubernetes などのオーケストレーターをターゲットとしている場合は、このアプローチは使用しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-315">But you should not use this approach if you are targeting Docker clusters and orchestrators like Docker Swarm, Mesosphere DC/OS, or Kubernetes.</span></span> <span data-ttu-id="f12d0-316">[Docker Swarm モード](https://docs.docker.com/engine/swarm/) (Docker CE for Windows および Mac のバージョン 1.12 以降で利用可能) などのクラスターを使用している場合、1 つのサービスに [docker service create](https://docs.docker.com/engine/reference/commandline/service_create/) などのその他のコマンドを使用して展開およびテストをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-316">If you are using a cluster like [Docker Swarm mode](https://docs.docker.com/engine/swarm/) (available in Docker CE for Windows and Mac since version 1.12), you need to deploy and test with additional commands like [docker service create](https://docs.docker.com/engine/reference/commandline/service_create/) for single services.</span></span> <span data-ttu-id="f12d0-317">いくつかのコンテナーで構成されるアプリケーションを展開する場合、[docker compose bundle](https://docs.docker.com/compose/reference/bundle/) および [docker deploy myBundleFile](https://docs.docker.com/engine/reference/commandline/deploy/) を使用して、構成されたアプリケーションを*スタック*として展開できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-317">If you are deploying an application composed of several containers, you use [docker compose bundle](https://docs.docker.com/compose/reference/bundle/) and [docker deploy myBundleFile](https://docs.docker.com/engine/reference/commandline/deploy/) to deploy the composed application as a *stack*.</span></span> <span data-ttu-id="f12d0-318">詳細については、Docker サイト上の Docker ドキュメント「[Introducing Experimental Distributed Application Bundles](https://blog.docker.com/2016/06/docker-app-bundle/)」(実験的な分散アプリケーション バンドルの概要) のブログ投稿を参照してください</span><span class="sxs-lookup"><span data-stu-id="f12d0-318">For more information, see the blog post [Introducing Experimental Distributed Application Bundles](https://blog.docker.com/2016/06/docker-app-bundle/) in the Docker documentation.</span></span> <span data-ttu-id="f12d0-319">。</span><span class="sxs-lookup"><span data-stu-id="f12d0-319">on the Docker site.</span></span>

<span data-ttu-id="f12d0-320">[DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) と [Kubernetes](https://kubernetes.io/docs/user-guide/deployments/) については、同様に別の展開用のコマンドとスクリプトを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-320">For [DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) and [Kubernetes](https://kubernetes.io/docs/user-guide/deployments/) you would use different deployment commands and scripts as well.</span></span>

![手順 6 の図](./media/image17.png)

## <a name="step-6-test-your-docker-application-using-your-local-docker-host"></a><span data-ttu-id="f12d0-322">手順 6.</span><span class="sxs-lookup"><span data-stu-id="f12d0-322">Step 6.</span></span> <span data-ttu-id="f12d0-323">ローカル Docker ホストを使用した Docker アプリケーションのテスト</span><span class="sxs-lookup"><span data-stu-id="f12d0-323">Test your Docker application using your local Docker host</span></span>

<span data-ttu-id="f12d0-324">この手順は、アプリケーションで何が実行されているかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-324">This step will vary depending on what your application is doing.</span></span> <span data-ttu-id="f12d0-325">単一のコンテナーやサービスとして展開された単純な .NET Core Web アプリケーションでは、図 5-13 に示すように、Docker ホストでブラウザーを開き、サイトに移動して、サービスにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-325">In a simple .NET Core Web application that is deployed as a single container or service, you can access the service by opening a browser on the Docker host and navigating to that site, as shown in Figure 5-13.</span></span> <span data-ttu-id="f12d0-326">(Dockerfile の構成で、コンテナーがホストの 80 以外のポートにマップされる場合、この URL にホスト ポストを含めます。)</span><span class="sxs-lookup"><span data-stu-id="f12d0-326">(If the configuration in the Dockerfile maps the container to a port on the host that is anything other than 80, include the host port in the URL.)</span></span>

![localhost を使用したローカルでの Docker アプリケーションのテスト例](./media/image18.png)

<span data-ttu-id="f12d0-328">**図 5-13**</span><span class="sxs-lookup"><span data-stu-id="f12d0-328">**Figure 5-13**.</span></span> <span data-ttu-id="f12d0-329">localhost を使用したローカルでの Docker アプリケーションのテスト例</span><span class="sxs-lookup"><span data-stu-id="f12d0-329">Example of testing your Docker application locally using localhost</span></span>

<span data-ttu-id="f12d0-330">localhost が Docker ホスト IP をポイントしていない場合 (Docker CE を使用している場合、既定ではしている必要があります)、サービスに移動するには、コンピューターのネットワーク カードの IP アドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-330">If localhost is not pointing to the Docker host IP (by default, when using Docker CE, it should), to navigate to your service, use the IP address of your machine’s network card.</span></span>

<span data-ttu-id="f12d0-331">ブラウザーのこの URL では、説明している特定のコンテナーの例に、ポート 80 を使用しています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-331">This URL in the browser uses port 80 for the particular container example being discussed.</span></span> <span data-ttu-id="f12d0-332">ただし、前の手順で説明したとおり、docker run コマンドで展開されたとおり、要求は内部でポート 5000 にリダイレクトされています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-332">However, internally the requests are being redirected to port 5000, because that was how it was deployed with the docker run command, as explained in a previous step.</span></span>

<span data-ttu-id="f12d0-333">図 5-14 のとおり、ターミナルからカールを使用して、アプリケーションをテストすることも可能です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-333">You can also test the application using curl from the terminal, as shown in Figure 5-14.</span></span> <span data-ttu-id="f12d0-334">Windows の Docker インストールでは、既定の Docker ホスト IP は、常にマシンの実際の IP アドレスに 10.0.75.1 を加えたものです。</span><span class="sxs-lookup"><span data-stu-id="f12d0-334">In a Docker installation on Windows, the default Docker Host IP is always 10.0.75.1 in addition to your machine’s actual IP address.</span></span>

![カールを使用したローカルでの Docker アプリケーションのテスト例](./media/image19.png)

<span data-ttu-id="f12d0-336">**図 5-14**</span><span class="sxs-lookup"><span data-stu-id="f12d0-336">**Figure 5-14**.</span></span> <span data-ttu-id="f12d0-337">カールを使用したローカルでの Docker アプリケーションのテスト例</span><span class="sxs-lookup"><span data-stu-id="f12d0-337">Example of testing your Docker application locally using curl</span></span>

### <a name="testing-and-debugging-containers-with-visual-studio-2017"></a><span data-ttu-id="f12d0-338">Visual Studio 2017 を使用したコンテナーのテストおよびデバッグ</span><span class="sxs-lookup"><span data-stu-id="f12d0-338">Testing and debugging containers with Visual Studio 2017</span></span>

<span data-ttu-id="f12d0-339">Visual Studio 2017 でコンテナーを実行またはデバッグする場合、.NET アプリケーションのデバッグは、コンテナーを使用しないでデバッグするのとほぼ同じ方法で実行できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-339">When running and debugging the containers with Visual Studio 2017, you can debug the .NET application in much the same way as you would when running without containers.</span></span>

### <a name="testing-and-debugging-without-visual-studio"></a><span data-ttu-id="f12d0-340">Visual Studio を使用しないデバッグおよびテスト</span><span class="sxs-lookup"><span data-stu-id="f12d0-340">Testing and debugging without Visual Studio</span></span>

<span data-ttu-id="f12d0-341">エディター/CLI アプローチを使用して開発をする場合、コンテナーのデバッグはより難しいので、トレースを生成してデバッグした方がよいでしょう。</span><span class="sxs-lookup"><span data-stu-id="f12d0-341">If you are developing using the editor/CLI approach, debugging containers is more difficult and you will want to debug by generating traces.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="f12d0-342">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="f12d0-342">Additional resources</span></span>

- <span data-ttu-id="f12d0-343">**ローカルの Docker コンテナーでアプリをデバッグする**</span><span class="sxs-lookup"><span data-stu-id="f12d0-343">**Debugging apps in a local Docker container**</span></span>

   [*https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh*](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)

- <span data-ttu-id="f12d0-344">**作成者: Steve Lasker。Docker を使用した ASP.NET Core アプリのビルド、デバッグおよび展開。**</span><span class="sxs-lookup"><span data-stu-id="f12d0-344">**Steve Lasker. Build, Debug, Deploy ASP.NET Core Apps with Docker.**</span></span> <span data-ttu-id="f12d0-345">ビデオ。</span><span class="sxs-lookup"><span data-stu-id="f12d0-345">Video.</span></span>

   [*https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T115*](https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T115)

## <a name="simplified-workflow-when-developing-containers-with-visual-studio"></a><span data-ttu-id="f12d0-346">Visual Studio でのコンテナー開発の簡略ワークフロー</span><span class="sxs-lookup"><span data-stu-id="f12d0-346">Simplified workflow when developing containers with Visual Studio</span></span>

<span data-ttu-id="f12d0-347">Visual Studio を使用するワークフローは、エディター/CLI アプローチを使用するワークフローよりも、実際はるかに簡単になります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-347">Effectively, the workflow when using Visual Studio is a lot simpler than if you use the editor/CLI approach.</span></span> <span data-ttu-id="f12d0-348">Dockerfile と docker-compose.yml ファイルに関係する Docker で必要な多くの手順は、図 5-15 のとおり、Visual Studio では背後で実行されるか、簡略化されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-348">Most of the steps required by Docker related to the Dockerfile and docker-compose.yml files are hidden or simplified by Visual Studio, as shown in Figure 5-15.</span></span>

![Visual Studio での開発の簡略ワークフロー](./media/image20.png)

<span data-ttu-id="f12d0-350">**図 5-15**。</span><span class="sxs-lookup"><span data-stu-id="f12d0-350">**Figure 5-15**.</span></span> <span data-ttu-id="f12d0-351">Visual Studio での開発の簡略ワークフロー</span><span class="sxs-lookup"><span data-stu-id="f12d0-351">Simplified workflow when developing with Visual Studio</span></span>

<span data-ttu-id="f12d0-352">これに加え、(プロジェクトに Docker のサポートを追加する) 手順 2 を、一度のみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-352">In addition, you need to perform step 2 (adding Docker support to your projects) just once.</span></span> <span data-ttu-id="f12d0-353">つまり、ワークフローは、他の任意の開発に .NET を使用する場合の通常の開発タスクと似たものになります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-353">Therefore, the workflow is similar to your usual development tasks when using .NET for any other development.</span></span> <span data-ttu-id="f12d0-354">背後で何が起こっているのか (イメージのビルド手順、使用している基本イメージ、コンテナーの展開など) を理解しておく必要があり、動作をカスタマイズするのに Dockerfile または docker-compose.yml ファイルを編集する必要がある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="f12d0-354">You need to know what is going on under the covers (the image build process, what base images you are using, deployment of containers, etc.) and sometimes you will also need to edit the Dockerfile or docker-compose.yml file to customize behaviors.</span></span> <span data-ttu-id="f12d0-355">しかし、多くの作業は Visual Studio を使用することで大幅に簡略化され、ユーザーの生産性を向上させます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-355">But most of the work is greatly simplified by using Visual Studio, making you a lot more productive.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="f12d0-356">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="f12d0-356">Additional resources</span></span>

- <span data-ttu-id="f12d0-357">**作成者: Steve Lasker。Visual Studio 2017 を使用した .NET Docker の開発**</span><span class="sxs-lookup"><span data-stu-id="f12d0-357">**Steve Lasker. .NET Docker Development with Visual Studio 2017**</span></span>

   [*https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T111*](https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T111)

- <span data-ttu-id="f12d0-358">**作成者: Jeffrey T. Fritz。Visual Studio の新しい Docker ツールを使用してコンテナーに .NET Core アプリを配置する**</span><span class="sxs-lookup"><span data-stu-id="f12d0-358">**Jeffrey T. Fritz. Put a .NET Core App in a Container with the new Docker Tools for Visual Studio**</span></span>

   [*https://blogs.msdn.microsoft.com/webdev/2016/11/16/new-docker-tools-for-visual-studio/*](https://blogs.msdn.microsoft.com/webdev/2016/11/16/new-docker-tools-for-visual-studio/)

## <a name="using-powershell-commands-in-a-dockerfile-to-set-up-windows-containers"></a><span data-ttu-id="f12d0-359">Windows コンテナーを設定するための PowerShell コマンドの使用</span><span class="sxs-lookup"><span data-stu-id="f12d0-359">Using PowerShell commands in a Dockerfile to set up Windows Containers</span></span>

<span data-ttu-id="f12d0-360">[Windows コンテナー](/virtualization/windowscontainers/about/)は、既存の Windows アプリケーションを Docker イメージに変換して、Docker エコシステムの残りと同じツールで展開できます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-360">[Windows Containers](/virtualization/windowscontainers/about/) allow you to convert your existing Windows applications into Docker images and deploy them with the same tools as the rest of the Docker ecosystem.</span></span> <span data-ttu-id="f12d0-361">Windows コンテナーを使用するには、次の例のように、Dockerfile で PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f12d0-361">To use Windows Containers, you run PowerShell commands in the Dockerfile, as shown in the following example:</span></span>

```Dockerfile
FROM microsoft/windowsservercore

LABEL Description="IIS" Vendor="Microsoft" Version="10"

RUN powershell -Command Add-WindowsFeature Web-Server

CMD [ "ping", "localhost", "-t" ]
```

<span data-ttu-id="f12d0-362">この場合は、Windows Server Core 基本イメージ (FROM 設定) を使用して、PowerShell コマンド (RUN 設定) で IIS をインストールしています。</span><span class="sxs-lookup"><span data-stu-id="f12d0-362">In this case, we are using a Windows Server Core base image (the FROM setting) and installing IIS with a PowerShell command (the RUN setting).</span></span> <span data-ttu-id="f12d0-363">同様に、PowerShell コマンドを使用して、ASP.NET 4.x、.NET 4.6、またはその他の任意の Windows ソフトウェアなどの追加コンポーネントを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-363">In a similar way, you could also use PowerShell commands to set up additional components like ASP.NET 4.x, .NET 4.6, or any other Windows software.</span></span> <span data-ttu-id="f12d0-364">たとえば、Dockerfile の次のコマンドでは、ASP.NET 4.5 が設定されます。</span><span class="sxs-lookup"><span data-stu-id="f12d0-364">For example, the following command in a Dockerfile sets up ASP.NET 4.5:</span></span>

```Dockerfile
RUN powershell add-windowsfeature web-asp-net45
```

### <a name="additional-resources"></a><span data-ttu-id="f12d0-365">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="f12d0-365">Additional resources</span></span>

- <span data-ttu-id="f12d0-366">**aspnet-docker/Dockerfile.**</span><span class="sxs-lookup"><span data-stu-id="f12d0-366">**aspnet-docker/Dockerfile.**</span></span> <span data-ttu-id="f12d0-367">Windows の機能を含めるために dockerfile から実行する Powershell コマンドの例です。</span><span class="sxs-lookup"><span data-stu-id="f12d0-367">Example Powershell commands to run from dockerfiles to include Windows features.</span></span>

   [*https://github.com/Microsoft/aspnet-docker/blob/master/4.6.2/Dockerfile*](https://github.com/Microsoft/aspnet-docker/blob/master/4.6.2/Dockerfile)

>[!div class="step-by-step"]
<span data-ttu-id="f12d0-368">[前へ](index.md)
[次へ](../net-core-single-containers-linux-windows-server-hosts/index.md)</span><span class="sxs-lookup"><span data-stu-id="f12d0-368">[Previous](index.md)
[Next](../net-core-single-containers-linux-windows-server-hosts/index.md)</span></span>