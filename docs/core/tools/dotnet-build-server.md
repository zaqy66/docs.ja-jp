---
title: dotnet build-server コマンド - .NET Core CLI
description: dotnet build-server コマンドは、ビルドによって起動されたサーバーとやり取りします。
author: mairaw
ms.author: mairaw
ms.date: 07/02/2018
ms.openlocfilehash: 1c59c85f246b79c7e2552f704db5b4f076f9b502
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37404334"
---
# <a name="dotnet-build-server"></a><span data-ttu-id="30d8f-103">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="30d8f-103">dotnet build-server</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="30d8f-104">name</span><span class="sxs-lookup"><span data-stu-id="30d8f-104">Name</span></span>

<span data-ttu-id="30d8f-105">`dotnet build-server` - ビルドによって起動されたサーバーとやり取りします。</span><span class="sxs-lookup"><span data-stu-id="30d8f-105">`dotnet build-server` - Interacts with servers started by a build.</span></span>

## <a name="synopsis"></a><span data-ttu-id="30d8f-106">構文</span><span class="sxs-lookup"><span data-stu-id="30d8f-106">Synopsis</span></span>

```
dotnet build-server shutdown [--msbuild] [--razor] [--vbcscompiler]
dotnet build-server shutdown [-h|--help]
dotnet build-server [-h|--help]
```

## <a name="commands"></a><span data-ttu-id="30d8f-107">コマンド</span><span class="sxs-lookup"><span data-stu-id="30d8f-107">Commands</span></span>

`shutdown`

<span data-ttu-id="30d8f-108">dotnet から起動されるビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="30d8f-108">Shuts down build servers that are started from dotnet.</span></span> <span data-ttu-id="30d8f-109">既定では、すべてのサーバーがシャットダウンされます。</span><span class="sxs-lookup"><span data-stu-id="30d8f-109">By default, all servers are shut down.</span></span>

## <a name="options"></a><span data-ttu-id="30d8f-110">オプション</span><span class="sxs-lookup"><span data-stu-id="30d8f-110">Options</span></span>

`-h|--help`

<span data-ttu-id="30d8f-111">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="30d8f-111">Prints out a short help for the command.</span></span>

`--msbuild`

<span data-ttu-id="30d8f-112">MSBuild ビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="30d8f-112">Shuts down the MSBuild build server.</span></span>

`--razor`

<span data-ttu-id="30d8f-113">Razor ビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="30d8f-113">Shuts down the Razor build server.</span></span>

`--vbcscompiler`

<span data-ttu-id="30d8f-114">VB/C# コンパイラ ビルド サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="30d8f-114">Shuts down the VB/C# compiler build server.</span></span>
