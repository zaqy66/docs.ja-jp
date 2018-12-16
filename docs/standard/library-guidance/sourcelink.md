---
title: SourceLink と .NET ライブラリ
description: SourceLink を使用して .NET ライブラリのデバッグ機能を改善するためのベスト プラクティス推奨事項。
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 3bc72e158a5773b656095f9ce58b442469f91e67
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53128929"
---
# <a name="sourcelink"></a>SourceLink

SourceLink は NuGet からの .NET アセンブリのソース コードを開発者がデバッグすることを可能にするテクノロジです。 SourceLink は NuGet パッケージの作成時に実行され、ソース コントロール メタデータをアセンブリとパッケージの内部に埋め込みます。 パッケージをダウンロードし、Visual Studio で SourceLink を有効にした開発者は、そのソース コードにステップ インできます。 SourceLink からは、効率的なデバッグを可能にするソース コントロール メタデータが提供されます。

## <a name="sourcelink-demo"></a>SourceLink デモ

> [!VIDEO https://www.youtube.com/embed/gyRGhCQPkB4?start=61]

## <a name="using-sourcelink"></a>SourceLink の使用

SourceLink の使用方法は、[dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub リポジトリにあります。

[NuGet パッケージ エクスプローラー](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer)を使用すれば、SourceLink メタデータがパッケージに正常に埋め込まれたことを確認できます。 `Repository` メタデータがコメント ID と共に存在すること、各ターゲットの .dll と共に .pdb ファイルが見つかることを確認します。

![NuGet パッケージ エクスプローラーの SourceLink](./media/sourcelink/nuget-package-explorer-sourcelink.png "NuGet パッケージ エクスプローラーの SourceLink")

**✔️ 検討** SourceLink を使用して、お使いのアセンブリと NuGet パッケージにソース管理のメタデータを追加する。

> [!TIP]
> デバッガー属性を型に追加することで開発者のデバッグ機能をさらに強化できます。
> * <xref:System.Diagnostics.DebuggerDisplayAttribute> では、デバッガーの変数ウィンドウでクラスやフィールドを表示する方法をカスタマイズできます。
> * <xref:System.Diagnostics.DebuggerStepThroughAttribute> では、デバッガーに対してコードのステップ インではなくステップ実行が指示されます。
> * <xref:System.Diagnostics.DebuggerBrowsableAttribute> では、デバッガー変数ウィンドウにメンバーを表示するかどうかが制御されます。

**✔️ 検討** NuGet パッケージにシンボル ファイル (`*.pdb`) を含める。

> 通常、[シンボル パッケージ](./nuget.md#symbol-packages)でシンボル ファイルを発行します。 現在、シンボル パッケージの主要なパブリック ホストは、SDK 形式のプロジェクトによって作成されたポータブル シンボル ファイル (`*.pdb`) をサポートしておらず、シンボル パッケージは便利ではありません。

>[!div class="step-by-step"]
>[前へ](dependencies.md)
>[次へ](publish-nuget-package.md)