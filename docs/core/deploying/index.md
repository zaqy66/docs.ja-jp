---
title: .NET Core アプリケーション展開
description: .NET Core アプリケーションの展開。
author: rpetrusha
ms.author: ronpet
ms.date: 09/03/2018
ms.openlocfilehash: 2ef63ebd737739b2c8e671d982c3844135689ab4
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43891312"
---
# <a name="net-core-application-deployment"></a>.NET Core アプリケーションの展開

.NET Core アプリケーションに対して、次の 2 種類の展開を作成できます。

- フレームワークに依存する展開。 名前が示すように、フレームワークに依存する展開 (FDD) は、ターゲット システムに .NET Core のシステム全体の共有バージョンが存在することに依存します。 .NET Core は既に存在するので、アプリは .NET Core のインストール間で移植することもできます。 アプリには、それ自体のコード、および .NET Core ライブラリの外部にあるサードパーティの依存関係のみが含まれています。 FDD には、コマンドラインから [dotnet ユーティリティ](../tools/dotnet.md)を使って起動できる *.dll* ファイルが含まれています。 たとえば、`dotnet app.dll` は `app` という名前のアプリケーションを実行します。

- 自己完結型の展開。 FDD とは異なり、自己完結型の展開 (SCD) は、ターゲット システムに共有コンポーネントが存在することに依存しません。 .NET Core ライブラリと .NET Core ランタイムの両方を含むすべてのコンポーネントがアプリケーションに含まれており、他の .NET Core アプリケーションから分離されています。 SCD には、プラットフォーム固有の .NET Core ホストの名前変更後のバージョンである実行可能ファイル (`app` という名前のアプリケーションに対する Windows プラットフォーム上の *app.exe* など)、および実際のアプリケーションである *.dll* ファイル (*app.dll* など) が含まれています。

## <a name="framework-dependent-deployments-fdd"></a>フレームワークに依存する展開 (FDD)

FDD では、アプリ、およびサードパーティの依存関係のみを展開します。 アプリは、ターゲット システムに存在する .NET Core のバージョンを使うので、.NET Core を展開する必要はありません。 これは、.NET Core および .NET Core をターゲットとする ASP.NET Core アプリの既定の展開モデルです。

### <a name="why-create-a-framework-dependent-deployment"></a>フレームワークに依存する展開を作成する理由

FDD の展開には、次のいくつかの利点があります。

- .NET Core アプリが実行されるターゲットのオペレーティング システムを事前に定義する必要はありません。 .NET Core は、オペレーティング システムに関係なく実行可能ファイルとライブラリに共通の PE ファイル形式を使用するので、.NET Core は、基になるオペレーティング システムに関係なくアプリを実行できます。 PE ファイル形式の詳細については、「[.NET Assembly File Format](../../standard/assembly-format.md)」 (.NET アセンブリのファイル形式) を参照してください。

- 展開パッケージは小サイズです。 .NET Core 自体ではなく、アプリとその依存関係のみを展開します。

- 複数のアプリが、同じ .NET Core インストールを使用します。これにより、ホスト システム上のディスク領域とメモリ使用量の両方が削減されます。

次のいくつかの短所もあります。

- ターゲットとする .NET Core のバージョンまたはそれ以降のバージョンがホスト システムに既にインストールされている場合にのみ、アプリを実行できます。

- 将来のリリースでは、ユーザーの認識なしに .NET Core ランタイムおよびライブラリが変更される場合があります。 まれなケースでは、アプリのビヘイビアーが変更される可能性があります。

## <a name="self-contained-deployments-scd"></a>自己完結型の展開 (SCD)

自己完結型の展開では、アプリおよびすべての必要なサードパーティの依存関係と共に、アプリのビルドに使った .NET Core のバージョンも展開します。 SCD の作成には、さまざまなプラットフォーム上の [.NET Core のネイティブの依存関係](https://github.com/dotnet/core/blob/master/Documentation/prereqs.md)は含まれないので、アプリが実行する前にこれらが存在している必要があります。 ランタイムのバージョン バインディングについて詳しくは、[.NET Core のバージョン バインディング](../versions/selection.md)に関する記事をご覧ください。

.NET Core 2.1 SDK (バージョン 2.1.300) 以降、.NET Core では "*修正プログラムのバージョンのロール フォワード*" がサポートされます。 自己完結型の展開を作成するときに、.NET Core のツールによって、アプリケーションがターゲットとする .NET Core のバージョンの最新のサービス提供されたランタイムが含まれます。 (最新のサービス提供されたランタイムには、セキュリティに関する修正プログラムとその他のバグの修正が含まれます。)サービス提供されたランタイムがビルド システム上に存在する必要はありません。これは NuGet.org から自動的にダウンロードされます。修正プログラムのバージョンのロール フォワードを無効にする方法など、詳細については「[自己完結型展開ランタイムのロール フォワード](runtime-patch-selection.md)」をご覧ください。

FDD および SCD の展開では別個のホスト実行可能ファイルを使用するため、発行元のシグネチャで SCD のホスト実行可能ファイルに署名できます。

### <a name="why-deploy-a-self-contained-deployment"></a>自己完結型の展開を展開する理由

自己完結型の展開を展開するのには、次の 2 つの主な利点があります。

- アプリで展開されている .NET Core のバージョンは、あなただけがコントロールできます。 .NET Core を操作できるのはあなただけです。

- ターゲット システムが実行できる .NET Core のバージョンを提供しているので、ターゲット システムで .NET Core アプリを確実に実行できます。

また、次のいくつかの短所もあります。

- .NET Core が展開パッケージに含まれているので、展開パッケージをビルドするターゲット プラットフォームを事前に選択する必要があります。

- .NET Core だけでなくアプリおよびそのサードパーティの依存関係を含める必要があるので、展開パッケージは比較的大きくなります。

  .NET Core 2.0 以降では、.NET Core の ["*グローバリゼーション インバリアント モード*"](https://github.com/dotnet/corefx/blob/master/Documentation/architecture/globalization-invariant-mode.md) を使用することで、Linux システムでの展開のサイズを約 28 MB 小さくすることができます。 通常、Linux 上の .NET Core は [ICU ライブラリ](https://github.com/dotnet/docs/issues/http%22//icu-project.org)に依存してグローバリゼーションをサポートします。 インバリアント モードでは、ライブラリは展開に含まれず、すべてのカルチャが[インバリアント カルチャ](xref:System.Globalization.CultureInfo.InvariantCulture?displayProperty=nameWithType)のように動作します。

- 多数の自己完結型の .NET Core アプリをシステムに展開すると、各アプリが .NET Core ファイルを複製するので、非常に多くのディスク領域を使用する可能性があります。

## <a name="step-by-step-examples"></a>手順の例

CLI ツールで .NET Core アプリを展開する手順の例については、「[Deploying .NET Core Apps with CLI Tools](deploy-with-cli.md)」(CLI ツールで .NET Core アプリを展開する) をご覧ください。 Visual Studio で .NET Core アプリを展開する手順の例については、「[Deploying .NET Core Apps with Visual Studio](deploy-with-vs.md)」(Visual Studio で .NET Core アプリを展開する) をご覧ください。 各トピックには、次の展開の例が含まれます。

- フレームワークに依存する展開
- サードパーティの依存関係を含む、フレームワークに依存する展開
- 自己完結型の展開
- サードパーティの依存関係を含む、自己完結型の展開

## <a name="see-also"></a>関連項目

* [CLI ツールで .NET Core アプリを展開する](deploy-with-cli.md)
* [Visual Studio で .NET Core アプリを展開する](deploy-with-vs.md)
* [パッケージ、メタパッケージ、フレームワーク](../packages.md)
* [.NET Core のランタイム識別子 (RID) のカタログ](../rid-catalog.md)
