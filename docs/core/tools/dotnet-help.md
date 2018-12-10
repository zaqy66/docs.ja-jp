---
title: dotnet help コマンド - .NET Core CLI
description: dotnet help コマンドでは、指定したコマンドについてより詳細なドキュメントがオンラインで表示されます。
ms.date: 12/04/2018
ms.openlocfilehash: 60d1cc706ca5c78fa3be877bd679888181213e88
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152176"
---
# <a name="dotnet-help-reference"></a><span data-ttu-id="8d6fa-103">dotnet help reference</span><span class="sxs-lookup"><span data-stu-id="8d6fa-103">dotnet help reference</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-2plus.md)]

## <a name="name"></a><span data-ttu-id="8d6fa-104">name</span><span class="sxs-lookup"><span data-stu-id="8d6fa-104">Name</span></span>

<span data-ttu-id="8d6fa-105">`dotnet help` - 指定したコマンドについて、より詳細なドキュメントがオンラインで表示されます。</span><span class="sxs-lookup"><span data-stu-id="8d6fa-105">`dotnet help` - Shows more detailed documentation online for the specified command.</span></span>

## <a name="synopsis"></a><span data-ttu-id="8d6fa-106">構文</span><span class="sxs-lookup"><span data-stu-id="8d6fa-106">Synopsis</span></span>

`dotnet help <COMMAND_NAME> [-h|--help]`

## <a name="description"></a><span data-ttu-id="8d6fa-107">説明</span><span class="sxs-lookup"><span data-stu-id="8d6fa-107">Description</span></span>

<span data-ttu-id="8d6fa-108">`dotnet help` コマンドは、docs.microsoft.com で、指定したコマンドに関する詳細情報のリファレンス ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8d6fa-108">The `dotnet help` command opens up the reference page for more detailed information about the specified command at docs.microsoft.com.</span></span>

## <a name="arguments"></a><span data-ttu-id="8d6fa-109">引数</span><span class="sxs-lookup"><span data-stu-id="8d6fa-109">Arguments</span></span>

* **`COMMAND_NAME`**

  <span data-ttu-id="8d6fa-110">.NET Core CLI コマンドの名前です。</span><span class="sxs-lookup"><span data-stu-id="8d6fa-110">Name of the .NET Core CLI command.</span></span> <span data-ttu-id="8d6fa-111">有効な CLI コマンドの一覧については、[CLI コマンド](index.md#cli-commands)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d6fa-111">For a list of the valid CLI commands, see [CLI commands](index.md#cli-commands).</span></span>

## <a name="options"></a><span data-ttu-id="8d6fa-112">オプション</span><span class="sxs-lookup"><span data-stu-id="8d6fa-112">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="8d6fa-113">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="8d6fa-113">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="8d6fa-114">使用例</span><span class="sxs-lookup"><span data-stu-id="8d6fa-114">Examples</span></span>

* <span data-ttu-id="8d6fa-115">ドキュメントの [dotnet new](dotnet-new.md) コマンドに関するページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8d6fa-115">Opens the documentation page for the [dotnet new](dotnet-new.md) command:</span></span>

  ```console
  dotnet help new
  ```