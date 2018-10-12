---
title: Docker アプリケーションの外側のループ DevOps ワークフローの手順を実行します。
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/10/2018
ms.openlocfilehash: a03853a508cfb3d5dd5fbfe66e4ef484b685faaa
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/15/2018
ms.locfileid: "45653240"
---
# <a name="steps-in-the-outer-loop-devops-workflow-for-a-docker-application"></a>Docker アプリケーションの外側のループ DevOps ワークフローの手順を実行します。

図 5-1 は、DevOps の外側のループのワークフローを構成する手順の説明、エンド ツー エンドの図を表示します。

![](./media/image1.png)

Microsoft ツールと Docker アプリケーション DevOps 外側のループ ワークフローを図 5-1:

次に、それぞれの手順を詳しく見ていきましょう。

## <a name="step-1-inner-loop-development-workflow"></a>手順 1: 内部ループ開発ワークフロー

この手順は、第 4 章で詳しく説明を要約すると、ここでは、外側のループ開始位置となる、開発者が CI パイプラインのアクションの開始 (Git) のようなソース コントロール管理システムにコードをプッシュする時点。

## <a name="step-2-source-code-control-integration-and-management-with-azure-devops-services-and-git"></a>手順 2: ソース コード管理の統合と Azure DevOps Services および Git を使用した管理

この手順では、チームのさまざまな開発者から、すべてのコードの統合されたバージョンを収集するバージョン管理システムに用意する必要があります。

アプリケーションを Docker イメージを送信する必要がありますいないを強調するために重要な場合でも、ソース コード管理 (SCC) とソース コード管理には、習慣にほとんどの開発者、DevOps ライフで Docker アプリケーションを作成するときのサイクルと思われる場合があります、直接、グローバル Docker レジストリに (Azure Container Registry や Docker Hub) など、開発者のマシンから。 反対に、グローバル ビルドまたはソース コード リポジトリ (Git) などに基づく CI パイプラインで、統合されることは、ソース コードのみにリリースされ、運用環境に展開する Docker イメージを作成する必要があります。

独自のマシン内でテストするときに、開発者だけで開発者自身によって生成されたローカル イメージを使用してください。 これは、ため、DevOps パイプラインを SCC コードからアクティブ化することが重要です。

Azure DevOps サービスと Team Foundation Server は、Git と Team Foundation バージョン管理をサポートします。 それらの間を選択し、エンド ツー エンドの Microsoft エクスペリエンスを使用できます。 ただし、管理することもできます (GitHub、Git リポジトリをオンプレミス、または Subversion) ような外部リポジトリでは、コードとそれに接続し、DevOps の CI パイプラインの開始点としてコードを取得できます。

## <a name="step-3-build-ci-integrate-and-test-with-azure-devops-services-and-docker"></a>手順 3: ビルド、CI、統合、および Azure DevOps を使用してテスト サービスと Docker

CI が最新のソフトウェアのテストおよび配信のための標準として登場しました。 Docker ソリューションでは、開発および運用チーム間での問題を明確に分離を維持します。 Docker イメージの不変性により、どのような開発、CI、テストおよび運用環境で実行が間に反復可能なデプロイ。 Docker エンジン開発者向けのノート パソコンに展開し、テスト インフラストラクチャは、環境間で、コンテナーを移植性。

この時点で、送信された正しいコードにバージョン管理システムがある必要があります、*サービスを構築*コードを選択し、グローバル ビルドとテストを実行します。

(CI、ビルド、テスト) この手順の内部ワークフローとは、ビルド サーバー (Azure DevOps サービス)、Docker エンジンと Docker レジストリをコード リポジトリ (Git など) から成る CI パイプラインを作成する方法。

できますサービスを使用する Azure DevOps の基盤として、アプリケーションを構築および、CI のパイプラインを設定するため、組み込みの「アイテム」を公開するため"アーティファクト リポジトリに、"については、次の手順で説明します。

Docker を使用して、展開は、「最終的な成果物」ときに展開するのには、アプリケーションやサービスを使用した Docker イメージ内に埋め込まれます。 これらのイメージのプッシュまたは発行を*Docker レジストリ*(Azure Container Registry で使用できるはまたはの公式の基本イメージの一般的な使用の Docker Hub レジストリなどのパブリック 1 などのプライベート リポジトリ)。

基本的な概念を次に示します。 CI のパイプラインは、Git などのソース コード管理リポジトリにコミットしてオフ開始になります。 図 5-2 に示すように、コミットは、Docker コンテナー内のビルド ジョブを実行し、そのジョブが正常に完了すると、Docker レジストリに Docker イメージをプッシュする DevOps サービスを Azure になります。

![](./media/image2.png)

図 5-2: 必要な手順では、CI

Docker と Azure DevOps サービスの基本的な CI ワークフロー手順を次に示します。

1.  開発者は、ソース コード管理リポジトリ (Git または Azure DevOps Services、GitHub など) にコミットをプッシュします。

2.  Azure DevOps Services または Git を使用している場合は、CI ビルドは、Azure DevOps サービスのチェック ボックスを選択するだけであることを意味します。 (GitHub) などの外部の SCC を使用している場合、 *webhook*更新プログラムの DevOps サービスを Azure に通知または Git と GitHub にプッシュされます。

3.  Azure DevOps サービスは、イメージだけでなく、アプリケーションとテストのコードを記述する DockerFile を含む、ソース コード管理リポジトリをプルします。

4.  Azure DevOps サービスは、Docker イメージをビルドおよびビルド番号のラベルします。

5.  Azure DevOps サービスは、プロビジョニング済みの Docker ホスト内の Docker コンテナーをインスタンス化し、適切なテストを実行します。

6.  「試みられたビルド」がわかるように、イメージが最初にわかりやすい名前を付け、テストが成功した場合は、(のように"/1.0.0"またはその他の任意のラベル)、(Docker Hub、Azure Container Registry、DTR など)、Docker レジストリにプッシュし、

### <a name="implementing-the-ci-pipeline-with-azure-devops-services-and-the-docker-extension-for-azure-devops-services"></a>Azure DevOps サービス用の Azure DevOps サービスと Docker 拡張機能を使用して、CI パイプラインの実装

[Azure DevOps サービスの Docker 拡張機能](https://aka.ms/vstsdockerextension)CI のパイプラインを Docker イメージを作成、認証済みの Docker レジストリに Docker イメージをプッシュ、または実行する Docker イメージ、Docker によって提供されるその他の操作を実行するタスクを追加します。CLI。 また、ビルド、プッシュ、および複数のコンテナーの Docker アプリケーションを実行または図 5-3 に示すように Docker Compose CLI によって提供されるその他の操作を実行に使用できる Docker Compose のタスクを追加します。

![](./media/image3.png)

図 5-3: Docker の CI パイプラインでは、Azure DevOps サービス

Docker 拡張機能は、Docker ホストとコンテナーまたはイメージ レジストリにサービス エンドポイントを使用できます。 (現在必要カスタム Azure DevOps サービス エージェント)。 使用可能な場合は、ローカル Docker ホストを使用する既定のタスクそれ以外の場合、Docker ホスト接続を指定することが必要です。 認証されると、イメージのプッシュなどの Docker レジストリに依存するアクションでは、Docker レジストリ接続を指定することが必要です。

Azure DevOps サービスの Docker 拡張機能では、Azure DevOps サービス アカウントに、次のコンポーネントがインストールされます。

-   Docker レジストリに接続するためのサービス エンドポイント

-   Docker コンテナーのホストに接続するためのサービス エンドポイント

-   以下を実行する Docker タスク:

-   イメージを作成します。

-   レジストリにイメージまたはリポジトリをプッシュします。

-   イメージをコンテナーで実行します。

-   Docker コマンドを実行します

-   Docker Compose のコマンドを実行する Docker Compose のタスク

これらの Azure DevOps サービス タスクでビルドを Linux Docker ホスト/VM Azure でプロビジョニングし、(Azure Container Registry、Docker Hub、プライベート Docker DTR、またはその他の任意の Docker レジストリ)、優先の Docker レジストリの Docker の CI パイプラインをアセンブルできますを非常に一貫した方法。

***要件:***

-   Azure DevOps サービス、またはオンプレミス インストールの場合、Team Foundation Server 2015 Update 3 またはそれ以降。

-   Docker バイナリを含む Azure DevOps サービス エージェント。

次のいずれかを作成する簡単な方法では、Docker を使用して、Azure DevOps サービス エージェントの Docker イメージに基づくコンテナーを実行します。

**詳細については** パイプラインし、チュートリアルを表示する、次のサイトを参照してください。 Azure DevOps サービスの Docker CI のアセンブリについての詳細読み取り。

Docker コンテナーとして Azure DevOps サービス エージェントを実行している: [ https://hub.docker.com/r/\ vsts agent//](https://hub.docker.com/r/microsoft/vsts-agent/)

Azure DevOps サービスの Docker 拡張機能: <https://aka.ms/vstsdockerextension>

Azure DevOps サービスを使用した .NET Core Linux Docker イメージを構築するには。 <https://blogs.msdn.microsoft.com/stevelasker/2016/06/13/building-net-core-linux-docker-images-with-visual-studio-team-services/>

Docker のサポートと Visual Studio Team Service の Linux ベースのビルド コンピューターの構築。 <http://donovanbrown.com/post/2016/06/03/Building-a-Linux-Based-Visual-Studio-Team-Service-Build-Machine-with-Docker-Support>

### <a name="integrate-test-and-validate-multicontainer-docker-applications"></a>統合、テスト、および複数のコンテナー Docker アプリケーションの検証

通常、1 つのコンテナーではなく、複数のコンテナーの Docker アプリケーションのほとんどがで構成されます。 良い例は、マイクロ サービスごとに 1 つのコンテナーが、マイクロ サービス指向アプリケーションです。 しかし、マイクロ サービス アプローチのパターンに厳密に従うと、しなくても、Docker アプリケーションは、複数のコンテナーまたはサービスの構成は非常に高い可能性が。

そのため、CI パイプラインでアプリケーション コンテナーをビルドした後も必要があります、展開、統合、およびすべての統合の Docker ホスト内で、またはさらには、コンテナーがテスト クラスターには、そのコンテナー全体のアプリケーションをテストするには分散されます。

1 つのホストを使用している場合は、docker などの Docker コマンドを使用することができます-ビルドしてデプロイをテストし、1 つの VM で Docker 環境を検証関連のコンテナーを作成します。 しかし、DC/OS、Kubernetes、Docker Swarm などをオーケストレーター クラスタを使用する場合は別のメカニズムまたはオーケストレーターで、選択したクラスター/スケジューラによって、コンテナーをデプロイする必要があります。

次に、Docker コンテナーに対して実行できるテストの種類をいくつか示します。

-   Docker コンテナー用の単体テスト

-   相互に関連するアプリケーションやマイクロ サービスのグループのテスト

-   運用環境と「カナリア」のリリースでのテストします。

重要な点は、統合と機能テストを実行するときに、コンテナーの外部からそれらのテストを実行する必要があります。 テストを定義しないと、コンテナーは運用環境にデプロイするものとまったく同じ必要のある静的なイメージに基づいているので、展開する場合は、コンテナー内で実行する必要があります。

複数のクラスター (クラスター、クラスターのステージング、および運用環境のクラスターのテスト) のテストなどのより高度なシナリオをテストするときに非常に適してのオプションでは、さまざまなクラスターでテストをレジストリにイメージを発行します。

### <a name="push-the-custom-application-docker-image-into-your-global-docker-registry"></a>グローバルな Docker レジストリをカスタム アプリケーションの Docker イメージをプッシュします。

Docker イメージをテストおよび検証した後にタグ付けし、Docker レジストリに公開します。 Docker レジストリは重要な部分を Docker アプリケーションのライフ サイクルの QA および実稼動環境にデプロイするのには、カスタム テスト (「試みられたイメージ」とも呼ばれます) を格納する中央の場所です。

方法、ソース コード管理リポジトリ (Git など) に格納されているアプリケーション コードは、「普遍の情報源」と同様に、Docker レジストリは、「ソース実のところの」、QA 環境または運用環境にデプロイするには、バイナリのアプリケーションやビットです。

通常、Azure コンテナー レジストリまたは Docker Trusted Registry のように、オンプレミスのレジストリまたは (制限付きのアクセス権を持つパブリック クラウドのレジストリで、カスタム イメージのプライベート リポジトリをプライベート リポジトリのいずれかがする可能性があります。Docker Hub)、この最後の場合、コードがオープン ソースの場合でも、ベンダーのセキュリティを信頼する必要があります。 どちらの方法でこれを行うメソッドとよく似ています docker push コマンド、に基づいて最終的に図 5-4 に示すようにします。

![](./media/image4.png)

図 5-4: カスタム イメージを Docker レジストリに発行します。

Azure Container Registry、Amazon Web Services Container Registry、Google Container Registry、Quay レジストリなどのクラウド ベンダーからの Docker レジストリの複数のサービス提供しています。

図 5-5 に示すようには、Azure DevOps サービスの Docker 拡張機能を使用して、一連の (Azure Container Registry) などの認証済みの Docker レジストリに、複数のタグでの docker-compose.yml ファイルで定義したサービスのイメージをプッシュできます。

![](./media/image5.png)

図 5-5: Azure DevOps サービスを使用して Docker レジストリにカスタム イメージを発行する

**詳細については** 詳細については、Azure DevOps サービスの Docker 拡張機能に移動します。<https://aka.ms/vstsdockerextension>します。 Azure Container Registry の詳細については、するには<https://aka.ms/azurecontainerregistry>します。

## <a name="step-4-cd-deploy"></a>手順 4: CD、展開

Docker イメージの不変性により、反復可能な展開に何が開発、CI、テストし、運用環境で実行します。 所持している複数の環境に展開したり、Docker レジストリ (プライベートまたはパブリック) で公開されているアプリケーションの Docker イメージを作成したら、(運用、QA、ステージングなど) Azure DevOps サービスを使用して、CD パイプラインからパイプラインのタスクまたは Azure DevOps サービス リリース管理されます。

ただし、この時点でに依存する展開する Docker アプリケーションの種類。 などのより複雑なアプリケーションを展開すると非常に異なるアプリケーションを配置する単純な (構成と展開の観点から)、モノリシックのようにいくつかのコンテナーやサービスを構成するアプリケーションと展開されたいくつかのサーバーまたは Vm には、ハイパー スケール機能を備えたマイクロ サービス指向アプリケーションです。 これら 2 つのシナリオは、次のセクションについて説明します。

### <a name="deploying-composed-docker-applications-to-multiple-docker-environments"></a>複数の Docker 環境への Docker アプリケーションの展開で構成されています

最初に、複雑なシナリオを見てみましょう。 単純で Docker ホスト (Vm またはサーバー) 環境を 1 つまたは複数の環境に展開する (品質保証、ステージング、および運用)。 このシナリオで内部的には、CD パイプラインできますを使用して docker-図 5-6 に示すようにコンテナーやサービス、その関連する一連の Docker アプリケーションを展開する (Azure DevOps サービス展開タスク) から作成します。

![](./media/image6.png)

図 5-6: 単純な Docker ホスト環境のレジストリへのアプリケーション コンテナーのデプロイ

図 5-7 は、タスクの追加 ダイアログ ボックスの Docker Compose をクリックして、Azure DevOps サービスを使用して、QA/テスト環境にビルド、CI を接続する方法を示しています。 ただし、ステージング環境または運用環境を展開する場合は、通常使用する Release Management の機能が複数の環境を処理 (などの QA、ステージング、および運用)。 Azure DevOps サービスを使用して単一の Docker ホストにデプロイする場合は"Docker Compose"タスク (、docker を呼び出すことですが、内部的にコマンドを作成)。 Azure Container Service にデプロイする場合は、以下のセクションで説明したように、Docker デプロイ タスクを使用します。

![](./media/image7.png)

図 5-7: Azure DevOps サービス パイプラインで Docker Compose のタスクを追加します。

Azure DevOps サービスで、リリースを作成するときに、一連の入力の成果物がかかります。 これらは複数の環境であるリリースの有効期間全体を通じて不変します。 コンテナーを導入するときに、入力の成果物を展開する、レジストリ内のイメージを識別します。 これら識別方法によっては、リリースでは、docker-compose ファイルから「myimage:latest」を参照するとき、最も明白なケースの全期間にわたって同じままで、保証はありません。

Azure DevOps サービス用 Docker 拡張機能は、ダイジェストとなる特定のレジストリのイメージが含まれているビルド成果物を生成する機能バイナリと同じイメージを一意に識別することが保証されます。 これらは実際に、リリースへの入力として使用します。

### <a name="managing-releases-to-docker-environments-by-using-azure-devops-services-release-management"></a>Azure DevOps Services Release Management を使用して Docker 環境にリリースを管理します。

Azure DevOps サービス拡張機能を通じて新しいイメージを構築する、Docker レジストリに発行して、Linux または Windows のホストで実行して docker などのコマンドを使用して、Azure DevOps などのアプリケーションが全体として複数のコンテナーをデプロイする作成図 5-8 に示すように複数の環境用リリース管理機能をサービスします。

![](./media/image8.png)

図 5-8: Azure DevOps サービス Release Management から Azure DevOps サービスの Docker Compose のタスクの構成

ただし、図 5-6 に示すように、図 5-8 の実装のシナリオが (単純な Docker ホストと Vm へのデプロイは、および 1 つのコンテナーまたはイメージごとにインスタンスがあるが) 非常に基本的ながあり、おそらく開発またはテスト sc にのみ使用することに留意してください。enarios します。 高可用性 (HA) にするほとんどのエンタープライズ運用環境シナリオでと間の負荷分散複数のノード、サーバー、Vm、および「インテリジェントなフェールオーバー」ようにする場合は、サーバーまたはノードでの管理が容易なスケーラビリティが失敗した場合は、そのサービスとコンテナーは、別のホスト サーバーまたは VM に移動されます。 その場合は、クラスターのコンテナー、オーケストレーター、およびスケジューラなどのより高度なテクノロジ必要があります。 したがって、これらのクラスターにデプロイする方法は、次のセクションで説明する高度なシナリオを正確にです。

### <a name="deploying-complex-docker-applications-to-docker-clusters-dcos-kubernetes-and-docker-swarm"></a>Docker クラスター (DC/OS、Kubernetes、および Docker Swarm) への複雑な Docker アプリケーションの展開

分散アプリケーションの性質も分散されるコンピューティング リソースが必要です。 運用スケール機能がある、高いスケーラビリティを提供する機能をクラスタ リングにする必要があり、プールされたリソースに基づいて HA します。

コンテナーを Docker Swarm などの CLI ツールからこれらのクラスターに手動でデプロイできます (使用するように[docker サービスを作成](https://docs.docker.com/engine/swarm/swarm-tutorial/deploy-service/)) または web UI など[Mesosphere Marathon](https://mesosphere.github.io/marathon/docs/marathon-ui.html) DC/OS クラスターが行う必要がありますpunctual 展開のテストにのみ、または管理などの目的でスケール アウトまたは監視目的では、を予約します。

CD の観点と Azure DevOps サービスから具体的には、タスクを実行できます特別に作成された展開コンテナーに分散クラスターにコンテナー化されたアプリケーションのデプロイは、Azure DevOps サービス リリース管理環境から図 5-9 に示すようには、サービスです。

![](./media/image9.png)

図 5-9: 分散アプリケーションをコンテナー サービスを展開します。

最初に、特定のクラスターやオーケストレーターをデプロイするときは従来使用して特定の展開スクリプトと各オーケストレーター (つまり、Mesosphere DC/OS または Docker と Docker のさまざまな展開メカニズムがある Kubernetes メカニズムSwarm) の代わりに、単純なと使いやすい docker compose、docker compose.yml 定義ファイルに基づいてツール。 ただし、図 5-10 に示すように、Microsoft Azure DevOps サービス Docker デプロイ タスクに協力してくれたするようになりましたも展開できます DC/OS に Microsoft では、「変換」を実行するために、使い慣れた docker compose.yml ファイルを使用するだけで (から、docker compose.yml ファイルを DC/OS で必要な他の形式)。

![](./media/image10.png)

図 5-10: RM 環境への Docker デプロイ タスクの追加

図 5-11 は、Docker の展開タスクを編集し、対象の型 (Azure Container Service DC/OS、ここでは)、Docker Compose ファイル、および (Azure Container Registry や Docker Hub) などの Docker レジストリ接続を指定する方法について説明します。 これは、タスクのすぐに使用できるカスタム Docker イメージ、DC/OS クラスター内のコンテナーとしてデプロイを取得する場所です。

![](./media/image11.png)

図 5-11: Docker デプロイ タスクの定義を展開する Azure Container Service DC/OS に

**詳細については** 詳細については、Azure DevOps サービスと Docker の CD パイプラインを次のサイトを参照してください。

Docker と Azure Container Service 用の azure の DevOps サービス拡張機能: [ https://aka.ms/\ vstsdockerextension](https://aka.ms/vstsdockerextension)

Azure Container Service: <https://aka.ms/azurecontainerservice>

Mesosphere DC/OS: <https://mesosphere.com/product/>

## <a name="step-5-run-and-manage"></a>手順 5: 実行および管理

エンタープライズ運用レベルは、し、それ自体のと操作の種類のための主要なサブジェクトと、ユーザーがこの領域の大きなスコープとそのレベル (IT 運用) にとって、全体を次に充てることが実行されていると、アプリケーションを管理するためこれを説明する章です。

## <a name="step-6-monitor-and-diagnose"></a>手順 6: 監視し、診断

このトピックでもについては [次へ] の章で実稼働システム; IT 操作を実行するタスクの一部としてただしが、アプリケーションが頻繁に改善するために、開発チームにこの手順で得られた知見をフィードする必要がありますを強調表示に重要です。 そのポイントの表示からもの一部では、DevOps タスクと操作は通常、実行が IT です。

監視と診断は、DevOps の領域内の 100% の場合にのみは、監視のプロセスとまたはベータ版のテスト環境に対して、開発チームによって実行された分析です。 これは、ロード テストを実行するか、ベータ版またはベータ テスト担当者が新しいバージョンを試みている、QA 環境を監視するだけで実行されます。

>[!div class="step-by-step"]
[前へ](index.md)
[次へ](../run-manage-monitor-docker-environments/index.md)
