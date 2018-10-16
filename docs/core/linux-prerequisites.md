---
title: Linux における .NET Core の前提条件
description: Linux マシンで .NET Core アプリケーションを開発、展開、および実行するために必要なサポートされている Linux のバージョンと .NET Core の依存関係。
author: jralexander
ms.author: johalex
ms.date: 08/20/2018
ms.openlocfilehash: d0e5b203dc8e1ec6807f28de7d910c74a2ffe665
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43506850"
---
# <a name="prerequisites-for-net-core-on-linux"></a>Linux における .NET Core の前提条件

この記事では、Linux で .NET Core アプリケーションを開発するために必要な依存関係を示します。 後述のサポートされている Linux ディストリビューション/バージョンと依存関係は、Linux で .NET Core アプリを開発する次の 2 つの方法に適用されます。

* [好みのエディターでのコマンドライン](tutorials/using-with-xplat-cli.md)
* [Visual Studio Code](https://code.visualstudio.com/)

> [!NOTE]
> .NET Core SDK パッケージは、運用サーバー/環境には必要はありません。 運用環境に展開されるアプリに必要なものは、.NET Core ランタイム パッケージだけです。 .NET Core ランタイムは自己完結型の展開の一部としてアプリと供に展開されますが、フレームワークに依存して展開されるアプリでは個別に展開する必要があります。 フレームワークに依存する展開と自己完結型の展開について詳しくは、「[.NET Core アプリケーションの展開](./deploying/index.md)」をご覧ください。 具体的なガイドラインについては、「[Self-contained Linux applications](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md)」(自己完結型 Linux アプリケーション) もご覧ください。

## <a name="supported-linux-versions"></a>サポートされている Linux バージョン

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

.NET Core 2.x は、1 つのオペレーティング システムとして Linux を扱います。 サポートされている Linux ディストリビューション用に、1 つの Linux ビルド (チップ アーキテクチャあたり) があります。

**NET Core 2.1**

NET Core 2.1 は、次の Linux ディストリビューション/バージョンでサポートされています。

* Red Hat Enterprise Linux 7、6 - 64 ビット (`x86_64` または `amd64`)
* CentOS 7 - 64 ビット (`x86_64` または `amd64`) 
* Oracle Linux 7 - 64 ビット (`x86_64` または `amd64`) 
* Fedora 28、27 - 64 ビット (`x86_64` または `amd64`) 
* Debian 9 (64 ビット、ARM32)、8.7 以降のバージョン - 64 ビット (`x86_64` または `amd64`)
* Ubuntu 18.04 (64 ビット、ARM32)、16.04、14.04 - 64 ビット (`x86_64` または `amd64`)
* Linux Mint 18、17 - 64 ビット (`x86_64` または `amd64`)
* openSUSE 42.3 以降のバージョン - 64 ビット (`x86_64` または `amd64`)
* SUSE Enterprise Linux (SLES) 12 Service Pack 2 以降 - 64 ビット (`x86_64` または `amd64`)
* Alpine Linux 3.7 以降のバージョン - 64 ビット (`x86_64` または `amd64`)

.NET Core 2.1 でサポートされているオペレーティング システム、ディストリビューション、バージョン、サポートされていない OS バージョン、ライフサイクル ポリシー リンクの完全なリストについては、[.NET Core 2.1 がサポートされる OS バージョン](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md)に関するページを参照してください。

**NET Core 2.0**

NET Core 2.0 は、次の Linux 64 ビット (`x86_64` または `amd64`) ディストリビューション/バージョンでサポートされています。

* Red Hat Enterprise Linux 7、6
* CentOS 7
* Oracle Linux 7
* Fedora 27
* Debian 9、8.7 以降のバージョン
* Ubuntu 18.04、16.04、14.04
* Linux Mint 18、17
* openSUSE 42.3 以降のバージョン
* SUSE Enterprise Linux (SLES) 12 Service Pack 2 以降

.NET Core 2.0 でサポートされているオペレーティング システム、ディストリビューション、バージョン、サポートされていない OS バージョン、ライフサイクル ポリシー リンクの完全なリストについては、[.NET Core 2.0 がサポートされる OS バージョン](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md)に関するページを参照してください。

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

.NET Core 1.x は、次の Linux 64 ビット (`x86_64` または `amd64`) ディストリビューション/バージョンでサポートされています。

* Red Hat Enterprise Linux 7
* CentOS 7
* Oracle Linux 7
* Fedora 28 (.NET Core 1.1)、27
* Debian 8.2 以降のバージョン
* Ubuntu 18.04 (.NET Core 1.1)、16.04、14.04
* Linux Mint 17
* openSUSE 42.3 以降のバージョン (.NET Core 1.1)

.NET Core 1.x がサポートされているオペレーティング システム (サポートされている OS バージョン以外) の完全なリスト、およびライフサイクル ポリシーのリンクについては、「[.NET Core 1.x Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md)」 (.NET Core 1.x がサポートされる OS のバージョン) を参照してください。

---

## <a name="linux-distribution-dependencies"></a>Linux ディストリビューションの依存関係

次に例を示します。 選択した Linux ディストリビューションで、バージョンと名前が多少異なる場合があります。

### <a name="ubuntu"></a>Ubuntu

Ubuntu ディストリビューションには、次のライブラリがインストールされている必要があります。

* liblttng-ust0
* libcurl3
* libssl1.0.0
* libkrb5-3
* zlib1g
* libicu52 (14.x 用)
* libicu55 (16.x 用)
* libicu57 (17.x 用)
* libicu60 (18.x 用)

.NET Core 2.1 より前のバージョンには、次の依存関係も必要です。

* libunwind8
* libuuid1

### <a name="centos-and-fedora"></a>CentOS と Fedora

CentOS ディストリビューションには、次のライブラリがインストールされている必要があります。

* lttng-ust
* libcurl
* openssl-libs
* krb5-libs
* libicu
* zlib

Fedora ユーザー: ご使用の openssl のバージョンが 1.1 以降の場合は、compat-openssl10 をインストールする必要があります。

.NET Core 2.1 より前のバージョンには、次の依存関係も必要です。

* libunwind
* libuuid

依存関係の詳細については、「[Self-contained Linux applications (自己完結型 Linux アプリケーション)](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md)」をご覧ください。

## <a name="installing-net-core-dependencies-with-the-native-installers"></a>ネイティブ インストーラーを使用した .NET Core の依存関係のインストール

.NET Core ネイティブ インストーラーは、サポートされている Linux ディストリビューション/バージョンに利用できます。 このネイティブ インストーラーは、サーバーへの admin (sudo) アクセスを必要とします。 ネイティブ インストーラーを使用することの利点は、.NET Core ネイティブの依存関係がすべてインストールされることです。 また、ネイティブ インストーラーでは、.NET Core SDK もシステム全体にインストールします。

Linux では、2 つのインストーラー パッケージから選択できます。

* フィードベースのパッケージ マネージャー (Ubuntu では apt-get、CentOS/RHEL では yum など) を使用する
* パッケージ自体 (DEB または RPM) を使用する

### <a name="scripting-installs-with-the-net-core-installer-script"></a>.NET Core インストーラー スクリプトを使用したスクリプトのインストール

[dotnet-install スクリプト](./tools/dotnet-install-script.md)は、CLI ツールチェーンと共有ランタイムの非管理者インストールを実行するために使用されます。 このスクリプトは [https://dot.net/v1/dotnet-install.sh](https://dot.net/v1/dotnet-install.sh) からダウンロードできます。

スクリプトは、既定で最新の "LTS" のバージョン (現在は .NET Core 1.1) をインストールします。 NET Core 2.x をインストールするには、次のスイッチを使用してスクリプトを実行します。

```console
./dotnet-install.sh -c Current
```

インストーラーの bash スクリプトは、自動化シナリオと管理者以外のインストールで使用されます。 このスクリプトは、PowerShell のスイッチも読み取るので、Linux/OS X システムのスクリプトで使うことができます。

## <a name="install-net-core-for-supported-red-hat-enterprise-linux-rhel-versions"></a>サポートされている Red Hat Enterprise Linux (RHEL) 用の .NET Core をインストールする

.NET Core をサポートされている RHEL のバージョンにインストールするには:

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

**.NET Core 2.1**

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. Red Hat Enterprise Linux インストール情報での最新の .NET Core 2.1 については、[.NET Core 2.1 の使用開始ガイド](https://access.redhat.com/documentation/en-us/net_core/2.1/html/getting_started_guide/)をご覧ください

**.NET Core 2.0**

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. Red Hat Enterprise Linux インストール情報での最新の .NET Core 2.0 については、[.NET Core 2.0 の使用開始ガイド](https://access.redhat.com/documentation/en-us/net_core/2.0/html/getting_started_guide/)をご覧ください 

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

**.NET Core 1.1**

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2.  Red Hat Enterprise Linux インストール情報での最新の .NET Core 1.1 については、[.NET Core 1.1 の使用開始ガイド](https://access.redhat.com/documentation/en-us/net_core/1.1/html/getting_started_guide/)をご覧ください
     
**.NET Core 1.0**

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2.  Red Hat Enterprise Linux インストール情報での最新の .NET Core 1.0 については、[.NET Core 1.0 の使用開始ガイド](https://access.redhat.com/documentation/en-us/net_core/1.0/html/getting_started_guide/)をご覧ください

Red Hat .NET チャネル アクセスの登録に関するヘルプについては、Red Hat の「[Chapter 1 of the .NET Core 1.1 Getting Started Guide](https://access.redhat.com/documentation/en/net-core/1.1/paged/getting-started-guide/)」 (.NET Core 1.1 ファースト ステップ ガイドの第 1 章) を参照してください。

---

## <a name="install-net-core-for-supported-ubuntu-and-linux-mint-distributionsversions-64-bit"></a>サポートされている Ubuntu および Linux Mint のディストリビューション/バージョン (64 ビット) 用の .NET Core をインストールする

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. サポートされている Ubuntu および Linux Mint のディストリビューション/バージョン (64 ビット) に .NET Core 2.x をインストールします。

**.NET Core 2.0**

|ランタイム/SDK          |Ubuntu 18.04    |Ubuntu 17.10    |Ubuntu 16.04 / Linux Mint 18|Ubuntu 14.04 / Linux Mint 17|
|-------------------------|----------------|----------------|----------------------------|----------------------------|
|.NET Core ランタイム 2.0.9  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.0.9)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.0.9)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.0.9)          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.0.9)            |
|.NET Core ランタイム 2.0.8  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.0.8)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.0.8)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.0.8)          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.0.8)            |
|.NET Core ランタイム 2.0.7  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.0.7)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.0.7)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.0.7)          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.0.7)            |
|.NET Core ランタイム 2.0.6  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.0.6)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.0.6)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.0.6)          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.0.6)            |
|.NET Core ランタイム 2.0.5  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.0.5)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.0.5)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.0.5)          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.0.5)            |
|.NET Core SDK 2.1.202    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.202)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.202)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.202)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.202)            |
|.NET Core SDK 2.1.201    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.201)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.201)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.201)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.201)            |
|.NET Core SDK 2.1.200    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.200)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.200)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.200)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.200)            |
|.NET Core SDK 2.1.105    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.105)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.105)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.105)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.105)            |
|.NET Core SDK 2.1.103    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.103)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.103)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.103)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.103)            |
|.NET Core SDK 2.0.3      |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.0.3)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.0.3)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.0.3)          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.0.3)            |
|.NET Core SDK 2.0.0      |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.0.0)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.0.0)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.0.0)          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.0.0)            |

**.NET Core 2.1**

>[!IMPORTANT]
> Visual Studio で .NET Core 2.1 を使用するには、[Visual Studio 2017 15.7 以降をインストールする](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)必要があります。

|ランタイム/SDK          |Ubuntu 18.04    |Ubuntu 17.10    |Ubuntu 16.04 / Linux Mint 18|Ubuntu 14.04 / Linux Mint 17|
|-------------------------|----------------|----------------|----------------------------|----------------------------|
|.NET Core ランタイム 2.1.2          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.1.2)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.1.2)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.1.2)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.1.2)            |
|.NET Core SDK 2.1.400     |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.400)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.400)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.400)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.400)            |
|.NET Core SDK 2.1.302     |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.302)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.302)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.302)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.302)            |
|.NET Core ランタイム 2.1.1          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.1.1)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.1.1)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.1.1)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.1.1)            |
|.NET Core SDK 2.1.301     |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.301)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.301)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.301)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.301)            |
|.NET Core ランタイム 2.1.0          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.1.0)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.1.0)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.1.0)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.1.0)            |
|.NET Core SDK 2.1.300     |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.300)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.300)|[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.300)            |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.300)            |

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. サポートされている Ubuntu および Linux Mint のディストリビューション/バージョン (64 ビット) に .NET Core 1.x をインストールします。

| ランタイム/SDK         |Ubuntu 16.04 / Linux Mint 18|Ubuntu 14.04 / Linux Mint 17|
|-------------------------|----------------------------|----------------------------|
|.NET Core ランタイム 1.1.9  |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.9-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.8-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core ランタイム 1.1.8  |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core ランタイム 1.1.7  |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core ランタイム 1.1.6  |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core ランタイム 1.1.5  |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.5-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.5-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core ランタイム 1.1.4  |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core ランタイム 1.0.10 |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.10-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.10-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core ランタイム 1.0.9  |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.9-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.9-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core ランタイム 1.0.8  |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.8-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.8-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core ランタイム 1.0.7  |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.7-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.7-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core ランタイム 1.0.5  |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.5-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.5-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core ランタイム 1.0.4  |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.4-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.4-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core SDK 1.1.10     |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.10-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.10-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core SDK 1.1.9      |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.9-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.9-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core SDK 1.1.8      |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.8-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.8-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core SDK 1.1.7      |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core SDK 1.1.5      |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core SDK 1.1.4      |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.4-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.4-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core SDK 1.0.4      |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-ubuntu-14.04-x64-binaries)            |
|.NET Core SDK 1.0.1      |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-ubuntu-16.04-x64-binaries)            |[インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-ubuntu-14.04-x64-binaries)            |

---

## <a name="install-net-core-for-supported-debian-versions-64-bit"></a>サポートされている Debian のバージョン (64 ビット) 用の .NET Core をインストールする

サポートされている Debian のバージョン (64 ビット) に .NET Core をインストールするには:

> [!NOTE]
> tar.gz から Linux システムをインストールするには、ユーザー指定のディレクトリが必要です。

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. サポートされている Debian のバージョン (64 ビット) に .NET Core 2.x をインストールします。

**.NET Core 2.0**

|ランタイム/SDK          |Debian 9       |Debian 8       |
|-------------------------|---------------|---------------|
|.NET Core ランタイム 2.0.9  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.9)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.9)   |
|.NET Core ランタイム 2.0.8  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.8)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.8)   |
|.NET Core ランタイム 2.0.7  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.7)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.7)   |
|.NET Core ランタイム 2.0.6  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.6)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.6)   |
|.NET Core ランタイム 2.0.5  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.5)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.5)   |
|.NET Core ランタイム 2.0.3  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.3)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.3)   |
|.NET Core ランタイム 2.0.0  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.0)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.0)   |
|.NET Core SDK 2.1.202    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.202)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.202)   |
|.NET Core SDK 2.1.201    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.201)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.201)   |
|.NET Core SDK 2.1.200    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.200)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.200)   |
|.NET Core SDK 2.1.105    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.105)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.105)   |
|.NET Core SDK 2.1.105    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.105)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.105)   |
|.NET Core SDK 2.1.104    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.104)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.104)   |
|.NET Core SDK 2.1.103    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.103)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.103)   |
|.NET Core SDK 2.1.102    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.102)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.102)   |
|.NET Core SDK 2.1.101    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.101)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.101)   |
|.NET Core SDK 2.0.3      |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.0.3)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.0.3)   |
|.NET Core SDK 2.0.0      |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.0.0)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.0.0)   |

**.NET Core 2.1**

>[!IMPORTANT]
> Visual Studio で .NET Core 2.1 を使用するには、[Visual Studio 2017 15.7 以降をインストールする](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)必要があります。

|ランタイム/SDK                  |Debian 9       |Debian 8       |
|---------------------------------|---------------|---------------|
|.NET Core ランタイム 2.1.2          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.1.2)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.1.2)   |
|.NET Core SDK 2.1.400        |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.400)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.400)        |
|.NET Core SDK 2.1.302        |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.302)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.302)        |
|.NET Core ランタイム 2.1.1          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.1.1)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.1.1)   |
|.NET Core SDK 2.1.301        |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.301)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.301)        |
|.NET Core ランタイム 2.1.0          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.1.0)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.1.0)   |
|.NET Core SDK 2.1.300        |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.300)   |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.300)        |

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. Debian 9 または Debian 8 に .NET Core 1.x をインストールします。

* .NET Core ランタイム 1.1.9 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.9-linux-debian-x64-binaries)
* .NET Core ランタイム 1.1.8 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.8-linux-debian-x64-binaries)
* .NET Core ランタイム 1.1.7 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-debian-x64-binaries)
* .NET Core ランタイム 1.1.6 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-debian-x64-binaries)
* .NET Core ランタイム 1.1.5 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.5-linux-debian-x64-binaries)
* .NET Core ランタイム 1.1.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-debian-x64-binaries)
* .NET Core ランタイム 1.1.2 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.2-linux-debian-x64-binaries)
* .NET Core ランタイム 1.1.1 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.1-linux-debian-x64-binaries)
* .NET Core ランタイム 1.1.0 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.0-linux-debian-x64-binaries)
* .NET Core ランタイム 1.0.10 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.10-linux-debian-x64-binaries)
* .NET Core ランタイム 1.0.9 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.9-linux-debian-x64-binaries)
* .NET Core ランタイム 1.0.8 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.8-linux-debian-x64-binaries)
* .NET Core ランタイム 1.0.7 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.7-linux-debian-x64-binaries)
* .NET Core ランタイム 1.0.5 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.5-linux-debian-x64-binaries)
* .NET Core ランタイム 1.0.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.4-linux-debian-x64-binaries)
* .NET Core SDK 1.1.10 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.10-linux-debian-x64-binaries)
* .NET Core SDK 1.1.9 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.9-linux-debian-x64-binaries)
* .NET Core SDK 1.1.8 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.8-linux-debian-x64-binaries)
* .NET Core SDK 1.1.7 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-debian-x64-binaries)
* .NET Core SDK 1.1.5 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5-linux-debian-x64-binaries)
* .NET Core SDK 1.1.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.4-linux-debian-x64-binaries)
* .NET Core SDK 1.0.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-debian-x64-binaries)
* .NET Core SDK 1.0.1 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-debian-x64-binaries)

---

## <a name="install-net-core-for-supported-fedora-versions-64-bit"></a>サポートされている Fedora のバージョン (64 ビット) 用の .NET Core をインストールする

サポートされている Fedora のバージョンに .NET Core をインストールするには:

> [!NOTE]
> tar.gz から Linux システムをインストールするには、ユーザー指定のディレクトリが必要です。

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. サポートされている Fedora のバージョン (64 ビット) に .NET Core 2.x をインストールします。

**.NET Core 2.0**

|ランタイム/SDK          |Fedora 26 以降 |Fedora 25 以前 |
|-------------------------|-------------------|----------------------|
|.NET Core ランタイム 2.0.9  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.9)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.9)           |
|.NET Core ランタイム 2.0.8  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.8)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.8)           |
|.NET Core ランタイム 2.0.7  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.7)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.7)           |
|.NET Core ランタイム 2.0.6  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.6)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.6)           |
|.NET Core ランタイム 2.0.5  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.5)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.5)           |
|.NET Core ランタイム 2.0.3  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.3)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.3)           |
|.NET Core ランタイム 2.0.0  |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.0)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.0)           |
|.NET Core SDK 2.1.200    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora26/sdk-2.1.200)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora25/sdk-2.1.200)           |
|.NET Core SDK 2.1.105    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora26/sdk-2.1.105)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora25/sdk-2.1.105)           |
|.NET Core SDK 2.1.103    |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora26/sdk-2.1.103)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora25/sdk-2.1.103)           |
|.NET Core SDK 2.0.3      |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora26/sdk-2.0.3)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora25/sdk-2.0.3)           |

**.NET Core 2.1**

>[!IMPORTANT]
> Visual Studio で .NET Core 2.1 を使用するには、[Visual Studio 2017 15.7 以降をインストールする](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)必要があります。

|ランタイム/SDK                  |Fedora 28          |Fedora 27             |
|---------------------------------|-------------------|----------------------|
|.NET Core ランタイム 2.1.2          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora28/runtime-2.1.2)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora27/runtime-2.1.2)           |
|.NET Core SDK 2.1.400          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora28/sdk-2.1.400)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora27/sdk-2.1.400)           |
|.NET Core SDK 2.1.302          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora28/sdk-2.1.302)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora27/sdk-2.1.302)           |
|.NET Core ランタイム 2.1.1          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora28/runtime-2.1.1)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora27/runtime-2.1.1)           |
|.NET Core SDK 2.1.301          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora28/sdk-2.1.301)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora27/sdk-2.1.301)           |
|.NET Core ランタイム 2.1.0          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora28/runtime-2.1.0)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora27/runtime-2.1.0)           |
|.NET Core SDK 2.1.300          |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora28/sdk-2.1.300)       |[インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/fedora27/sdk-2.1.300)           |

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. サポートされている Fedora のバージョン (64 ビット) に .NET Core 1.x をインストールします。

**Fedora 24**

* .NET Core ランタイム 1.1.8 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.8-linux-fedora-24-x64-binaries)
* .NET Core ランタイム 1.1.7 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-fedora-24-x64-binaries)
* .NET Core ランタイム 1.1.6 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-fedora-24-x64-binaries)
* .NET Core ランタイム 1.1.5 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.5-linux-fedora-24-x64-binaries)
* .NET Core ランタイム 1.1.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-fedora-24-x64-binaries)
* .NET Core ランタイム 1.1.2 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.2-linux-fedora-24-x64-binaries)
* .NET Core ランタイム 1.1.1 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.1-linux-fedora-24-x64-binaries)
* .NET Core SDK 1.1.9 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.9-linux-fedora-24-x64-binaries)
* .NET Core SDK 1.1.8 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.8-linux-fedora-24-x64-binaries)
* .NET Core SDK 1.1.7 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-fedora-24-x64-binaries)
* .NET Core SDK 1.1.5 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5linux-fedora-24-x64-binaries)
* .NET Core SDK 1.1.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5linux-fedora-24-x64-binaries)
* .NET Core SDK 1.0.1 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-debian-x64-binaries)

**Fedora 23**

* .NET Core ランタイム 1.1.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-fedora-23-x64-binaries)
* .NET Core ランタイム 1.1.2 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.2-linux-fedora-23-x64-binaries)
* .NET Core ランタイム 1.1.1 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.1-linux-fedora-23-x64-binaries)
* .NET Core ランタイム 1.0.9 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.9-linux-fedora-23-x64-binaries)
* .NET Core ランタイム 1.0.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.4-linux-fedora-23-x64-binaries)
* .NET Core SDK 1.1.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.4linux-fedora-23-x64-binaries)
* .NET Core SDK 1.1.2 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.2linux-fedora-23-x64-binaries)
* .NET Core SDK 1.1.2 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.2linux-fedora-23-x64-binaries)
* .NET Core SDK 1.0.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-fedora-23-x64-binaries)
* .NET Core SDK 1.0.1 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-fedora-23-x64-binaries)

---

## <a name="install-net-core-for-supported-centos-and-oracle-linux-distributionsversions-64-bit"></a>サポートされている CentOS および Oracle Linux のディストリビューション/バージョン (64 ビット) 用の .NET Core をインストールする

サポートされている CentOS および Oracle Linux のディストリビューション/バージョン (64 ビット) 用の .NET Core をインストールするには:

> [!NOTE]
> tar.gz から Linux システムをインストールするには、ユーザー指定のディレクトリが必要です。

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. サポートされている CentOS および Oracle Linux のディストリビューション/バージョン (64 ビット) に .NET Core 2.x をインストールします。

**.NET Core 2.0**

* .NET Core ランタイム 2.0.9 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.9)
* .NET Core ランタイム 2.0.8 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.8)
* .NET Core ランタイム 2.0.7 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.7)
* .NET Core ランタイム 2.0.6 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.6)
* .NET Core ランタイム 2.0.5 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.5)
* .NET Core ランタイム 2.0.3 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.3)
* .NET Core ランタイム 2.0.0 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.0)
* .NET Core SDK 2.1.202 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.202)
* .NET Core SDK 2.1.201 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.201)
* .NET Core SDK 2.1.200 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.200)
* .NET Core SDK 2.1.105 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.105)
* .NET Core SDK 2.1.104 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.104)
* .NET Core SDK 2.1.103 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.103)
* .NET Core SDK 2.1.102 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.102)
* .NET Core SDK 2.0.3 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.0.3)
* .NET Core SDK 2.0.0 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.0.0)
 
**.NET Core 2.1**

>[!IMPORTANT]
> Visual Studio で .NET Core 2.1 を使用するには、[Visual Studio 2017 15.7 以降をインストールする](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)必要があります。

* .NET Core ランタイム 2.1.2 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.1.2)
* .NET Core SDK 2.1.400 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.400)
* .NET Core SDK 2.1.302 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.302)
* .NET Core ランタイム 2.1.1 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.1.1)
* .NET Core SDK 2.1.301 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.301)
* .NET Core ランタイム 2.1.0 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.1.0)
* .NET Core SDK 2.1.300 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.300)

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. サポートされている CentOS および Oracle Linux のディストリビューション/バージョン (64 ビット) に .NET Core 1.x をインストールします。

* .NET Core ランタイム 1.1.9 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.9-linux-centos-x64-binaries)
* .NET Core ランタイム 1.1.8 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.8-linux-centos-x64-binaries)
* .NET Core ランタイム 1.1.7 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-centos-x64-binaries)
* .NET Core ランタイム 1.1.6 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-centos-x64-binaries)
* .NET Core ランタイム 1.1.5 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.5-linux-centos-x64-binaries)
* .NET Core ランタイム 1.1.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-centos-x64-binaries)
* .NET Core ランタイム 1.1.2 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.2-linux-centos-x64-binaries)
* .NET Core ランタイム 1.1.1 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.1-linux-centos-x64-binaries)
* .NET Core ランタイム 1.0.12 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.12-linux-centos-x64-binaries)
* .NET Core ランタイム 1.0.11 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.11-linux-centos-x64-binaries)
* .NET Core ランタイム 1.0.10 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.10-linux-centos-x64-binaries)
* .NET Core ランタイム 1.0.9 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.9-linux-centos-x64-binaries)
* .NET Core ランタイム 1.0.8 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.8-linux-centos-x64-binaries)
* .NET Core ランタイム 1.0.7 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.7-linux-centos-x64-binaries)
* .NET Core ランタイム 1.0.5 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.5-linux-centos-x64-binaries)
* .NET Core ランタイム 1.0.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.4-linux-centos-x64-binaries)
* .NET Core SDK 1.1.10 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.10-linux-centos-x64-binaries)
* .NET Core SDK 1.1.9 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.9-linux-centos-x64-binaries)
* .NET Core SDK 1.1.8 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.8-linux-centos-x64-binaries)
* .NET Core SDK 1.1.7 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-centos-x64-binaries)
* .NET Core SDK 1.1.5 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5-linux-centos-x64-binaries)
* .NET Core SDK 1.1.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.4-linux-centos-x64-binaries)
* .NET Core SDK 1.0.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-centos-x64-binaries)
* .NET Core SDK 1.0.1 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-centos-x64-binaries)

---

## <a name="install-net-core-for-supported-suse-linux-enterprise-server-and-opensuse-distributionsversions-64-bit"></a>サポートされている SUSE Linux Enterprise Server および OpenSUSE のディストリビューション/バージョン (64 ビット) 用の .NET Core をインストールする

サポートされている SUSE Linux Enterprise Server および OpenSUSE のディストリビューション/バージョン (64 ビット) 用の .NET Core 2.x をインストールするには:

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. サポートされている SUSE Linux Enterprise Server および OpenSUSE のディストリビューション/バージョン (64 ビット) に .NET Core 2.x をインストールします。

**.NET Core 2.0**

**SUSE Linux Enterprise Server**

* .NET Core ランタイム 2.0.9 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.9)
* .NET Core ランタイム 2.0.8 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.8)
* .NET Core ランタイム 2.0.7 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.7)
* .NET Core ランタイム 2.0.6 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.6)
* .NET Core ランタイム 2.0.5 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.5)
* .NET Core ランタイム 2.0.3 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.3)
* .NET Core ランタイム 2.0.0 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.0)
* .NET Core SDK 2.1.202 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.202)
* .NET Core SDK 2.1.201 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.201)
* .NET Core SDK 2.1.200 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.200)
* .NET Core SDK 2.1.105 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.105)
* .NET Core SDK 2.1.104 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.104)
* .NET Core SDK 2.1.103 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.103)
* .NET Core SDK 2.1.102 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.102)
* .NET Core SDK 2.1.101 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.101)
* .NET Core SDK 2.1.100 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.100)
* .NET Core SDK 2.1.4 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.4)
* .NET Core SDK 2.1.2 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.2)
* .NET Core SDK 2.0.3 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.0.3)
* .NET Core SDK 2.0.0 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.0.0)

**openSUSE**

* .NET Core ランタイム 2.0.9 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.9)
* .NET Core ランタイム 2.0.8 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.8)
* .NET Core ランタイム 2.0.7 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.7)
* .NET Core ランタイム 2.0.6 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.6)
* .NET Core ランタイム 2.0.5 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.5)
* .NET Core ランタイム 2.0.3 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.3)
* .NET Core ランタイム 2.0.0 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.0)
* .NET Core SDK 2.1.202 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.202)
* .NET Core SDK 2.1.201 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.201)
* .NET Core SDK 2.1.200 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.200)
* .NET Core SDK 2.1.105 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.105)
* .NET Core SDK 2.1.103 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.103)
* .NET Core SDK 2.1.102 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.102)
* .NET Core SDK 2.1.101 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.101)
* .NET Core SDK 2.1.100 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.100)
* .NET Core SDK 2.1.4 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.4)
* .NET Core SDK 2.1.2 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.2)
* .NET Core SDK 2.0.3 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.0.3)
* .NET Core SDK 2.0.0 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.0.0)
 
**.NET Core 2.1**

>[!IMPORTANT]
> Visual Studio で .NET Core 2.1 を使用するには、[Visual Studio 2017 15.7 以降をインストールする](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)必要があります。

**SUSE Linux Enterprise Server**

* .NET Core ランタイム 2.1.2 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.1.2)
* .NET Core SDK 2.1.400 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.400)
* .NET Core SDK 2.1.302 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.302)
* .NET Core ランタイム 2.1.1 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.1.1)
* .NET Core SDK 2.1.301 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.301)
* .NET Core ランタイム 2.1.0 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.1.0)
* .NET Core SDK 2.1.300 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.300)

**openSUSE**

* .NET Core ランタイム 2.1.2 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.1.2)
* .NET Core SDK 2.1.400 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.400)
* .NET Core SDK 2.1.302 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.302)
* .NET Core ランタイム 2.1.1 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.1.1)
* .NET Core SDK 2.1.301 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.301)
* .NET Core ランタイム 2.1.0 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.1.0)
* .NET Core SDK 2.1.300 [インストール リンク](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.300)

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

1. システムから**以前のプレビュー** バージョンの .NET Core を削除します。

2. サポートされている SUSE Linux Enterprise Server および OpenSUSE のディストリビューション/バージョン (64 ビット) に .NET Core 1.x をインストールします。

**SUSE Linux Enterprise Server 13.2**

* .NET Core ランタイム 1.1.7 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-opensuse-13.2-x64-binaries)
* .NET Core ランタイム 1.1.6 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-opensuse-13.2-x64-binaries)
* .NET Core SDK 1.1.7 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-opensuse-13.2-x64-binaries)
* .NET Core SDK 1.0.4 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-opensuse-13.2-x64-binaries)
* .NET Core SDK 1.0.1 [インストール リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-opensuse-13.2-x64-binaries)

---

## <a name="install-net-core-for-supported-alpine-linux-versions-64-bit"></a>サポートされている Alpine Linux のバージョン (64 ビット) 用の .NET Core をインストールする

> [!NOTE]
> tar.gz から Linux システムをインストールするには、ユーザー指定のディレクトリが必要です。

次のリンクにあるサポートされている Alpine Linux バージョン (64 ビット) 用の .NET Core 2.1 インストール手順をダウンロードして、手順に従います。

* .NET Core ランタイム 2.1.2 [ダウンロード リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-2.1.2-linux-x64-alpine-binaries)
* .NET Core SDK 2.1.400 [ダウンロード リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-2.1.400-linux-x64-alpine-binaries)
* .NET Core SDK 2.1.302 [ダウンロード リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-2.1.302-linux-x64-alpine-binaries)
* .NET Core ランタイム 2.1.1 [ダウンロード リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-2.1.1-linux-x64-alpine-binaries)
* .NET Core SDK 2.1.301 [ダウンロード リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-2.1.301-linux-x64-alpine-binaries)
* .NET Core ランタイム 2.1.0 [ダウンロード リンク](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-2.1.0-linux-x64-alpine-binaries)
* .NET Core SDK 2.1.300 [ダウンロード リンク](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-2.1.300-linux-x64-alpine-binaries)

> [!IMPORTANT]
> サポートされている Linux ディストリビューション/バージョンへの .NET Core のインストールに問題がある場合は、インストールしているディストリビューション/バージョンに関する以下のトピックをご覧ください。
> * [.NET Core 2.1 の既知の問題](https://github.com/dotnet/core/tree/master/release-notes/2.1)
> * [.NET Core 2.0 の既知の問題](https://github.com/dotnet/core/tree/master/release-notes/2.0)
> * [.NET Core 1.1 の既知の問題](https://github.com/dotnet/core/blob/master/release-notes/1.1)
> * [.NET Core 1.0 の既知の問題](https://github.com/dotnet/core/blob/master/release-notes/1.0)
