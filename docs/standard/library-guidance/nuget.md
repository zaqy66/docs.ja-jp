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
# <a name="nuget"></a><span data-ttu-id="7346f-103">NuGet</span><span class="sxs-lookup"><span data-stu-id="7346f-103">NuGet</span></span>

<span data-ttu-id="7346f-104">NuGet では、.NET エコシステムのパッケージ マネージャーし、は主な方法は開発者が発見し、.NET オープン ソース ライブラリを取得します。</span><span class="sxs-lookup"><span data-stu-id="7346f-104">NuGet is a package manager for the .NET ecosystem and is the primary way developers discover and acquire .NET open-source libraries.</span></span> <span data-ttu-id="7346f-105">[NuGet.org](https://www.nuget.org/)、NuGet パッケージをホストするために、Microsoft によって提供される無料のサービスは、パブリック NuGet パッケージのプライマリ ホストが、カスタム NuGet サービスに発行することができます、 [MyGet](https://www.myget.org/)と[Azure 成果物](https://azure.microsoft.com/services/devops/artifacts/).</span><span class="sxs-lookup"><span data-stu-id="7346f-105">[NuGet.org](https://www.nuget.org/), a free service provided by Microsoft for hosting NuGet packages, is the primary host for public NuGet packages, but you can publish to custom NuGet services like [MyGet](https://www.myget.org/) and [Azure Artifacts](https://azure.microsoft.com/services/devops/artifacts/).</span></span>

<span data-ttu-id="7346f-106">![NuGet](./media/nuget/nuget-logo.png "NuGet")</span><span class="sxs-lookup"><span data-stu-id="7346f-106">![NuGet](./media/nuget/nuget-logo.png "NuGet")</span></span>

## <a name="create-a-nuget-package"></a><span data-ttu-id="7346f-107">NuGet パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="7346f-107">Create a NuGet package</span></span>

<span data-ttu-id="7346f-108">NuGet パッケージ (`*.nupkg`) は .NET アセンブリと関連メタデータを含む zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="7346f-108">A NuGet package (`*.nupkg`) is a zip file that contains .NET assemblies and associated metadata.</span></span>

<span data-ttu-id="7346f-109">NuGet パッケージを作成する 2 つの主な方法はあります。</span><span class="sxs-lookup"><span data-stu-id="7346f-109">There are two main ways to create a NuGet package.</span></span> <span data-ttu-id="7346f-110">SDK スタイル プロジェクトからパッケージを作成する、新しい推奨される方法は、(プロジェクト ファイルの内容が始まる`<Project Sdk="Microsoft.NET.Sdk">`)。</span><span class="sxs-lookup"><span data-stu-id="7346f-110">The newer and recommended way is to create a package from a SDK-style project (project file whose content starts with `<Project Sdk="Microsoft.NET.Sdk">`).</span></span> <span data-ttu-id="7346f-111">アセンブリとターゲットがパッケージに自動的に追加し、残りのメタデータがパッケージの名前とバージョン番号のように、MSBuild ファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="7346f-111">Assemblies and targets are automatically added to the package and remaining metadata is added to the MSBuild file, like package name and version number.</span></span> <span data-ttu-id="7346f-112">コンパイルすると、 [ `dotnet pack` ](../../core/tools/dotnet-pack.md)コマンドの出力を`*.nupkg`アセンブリではなくファイル。</span><span class="sxs-lookup"><span data-stu-id="7346f-112">Compiling with the [`dotnet pack`](../../core/tools/dotnet-pack.md) command outputs a `*.nupkg` file instead of assemblies.</span></span>

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

<span data-ttu-id="7346f-113">従来の NuGet パッケージの作成の方法は、`*.nuspec`ファイルと`nuget.exe`コマンド ライン ツール。</span><span class="sxs-lookup"><span data-stu-id="7346f-113">The older way of creating a NuGet package is with a `*.nuspec` file and the `nuget.exe` command-line tool.</span></span> <span data-ttu-id="7346f-114">優れたの nuspec ファイルに制御できますが、最終的な NuGet パッケージに含めるにはどのようなアセンブリとターゲットを慎重に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7346f-114">A nuspec file gives you great control but you must carefully specify what assemblies and targets to include in the final NuGet package.</span></span> <span data-ttu-id="7346f-115">間違いやすいまたは他のユーザーを忘れずに変更を加える場合は、nuspec を更新します。</span><span class="sxs-lookup"><span data-stu-id="7346f-115">It's easy to make a mistake or for someone to forget to update the nuspec when making changes.</span></span> <span data-ttu-id="7346f-116">使用できます、nuspec の利点は、SDK スタイル プロジェクトのファイルをサポートしないフレームワーク用 NuGet パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="7346f-116">The advantage of a nuspec is you can use it create NuGet packages for frameworks that don't yet support an SDK-style project file.</span></span>

<span data-ttu-id="7346f-117">**✔️ をご検討ください**SDK スタイル プロジェクト ファイルを使用した NuGet パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="7346f-117">**✔️ CONSIDER** using an SDK-style project file to create the NuGet package.</span></span>

<span data-ttu-id="7346f-118">**✔️ をご検討ください**アセンブリや NuGet パッケージにソース コントロールのメタデータを追加する SourceLink を設定します。</span><span class="sxs-lookup"><span data-stu-id="7346f-118">**✔️ CONSIDER** setting up SourceLink to add source control metadata to your assemblies and NuGet package.</span></span>

## <a name="package-dependencies"></a><span data-ttu-id="7346f-119">パッケージの依存関係</span><span class="sxs-lookup"><span data-stu-id="7346f-119">Package dependencies</span></span>

<span data-ttu-id="7346f-120">NuGet パッケージの依存関係での詳細については、[依存関係](./dependencies.md)記事。</span><span class="sxs-lookup"><span data-stu-id="7346f-120">NuGet package dependencies are covered in detail in the [Dependencies](./dependencies.md) article.</span></span>

## <a name="important-nuget-package-metadata"></a><span data-ttu-id="7346f-121">重要な NuGet パッケージ メタデータ</span><span class="sxs-lookup"><span data-stu-id="7346f-121">Important NuGet package metadata</span></span>

<span data-ttu-id="7346f-122">NuGet パッケージの多くをサポートしている[メタデータ プロパティ](/nuget/reference/nuspec)します。</span><span class="sxs-lookup"><span data-stu-id="7346f-122">A NuGet package supports many [metadata properties](/nuget/reference/nuspec).</span></span> <span data-ttu-id="7346f-123">次の表には、すべてのオープン ソース プロジェクトが提供するコア メタデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7346f-123">The following table contains the core metadata that every open-source project should provide:</span></span>

| <span data-ttu-id="7346f-124">MSBuild プロパティ名</span><span class="sxs-lookup"><span data-stu-id="7346f-124">MSBuild Property name</span></span>              | <span data-ttu-id="7346f-125">Nuspec 名</span><span class="sxs-lookup"><span data-stu-id="7346f-125">Nuspec name</span></span>              | <span data-ttu-id="7346f-126">説明</span><span class="sxs-lookup"><span data-stu-id="7346f-126">Description</span></span>  |
| ---------------------------------- | ------------------------ | ------------ |
| `PackageId`                        | `id`                       | <span data-ttu-id="7346f-127">パッケージの識別子です。</span><span class="sxs-lookup"><span data-stu-id="7346f-127">The package identifier.</span></span> <span data-ttu-id="7346f-128">満たしている場合、識別子のプレフィックスを予約できる、[条件](/nuget/reference/id-prefix-reservation)します。</span><span class="sxs-lookup"><span data-stu-id="7346f-128">A prefix from the identifier can be reserved if it meets the [criteria](/nuget/reference/id-prefix-reservation).</span></span> |
| `PackageVersion`                   | `version`                  | <span data-ttu-id="7346f-129">NuGet パッケージのバージョン。</span><span class="sxs-lookup"><span data-stu-id="7346f-129">NuGet package version.</span></span> <span data-ttu-id="7346f-130">詳細については、次を参照してください。 [NuGet パッケージ バージョン](./versioning.md#nuget-package-version)します。</span><span class="sxs-lookup"><span data-stu-id="7346f-130">For more information, see [NuGet package version](./versioning.md#nuget-package-version).</span></span>             |
| `Title`                            | `title`                    | <span data-ttu-id="7346f-131">パッケージのわかりやすいタイトルです。</span><span class="sxs-lookup"><span data-stu-id="7346f-131">A human-friendly title of the package.</span></span> <span data-ttu-id="7346f-132">既定値は、`PackageId`します。</span><span class="sxs-lookup"><span data-stu-id="7346f-132">It defaults to the `PackageId`.</span></span>             |
| `Description`                      | `description`              | <span data-ttu-id="7346f-133">UI に表示されるパッケージの長い説明。</span><span class="sxs-lookup"><span data-stu-id="7346f-133">A long description of the package displayed in UI.</span></span>             |
| `Authors`                          | `authors`                  | <span data-ttu-id="7346f-134">Nuget.org のプロファイル名に一致するパッケージの作成者のコンマ区切りの一覧。</span><span class="sxs-lookup"><span data-stu-id="7346f-134">A comma-separated list of package authors, matching the profile names on nuget.org.</span></span>             |
| `PackageTags`                      | `tags`                     | <span data-ttu-id="7346f-135">パッケージを記述するタグやキーワードのスペースで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="7346f-135">A space-delimited list of tags and keywords that describe the package.</span></span> <span data-ttu-id="7346f-136">タグは、パッケージを検索するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="7346f-136">Tags are used when searching for packages.</span></span>             |
| `PackageIconUrl`                   | `iconUrl`                  | <span data-ttu-id="7346f-137">パッケージのアイコンとして使用するイメージの URL。</span><span class="sxs-lookup"><span data-stu-id="7346f-137">A URL for an image to use as the icon for the package.</span></span> <span data-ttu-id="7346f-138">URL が HTTPS にする必要があり、イメージが 64 x 64 に透明な背景。</span><span class="sxs-lookup"><span data-stu-id="7346f-138">URL should be HTTPS and the image should be 64x64 and have a transparent background.</span></span>             |
| `PackageProjectUrl`                | `projectUrl`               | <span data-ttu-id="7346f-139">プロジェクトのホーム ページまたはソース リポジトリの URL。</span><span class="sxs-lookup"><span data-stu-id="7346f-139">A URL for the project homepage or source repository.</span></span>             |
| `PackageLicenseUrl`                | `licenseUrl`               | <span data-ttu-id="7346f-140">プロジェクトのライセンスの URL。</span><span class="sxs-lookup"><span data-stu-id="7346f-140">A URL to the project license.</span></span> <span data-ttu-id="7346f-141">URL を指定できます、`LICENSE`ソース管理内のファイル。</span><span class="sxs-lookup"><span data-stu-id="7346f-141">Can be the URL to the `LICENSE` file in source control.</span></span>             |

<span data-ttu-id="7346f-142">**✔️ をご検討ください**NuGet のプレフィックスの予約を満たしているプレフィックスを持つ NuGet パッケージの名前を選択する[条件](/nuget/reference/id-prefix-reservation)します。</span><span class="sxs-lookup"><span data-stu-id="7346f-142">**✔️ CONSIDER** choosing a NuGet package name with a prefix that meets NuGet's prefix reservation [criteria](/nuget/reference/id-prefix-reservation).</span></span>

<span data-ttu-id="7346f-143">**✔️ をご検討ください**を使用して、`LICENSE`としてソース管理内のファイル、`LicenseUrl`します。</span><span class="sxs-lookup"><span data-stu-id="7346f-143">**✔️ CONSIDER** using the `LICENSE` file in source control as the `LicenseUrl`.</span></span> <span data-ttu-id="7346f-144">たとえば、 [LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md)します。</span><span class="sxs-lookup"><span data-stu-id="7346f-144">For example, [LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7346f-145">ライセンスの既定値なしのプロジェクト[排他著作権](https://choosealicense.com/no-permission/)、他のユーザーが使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="7346f-145">A project without a license defaults to [exclusive copyright](https://choosealicense.com/no-permission/), making it impossible for other people to use.</span></span>

<span data-ttu-id="7346f-146">**✔️ は**パッケージ アイコンに HTTPS href を使用します。</span><span class="sxs-lookup"><span data-stu-id="7346f-146">**✔️ DO** use an HTTPS href to your package icon.</span></span>

> <span data-ttu-id="7346f-147">NuGet.org のようなサイトは、HTTPS が有効で実行され、HTTPS 以外のイメージを表示すると、混合コンテンツ警告が作成されます。</span><span class="sxs-lookup"><span data-stu-id="7346f-147">Sites like NuGet.org run with HTTPS enabled and displaying a non-HTTPS image will create a mixed content warning.</span></span>

<span data-ttu-id="7346f-148">**✔️ は**64 x 64 が、結果を表示する最良の透明な背景パッケージ アイコン イメージを使用します。</span><span class="sxs-lookup"><span data-stu-id="7346f-148">**✔️ DO** use a package icon image that is 64x64 and has a transparent background for best viewing results.</span></span>

## <a name="pre-release-packages"></a><span data-ttu-id="7346f-149">プレリリース パッケージ</span><span class="sxs-lookup"><span data-stu-id="7346f-149">Pre-release packages</span></span>

<span data-ttu-id="7346f-150">NuGet パッケージのバージョン サフィックスを持つ読晗ェホロ[プレリリース](/nuget/create-packages/prerelease-packages)します。</span><span class="sxs-lookup"><span data-stu-id="7346f-150">NuGet packages with a version suffix are considered [pre-release](/nuget/create-packages/prerelease-packages).</span></span> <span data-ttu-id="7346f-151">既定では、NuGet パッケージ マネージャー UI では、ユーザー opts にプレリリース パッケージをプレリリース パッケージを制限付きユーザーのテストに最適に行う場合を除きに安定したリリースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7346f-151">By default, the NuGet Package Manager UI shows stable releases unless a user opts-in to pre-release packages, making pre-release packages ideal for limited user testing.</span></span>

```xml
<PackageVersion>1.0.1-beta1</PackageVersion>
```

> [!NOTE]
> <span data-ttu-id="7346f-152">安定したパッケージは、プレリリース版のパッケージに依存できません。</span><span class="sxs-lookup"><span data-stu-id="7346f-152">A stable package cannot depend on a pre-release package.</span></span> <span data-ttu-id="7346f-153">独自のパッケージのプレリリース版を行うか、または以前の安定したバージョンに依存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7346f-153">You must either make your own package pre-release or depend on an older stable version.</span></span>

<span data-ttu-id="7346f-154">![NuGet プレリリース パッケージの依存関係](./media/nuget/nuget-prerelease-package.png "NuGet プレリリース パッケージの依存関係")</span><span class="sxs-lookup"><span data-stu-id="7346f-154">![NuGet pre-release package dependency](./media/nuget/nuget-prerelease-package.png "NuGet pre-release package dependency")</span></span>

<span data-ttu-id="7346f-155">**✔️ は**テスト、プレビュー、または実験時にプレリリース パッケージを発行します。</span><span class="sxs-lookup"><span data-stu-id="7346f-155">**✔️ DO** publish a pre-release package when testing, previewing, or experimenting.</span></span>

<span data-ttu-id="7346f-156">**✔️ は**その準備完了他の安定版パッケージ参照できる場合に、安定したパッケージを発行します。</span><span class="sxs-lookup"><span data-stu-id="7346f-156">**✔️ DO** publish a stable package when its ready so other stable packages can reference it.</span></span>

## <a name="symbol-packages"></a><span data-ttu-id="7346f-157">シンボル パッケージ</span><span class="sxs-lookup"><span data-stu-id="7346f-157">Symbol packages</span></span>

<span data-ttu-id="7346f-158">NuGet をサポートしています[別のシンボル パッケージを生成する](/nuget/create-packages/symbol-packages)を含む .NET アセンブリを含むメイン パッケージと共に PDB ファイルをデバッグします。</span><span class="sxs-lookup"><span data-stu-id="7346f-158">NuGet supports [generating a separate symbol package](/nuget/create-packages/symbol-packages) containing debug PDB files alongside the main package containing .NET assemblies.</span></span> <span data-ttu-id="7346f-159">シンボル パッケージの考え方は、シンボル サーバー上でホストする、Visual Studio などのツールをオンデマンドでダウンロードされるのみです。</span><span class="sxs-lookup"><span data-stu-id="7346f-159">The idea of symbol packages is they're hosted on a symbol server and are only downloaded by a tool like Visual Studio on demand.</span></span>

<span data-ttu-id="7346f-160">シンボルのメインのパブリック ホストに現在[SymbolSource](http://www.symbolsource.org/) -作成された、ポータブル Pdb をサポートしていない SDK スタイル プロジェクト、シンボル パッケージ役に立たない。</span><span class="sxs-lookup"><span data-stu-id="7346f-160">Currently the main public host for symbols - [SymbolSource](http://www.symbolsource.org/) - doesn't support the portable PDBs created by SDK-style projects and symbol packages aren't useful.</span></span>

<span data-ttu-id="7346f-161">**✔️ をご検討ください**メイン NuGet パッケージに Pdb を埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="7346f-161">**✔️ CONSIDER** embedding PDBs in the main NuGet package.</span></span>

<span data-ttu-id="7346f-162">**❌ 避け**Pdb が含まれるシンボル パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="7346f-162">**❌ AVOID** creating a symbols package containing PDBs.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="7346f-163">[前へ](./strong-naming.md)
[次へ](./dependencies.md)</span><span class="sxs-lookup"><span data-stu-id="7346f-163">[Previous](./strong-naming.md)
[Next](./dependencies.md)</span></span>
