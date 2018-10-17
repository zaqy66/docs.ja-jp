---
title: SourceLink および .NET ライブラリ
description: SourceLink を使用して .NET ライブラリのデバッグを改善するための推奨されるベスト プラクティスです。
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: fa4af47eaa5dd1510640c2bf0ebb2187b56efae0
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2018
ms.locfileid: "49370315"
---
# <a name="sourcelink"></a>SourceLink

SourceLink は、開発者が NuGet から .NET アセンブリのソース コードのデバッグを有効にするテクノロジです。 SourceLink は NuGet パッケージを作成するときに実行し、アセンブリとパッケージ内のソース コントロールのメタデータを埋め込みます。 パッケージをダウンロードし、Visual Studio で有効になっている SourceLink がある開発者は、そのソース コードにステップ インできます。 SourceLink では、優れたデバッグ エクスペリエンスを作成するソース コントロールのメタデータを提供します。

## <a name="sourcelink-demo"></a>SourceLink デモ

> [!VIDEO https://www.youtube.com/embed/gyRGhCQPkB4?start=61]

## <a name="using-sourcelink"></a>SourceLink を使用します。

SourceLink を使用するための手順で確認できます、 [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub リポジトリ。

使用することができます[NuGet パッケージ エクスプ ローラー](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) SourceLink メタデータがパッケージに正常に埋め込まれていることを確認します。 チェック、`Repository`メタデータがコメントの識別子を持つ存在し、各ターゲットの .dll で .pdb ファイルがあります。

![NuGet パッケージ エクスプ ローラーで SourceLink](./media/sourcelink/nuget-package-explorer-sourcelink.png "NuGet パッケージ エクスプ ローラーで SourceLink")

**✔️ をご検討ください**SourceLink を使用して、アセンブリと NuGet パッケージをソース コントロールのメタデータを追加します。

**✔️ をご検討ください**NuGet パッケージに PDB ファイルを含めます。

>[!div class="step-by-step"]
[前へ](./dependencies.md)
[次へ](./publish-nuget-package.md)
