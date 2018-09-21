---
title: Visual Studio Tools for Docker (Windows で Visual Studio) を使用
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: af14c92ab27885deec878dc33e7b94035f43e65b
ms.sourcegitcommit: dfb2a100cfb4d3902c042f17b3204f49bc7635e7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2018
ms.locfileid: "46516744"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a>Visual Studio Tools for Docker (Windows で Visual Studio) を使用

Visual Studio Code と Docker CLI を使用する場合は、Docker を Visual Studio Tools を使用する場合は、開発ワークフローをワークフローに似ています。 実際には、同じの Docker CLI に基づきますが容易に開始、プロセスを簡略化、および生産性の向上を提供します、ビルドの実行、およびタスクを構成します。 実行し、f5 キーを押して、Visual Studio から ctrl キーを押しながら f5 キーなどの単純なアクションを使用してコンテナーをデバッグすることもできます。 実行し、1 つのコンテナーをデバッグできることに加え、省略可能なコンテナー オーケストレーションのサポートは、実行し、コンテナー (ソリューション全体) のグループを同時にデバッグできます。 同じコンテナーを定義するだけ*docker compose.yml*ソリューション レベルでのファイル。

## <a name="configuring-your-local-environment"></a>ローカル環境を構成します。

Docker のサポートは、インストールされている .NET と .NET Core のワークロードのいずれかで Visual Studio 2017 に含まれます。 Docker for Windows を個別にインストールします。

Docker for Windows の最新バージョンでは、これまでにアプリケーションを開発 Docker、次の参照で説明したように、セットアップは簡単なためより簡単になります。

**詳細情報:** Docker for Windows をインストールする方法の詳細については、するには<https://docs.docker.com/docker-for-windows/>します。

**詳細情報:** Visual Studio をインストールする方法の詳細についてを参照してください[ https://visualstudio.microsoft.com/downloads/](https://visualstudio.microsoft.com/downloads/)します。

Visual Studio Tools for Docker をインストールする詳細を表示するには<http://aka.ms/vstoolsfordocker>と<https://docs.microsoft.com/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker>します。

## <a name="using-docker-tools-in-visual-studio-2017"></a>Visual Studio 2017 での Docker ツールの使用

プロジェクトに Docker サポートを追加するときに (図 4-26 参照)、Visual Studio の追加、 *Dockerfile*をプロジェクトのルート。

![Visual Studio 2017 プロジェクトでの Docker ソリューションのサポートの有効化](./media/image32.png)

図 4-26: Visual Studio 2017 プロジェクトでの Docker ソリューションのサポートの有効化

 既定では Visual Studio 2017 バージョン 15.7 またはそれ以前で、Docker Compose を使用して、コンテナー オーケストレーションのサポートが追加されます。 コンテナー オーケストレーションのサポートは、Visual Studio 2017 バージョン 15.8 オプトイン機能または後で、どの場合 Docker Compose と Service Fabric がサポートされます。

Visual Studio 15.8 およびそれ以降のバージョンを使用して、関連するコンテナーがあるソリューションで複数のプロジェクトのサポートを追加できます。 ソリューションまたはプロジェクト ノードを右クリックして**ソリューション エクスプ ローラー**、選択**追加** > **コンテナー オーケストレーション サポート**します。  クリックして**Docker Compose**または**Service Fabric**コンテナーを管理します。

選択すると**Docker Compose**、Visual Studio でソリューションのサービス セクションを追加する*docker compose.yml*ファイル (または存在していない場合、ファイルが作成されます)。 マルチ コンテナー ソリューションの作成を開始する簡単な方法開くことができます、 *docker compose.yml*ファイルし、その他の機能を更新します。

この操作は、必要な構成をコード行を追加します、 *docker compose.yml*ソリューション レベルで設定します。

できます Docker サポートの Visual Studio 2017 では、ASP.NET Core プロジェクトを作成するときに図 4-27 に示すようにします。

![プロジェクトを作成するときに Docker サポートの有効化](./media/image33.png)

図 4-27: Docker のサポート、プロジェクトを作成するときにオン

Visual Studio でソリューションに Docker サポートを追加した後も表示されますに新しいノード ツリー**ソリューション エクスプ ローラー**と、 *docker compose.yml*ファイル、図 4-28 に示すようにします。

![docker compose.yml ファイルがソリューション エクスプ ローラーで表示されます。](./media/image34.PNG)

図 4-28: docker compose.yml ファイルに表示されます**ソリューション エクスプ ローラー**

1 つを使用して複数コンテナー アプリを展開する可能性があります*docker compose.yml*ファイルを実行する場合に`docker-compose up`ただし、Visual Studio 環境 (開発対によっての値をオーバーライドするために、それらのグループを追加します。運用環境) と実行 (リリース対デバッグ) を入力します。 この機能は以降の章で強化について説明します。

複数のコンテナーを管理するのに Docker Compose ではなく Service Fabric を使用することもできます。 参照してください[チュートリアル: Azure Service Fabric への Windows コンテナーで .NET アプリケーションのデプロイ](https://docs.microsoft.com/azure/service-fabric/service-fabric-host-app-in-a-container)します。

**詳細情報:** サービスの実装と Visual Studio tools for Docker の使用の詳細については、次の記事を参照します。

ビルド、デバッグ、更新、およびローカル Docker コンテナーでアプリを更新します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)

コンテナー レジストリには、ASP.NET Core の Docker コンテナーを展開します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)

>[!div class="step-by-step"]
[前へ](docker-apps-inner-loop-workflow.md)
[次へ](set-up-windows-containers-with-powershell.md)
