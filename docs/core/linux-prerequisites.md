---
title: Linux における .NET Core の前提条件
description: Linux マシンで .NET Core アプリケーションを開発、展開、および実行するために必要なサポートされている Linux のバージョンと .NET Core の依存関係。
author: thraka
ms.author: adegeo
ms.date: 12/03/2018
ms.openlocfilehash: e250158d10c6a03535f4e693e74954747f860a3c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53148332"
---
# <a name="prerequisites-for-net-core-on-linux"></a><span data-ttu-id="2ea13-103">Linux における .NET Core の前提条件</span><span class="sxs-lookup"><span data-stu-id="2ea13-103">Prerequisites for .NET Core on Linux</span></span>

<span data-ttu-id="2ea13-104">この記事では、Linux で .NET Core アプリケーションを開発するために必要な依存関係を示します。</span><span class="sxs-lookup"><span data-stu-id="2ea13-104">This article shows the dependencies needed to develop .NET Core applications on Linux.</span></span> <span data-ttu-id="2ea13-105">後述のサポートされている Linux ディストリビューション/バージョンと依存関係は、Linux で .NET Core アプリを開発する次の 2 つの方法に適用されます。</span><span class="sxs-lookup"><span data-stu-id="2ea13-105">The supported Linux distributions/versions, and dependencies that follow apply to the two ways of developing .NET Core apps on Linux:</span></span>

* [<span data-ttu-id="2ea13-106">好みのエディターでのコマンドライン</span><span class="sxs-lookup"><span data-stu-id="2ea13-106">Command-line with your favorite editor</span></span>](tutorials/using-with-xplat-cli.md)
* [<span data-ttu-id="2ea13-107">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="2ea13-107">Visual Studio Code</span></span>](https://code.visualstudio.com/)

> [!NOTE]
> <span data-ttu-id="2ea13-108">.NET Core SDK パッケージは、運用サーバー/環境には必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2ea13-108">The .NET Core SDK package is not required for production servers/environments.</span></span> <span data-ttu-id="2ea13-109">運用環境に展開されるアプリに必要なものは、.NET Core ランタイム パッケージだけです。</span><span class="sxs-lookup"><span data-stu-id="2ea13-109">Only the .NET Core runtime package is needed for apps deployed to production environments.</span></span> <span data-ttu-id="2ea13-110">.NET Core ランタイムは自己完結型の展開の一部としてアプリと供に展開されますが、フレームワークに依存して展開されるアプリでは個別に展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ea13-110">The .NET Core runtime is deployed with apps as part of a self-contained deployment, however, it must be deployed for Framework-dependent deployed apps separately.</span></span> <span data-ttu-id="2ea13-111">フレームワークに依存する展開と自己完結型の展開について詳しくは、「[.NET Core アプリケーションの展開](./deploying/index.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2ea13-111">For more information about framework-dependent and self-contained deployment types, see [.NET Core application deployment](./deploying/index.md).</span></span> <span data-ttu-id="2ea13-112">具体的なガイドラインについては、「[Self-contained Linux applications](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md)」(自己完結型 Linux アプリケーション) もご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2ea13-112">Also see [Self-contained Linux applications](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md) for specific guidelines.</span></span>

## <a name="supported-linux-versions"></a><span data-ttu-id="2ea13-113">サポートされている Linux バージョン</span><span class="sxs-lookup"><span data-stu-id="2ea13-113">Supported Linux versions</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="2ea13-114">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="2ea13-114">.NET Core 2.x</span></span>](#tab/netcore2x)

<span data-ttu-id="2ea13-115">.NET Core 2.x は、1 つのオペレーティング システムとして Linux を扱います。</span><span class="sxs-lookup"><span data-stu-id="2ea13-115">.NET Core 2.x treats Linux as a single operating system.</span></span> <span data-ttu-id="2ea13-116">サポートされている Linux ディストリビューション用に、1 つの Linux ビルド (チップ アーキテクチャあたり) があります。</span><span class="sxs-lookup"><span data-stu-id="2ea13-116">There is a single Linux build (per chip architecture) for supported Linux distributions.</span></span> 

<span data-ttu-id="2ea13-117">ダウンロード リンクと詳細については、[.NET Core 2.2 のダウンロード](https://www.microsoft.com/net/download/dotnet-core/2.2)または [.NET Core 2.1](https://www.microsoft.com/net/download/dotnet-core/2.1) のダウンロードのページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ea13-117">For download links and more information, see [.NET Core 2.2 downloads](https://www.microsoft.com/net/download/dotnet-core/2.2) or [.NET Core 2.1 downloads](https://www.microsoft.com/net/download/dotnet-core/2.1).</span></span>

<span data-ttu-id="2ea13-118">.NET Core 2.x は、次の Linux ディストリビューション/バージョンでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="2ea13-118">.NET Core 2.x is supported on the following Linux distributions/versions:</span></span>

* <span data-ttu-id="2ea13-119">Red Hat Enterprise Linux 7、6 - 64 ビット (`x86_64` または `amd64`)</span><span class="sxs-lookup"><span data-stu-id="2ea13-119">Red Hat Enterprise Linux 7, 6 - 64-bit (`x86_64` or `amd64`)</span></span>
* <span data-ttu-id="2ea13-120">CentOS 7 - 64 ビット (`x86_64` または `amd64`)</span><span class="sxs-lookup"><span data-stu-id="2ea13-120">CentOS 7  - 64-bit (`x86_64` or `amd64`)</span></span> 
* <span data-ttu-id="2ea13-121">Oracle Linux 7 - 64 ビット (`x86_64` または `amd64`)</span><span class="sxs-lookup"><span data-stu-id="2ea13-121">Oracle Linux 7 - 64-bit (`x86_64` or `amd64`)</span></span> 
* <span data-ttu-id="2ea13-122">Fedora 28、27 - 64 ビット (`x86_64` または `amd64`)</span><span class="sxs-lookup"><span data-stu-id="2ea13-122">Fedora 28, 27 - 64-bit (`x86_64` or `amd64`)</span></span> 
* <span data-ttu-id="2ea13-123">Debian 9 (64 ビット、`arm32`), 8.7 以降のバージョン - 64 ビット (`x86_64` または `amd64`)</span><span class="sxs-lookup"><span data-stu-id="2ea13-123">Debian 9 (64-bit, `arm32`), 8.7 or later versions - 64-bit (`x86_64` or `amd64`)</span></span>
* <span data-ttu-id="2ea13-124">Ubuntu 18.04 (64 ビット、`arm32`)、16.04、14.04 - 64 ビット (`x86_64` または `amd64`)</span><span class="sxs-lookup"><span data-stu-id="2ea13-124">Ubuntu 18.04 (64-bit, `arm32`), 16.04, 14.04 - 64-bit (`x86_64` or `amd64`)</span></span>
* <span data-ttu-id="2ea13-125">Linux Mint 18、17 - 64 ビット (`x86_64` または `amd64`)</span><span class="sxs-lookup"><span data-stu-id="2ea13-125">Linux Mint 18, 17 - 64-bit (`x86_64` or `amd64`)</span></span>
* <span data-ttu-id="2ea13-126">openSUSE 42.3 以降のバージョン - 64 ビット (`x86_64` または `amd64`)</span><span class="sxs-lookup"><span data-stu-id="2ea13-126">openSUSE 42.3 or later versions - 64-bit (`x86_64` or `amd64`)</span></span>
* <span data-ttu-id="2ea13-127">SUSE Enterprise Linux (SLES) 12 Service Pack 2 以降 - 64 ビット (`x86_64` または `amd64`)</span><span class="sxs-lookup"><span data-stu-id="2ea13-127">SUSE Enterprise Linux (SLES) 12 Service Pack 2 or later - 64-bit (`x86_64` or `amd64`)</span></span>
* <span data-ttu-id="2ea13-128">Alpine Linux 3.7 以降のバージョン - 64 ビット (`x86_64` または `amd64`)</span><span class="sxs-lookup"><span data-stu-id="2ea13-128">Alpine Linux 3.7 or later versions - 64-bit (`x86_64` or `amd64`)</span></span>

<span data-ttu-id="2ea13-129">.NET Core 2.1 と .NET Core 2.2 がサポートされているオペレーティング システム、ディストリビューション、バージョン、サポートされていない OS バージョン、ライフサイクル ポリシー リンクの完全なリストについては、[.NET Core 2.1 がサポートされる OS バージョン](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md)と [.NET Core 2.2 がサポートされている OS バージョン](https://github.com/dotnet/core/blob/master/release-notes/2.2/2.2-supported-os.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ea13-129">See [.NET Core 2.1 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md) and [.NET Core 2.2 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.2/2.2-supported-os.md) for the complete list of .NET Core 2.1 and .NET Core 2.2 supported operating systems, distributions and versions, out of support OS versions, and lifecycle policy links.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="2ea13-130">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="2ea13-130">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="2ea13-131">ダウンロード リンクと詳細については、[.NET Core 1.1 のダウンロード](https://www.microsoft.com/net/download/dotnet-core/1.1)または [.NET Core 1.0](https://www.microsoft.com/net/download/dotnet-core/1.0) のダウンロードのページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ea13-131">For download links and more information, see [.NET Core 1.1 downloads](https://www.microsoft.com/net/download/dotnet-core/1.1) or [.NET Core 1.0 downloads](https://www.microsoft.com/net/download/dotnet-core/1.0).</span></span>

<span data-ttu-id="2ea13-132">.NET Core 1.x は、次の Linux 64 ビット (`x86_64` または `amd64`) ディストリビューション/バージョンでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="2ea13-132">.NET Core 1.x is supported on the following Linux 64-bit (`x86_64` or `amd64`) distributions/versions:</span></span>

* <span data-ttu-id="2ea13-133">Red Hat Enterprise Linux 7</span><span class="sxs-lookup"><span data-stu-id="2ea13-133">Red Hat Enterprise Linux 7</span></span>
* <span data-ttu-id="2ea13-134">CentOS 7</span><span class="sxs-lookup"><span data-stu-id="2ea13-134">CentOS 7</span></span>
* <span data-ttu-id="2ea13-135">Oracle Linux 7</span><span class="sxs-lookup"><span data-stu-id="2ea13-135">Oracle Linux 7</span></span>
* <span data-ttu-id="2ea13-136">Fedora 28 (.NET Core 1.1)、27</span><span class="sxs-lookup"><span data-stu-id="2ea13-136">Fedora 28 (.NET Core 1.1), 27</span></span>
* <span data-ttu-id="2ea13-137">Debian 8.2 以降のバージョン</span><span class="sxs-lookup"><span data-stu-id="2ea13-137">Debian 8.2 or later versions</span></span>
* <span data-ttu-id="2ea13-138">Ubuntu 18.04 (.NET Core 1.1)、16.04、14.04</span><span class="sxs-lookup"><span data-stu-id="2ea13-138">Ubuntu 18.04 (.NET Core 1.1), 16.04, 14.04</span></span>
* <span data-ttu-id="2ea13-139">Linux Mint 17</span><span class="sxs-lookup"><span data-stu-id="2ea13-139">Linux Mint 17</span></span>
* <span data-ttu-id="2ea13-140">openSUSE 42.3 以降のバージョン (.NET Core 1.1)</span><span class="sxs-lookup"><span data-stu-id="2ea13-140">openSUSE 42.3 or later versions (.NET Core 1.1)</span></span>

<span data-ttu-id="2ea13-141">.NET Core 1.x がサポートされているオペレーティング システム (サポートされている OS バージョン以外) の完全なリスト、およびライフサイクル ポリシーのリンクについては、「[.NET Core 1.x Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md)」 (.NET Core 1.x がサポートされる OS のバージョン) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ea13-141">See [.NET Core 1.x Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md) for the complete list of .NET Core 1.x supported operating systems, out of support OS versions, and lifecycle policy links.</span></span>

---

## <a name="linux-distribution-dependencies"></a><span data-ttu-id="2ea13-142">Linux ディストリビューションの依存関係</span><span class="sxs-lookup"><span data-stu-id="2ea13-142">Linux distribution dependencies</span></span>

<span data-ttu-id="2ea13-143">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="2ea13-143">The following are intended to be examples.</span></span> <span data-ttu-id="2ea13-144">選択した Linux ディストリビューションで、バージョンと名前が多少異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="2ea13-144">The exact versions and names may vary slightly on your Linux distribution of choice.</span></span>

### <a name="ubuntu"></a><span data-ttu-id="2ea13-145">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="2ea13-145">Ubuntu</span></span>

<span data-ttu-id="2ea13-146">Ubuntu ディストリビューションには、次のライブラリがインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ea13-146">Ubuntu distributions require the following libraries installed:</span></span>

* <span data-ttu-id="2ea13-147">liblttng-ust0</span><span class="sxs-lookup"><span data-stu-id="2ea13-147">liblttng-ust0</span></span>
* <span data-ttu-id="2ea13-148">libcurl3</span><span class="sxs-lookup"><span data-stu-id="2ea13-148">libcurl3</span></span>
* <span data-ttu-id="2ea13-149">libssl1.0.0</span><span class="sxs-lookup"><span data-stu-id="2ea13-149">libssl1.0.0</span></span>
* <span data-ttu-id="2ea13-150">libkrb5-3</span><span class="sxs-lookup"><span data-stu-id="2ea13-150">libkrb5-3</span></span>
* <span data-ttu-id="2ea13-151">zlib1g</span><span class="sxs-lookup"><span data-stu-id="2ea13-151">zlib1g</span></span>
* <span data-ttu-id="2ea13-152">libicu52 (14.x 用)</span><span class="sxs-lookup"><span data-stu-id="2ea13-152">libicu52 (for 14.x)</span></span>
* <span data-ttu-id="2ea13-153">libicu55 (16.x 用)</span><span class="sxs-lookup"><span data-stu-id="2ea13-153">libicu55 (for 16.x)</span></span>
* <span data-ttu-id="2ea13-154">libicu57 (17.x 用)</span><span class="sxs-lookup"><span data-stu-id="2ea13-154">libicu57 (for 17.x)</span></span>
* <span data-ttu-id="2ea13-155">libicu60 (18.x 用)</span><span class="sxs-lookup"><span data-stu-id="2ea13-155">libicu60 (for 18.x)</span></span>

<span data-ttu-id="2ea13-156">.NET Core 2.1 より前のバージョンには、次の依存関係も必要です。</span><span class="sxs-lookup"><span data-stu-id="2ea13-156">For versions earlier than .NET Core 2.1, following dependencies are also required:</span></span>

* <span data-ttu-id="2ea13-157">libunwind8</span><span class="sxs-lookup"><span data-stu-id="2ea13-157">libunwind8</span></span>
* <span data-ttu-id="2ea13-158">libuuid1</span><span class="sxs-lookup"><span data-stu-id="2ea13-158">libuuid1</span></span>

### <a name="centos-and-fedora"></a><span data-ttu-id="2ea13-159">CentOS と Fedora</span><span class="sxs-lookup"><span data-stu-id="2ea13-159">CentOS and Fedora</span></span>

<span data-ttu-id="2ea13-160">CentOS ディストリビューションには、次のライブラリがインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ea13-160">CentOS distributions require the following libraries installed:</span></span>

* <span data-ttu-id="2ea13-161">lttng-ust</span><span class="sxs-lookup"><span data-stu-id="2ea13-161">lttng-ust</span></span>
* <span data-ttu-id="2ea13-162">libcurl</span><span class="sxs-lookup"><span data-stu-id="2ea13-162">libcurl</span></span>
* <span data-ttu-id="2ea13-163">openssl-libs</span><span class="sxs-lookup"><span data-stu-id="2ea13-163">openssl-libs</span></span>
* <span data-ttu-id="2ea13-164">krb5-libs</span><span class="sxs-lookup"><span data-stu-id="2ea13-164">krb5-libs</span></span>
* <span data-ttu-id="2ea13-165">libicu</span><span class="sxs-lookup"><span data-stu-id="2ea13-165">libicu</span></span>
* <span data-ttu-id="2ea13-166">zlib</span><span class="sxs-lookup"><span data-stu-id="2ea13-166">zlib</span></span>

<span data-ttu-id="2ea13-167">Fedora ユーザー: ご使用の openssl のバージョンが 1.1 以降の場合は、compat-openssl10 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ea13-167">Fedora users: If your openssl's version >= 1.1, you'll need to install compat-openssl10.</span></span>

<span data-ttu-id="2ea13-168">.NET Core 2.1 より前のバージョンには、次の依存関係も必要です。</span><span class="sxs-lookup"><span data-stu-id="2ea13-168">For versions earlier than .NET Core 2.1, following dependencies are also required:</span></span>

* <span data-ttu-id="2ea13-169">libunwind</span><span class="sxs-lookup"><span data-stu-id="2ea13-169">libunwind</span></span>
* <span data-ttu-id="2ea13-170">libuuid</span><span class="sxs-lookup"><span data-stu-id="2ea13-170">libuuid</span></span>

<span data-ttu-id="2ea13-171">依存関係の詳細については、「[Self-contained Linux applications (自己完結型 Linux アプリケーション)](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2ea13-171">For more information about the dependencies, see [Self-contained Linux applications](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md).</span></span>

## <a name="installing-net-core-dependencies-with-the-native-installers"></a><span data-ttu-id="2ea13-172">ネイティブ インストーラーを使用した .NET Core の依存関係のインストール</span><span class="sxs-lookup"><span data-stu-id="2ea13-172">Installing .NET Core dependencies with the native installers</span></span>

<span data-ttu-id="2ea13-173">.NET Core ネイティブ インストーラーは、サポートされている Linux ディストリビューション/バージョンに利用できます。</span><span class="sxs-lookup"><span data-stu-id="2ea13-173">.NET Core native installers are available for supported Linux distributions/versions.</span></span> <span data-ttu-id="2ea13-174">このネイティブ インストーラーは、サーバーへの admin (sudo) アクセスを必要とします。</span><span class="sxs-lookup"><span data-stu-id="2ea13-174">The native installers require admin (sudo) access to the server.</span></span> <span data-ttu-id="2ea13-175">ネイティブ インストーラーを使用することの利点は、.NET Core ネイティブの依存関係がすべてインストールされることです。</span><span class="sxs-lookup"><span data-stu-id="2ea13-175">The advantage of using a native installer is that all of the .NET Core native dependencies are installed.</span></span> <span data-ttu-id="2ea13-176">また、ネイティブ インストーラーでは、.NET Core SDK もシステム全体にインストールします。</span><span class="sxs-lookup"><span data-stu-id="2ea13-176">Native installers also install the .NET Core SDK system-wide.</span></span>

<span data-ttu-id="2ea13-177">Linux では、2 つのインストーラー パッケージから選択できます。</span><span class="sxs-lookup"><span data-stu-id="2ea13-177">On Linux, there are two installer package choices:</span></span>

* <span data-ttu-id="2ea13-178">フィードベースのパッケージ マネージャー (Ubuntu では apt-get、CentOS/RHEL では yum など) を使用する</span><span class="sxs-lookup"><span data-stu-id="2ea13-178">Using a feed-based package manager, such as apt-get for Ubuntu, or yum for CentOS/RHEL.</span></span>
* <span data-ttu-id="2ea13-179">パッケージ自体 (DEB または RPM) を使用する</span><span class="sxs-lookup"><span data-stu-id="2ea13-179">Using the packages themselves, DEB or RPM.</span></span>

### <a name="scripting-installs-with-the-net-core-installer-script"></a><span data-ttu-id="2ea13-180">.NET Core インストーラー スクリプトを使用したスクリプトのインストール</span><span class="sxs-lookup"><span data-stu-id="2ea13-180">Scripting Installs with the .NET Core installer script</span></span>

<span data-ttu-id="2ea13-181">[dotnet-install スクリプト](./tools/dotnet-install-script.md)は、CLI ツールチェーンと共有ランタイムの非管理者インストールを実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ea13-181">The [dotnet-install scripts](./tools/dotnet-install-script.md) are used to perform a non-admin install of the CLI toolchain and the shared runtime.</span></span> <span data-ttu-id="2ea13-182">このスクリプトは [https://dot.net/v1/dotnet-install.sh](https://dot.net/v1/dotnet-install.sh) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="2ea13-182">You can download the script from [https://dot.net/v1/dotnet-install.sh](https://dot.net/v1/dotnet-install.sh).</span></span>

<span data-ttu-id="2ea13-183">スクリプトは、既定で最新の "LTS" のバージョン (現在は .NET Core 1.1) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="2ea13-183">The script defaults to installing the latest "LTS" version, which is currently .NET Core 1.1.</span></span> <span data-ttu-id="2ea13-184">NET Core 2.1 をインストールするには、次のスイッチを使用してスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="2ea13-184">To install .NET Core 2.1, run the script with the following switch:</span></span>

```console
./dotnet-install.sh -c Current
```

<span data-ttu-id="2ea13-185">インストーラーの bash スクリプトは、自動化シナリオと管理者以外のインストールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ea13-185">The installer bash script is used in automation scenarios and non-admin installations.</span></span> <span data-ttu-id="2ea13-186">このスクリプトは、PowerShell のスイッチも読み取るので、Linux/OS X システムのスクリプトで使うことができます。</span><span class="sxs-lookup"><span data-stu-id="2ea13-186">This script also reads PowerShell switches, so they can be used with the script on Linux/OS X systems.</span></span>

## <a name="troubleshoot"></a><span data-ttu-id="2ea13-187">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="2ea13-187">Troubleshoot</span></span>

<span data-ttu-id="2ea13-188">サポートされている Linux ディストリビューション/バージョンへの .NET Core のインストールに問題がある場合は、インストールしているディストリビューション/バージョンに関する以下のトピックをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2ea13-188">If you have problems with a .NET Core installation on a supported Linux distribution/version, consult the following topics for your installed distributions/versions:</span></span>

* [<span data-ttu-id="2ea13-189">.NET Core 3.0 の既知の問題</span><span class="sxs-lookup"><span data-stu-id="2ea13-189">.NET Core 3.0 known issues</span></span>](https://github.com/dotnet/core/tree/master/release-notes/3.0)
* [<span data-ttu-id="2ea13-190">.NET Core 2.2 の既知の問題</span><span class="sxs-lookup"><span data-stu-id="2ea13-190">.NET Core 2.2 known issues</span></span>](https://github.com/dotnet/core/tree/master/release-notes/2.2)
* [<span data-ttu-id="2ea13-191">.NET Core 2.1 の既知の問題</span><span class="sxs-lookup"><span data-stu-id="2ea13-191">.NET Core 2.1 known issues</span></span>](https://github.com/dotnet/core/tree/master/release-notes/2.1)
* [<span data-ttu-id="2ea13-192">.NET Core 1.1 の既知の問題</span><span class="sxs-lookup"><span data-stu-id="2ea13-192">.NET Core 1.1 known issues</span></span>](https://github.com/dotnet/core/blob/master/release-notes/1.1)
* [<span data-ttu-id="2ea13-193">.NET Core 1.0 の既知の問題</span><span class="sxs-lookup"><span data-stu-id="2ea13-193">.NET Core 1.0 known issues</span></span>](https://github.com/dotnet/core/blob/master/release-notes/1.0)
