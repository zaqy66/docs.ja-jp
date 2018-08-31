---
title: .NET Core のバージョン履歴
description: .NET Core ランタイム、.NET Core SDK、C# コンパイラおよび VB.NET コンパイラのバージョンのタイムラインを確認します。
ms.date: 07/26/2018
ms.openlocfilehash: 90fd4ba57620a3a005f2148c0335a76a6fa54a30
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42936624"
---
# <a name="net-core-version-history"></a>.NET Core のバージョン履歴

.NET Core のバージョン番号は、.NET Core SDK と .NET Core ランタイムが異なる頻度でリリースされているため、わかりにくくなっています。 頻度が異なっているのは、チームが次の 3 つのうちの 2 のみを行う必要があったことを意味します。

1. 特にツール、C# および VB を .NET Core ランタイムよりも早く進められるように、単独でリリースする。
2. .NET Core SDK と .NET Core ランタイムのバージョン アラインメントを維持する。
3. .NET Core SDK と .NET Core ランタイムの両方にセマンティック バージョニングを使用する。

2.0.0 では、バージョン アラインメントを実行し、1 つのリリースを円滑に進めました。 2017 年 12 月、.NET Core SDK では機能リリースがありましたが、.NET Core ランタイムでは対応するリリースはありませんでした。 チームは、目標の 1 と 3 を選択し、.NET Core ランタイムと SDK 間のアラインメントは失われることになりました。 .NET Core ランタイム 2.1 がリリースされるまでに、いくつかの .NET Core SDK 2.1.x バージョンがリリースされました。 SDK には上位互換性がないため、SDK 2.1.x のこれらのバージョンは、.NET Core ランタイム 2.1 を対象にできませんでした。 チームは、「[.NET Core バージョン管理](index.md#versioning-details)」に記載されているように、セマンティック バージョニングを放棄して、目標 1 と 2 に切り替えることによって、大きな混乱に対応しました。

セマンティック バージョニングの破棄が決定されるまでのタイミングのため、バージョン番号 2.1.10x から 2.1.20x までの間に暫定リリースがありましたが、こちらも .NET Core ランタイム 2.1 を対象とすることはできません。

バージョン番号の最初の 2 桁が、.NET Core ランタイムの 2.1.0 バージョンと、NET Core SDK の 2.1.300 バージョンと再度アラインされます。

フレームワークと言語コンパイラのバージョンを含む、個々のコンポーネントのバージョンに関する詳細情報は、[.NET Core のダウンロード ページ](https://www.microsoft.com/net/download/dotnet-core/current)を参照してください。 以前のバージョンの詳細については、[.NET Core のダウンロードのアーカイブ ページ](https://www.microsoft.com/net/download/archives)から、必要なバージョンを選択してください。 詳細なサポート情報は、公式の[.NET サポート ポリシー](https://www.microsoft.com/net/Support/Policy)を説明する記事で得られます。