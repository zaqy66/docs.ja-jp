---
title: 高いスケーラビリティと可用性のためにマイクロサービスと複数のコンテナー アプリケーションを調整する
description: 実際の運用アプリケーションでは、デプロイし、正常性、ワークロードおよびすべてのコンテナーのライフ サイクルを処理するオーケストレーターで管理する必要があります。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 749b613ac847c57eb993bff90b36f02a0b39477f
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221161"
---
# <a name="orchestrating-microservices-and-multicontainer-applications-for-high-scalability-and-availability"></a>マイクロ サービスと高いスケーラビリティと可用性のための複数のコンテナー アプリケーションを調整すること

アプリケーションがマイクロサービスに基づく場合や、単に複数のコンテナーに分割されている場合、運用可能なアプリケーションのオーケストレーターを使用することが不可欠です。 前述のとおり、マイクロサービス ベースの方法では、マイクロサービスはそれぞれモデルとデータを所有しているため、開発と展開の観点から自立していることになります。 (SOA) のような複数のサービスで構成される従来のアプリケーションがある場合でもも、複数のコンテナーまたは分散システムとして展開する必要がある 1 つのビジネス アプリケーションを構成するサービス。 このようなシステムは複雑でスケール アウトおよび管理できます。したがって、実稼働可能かつスケーラブルな複数のコンテナー アプリケーションを用意する場合、orchestrator 絶対に必要です。

図 4-6 は、複数のマイクロ サービス (コンテナー) から成るアプリケーションのクラスターへの展開を示しています。

![](./media/image6.png)

図 4-6:コンテナーのクラスター

これは論理的な方法のように見えます。 しかし、どのようにする処理の負荷分散、ルーティング、およびこれらの構成済みのアプリケーションを調整することでしょうか。

Docker コマンド ライン インターフェイス (CLI) には、1 つのホスト上の 1 つのコンテナーの管理のニーズより複雑な分散アプリケーションの複数のホストに展開されている複数のコンテナーを管理する際に短いなります。 ほとんどの場合は、管理プラットフォームは自動的にコンテナーを開始、停止、またはシャット ダウンする必要がおよび理想的も制御ネットワークおよびデータ ストレージなどのリソースにアクセスする方法で必要があります。

個々のコンテナーまたは非常に単純な構成アプリを管理するだけでなく、マイクロサービスを使用してより大きなエンタープライズ アプリケーションを管理するには、オーケストレーションおよびクラスタリング プラットフォームが必要になります。

アーキテクチャと開発の観点から、マイクロ サービス ベースの構築、大規模なエンタープライズは、アプリケーションは次のプラットフォームと高度なシナリオをサポートする製品を理解しておく必要。

-   **クラスターとオーケストレーター** スケールする必要がある場合に、多くの Docker ホストのアプリケーションをなど大規模なマイクロ サービス ベースのアプリケーションにすることが重要で 1 つのクラスターとしてそれらのホストのすべてを管理できます。基になるプラットフォームの複雑さを抽象化します。 コンテナーのクラスターとオーケストレーターの提供内容です。 オーケストレーターには、Docker Swarm、Mesosphere DC/OS、Kubernetes (最初の 3 つ Azure Container Service で使用できる)、および Azure Service Fabric があります。

-   **スケジューラ** *スケジュール*管理者がユーザー インターフェイスも提供するために、クラスター内のコンテナーを起動する機能を搭載することを意味します。 クラスター スケジューラにはいくつかの役割があります。たとえば、クラスターのリソースを効率的に使用すること、ユーザーによって指定される制約を設定すること、ノードまたはホスト全体でのコンテナーの負荷分散を効率的に行うこと、高可用性を提供すると同時にエラーに対して堅牢であることなどです。

クラスターとスケジューラの概念は密接に関連しており、さまざまなベンダーによって提供される製品では、多くの場合、両方の機能セットが提供されます。 表 4-1 には、最も重要なプラットフォームとクラスターとスケジューラーがあるソフトウェアの選択肢が一覧表示します。 これらのクラスターは、Azure などのパブリック クラウドで一般に提供されます。

表 4-1:コンテナーのクラスタリング、オーケストレーション、スケジューリングのためのソフトウェア プラットフォーム

| プラットフォーム | 説明 |
|---|---|
| Docker Swarm<br/> ![Docker Swarm ロゴ](./media/image7.png) | Docker Swarm では、クラスターし、Docker のコンテナーをスケジュールする機能を提供します。 Swarm を使用することで、Docker ホストのプールを単一の仮想 Docker ホストにすることができます。 クライアントは、ホスト、つまり、Swarm を簡単にスケールするアプリケーションを複数のホストを同じ方法で、Swarm を API 要求を行うことができます。 <br /><br /> Docker Swarm は Docker 社の製品です。 <br /><br /> Docker v1.12 以降ではネイティブの組み込み Swarm モードを実行できます。 |
| Mesosphere DC/OS<br/>![Mesosphere DC/OS ロゴ](./media/image8.png) |  Mesosphere Enterprise DC/OS (Apache Mesos に基づく) は、コンテナーと分散アプリケーションを実行するための運用可能なプラットフォームです。 <br /><br /> DC/OS は、クラスターで使用可能なリソースのコレクションを抽象化し、これらのリソースをその上に構築されたコンポーネントで使用できるようにすることで機能します。 Marathon は通常、DC/OS と統合されたスケジューラとして使用されます。 |
| Google Kubernetes<br />![Google の Kubernetes のロゴ](./media/image9.png) | Kubernetes はオープンソースの製品であり、クラスターのインフラストラクチャとコンテナーのスケジューリングからオーケストレーション機能までの機能を提供します。 ホストのクラスターのデプロイ、スケーリング、およびアプリケーション コンテナーの操作を自動化できます。 <br /><br /> Kubernetes ではコンテナー中心のインフラストラクチャが提供され、アプリケーション コンテナーを論理ユニットにグループ化し、管理と検出を容易にします。 |
| Azure Service Fabric<br />![Azure Service Fabric ロゴ](./media/image10.png) | [Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview) は、アプリケーションを構築するための Microsoft マイクロサービス プラットフォームです。 サービスの[オーケストレーター](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-introduction)であり、マシンのクラスターを作成します。 既定では、Service Fabric デプロイし、プロセスとしてのサービスをアクティブ化が Service Fabric が Docker コンテナー イメージ内のサービスをデプロイできます。 重要な同じアプリケーション内のコンテナー内のサービスとプロセスにサービスが混在することができます。 <br /><br /> 2017 年 5 月の時点で、Docker コンテナーとして展開するサービスをサポートする Service Fabric の機能はプレビュー状態です。 <br /><br /> 使用してから、さまざまな方法で Service Fabric サービスを開発することができます、 [Service Fabric プログラミング モデル](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework)デプロイ[ゲスト実行可能ファイル](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-existing-app)コンテナーおよびコンテナー。 Service Fabric などの規範的なアプリケーションのモデルをサポートしている[ステートフル サービス](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction)と[Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction)します。

## <a name="using-container-based-orchestrators-in-azure"></a>Azure でコンテナー ベースのオーケストレーターの使用

いくつかのクラウド ベンダーは、Docker コンテナーのサポートと Docker クラスターおよびオーケストレーション サポート (Azure、Amazon EC2 Container Service、および Google Container Engine を含む) を提供します。 Azure は、次のセクションで説明したように、Docker の Azure Container Service でクラスターとオーケストレーターのサポートを提供します。

別の選択肢では、Azure Service Fabric は、また Linux と Windows コンテナーに基づく Docker のサポートを使用します。 Service Fabric は Azure またはその他のクラウドだけでなく[オンプレミス](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-anywhere)します。

## <a name="using-azure-container-service"></a>Azure Container Service の使用

Docker クラスターは複数の Docker ホストをプールし、単一の Docker ホストとして公開するため、複数のコンテナーをクラスターに展開できます。 クラスターでは、正常性、スケーラビリティなどのすべての複雑な管理機能を処理します。 図 4-7 では、コンテナー サービスに構成されたアプリケーションの Docker クラスターがどのようにマップを表します。

Container Service では、作成、構成、およびコンテナー化されたアプリケーションを実行するあらかじめ構成されている Vm のクラスターの管理を簡略化する方法を提供します。 人気のオープン ソースのスケジューリングおよびオーケストレーション ツールの最適化された構成を使用して、コンテナー サービスにより、既存のスキルを使用して、またはコミュニティの専門知識を展開し、コンテナー ベースの管理の増加し続けるの本文に描画するにはAzure でのアプリケーション。

Container Service では、Azure 専用の一般的な Docker クラスタ リング オープン ソース ツールとテクノロジの構成を最適化します。 コンテナーとアプリケーションの構成の両方に移植性を提供するオープン ソリューションが得られます。 ユーザーはサイズ、ホストの数、オーケストレーター ツールを選択し、Container Service は他のすべてを処理します。

Container Service では、Docker イメージを使用して、アプリケーション コンテナーが完全に移植可能であることを確認します。 これらのアプリケーションが数千または数千のコンテナーの数十台でもまで拡張できることを確認する DC/OS、Kubernetes、Docker Swarm などのオープン ソースのオーケストレーション プラットフォームの選択肢をサポートします。

Azure Container service では、オーケストレーション レイヤーなど、アプリケーションの移植性を維持しながら Azure のエンタープライズ級の機能を活用がかかります。

![](./media/image11.png)

図 4-7:Azure Container Service でのクラスタリングの選択肢

図 4-8 に示すように、コンテナー サービス DC/OS、Kubernetes、または Docker Swarm を展開するために Azure によって提供されるインフラストラクチャだけですが、追加のオーケストレーターを実装していません。 そのため、コンテナー サービスにはできません、orchestrator では、そのためです。コンテナーの既存のオープン ソース オーケストレーターを活用する単なるインフラストラクチャになります。

![](./media/image12.png)

図 4-8:Container Service でのオーケストレーター

使用量の観点からは、コンテナー サービスの目的は、一般的なオープン ソース ツールとテクノロジを使用して、コンテナーのホスティング環境を提供します。 この目的を達成するために、選択されたオーケストレーターの標準的な API エンドポイントが公開されます。 これらのエンドポイントを使用すると、それらのエンドポイントと通信できる任意のソフトウェアを使用することができます。 たとえば、Docker Swarm エンドポイントの場合、Docker CLI を使用すると選択します。 DC/OS では、DC/OS CLI を使用するよう選択できます。

### <a name="getting-started-with-container-service"></a>Container Service の概要

コンテナー サービスを使用するには、Azure Resource Manager テンプレートを使用して、Azure portal からコンテナー サービス クラスターを展開する、または[CLI](https://docs.microsoft.com/cli/azure/install-azure-cli)します。 使用可能なテンプレートには、[Docker Swarm](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-swarm)、[Kubernetes](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-kubernetes)、[DC/OS](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-dcos) があります。 追加または高度な Azure 構成を含めるクイック スタート テンプレートを変更することができます。

**詳細については** 、Azure の web サイトのコンテナー サービス クラスターのデプロイに関する詳細は[Azure Container Service クラスターのデプロイ](https://docs.microsoft.com/azure/container-service/dcos-swarm/container-service-deployment)します。

ACS の一部として既定でインストールされるソフトウェアはいずれも無料です。 既定のすべてのオプションはオープン ソース ソフトウェアと共に実装されます。

Container Service では、Standard A、D、DS、G、および GS シリーズの Linux Vm は Azure で現在使用できます。 その他の記憶域やネットワークなど、使用されたインフラストラクチャの基盤となるリソースと選択したコンピューティング インスタンスに対してのみ課金されます。 料金はかかりません増分 Container Service の自体です。

### <a name="additional-resources"></a>その他の技術情報

追加情報の検索場所の場所を次に示します。

-   Docker コンテナー ホスティング ソリューション Container service の概要:  
    https://docs.microsoft.com/azure/container-service/kubernetes/container-service-intro-kubernetes>

-   Docker Swarm の概要:  
    <https://docs.docker.com/swarm/overview/>

-   Swarm モード概要:  
    <https://docs.docker.com/engine/swarm/>

-   Mesosphere DC/OS 概要:    
    <https://docs.mesosphere.com/1.7/overview/>

-   Kubernetes (公式サイト):  
    <https://kubernetes.io/>

## <a name="using-service-fabric"></a>Service Fabric の使用

サービスの提供に「ボックス」の製品は、通常、モノリシック スタイルの実現を移行する Microsoft の Service Fabric が発生しました。 Service Fabric の構築と Azure SQL Database、Azure Document DB、Azure Service Bus、Cortana のバックエンドなどの規模での大規模なサービスの運用の経験から形成されました。 プラットフォームは時間をかけてより多くのサービスを採用するように進化しました。 重要なのは、Service Fabric は、Azure 内だけでなく、スタンドアロン Windows Server の展開でも実行する必要があることです。

Service Fabric の目的は、構築し、サービスを実行し、チームがマイクロ サービス アプローチを使用してビジネス上の問題を解決するためにインフラストラクチャ リソースを効率的に利用するの困難な問題を解決するためにです。

Service Fabric は、マイクロサービス アプローチを使用するアプリケーションの構築に役立つ 2 つの広範な領域を提供します。

-   展開、拡張、アップグレード、検出のためのシステム サービス、失敗したサービスの再起動、サービスの場所の検出、状態の管理、正常性の監視を提供するプラットフォーム。 これらのシステム サービスを使用して、前に説明したマイクロ サービスの特性の多く有効で提供します。

-   アプリケーションをマイクロサービスとして構築するために役立つプログラミング API またはフレームワーク: [Reliable Actors と Reliable Services](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework)。 もちろん、マイクロサービスを構築するための任意のコードを選択できますが、これらの API によってジョブがさらにわかりやすくなり、より深いレベルでプラットフォームと統合されます。 この方法で正常性情報と診断情報を取得し、信頼できる状態管理を利用することができます。

Service Fabric は、サービスの構築方法に依存しないので、任意のテクノロジを使用することができます。 ただし、マイクロサービスをビルドしやすくする組み込みのプログラミング API を提供します。

図 4-9 では、作成および単純なプロセス、または Docker コンテナーとして、Service Fabric でマイクロ サービスを実行する方法について説明します。 コンテナーベースのマイクロサービスとプロセッサーベースのマイクロサービスを同じ Service Fabric クラスター内に混在させることもできます。

![](./media/image13.png)

図 4-9:Azure Service Fabric 内のプロセッサーまたはコンテナーとしてマイクロサービスを展開する

Linux と Windows ホストに基づく Service Fabric クラスターには、Docker Linux コンテナーと Windows コンテナーを実行できます。

**詳細については** 、Azure の web サイト、Service fabric でコンテナー サポートの最新情報については、読み取り[Service Fabric とコンテナー](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview)します。

Service Fabric は、異なる論理アーキテクチャ (ビジネス マイクロ サービスまたは有界コンテキスト) 物理的な実装を定義できますプラットフォームの良い例です。 実装する場合など、[ステートフル Reliable Services](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction)で[Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview)、次のセクションで導入された"[ステートレスとステートフル マイクロ サービス](#stateless-versus-stateful-microservices)、"複数の物理サービスを含むビジネス マイクロ サービスの概念があります。

Service Fabric ステートフル Reliable Service を実装するときに論理的/ビジネス マイクロ サービスの観点から考えると、図 4-10 に示す、通常必要があります 2 層のサービスを実装します。 1 つは、バックエンド ステートフル リライアブル サービスで複数のパーティションを処理します。 2 つ目は、フロント エンド サービスは、または複数のパーティションまたはステートフルなサービス インスタンス間でルーティングとデータの集計を担当のゲートウェイ サービスです。 ゲートウェイ サービスは、Service Fabric と組み合わせて使用するバックエンド サービスにアクセスする再試行ループでクライアント側の通信を処理するも[リバース プロキシ](https://docs.microsoft.com/azure/service-fabric/service-fabric-reverseproxy)します。

![](./media/image14.png)

図 4-10:Service Fabric でいくつかのステートフルおよびステートレスなサービスを使ってビジネス マイクロ サービス

いずれの場合でも、Service Fabric ステートフル Reliable Services を使用する場合、通常は複数の物理サービスで構成される論理的/ビジネス マイクロサービス (境界指定されたコンテキスト) も使用できます。 それぞれに、ゲートウェイ サービス、およびパーティションのサービスのアドレスは、図 4-10 に示すように、ASP.NET Web API サービスとして実装できます。

Service Fabric では、サービスをグループ化して、サービスのグループを [Service Fabric アプリケーション](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-model)として展開することができます。これは、オーケストレーターおよびクラスター用のパッケージ化および展開の単位です。 そのため、Service Fabric アプリケーションもこの自律的なビジネスおよび論理マイクロ サービス境界または境界コンテキストにマップします。

### <a name="service-fabric-and-containers"></a>Service Fabric とコンテナー

Service Fabric 内のコンテナー、に関してもに、Service Fabric クラスター内のコンテナー イメージのサービスを展開できます。 図 4-11 は、そのほとんどのサービスごとに 1 つだけのコンテナーがある場合を示しています。

![](./media/image15.png)

図 4-11:Service Fabric 内に複数のサービス (コンテナー) を持つビジネス マイクロサービス

ただし、いわゆる "サイドカー" コンテナー (論理サービスの一部としてまとめて展開する必要がある 2 つのコンテナー) は Service Fabric でも可能です。 重要な点は、ビジネス マイクロサービスが、いくつかのまとまりのある要素を囲む論理的な境界であることです。 多くの場合、1 つのデータ モデルでは、1 つのサービスがありますが、場合によっては他の物理的な複数のサービスもする必要があります。

この作成 (2017 年 4 月) 時点で Service Fabric でことはできません SF 信頼性の高いステートフル サービスをデプロイするコンテナー — ゲスト コンテナー、ステートレス サービス、またはコンテナー内のアクター サービスをデプロイすることができます。 図 4-12 に示すように、同じ Service Fabric アプリケーションのコンテナーでのプロセスでのサービスとサービスを混在させることことに注意してください。

![](./media/image16.png)

図 4-12:コンテナーとステートフル サービスを含む Service Fabric アプリケーションにマップされているビジネス マイクロサービス

サポートは、Linux または Windows コンテナーで Docker コンテナーを使用しているかどうかに応じて異なるもあります。 今後のリリースでは、Service Fabric でコンテナーのサポートが拡大されます。 Azure の web サイトでは、Service fabric でコンテナー サポートに関する最新のニュース読み取り[Service Fabric とコンテナー](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview)します。

## <a name="stateless-versus-stateful-microservices"></a>ステートレス マイクロサービスとステートフル マイクロサービスの比較

前述のように、各マイクロサービス (論理的な境界指定されたコンテキスト) は、ドメイン モデル (データとロジック) を所有している必要があります。 場合は、ステートレス マイクロ サービス データベースを SQL Server のようなリレーショナル オプションまたは MongoDB、Azure DocumentDB などの NoSQL オプションを使用して、外部になります。

サービス自体もできるステートフルなマイクロ サービス内のデータが置かれているためです。 このデータは、だけでなく、同じサーバーでは、メモリ内のマイクロ サービス プロセス内に存在可能性がありますとドライブに保存され、その他のノードにレプリケートされます。 図 4-13 は、いくつかの方法を示しています。

![](./media/image17.png)

図 4-13:ステートレス マイクロサービスとステートフル マイクロサービスの比較

ステートレスな方法は、完全に有効な従来から使い慣れているパターンに似ているために、ステートフル マイクロ サービスよりも実装する方が簡単です。 ステートレス マイクロサービスは、プロセスおよびデータ ソース間の遅延を強制します。 追加のキャッシュとキューを使用してパフォーマンスを改善しようとしている場合は、含まれる移動する部分が増加します。 結果として、階層の数が多すぎる複雑なアーキテクチャになる可能性があります。

これに対し、[ステートフル マイクロ サービス](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis)ドメイン ロジックとデータ間の待機時間がないために、高度なシナリオで excel ことができます。 大量のデータ処理、ゲームに対応したバックエンド、サービス、およびその他の低待機時間シナリオを高速アクセスをローカルの状態を提供する、ステートフル サービスのメリットすべてとしてデータベースします。

ステートレス サービスおよびステートフル サービスは相互に補完します。 たとえば、ステートフル サービスは、複数のパーティションに分割できます。 それらのパーティションにアクセスするには、パーティション キーに基づく各パーティションへのアドレス指定方法を知っているゲートウェイ サービスとして、ステートレス サービスが動作する必要があります。

ステートフル サービスには欠点があります。 スケール アウトするための複雑さのレベルが課せられます。通常外部データベース システムによって実装される機能は、ステートフル マイクロサービスにまたがるレプリケーションや、データのパーティション分割などの機能として対処する必要があります。 ただし、これは、領域などのオーケストレーターのいずれかの[Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-platform-architecture)でその[ステートフル reliable services](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis)が最も役立つ-開発ステートフルのライフ サイクルを効率化し、マイクロ サービスを使用して、 [Reliable Services API](https://docs.microsoft.com/azure/service-fabric/service-fabric-work-with-reliable-collections)と[Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction)します。

ステートフル サービスを許可し、Actor パターンをサポートし、ビジネス ロジックとデータ間のフォールト トレランスと遅延を改善する他のマイクロサービス フレームワークは、Microsoft [Orleans](https://github.com/dotnet/orleans)、Microsoft Research、および [Akka.NET](https://getakka.net/) です。 両方のフレームワークは、現在 Docker のサポートを向上させています。

Docker コンテナーはそれ自身ステートレスなことに注意してください。 ステートフル サービスを実装する場合は、前に説明した追加の規範的で高度なフレームワークの 1 つが必要です。 ただし、この執筆時点で、Service Fabric のステートフル サービスはサポートされていませんプレーンなマイクロ サービスとしてのコンテナーとして。 コンテナー内の信頼性の高いサービスのサポートは、Service Fabric の今後のバージョンで使用できるになります。

>[!div class="step-by-step"]
>[前へ](soa-applications.md)
>[次へ](deploy-azure-kubernetes-service.md)
