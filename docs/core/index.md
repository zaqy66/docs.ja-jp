---
title: .NET Core のガイド
description: .NET Core は、Windows、Linux、および Mac アプリを作成するためのモジュール型の高性能な .NET 実装です。 ここでは、.NET Core の概要について説明します。
author: richlander
ms.author: mairaw
ms.date: 08/01/2018
ms.custom: updateeachrelease
ms.openlocfilehash: b302b6fc7e097a811c718d2244f603246cb5c259
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2018
ms.locfileid: "49121039"
---
# <a name="net-core-guide"></a>.NET Core のガイド

[.NET Core](about.md) は、[GitHub](https://github.com/dotnet/core) で Microsoft および .NET コミュニティによって管理される[オープンソース](https://github.com/dotnet/coreclr/blob/master/LICENSE.TXT)の一般的な開発プラットフォームです。 クロスプラットフォームであり、Windows、macOS、Linux をサポートし、デバイス、クラウド、および IoT アプリケーションで使用できます。

特徴、サポートされる言語とフレームワーク、キー API など、.NET Core について詳しくは、「[About .NET Core](about.md)」(.NET Core について) をご覧ください。

「[.NET Core チュートリアル](tutorials/index.md)」では、単純な .NET Core アプリケーションを作成する方法を学習できます。 最初のアプリを、ほんの数分で起動および実行できます。 ブラウザーで .NET Core を使用してみたい場合は、[C# における数値](https://docs.microsoft.com/dotnet/csharp/quick-starts/numbers-in-csharp)に関するクイックスタートをご覧ください。

## <a name="download-net-core-21"></a>NET Core 2.1 のダウンロード

[.NET Core  2.1 SDK](https://www.microsoft.com/net/download) をダウンロードして、Windows、macOS、または Linux マシンで .NET Core をお試しください。 Docker コンテナーを使用する方がよければ、[microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet/) にアクセスしてください。

別の .NET Core バージョンを探している場合も、すべての .NET Core バージョンを [.NET Core のダウンロード](https://www.microsoft.com/net/download/archives)で入手できます。

## <a name="net-core-21"></a>.NET Core 2.1

最新バージョンは [.NET Core 2.1](whats-new/dotnet-core-2-1.md) です。 新機能には、グローバル ツール、高パフォーマンス API (<xref:System.Span%601?displayProperty=nameWithType> など)、階層型 JIT コンパイル、[ビルド](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/)と[ランタイムのパフォーマンスの向上](https://blogs.msdn.microsoft.com/dotnet/2018/04/18/performance-improvements-in-net-core-2-1/)、Alpine と ARM32 のサポートが含まれます。

## <a name="create-your-first-application"></a>最初のアプリケーションの作成

.NET Core SDK をインストールしたらコマンド プロンプトを開きます。 次の `dotnet` コマンドを入力し、C# アプリケーションを作成して実行します。

```console
dotnet new console
dotnet run
```

次の出力が表示されます。

```console
Hello World!
```

## <a name="support"></a>サポート

.NET Core は、Microsoft Windows、macOS、Linux で[サポート](https://www.microsoft.com/net/support/policy)されています。 年に数回、通常は毎月、セキュリティと品質向上のために更新されます。

.NET Core のバイナリ形式の配布は、Azure 内のマイクロソフトが管理するサーバーで構築されてテストされ、他のすべてのマイクロソフト製品と同様にサポートされます。

Red Hat Enterprise Linux (RHEL) では [.NET Core は Red Hat によってサポート](http://redhatloves.net/)されます。 Red Hat がソースから .NET Core をビルドして、[Red Hat ソフトウェア コレクション](https://developers.redhat.com/products/softwarecollections/overview/)で使用できるようにします。 Red Hat とマイクロソフトが共同して、.NET Core が RHEL 上で適切に動作するようにします。
