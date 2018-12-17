---
title: dotnet clean コマンド - .NET Core CLI
description: dotnet clean コマンドは現在のディレクトリを消去します。
ms.date: 12/04/2018
ms.openlocfilehash: 9930d2905f234e7125f27367cda36aa85ae23b87
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53144456"
---
# <a name="dotnet-clean"></a>dotnet clean

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>name

`dotnet clean` - プロジェクトの出力を消去します。

## <a name="synopsis"></a>構文

```
dotnet clean [<PROJECT>] [-c|--configuration] [-f|--framework] [-o|--output] [-r|--runtime] [-v|--verbosity]
dotnet clean [-h|--help]
```

## <a name="description"></a>説明

`dotnet clean` コマンドは、以前のビルドの出力を消去します。 [MSBuild ターゲット](/visualstudio/msbuild/msbuild-targets)として実装されます。そのため、コマンドの実行時にプロジェクトが評価されます。 ビルド中に作成された出力のみが消去されます。 中間 (*obj*) と最終出力 (*bin*) フォルダーの両方が消去されます。

## <a name="arguments"></a>引数

`PROJECT`

消去する MSBuild プロジェクトです。 プロジェクト ファイルを指定しない場合、MSBuild は、現在の作業ディレクトリから *proj* で終わるファイル名拡張子を検索し、そのファイルを使います。

## <a name="options"></a>オプション

* **`-c|--configuration {Debug|Release}`**

  ビルド構成を定義します。 既定値は `Debug` です。 このオプションは、ビルド時に指定した場合にのみ、消去時にも必要です。

* **`-f|--framework <FRAMEWORK>`**

  ビルド時に指定された[フレームワーク](../../standard/frameworks.md)です。 フレームワークは、[プロジェクト ファイル](csproj.md)で定義する必要があります。 ビルド時にフレームワークを指定した場合は、消去時にフレームワークを指定する必要があります。

* **`-h|--help`**

  コマンドの短いヘルプを印刷します。

* **`-o|--output <OUTPUT_DIRECTORY>`**

  ビルド出力が配置されたディレクトリです。 プロジェクトのビルド時にフレームワークを指定した場合、出力ディレクトリ スイッチと共に `-f|--framework <FRAMEWORK>` スイッチを指定します。

* **`-r|--runtime <RUNTIME_IDENTIFIER>`**

  指定したランタイムの出力フォルダーをクリーンアップします。 これは、[自己完結型の展開](../deploying/index.md#self-contained-deployments-scd)が作成された場合に使用されます。 .NET Core 2.0 SDK 以降、使用できるオプションです。

* **`-v|--verbosity <LEVEL>`**

  コマンドの詳細レベルを設定します。 指定できるレベルは、q[uiet]、m[inimal]、n[ormal]、d[etailed]、diag[nostic] です。

## <a name="examples"></a>使用例

* プロジェクトの既定のビルドを消去します。

  ```console
  dotnet clean
  ```

* リリース構成を使用してビルドされたプロジェクトを消去します。

  ```console
  dotnet clean --configuration Release
  ```