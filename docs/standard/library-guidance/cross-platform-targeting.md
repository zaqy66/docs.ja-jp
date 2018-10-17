---
title: クロス プラットフォームを対象とします。
description: クロス プラットフォームの .NET ライブラリを作成するための推奨されるベスト プラクティスです。
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 72fa891d5b1054af485a98d89b4efb11d6b0018b
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374894"
---
# <a name="cross-platform-targeting"></a><span data-ttu-id="03557-103">クロス プラットフォームを対象とします。</span><span class="sxs-lookup"><span data-stu-id="03557-103">Cross-platform targeting</span></span>

<span data-ttu-id="03557-104">最新の .NET には、複数のオペレーティング システムとデバイスがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="03557-104">Modern .NET supports multiple operating systems and devices.</span></span> <span data-ttu-id="03557-105">Azure、または Unity で .NET のゲームでホストされている ASP.NET web サイトを開発しているかどうかが、できるだけ多くの開発者をサポートするために .NET オープン ソース ライブラリの重要です。</span><span class="sxs-lookup"><span data-stu-id="03557-105">It's important for .NET open-source libraries to support as many developers as possible, whether they're building an ASP.NET website hosted in Azure, or a .NET game in Unity.</span></span>

## <a name="net-standard"></a><span data-ttu-id="03557-106">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="03557-106">.NET Standard</span></span>

<span data-ttu-id="03557-107">.NET standard には、.NET ライブラリにクロス プラットフォーム サポートを追加する最善の方法を示します。</span><span class="sxs-lookup"><span data-stu-id="03557-107">.NET Standard is the best way to add cross-platform support to a .NET library.</span></span> <span data-ttu-id="03557-108">[.NET standard](../net-standard.md)すべての .NET 実装で使用できる .NET Api の仕様です。</span><span class="sxs-lookup"><span data-stu-id="03557-108">[.NET Standard](../net-standard.md) is a specification of .NET APIs that are available on all .NET implementations.</span></span> <span data-ttu-id="03557-109">.NET Standard をターゲットにすると、そのバージョンの .NET Standard を実装するすべてのプラットフォームでは、使用可能なことを意味する .NET Standard の特定のバージョンに含まれる Api を使用して制限されているライブラリを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="03557-109">Targeting .NET Standard lets you produce libraries that are constrained to use APIs that are in a given version of .NET Standard, which means it's usable by all platforms that implement that version of the .NET Standard.</span></span>

<span data-ttu-id="03557-110">![.NET standard](./media/cross-platform-targeting/platforms-netstandard.png ".NET Standard")</span><span class="sxs-lookup"><span data-stu-id="03557-110">![.NET Standard](./media/cross-platform-targeting/platforms-netstandard.png ".NET Standard")</span></span>

<span data-ttu-id="03557-111">.NET Standard を対象として、プロジェクトを正常にコンパイルを保証していません、ライブラリは、すべてのプラットフォームで正常に実行されます。</span><span class="sxs-lookup"><span data-stu-id="03557-111">Targeting .NET Standard, and successfully compiling your project, doesn't guarantee the library will run successfully on all platforms:</span></span>

1. <span data-ttu-id="03557-112">プラットフォーム固有の Api は、他のプラットフォームでは失敗します。</span><span class="sxs-lookup"><span data-stu-id="03557-112">Platform-specific APIs will fail on other platforms.</span></span> <span data-ttu-id="03557-113">たとえば、<xref:Microsoft.Win32.Registry?displayProperty=nameWithType>が Windows で成功してスロー<xref:System.PlatformNotSupportedException>他の任意の OS で使用する場合。</span><span class="sxs-lookup"><span data-stu-id="03557-113">For example, <xref:Microsoft.Win32.Registry?displayProperty=nameWithType> will succeed on Windows and throw <xref:System.PlatformNotSupportedException> when used on any other OS.</span></span>
2. <span data-ttu-id="03557-114">Api の動作が異なることができます。</span><span class="sxs-lookup"><span data-stu-id="03557-114">APIs can behave differently.</span></span> <span data-ttu-id="03557-115">たとえば、リフレクション Api さまざまなパフォーマンスの特性があります、アプリケーションが iOS または UWP で先行コンパイルを使用する場合。</span><span class="sxs-lookup"><span data-stu-id="03557-115">For example, reflection APIs have different performance characteristics when an application uses ahead-of-time compilation on iOS or UWP.</span></span>

> [!TIP]
> <span data-ttu-id="03557-116">.NET チーム[提供する Roslyn アナライザー](../analyzers/api-analyzer.md)考えられる問題を発見しやすくします。</span><span class="sxs-lookup"><span data-stu-id="03557-116">The .NET team [offers a Roslyn analyzer](../analyzers/api-analyzer.md) to help you discover possible issues.</span></span>

<span data-ttu-id="03557-117">**✔️ は**などの開始、`netstandard2.0`ターゲット。</span><span class="sxs-lookup"><span data-stu-id="03557-117">**✔️ DO** start with including a `netstandard2.0` target.</span></span>

> <span data-ttu-id="03557-118">最も汎用的なライブラリでは、.NET Standard 2.0 以外の Api は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="03557-118">Most general-purpose libraries should not need APIs outside of .NET Standard 2.0.</span></span> <span data-ttu-id="03557-119">.NET standard 2.0 は、すべての最新のプラットフォームでサポートされて、1 つのターゲットで複数のプラットフォームをサポートするために推奨される方法です。</span><span class="sxs-lookup"><span data-stu-id="03557-119">.NET Standard 2.0 is supported by all modern platforms and is the recommended way to support multiple platforms with one target.</span></span>

<span data-ttu-id="03557-120">**❌ 避け**など、`netstandard1.x`ターゲット。</span><span class="sxs-lookup"><span data-stu-id="03557-120">**❌ AVOID** including a `netstandard1.x` target.</span></span>

> <span data-ttu-id="03557-121">.NET standard 1.x は、NuGet パッケージの細かいレベルで設定を大きなパッケージの依存関係グラフを作成して、開発者が構築するときに、多くのパッケージのダウンロードの結果として配布されます。</span><span class="sxs-lookup"><span data-stu-id="03557-121">.NET Standard 1.x is distributed as a granular set of NuGet packages, which creates a large package dependency graph and results in developers downloading a lot of packages when building.</span></span> <span data-ttu-id="03557-122">.NET Framework 4.6.1、UWP、Xamarin など、最新の .NET プラットフォームすべては、.NET Standard 2.0 をサポートします。</span><span class="sxs-lookup"><span data-stu-id="03557-122">Modern .NET platforms, including .NET Framework 4.6.1, UWP and Xamarin, all support .NET Standard 2.0.</span></span> <span data-ttu-id="03557-123">.NET Standard がのみ対象 1.x 以前のプラットフォームを対象にする必要がある場合。</span><span class="sxs-lookup"><span data-stu-id="03557-123">You should only target .NET Standard 1.x if you specifically need to target an older platform.</span></span>

<span data-ttu-id="03557-124">**✔️ は**含める、`netstandard2.0`ターゲットが必要な場合、`netstandard1.x`ターゲット。</span><span class="sxs-lookup"><span data-stu-id="03557-124">**✔️ DO** include a `netstandard2.0` target if you require a `netstandard1.x` target.</span></span>

> <span data-ttu-id="03557-125">.NET Standard 2.0 をサポートしているすべてのプラットフォームを使用して、`netstandard2.0`をターゲットし、小規模なパッケージ グラフを古いプラットフォームの機能し、を代わりに使用がまだなく、`netstandard1.x`ターゲット。</span><span class="sxs-lookup"><span data-stu-id="03557-125">All platforms supporting .NET Standard 2.0 will use the `netstandard2.0` target and benefit from having a smaller package graph while older platforms will still work and fall back to using the `netstandard1.x` target.</span></span>

<span data-ttu-id="03557-126">**❌ しない**ライブラリは、プラットフォーム固有のアプリ モデルに依存する場合は、.NET Standard ターゲットを含めます。</span><span class="sxs-lookup"><span data-stu-id="03557-126">**❌ DO NOT** include a .NET Standard target if the library relies on a platform-specific app model.</span></span>

> <span data-ttu-id="03557-127">たとえば、UWP コントロール toolkit ライブラリは、UWP で提供されるのみアプリ モデルによって異なります。</span><span class="sxs-lookup"><span data-stu-id="03557-127">For example, a UWP control toolkit library depends on an app model that is only available on UWP.</span></span> <span data-ttu-id="03557-128">アプリ モデル固有の Api は .NET Standard で使用されません。</span><span class="sxs-lookup"><span data-stu-id="03557-128">App model specific APIs will not be available in .NET Standard.</span></span>

## <a name="multi-targeting"></a><span data-ttu-id="03557-129">マルチターゲット</span><span class="sxs-lookup"><span data-stu-id="03557-129">Multi-targeting</span></span>

<span data-ttu-id="03557-130">ライブラリからフレームワークに固有の Api にアクセスする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="03557-130">Sometimes you need to access framework-specific APIs from your libraries.</span></span> <span data-ttu-id="03557-131">フレームワーク固有の Api を呼び出すための最善の方法を使用して複数バージョン対応、多くのプロジェクトをビルドする[.NET ターゲット フレームワーク](../frameworks.md)ではなく 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="03557-131">The best way to call framework-specific APIs is using multi-targeting, which builds your project for many [.NET target frameworks](../frameworks.md) rather than for just one.</span></span>

<span data-ttu-id="03557-132">個々 のフレームワークを構築することから、コンシューマーをシールドするには、.NET の標準出力と 1 つまたは複数のフレームワーク固有の出力があるよう努力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03557-132">To shield your consumers from having to build for individual frameworks, you should strive to have a .NET Standard output plus one or more framework-specific outputs.</span></span> <span data-ttu-id="03557-133">マルチ ターゲットのすべてのアセンブリは、1 つの NuGet パッケージ内にパッケージ化されます。</span><span class="sxs-lookup"><span data-stu-id="03557-133">With multi-targeting, all assemblies are packaged inside a single NuGet package.</span></span> <span data-ttu-id="03557-134">コンシューマーは、同じパッケージを参照でき、NuGet は、適切な実装を取得します。</span><span class="sxs-lookup"><span data-stu-id="03557-134">Consumers can then reference the same package and NuGet will pick the appropriate implementation.</span></span> <span data-ttu-id="03557-135">.NET Standard ライブラリには、フォールバック ライブラリが使用される、NuGet パッケージがフレームワークに固有の実装を提供する場合を除いて、すべてが機能します。</span><span class="sxs-lookup"><span data-stu-id="03557-135">Your .NET Standard library serves as the fallback library that is used everywhere, except for the cases where your NuGet package offers a framework-specific implementation.</span></span> <span data-ttu-id="03557-136">複数バージョン対応する、コードで条件付きコンパイルを使用して、フレームワーク固有の Api を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="03557-136">Multi-targeting allows you to use conditional compilation in your code and call framework-specific APIs.</span></span>

<span data-ttu-id="03557-137">![複数のアセンブリを使用した NuGet パッケージ](./media/cross-platform-targeting/nuget-package-multiple-assemblies.png "複数のアセンブリを使用した NuGet パッケージ")</span><span class="sxs-lookup"><span data-stu-id="03557-137">![NuGet package with multiple assemblies](./media/cross-platform-targeting/nuget-package-multiple-assemblies.png "NuGet package with multiple assemblies")</span></span>

<span data-ttu-id="03557-138">**✔️ をご検討ください**だけでなく .NET Standard の .NET 実装を対象とします。</span><span class="sxs-lookup"><span data-stu-id="03557-138">**✔️ CONSIDER** targeting .NET implementations in addition to .NET Standard.</span></span>

> <span data-ttu-id="03557-139">.NET 実装を対象とすると、.NET Standard の外にあるプラットフォーム固有の Api を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="03557-139">Targeting .NET implementations allows you to call platform-specific APIs that are outside of .NET Standard.</span></span>
>
> <span data-ttu-id="03557-140">これを行うときに、.NET Standard のサポートを削除できません。</span><span class="sxs-lookup"><span data-stu-id="03557-140">Do not drop support for .NET Standard when you do this.</span></span> <span data-ttu-id="03557-141">代わりに、実装からスローし、Api の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="03557-141">Instead, throw from the implementation and offer capability APIs.</span></span> <span data-ttu-id="03557-142">これにより、ライブラリはどこでも使用でき、ランタイム機能のライト アップをサポートします。</span><span class="sxs-lookup"><span data-stu-id="03557-142">This way, your library can be used anywhere and supports runtime light-up of features.</span></span>

<span data-ttu-id="03557-143">**❌ 避け**ソース コードは、すべてのターゲットの同じ場合、.NET Standard を使用したマルチ ターゲットを使用します。</span><span class="sxs-lookup"><span data-stu-id="03557-143">**❌ AVOID** using multi-targeting with .NET Standard if your source code is the same for all targets.</span></span>

> <span data-ttu-id="03557-144">.NET Standard のアセンブリは、NuGet によって自動的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="03557-144">The .NET Standard assembly will automatically be used by NuGet.</span></span> <span data-ttu-id="03557-145">個々 の .NET 実装を対象とするが増加、`*.nupkg`サイズ メリットがありません。</span><span class="sxs-lookup"><span data-stu-id="03557-145">Targeting individual .NET implementations increases the `*.nupkg` size for no benefit.</span></span>

<span data-ttu-id="03557-146">**✔️ をご検討ください**のターゲットを追加する`net461`提供しているときに、`netstandard2.0`ターゲット。</span><span class="sxs-lookup"><span data-stu-id="03557-146">**✔️ CONSIDER** adding a target for `net461` when you're offering a `netstandard2.0` target.</span></span> 

> <span data-ttu-id="03557-147">.NET Framework から .NET Standard 2.0 には、.NET Framework 4.7.2 で対処された問題のいくつかがあります。</span><span class="sxs-lookup"><span data-stu-id="03557-147">Using .NET Standard 2.0 from .NET Framework has some issues that were addressed in .NET Framework 4.7.2.</span></span> <span data-ttu-id="03557-148">.NET Framework 4.6.1 の .NET Framework 4.6.1 がビルドされるバイナリを提供して 4.7.1 上に残っている開発者のエクスペリエンスを向上できます。</span><span class="sxs-lookup"><span data-stu-id="03557-148">You can improve the experience for developers that are still on .NET Framework 4.6.1 - 4.7.1 by offering them a binary that is built for .NET Framework 4.6.1.</span></span>

<span data-ttu-id="03557-149">**✔️ は**NuGet パッケージを使用して、ライブラリを配布します。</span><span class="sxs-lookup"><span data-stu-id="03557-149">**✔️ DO** distribute your library using a NuGet package.</span></span>

> <span data-ttu-id="03557-150">NuGet は開発者にとって最適なターゲットを選択し、シールドする適切な実装を選択する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="03557-150">NuGet will select the best target for the developer and shield them having to pick the appropriate implementation.</span></span>

<span data-ttu-id="03557-151">**✔️ は**プロジェクト ファイルを使用して`TargetFrameworks`複数バージョン対応するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="03557-151">**✔️ DO** use a project file's `TargetFrameworks` property when multi-targeting.</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <!-- This project will output netstandard2.0 and net461 assemblies -->
    <TargetFrameworks>netstandard2.0;net461</TargetFrameworks>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="03557-152">**✔️ をご検討ください**を使用して[MSBuild.Sdk.Extras](https://github.com/onovotny/MSBuildSdkExtras)と複数バージョン対応 UWP および Xamarin のように、プロジェクト ファイルを大幅に簡略化します。</span><span class="sxs-lookup"><span data-stu-id="03557-152">**✔️ CONSIDER** using [MSBuild.Sdk.Extras](https://github.com/onovotny/MSBuildSdkExtras) when multi-targeting for UWP and Xamarin as it greatly simplifies your project file.</span></span>

## <a name="older-targets"></a><span data-ttu-id="03557-153">古いターゲット</span><span class="sxs-lookup"><span data-stu-id="03557-153">Older targets</span></span>

<span data-ttu-id="03557-154">.NET では、長い不要になった一般的に使用されるプラットフォームと同様にサポート外である .NET Framework のターゲットのバージョンをサポートします。</span><span class="sxs-lookup"><span data-stu-id="03557-154">.NET supports targeting versions of the .NET Framework that are long out of support as well as platforms that are no longer commonly used.</span></span> <span data-ttu-id="03557-155">ワーク作成のため、ライブラリの Api がないを回避すること、できるだけ多くのターゲットを追加できるように大幅なオーバーヘッドに値がある間は。</span><span class="sxs-lookup"><span data-stu-id="03557-155">While there's value in making your library work on as many targets as possible, having to work around missing APIs can add significant overhead.</span></span> <span data-ttu-id="03557-156">思わ特定のフレームワークされなく価値が対象とすると、その範囲や制限事項を検討します。</span><span class="sxs-lookup"><span data-stu-id="03557-156">We believe certain frameworks are no longer worth targeting, considering their reach and limitations.</span></span>

<span data-ttu-id="03557-157">**❌ しない**ポータブル クラス ライブラリ (PCL) ターゲットを含めます。</span><span class="sxs-lookup"><span data-stu-id="03557-157">**❌ DO NOT** include a Portable Class Library (PCL) target.</span></span> <span data-ttu-id="03557-158">たとえば、`portable-net45+win8+wpa81+wp8` のようにします。</span><span class="sxs-lookup"><span data-stu-id="03557-158">For example, `portable-net45+win8+wpa81+wp8`.</span></span>

> <span data-ttu-id="03557-159">.NET standard は、クロスプラット フォーム対応 .NET ライブラリをサポートする最新の方法は、し、Pcl を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="03557-159">.NET Standard is the modern way to support cross-platform .NET libraries and replaces PCLs.</span></span>

<span data-ttu-id="03557-160">**❌ しない**はサポートされなくなった .NET プラットフォーム用のターゲットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="03557-160">**❌ DO NOT** include targets for .NET platforms that are no longer supported.</span></span> <span data-ttu-id="03557-161">たとえば、`SL4`、`WP` のようになります。</span><span class="sxs-lookup"><span data-stu-id="03557-161">For example, `SL4`, `WP`.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="03557-162">[前へ](./get-started.md)
[次へ](./strong-naming.md)</span><span class="sxs-lookup"><span data-stu-id="03557-162">[Previous](./get-started.md)
[Next](./strong-naming.md)</span></span>
