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
# <a name="dotnet-remove-package"></a>dotnet remove package

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>name

`dotnet remove package` - プロジェクト ファイルからパッケージ参照を削除します。

## <a name="synopsis"></a>構文

`dotnet remove [<PROJECT>] package <PACKAGE_NAME> [-h|--help]`

## <a name="description"></a>説明

`dotnet remove package` コマンドは、NuGet パッケージ参照をプロジェクトから削除する便利なオプションを提供します。

## <a name="arguments"></a>引数

`PROJECT`

プロジェクト ファイルを指定します。 指定されていない場合、現在のディレクトリで検索されます。

`PACKAGE_NAME`

削除するパッケージ参照。

## <a name="options"></a>オプション

`-h|--help`

コマンドの短いヘルプを印刷します。

## <a name="examples"></a>使用例

現在のディレクトリにあるプロジェクトから `Newtonsoft.Json` NuGet パッケージを削除する:

`dotnet remove package Newtonsoft.Json`