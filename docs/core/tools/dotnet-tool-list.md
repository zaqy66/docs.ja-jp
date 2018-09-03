---
title: dotnet tool list コマンド - .NET Core CLI
description: dotnet tool list コマンドは、マシン上の指定された .NET Core グローバル ツールを一覧表示します。
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: e2bea974207d3098ed67b69ed16a72a03c44cd8b
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2018
ms.locfileid: "43467057"
---
# <a name="dotnet-tool-list"></a><span data-ttu-id="b4f7e-103">dotnet tool list</span><span class="sxs-lookup"><span data-stu-id="b4f7e-103">dotnet tool list</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="b4f7e-104">name</span><span class="sxs-lookup"><span data-stu-id="b4f7e-104">Name</span></span>

<span data-ttu-id="b4f7e-105">`dotnet tool list` - マシン上の既定のディレクトリまたは指定したパスに現在インストールされているすべての [.NET Core グローバル ツール](global-tools.md)を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-105">`dotnet tool list` - Lists all [.NET Core Global Tools](global-tools.md) currently installed in the default directory on your machine or in the specified path.</span></span>

## <a name="synopsis"></a><span data-ttu-id="b4f7e-106">構文</span><span class="sxs-lookup"><span data-stu-id="b4f7e-106">Synopsis</span></span>

```console
dotnet tool list <-g|--global>
dotnet tool list <--tool-path>
dotnet tool list <-h|--help>
```

## <a name="description"></a><span data-ttu-id="b4f7e-107">説明</span><span class="sxs-lookup"><span data-stu-id="b4f7e-107">Description</span></span>

<span data-ttu-id="b4f7e-108">`dotnet tool list` コマンドは、マシン上 (現在のユーザー プロファイル) または指定したパスにインストールされたユーザー全体のすべての .NET Core グローバル ツールを一覧表示する方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-108">The `dotnet tool list` command provides a way for you to list all .NET Core Global Tools installed user-wide on your machine (current user profile) or in the specified path.</span></span> <span data-ttu-id="b4f7e-109">このコマンドは、パッケージ名、インストールされているバージョン、およびグローバル ツールのコマンドを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-109">The command lists the package name, version installed, and the Global Tool command.</span></span> <span data-ttu-id="b4f7e-110">list コマンドを使用するには、`--global` オプションを使用してユーザー全体のツールをすべて表示することを指定するか、`--tool-path` オプションを使用してカスタム パスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-110">To use the list command, you either have to specify that you want to see all user-wide tools using the `--global` option or specify a custom path using the `--tool-path` option.</span></span>

## <a name="options"></a><span data-ttu-id="b4f7e-111">オプション</span><span class="sxs-lookup"><span data-stu-id="b4f7e-111">Options</span></span>

`-g|--global`

<span data-ttu-id="b4f7e-112">ユーザー全体のグローバル ツールを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-112">Lists user-wide Global Tools.</span></span> <span data-ttu-id="b4f7e-113">`--tool-path` オプションと組み合わせることはできません。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-113">Can't be combined with the `--tool-path` option.</span></span> <span data-ttu-id="b4f7e-114">このオプションを指定しない場合は、`--tool-path` オプションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-114">If you don't specify this option, you must specify the `--tool-path` option.</span></span>

`-h|--help`

<span data-ttu-id="b4f7e-115">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-115">Prints out a short help for the command.</span></span>

`--tool-path <PATH>`

<span data-ttu-id="b4f7e-116">グローバル ツールを検索するカスタムの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-116">Specifies a custom location where to find Global Tools.</span></span> <span data-ttu-id="b4f7e-117">パスは絶対パスでも相対パスでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-117">PATH can be absolute or relative.</span></span> <span data-ttu-id="b4f7e-118">`--global` オプションと組み合わせることはできません。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-118">Can't be combined with the `--global` option.</span></span> <span data-ttu-id="b4f7e-119">このオプションを指定しない場合は、`--global` オプションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-119">If you don't specify this option, you must specify the `--global` option.</span></span>

## <a name="examples"></a><span data-ttu-id="b4f7e-120">使用例</span><span class="sxs-lookup"><span data-stu-id="b4f7e-120">Examples</span></span>

<span data-ttu-id="b4f7e-121">マシン (現在のユーザー プロファイル) 上にユーザー全体でインストールされているすべてのグローバル ツールを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-121">Lists all Global Tools installed user-wide on your machine (current user profile):</span></span>

`dotnet tool list -g`

<span data-ttu-id="b4f7e-122">特定の Windows フォルダーからグローバル ツールを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-122">Lists the Global Tools from a specific Windows folder:</span></span>

`dotnet tool list --tool-path c:\global-tools`

<span data-ttu-id="b4f7e-123">特定の Linux/macOS フォルダーからグローバル ツールを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b4f7e-123">Lists the Global Tools from a specific Linux/macOS folder:</span></span>

`dotnet tool list --tool-path ~/bin`

## <a name="see-also"></a><span data-ttu-id="b4f7e-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4f7e-124">See also</span></span>

* [<span data-ttu-id="b4f7e-125">.NET Core グローバル ツール</span><span class="sxs-lookup"><span data-stu-id="b4f7e-125">.NET Core Global Tools</span></span>](global-tools.md)