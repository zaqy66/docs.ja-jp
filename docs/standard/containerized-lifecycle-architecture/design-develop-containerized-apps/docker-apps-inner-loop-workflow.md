---
title: Docker アプリの内部ループ開発ワークフロー
description: Docker アプリケーションの開発の「内部ループ」ワークフローをについて説明します。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 2d592f92153040d910dcf529ec21770693f5973c
ms.sourcegitcommit: acd8ed14fe94e9d4e3a7fb685fe83d05e941073c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/20/2019
ms.locfileid: "56442322"
---
# <a name="inner-loop-development-workflow-for-docker-apps"></a>Docker アプリの内部ループ開発ワークフロー

サイクル全体の DevOps のまたがりメモリ割り当て、外側のループのワークフローをトリガーする前に、各開発者のコンピューターで、アプリ自体のコーディングや、好みの言語またはプラットフォームを使用してローカルでテストして (図 4-14) すべてが開始されます。 すべてのケースでは非常に重要なポイントに共通どのような言語、フレームワーク、またはプラットフォームを選んでも。 この特定のワークフローで常に開発およびがローカルで Docker コンテナーをテストします。

![](./media/image18.png)

図 4-14:内部ループ開発コンテキスト

コンテナーまたは Docker イメージのインスタンスは、これらのコンポーネントが含まれます。

-   (たとえば、Linux ディストリビューションまたは Windows)、オペレーティング システムの選択

-   (たとえば、アプリ バイナリ) の開発者によって追加されたファイル

-   構成 (たとえば、環境の設定との依存関係)

-   Docker で実行するどのようなプロセスの手順

(次のセクションで説明されている) プロセスとして Docker を使用する内部ループ開発ワークフローを設定することができます。 環境を設定するには、最初の手順が含まれているがないことを考慮に入れてを 1 回だけ実行する必要があるためです。

## <a name="building-a-single-app-within-a-docker-container-using-visual-studio-code-and-docker-cli"></a>Visual Studio Code と Docker CLI を使用して、Docker コンテナー内の 1 つのアプリの構築

アプリは、独自のサービスとその他のライブラリ (依存関係) から構成されます。

図 4-15 では、通常は各手順の詳細な説明の後に、Docker アプリを構築するときに実行するために必要な基本手順を示します。

![](./media/image19.png)

図 4-15:Docker CLI を使用してコンテナー化された Docker アプリケーションのライフ サイクルの高度なワークフロー

### <a name="step-1-start-coding-in-visual-studio-code-and-create-your-initial-appservice-baseline"></a>手順 1: Visual Studio Code でコーディングを開始し、アプリやサービスの初期ベースラインを作成します。

アプリケーションを開発する方法は、Docker を使用しないことを行う方法とよく似ています。 違いは、開発中に、展開しているアプリケーションまたは (Windows や Linux VM) など、ローカル環境で配置された Docker コンテナー内で実行されているサービスをテストします。

**ローカル環境の設定**

Mac および Windows 用 Docker の最新バージョンでは、これまでに、Docker アプリケーションの開発よりも簡単ですし、セットアップは簡単です。

**詳細については** Docker for Windows の設定手順についてを参照してください[ https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)します。

Docker for Mac の設定手順については、<https://docs.docker.com/docker-for-mac/>します。

さらに、実際に Docker CLI を使用しているときにアプリケーションを開発することができるように、コード エディターが必要があります。

Microsoft は、Visual Studio Code では、軽量なコード エディターは、Mac、Windows、および Linux でサポートされ、IntelliSense を提供しますです[多くの言語サポート](https://code.visualstudio.com/docs/languages/overview)(JavaScript、.NET、Go、Java、Ruby、Python、およびほとんど最新の言語の)[デバッグ](https://code.visualstudio.com/Docs/editor/debugging)、 [Git との統合](https://code.visualstudio.com/Docs/editor/versioncontrol)と[拡張機能のサポート](https://code.visualstudio.com/docs/extensions/overview)します。 このエディターは、Mac および Linux の開発者に最適です。 Windows でもに完全な Visual Studio アプリケーションを使用できます。

**詳細については** Visual Studio for Windows、Mac、または Linux をインストールする方法の詳細についてを参照してください<https://code.visualstudio.com/docs/setup/setup-overview/>します。

Docker CLI を使用して、コード エディターを使用してコードを記述が Visual Studio Code を使用する場合、Dockerfile を作成することが容易と docker compose.yml ファイル ワークスペースでします。 さらに、メッセージの下に、Docker CLI を使用して、詳細な操作を実行できるスクリプトを表示する IDE から Visual Studio Code のタスクを実行できます。

Visual Studio Code は、インストールする必要があります拡張機能によって提供されます。 キーを押して Ctrl + Shift + P、これを行うには、入力**ext インストール**、拡張機能を実行します。Marketplace 拡張機能の一覧を表示する拡張機能のコマンドをインストールします。 次に、入力**docker**結果をフィルター処理し、図 4-16 に示すように、Dockerfile と Docker Compose ファイル (yml) サポートの拡張機能を選択します。

![](./media/image20.png)

図 4-16:Visual Studio Code での Docker 拡張機能のインストール

### <a name="step-2-create-a-dockerfile-related-to-an-existing-image-plain-os-or-dev-environments-like-net-core-nodejs-and-ruby"></a>手順 2: 既存のイメージ (プレーンな OS または .NET Core、Node.js、Ruby などの開発環境) に関連する DockerFile を作成します。

カスタム イメージを構築およびデプロイするコンテナーごとに DockerFile が必要になります、そのため、1 つのカスタム サービスのアプリが構成されている場合は、DockerFile が 1 つを必要があります。 アプリが (マイクロ サービス アーキテクチャ) のように複数のサービスで構成される場合、サービスごとの 1 つの Dockerfile が必要があります。

DockerFile では、通常は、アプリまたはサービスのルート フォルダー内に配置され、Docker を設定して、そのアプリやサービスを実行する方法を認識できるように、必要なコマンドが含まれています。 DockerFile を作成し、コードと共にプロジェクトに追加 (.NET Core、node.js など)、または、環境に慣れていない場合、次のヒントを参照してください。

> [!TIP]
> というコマンド ライン ツールを使用する[yo docker](https://github.com/Microsoft/generator-docker)言語を選択して、必要な Docker 構成ファイルを追加で、プロジェクトからファイルをスキャフォールディングします。 基本的には、開発者の作業の開始を支援するために作成、適切な DockerFile、docker-compose.yml とその他の関連のスクリプトをビルドして Docker コンテナーを実行します。 選択した開発言語と移行先コンテナーのホストを確認するいくつかの質問はこの yeoman ジェネレーターから求められます。

![yo docker](./media/image21.png)

たとえば、図 4-17 を示しています、端末からの 2 つのスクリーン ショットでは、Windows と Mac では、どちらの場合も、実行されている yo docker で作業を既に構成されているサンプル コード プロジェクト (.NET Core では現在、Golang、およびサポートされている言語として Node.js を使用) が生成されます。Docker の先頭。

![](./media/image22.PNG)  ![](./media/image23.png)

図 4-17: yo docker コマンド ツール (左) の Windows と Mac

図 4-18 では、docker を使用して yo をスキャフォールディングする場所に既存の .NET Core プロジェクトを用意した後例を示します。

![](./media/image24.PNG)

図 4-18: yo の既存の .NET Core の docker プロジェクト実施中

DockerFile からは、(microsoft/dotnet:1.0.0-core"から"を使用して) などに使用する基本の Docker イメージを指定します。 通常、公式のリポジトリでから取得できる基本イメージ上にカスタム イメージをビルドは、 [Docker Hub レジストリ](https://hub.docker.com/)(など、 [.NET Core のイメージ](https://hub.docker.com/r/microsoft/dotnet/)1 つまたは[for Node.js](https://hub.docker.com/_/node/)).

***オプション a:既存の公式 Docker イメージを使用して、***

バージョン番号を持つ言語のスタックの公式のリポジトリを使用してにより、同じ言語機能が (開発、テスト、および運用環境を含む) すべてのコンピューターで使用できます。

.NET Core コンテナーのサンプル DockerFile を次に示します。

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

この場合は、Linux microsoft/aspnetcore:1.0.1 という名前の公式の ASP.NET Core Docker イメージのバージョン 1.0.1 以降を使用しては。 詳細についてを参照してください、 [ASP.NET Core Docker イメージ ページ](https://hub.docker.com/r/microsoft/aspnetcore/)と[.NET Core Docker イメージ ページ](https://hub.docker.com/r/microsoft/dotnet/)します。 でしたするイメージを使用するもう 1 つ比較可能なノード: 4 のように、Node.js、またはその他の多くの事前構成済みイメージで提供されている開発言語の onbuild [Docker Hub](https://hub.docker.com/explore/)。

DockerFile では、(ポート 80) などの実行時に使用する TCP ポートをリッスンするように Docker に指示する必要があります。

Docker は、アプリを実行する方法を認識できるように、DockerFile を使用している言語/フレームワークに応じてで追加できる構成の他の行があります。 たとえば、必要があるのでは、ENTRYPOINT 行\["dotnet"、"MyCustomMicroservice.dll"\]をビルドして、サービスの実行方法によっては、複数のバリアントを設定できますが、.NET Core アプリを実行します。 SDK と dotnet CLI をビルドして、.NET アプリの実行を使用している場合は、若干異なるがなります。 一番下の行は、ENTRYPOINT 行と行が追加されるアプリケーション用に選択した言語とプラットフォームによって異なります。

**詳細については** .NET Core アプリケーション用の Docker イメージを構築する方法の詳細についてを参照してください[ https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images](../../../core/docker/building-net-docker-images.md)します。

詳細については、独自のイメージを構築するには[ https://docs.docker.com/engine/\ チュートリアル/dockerimages/](https://docs.docker.com/engine/tutorials/dockerimages/)します。

**マルチプラット フォームのイメージ リポジトリ**

Windows コンテナーより一般的になると、1 つのリポジトリは、Linux および Windows のイメージなどのプラットフォーム バリアントを含めることができます。 これにより、複数のプラットフォームを対象に 1 つのリポジトリを使用する仕入先の Docker で新機能は、 [microsoft/aspdotnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) DockerHub レジストリでは使用できるリポジトリ。 ように、この機能は、アライブに関しては、Windows ホストからのこのイメージのプルをプルする、Windows バリアントは、Linux バリアントがプルは Linux ホストから同じイメージ名を取得します。

***オプション b:最初から基本イメージを作成します。***

これで説明したように、最初から、独自の Docker 基本イメージを作成することができます[記事](https://docs.docker.com/engine/userguide/eng-image/baseimages/)Docker から。 これはシナリオですが、Docker を使い始めたばかりの場合に適していない可能性がありますが、基本イメージの特定のビットを設定する場合は、行うことができます。

### <a name="step-3-create-your-custom-docker-images-embedding-your-service-in-it"></a>手順 3: これで、サービスを埋め込み、カスタム Docker イメージを作成します。

サービスごとにカスタム アプリを構成するには、関連するイメージを作成する必要があります。 1 つのサービスまたは web アプリのアプリが構成されている場合は、1 つのイメージを必要があります。

> [!NOTE]
> 「外側のループ DevOps ワークフロー」を考慮に入れて、イメージから作成されるビルド プロセスを自動化して、イメージはグローバル環境で作成できるように、Git リポジトリ (継続的インテグレーション) に、ソース コードをプッシュするたびに、ソース コードです。

ただし、その外側のループのルートに、検討する前に、Docker アプリケーションが実際に正しく動作するソース管理システム (Git など) が正しく動作しないコードをプッシュしないようにすることを確認する必要があります。

したがって、各開発者をローカルでテストし、完全な機能をプッシュするか、ソース管理システムに変更するまでの開発を続ける全体の内側のループ処理を行う最初が必要です。

図 4-19 に示すよう、ローカル環境と DockerFile を使用して、イメージを作成する docker ビルド コマンドを使用することができます (を実行することも、docker-compose up をいくつかのコンテナー/サービスによって構成されたアプリケーションのビルド)。

![](./media/image25.png)

図 4-19:Docker のビルドを実行しています。

まずを作成して展開可能なフォルダー実行 dotnet を使用して、コマンドを発行し、docker のビルドを実行に必要な .NET ライブラリと、必要に応じて、docker を直接実行する代わりに、プロジェクトのフォルダーから構築できます。

この例で、名前 cesardl/netcore から web api マイクロ サービスで Docker イメージを作成これ-docker: 最初 (: 特定のバージョンのように、タグを 1 つ目は)。 複数のコンテナーで、構成した Docker アプリケーションを作成する必要がある各カスタム イメージでは、この手順を実行できます。

既存のイメージで見つかりますローカル リポジトリ (開発用コンピューター)、docker を使用してイメージのコマンドを図 4-20 に示すようにします。

![](./media/image26.png)

図 4-20:Docker イメージを使用して既存のイメージを表示します。

### <a name="step-4-optional-define-your-services-in-docker-composeyml-when-building-a-composed-docker-app-with-multiple-services"></a>手順 4: (省略可能)複数のサービスで構成された Docker アプリを構築するときに docker compose.yml で、サービスを定義します。

Docker compose.yml ファイルを使用して、次のセクションの手順で説明されている展開コマンドを使用して、構成されたアプリケーションとしてデプロイに関連するサービスのセットを定義できます。

そのファイルでメインまたはルート ソリューション フォルダーを作成する必要があります。次の docker compose.yml ファイルに類似のコンテンツになります。

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

このケースでこのファイルは 2 つのサービスを定義します。 web サービス (カスタム サービス) と、redis サービス (一般的なキャッシュ サービス)。 各サービスは、各具象の Docker イメージを使用する必要があります、コンテナーとしてデプロイされます。 この特定の web サービスのイメージは、以下を行う必要があります。

-   現在のディレクトリに DockerFile からビルドします。

-   公開されているポート 80 をコンテナー ホスト コンピューター上でポート 81 上での転送します。

-   イメージを再構築することがなく、コードを変更することができるので、コンテナー内で指定するホスト上のプロジェクト ディレクトリをマウントします。

-   Redis サービスに web サービスをリンクします。

Redis サービスの使用、[最新のパブリック redis イメージ](https://hub.docker.com/_/redis/)Docker Hub レジストリからプルします。 [redis](https://redis.io/)はサーバー側アプリケーションでの非常に人気のあるキャッシュ システムです。

### <a name="step-5-build-and-run-your-docker-app"></a>手順 5: ビルドして Docker アプリの実行

アプリに 1 つのコンテナーのみがある場合だけ、Docker ホスト (VM または物理サーバー) にデプロイして実行する必要があります。 ただし、複数のサービス、アプリが構成されている場合をする必要があります*組み立てること*もします。 さまざまなオプションを見てみましょう。

***オプション a:1 つのコンテナーまたはサービスを実行します。***

次に示すように docker run コマンドを使用して、Docker イメージを実行できます。

```
docker run -t -d -p 80:5000
cesardl/netcore-webapi-microservice-docker:first
```

この配置のいます 要求をリダイレクトする内部ポート 5000 をポート 80 に送信されるに注意してください。 ここで、アプリケーションは外部ポート、ホスト レベル 80 でリッスンします。

***オプション b:構成して複数コンテナー アプリケーションの実行***

ほとんどのエンタープライズ シナリオでは、Docker アプリケーションを複数のサービスはから構成します。 コマンドを実行するような場合、docker compose を (図 4-21)、以前作成した可能性があります、docker-compose.yml ファイルを使用します。 このコマンドを実行するには、すべての関連するコンテナーの構成済みのアプリケーションはデプロイします。

![](./media/image27.png)

図 4-21:"、Docker-compose up"コマンドの実行結果

Docker を実行した後、compose をデプロイする必要が、アプリケーションとその関連コンテナー、Docker ホストに VM の表記で図 4-22 に示すようにします。

![](./media/image28.png)

図 4-22:Docker コンテナーが展開された VM

注、docker-compose up および docker の実行は、開発環境で、コンテナーをテストするための十分に可能性がありますがないそれらを使用するすべての場合は、Docker クラスターの操作を想定しているし、Docker Swarm、Mesosphere DC/OS、または Kubernetes などのオーケストレータースケール アップできるようにするには。 などのクラスターを使用している場合[Docker Swarm mode](https://docs.docker.com/engine/swarm/)デプロイし、した場合など、docker サービスを 1 つのサービスの作成やその他のコマンドでテストに必要な (可能で、Docker for Windows と Mac バージョン 1.12 以降)、複数のコンテナーから成るアプリを展開するには、docker を使用してバンドルの作成し、docker は、情報の記事で説明したように、スタックとして構成済みのアプリを展開することで、myBundleFile をデプロイ[分散アプリケーション バンドル](https://blog.docker.com/2016/06/docker-app-bundle/)Docker から。

[DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/)と[Kubernetes](https://kubernetes.io/docs/user-guide/deployments/#creating-a-deployment)さまざまな展開コマンドと、スクリプトを使用します。

### <a name="step-6-test-your-docker-application-locally-in-your-local-cd-vm"></a>手順 6: (ローカル CD VM) では、ローカルで Docker アプリケーションをテストします。

この手順は、アプリの実行内容によって異なります。

非常に単純な .NET Core Web API の"Hello World"を 1 つのコンテナーまたはサービスとしてデプロイされている場合、DockerFile で指定された TCP ポートを提供することで、サービスにアクセスするとだけです。

サービスに移動する localhost が有効でない場合は、このコマンドを使用して、マシンの IP アドレスを検索します。

docker-machine ip *your-container-name*

Docker ホストでは、ブラウザーを開いて、そのサイトに移動します図 4-23 に示すようにアプリ/サービスを実行して、参照してください必要があります。

![](./media/image29.png)

図 4-23:Localhost を使用してローカルで Docker アプリケーションのテスト

前に説明したように、実行するには、docker で展開された方法であるためですはポート 80 が使用が内部的にはポート 5000 にリダイレクトされましたされていることに注意してください。

これは、CURL を使用して、ターミナルから、テストできます。 図 4-24 に示すように、Windows で Docker のインストールでは、既定の IP、10.0.75.1、です。

![](./media/image30.png)

図 4-24:CURL を使用してローカルの Docker アプリケーションのテスト

**Docker で実行されているコンテナーのデバッグ**

Visual Studio Code は、Node.js と .NET Core コンテナーなどの他のプラットフォームを使用している場合に、Docker のデバッグをサポートします。

デバッグすることもできます Docker で .NET Core コンテナー、Visual Studio を使用する場合、次のセクションで説明されているとします。

**詳細情報:** Node.js の Docker コンテナーのデバッグに関する詳細については、するには<https://blog.docker.com/2016/07/live-debugging-docker/>と[https://blogs.msdn.microsoft.com/\ユーザー\_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/](https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/)します。

>[!div class="step-by-step"]
>[前へ](docker-apps-development-environment.md)
>[次へ](visual-studio-tools-for-docker.md)