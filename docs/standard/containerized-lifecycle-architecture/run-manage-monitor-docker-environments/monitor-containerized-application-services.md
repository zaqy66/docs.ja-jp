---
title: コンテナー化されたアプリケーションのサービスを監視します。
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 4bdc4470624ce6e905ab858a2bd8b607c8d3d646
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2018
ms.locfileid: "45619124"
---
# <a name="monitor-containerized-application-services"></a>コンテナー化されたアプリケーションのサービスを監視します。

アプリケーションが複数のコンテナーとマイクロ サービスに分割に監視し、アプリケーションの動作を分析する方法を実装するが重要です。

## <a name="microsoft-application-insights"></a>Microsoft Application Insights

[Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview)はライブ アプリケーションを監視する拡張可能な分析サービスです。 検出してパフォーマンスの問題を診断し、で何が実際に実行、アプリを理解することができます。 継続的にパフォーマンスを向上させるに役立つインテントと、サービスまたはアプリケーションの使いやすさの開発者に設計されています。 Application Insights は、さまざまなプラットフォームなど、.NET、Java、Node.js とその他の多くのプラットフォームは、オンプレミスでホストされているのかクラウド内でアプリを web/サービスとスタンドアロンの両方で動作します。

### <a name="analyzing-docker-apps-in-qa-environments-using-application-insights"></a>Application Insights を使用して、QA 環境での Docker アプリの分析

Docker に関連して、ライフ サイクル イベントと Application Insights 上の Docker コンテナーからパフォーマンス カウンターをグラフにできます。 だけを実行する必要があります、 [Application Insights の Docker イメージ](https://hub.docker.com/r/microsoft/applicationinsights/)ように、ホストし、コンテナーは他の Docker イメージの場合と同様のホストのパフォーマンス カウンターを表示します。 この Application Insights の Docker イメージ (図 6-1) のパフォーマンスとの Docker ホスト (つまり、Linux Vm)、Docker コンテナーを実行しているアプリケーションのアクティビティに関するテレメトリを収集することで、コンテナー化アプリケーションを監視することに役立ちます内にします。

![例](./media/image1.png)

図 6-1: Application Insights の Docker ホストとコンテナーの監視

実行すると、 [Application Insights の Docker イメージ](https://hub.docker.com/r/microsoft/applicationinsights/)次のメリットの Docker ホストで。

-   ライフ サイクル ホストで実行されているすべてのコンテナーに関する製品利用統計情報: 開始、停止、および具合です。

-   すべてのコンテナーのパフォーマンス カウンター: CPU、メモリ、ネットワーク使用率などです。

-   インストールされている場合[Application Insights SDK](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net)コンテナーで実行されているアプリでこれらのアプリのすべてのテレメトリがコンテナーとホスト マシンを識別する追加のプロパティが。 そのため、たとえば、1 つ以上のホストで実行されているアプリのインスタンスがあれば、簡単にことができますをホストして、アプリのテレメトリをフィルター処理します。

### <a name="setting-up-application-insights-to-monitor-docker-applications-and-docker-hosts"></a>アプリケーションの Docker および Docker ホストを監視するための Application Insights の設定

Application Insights リソースを作成するには、次の一覧に記事の指示に従います。 Azure Portal を必要なスクリプトを作成します。

-   **Application Insights で Docker アプリケーションを監視します。**  [https://docs.microsoft.com/azure/application-insights/app-insights-docker](https://docs.microsoft.com/azure/application-insights/app-insights-docker)

-   **Docker Hub や Github にある application Insights の Docker イメージ:**  
[https://hub.docker.com/r/microsoft/applicationinsights/](https://hub.docker.com/r/microsoft/applicationinsights/) そして <https://github.com/Microsoft/ApplicationInsights-Docker>

-   **ASP.NET 用の Application Insights を設定します。**  
[https://docs.microsoft.com/azure/application-insights/app-insights-asp-net](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net)

-   **Web ページ用の application Insights:**  
<https://docs.microsoft.com/azure/application-insights/app-insights-javascript>

## <a name="microsoft-operations-management-suite"></a>Microsoft Operations Management Suite

[Operations Management Suite](https://microsoft.com/oms)は log analytics、automation、backup、およびサイトの回復を提供する簡素化された IT 管理ソリューションです。 基づく[クエリ](https://blogs.technet.microsoft.com/msoms/2016/01/21/easy-microsoft-operations-management-suite-search-queries/)Operations Management suite で上げることができます[アラート](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-monitoring-alerts)経由で修復の設定と[Azure Automation](https://docs.microsoft.com/azure/automation/)します。 1 つのウィンドウでガラスのビューを提供する、既存の管理ソリューションともシームレスに統合します。 Operations Management Suite では、オンプレミスの保護やクラウドのインフラストラクチャを管理することができます。

### <a name="operations-management-suitehttpsmicrosoftcomoms-container-solution-for-docker"></a>[Operations Management Suite](https://microsoft.com/oms) Docker のコンテナー ソリューション

Operations Management Suite のコンテナー ソリューションで管理し、場所、コンテナーとコンテナー ホストである、に関する情報を表示することによって Docker ホストとコンテナーを監視するだけでなく、独自の有益なサービスを提供すること、コンテナーを実行しています。失敗した場合、または、Docker デーモンとコンテナーでのログに送信される*stdout*と*stderr*。 また、CPU、メモリ、ネットワーク、コンテナーとホストのストレージなどのパフォーマンス メトリックを表示し、トラブルシューティングやノイズの多い近隣のコンテナーの検出に役立てることもできます。

![](./media/image2.png)

図 6-2: Operations Management Suite で示すように Docker コンテナーについて

アクティビティの監視に重点を application Insights と Operations Management Suiteただし、Application Insights は、アプリ内で実行されているその SDK に協力してくれた、アプリ自体の監視についてより説明します。 ただし、Operations Management Suite について重点的により、ホストのインフラストラクチャ、さらにデータ ドリブンの非常に柔軟性の検索/クエリ システムを提供しながらログの詳細に分析を提供しています。

Operations Management Suite はクラウド ベース サービスとして実装されている、ためにことができますが稼働してすばやくインフラストラクチャ サービスに最小限の投資で。 新機能では、保存する継続的なメンテナンスに、自動的に配信され、アップグレードのコスト。

Operations Management Suite のコンテナー ソリューションでは、次の操作を行うことができます。

-   集中管理し、何百万もの規模での Docker コンテナーからログを関連付ける

-   1 つの場所ですべてのコンテナー ホストに関する情報を参照してください。

-   どのコンテナーが実行されている、および実行しているどのようなイメージを実行します。

-   コンテナー ホスト上の問題を引き起こす可能性のある「迷惑な隣人」コンテナーをすばやく診断します。

-   コンテナーの操作の監査証跡を参照してください。

-   表示および Docker ホストへのリモート処理せず、一元化されたログを検索してトラブルシューティングを行う

-   「うるさい隣人」と、ホスト上の余分なリソースを消費する可能性がありますコンテナーを検索します。

-   一元的な CPU、メモリ、ストレージ、およびコンテナーのネットワークの使用状況とパフォーマンス情報を表示します。

-   生成テスト Azure Automation での Docker コンテナー

型のようなクエリを実行しているパフォーマンス情報を表示する図 6-3 に示すように、パフォーマンスを = です。

![DockerPerfMetricsView](./media/image3.png){width="5.78625in" height="3.25in"}

Operations Management Suite で示すように Docker ホストのパフォーマンス メトリックを図 6-3:

Operations Management Suite での標準的な機能もとに役立つクエリを保存する際に役立つし、システム内の傾向を検出するクエリを保持します。

**詳細については** でコンテナー ソリューションをインストールして、Docker の構成に関する情報を検索する[Operations Management Suite](https://microsoft.com/oms)に移動して、<https://docs.microsoft.com/azure/log-analytics/log-analytics-containers>します。

>[!div class="step-by-step"]
[前へ](manage-production-docker-environments.md)
[次へ](../key-takeaways/index.md)
