---
title: dotnet remove package コマンド
description: dotnet remove package コマンドは、プロジェクトへの NuGet パッケージ参照を削除する便利なオプションを提供します。
ms.date: 05/29/2018
ms.openlocfilehash: 4cc8ac927b761547dc5e53be9abeba827bf1e1d9
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53168729"
---
# <a name="dotnet-remove-package"></a><span data-ttu-id="ee23f-103">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="ee23f-103">dotnet remove package</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="ee23f-104">name</span><span class="sxs-lookup"><span data-stu-id="ee23f-104">Name</span></span>

<span data-ttu-id="ee23f-105">`dotnet remove package` - プロジェクト ファイルからパッケージ参照を削除します。</span><span class="sxs-lookup"><span data-stu-id="ee23f-105">`dotnet remove package` - Removes package reference from a project file.</span></span>

## <a name="synopsis"></a><span data-ttu-id="ee23f-106">構文</span><span class="sxs-lookup"><span data-stu-id="ee23f-106">Synopsis</span></span>

`dotnet remove [<PROJECT>] package <PACKAGE_NAME> [-h|--help]`

## <a name="description"></a><span data-ttu-id="ee23f-107">説明</span><span class="sxs-lookup"><span data-stu-id="ee23f-107">Description</span></span>

<span data-ttu-id="ee23f-108">`dotnet remove package` コマンドは、NuGet パッケージ参照をプロジェクトから削除する便利なオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="ee23f-108">The `dotnet remove package` command provides a convenient option to remove a NuGet package reference from a project.</span></span>

## <a name="arguments"></a><span data-ttu-id="ee23f-109">引数</span><span class="sxs-lookup"><span data-stu-id="ee23f-109">Arguments</span></span>

`PROJECT`

<span data-ttu-id="ee23f-110">プロジェクト ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee23f-110">Specifies the project file.</span></span> <span data-ttu-id="ee23f-111">指定されていない場合、現在のディレクトリで検索されます。</span><span class="sxs-lookup"><span data-stu-id="ee23f-111">If not specified, the command searches the current directory for one.</span></span>

`PACKAGE_NAME`

<span data-ttu-id="ee23f-112">削除するパッケージ参照。</span><span class="sxs-lookup"><span data-stu-id="ee23f-112">The package reference to remove.</span></span>

## <a name="options"></a><span data-ttu-id="ee23f-113">オプション</span><span class="sxs-lookup"><span data-stu-id="ee23f-113">Options</span></span>

`-h|--help`

<span data-ttu-id="ee23f-114">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="ee23f-114">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="ee23f-115">使用例</span><span class="sxs-lookup"><span data-stu-id="ee23f-115">Examples</span></span>

<span data-ttu-id="ee23f-116">現在のディレクトリにあるプロジェクトから `Newtonsoft.Json` NuGet パッケージを削除する:</span><span class="sxs-lookup"><span data-stu-id="ee23f-116">Removes `Newtonsoft.Json` NuGet package from a project in the current directory:</span></span>

`dotnet remove package Newtonsoft.Json`