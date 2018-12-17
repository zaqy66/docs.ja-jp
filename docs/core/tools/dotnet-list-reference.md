---
title: dotnet list reference コマンド - .NET Core CLI
description: dotnet list 参照コマンドは、プロジェクト間参照を列挙する便利なオプションを提供します。
ms.date: 12/03/2018
ms.openlocfilehash: 58b4e07abfe95d1febdd54d117825ecedf502e61
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152606"
---
# <a name="dotnet-list-reference"></a><span data-ttu-id="6abe9-103">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="6abe9-103">dotnet list reference</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="6abe9-104">name</span><span class="sxs-lookup"><span data-stu-id="6abe9-104">Name</span></span>

<span data-ttu-id="6abe9-105">`dotnet list reference` - プロジェクト間参照を列挙します。</span><span class="sxs-lookup"><span data-stu-id="6abe9-105">`dotnet list reference` - Lists project-to-project references.</span></span>

## <a name="synopsis"></a><span data-ttu-id="6abe9-106">構文</span><span class="sxs-lookup"><span data-stu-id="6abe9-106">Synopsis</span></span>

`dotnet list [<PROJECT>] reference [-h|--help]`

## <a name="description"></a><span data-ttu-id="6abe9-107">説明</span><span class="sxs-lookup"><span data-stu-id="6abe9-107">Description</span></span>

<span data-ttu-id="6abe9-108">`dotnet list reference` コマンドは、特定のプロジェクトまたはソリューションのプロジェクト参照を列挙する便利なオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="6abe9-108">The `dotnet list reference` command provides a convenient option to list project references for a given project or solution.</span></span>

## <a name="arguments"></a><span data-ttu-id="6abe9-109">引数</span><span class="sxs-lookup"><span data-stu-id="6abe9-109">Arguments</span></span>

* **`PROJECT`**

  <span data-ttu-id="6abe9-110">参照の一覧取得に使うプロジェクト ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="6abe9-110">Specifies the project file to use for listing references.</span></span> <span data-ttu-id="6abe9-111">指定されていない場合、コマンドではプロジェクト ファイルを現在のディレクトリで検索します。</span><span class="sxs-lookup"><span data-stu-id="6abe9-111">If not specified, the command searches the current directory for a project file.</span></span>

## <a name="options"></a><span data-ttu-id="6abe9-112">オプション</span><span class="sxs-lookup"><span data-stu-id="6abe9-112">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="6abe9-113">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="6abe9-113">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="6abe9-114">使用例</span><span class="sxs-lookup"><span data-stu-id="6abe9-114">Examples</span></span>

* <span data-ttu-id="6abe9-115">指定したプロジェクトのプロジェクト参照を列挙する:</span><span class="sxs-lookup"><span data-stu-id="6abe9-115">List the project references for the specified project:</span></span>

  ```console
  dotnet list app/app.csproj reference
  ```

* <span data-ttu-id="6abe9-116">現在のディレクトリ内のプロジェクトのプロジェクト参照を列挙する:</span><span class="sxs-lookup"><span data-stu-id="6abe9-116">List the project references for the project in the current directory:</span></span>

  ```console
  dotnet list reference
  ```