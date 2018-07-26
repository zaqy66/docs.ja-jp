---
title: F# のインストールします。
description: お客様の環境に基づいて、f# をインストールする方法について説明します。
ms.date: 07/03/2018
ms.openlocfilehash: 142265a95e1d3ee1603a89f650a24c6a45709181
ms.sourcegitcommit: 59b51cd7c95c75be85bd6ef715e9ef8c85720bac
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2018
ms.locfileid: "37878847"
---
# <a name="install-f"></a>F# のインストールします。 #

複数の方法で f# をインストールと、環境に応じてことができます。

## <a name="install-f-with-visual-studio"></a>Visual Studio を使用した f# のインストールします。

ダウンロードしている場合[Visual Studio](https://visualstudio.microsoft.com/)最初に、これは最初にインストール、Visual Studio インストーラー。 インストーラーから、適切な SKU の Visual Studio をインストールします。 既にインストールされていること、クリックして**変更**します。

次のワークロードの一覧を確認します。 選択**ASP.NET および web 開発**、のど f# サポート、.NET Core のサポートをインストールして、プロジェクトの f# ASP.NET Core のサポート。

次に、クリックして**変更**下部右側にあります。  これは、選択したすべてのものにインストールされます。 クリックして、f# 言語サポートと Visual Studio 2017 を開くことができますし、**起動**します。

## <a name="install-f-with-visual-studio-for-mac"></a>F# で Visual Studio for Mac をインストールします。

既定で f# がインストールされている[Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/)、選択したどのような構成です。

インストールが完了した後は、"Visual Studio を起動する"を選択します。 起動してもかまいませんが Finder を macOS でします。

## <a name="install-f-with-visual-studio-code"></a>Visual Studio Code で f# のインストールします。

必要があります[git がインストールされている](https://git-scm.com/download)と、パスにするに収録 ionide の概要でのプロジェクト テンプレートの使用します。 」と入力して正しくインストールされていることを確認する`git --version`キーを押して、コマンド プロンプトで**Enter**します。

### <a name="macostabmacos"></a>[macOS](#tab/macos)

Ionide の概要を使用して[Mono](http://www.mono-project.com)します。 MacOS で Mono をインストールする最も簡単な方法は、Homebrew を使用してです。 単に、ターミナルに、次を入力します。

```console
brew install mono
```

インストールする必要がありますも、 [.NET Core SDK](https://www.microsoft.com/net/download)します。

### <a name="linuxtablinux"></a>[Linux](#tab/linux)

Linux では、ionide の概要も使用して[Mono](https://www.mono-project.com)します。 Debian または Ubuntu の場合は、次を使用できます。

```console
sudo apt-get update
sudo apt-get install mono-complete fsharp
```

インストールする必要がありますも、 [.NET Core SDK](https://www.microsoft.com/net/download)します。

### <a name="windowstabwindows"></a>[Windows](#tab/windows)

Windows の場合は、まず[f# サポートを含む Visual Studio をインストール](#install-f-with-visual-studio)します。 これにより、書き込み、コンパイル、および f# コードの実行に必要なすべてのコンポーネントがインストールされます。

インストールする必要がありますも、 [.NET Core SDK](https://www.microsoft.com/net/download/)します。

---

その後[Visual Studio Code](https://code.visualstudio.com)をインストールします。

次に、「ionide の概要」の検索と拡張機能アイコンをクリックします。

Visual Studio Code での f# サポートが必要な唯一のプラグイン[ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp)します。 ただし、インストールすることも[Ionide フェイク](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-FAKE)を取得する[フェイク](https://fsharp.github.io/FAKE/)サポートと[Ionide パケット](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-Paket)を取得する[パケットを作成](https://fsprojects.github.io/Paket/)をサポートします。 偽の追加 f# コミュニティのツールをプロジェクトのビルドとの依存関係をそれぞれ管理は、パケットを作成します。