---
title: NuGet と .NET ライブラリ
description: .NET ライブラリの nuget のパッケージ化の推奨されるベスト プラクティスです。
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: d0ea462a7f52dd9a6b2f14be9ed5770160bf66b1
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374503"
---
# <a name="nuget"></a>NuGet

NuGet では、.NET エコシステムのパッケージ マネージャーし、は主な方法は開発者が発見し、.NET オープン ソース ライブラリを取得します。 [NuGet.org](https://www.nuget.org/)、NuGet パッケージをホストするために、Microsoft によって提供される無料のサービスは、パブリック NuGet パッケージのプライマリ ホストが、カスタム NuGet サービスに発行することができます、 [MyGet](https://www.myget.org/)と[Azure 成果物](https://azure.microsoft.com/services/devops/artifacts/).

![NuGet](./media/nuget/nuget-logo.png "NuGet")

## <a name="create-a-nuget-package"></a>NuGet パッケージを作成します。

NuGet パッケージ (`*.nupkg`) は .NET アセンブリと関連メタデータを含む zip ファイルです。

NuGet パッケージを作成する 2 つの主な方法はあります。 SDK スタイル プロジェクトからパッケージを作成する、新しい推奨される方法は、(プロジェクト ファイルの内容が始まる`<Project Sdk="Microsoft.NET.Sdk">`)。 アセンブリとターゲットがパッケージに自動的に追加し、残りのメタデータがパッケージの名前とバージョン番号のように、MSBuild ファイルに追加します。 コンパイルすると、 [ `dotnet pack` ](../../core/tools/dotnet-pack.md)コマンドの出力を`*.nupkg`アセンブリではなくファイル。

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <TargetFramework>netstandard2.0</TargetFramework>
    <AssemblyName>Contoso.Api</AssemblyName>
    <PackageVersion>1.1.0</PackageVersion>
    <Authors>John Doe</Authors>
  </PropertyGroup>
</Project>
```

従来の NuGet パッケージの作成の方法は、`*.nuspec`ファイルと`nuget.exe`コマンド ライン ツール。 優れたの nuspec ファイルに制御できますが、最終的な NuGet パッケージに含めるにはどのようなアセンブリとターゲットを慎重に指定する必要があります。 間違いやすいまたは他のユーザーを忘れずに変更を加える場合は、nuspec を更新します。 使用できます、nuspec の利点は、SDK スタイル プロジェクトのファイルをサポートしないフレームワーク用 NuGet パッケージを作成します。

**✔️ をご検討ください**SDK スタイル プロジェクト ファイルを使用した NuGet パッケージを作成します。

**✔️ をご検討ください**アセンブリや NuGet パッケージにソース コントロールのメタデータを追加する SourceLink を設定します。

## <a name="package-dependencies"></a>パッケージの依存関係

NuGet パッケージの依存関係での詳細については、[依存関係](./dependencies.md)記事。

## <a name="important-nuget-package-metadata"></a>重要な NuGet パッケージ メタデータ

NuGet パッケージの多くをサポートしている[メタデータ プロパティ](/nuget/reference/nuspec)します。 次の表には、すべてのオープン ソース プロジェクトが提供するコア メタデータが含まれています。

| MSBuild プロパティ名              | Nuspec 名              | 説明  |
| ---------------------------------- | ------------------------ | ------------ |
| `PackageId`                        | `id`                       | パッケージの識別子です。 満たしている場合、識別子のプレフィックスを予約できる、[条件](/nuget/reference/id-prefix-reservation)します。 |
| `PackageVersion`                   | `version`                  | NuGet パッケージのバージョン。 詳細については、次を参照してください。 [NuGet パッケージ バージョン](./versioning.md#nuget-package-version)します。             |
| `Title`                            | `title`                    | パッケージのわかりやすいタイトルです。 既定値は、`PackageId`します。             |
| `Description`                      | `description`              | UI に表示されるパッケージの長い説明。             |
| `Authors`                          | `authors`                  | Nuget.org のプロファイル名に一致するパッケージの作成者のコンマ区切りの一覧。             |
| `PackageTags`                      | `tags`                     | パッケージを記述するタグやキーワードのスペースで区切られた一覧。 タグは、パッケージを検索するときに使用されます。             |
| `PackageIconUrl`                   | `iconUrl`                  | パッケージのアイコンとして使用するイメージの URL。 URL が HTTPS にする必要があり、イメージが 64 x 64 に透明な背景。             |
| `PackageProjectUrl`                | `projectUrl`               | プロジェクトのホーム ページまたはソース リポジトリの URL。             |
| `PackageLicenseUrl`                | `licenseUrl`               | プロジェクトのライセンスの URL。 URL を指定できます、`LICENSE`ソース管理内のファイル。             |

**✔️ をご検討ください**NuGet のプレフィックスの予約を満たしているプレフィックスを持つ NuGet パッケージの名前を選択する[条件](/nuget/reference/id-prefix-reservation)します。

**✔️ をご検討ください**を使用して、`LICENSE`としてソース管理内のファイル、`LicenseUrl`します。 たとえば、 [LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md)します。

> [!IMPORTANT]
> ライセンスの既定値なしのプロジェクト[排他著作権](https://choosealicense.com/no-permission/)、他のユーザーが使用できなくなります。

**✔️ は**パッケージ アイコンに HTTPS href を使用します。

> NuGet.org のようなサイトは、HTTPS が有効で実行され、HTTPS 以外のイメージを表示すると、混合コンテンツ警告が作成されます。

**✔️ は**64 x 64 が、結果を表示する最良の透明な背景パッケージ アイコン イメージを使用します。

## <a name="pre-release-packages"></a>プレリリース パッケージ

NuGet パッケージのバージョン サフィックスを持つ読晗ェホロ[プレリリース](/nuget/create-packages/prerelease-packages)します。 既定では、NuGet パッケージ マネージャー UI では、ユーザー opts にプレリリース パッケージをプレリリース パッケージを制限付きユーザーのテストに最適に行う場合を除きに安定したリリースが表示されます。

```xml
<PackageVersion>1.0.1-beta1</PackageVersion>
```

> [!NOTE]
> 安定したパッケージは、プレリリース版のパッケージに依存できません。 独自のパッケージのプレリリース版を行うか、または以前の安定したバージョンに依存する必要があります。

![NuGet プレリリース パッケージの依存関係](./media/nuget/nuget-prerelease-package.png "NuGet プレリリース パッケージの依存関係")

**✔️ は**テスト、プレビュー、または実験時にプレリリース パッケージを発行します。

**✔️ は**その準備完了他の安定版パッケージ参照できる場合に、安定したパッケージを発行します。

## <a name="symbol-packages"></a>シンボル パッケージ

NuGet をサポートしています[別のシンボル パッケージを生成する](/nuget/create-packages/symbol-packages)を含む .NET アセンブリを含むメイン パッケージと共に PDB ファイルをデバッグします。 シンボル パッケージの考え方は、シンボル サーバー上でホストする、Visual Studio などのツールをオンデマンドでダウンロードされるのみです。

シンボルのメインのパブリック ホストに現在[SymbolSource](http://www.symbolsource.org/) -作成された、ポータブル Pdb をサポートしていない SDK スタイル プロジェクト、シンボル パッケージ役に立たない。

**✔️ をご検討ください**メイン NuGet パッケージに Pdb を埋め込みます。

**❌ 避け**Pdb が含まれるシンボル パッケージを作成します。

>[!div class="step-by-step"]
[前へ](./strong-naming.md)
[次へ](./dependencies.md)
