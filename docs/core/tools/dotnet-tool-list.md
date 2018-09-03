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
# <a name="dotnet-tool-list"></a>dotnet tool list

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a>name

`dotnet tool list` - マシン上の既定のディレクトリまたは指定したパスに現在インストールされているすべての [.NET Core グローバル ツール](global-tools.md)を一覧表示します。

## <a name="synopsis"></a>構文

```console
dotnet tool list <-g|--global>
dotnet tool list <--tool-path>
dotnet tool list <-h|--help>
```

## <a name="description"></a>説明

`dotnet tool list` コマンドは、マシン上 (現在のユーザー プロファイル) または指定したパスにインストールされたユーザー全体のすべての .NET Core グローバル ツールを一覧表示する方法を提供します。 このコマンドは、パッケージ名、インストールされているバージョン、およびグローバル ツールのコマンドを一覧表示します。 list コマンドを使用するには、`--global` オプションを使用してユーザー全体のツールをすべて表示することを指定するか、`--tool-path` オプションを使用してカスタム パスを指定する必要があります。

## <a name="options"></a>オプション

`-g|--global`

ユーザー全体のグローバル ツールを一覧表示します。 `--tool-path` オプションと組み合わせることはできません。 このオプションを指定しない場合は、`--tool-path` オプションを指定する必要があります。

`-h|--help`

コマンドの短いヘルプを印刷します。

`--tool-path <PATH>`

グローバル ツールを検索するカスタムの場所を指定します。 パスは絶対パスでも相対パスでもかまいません。 `--global` オプションと組み合わせることはできません。 このオプションを指定しない場合は、`--global` オプションを指定する必要があります。

## <a name="examples"></a>使用例

マシン (現在のユーザー プロファイル) 上にユーザー全体でインストールされているすべてのグローバル ツールを一覧表示します。

`dotnet tool list -g`

特定の Windows フォルダーからグローバル ツールを一覧表示します。

`dotnet tool list --tool-path c:\global-tools`

特定の Linux/macOS フォルダーからグローバル ツールを一覧表示します。

`dotnet tool list --tool-path ~/bin`

## <a name="see-also"></a>関連項目

* [.NET Core グローバル ツール](global-tools.md)