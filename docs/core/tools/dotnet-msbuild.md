---
title: dotnet msbuild コマンド - .NET Core CLI
description: dotnet msbuild コマンドは、MSBuild コマンド ラインへのアクセスを提供します。
author: mairaw
ms.author: mairaw
ms.date: 05/25/2018
ms.openlocfilehash: 76165590478b0e76d19d546c87e012da4716b6db
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2018
ms.locfileid: "47421191"
---
# <a name="dotnet-msbuild"></a><span data-ttu-id="b4556-103">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="b4556-103">dotnet msbuild</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="b4556-104">name</span><span class="sxs-lookup"><span data-stu-id="b4556-104">Name</span></span>

<span data-ttu-id="b4556-105">`dotnet msbuild` - プロジェクトとそのすべての依存関係をビルドします。</span><span class="sxs-lookup"><span data-stu-id="b4556-105">`dotnet msbuild` - Builds a project and all of its dependencies.</span></span>

## <a name="synopsis"></a><span data-ttu-id="b4556-106">構文</span><span class="sxs-lookup"><span data-stu-id="b4556-106">Synopsis</span></span>

`dotnet msbuild <msbuild_arguments> [-h]`

## <a name="description"></a><span data-ttu-id="b4556-107">説明</span><span class="sxs-lookup"><span data-stu-id="b4556-107">Description</span></span>

<span data-ttu-id="b4556-108">`dotnet msbuild` コマンドでは、完全に機能する MSBuild へのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="b4556-108">The `dotnet msbuild` command allows access to a fully functional MSBuild.</span></span>

<span data-ttu-id="b4556-109">このコマンドには、既存の MSBuild コマンド ライン クライアントとまったく同じ機能があります。</span><span class="sxs-lookup"><span data-stu-id="b4556-109">The command has the exact same capabilities as existing MSBuild command-line client.</span></span> <span data-ttu-id="b4556-110">オプションはすべて同じです。</span><span class="sxs-lookup"><span data-stu-id="b4556-110">The options are all the same.</span></span> <span data-ttu-id="b4556-111">使用可能なオプションの詳細については、「[MSBuild コマンド ライン リファレンス](/visualstudio/msbuild/msbuild-command-line-reference)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4556-111">For more information about the available options, see the [MSBuild Command-Line Reference](/visualstudio/msbuild/msbuild-command-line-reference).</span></span>

## <a name="examples"></a><span data-ttu-id="b4556-112">使用例</span><span class="sxs-lookup"><span data-stu-id="b4556-112">Examples</span></span>

<span data-ttu-id="b4556-113">プロジェクトとその依存関係をビルドします。</span><span class="sxs-lookup"><span data-stu-id="b4556-113">Build a project and its dependencies:</span></span>

`dotnet msbuild`

<span data-ttu-id="b4556-114">リリース構成を使用して、プロジェクトとその依存関係をビルドします。</span><span class="sxs-lookup"><span data-stu-id="b4556-114">Build a project and its dependencies using Release configuration:</span></span>

`dotnet msbuild -p:Configuration=Release`

<span data-ttu-id="b4556-115">発行先を実行して、RID `osx.10.11-x64` に発行します。</span><span class="sxs-lookup"><span data-stu-id="b4556-115">Run the publish target and publish for the `osx.10.11-x64` RID:</span></span>

`dotnet msbuild -t:Publish -p:RuntimeIdentifiers=osx.10.11-x64`

<span data-ttu-id="b4556-116">プロジェクト全体と SDK に付属するすべてのターゲットをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b4556-116">See the whole project with all targets included by the SDK:</span></span>

`dotnet msbuild -pp`
