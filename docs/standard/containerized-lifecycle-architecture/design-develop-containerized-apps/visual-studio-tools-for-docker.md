---
title: Visual Studio Tools for Windows 上の Docker
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: cd140c12ef4a0187cce096e013937d5c98cd4b39
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47170796"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a>Visual Studio Tools for Docker (Windows で Visual Studio) を使用

Visual Studio Tools for Docker 開発者のワークフローは、Visual Studio Code と Docker CLI を (同じ Docker CLI に基づきます) を使用してに似ています。 Visual Studio Tools の Docker を開始するのにはいっそう簡単に、プロセスを簡略化され、ビルドで生産性の向上が提供、実行、およびタスクを構成します。 実行し、デバッグのような単純なアクションを使用して、コンテナー **F5**と**Ctrl**+**F5**します。

> [!NOTE]
> この記事は、Windows 上の Visual Studio と Visual Studio for mac。

## <a name="configure-your-local-environment"></a>ローカル環境を構成します。

Docker for Windows の最新バージョン ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/))、簡単なセットアップでは、Docker アプリケーションの開発が容易にします。

Visual Studio 2017 では、docker のサポートが含まれます。 ここで Visual Studio 2017 をダウンロードします。 [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)

## <a name="use-docker-tools-in-visual-studio-2017"></a>Visual Studio 2017 での Docker ツールを使用します。

Docker のサポートをプロジェクトに追加することの 2 つのレベルがあります。 .NET Core web アプリのプロジェクトに追加できます、 *Dockerfile*に Docker サポートを有効にすると、プロジェクト ファイル。 次のレベルはコンテナー オーケストレーター サポートは、追加、 *Dockerfile* (まだ存在しない) 場合は、プロジェクトに、 *docker compose.yml*ソリューション レベルでのファイル。

**追加** > **Docker サポート**と**追加** > **コンテナー オーケストレーター サポート**コマンドは、web アプリ プロジェクトのプロジェクト ノードの右クリック メニュー (またはコンテキスト メニュー) にある**ソリューション エクスプ ローラー**図 4-26 に示すようにします。

![Visual Studio での Docker サポート メニュー オプションを追加します。](media/add-docker-support-menu.png)

図 4-26: Visual Studio 2017 のプロジェクトに Docker サポートを追加します。

### <a name="add-docker-support"></a>Docker サポートを追加します。

選択して、既存の .NET Core web アプリ プロジェクトに Docker サポートを追加する**追加** > **Docker サポート**で**ソリューション エクスプ ローラー**します。 選択して、プロジェクトの作成時に Docker サポートを有効することも**Docker サポートを有効にする**で、**新しい ASP.NET Core Web アプリケーション**クリックした後に表示されたダイアログ ボックス**ok**で、**新しいプロジェクト** ダイアログ ボックスで、図 4-27 に示すようにします。

![Visual Studio での新しい ASP.NET Core web アプリの Docker サポートを有効にします。](./media/enable-docker-support-visual-studio.png)

図 4-27: Visual Studio 2017 でプロジェクトの作成時に Docker サポートを有効にします。

Docker サポートを有効にすると、Visual Studio の追加、 *Dockerfile*ファイルをプロジェクトにします。

> [!NOTE]
> 図 4-28 に示すように .NET Framework web アプリ プロジェクト (いない .NET Core web アプリのプロジェクト) のプロジェクトの作成時に Docker Compose のサポートが有効、コンテナー オーケストレーター サポートも追加されます。
>
> ![Docker を有効にする .NET Framework web アプリ プロジェクトのサポートの構成](media/enable-docker-compose-support.png)

> 図 4-28: Visual Studio 2017 で .NET Framework web アプリ プロジェクトでの Docker Compose のサポートを有効にします。

### <a name="add-container-orchestrator-support"></a>コンテナー オーケストレーター サポートを追加します。

複数のコンテナー ソリューションを作成する場合は、コンテナー オーケストレーター サポートをプロジェクトに追加します。 コンテナー オーケストレーター サポートを追加すると Visual Studio が追加されます、 *Dockerfile* (まだ存在しない) 場合は、プロジェクトと、グローバルに*docker compose.yml*ソリューション レベルでのファイル。 これにより、実行およびで同じ定義している場合、コンテナー (ソリューション全体) のグループを同時にデバッグ*docker compose.yml*ファイル。 場合*docker compose.yml*が既に存在する Visual Studio に必要な構成コードの行を追加するだけです。

プロジェクトに追加の Dockerfile を参照してくださいコンテナー オーケストレーションのサポートをプロジェクトに追加した後、 **docker compose**でソリューションに追加されたフォルダー**ソリューション エクスプ ローラー**図 4-29 に示すように。

![Visual Studio でソリューション エクスプ ローラーでの docker ファイル](media/docker-support-solution-explorer.png)

Visual Studio 2017 でのソリューション エクスプ ローラーで、図 4-29: Docker ファイル

**詳細については:** サービスの実装と Visual Studio tools for Docker の使用の詳細については、次の記事を参照します。

ビルド、デバッグ、更新、およびローカル Docker コンテナーでアプリを更新します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)

コンテナー レジストリには、ASP.NET Core の Docker コンテナーを展開します。 [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)

>[!div class="step-by-step"]
[前へ](docker-apps-inner-loop-workflow.md)
[次へ](set-up-windows-containers-with-powershell.md)