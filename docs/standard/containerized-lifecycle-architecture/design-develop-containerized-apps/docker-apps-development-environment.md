---
title: Docker アプリの開発環境
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 471b52fd577e5560bd93e6da50f2032d63eb2e6f
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152417"
---
# <a name="development-environment-for-docker-apps"></a>Docker アプリの開発環境

## <a name="development-tools-choices-ide-or-editor"></a>開発ツールの選択。IDE またはエディター

いたとしてもする場合、完全で強力な IDE または軽量でアジャイルなエディターでは、マイクロソフトは、Docker アプリケーションの開発なったときに対応しています。

### <a name="visual-studio-code-and-docker-cli-cross-platform-tools-for-mac-linux-and-windows"></a>Visual Studio Code と Docker CLI (Mac、Linux、および Windows 用のクロス プラットフォーム ツール)

軽量でクロスプラット フォーム対応のエディターが任意の開発言語をサポートしている場合は、Visual Studio Code と Docker CLI を使用することができます。 これらの製品では、開発者のワークフローを合理化するための重要なは、簡単かつ堅牢のエクスペリエンスを提供します。 "Docker for Mac"または"Docker for Windows"(開発環境) をインストールすると、Docker 開発者は、Windows または Linux (ランタイム環境) の両方のアプリを構築するのに 1 つの Docker CLI を使用できます。 さらに、Visual Studio Code エディターから Docker コマンドを実行するには、Dockerfile とショートカット タスク用の IntelliSense での Docker の拡張機能をサポートしています。

> [!NOTE]
> Visual Studio Code をダウンロードするには<https://code.visualstudio.com/download>します。

Mac および Windows 用 Docker をダウンロードするには<https://www.docker.com/products/docker>します。

### <a name="visual-studio-with-docker-tools"></a>Visual Studio と Docker ツール

Visual Studio 2015 を使用しているときに、「Visual Studio 用 Docker ツールです」アドオン ツールをインストールすることができます。 Visual Studio 2017 での Docker ツール組み込まで既にします。 どちらの場合も開発、実行、および選択した Docker 環境で直接アプリケーションを検証することができます。 F5 キーを Docker に直接アプリケーション (1 つのコンテナーまたは複数のコンテナー) は、デバッグとホストまたはを編集して、コンテナーを再構築しなくても、アプリを更新するには、Ctrl + F5 キーを押します。 これは、Linux または Windows の Docker コンテナーを作成する Windows 開発者にとって最も簡単でより強力な選択肢です。

> [!NOTE]
> Visual Studio 用 Docker ツールをダウンロードするには<https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>します。

## <a name="language-and-framework-choices"></a>言語とフレームワークの選択

Docker アプリケーションと最新の言語でマイクロソフトのツールを開発することができます。 次に、最初のリストが、これに限定されません。

-   .NET Core および ASP.NET Core
-   Node.js
-   Golang
-   Java
-   Ruby
-   Python

基本的には、Linux または Windows で Docker でサポートされている最新の言語を使用することができます。

>[!div class="step-by-step"]
>[前へ](orchestrate-high-scalability-availability.md)
>[次へ](docker-apps-inner-loop-workflow.md)