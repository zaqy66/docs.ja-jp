---
title: dotnet build-server コマンド - .NET Core CLI
description: dotnet build-server コマンドは、ビルドによって起動されたサーバーとやり取りします。
ms.date: 12/04/2018
ms.openlocfilehash: 2746ade12cc819089258483e84a8c0f02a64c755
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53125679"
---
# <a name="dotnet-build-server"></a><span data-ttu-id="2aa75-103">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="2aa75-103">dotnet build-server</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="2aa75-104">name</span><span class="sxs-lookup"><span data-stu-id="2aa75-104">Name</span></span>

<span data-ttu-id="2aa75-105">`dotnet build-server` - ビルドによって起動されたサーバーとやり取りします。</span><span class="sxs-lookup"><span data-stu-id="2aa75-105">`dotnet build-server` - Interacts with servers started by a build.</span></span>

## <a name="synopsis"></a><span data-ttu-id="2aa75-106">構文</span><span class="sxs-lookup"><span data-stu-id="2aa75-106">Synopsis</span></span>

```
dotnet build-server shutdown [--msbuild] [--razor] [--vbcscompiler]
dotnet build-server shutdown [-h|--help]
dotnet build-server [-h|--help]
```

## <a name="commands"></a><span data-ttu-id="2aa75-107">コマンド</span><span class="sxs-lookup"><span data-stu-id="2aa75-107">Commands</span></span>

* **`shutdown`**

  <span data-ttu-id="2aa75-108">dotnet から起動されるビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="2aa75-108">Shuts down build servers that are started from dotnet.</span></span> <span data-ttu-id="2aa75-109">既定では、すべてのサーバーがシャットダウンされます。</span><span class="sxs-lookup"><span data-stu-id="2aa75-109">By default, all servers are shut down.</span></span>

## <a name="options"></a><span data-ttu-id="2aa75-110">オプション</span><span class="sxs-lookup"><span data-stu-id="2aa75-110">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="2aa75-111">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="2aa75-111">Prints out a short help for the command.</span></span>

* **`--msbuild`**

  <span data-ttu-id="2aa75-112">MSBuild ビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="2aa75-112">Shuts down the MSBuild build server.</span></span>

* **`--razor`**

  <span data-ttu-id="2aa75-113">Razor ビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="2aa75-113">Shuts down the Razor build server.</span></span>

* **`--vbcscompiler`**

  <span data-ttu-id="2aa75-114">VB/C# コンパイラ ビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="2aa75-114">Shuts down the VB/C# compiler build server.</span></span>