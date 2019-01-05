---
title: dotnet build-server コマンド
description: dotnet build-server コマンドは、ビルドによって起動されたサーバーとやり取りします。
ms.date: 12/04/2018
ms.openlocfilehash: 7f78a0cae6e3297f3084754dc56b0da4eac38caf
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169660"
---
# <a name="dotnet-build-server"></a><span data-ttu-id="f36b9-103">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="f36b9-103">dotnet build-server</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="f36b9-104">name</span><span class="sxs-lookup"><span data-stu-id="f36b9-104">Name</span></span>

<span data-ttu-id="f36b9-105">`dotnet build-server` - ビルドによって起動されたサーバーとやり取りします。</span><span class="sxs-lookup"><span data-stu-id="f36b9-105">`dotnet build-server` - Interacts with servers started by a build.</span></span>

## <a name="synopsis"></a><span data-ttu-id="f36b9-106">構文</span><span class="sxs-lookup"><span data-stu-id="f36b9-106">Synopsis</span></span>

```
dotnet build-server shutdown [--msbuild] [--razor] [--vbcscompiler]
dotnet build-server shutdown [-h|--help]
dotnet build-server [-h|--help]
```

## <a name="commands"></a><span data-ttu-id="f36b9-107">コマンド</span><span class="sxs-lookup"><span data-stu-id="f36b9-107">Commands</span></span>

* **`shutdown`**

  <span data-ttu-id="f36b9-108">dotnet から起動されるビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="f36b9-108">Shuts down build servers that are started from dotnet.</span></span> <span data-ttu-id="f36b9-109">既定では、すべてのサーバーがシャットダウンされます。</span><span class="sxs-lookup"><span data-stu-id="f36b9-109">By default, all servers are shut down.</span></span>

## <a name="options"></a><span data-ttu-id="f36b9-110">オプション</span><span class="sxs-lookup"><span data-stu-id="f36b9-110">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="f36b9-111">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="f36b9-111">Prints out a short help for the command.</span></span>

* **`--msbuild`**

  <span data-ttu-id="f36b9-112">MSBuild ビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="f36b9-112">Shuts down the MSBuild build server.</span></span>

* **`--razor`**

  <span data-ttu-id="f36b9-113">Razor ビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="f36b9-113">Shuts down the Razor build server.</span></span>

* **`--vbcscompiler`**

  <span data-ttu-id="f36b9-114">VB/C# コンパイラ ビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="f36b9-114">Shuts down the VB/C# compiler build server.</span></span>