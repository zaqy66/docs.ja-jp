---
title: Linux コンテナーと AKS/Kubernetes クラスターにデプロイされた ASP.NET Core 2.1 アプリケーションを構築します。
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: b03b6fab9dcd53e97c2bc4d7e5c958ca4b931077
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221486"
---
# <a name="build-aspnet-core-21-applications-deployed-as-linux-containers-into-akskubernetes-orchestrator"></a><span data-ttu-id="10fd5-103">AKS/Kubernetes オーケストレーターに Linux コンテナーとして展開されている ASP.NET Core 2.1 アプリケーションを構築します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-103">Build ASP.NET Core 2.1 applications deployed as Linux containers into AKS/Kubernetes orchestrator</span></span>

<span data-ttu-id="10fd5-104">Azure Kubernetes サービス (AKS) は、Azure の管理された Kubernetes オーケストレーション サービスをコンテナーのデプロイと管理を簡略化します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-104">Azure Kubernetes Services (AKS) is Azure's managed Kubernetes orchestrations services that simplify container deployment and management.</span></span>

<span data-ttu-id="10fd5-105">AKS の主な機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="10fd5-105">AKS main features are:</span></span>

- <span data-ttu-id="10fd5-106">Azure でホストされるコントロール プレーンは、</span><span class="sxs-lookup"><span data-stu-id="10fd5-106">An Azure-hosted control plane</span></span>
- <span data-ttu-id="10fd5-107">自動アップグレード</span><span class="sxs-lookup"><span data-stu-id="10fd5-107">Automated upgrades</span></span>
- <span data-ttu-id="10fd5-108">自己復旧機能</span><span class="sxs-lookup"><span data-stu-id="10fd5-108">Self-healing</span></span>
- <span data-ttu-id="10fd5-109">ユーザー構成可能なスケーリング</span><span class="sxs-lookup"><span data-stu-id="10fd5-109">User configurable scaling</span></span>
- <span data-ttu-id="10fd5-110">開発者とクラスター オペレーターの両方に簡単なユーザー エクスペリエンス。</span><span class="sxs-lookup"><span data-stu-id="10fd5-110">A simpler user experience for both developers and cluster operators.</span></span>

<span data-ttu-id="10fd5-111">次の例では、Linux で実行され、開発が完了、Azure では、AKS クラスターを展開する ASP.NET Core 2.1 アプリケーションの作成を探索する Visual Studio 2017 を使用します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-111">The following examples explore the creation of an ASP.NET Core 2.1 application that runs on Linux and deploys to an AKS Cluster in Azure, while development is done using Visual Studio 2017.</span></span>

## <a name="creating-the-aspnet-core-21-project-using-visual-studio-2017"></a><span data-ttu-id="10fd5-112">Visual Studio 2017 を使用して ASP.NET Core 2.1 のプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="10fd5-112">Creating the ASP.NET Core 2.1 Project using Visual Studio 2017</span></span>

<span data-ttu-id="10fd5-113">ASP.NET Core は、Microsoft と GitHub の .NET コミュニティによって管理される汎用的な開発プラットフォームです。</span><span class="sxs-lookup"><span data-stu-id="10fd5-113">ASP.NET Core is a general-purpose development platform maintained by Microsoft and the .NET community on GitHub.</span></span> <span data-ttu-id="10fd5-114">クロスプラットフォームであり、Windows、macOS、Linux をサポートし、デバイス、クラウド、および埋め込み/IoT シナリオで使用できます。</span><span class="sxs-lookup"><span data-stu-id="10fd5-114">It is cross-platform, supporting Windows, macOS and Linux, and can be used in device, cloud, and embedded/IoT scenarios.</span></span>

<span data-ttu-id="10fd5-115">この例では、単純なプロジェクト基づいている、Visual Studio の Web API テンプレートに基づいているため、サンプルを作成する追加に関する知識は不要で使用します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-115">This example uses a simple project that's based based on a Visual Studio Web API template, so you don't need any additional knowledge to create the sample.</span></span> <span data-ttu-id="10fd5-116">のみ、ASP.NET Core 2.1 のテクノロジを使用して、REST API を使用した小規模なプロジェクトを実行するすべての要素を含む標準のテンプレートを使用してプロジェクトを作成する必要があるとします。</span><span class="sxs-lookup"><span data-stu-id="10fd5-116">You only have to create the project using a standard template that includes all the elements to run a small project with a REST API, using ASP.NET Core 2.1 technology.</span></span>

![ASP.NET Core Web アプリケーションを選択すると、Visual Studio で新しいプロジェクト ウィンドウを追加します。](media/create-aspnet-core-application.png)

<span data-ttu-id="10fd5-118">**図 4 ~ 36**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-118">**Figure 4-36**.</span></span> <span data-ttu-id="10fd5-119">ASP.NET Core アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-119">Creating ASP.NET Core Application</span></span>

<span data-ttu-id="10fd5-120">サンプル プロジェクトを作成するには、選択する必要が**ファイル** > **新規** > **プロジェクト**Visual Studio でします。</span><span class="sxs-lookup"><span data-stu-id="10fd5-120">To create the sample project, you have to select **File** > **New** > **Project** on Visual Studio.</span></span> <span data-ttu-id="10fd5-121">検索がある、いくつかの種類のプロジェクト、テンプレートの一覧が表示されます、 **Web** > **.NET Core**左側のパネルにします。</span><span class="sxs-lookup"><span data-stu-id="10fd5-121">Then you'll see a list of templates for several types of projects, where you have to look for **Web** > **.NET Core** on the left panel.</span></span> <span data-ttu-id="10fd5-122">この例では次のように選択します。 **ASP.NET Core Web アプリケーション**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-122">For this example select **ASP.NET Core Web Application**.</span></span>

<span data-ttu-id="10fd5-123">次のダイアログ ボックスでは、4-37 の図に示すように、上位 pulldowns でターゲット フレームワークとして .NET Core と ASP.NET Core 2.1 が選択されているし、ASP.NET Core Web API アプリケーションを作成する、API オプションを選択することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="10fd5-123">In the next dialog ensure that you have selected .NET Core and ASP.NET Core 2.1 as the target framework in the top pulldowns, as shown in figure 4-37, and then select the API option, to create an ASP.NET Core Web API application.</span></span>

<span data-ttu-id="10fd5-124">.NET Core 2.1 は、Visual Studio 2017 バージョン 15.7.0 に含まれる以上と、自動的にインストールされているし、選択すると、構成、 **.NET Core クロス プラットフォーム開発**ワークロードのインストール時にします。</span><span class="sxs-lookup"><span data-stu-id="10fd5-124">The .NET Core 2.1 is included in Visual Studio 2017 version 15.7.0 or higher and is automatically installed and configured for you when you select the **.NET Core cross-platform development** workload during installation.</span></span>

![API オプションを選択して、ASP.NET Core Web アプリケーションの種類を選択するための visual Studio のダイアログ。](media/create-web-api-application.png)

<span data-ttu-id="10fd5-126">**図 4-37**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-126">**Figure 4-37**.</span></span> <span data-ttu-id="10fd5-127">ASP.NET CORE 2.1 を選択し、Web API プロジェクトの種類</span><span class="sxs-lookup"><span data-stu-id="10fd5-127">Selecting ASP.NET CORE 2.1 and Web API project type</span></span>

<span data-ttu-id="10fd5-128">以前のバージョンの .NET Core を使っている場合は、ダウンロードしてからバージョン 2.1 のインストール<https://www.microsoft.com/net/download/core#/sdk>します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-128">If you have any previous version of .NET Core, you can download and install the 2.1 version from <https://www.microsoft.com/net/download/core#/sdk>.</span></span>

<span data-ttu-id="10fd5-129">前の手順で、または後で、プロジェクトの開始後に生じた場合に、プロジェクトを作成する場合は、Docker サポートを追加できます。</span><span class="sxs-lookup"><span data-stu-id="10fd5-129">You can add Docker support when creating the project in the previous step, or later, if the need arises after starting the project.</span></span> <span data-ttu-id="10fd5-130">プロジェクトの作成後に、Docker サポートを追加するでプロジェクト ファイルを右クリックし、**ソリューション エクスプ ローラー**選択**追加** > **Docker サポート**でコンテキスト メニュー。</span><span class="sxs-lookup"><span data-stu-id="10fd5-130">To add the Docker support after the project creation, right-click on the project file in the **Solution Explorer** and select **Add** > **Docker support** on the context menu.</span></span>

![既存のプロジェクトに Docker サポートを追加するコンテキスト メニュー オプション:(プロジェクト) を右クリックして > 追加 > Docker のサポート。](media/add-docker-support-to-project.png)

<span data-ttu-id="10fd5-132">**図 4-38**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-132">**Figure 4-38**.</span></span> <span data-ttu-id="10fd5-133">既存のプロジェクトに Docker サポートの追加</span><span class="sxs-lookup"><span data-stu-id="10fd5-133">Adding Docker support to existing project</span></span>

<span data-ttu-id="10fd5-134">Docker のサポートを追加を完了するには、するには、Windows または Linux の選択肢があります。</span><span class="sxs-lookup"><span data-stu-id="10fd5-134">To complete adding Docker support, you have the choice of Windows or Linux.</span></span> <span data-ttu-id="10fd5-135">この場合は、選択**Linux**AKS は (2018 年末) としての Windows コンテナーをサポートしないためです。</span><span class="sxs-lookup"><span data-stu-id="10fd5-135">In this case, select **Linux**, because AKS doesn’t support Windows Containers (as of late 2018).</span></span>

![Dockerfile のターゲット OS を選択するオプションのダイアログ。](media/select-linux-docker-support.png)

<span data-ttu-id="10fd5-137">**図 4-39**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-137">**Figure 4-39**.</span></span> <span data-ttu-id="10fd5-138">Linux コンテナーを選択します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-138">Selecting Linux containers.</span></span>

<span data-ttu-id="10fd5-139">簡単な手順では、ASP.NET Core 2.1 アプリケーションを Linux コンテナーで実行されているがあります。</span><span class="sxs-lookup"><span data-stu-id="10fd5-139">With these simple steps, you will have your ASP.NET Core 2.1 application running on a Linux container.</span></span>

<span data-ttu-id="10fd5-140">ご覧のように、Visual Studio 2017 と Docker の統合は完全に達成するため、開発者の生産性です。</span><span class="sxs-lookup"><span data-stu-id="10fd5-140">As you can see, the integration between Visual Studio 2017 and Docker is totally oriented to the developer’s productivity.</span></span>

<span data-ttu-id="10fd5-141">キーを押してこれ**F5**をビルドして、アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-141">Now you can press **F5** to build and run your application.</span></span>

<span data-ttu-id="10fd5-142">使用してイメージを一覧表示、プロジェクトを実行した後、`docker images`コマンド。</span><span class="sxs-lookup"><span data-stu-id="10fd5-142">After running the project, you can list the images using the `docker images` command.</span></span> <span data-ttu-id="10fd5-143">表示する必要があります、`mssampleapplication`プロジェクトを Visual Studio 2017 での自動デプロイで作成されたイメージ。</span><span class="sxs-lookup"><span data-stu-id="10fd5-143">You should see the `mssampleapplication` image created with the automatic deploy of our project with Visual Studio 2017.</span></span>

```console
docker images
```

![Docker images コマンドをからの出力をコンソールには、一覧が表示されます。リポジトリ、タグ、イメージ ID、作成済み (日)、およびサイズ。](media/docker-images-command.png)

<span data-ttu-id="10fd5-145">**図 4-40**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-145">**Figure 4-40**.</span></span> <span data-ttu-id="10fd5-146">Docker イメージの表示</span><span class="sxs-lookup"><span data-stu-id="10fd5-146">View of Docker images</span></span>

## <a name="register-the-solution-in-the-azure-container-registry"></a><span data-ttu-id="10fd5-147">Azure Container registry のソリューションを登録します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-147">Register the Solution in the Azure Container Registry</span></span>

<span data-ttu-id="10fd5-148">このような任意の Docker レジストリにイメージをアップロード[Azure Container Registry (ACR)](https://azure.microsoft.com/services/container-registry/)または Docker Hub イメージは、そのレジストリから AKS クラスターにデプロイできるようにします。</span><span class="sxs-lookup"><span data-stu-id="10fd5-148">Upload the image to any Docker registry, like [Azure Container Registry (ACR)](https://azure.microsoft.com/services/container-registry/) or Docker Hub so the images can be deployed to the AKS cluster from that registry.</span></span> <span data-ttu-id="10fd5-149">ここでは、Azure Container Registry にイメージをアップロードしています。</span><span class="sxs-lookup"><span data-stu-id="10fd5-149">In this case, we’re uploading the image to Azure Container Registry.</span></span>

### <a name="create-the-image-in-release-mode"></a><span data-ttu-id="10fd5-150">リリース モードでイメージを作成します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-150">Create the image in Release mode</span></span>

<span data-ttu-id="10fd5-151">内のイメージを作成する**リリース**次に示すようにリリース モード (実稼働の準備) を変更して、アプリケーションを再実行して F5 キーを押します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-151">Create the image in **Release** Mode (ready for production) changing to Release as shown here and press F5 to run the application again.</span></span>

![VS でオプションをリリース モードでビルドするツールバーです。](media/select-release-mode.png)

<span data-ttu-id="10fd5-153">**図 4-41**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-153">**Figure 4-41**.</span></span> <span data-ttu-id="10fd5-154">リリース モードを選択します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-154">Selecting Release Mode</span></span>

<span data-ttu-id="10fd5-155">実行する場合、`docker image`コマンドを作成した両方のイメージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="10fd5-155">If you execute the `docker image` command, you'll see both images created.</span></span> <span data-ttu-id="10fd5-156">1 つずつ`debug`およびその他の`release`モード。</span><span class="sxs-lookup"><span data-stu-id="10fd5-156">One for `debug` and the other for `release` mode.</span></span>

### <a name="create-a-new-tag-for-the-image"></a><span data-ttu-id="10fd5-157">イメージの新しいタグを作成します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-157">Create a new Tag for the Image</span></span>

<span data-ttu-id="10fd5-158">各コンテナー イメージをタグが付けられる必要があります、`loginServer`レジストリの名前。</span><span class="sxs-lookup"><span data-stu-id="10fd5-158">Each container image needs to be tagged with the `loginServer` name of the registry.</span></span> <span data-ttu-id="10fd5-159">このタグは、ルーティング、イメージ レジストリにコンテナー イメージをプッシュするときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="10fd5-159">This tag is used for routing when pushing container images to an image registry.</span></span>

<span data-ttu-id="10fd5-160">表示することができます、 `loginServer` Azure Container Registry からの情報を受け取り、Azure portal から名前</span><span class="sxs-lookup"><span data-stu-id="10fd5-160">You can view the `loginServer` name from the Azure portal, taking the information from the Azure Container Registry</span></span>

![右上の Azure コンテナー レジストリ名のブラウザー ビュー。](media/loginServer-name.png)

<span data-ttu-id="10fd5-162">**図 4-42**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-162">**Figure 4-42**.</span></span> <span data-ttu-id="10fd5-163">レジストリの名前のビュー</span><span class="sxs-lookup"><span data-stu-id="10fd5-163">View of the name of the Registry</span></span>

<span data-ttu-id="10fd5-164">または、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-164">Or by running the following command:</span></span>

```console
az acr list --resource-group MSSampleResourceGroup --query "[].{acrLoginServer:loginServer}" --output table
```

![上記のコマンドから出力コンソール。](media/az-cli-loginServer-name.png)

<span data-ttu-id="10fd5-166">**図 4-43**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-166">**Figure 4-43**.</span></span> <span data-ttu-id="10fd5-167">PowerShell を使用して、レジストリの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-167">Get the name of the registry using PowerShell</span></span>

<span data-ttu-id="10fd5-168">どちらの場合は、名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-168">In both cases, you'll obtain the name.</span></span> <span data-ttu-id="10fd5-169">この例では`mssampleacr.azurecr.io`します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-169">In our example, `mssampleacr.azurecr.io`.</span></span>

<span data-ttu-id="10fd5-170">ようになりました、イメージをタグを次のコマンドを使用して、最新のイメージ (イメージのリリース) を取得します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-170">Now you can tag the image, taking the latest image (Release image), with the following command:</span></span>

```console
docker tag mssampleaksapplication:latest mssampleacr.azurecr.io/mssampleaksapplication:v1
```

<span data-ttu-id="10fd5-171">実行後、`docker tag`コマンドでのイメージを一覧表示、`docker images`コマンド。</span><span class="sxs-lookup"><span data-stu-id="10fd5-171">After running the `docker tag` command, list the images with the `docker images` command.</span></span> <span data-ttu-id="10fd5-172">新しいタグを持つイメージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="10fd5-172">You should see the image with the new tag.</span></span>

![Docker イメージのコマンドからの出力をコンソール。](media/tagged-docker-images-list.png)

<span data-ttu-id="10fd5-174">**図 4-44**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-174">**Figure 4-44**.</span></span> <span data-ttu-id="10fd5-175">タグが付けられたイメージの表示</span><span class="sxs-lookup"><span data-stu-id="10fd5-175">View of tagged images</span></span>

### <a name="push-the-image-into-the-azure-acr"></a><span data-ttu-id="10fd5-176">Azure の ACR にイメージをプッシュします。</span><span class="sxs-lookup"><span data-stu-id="10fd5-176">Push the image into the Azure ACR</span></span>

<span data-ttu-id="10fd5-177">次のコマンドを使用して、Azure の ACR にイメージをプッシュします。</span><span class="sxs-lookup"><span data-stu-id="10fd5-177">Push the image into the Azure ACR, using the following command:</span></span>

```console
docker push mssampleacr.azurecr.io/mssampleaksapplication:v1
```

<span data-ttu-id="10fd5-178">このコマンドがかかるイメージのアップロード プロセスでフィードバックが用意されています。</span><span class="sxs-lookup"><span data-stu-id="10fd5-178">This command takes a while uploading the images but gives you feedback in the process.</span></span>

![Docker push コマンドからの出力をコンソール: 各レイヤーの文字ベースの進行状況バーが表示されます。](media/uploading-image-to-acr.png)

<span data-ttu-id="10fd5-180">**図 4-45**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-180">**Figure 4-45**.</span></span> <span data-ttu-id="10fd5-181">ACR にイメージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="10fd5-181">Uploading the image to the ACR</span></span>

<span data-ttu-id="10fd5-182">後述する結果が完了すると、プロセスを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10fd5-182">You can see below the result you should get when the process completes:</span></span>

![完了したら、すべてのレイヤーまたはノードを示す docker push コマンドから出力コンソール。](media/uploading-docker-images-complete.png)

<span data-ttu-id="10fd5-184">**図 4-46**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-184">**Figure 4-46**.</span></span> <span data-ttu-id="10fd5-185">ノードのビュー</span><span class="sxs-lookup"><span data-stu-id="10fd5-185">View of nodes</span></span>

<span data-ttu-id="10fd5-186">次の手順では、AKS の Kubernetes クラスターにコンテナーをデプロイします。</span><span class="sxs-lookup"><span data-stu-id="10fd5-186">The next step is to deploy your container into your AKS Kubernetes cluster.</span></span> <span data-ttu-id="10fd5-187">そのためには、ファイルが必要です。 (**.yml ファイルをデプロイする**)、この場合、含まれています。</span><span class="sxs-lookup"><span data-stu-id="10fd5-187">For that you need a file (**.yml deploy file**) that, in this case, contains:</span></span>

```yml
apiVersion: apps/v1beta1
kind: Deployment
metadata:
  name: mssamplesbook
spec:
  replicas: 1
  template:
    metadata:
      labels:
        app: mssample-kub-app
    spec:
      containers:
        - mane: mssample-services-app
          image: mssampleacr.azurecr.io/mssampleaksapplication:v1
          ports:
            - containerPort: 80
---
apiVersion: v1
kind: Service
metadata:
    name: mssample-kub-app
spec:
  ports:
    - name: http-port
      port: 80
      targetPort: 80
  selector:
    app: mssample-kub-app
  type: LoadBalancer
```

> [!NOTE]
> <span data-ttu-id="10fd5-188">Kubernetes を使用した展開の詳細については、次を参照してください。 <https://kubernetes.io/docs/reference/kubectl/cheatsheet/></span><span class="sxs-lookup"><span data-stu-id="10fd5-188">For more information on deployment with Kubernetes see: <https://kubernetes.io/docs/reference/kubectl/cheatsheet/></span></span>

<span data-ttu-id="10fd5-189">これで、使用してデプロイする準備はほとんど**Kubectl**、まず、このコマンドを使用して AKS クラスターに資格情報を取得する必要がありますが。</span><span class="sxs-lookup"><span data-stu-id="10fd5-189">Now you're almost ready to deploy using **Kubectl**, but first you must get the credentials to the AKS Cluster with this command:</span></span>

```console
az aks get-credentials --resource-group MSSampleResourceGroupAKS --name mssampleclusterk801
```

![上記のコマンドから出力コンソール:現在のコンテキストで/root/.kube/config としてマージ"MSSampleK8Cluster](media/getting-aks-credentials.png)

<span data-ttu-id="10fd5-191">**図 4-47**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-191">**Figure 4-47**.</span></span> <span data-ttu-id="10fd5-192">資格情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-192">getting credentials</span></span>

<span data-ttu-id="10fd5-193">次に、使用、`kubectl create`展開を起動するコマンド。</span><span class="sxs-lookup"><span data-stu-id="10fd5-193">Then, use the `kubectl create` command to launch the deployment.</span></span>

```console
kubectl create -f mssample-deploy.yml
```

![上記のコマンドからの出力をコンソール: 展開"mssamplesbook"を作成します。](media/kubectl-create-command.png)

<span data-ttu-id="10fd5-196">**図 4-48**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-196">**Figure 4-48**.</span></span> <span data-ttu-id="10fd5-197">Kubernetes へのデプロイします。</span><span class="sxs-lookup"><span data-stu-id="10fd5-197">Deploy to Kubernetes</span></span>

<span data-ttu-id="10fd5-198">デプロイが完了したら、次のコマンドで一時的にアクセスできるローカル プロキシを使用した Kubernetes コンソールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="10fd5-198">When the deployment completes, you can access the Kubernetes console with a local proxy that you can temporally access with this command:</span></span>

```console
az aks browse --resource-group MSSampleResourceGroupAKS --name mssampleclusterk801
```

<span data-ttu-id="10fd5-199">Url にアクセスして`http://127.0.0.1:8001`します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-199">And accessing the url `http://127.0.0.1:8001`.</span></span>

![展開、ポッド、レプリカ セット、およびサービスを表示、Kubernetes ダッシュ ボードのブラウザー ビュー。](media/kubernetes-cluster-information.png)

<span data-ttu-id="10fd5-201">**図 4 ~ 49**します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-201">**Figure 4-49**.</span></span> <span data-ttu-id="10fd5-202">Kubernetes クラスターの情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="10fd5-202">View Kubernetes cluster information</span></span>

<span data-ttu-id="10fd5-203">Linux コンテナーと AKS の Kubernetes クラスターを使用して Azure にデプロイされたアプリケーションをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="10fd5-203">Now you have your application deployed on Azure, using a Linux Container, and an AKS Kubernetes Cluster.</span></span> <span data-ttu-id="10fd5-204">Azure portal から取得できるサービスのパブリック IP を参照するアプリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="10fd5-204">You can access your app browsing to the public IP of your service, which you can get from the Azure portal.</span></span>

> [!NOTE]
> <span data-ttu-id="10fd5-205">セクションでこのサンプルの AKS クラスターを作成する方法を確認できます[ **Deploy Azure Kubernetes Service (AKS) を**](deploy-azure-kubernetes-service.md)このガイドにします。</span><span class="sxs-lookup"><span data-stu-id="10fd5-205">You can see how to create the AKS Cluster for this sample in section [**Deploy to Azure Kubernetes Service (AKS)**](deploy-azure-kubernetes-service.md) on this guide.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="10fd5-206">[前へ](set-up-windows-containers-with-powershell.md)
>[次へ](../docker-devops-workflow/index.md)</span><span class="sxs-lookup"><span data-stu-id="10fd5-206">[Previous](set-up-windows-containers-with-powershell.md)
[Next](../docker-devops-workflow/index.md)</span></span>
