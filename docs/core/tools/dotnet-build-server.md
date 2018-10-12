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
# <a name="dotnet-build-server"></a>dotnet build-server

[!INCLUDE [topic-appliesto-net-core-21plus](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a>name

`dotnet build-server` - ビルドによって起動されたサーバーとやり取りします。

## <a name="synopsis"></a>構文

```
dotnet build-server shutdown [--msbuild] [--razor] [--vbcscompiler]
dotnet build-server shutdown [-h|--help]
dotnet build-server [-h|--help]
```

## <a name="commands"></a>コマンド

`shutdown`

dotnet から起動されるビルド サーバーをシャットダウンします。 既定では、すべてのサーバーがシャットダウンされます。

## <a name="options"></a>オプション

`-h|--help`

コマンドの短いヘルプを印刷します。

`--msbuild`

MSBuild ビルド サーバーをシャットダウンします。

`--razor`

Razor ビルド サーバーをシャットダウンします。

`--vbcscompiler`

VB/C# コンパイラ ビルド サーバーをシャットダウンします。
