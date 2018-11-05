---
title: NuGet および .NET ライブラリ
description: .NET ライブラリ対応の NuGet によるパッケージ化のベスト プラクティスの推奨事項
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 479d1786c232ef1f843877169954e847453681c9
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50185625"
---
# <a name="nuget"></a>NuGet

NuGet は .NET エコシステムのパッケージ マネージャーであり、開発者が .NET オープンソース ライブラリを見つけて入手するための主要な方法です。 NuGet パッケージをホストするために Microsoft が提供している無料サービスの [NuGet.org](https://www.nuget.org/) は、パブリック NuGet パッケージのプライマリ ホストですが、[MyGet](https://www.myget.org/) および [Azure Artifacts](https://azure.microsoft.com/services/devops/artifacts/) などのカスタム NuGet サービスに公開できます。

![NuGet](./media/nuget/nuget-logo.png "NuGet")

## <a name="create-a-nuget-package"></a>NuGet パッケージの作成

NuGet パッケージ (`*.nupkg`) は、.NET アセンブリと関連するメタデータを含む zip ファイルです。

NuGet パッケージを作成するには、主な方法が 2 つあります。 より新しいお勧めの方法は、SDK 形式のプロジェクト (コンテンツが `<Project Sdk="Microsoft.NET.Sdk">` から始まるプロジェクト ファイル) からパッケージを作成することです。 アセンブリとターゲットが自動的にパッケージに追加され、パッケージ名やバージョン番号などの残りのメタデータが、MSBuild ファイルに追加されます。 [`dotnet pack`](../../core/tools/dotnet-pack.md) コマンドを使ってコンパイルすると、アセンブリの代わりに `*.nupkg` ファイルが出力されます。

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

NuGet パッケージを作成する従来からの方法では、`*.nuspec` ファイルと `nuget.exe` コマンドライン ツールを使用します。 nuspec ファイルを使用すると、優れた制御を利用できますが、最終的な NuGet パッケージに含めるアセンブリとターゲットを慎重に指定する必要があります。 間違えやすいうえに、変更を加える際にユーザーは nuspec の更新を忘れやすいです。 nuspec の利点は、まだ SDK 形式のプロジェクト ファイルをサポートしていないフレームワークの NuGet パッケージを作成するために使用できることです。

**✔️ 検討** SDK 形式のプロジェクト ファイルを使用して、NuGet パッケージを作成する。

**✔️ 検討** SourceLink を設定して、お使いのアセンブリと NuGet パッケージにソース管理のメタデータを追加する。

## <a name="package-dependencies"></a>パッケージの依存関係

NuGet パッケージの依存関係については、「[Dependencies](./dependencies.md)」 (依存関係) の記事で説明しています。

## <a name="important-nuget-package-metadata"></a>重要な NuGet パッケージ メタデータ

NuGet パッケージは、多数の[メタデータ プロパティ](/nuget/reference/nuspec)をサポートしています。 次の表に、どのオープンソース プロジェクトでも指定する必要があるコア メタデータを示します。

| MSBuild プロパティの名前              | Nuspec の名前              | 説明  |
| ---------------------------------- | ------------------------ | ------------ |
| `PackageId`                        | `id`                       | パッケージ ID。 [条件](/nuget/reference/id-prefix-reservation)を満たしている場合、ID のプレフィックスは予約できます。 |
| `PackageVersion`                   | `version`                  | NuGet パッケージ バージョン。 詳細については、「[NuGet package version](./versioning.md#nuget-package-version)」(NuGet package version パッケージ バージョン) をご覧ください。             |
| `Title`                            | `title`                    | わかりやすいパッケージ タイトル。 既定値は `PackageId` です。             |
| `Description`                      | `description`              | UI に表示されるパッケージの長い説明。             |
| `Authors`                          | `authors`                  | パッケージ作成者のコンマで区切りの一覧。nuget.org のプロファイル名と一致します。             |
| `PackageTags`                      | `tags`                     | パッケージを説明するタグとキーワードのスペース区切りの一覧。 タグは、パッケージを検索するときに使用されます。             |
| `PackageIconUrl`                   | `iconUrl`                  | パッケージのアイコンとして使用するイメージの URL。 URL は HTTPS にする必要があり、イメージは 64 x 64 で透明な背景になっている必要があります。             |
| `PackageProjectUrl`                | `projectUrl`               | プロジェクトのホーム ページまたはソース リポジトリの URL。             |
| `PackageLicenseUrl`                | `licenseUrl`               | プロジェクト ライセンスの URL。 ソース管理の `LICENSE` ファイルの URL にすることもできます。             |

**✔️ 検討** NuGet のプレフィックスの予約[条件](/nuget/reference/id-prefix-reservation)を満たしているプレフィックスを持つ NuGet パッケージ名を選択する。

**✔️ 検討** ソース管理の `LICENSE` ファイルを `LicenseUrl` として使用する。 たとえば、[LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md)。

> [!IMPORTANT]
> ライセンス既定値が、他のユーザーからは使用できなくなる[排他的な著作権](https://choosealicense.com/no-permission/)に設定されていないプロジェクト。

**✔️ 実行** パッケージのアイコンに HTTPS href を使用する。

> NuGet.org のようなサイトは HTTPS を有効にした状態で実行され、HTTPS ではないイメージを表示すると、コンテンツの混合を示す警告が作成されます。

**✔️ 実行** 64 x 64 のパッケージ アイコン イメージを使用し、最善の表示結果を透明な背景にする。

## <a name="pre-release-packages"></a>プレリリース パッケージ

バージョン サフィックスがある NuGet パッケージは、[プレリリース](/nuget/create-packages/prerelease-packages)と見なされます。 プレリリース パッケージが制限付きユーザーのテスト実行に最適になるように、ユーザーがプレリリース パッケージを選択しない限り、既定では、NuGet パッケージ マネージャーの UI は、安定版リリースを表示します。

```xml
<PackageVersion>1.0.1-beta1</PackageVersion>
```

> [!NOTE]
> 安定版パッケージは、プレリリース パッケージに依存できません。 独自のパッケージをプレリリースにするか、または旧来の安定版バージョンに依存する必要があります。

![NuGet プレリリース パッケージの依存関係](./media/nuget/nuget-prerelease-package.png "NuGet プレリリース パッケージの依存関係")

**✔️ 実行** テスト、プレビュー、または実験時に、プレリリース パッケージを公開する。

**✔️ 実行** 他の安定版パッケージから参照できるように、準備ができ次第、安定版パッケージを公開する。

## <a name="symbol-packages"></a>シンボル パッケージ

シンボル ファイル (`*.pdb`) は、アセンブリと共に .NET コンパイラによって生成されます。 デバッガ―を使用して実行しながらソース コード全体をステップ実行できるように、シンボル ファイルは、実行場所を元のソース コードにマップします。 NuGet では、.NET アセンブリを含む主要なパッケージと共に、シンボル ファイルを格納している[別個のシンボル パッケージの生成](/nuget/create-packages/symbol-packages)をサポートしています。 シンボル サーバー上でホストされ、Visual Studio などのツールによってオンデマンドでしかダウンロードできないのが、シンボル パッケージの考え方です。

現在、シンボルの主要なパブリック ホスト ([SymbolSource](http://www.symbolsource.org/)) は、SDK 形式のプロジェクトによって作成された新しい[ポータブル シンボル ファイル](https://github.com/dotnet/core/blob/master/Documentation/diagnostics/portable_pdb.md) (`*.pdb`) をサポートしておらず、シンボル パッケージは便利ではありません。 シンボル パッケージに対応した推奨ホストができるまで、シンボル ファイルは主要な NuGet パッケージに埋め込むことができます。 SDK 形式のプロジェクトを使用して NuGet パッケージを構築している場合、`AllowedOutputExtensionsInPackageBuildOutputFolder` プロパティを設定してシンボル ファイルを埋め込むことができます。 

```xml
<Project Sdk="Microsoft.NET.Sdk">
 <PropertyGroup>
    <!-- Include symbol files (*.pdb) in the built .nupkg -->
    <AllowedOutputExtensionsInPackageBuildOutputFolder>$(AllowedOutputExtensionsInPackageBuildOutputFolder);.pdb</AllowedOutputExtensionsInPackageBuildOutputFolder>
  </PropertyGroup>
</Project>
```

**✔️ 検討** 主要な NuGet パッケージにシンボル ファイルを埋め込む。

**❌ 禁止**シンボル ファイルを含むシンボル パッケージを作成する。

>[!div class="step-by-step"]
[前へ](./strong-naming.md)
[次へ](./dependencies.md)
