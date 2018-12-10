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

* **`shutdown`**

  dotnet から起動されるビルド サーバーをシャットダウンします。 既定では、すべてのサーバーがシャットダウンされます。

## <a name="options"></a>オプション

* **`-h|--help`**

  コマンドの短いヘルプを印刷します。

* **`--msbuild`**

  MSBuild ビルド サーバーをシャットダウンします。

* **`--razor`**

  Razor ビルド サーバーをシャットダウンします。

* **`--vbcscompiler`**

  VB/C# コンパイラ ビルド サーバーをシャットダウンします。