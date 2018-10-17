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
# <a name="cross-platform-targeting"></a>クロス プラットフォームを対象とします。

最新の .NET には、複数のオペレーティング システムとデバイスがサポートしています。 Azure、または Unity で .NET のゲームでホストされている ASP.NET web サイトを開発しているかどうかが、できるだけ多くの開発者をサポートするために .NET オープン ソース ライブラリの重要です。

## <a name="net-standard"></a>.NET Standard

.NET standard には、.NET ライブラリにクロス プラットフォーム サポートを追加する最善の方法を示します。 [.NET standard](../net-standard.md)すべての .NET 実装で使用できる .NET Api の仕様です。 .NET Standard をターゲットにすると、そのバージョンの .NET Standard を実装するすべてのプラットフォームでは、使用可能なことを意味する .NET Standard の特定のバージョンに含まれる Api を使用して制限されているライブラリを生成することができます。

![.NET standard](./media/cross-platform-targeting/platforms-netstandard.png ".NET Standard")

.NET Standard を対象として、プロジェクトを正常にコンパイルを保証していません、ライブラリは、すべてのプラットフォームで正常に実行されます。

1. プラットフォーム固有の Api は、他のプラットフォームでは失敗します。 たとえば、<xref:Microsoft.Win32.Registry?displayProperty=nameWithType>が Windows で成功してスロー<xref:System.PlatformNotSupportedException>他の任意の OS で使用する場合。
2. Api の動作が異なることができます。 たとえば、リフレクション Api さまざまなパフォーマンスの特性があります、アプリケーションが iOS または UWP で先行コンパイルを使用する場合。

> [!TIP]
> .NET チーム[提供する Roslyn アナライザー](../analyzers/api-analyzer.md)考えられる問題を発見しやすくします。

**✔️ は**などの開始、`netstandard2.0`ターゲット。

> 最も汎用的なライブラリでは、.NET Standard 2.0 以外の Api は必要ありません。 .NET standard 2.0 は、すべての最新のプラットフォームでサポートされて、1 つのターゲットで複数のプラットフォームをサポートするために推奨される方法です。

**❌ 避け**など、`netstandard1.x`ターゲット。

> .NET standard 1.x は、NuGet パッケージの細かいレベルで設定を大きなパッケージの依存関係グラフを作成して、開発者が構築するときに、多くのパッケージのダウンロードの結果として配布されます。 .NET Framework 4.6.1、UWP、Xamarin など、最新の .NET プラットフォームすべては、.NET Standard 2.0 をサポートします。 .NET Standard がのみ対象 1.x 以前のプラットフォームを対象にする必要がある場合。

**✔️ は**含める、`netstandard2.0`ターゲットが必要な場合、`netstandard1.x`ターゲット。

> .NET Standard 2.0 をサポートしているすべてのプラットフォームを使用して、`netstandard2.0`をターゲットし、小規模なパッケージ グラフを古いプラットフォームの機能し、を代わりに使用がまだなく、`netstandard1.x`ターゲット。

**❌ しない**ライブラリは、プラットフォーム固有のアプリ モデルに依存する場合は、.NET Standard ターゲットを含めます。

> たとえば、UWP コントロール toolkit ライブラリは、UWP で提供されるのみアプリ モデルによって異なります。 アプリ モデル固有の Api は .NET Standard で使用されません。

## <a name="multi-targeting"></a>マルチターゲット

ライブラリからフレームワークに固有の Api にアクセスする必要がある場合があります。 フレームワーク固有の Api を呼び出すための最善の方法を使用して複数バージョン対応、多くのプロジェクトをビルドする[.NET ターゲット フレームワーク](../frameworks.md)ではなく 1 つだけです。

個々 のフレームワークを構築することから、コンシューマーをシールドするには、.NET の標準出力と 1 つまたは複数のフレームワーク固有の出力があるよう努力する必要があります。 マルチ ターゲットのすべてのアセンブリは、1 つの NuGet パッケージ内にパッケージ化されます。 コンシューマーは、同じパッケージを参照でき、NuGet は、適切な実装を取得します。 .NET Standard ライブラリには、フォールバック ライブラリが使用される、NuGet パッケージがフレームワークに固有の実装を提供する場合を除いて、すべてが機能します。 複数バージョン対応する、コードで条件付きコンパイルを使用して、フレームワーク固有の Api を呼び出すことができます。

![複数のアセンブリを使用した NuGet パッケージ](./media/cross-platform-targeting/nuget-package-multiple-assemblies.png "複数のアセンブリを使用した NuGet パッケージ")

**✔️ をご検討ください**だけでなく .NET Standard の .NET 実装を対象とします。

> .NET 実装を対象とすると、.NET Standard の外にあるプラットフォーム固有の Api を呼び出すことができます。
>
> これを行うときに、.NET Standard のサポートを削除できません。 代わりに、実装からスローし、Api の機能を提供します。 これにより、ライブラリはどこでも使用でき、ランタイム機能のライト アップをサポートします。

**❌ 避け**ソース コードは、すべてのターゲットの同じ場合、.NET Standard を使用したマルチ ターゲットを使用します。

> .NET Standard のアセンブリは、NuGet によって自動的に使用されます。 個々 の .NET 実装を対象とするが増加、`*.nupkg`サイズ メリットがありません。

**✔️ をご検討ください**のターゲットを追加する`net461`提供しているときに、`netstandard2.0`ターゲット。 

> .NET Framework から .NET Standard 2.0 には、.NET Framework 4.7.2 で対処された問題のいくつかがあります。 .NET Framework 4.6.1 の .NET Framework 4.6.1 がビルドされるバイナリを提供して 4.7.1 上に残っている開発者のエクスペリエンスを向上できます。

**✔️ は**NuGet パッケージを使用して、ライブラリを配布します。

> NuGet は開発者にとって最適なターゲットを選択し、シールドする適切な実装を選択する必要はありません。

**✔️ は**プロジェクト ファイルを使用して`TargetFrameworks`複数バージョン対応するプロパティ。

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <!-- This project will output netstandard2.0 and net461 assemblies -->
    <TargetFrameworks>netstandard2.0;net461</TargetFrameworks>
  </PropertyGroup>
</Project>
```

**✔️ をご検討ください**を使用して[MSBuild.Sdk.Extras](https://github.com/onovotny/MSBuildSdkExtras)と複数バージョン対応 UWP および Xamarin のように、プロジェクト ファイルを大幅に簡略化します。

## <a name="older-targets"></a>古いターゲット

.NET では、長い不要になった一般的に使用されるプラットフォームと同様にサポート外である .NET Framework のターゲットのバージョンをサポートします。 ワーク作成のため、ライブラリの Api がないを回避すること、できるだけ多くのターゲットを追加できるように大幅なオーバーヘッドに値がある間は。 思わ特定のフレームワークされなく価値が対象とすると、その範囲や制限事項を検討します。

**❌ しない**ポータブル クラス ライブラリ (PCL) ターゲットを含めます。 たとえば、`portable-net45+win8+wpa81+wp8` のようにします。

> .NET standard は、クロスプラット フォーム対応 .NET ライブラリをサポートする最新の方法は、し、Pcl を置き換えます。

**❌ しない**はサポートされなくなった .NET プラットフォーム用のターゲットが含まれます。 たとえば、`SL4`、`WP` のようになります。

>[!div class="step-by-step"]
[前へ](./get-started.md)
[次へ](./strong-naming.md)
