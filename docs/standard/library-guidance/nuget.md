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
# <a name="nuget"></a><span data-ttu-id="d0d03-103">NuGet</span><span class="sxs-lookup"><span data-stu-id="d0d03-103">NuGet</span></span>

<span data-ttu-id="d0d03-104">NuGet は .NET エコシステムのパッケージ マネージャーであり、開発者が .NET オープンソース ライブラリを見つけて入手するための主要な方法です。</span><span class="sxs-lookup"><span data-stu-id="d0d03-104">NuGet is a package manager for the .NET ecosystem and is the primary way developers discover and acquire .NET open-source libraries.</span></span> <span data-ttu-id="d0d03-105">NuGet パッケージをホストするために Microsoft が提供している無料サービスの [NuGet.org](https://www.nuget.org/) は、パブリック NuGet パッケージのプライマリ ホストですが、[MyGet](https://www.myget.org/) および [Azure Artifacts](https://azure.microsoft.com/services/devops/artifacts/) などのカスタム NuGet サービスに公開できます。</span><span class="sxs-lookup"><span data-stu-id="d0d03-105">[NuGet.org](https://www.nuget.org/), a free service provided by Microsoft for hosting NuGet packages, is the primary host for public NuGet packages, but you can publish to custom NuGet services like [MyGet](https://www.myget.org/) and [Azure Artifacts](https://azure.microsoft.com/services/devops/artifacts/).</span></span>

<span data-ttu-id="d0d03-106">![NuGet](./media/nuget/nuget-logo.png "NuGet")</span><span class="sxs-lookup"><span data-stu-id="d0d03-106">![NuGet](./media/nuget/nuget-logo.png "NuGet")</span></span>

## <a name="create-a-nuget-package"></a><span data-ttu-id="d0d03-107">NuGet パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="d0d03-107">Create a NuGet package</span></span>

<span data-ttu-id="d0d03-108">NuGet パッケージ (`*.nupkg`) は、.NET アセンブリと関連するメタデータを含む zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="d0d03-108">A NuGet package (`*.nupkg`) is a zip file that contains .NET assemblies and associated metadata.</span></span>

<span data-ttu-id="d0d03-109">NuGet パッケージを作成するには、主な方法が 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="d0d03-109">There are two main ways to create a NuGet package.</span></span> <span data-ttu-id="d0d03-110">より新しいお勧めの方法は、SDK 形式のプロジェクト (コンテンツが `<Project Sdk="Microsoft.NET.Sdk">` から始まるプロジェクト ファイル) からパッケージを作成することです。</span><span class="sxs-lookup"><span data-stu-id="d0d03-110">The newer and recommended way is to create a package from a SDK-style project (project file whose content starts with `<Project Sdk="Microsoft.NET.Sdk">`).</span></span> <span data-ttu-id="d0d03-111">アセンブリとターゲットが自動的にパッケージに追加され、パッケージ名やバージョン番号などの残りのメタデータが、MSBuild ファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="d0d03-111">Assemblies and targets are automatically added to the package and remaining metadata is added to the MSBuild file, like package name and version number.</span></span> <span data-ttu-id="d0d03-112">[`dotnet pack`](../../core/tools/dotnet-pack.md) コマンドを使ってコンパイルすると、アセンブリの代わりに `*.nupkg` ファイルが出力されます。</span><span class="sxs-lookup"><span data-stu-id="d0d03-112">Compiling with the [`dotnet pack`](../../core/tools/dotnet-pack.md) command outputs a `*.nupkg` file instead of assemblies.</span></span>

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

<span data-ttu-id="d0d03-113">NuGet パッケージを作成する従来からの方法では、`*.nuspec` ファイルと `nuget.exe` コマンドライン ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="d0d03-113">The older way of creating a NuGet package is with a `*.nuspec` file and the `nuget.exe` command-line tool.</span></span> <span data-ttu-id="d0d03-114">nuspec ファイルを使用すると、優れた制御を利用できますが、最終的な NuGet パッケージに含めるアセンブリとターゲットを慎重に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0d03-114">A nuspec file gives you great control but you must carefully specify what assemblies and targets to include in the final NuGet package.</span></span> <span data-ttu-id="d0d03-115">間違えやすいうえに、変更を加える際にユーザーは nuspec の更新を忘れやすいです。</span><span class="sxs-lookup"><span data-stu-id="d0d03-115">It's easy to make a mistake or for someone to forget to update the nuspec when making changes.</span></span> <span data-ttu-id="d0d03-116">nuspec の利点は、まだ SDK 形式のプロジェクト ファイルをサポートしていないフレームワークの NuGet パッケージを作成するために使用できることです。</span><span class="sxs-lookup"><span data-stu-id="d0d03-116">The advantage of a nuspec is you can use it create NuGet packages for frameworks that don't yet support an SDK-style project file.</span></span>

<span data-ttu-id="d0d03-117">**✔️ 検討** SDK 形式のプロジェクト ファイルを使用して、NuGet パッケージを作成する。</span><span class="sxs-lookup"><span data-stu-id="d0d03-117">**✔️ CONSIDER** using an SDK-style project file to create the NuGet package.</span></span>

<span data-ttu-id="d0d03-118">**✔️ 検討** SourceLink を設定して、お使いのアセンブリと NuGet パッケージにソース管理のメタデータを追加する。</span><span class="sxs-lookup"><span data-stu-id="d0d03-118">**✔️ CONSIDER** setting up SourceLink to add source control metadata to your assemblies and NuGet package.</span></span>

## <a name="package-dependencies"></a><span data-ttu-id="d0d03-119">パッケージの依存関係</span><span class="sxs-lookup"><span data-stu-id="d0d03-119">Package dependencies</span></span>

<span data-ttu-id="d0d03-120">NuGet パッケージの依存関係については、「[Dependencies](./dependencies.md)」 (依存関係) の記事で説明しています。</span><span class="sxs-lookup"><span data-stu-id="d0d03-120">NuGet package dependencies are covered in detail in the [Dependencies](./dependencies.md) article.</span></span>

## <a name="important-nuget-package-metadata"></a><span data-ttu-id="d0d03-121">重要な NuGet パッケージ メタデータ</span><span class="sxs-lookup"><span data-stu-id="d0d03-121">Important NuGet package metadata</span></span>

<span data-ttu-id="d0d03-122">NuGet パッケージは、多数の[メタデータ プロパティ](/nuget/reference/nuspec)をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d0d03-122">A NuGet package supports many [metadata properties](/nuget/reference/nuspec).</span></span> <span data-ttu-id="d0d03-123">次の表に、どのオープンソース プロジェクトでも指定する必要があるコア メタデータを示します。</span><span class="sxs-lookup"><span data-stu-id="d0d03-123">The following table contains the core metadata that every open-source project should provide:</span></span>

| <span data-ttu-id="d0d03-124">MSBuild プロパティの名前</span><span class="sxs-lookup"><span data-stu-id="d0d03-124">MSBuild Property name</span></span>              | <span data-ttu-id="d0d03-125">Nuspec の名前</span><span class="sxs-lookup"><span data-stu-id="d0d03-125">Nuspec name</span></span>              | <span data-ttu-id="d0d03-126">説明</span><span class="sxs-lookup"><span data-stu-id="d0d03-126">Description</span></span>  |
| ---------------------------------- | ------------------------ | ------------ |
| `PackageId`                        | `id`                       | <span data-ttu-id="d0d03-127">パッケージ ID。</span><span class="sxs-lookup"><span data-stu-id="d0d03-127">The package identifier.</span></span> <span data-ttu-id="d0d03-128">[条件](/nuget/reference/id-prefix-reservation)を満たしている場合、ID のプレフィックスは予約できます。</span><span class="sxs-lookup"><span data-stu-id="d0d03-128">A prefix from the identifier can be reserved if it meets the [criteria](/nuget/reference/id-prefix-reservation).</span></span> |
| `PackageVersion`                   | `version`                  | <span data-ttu-id="d0d03-129">NuGet パッケージ バージョン。</span><span class="sxs-lookup"><span data-stu-id="d0d03-129">NuGet package version.</span></span> <span data-ttu-id="d0d03-130">詳細については、「[NuGet package version](./versioning.md#nuget-package-version)」(NuGet package version パッケージ バージョン) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d0d03-130">For more information, see [NuGet package version](./versioning.md#nuget-package-version).</span></span>             |
| `Title`                            | `title`                    | <span data-ttu-id="d0d03-131">わかりやすいパッケージ タイトル。</span><span class="sxs-lookup"><span data-stu-id="d0d03-131">A human-friendly title of the package.</span></span> <span data-ttu-id="d0d03-132">既定値は `PackageId` です。</span><span class="sxs-lookup"><span data-stu-id="d0d03-132">It defaults to the `PackageId`.</span></span>             |
| `Description`                      | `description`              | <span data-ttu-id="d0d03-133">UI に表示されるパッケージの長い説明。</span><span class="sxs-lookup"><span data-stu-id="d0d03-133">A long description of the package displayed in UI.</span></span>             |
| `Authors`                          | `authors`                  | <span data-ttu-id="d0d03-134">パッケージ作成者のコンマで区切りの一覧。nuget.org のプロファイル名と一致します。</span><span class="sxs-lookup"><span data-stu-id="d0d03-134">A comma-separated list of package authors, matching the profile names on nuget.org.</span></span>             |
| `PackageTags`                      | `tags`                     | <span data-ttu-id="d0d03-135">パッケージを説明するタグとキーワードのスペース区切りの一覧。</span><span class="sxs-lookup"><span data-stu-id="d0d03-135">A space-delimited list of tags and keywords that describe the package.</span></span> <span data-ttu-id="d0d03-136">タグは、パッケージを検索するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="d0d03-136">Tags are used when searching for packages.</span></span>             |
| `PackageIconUrl`                   | `iconUrl`                  | <span data-ttu-id="d0d03-137">パッケージのアイコンとして使用するイメージの URL。</span><span class="sxs-lookup"><span data-stu-id="d0d03-137">A URL for an image to use as the icon for the package.</span></span> <span data-ttu-id="d0d03-138">URL は HTTPS にする必要があり、イメージは 64 x 64 で透明な背景になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0d03-138">URL should be HTTPS and the image should be 64x64 and have a transparent background.</span></span>             |
| `PackageProjectUrl`                | `projectUrl`               | <span data-ttu-id="d0d03-139">プロジェクトのホーム ページまたはソース リポジトリの URL。</span><span class="sxs-lookup"><span data-stu-id="d0d03-139">A URL for the project homepage or source repository.</span></span>             |
| `PackageLicenseUrl`                | `licenseUrl`               | <span data-ttu-id="d0d03-140">プロジェクト ライセンスの URL。</span><span class="sxs-lookup"><span data-stu-id="d0d03-140">A URL to the project license.</span></span> <span data-ttu-id="d0d03-141">ソース管理の `LICENSE` ファイルの URL にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d0d03-141">Can be the URL to the `LICENSE` file in source control.</span></span>             |

<span data-ttu-id="d0d03-142">**✔️ 検討** NuGet のプレフィックスの予約[条件](/nuget/reference/id-prefix-reservation)を満たしているプレフィックスを持つ NuGet パッケージ名を選択する。</span><span class="sxs-lookup"><span data-stu-id="d0d03-142">**✔️ CONSIDER** choosing a NuGet package name with a prefix that meets NuGet's prefix reservation [criteria](/nuget/reference/id-prefix-reservation).</span></span>

<span data-ttu-id="d0d03-143">**✔️ 検討** ソース管理の `LICENSE` ファイルを `LicenseUrl` として使用する。</span><span class="sxs-lookup"><span data-stu-id="d0d03-143">**✔️ CONSIDER** using the `LICENSE` file in source control as the `LicenseUrl`.</span></span> <span data-ttu-id="d0d03-144">たとえば、[LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md)。</span><span class="sxs-lookup"><span data-stu-id="d0d03-144">For example, [LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0d03-145">ライセンス既定値が、他のユーザーからは使用できなくなる[排他的な著作権](https://choosealicense.com/no-permission/)に設定されていないプロジェクト。</span><span class="sxs-lookup"><span data-stu-id="d0d03-145">A project without a license defaults to [exclusive copyright](https://choosealicense.com/no-permission/), making it impossible for other people to use.</span></span>

<span data-ttu-id="d0d03-146">**✔️ 実行** パッケージのアイコンに HTTPS href を使用する。</span><span class="sxs-lookup"><span data-stu-id="d0d03-146">**✔️ DO** use an HTTPS href to your package icon.</span></span>

> <span data-ttu-id="d0d03-147">NuGet.org のようなサイトは HTTPS を有効にした状態で実行され、HTTPS ではないイメージを表示すると、コンテンツの混合を示す警告が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d0d03-147">Sites like NuGet.org run with HTTPS enabled and displaying a non-HTTPS image will create a mixed content warning.</span></span>

<span data-ttu-id="d0d03-148">**✔️ 実行** 64 x 64 のパッケージ アイコン イメージを使用し、最善の表示結果を透明な背景にする。</span><span class="sxs-lookup"><span data-stu-id="d0d03-148">**✔️ DO** use a package icon image that is 64x64 and has a transparent background for best viewing results.</span></span>

## <a name="pre-release-packages"></a><span data-ttu-id="d0d03-149">プレリリース パッケージ</span><span class="sxs-lookup"><span data-stu-id="d0d03-149">Pre-release packages</span></span>

<span data-ttu-id="d0d03-150">バージョン サフィックスがある NuGet パッケージは、[プレリリース](/nuget/create-packages/prerelease-packages)と見なされます。</span><span class="sxs-lookup"><span data-stu-id="d0d03-150">NuGet packages with a version suffix are considered [pre-release](/nuget/create-packages/prerelease-packages).</span></span> <span data-ttu-id="d0d03-151">プレリリース パッケージが制限付きユーザーのテスト実行に最適になるように、ユーザーがプレリリース パッケージを選択しない限り、既定では、NuGet パッケージ マネージャーの UI は、安定版リリースを表示します。</span><span class="sxs-lookup"><span data-stu-id="d0d03-151">By default, the NuGet Package Manager UI shows stable releases unless a user opts-in to pre-release packages, making pre-release packages ideal for limited user testing.</span></span>

```xml
<PackageVersion>1.0.1-beta1</PackageVersion>
```

> [!NOTE]
> <span data-ttu-id="d0d03-152">安定版パッケージは、プレリリース パッケージに依存できません。</span><span class="sxs-lookup"><span data-stu-id="d0d03-152">A stable package cannot depend on a pre-release package.</span></span> <span data-ttu-id="d0d03-153">独自のパッケージをプレリリースにするか、または旧来の安定版バージョンに依存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0d03-153">You must either make your own package pre-release or depend on an older stable version.</span></span>

<span data-ttu-id="d0d03-154">![NuGet プレリリース パッケージの依存関係](./media/nuget/nuget-prerelease-package.png "NuGet プレリリース パッケージの依存関係")</span><span class="sxs-lookup"><span data-stu-id="d0d03-154">![NuGet pre-release package dependency](./media/nuget/nuget-prerelease-package.png "NuGet pre-release package dependency")</span></span>

<span data-ttu-id="d0d03-155">**✔️ 実行** テスト、プレビュー、または実験時に、プレリリース パッケージを公開する。</span><span class="sxs-lookup"><span data-stu-id="d0d03-155">**✔️ DO** publish a pre-release package when testing, previewing, or experimenting.</span></span>

<span data-ttu-id="d0d03-156">**✔️ 実行** 他の安定版パッケージから参照できるように、準備ができ次第、安定版パッケージを公開する。</span><span class="sxs-lookup"><span data-stu-id="d0d03-156">**✔️ DO** publish a stable package when its ready so other stable packages can reference it.</span></span>

## <a name="symbol-packages"></a><span data-ttu-id="d0d03-157">シンボル パッケージ</span><span class="sxs-lookup"><span data-stu-id="d0d03-157">Symbol packages</span></span>

<span data-ttu-id="d0d03-158">シンボル ファイル (`*.pdb`) は、アセンブリと共に .NET コンパイラによって生成されます。</span><span class="sxs-lookup"><span data-stu-id="d0d03-158">Symbol files (`*.pdb`) are produced by the .NET compiler alongside assemblies.</span></span> <span data-ttu-id="d0d03-159">デバッガ―を使用して実行しながらソース コード全体をステップ実行できるように、シンボル ファイルは、実行場所を元のソース コードにマップします。</span><span class="sxs-lookup"><span data-stu-id="d0d03-159">Symbol files map execution locations to the original source code so you can step through source code as it is running using a debugger.</span></span> <span data-ttu-id="d0d03-160">NuGet では、.NET アセンブリを含む主要なパッケージと共に、シンボル ファイルを格納している[別個のシンボル パッケージの生成](/nuget/create-packages/symbol-packages)をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d0d03-160">NuGet supports [generating a separate symbol package](/nuget/create-packages/symbol-packages) containing symbol files alongside the main package containing .NET assemblies.</span></span> <span data-ttu-id="d0d03-161">シンボル サーバー上でホストされ、Visual Studio などのツールによってオンデマンドでしかダウンロードできないのが、シンボル パッケージの考え方です。</span><span class="sxs-lookup"><span data-stu-id="d0d03-161">The idea of symbol packages is they're hosted on a symbol server and are only downloaded by a tool like Visual Studio on demand.</span></span>

<span data-ttu-id="d0d03-162">現在、シンボルの主要なパブリック ホスト ([SymbolSource](http://www.symbolsource.org/)) は、SDK 形式のプロジェクトによって作成された新しい[ポータブル シンボル ファイル](https://github.com/dotnet/core/blob/master/Documentation/diagnostics/portable_pdb.md) (`*.pdb`) をサポートしておらず、シンボル パッケージは便利ではありません。</span><span class="sxs-lookup"><span data-stu-id="d0d03-162">Currently the main public host for symbols - [SymbolSource](http://www.symbolsource.org/) - doesn't support the new [portable symbol files](https://github.com/dotnet/core/blob/master/Documentation/diagnostics/portable_pdb.md) (`*.pdb`) created by SDK-style projects, and symbol packages aren't useful.</span></span> <span data-ttu-id="d0d03-163">シンボル パッケージに対応した推奨ホストができるまで、シンボル ファイルは主要な NuGet パッケージに埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="d0d03-163">Until there is a recommended host for symbol packages, symbol files can be embedded in the main NuGet package.</span></span> <span data-ttu-id="d0d03-164">SDK 形式のプロジェクトを使用して NuGet パッケージを構築している場合、`AllowedOutputExtensionsInPackageBuildOutputFolder` プロパティを設定してシンボル ファイルを埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="d0d03-164">If you are building your NuGet package using an SDK-style project you can embed symbol files by setting the `AllowedOutputExtensionsInPackageBuildOutputFolder` property:</span></span> 

```xml
<Project Sdk="Microsoft.NET.Sdk">
 <PropertyGroup>
    <!-- Include symbol files (*.pdb) in the built .nupkg -->
    <AllowedOutputExtensionsInPackageBuildOutputFolder>$(AllowedOutputExtensionsInPackageBuildOutputFolder);.pdb</AllowedOutputExtensionsInPackageBuildOutputFolder>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="d0d03-165">**✔️ 検討** 主要な NuGet パッケージにシンボル ファイルを埋め込む。</span><span class="sxs-lookup"><span data-stu-id="d0d03-165">**✔️ CONSIDER** embedding symbol files in the main NuGet package.</span></span>

<span data-ttu-id="d0d03-166">**❌ 禁止**シンボル ファイルを含むシンボル パッケージを作成する。</span><span class="sxs-lookup"><span data-stu-id="d0d03-166">**❌ AVOID** creating a symbols package containing symbol files.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="d0d03-167">[前へ](./strong-naming.md)
[次へ](./dependencies.md)</span><span class="sxs-lookup"><span data-stu-id="d0d03-167">[Previous](./strong-naming.md)
[Next](./dependencies.md)</span></span>
