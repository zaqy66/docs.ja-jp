---
title: .NET Core のガイド
description: .NET Core は、Windows、Linux、および Mac アプリを作成するためのモジュール型の高性能な .NET 実装です。 ここでは、.NET Core の概要について説明します。
author: richlander
ms.author: mairaw
ms.date: 08/01/2018
ms.custom: updateeachrelease
ms.openlocfilehash: b302b6fc7e097a811c718d2244f603246cb5c259
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2018
ms.locfileid: "49121039"
---
# <a name="net-core-guide"></a><span data-ttu-id="52871-104">.NET Core のガイド</span><span class="sxs-lookup"><span data-stu-id="52871-104">.NET Core Guide</span></span>

<span data-ttu-id="52871-105">[.NET Core](about.md) は、[GitHub](https://github.com/dotnet/core) で Microsoft および .NET コミュニティによって管理される[オープンソース](https://github.com/dotnet/coreclr/blob/master/LICENSE.TXT)の一般的な開発プラットフォームです。</span><span class="sxs-lookup"><span data-stu-id="52871-105">[.NET Core](about.md) is an [open-source](https://github.com/dotnet/coreclr/blob/master/LICENSE.TXT) general-purpose development platform maintained by Microsoft and the .NET community on [GitHub](https://github.com/dotnet/core).</span></span> <span data-ttu-id="52871-106">クロスプラットフォームであり、Windows、macOS、Linux をサポートし、デバイス、クラウド、および IoT アプリケーションで使用できます。</span><span class="sxs-lookup"><span data-stu-id="52871-106">It's cross-platform, supporting Windows, macOS and Linux, and can be used in device, cloud, and IoT applications.</span></span>

<span data-ttu-id="52871-107">特徴、サポートされる言語とフレームワーク、キー API など、.NET Core について詳しくは、「[About .NET Core](about.md)」(.NET Core について) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="52871-107">See [About .NET Core](about.md) to learn more about .NET Core, including its characteristics, supported languages and frameworks, and key APIs.</span></span>

<span data-ttu-id="52871-108">「[.NET Core チュートリアル](tutorials/index.md)」では、単純な .NET Core アプリケーションを作成する方法を学習できます。</span><span class="sxs-lookup"><span data-stu-id="52871-108">Check out [.NET Core Tutorials](tutorials/index.md) to learn how to create a simple .NET Core application.</span></span> <span data-ttu-id="52871-109">最初のアプリを、ほんの数分で起動および実行できます。</span><span class="sxs-lookup"><span data-stu-id="52871-109">It only takes a few minutes to get your first app up and running.</span></span> <span data-ttu-id="52871-110">ブラウザーで .NET Core を使用してみたい場合は、[C# における数値](https://docs.microsoft.com/dotnet/csharp/quick-starts/numbers-in-csharp)に関するクイックスタートをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="52871-110">If you want to try .NET Core in your browser, look at the [Numbers in C#](https://docs.microsoft.com/dotnet/csharp/quick-starts/numbers-in-csharp) quickstart.</span></span>

## <a name="download-net-core-21"></a><span data-ttu-id="52871-111">NET Core 2.1 のダウンロード</span><span class="sxs-lookup"><span data-stu-id="52871-111">Download .NET Core 2.1</span></span>

<span data-ttu-id="52871-112">[.NET Core  2.1 SDK](https://www.microsoft.com/net/download) をダウンロードして、Windows、macOS、または Linux マシンで .NET Core をお試しください。</span><span class="sxs-lookup"><span data-stu-id="52871-112">Download the [.NET Core  2.1 SDK](https://www.microsoft.com/net/download) to try .NET Core on your Windows, macOS, or Linux machine.</span></span> <span data-ttu-id="52871-113">Docker コンテナーを使用する方がよければ、[microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet/) にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="52871-113">Visit [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet/) if you prefer to use Docker containers.</span></span>

<span data-ttu-id="52871-114">別の .NET Core バージョンを探している場合も、すべての .NET Core バージョンを [.NET Core のダウンロード](https://www.microsoft.com/net/download/archives)で入手できます。</span><span class="sxs-lookup"><span data-stu-id="52871-114">All .NET Core versions are available at [.NET Core Downloads](https://www.microsoft.com/net/download/archives) if you're looking for another .NET Core version.</span></span>

## <a name="net-core-21"></a><span data-ttu-id="52871-115">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="52871-115">.NET Core 2.1</span></span>

<span data-ttu-id="52871-116">最新バージョンは [.NET Core 2.1](whats-new/dotnet-core-2-1.md) です。</span><span class="sxs-lookup"><span data-stu-id="52871-116">The latest version is [.NET Core 2.1](whats-new/dotnet-core-2-1.md).</span></span> <span data-ttu-id="52871-117">新機能には、グローバル ツール、高パフォーマンス API (<xref:System.Span%601?displayProperty=nameWithType> など)、階層型 JIT コンパイル、[ビルド](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/)と[ランタイムのパフォーマンスの向上](https://blogs.msdn.microsoft.com/dotnet/2018/04/18/performance-improvements-in-net-core-2-1/)、Alpine と ARM32 のサポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="52871-117">New features include: global tools, high-performance APIs (such as <xref:System.Span%601?displayProperty=nameWithType>), tiered JIT compilation, [build](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) and [runtime performance improvements](https://blogs.msdn.microsoft.com/dotnet/2018/04/18/performance-improvements-in-net-core-2-1/), and support for Alpine and ARM32.</span></span>

## <a name="create-your-first-application"></a><span data-ttu-id="52871-118">最初のアプリケーションの作成</span><span class="sxs-lookup"><span data-stu-id="52871-118">Create your first application</span></span>

<span data-ttu-id="52871-119">.NET Core SDK をインストールしたらコマンド プロンプトを開きます。</span><span class="sxs-lookup"><span data-stu-id="52871-119">After installing the .NET Core SDK, open a command prompt.</span></span> <span data-ttu-id="52871-120">次の `dotnet` コマンドを入力し、C# アプリケーションを作成して実行します。</span><span class="sxs-lookup"><span data-stu-id="52871-120">Type the following `dotnet` commands to create and run a C# application.</span></span>

```console
dotnet new console
dotnet run
```

<span data-ttu-id="52871-121">次の出力が表示されます。</span><span class="sxs-lookup"><span data-stu-id="52871-121">You should see the following output:</span></span>

```console
Hello World!
```

## <a name="support"></a><span data-ttu-id="52871-122">サポート</span><span class="sxs-lookup"><span data-stu-id="52871-122">Support</span></span>

<span data-ttu-id="52871-123">.NET Core は、Microsoft Windows、macOS、Linux で[サポート](https://www.microsoft.com/net/support/policy)されています。</span><span class="sxs-lookup"><span data-stu-id="52871-123">.NET Core is [supported by Microsoft](https://www.microsoft.com/net/support/policy), on Windows, macOS and Linux.</span></span> <span data-ttu-id="52871-124">年に数回、通常は毎月、セキュリティと品質向上のために更新されます。</span><span class="sxs-lookup"><span data-stu-id="52871-124">It's updated for security and quality several times a year, typically monthly.</span></span>

<span data-ttu-id="52871-125">.NET Core のバイナリ形式の配布は、Azure 内のマイクロソフトが管理するサーバーで構築されてテストされ、他のすべてのマイクロソフト製品と同様にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="52871-125">.NET Core binary distributions are built and tested on Microsoft-maintained servers in Azure and supported just like any Microsoft product.</span></span>

<span data-ttu-id="52871-126">Red Hat Enterprise Linux (RHEL) では [.NET Core は Red Hat によってサポート](http://redhatloves.net/)されます。</span><span class="sxs-lookup"><span data-stu-id="52871-126">[Red Hat supports .NET Core](http://redhatloves.net/) on Red Hat Enterprise Linux (RHEL).</span></span> <span data-ttu-id="52871-127">Red Hat がソースから .NET Core をビルドして、[Red Hat ソフトウェア コレクション](https://developers.redhat.com/products/softwarecollections/overview/)で使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="52871-127">Red Hat builds .NET Core from source and makes it available in the [Red Hat Software Collections](https://developers.redhat.com/products/softwarecollections/overview/).</span></span> <span data-ttu-id="52871-128">Red Hat とマイクロソフトが共同して、.NET Core が RHEL 上で適切に動作するようにします。</span><span class="sxs-lookup"><span data-stu-id="52871-128">Red Hat and Microsoft collaborate to ensure that .NET Core works well on RHEL.</span></span>
