---
title: Visual Studio Tools for Windows 上の Docker
description: Visual Studio 2017 バージョン 15.7 以降で使用可能な Docker ツールの説明を取得します。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.custom: vs-dotnet
ms.openlocfilehash: a373a8ebfef605b9845a684d3987355f8841aa1b
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219543"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a>Visual Studio Tools for Docker (Windows で Visual Studio) を使用

Visual Studio Code と Docker CLI を使用する場合は、Visual Studio Tools for Docker 開発ワークフローをワークフローに似ています。 実際には、同じの Docker CLI に基づきますが容易に開始、プロセスを簡略化、および生産性の向上を提供します、ビルドの実行、およびタスクを構成します。 実行し、デバッグのような単純なアクションを使用して、コンテナー **F5**と**Ctrl**+**F5**します。 実行し、1 つのコンテナーをデバッグできることに加え、省略可能なコンテナー オーケストレーションのサポートは、実行し、コンテナー (ソリューション全体) のグループを同時にデバッグできます。

> [!NOTE]
> この記事は、Windows 上の Visual Studio と Visual Studio for mac。

## <a name="configure-your-local-environment"></a>ローカル環境を構成します。

Docker for Windows の最新バージョン ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/))、簡単なセットアップでは、Docker アプリケーションの開発が容易にします。

Visual Studio 2017 では、docker のサポートが含まれます。 ここで Visual Studio 2017 をダウンロードします。 [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)

## <a name="use-docker-tools-in-visual-studio-2017"></a>Visual Studio 2017 での Docker ツールを使用します。

Docker のサポートをプロジェクトに追加することの 2 つのレベルがあります。 .NET Core web アプリのプロジェクトに追加できます、 *Dockerfile*に Docker サポートを有効にすると、プロジェクト ファイル。 次のレベルは、追加コンテナー オーケストレーションのサポート、 *Dockerfile* (まだ存在しない) 場合は、プロジェクトに、 *docker compose.yml*ソリューション レベルでのファイル。 既定では Visual Studio 2017 バージョン 15.7 またはそれ以前で、Docker Compose を使用して、コンテナー オーケストレーションのサポートが追加されます。 コンテナー オーケストレーションのサポートは、Visual Studio 2017 バージョン 15.8 オプトイン機能または後で、どの場合 Docker Compose と Service Fabric がサポートされます。

**追加** > **Docker サポート**と**追加** > **コンテナー オーケストレーション サポート**コマンドは、web アプリ プロジェクトのプロジェクト ノードの右クリック メニュー (またはコンテキスト メニュー) にある**ソリューション エクスプ ローラー**図 4-26 に示すようにします。

![Visual Studio での Docker サポート メニュー オプションを追加します。](media/add-docker-support-menu.png)

図 4-26:Visual Studio 2017 のプロジェクトに Docker サポートの追加

### <a name="add-docker-support"></a>Docker サポートを追加します。

選択して、既存の .NET Core web アプリ プロジェクトに Docker サポートを追加する**追加** > **Docker サポート**で**ソリューション エクスプ ローラー**します。 選択して、プロジェクトの作成時に Docker サポートを有効することも**Docker サポートを有効にする**で、**新しい ASP.NET Core Web アプリケーション**クリックした後に表示されたダイアログ ボックス**ok**で、**新しいプロジェクト** ダイアログ ボックスで、図 4-27 に示すようにします。

![Visual Studio での新しい ASP.NET Core web アプリの Docker サポートを有効にします。](./media/enable-docker-support-visual-studio.png)

図 4-27:Visual Studio 2017 でプロジェクトの作成時に Docker サポートを有効にします。

Docker サポートを有効にすると、Visual Studio の追加、 *Dockerfile*ファイルをプロジェクトにします。

> [!NOTE]
> 図 4-28 に示すように .NET Framework web アプリ プロジェクト (いない .NET Core web アプリのプロジェクト) のプロジェクトの作成時に Docker Compose のサポートが有効、コンテナー オーケストレーションのサポートも追加されます。
>
> ![Docker を有効にする .NET Framework web アプリ プロジェクトのサポートの構成](media/enable-docker-compose-support.png)

> 図 4-28:Visual Studio 2017 で .NET Framework web アプリ プロジェクトでの Docker Compose のサポートを有効にします。

### <a name="add-container-orchestration-support"></a>コンテナー オーケストレーションのサポートを追加します。

複数のコンテナー ソリューションを作成する場合は、コンテナー オーケストレーションのサポートをプロジェクトに追加します。 これにより、実行およびで同じ定義している場合、コンテナー (ソリューション全体) のグループを同時にデバッグ*docker compose.yml*ファイル。

コンテナー オーケストレーションのサポートを追加するには、ソリューションまたはプロジェクトのノードを右クリックし**ソリューション エクスプ ローラー**、選択**追加** > **コンテナー オーケストレーション サポート**. クリックして**Docker Compose**または**Service Fabric**コンテナーを管理します。

プロジェクトに追加の Dockerfile を参照してくださいコンテナー オーケストレーションのサポートをプロジェクトに追加した後、 **docker compose**でソリューションに追加されたフォルダー**ソリューション エクスプ ローラー**図 4-29 に示すように。

![Visual Studio でソリューション エクスプ ローラーでの docker ファイル](media/docker-support-solution-explorer.png)

図 4-29:Visual Studio 2017 でのソリューション エクスプ ローラーでの docker ファイル

場合*docker compose.yml*が既に存在する Visual Studio に必要な構成コードの行を追加するだけです。

## <a name="configure-docker-tools"></a>Docker ツールを構成します。

メイン メニューで、次のように選択します。**ツール** > **オプション**、展開と**コンテナー ツール** > **設定**します。 コンテナーのツールの設定が表示されます。

![](./media/visual-studio-docker-tools-options.png)

図 4-30:Docker Tools のオプション

次の表は、これらのオプションを設定する方法を決定するのに役立ちます。

| 名前 | 既定の設定 | 対象 | 説明 |
| -----|:---------------:|:----------:| ----------- |
| プロジェクトの読み込みで必要な Docker イメージを自動的にプルします。 | オン | Docker Compose | パフォーマンス向上のためのプロジェクトを読み込むときに、Visual Studio は、イメージが既にダウンロードしてコードを実行する準備ができたら、ダウンロード処理中にまたは、バック グラウンドで Docker プルの操作が開始されます。 プロジェクトをロードする場合だけ、コードを参照するには、これをオフにできます必要はありません、コンテナー イメージをダウンロードしないようにする場合。 |
| コンテナーをバック グラウンドで自動的に開始します。 | オン | Docker Compose | もう一度パフォーマンスを向上させる Visual Studio によりコンテナーとボリューム マウント ビルドおよびコンテナーを実行する場合に対応。 コンテナーが作成されたときを制御するには、これをオフにします。 |
| 自動的に強制終了のコンテナー ソリューションを閉じる | オン | Docker Compose | コンテナー ソリューションを閉じるか、Visual Studio の終了後も引き続き実行に、ソリューションが希望される場合は、これをオフにします。 |
| Localhost SSL 証明書を信頼する側は表示しません | オフ | ASP.NET Core 2.1 プロジェクト | Localhost SSL 証明書が信頼されていない場合は、Visual Studio は必要ない限り、このチェック ボックスをオンになって、プロジェクトを実行するたびと求められます。 |

> [!WARNING]
> Localhost SSL 証明書は信頼されず、プロンプトを抑制するボックスをチェックする場合は、アプリまたはサービスの実行時に HTTPS web 要求が失敗します。 その場合は、オフにして、**を求めない** チェック ボックスは、プロジェクトを実行し、プロンプトでの信頼関係を示します。

**詳細については:** サービスの実装と Visual Studio tools for Docker の使用の詳細については、次の記事を参照します。

ビルド、デバッグ、更新、およびローカル Docker コンテナーでアプリを更新します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)

コンテナー レジストリには、ASP.NET Core の Docker コンテナーを展開します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)

>[!div class="step-by-step"]
>[前へ](docker-apps-inner-loop-workflow.md)
>[次へ](set-up-windows-containers-with-powershell.md)