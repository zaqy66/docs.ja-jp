---
title: dotnet tool list コマンド
description: dotnet tool list コマンドは、マシン上の指定された .NET Core グローバル ツールを一覧表示します。
ms.date: 05/29/2018
ms.openlocfilehash: 0c17534beb80ed87a8f260342b0f82882a9e17b6
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169764"
---
# <a name="dotnet-tool-list"></a><span data-ttu-id="449a1-103">dotnet tool list</span><span class="sxs-lookup"><span data-stu-id="449a1-103">dotnet tool list</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="449a1-104">name</span><span class="sxs-lookup"><span data-stu-id="449a1-104">Name</span></span>

<span data-ttu-id="449a1-105">`dotnet tool list` - マシン上の既定のディレクトリまたは指定したパスに現在インストールされているすべての [.NET Core グローバル ツール](global-tools.md)を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="449a1-105">`dotnet tool list` - Lists all [.NET Core Global Tools](global-tools.md) currently installed in the default directory on your machine or in the specified path.</span></span>

## <a name="synopsis"></a><span data-ttu-id="449a1-106">構文</span><span class="sxs-lookup"><span data-stu-id="449a1-106">Synopsis</span></span>

```console
dotnet tool list <-g|--global>
dotnet tool list <--tool-path>
dotnet tool list <-h|--help>
```

## <a name="description"></a><span data-ttu-id="449a1-107">説明</span><span class="sxs-lookup"><span data-stu-id="449a1-107">Description</span></span>

<span data-ttu-id="449a1-108">`dotnet tool list` コマンドは、マシン上 (現在のユーザー プロファイル) または指定したパスにインストールされたユーザー全体のすべての .NET Core グローバル ツールを一覧表示する方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="449a1-108">The `dotnet tool list` command provides a way for you to list all .NET Core Global Tools installed user-wide on your machine (current user profile) or in the specified path.</span></span> <span data-ttu-id="449a1-109">このコマンドは、パッケージ名、インストールされているバージョン、およびグローバル ツールのコマンドを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="449a1-109">The command lists the package name, version installed, and the Global Tool command.</span></span> <span data-ttu-id="449a1-110">list コマンドを使用するには、`--global` オプションを使用してユーザー全体のツールをすべて表示することを指定するか、`--tool-path` オプションを使用してカスタム パスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="449a1-110">To use the list command, you either have to specify that you want to see all user-wide tools using the `--global` option or specify a custom path using the `--tool-path` option.</span></span>

## <a name="options"></a><span data-ttu-id="449a1-111">オプション</span><span class="sxs-lookup"><span data-stu-id="449a1-111">Options</span></span>

`-g|--global`

<span data-ttu-id="449a1-112">ユーザー全体のグローバル ツールを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="449a1-112">Lists user-wide Global Tools.</span></span> <span data-ttu-id="449a1-113">`--tool-path` オプションと組み合わせることはできません。</span><span class="sxs-lookup"><span data-stu-id="449a1-113">Can't be combined with the `--tool-path` option.</span></span> <span data-ttu-id="449a1-114">このオプションを指定しない場合は、`--tool-path` オプションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="449a1-114">If you don't specify this option, you must specify the `--tool-path` option.</span></span>

`-h|--help`

<span data-ttu-id="449a1-115">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="449a1-115">Prints out a short help for the command.</span></span>

`--tool-path <PATH>`

<span data-ttu-id="449a1-116">グローバル ツールを検索するカスタムの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="449a1-116">Specifies a custom location where to find Global Tools.</span></span> <span data-ttu-id="449a1-117">パスは絶対パスでも相対パスでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="449a1-117">PATH can be absolute or relative.</span></span> <span data-ttu-id="449a1-118">`--global` オプションと組み合わせることはできません。</span><span class="sxs-lookup"><span data-stu-id="449a1-118">Can't be combined with the `--global` option.</span></span> <span data-ttu-id="449a1-119">このオプションを指定しない場合は、`--global` オプションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="449a1-119">If you don't specify this option, you must specify the `--global` option.</span></span>

## <a name="examples"></a><span data-ttu-id="449a1-120">使用例</span><span class="sxs-lookup"><span data-stu-id="449a1-120">Examples</span></span>

<span data-ttu-id="449a1-121">マシン (現在のユーザー プロファイル) 上にユーザー全体でインストールされているすべてのグローバル ツールを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="449a1-121">Lists all Global Tools installed user-wide on your machine (current user profile):</span></span>

`dotnet tool list -g`

<span data-ttu-id="449a1-122">特定の Windows フォルダーからグローバル ツールを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="449a1-122">Lists the Global Tools from a specific Windows folder:</span></span>

`dotnet tool list --tool-path c:\global-tools`

<span data-ttu-id="449a1-123">特定の Linux/macOS フォルダーからグローバル ツールを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="449a1-123">Lists the Global Tools from a specific Linux/macOS folder:</span></span>

`dotnet tool list --tool-path ~/bin`

## <a name="see-also"></a><span data-ttu-id="449a1-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="449a1-124">See also</span></span>

* [<span data-ttu-id="449a1-125">.NET Core グローバル ツール</span><span class="sxs-lookup"><span data-stu-id="449a1-125">.NET Core Global Tools</span></span>](global-tools.md)