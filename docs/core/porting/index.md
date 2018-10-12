---
title: .NET Framework から .NET Core への移植
description: 移植プロセスを理解し、.NET Framework プロジェクトを .NET Core に移植する際に役立つツールを確認します。
author: cartermp
ms.author: mairaw
ms.date: 06/20/2016
ms.openlocfilehash: d273b3abe46de59aa55b5b9a531d3c572a065124
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2018
ms.locfileid: "48835393"
---
# <a name="porting-to-net-core-from-net-framework"></a><span data-ttu-id="3b5e3-103">.NET Framework から .NET Core への移植</span><span class="sxs-lookup"><span data-stu-id="3b5e3-103">Porting to .NET Core from .NET Framework</span></span>

<span data-ttu-id="3b5e3-104">.NET Framework で実行されているコードがある場合は、.NET Core 1.0 でコードを実行することに関心があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-104">If you've got code running on the .NET Framework, you may be interested in running your code on .NET Core 1.0.</span></span>  <span data-ttu-id="3b5e3-105">この記事では、移植プロセスの概要と、.NET Core に移植するときに役立つツールの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-105">This article covers an overview of the porting process and a list of the tools you may find helpful when porting to .NET Core.</span></span>

## <a name="overview-of-the-porting-process"></a><span data-ttu-id="3b5e3-106">移植プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="3b5e3-106">Overview of the Porting Process</span></span>

<span data-ttu-id="3b5e3-107">移植の推奨プロセスでは、次の一連の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-107">The recommended process for porting follows the following series of steps.</span></span>  <span data-ttu-id="3b5e3-108">プロセスのこれらの各部分については、他の記事で詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-108">Each of these parts of the process are covered in more detail in further articles.</span></span>

1. <span data-ttu-id="3b5e3-109">サードパーティの依存関係を識別し、理解します。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-109">Identify and account for your third-party dependencies.</span></span>

   <span data-ttu-id="3b5e3-110">このプロセスでは、サードパーティの依存関係がどのようなものか、それらにどのように依存しているか、それらが .NET Core でも実行されるかどうかを確認する方法、および実行されない場合に従う手順について理解します。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-110">This will involve understanding what your third-party dependencies are, how you depend on them, how to see if they also run on .NET Core, and steps you can take if they don't.</span></span>
   
2. <span data-ttu-id="3b5e3-111">ターゲットの .NET Framework 4.6.2 に移植するすべてのプロジェクトをターゲットとして再指定します。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-111">Retarget all projects you wish to port to target .NET Framework 4.6.2.</span></span>

   <span data-ttu-id="3b5e3-112">これにより、.NET Core が特定の API をサポートできない場合に、.NET Framework 固有のターゲットに対して API の代替を確実に使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-112">This ensures that you can use API alternatives for .NET Framework-specific targets in the cases where .NET Core can't support a particular API.</span></span>
   
3. <span data-ttu-id="3b5e3-113">[.NET Portability Analyzer](../../standard/analyzers/portability-analyzer.md)使用して、アセンブリを分析し、その結果に基づいて移植を行う計画を作成します。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-113">Use the [.NET Portability Analyzer](../../standard/analyzers/portability-analyzer.md) to analyze your assemblies and develop a plan to port based on its results.</span></span>

   <span data-ttu-id="3b5e3-114">API Portability Analyzer ツールは、コンパイル済みアセンブリを分析し、レポートを生成します。このレポートには、移植性の概要と、.NET Core ではサポートされていない使用中の各 API の内訳が示されます。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-114">The API Portability Analyzer tool will analyze your compiled assemblies and generate a report which shows a high-level portability summary and a breakdown of each API you're using that isn't available on .NET Core.</span></span>  <span data-ttu-id="3b5e3-115">このレポートをコードベースの分析と共に使用して、コードを移植する方法の計画を作成します。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-115">You can use this report alongside an analysis of your codebase to develop a plan for how you'll port your code over.</span></span>
   
4. <span data-ttu-id="3b5e3-116">テスト コードを移植します。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-116">Port your tests code.</span></span>

   <span data-ttu-id="3b5e3-117">.NET Core への移植はコードベースにとって大きな変更となるため、コードの移植時にテストを実行できるように、テスト コードを移植することが推奨されます。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-117">Because porting to .NET Core is such a big change to your codebase, it's highly recommended to get your tests ported so that you can run tests as you port code over.</span></span>  <span data-ttu-id="3b5e3-118">現在、MSTest、xUnit、および NUnit は .NET Core 1.0 をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-118">MSTest, xUnit, and NUnit all support .NET Core 1.0 today.</span></span>
   
6. <span data-ttu-id="3b5e3-119">移植の計画を実行します。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-119">Execute your plan for porting!</span></span>

## <a name="tools-to-help"></a><span data-ttu-id="3b5e3-120">役立つツール</span><span class="sxs-lookup"><span data-stu-id="3b5e3-120">Tools to help</span></span>

<span data-ttu-id="3b5e3-121">役立つツールの簡単な一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-121">Here's a short list of the tools you'll find helpful:</span></span>

* <span data-ttu-id="3b5e3-122">NuGet - [Nuget クライアント](https://dist.nuget.org/index.html)または [NuGet パッケージ エクスプローラー](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer)。 .NET 実装用の Microsoft のパッケージ マネージャー。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-122">NuGet - [Nuget Client](https://dist.nuget.org/index.html) or [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer), Microsoft's package manager for .NET implementations.</span></span>
* <span data-ttu-id="3b5e3-123">Api Portability Analyzer - [コマンドライン ツール](https://github.com/Microsoft/dotnet-apiport/releases)または [Visual Studio 拡張機能](https://visualstudiogallery.msdn.microsoft.com/1177943e-cfb7-4822-a8a6-e56c7905292b)。アセンブリごとの問題の内訳を含む、.NET Framework と .NET Core の間のコードの移植性に関するレポートを生成できるツール チェーンです。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-123">Api Portability Analyzer - [command line tool](https://github.com/Microsoft/dotnet-apiport/releases) or [Visual Studio Extension](https://visualstudiogallery.msdn.microsoft.com/1177943e-cfb7-4822-a8a6-e56c7905292b), a toolchain that can generate a report of how portable your code is between .NET Framework and .NET Core, with an assembly-by-assembly breakdown of issues.</span></span>  <span data-ttu-id="3b5e3-124">「[Tooling to help you on the process](https://github.com/Microsoft/dotnet-apiport/blob/master/docs/HowTo/)」 (作業に役立つツール) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-124">See [Tooling to help you on the process](https://github.com/Microsoft/dotnet-apiport/blob/master/docs/HowTo/) for more information.</span></span>
* <span data-ttu-id="3b5e3-125">Reverse Package Search - 型を検索し、その型を含むパッケージを検索するための[便利な Web サービス](https://packagesearch.azurewebsites.net)。</span><span class="sxs-lookup"><span data-stu-id="3b5e3-125">Reverse Package Search - A [useful web service](https://packagesearch.azurewebsites.net) that allows you to search for a type and find packages containing that type.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3b5e3-126">次の手順</span><span class="sxs-lookup"><span data-stu-id="3b5e3-126">Next steps</span></span>

[<span data-ttu-id="3b5e3-127">サードパーティの依存関係の分析</span><span class="sxs-lookup"><span data-stu-id="3b5e3-127">Analyzing your third-party dependencies.</span></span>](third-party-deps.md)
   
