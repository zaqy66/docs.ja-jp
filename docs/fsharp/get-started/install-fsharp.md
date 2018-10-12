---
title: F# のインストールします。
description: お客様の環境に基づいて、f# をインストールする方法について説明します。
ms.date: 08/28/2018
ms.openlocfilehash: 909e1c07ff7f6d52db77a987639d1c749146fdca
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2018
ms.locfileid: "49120935"
---
# <a name="install-f"></a>F# のインストールします。 #

複数の方法で f# をインストールと、環境に応じてことができます。

## <a name="install-f-with-visual-studio"></a>Visual Studio を使用した f# のインストールします。

ダウンロードしている場合[Visual Studio](https://visualstudio.microsoft.com/)最初に、これは最初にインストール、Visual Studio インストーラー。 インストーラーから、適切な SKU の Visual Studio をインストールします。 既にインストールされていること、クリックして**変更**します。

次のワークロードの一覧を確認します。 選択**ASP.NET および web 開発**f# サポートおよび ASP.NET Core プロジェクトの .NET Core のサポートがインストールされます。

次に、クリックして**変更**下部右側にあります。  これは、選択したすべてのものにインストールされます。 クリックして、f# 言語サポートと Visual Studio 2017 を開くことができますし、**起動**します。

## <a name="install-f-with-visual-studio-for-mac"></a>F# で Visual Studio for Mac をインストールします。

既定で f# がインストールされている[Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/)、選択した構成に関係なく。

インストールが完了した後は、"Visual Studio を起動する"を選択します。 起動してもかまいませんが Finder を macOS でします。

## <a name="install-f-with-visual-studio-code"></a>Visual Studio Code で f# のインストールします。

必要があります[git がインストールされている](https://git-scm.com/download)を PATH にで使用可能なプロジェクト テンプレートの使用します。 」と入力して正しくインストールされていることを確認する`git --version`キーを押して、コマンド プロンプトで**Enter**します。

### <a name="macostabmacos"></a>[macOS](#tab/macos)

[Mono](http://www.mono-project.com)使用[f# Interactive](../tutorials/fsharp-interactive/index.md)をサポートします。 MacOS で Mono をインストールする最も簡単な方法は、Homebrew を使用してです。 単に、ターミナルに、次を入力します。

```console
brew install mono
```

インストールことも、 [.NET Core SDK](https://www.microsoft.com/net/download)します。

### <a name="linuxtablinux"></a>[Linux](#tab/linux)

[Mono](https://www.mono-project.com)使用[f# Interactive](../tutorials/fsharp-interactive/index.md)をサポートします。 Debian または Ubuntu の場合は、次を使用できます。

```console
sudo apt-get update
sudo apt-get install mono-complete fsharp
```

インストールことも、 [.NET Core SDK](https://www.microsoft.com/net/download)します。

### <a name="windowstabwindows"></a>[Windows](#tab/windows)

インストール[f# のサポートを使用した Visual Studio](#install-f-with-visual-studio)します。 これにより、書き込み、コンパイル、および f# コードの実行に必要なすべてのコンポーネントがインストールされます。

インストールことも、 [.NET Core SDK](https://www.microsoft.com/net/download/)します。

---

その後[Visual Studio Code](https://code.visualstudio.com)をインストールします。

次に、「ionide の概要」の検索と拡張機能アイコンをクリックします。

Visual Studio Code での f# サポートが必要な唯一のプラグイン[ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp)します。 ただし、インストールすることも[Ionide フェイク](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-FAKE)を取得する[フェイク](https://fsharp.github.io/FAKE/)サポートと[Ionide パケット](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-Paket)を取得する[パケットを作成](https://fsprojects.github.io/Paket/)をサポートします。 偽の追加 f# コミュニティのツールをプロジェクトのビルドとの依存関係をそれぞれ管理は、パケットを作成します。
