---
title: dotnet msbuild コマンド
description: dotnet msbuild コマンドは、MSBuild コマンド ラインへのアクセスを提供します。
ms.date: 12/03/2018
ms.openlocfilehash: f025b5b92e57c7b804b9bdd59c8b4a4a806796da
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169080"
---
# <a name="dotnet-msbuild"></a>dotnet msbuild

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>name

`dotnet msbuild` - プロジェクトとそのすべての依存関係をビルドします。

## <a name="synopsis"></a>構文

`dotnet msbuild <msbuild_arguments> [-h]`

## <a name="description"></a>説明

`dotnet msbuild` コマンドでは、完全に機能する MSBuild へのアクセスを許可します。

このコマンドには、SDK スタイルのプロジェクトに対してのみ、既存の MSBuild コマンド ライン クライアントとまったく同じ機能があります。 オプションはすべて同じです。 使用可能なオプションの詳細については、「[MSBuild コマンド ライン リファレンス](/visualstudio/msbuild/msbuild-command-line-reference)」を参照してください。

[dotnet build](dotnet-build.md) コマンドは、`dotnet msbuild -restore -target:Build` に相当します。 プロジェクトの構築では `dotnet build` のほうが一般的に使用されますが、`dotnet msbuild` のほうが細かい制御を実行できます。 たとえば、実行したい特定のターゲットがあるが、ビルドしたターゲットを実行したくない場合は、`dotnet msbuild` を使用できます。

## <a name="examples"></a>使用例

* プロジェクトとその依存関係をビルドします。

  ```console
  dotnet msbuild
  ```

* リリース構成を使用して、プロジェクトとその依存関係をビルドします。

  ```console
  dotnet msbuild -p:Configuration=Release
  ```

* 発行先を実行して、RID `osx.10.11-x64` に発行します。

  ```console
  dotnet msbuild -t:Publish -p:RuntimeIdentifiers=osx.10.11-x64
  ```

* プロジェクト全体と SDK に付属するすべてのターゲットをご覧ください。

  ```console
  dotnet msbuild -pp
  ```