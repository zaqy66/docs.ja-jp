---
title: コンテナー化されたアプリケーションのサービスを監視します。
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 4bdc4470624ce6e905ab858a2bd8b607c8d3d646
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44064330"
---
# <a name="monitor-containerized-application-services"></a><span data-ttu-id="128db-103">コンテナー化されたアプリケーションのサービスを監視します。</span><span class="sxs-lookup"><span data-stu-id="128db-103">Monitor containerized application services</span></span>

<span data-ttu-id="128db-104">アプリケーションが複数のコンテナーとマイクロ サービスに分割に監視し、アプリケーションの動作を分析する方法を実装するが重要です。</span><span class="sxs-lookup"><span data-stu-id="128db-104">It is critical for applications split into multiple containers and microservices to have a way to monitor and analyze the behavior of the application.</span></span>

## <a name="microsoft-application-insights"></a><span data-ttu-id="128db-105">Microsoft Application Insights</span><span class="sxs-lookup"><span data-stu-id="128db-105">Microsoft Application Insights</span></span>

<span data-ttu-id="128db-106">[Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview)はライブ アプリケーションを監視する拡張可能な分析サービスです。</span><span class="sxs-lookup"><span data-stu-id="128db-106">[Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview) is an extensible analytics service that monitors your live application.</span></span> <span data-ttu-id="128db-107">検出してパフォーマンスの問題を診断し、で何が実際に実行、アプリを理解することができます。</span><span class="sxs-lookup"><span data-stu-id="128db-107">It helps you to detect and diagnose performance issues and to understand what users actually do with your app.</span></span> <span data-ttu-id="128db-108">継続的にパフォーマンスを向上させるに役立つインテントと、サービスまたはアプリケーションの使いやすさの開発者に設計されています。</span><span class="sxs-lookup"><span data-stu-id="128db-108">It's designed for developers, with the intent of helping you to continuously improve the performance and usability of your services or applications.</span></span> <span data-ttu-id="128db-109">Application Insights は、さまざまなプラットフォームなど、.NET、Java、Node.js とその他の多くのプラットフォームは、オンプレミスでホストされているのかクラウド内でアプリを web/サービスとスタンドアロンの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="128db-109">Application Insights works with both web/services and standalone apps on a wide variety of platforms like .NET, Java, Node.js and many other platforms, hosted on-premises or in the cloud.</span></span>

### <a name="analyzing-docker-apps-in-qa-environments-using-application-insights"></a><span data-ttu-id="128db-110">Application Insights を使用して、QA 環境での Docker アプリの分析</span><span class="sxs-lookup"><span data-stu-id="128db-110">Analyzing Docker apps in QA environments using Application Insights</span></span>

<span data-ttu-id="128db-111">Docker に関連して、ライフ サイクル イベントと Application Insights 上の Docker コンテナーからパフォーマンス カウンターをグラフにできます。</span><span class="sxs-lookup"><span data-stu-id="128db-111">As it pertains to Docker, you can chart life-cycle events and performance counters from Docker containers on Application Insights.</span></span> <span data-ttu-id="128db-112">だけを実行する必要があります、 [Application Insights の Docker イメージ](https://hub.docker.com/r/microsoft/applicationinsights/)ように、ホストし、コンテナーは他の Docker イメージの場合と同様のホストのパフォーマンス カウンターを表示します。</span><span class="sxs-lookup"><span data-stu-id="128db-112">You just need to run the [Application Insights Docker image](https://hub.docker.com/r/microsoft/applicationinsights/) as a container in your host, and it will display performance counters for the host as well as for the other Docker images.</span></span> <span data-ttu-id="128db-113">この Application Insights の Docker イメージ (図 6-1) のパフォーマンスとの Docker ホスト (つまり、Linux Vm)、Docker コンテナーを実行しているアプリケーションのアクティビティに関するテレメトリを収集することで、コンテナー化アプリケーションを監視することに役立ちます内にします。</span><span class="sxs-lookup"><span data-stu-id="128db-113">This Application Insights Docker image (Figure 6-1) helps you to monitor your containerized applications by collecting telemetry about the performance and activity of your Docker host (that is, your Linux VMs), Docker containers and the applications running within them.</span></span>

![例](./media/image1.png)

<span data-ttu-id="128db-115">図 6-1: Application Insights の Docker ホストとコンテナーの監視</span><span class="sxs-lookup"><span data-stu-id="128db-115">Figure 6-1: Application Insights monitoring Docker hosts and containers</span></span>

<span data-ttu-id="128db-116">実行すると、 [Application Insights の Docker イメージ](https://hub.docker.com/r/microsoft/applicationinsights/)次のメリットの Docker ホストで。</span><span class="sxs-lookup"><span data-stu-id="128db-116">When you run the [Application Insights Docker image](https://hub.docker.com/r/microsoft/applicationinsights/) on your Docker host, you benefit from the following:</span></span>

-   <span data-ttu-id="128db-117">ライフ サイクル ホストで実行されているすべてのコンテナーに関する製品利用統計情報: 開始、停止、および具合です。</span><span class="sxs-lookup"><span data-stu-id="128db-117">Life-cycle telemetry about all the containers running on the host—start, stop, and so on.</span></span>

-   <span data-ttu-id="128db-118">すべてのコンテナーのパフォーマンス カウンター: CPU、メモリ、ネットワーク使用率などです。</span><span class="sxs-lookup"><span data-stu-id="128db-118">Performance counters for all the containers: CPU, memory, network usage, and more.</span></span>

-   <span data-ttu-id="128db-119">インストールされている場合[Application Insights SDK](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net)コンテナーで実行されているアプリでこれらのアプリのすべてのテレメトリがコンテナーとホスト マシンを識別する追加のプロパティが。</span><span class="sxs-lookup"><span data-stu-id="128db-119">If you also installed [Application Insights SDK](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net) in the apps running in the containers, all the telemetry of those apps will have additional properties identifying the container and host machine.</span></span> <span data-ttu-id="128db-120">そのため、たとえば、1 つ以上のホストで実行されているアプリのインスタンスがあれば、簡単にことができますをホストして、アプリのテレメトリをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="128db-120">So, for example, if you have instances of an app running in more than one host, you'll easily be able to filter your app telemetry by host.</span></span>

### <a name="setting-up-application-insights-to-monitor-docker-applications-and-docker-hosts"></a><span data-ttu-id="128db-121">アプリケーションの Docker および Docker ホストを監視するための Application Insights の設定</span><span class="sxs-lookup"><span data-stu-id="128db-121">Setting up Application Insights to monitor Docker applications and Docker hosts</span></span>

<span data-ttu-id="128db-122">Application Insights リソースを作成するには、次の一覧に記事の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="128db-122">To create an Application Insights resource, follow the instructions in the articles presented in the list that follows.</span></span> <span data-ttu-id="128db-123">Azure Portal を必要なスクリプトを作成します。</span><span class="sxs-lookup"><span data-stu-id="128db-123">Azure Portal will create the necessary script for you.</span></span>

-   <span data-ttu-id="128db-124">**Application Insights で Docker アプリケーションを監視します。**  [https://docs.microsoft.com/azure/application-insights/app-insights-docker](https://docs.microsoft.com/azure/application-insights/app-insights-docker)</span><span class="sxs-lookup"><span data-stu-id="128db-124">**Monitor Docker applications in Application Insights:**  [https://docs.microsoft.com/azure/application-insights/app-insights-docker](https://docs.microsoft.com/azure/application-insights/app-insights-docker)</span></span>

-   <span data-ttu-id="128db-125">**Docker Hub や Github にある application Insights の Docker イメージ:**</span><span class="sxs-lookup"><span data-stu-id="128db-125">**Application Insights Docker image at Docker Hub and Github:**</span></span>  
<span data-ttu-id="128db-126">[https://hub.docker.com/r/microsoft/applicationinsights/](https://hub.docker.com/r/microsoft/applicationinsights/) そして <https://github.com/Microsoft/ApplicationInsights-Docker></span><span class="sxs-lookup"><span data-stu-id="128db-126">[https://hub.docker.com/r/microsoft/applicationinsights/](https://hub.docker.com/r/microsoft/applicationinsights/) and <https://github.com/Microsoft/ApplicationInsights-Docker></span></span>

-   <span data-ttu-id="128db-127">**ASP.NET 用の Application Insights を設定します。**</span><span class="sxs-lookup"><span data-stu-id="128db-127">**Set up Application Insights for ASP.NET:**</span></span>  
[https://docs.microsoft.com/azure/application-insights/app-insights-asp-net](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net)

-   <span data-ttu-id="128db-128">**Web ページ用の application Insights:**</span><span class="sxs-lookup"><span data-stu-id="128db-128">**Application Insights for web pages:**</span></span>  
<https://docs.microsoft.com/azure/application-insights/app-insights-javascript>

## <a name="microsoft-operations-management-suite"></a><span data-ttu-id="128db-129">Microsoft Operations Management Suite</span><span class="sxs-lookup"><span data-stu-id="128db-129">Microsoft Operations Management Suite</span></span>

<span data-ttu-id="128db-130">[Operations Management Suite](https://microsoft.com/oms)は log analytics、automation、backup、およびサイトの回復を提供する簡素化された IT 管理ソリューションです。</span><span class="sxs-lookup"><span data-stu-id="128db-130">[Operations Management Suite](https://microsoft.com/oms) is a simplified IT management solution that provides log analytics, automation, backup, and site recovery.</span></span> <span data-ttu-id="128db-131">基づく[クエリ](https://blogs.technet.microsoft.com/msoms/2016/01/21/easy-microsoft-operations-management-suite-search-queries/)Operations Management suite で上げることができます[アラート](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-monitoring-alerts)経由で修復の設定と[Azure Automation](https://docs.microsoft.com/azure/automation/)します。</span><span class="sxs-lookup"><span data-stu-id="128db-131">Based on [queries](https://blogs.technet.microsoft.com/msoms/2016/01/21/easy-microsoft-operations-management-suite-search-queries/) in Operations Management Suite, you can raise [alerts](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-monitoring-alerts) and set remediation via [Azure Automation](https://docs.microsoft.com/azure/automation/).</span></span> <span data-ttu-id="128db-132">1 つのウィンドウでガラスのビューを提供する、既存の管理ソリューションともシームレスに統合します。</span><span class="sxs-lookup"><span data-stu-id="128db-132">It also seamlessly integrates with your existing management solutions to provide a single pane-of-glass view.</span></span> <span data-ttu-id="128db-133">Operations Management Suite では、オンプレミスの保護やクラウドのインフラストラクチャを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="128db-133">Operations Management Suite helps you to manage and protect your on-premises and cloud infrastructure.</span></span>

### <a name="operations-management-suitehttpsmicrosoftcomoms-container-solution-for-docker"></a><span data-ttu-id="128db-134">[Operations Management Suite](https://microsoft.com/oms) Docker のコンテナー ソリューション</span><span class="sxs-lookup"><span data-stu-id="128db-134">[Operations Management Suite](https://microsoft.com/oms) Container Solution for Docker</span></span>

<span data-ttu-id="128db-135">Operations Management Suite のコンテナー ソリューションで管理し、場所、コンテナーとコンテナー ホストである、に関する情報を表示することによって Docker ホストとコンテナーを監視するだけでなく、独自の有益なサービスを提供すること、コンテナーを実行しています。失敗した場合、または、Docker デーモンとコンテナーでのログに送信される*stdout*と*stderr*。</span><span class="sxs-lookup"><span data-stu-id="128db-135">In addition to providing valuable services on its own, the Operations Management Suite Container Solution can manage and monitor Docker hosts and containers by showing information about where your containers and container hosts are, which containers are running or failed, and Docker daemon and container logs sent to *stdout* and *stderr*.</span></span> <span data-ttu-id="128db-136">また、CPU、メモリ、ネットワーク、コンテナーとホストのストレージなどのパフォーマンス メトリックを表示し、トラブルシューティングやノイズの多い近隣のコンテナーの検出に役立てることもできます。</span><span class="sxs-lookup"><span data-stu-id="128db-136">It also shows performance metrics such as CPU, memory, network, and storage for the container and hosts to help you troubleshoot and find noisy neighbor containers.</span></span>

![](./media/image2.png)

<span data-ttu-id="128db-137">図 6-2: Operations Management Suite で示すように Docker コンテナーについて</span><span class="sxs-lookup"><span data-stu-id="128db-137">Figure 6-2: Information about Docker containers shown by Operations Management Suite</span></span>

<span data-ttu-id="128db-138">アクティビティの監視に重点を application Insights と Operations Management Suiteただし、Application Insights は、アプリ内で実行されているその SDK に協力してくれた、アプリ自体の監視についてより説明します。</span><span class="sxs-lookup"><span data-stu-id="128db-138">Application Insights and Operations Management Suite both focus on monitoring activities; however, Application Insights focuses more on monitoring the apps themselves thanks to its SDK running within the app.</span></span> <span data-ttu-id="128db-139">ただし、Operations Management Suite について重点的により、ホストのインフラストラクチャ、さらにデータ ドリブンの非常に柔軟性の検索/クエリ システムを提供しながらログの詳細に分析を提供しています。</span><span class="sxs-lookup"><span data-stu-id="128db-139">However, Operations Management Suite focuses much more on the infrastructure around the hosts, plus it offers deep analysis on logs at scale while providing a very flexible data-driven search/query system.</span></span>

<span data-ttu-id="128db-140">Operations Management Suite はクラウド ベース サービスとして実装されている、ためにことができますが稼働してすばやくインフラストラクチャ サービスに最小限の投資で。</span><span class="sxs-lookup"><span data-stu-id="128db-140">Because Operations Management Suite is implemented as a cloud-based service, you can have it up and running quickly with minimal investment in infrastructure services.</span></span> <span data-ttu-id="128db-141">新機能では、保存する継続的なメンテナンスに、自動的に配信され、アップグレードのコスト。</span><span class="sxs-lookup"><span data-stu-id="128db-141">New features are delivered automatically, saving you from ongoing maintenance and upgrade costs.</span></span>

<span data-ttu-id="128db-142">Operations Management Suite のコンテナー ソリューションでは、次の操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="128db-142">Using Operations Management Suite Container Solution, you can do the following:</span></span>

-   <span data-ttu-id="128db-143">集中管理し、何百万もの規模での Docker コンテナーからログを関連付ける</span><span class="sxs-lookup"><span data-stu-id="128db-143">Centralize and correlate millions of logs from Docker containers at scale</span></span>

-   <span data-ttu-id="128db-144">1 つの場所ですべてのコンテナー ホストに関する情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="128db-144">See information about all container hosts in a single location</span></span>

-   <span data-ttu-id="128db-145">どのコンテナーが実行されている、および実行しているどのようなイメージを実行します。</span><span class="sxs-lookup"><span data-stu-id="128db-145">Know which containers are running, what image they're running, and where they're running</span></span>

-   <span data-ttu-id="128db-146">コンテナー ホスト上の問題を引き起こす可能性のある「迷惑な隣人」コンテナーをすばやく診断します。</span><span class="sxs-lookup"><span data-stu-id="128db-146">Quickly diagnose "noisy neighbor" containers that can cause problems on container hosts</span></span>

-   <span data-ttu-id="128db-147">コンテナーの操作の監査証跡を参照してください。</span><span class="sxs-lookup"><span data-stu-id="128db-147">See an audit trail for actions on containers</span></span>

-   <span data-ttu-id="128db-148">表示および Docker ホストへのリモート処理せず、一元化されたログを検索してトラブルシューティングを行う</span><span class="sxs-lookup"><span data-stu-id="128db-148">Troubleshoot by viewing and searching centralized logs without remoting to the Docker hosts</span></span>

-   <span data-ttu-id="128db-149">「うるさい隣人」と、ホスト上の余分なリソースを消費する可能性がありますコンテナーを検索します。</span><span class="sxs-lookup"><span data-stu-id="128db-149">Find containers that might be "noisy neighbors" and consuming excess resources on a host</span></span>

-   <span data-ttu-id="128db-150">一元的な CPU、メモリ、ストレージ、およびコンテナーのネットワークの使用状況とパフォーマンス情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="128db-150">View centralized CPU, memory, storage, and network usage and performance information for containers</span></span>

-   <span data-ttu-id="128db-151">生成テスト Azure Automation での Docker コンテナー</span><span class="sxs-lookup"><span data-stu-id="128db-151">Generate test Docker containers with Azure Automation</span></span>

<span data-ttu-id="128db-152">型のようなクエリを実行しているパフォーマンス情報を表示する図 6-3 に示すように、パフォーマンスを = です。</span><span class="sxs-lookup"><span data-stu-id="128db-152">You can see performance information by running queries like Type=Perf, as shown in Figure 6-3.</span></span>

![DockerPerfMetricsView](./media/image3.png)<span data-ttu-id="128db-154">{width="5.78625in" height="3.25in"}</span><span class="sxs-lookup"><span data-stu-id="128db-154">{width="5.78625in" height="3.25in"}</span></span>

<span data-ttu-id="128db-155">Operations Management Suite で示すように Docker ホストのパフォーマンス メトリックを図 6-3:</span><span class="sxs-lookup"><span data-stu-id="128db-155">Figure 6-3: Performance metrics of Docker hosts shown by Operations Management Suite</span></span>

<span data-ttu-id="128db-156">Operations Management Suite での標準的な機能もとに役立つクエリを保存する際に役立つし、システム内の傾向を検出するクエリを保持します。</span><span class="sxs-lookup"><span data-stu-id="128db-156">Saving queries is also a standard feature in Operations Management Suite and can help you keep queries you've found useful and discover trends in your system.</span></span>

<span data-ttu-id="128db-157">**詳細については** でコンテナー ソリューションをインストールして、Docker の構成に関する情報を検索する[Operations Management Suite](https://microsoft.com/oms)に移動して、<https://docs.microsoft.com/azure/log-analytics/log-analytics-containers>します。</span><span class="sxs-lookup"><span data-stu-id="128db-157">**More info** To find information on installing and configuring the Docker container solution in [Operations Management Suite](https://microsoft.com/oms), go to <https://docs.microsoft.com/azure/log-analytics/log-analytics-containers>.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="128db-158">[前へ](manage-production-docker-environments.md)
[次へ](../key-takeaways/index.md)</span><span class="sxs-lookup"><span data-stu-id="128db-158">[Previous](manage-production-docker-environments.md)
[Next](../key-takeaways/index.md)</span></span>
