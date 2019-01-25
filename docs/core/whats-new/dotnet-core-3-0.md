---
title: .NET Core 3.0 の新機能
description: .NET Core 3.0 の新機能について説明します。
dev_langs:
- csharp
- vb
author: thraka
ms.author: adegeo
ms.date: 12/04/2018
ms.openlocfilehash: 26fb7cb25b9bf7f00f87059fbe1848763f7f175d
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54415547"
---
# <a name="whats-new-in-net-core-30-preview-1"></a>.NET Core 3.0 (Preview 1) の新機能

この記事では、.NET Core 3.0 (Preview 1) の新機能について説明します。 最も大きな強化点の 1 つは、Windows デスクトップ アプリケーションのサポートです (Windows のみ)。 Windows デスクトップという .NET Core 3.0 コンポーネントを利用して、Windows フォーム Windows Presentation Foundation (WPF) アプリケーションを移植することができます。 誤解のないように言うと、Windows Desktop コンポーネントは Windows でのみサポートされています。 詳細については、以下の「[Windows デスクトップ](#windows-desktop)」セクションを参照してください。

.NET Core 3.0 では C# 8.0 のサポートが追加されています。

[.NET Core 3 Preview 1 を今すぐダウンロード](https://aka.ms/netcore3download)して Windows、Mac、Linux 上で使い始めましょう。 リリースの詳細については、[.NET Core 3 Preview 1 のリリース ノート](https://aka.ms/netcore3releasenotes)を参照してください。

詳細については、[.NET Core 3.0 Preview 1 のお知らせ](https://blogs.msdn.microsoft.com/dotnet/2018/12/04/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/)に関するページを参照してください。

## <a name="net-standard-21"></a>.NET Standard 2.1

.NET core 3.0 では .NET Standard 2.1 も実装されます。

## <a name="default-executables"></a>既定の実行可能ファイル

.NET Core では、既定で[フレームワーク依存の実行可能ファイル](../deploying/index.md#framework-dependent-executables-fde)が作成されるようになります。 これは、グローバルにインストールされているバージョンの .NET Core を使用するアプリケーションの新機能です。 これまでは、[自己完結型のデプロイ](../deploying/index.md#self-contained-deployments-scd)でのみ実行可能ファイルが生成されました。

`dotnet build` または `dotnet publish` の実行中に、使用している SDK の環境およびプラットフォームと一致する実行可能ファイルが作成されます。 これらの実行可能ファイルでは、次のような他のネイティブ実行可能ファイルと同じことを期待できます。

* 実行可能ファイルはダブルクリックすることができます。
* Windows では `myapp.exe`、Linux と macOS では`./myapp` など、コマンド プロンプトからアプリケーションを直接起動できます。

## <a name="build-copies-dependencies"></a>ビルドによる依存関係のコピー

`dotnet build` で、アプリケーションの NuGet 依存関係が NuGet キャッシュからビルド出力フォルダーにコピーされるようになりました。 以前は、依存関係のコピーは `dotnet publish` の一部としてのみ行われていました。 

リンクや razor ページの発行など、まだ発行が必要な操作がいくつかあります。


## <a name="local-dotnet-tools"></a>ローカルの dotnet ツール

.NET Core 2.1 はグローバル ツールをサポートしていましたが、.NET Core 3.0 にはローカル ツールが追加されました。 ローカル ツールはグローバル ツールに似ていますが、ディスク上の特定の場所に関連付けられています。 これで、プロジェクト単位およびリポジトリ単位のツールが可能になります。 ローカルにインストールされたツールはいずれも、グローバルでは使用できません。

ローカル ツールは、現在のディレクトリ内のマニフェスト ファイル名 `dotnet-tools.json` に依存しています。 このマニフェスト ファイルでは、使用できるツールを定義します。 リポジトリのルートにこのマニフェスト ファイルを作成することで、コードを複製したすべての人が、コードを正常に処理するために必要なツールを復元し、使用できるようになります。

ローカル ツール マニフェスト ファイルを使用できる場合は、次のコマンドを使用して、自動的にこれらのツールをローカルにダウンロードしてインストールします。

```console
dotnet tool restore
```

次のコマンドでローカル ツールを実行します。

```console
dotnet tool run <tool-command-name>
```

ローカル ツールが呼び出されると、dotnet でそのディレクトリ構造内のマニフェストが検索されます。 ツール マニフェスト ファイルが見つかると、要求されたツールが検索されます。 ツールが見つかった場合は、NuGet グローバル パッケージの場所にあるツールを見つけるために必要な情報が含まれています。 

キャッシュではなくマニフェスト内にツールが見つかった場合、ユーザーはエラーを受け取ります。 Preview 1 の後に、ユーザーが `dotnet tool restore` を実行することを要求するようにメッセージが改善される予定です。

ディレクトリにローカル ツールを追加するには、まずツール マニフェスト ファイルを作成する必要があります。 Preview 1 の後に、dotnet の新しいテンプレートなど、ツール マニフェスト ファイルを作成するためのメカニズムを提供する予定です。 Preview 1 では、`dotnet-tools.json` という次の内容のファイルを作成する必要があります。

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {}
}
```

マニフェストが作成されたら、次を使用してマニフェストにローカル ツールを追加できます。

```console
dotnet tool install <toolPackageId>
```

別のバージョンが指定されていない場合、このコマンドでツールの最新バージョンがインストールされます。  最新のバージョンが自動的に選択された場合でも、ツールのマニフェスト ファイルにツールのバージョンを書き込み、正しいバージョンのツールを復元または実行することができます。

ツール マニフェスト ファイルは、手動で編集できるように設計されています。そのため、リポジトリを操作するために必要なバージョンを更新することができます。

`dotnet-tools.json` ファイルの例を次に示します。

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {
    "dotnetsay": {
      "version": "2.1.4",
      "commands": [
        "dotnetsay"
      ]
    },
    "t-rex": {
      "version": "1.0.103",
      "commands": [
        "t-rex"
      ]
    }
  }
}
```

ツール マニフェスト ファイルからツールを削除するには、次のコマンドを実行します。

```console
dotnet tool uninstall <toolPackageId>
```

グローバル ツールとローカル ツールの両方で、ランタイムの互換バージョンが必要です。 現在 NuGet.org 上にある多くのツールは、.NET Core Runtime 2.1 をターゲットとしています。 グローバルにまたはローカルにそれらをインストールするには、[NET Core 2.1 ランタイム](https://dotnet.microsoft.com/download/dotnet-core/2.1)をインストールする必要があります。

詳細については、[Local Tools Early Preview のドキュメント](https://github.com/dotnet/cli/issues/10288)を参照してください。

## <a name="windows-desktop"></a>Windows デスクトップ

.NET Core 3.0 Preview 1 以降では、WPF および Windows フォームを使用して Windows デスクトップ アプリケーションを構築できます。 これらのフレームワークでは、Windows UI XAML ライブラリ (WinUI) の最新のコントロールと Fluent スタイルを [XAML Islands](/windows/uwp/xaml-platform/xaml-host-controls) 経由で使用することもできます。

Windows デスクトップ コンポーネントは、Windows .NET Core 3.0 SDK の一部です。

次の `dotnet` コマンドを使用して、新しい WPF または Windows フォーム アプリケーションを作成できます。

```console
dotnet new wpf
dotnet new winforms
```

また、Visual Studio 2019 Preview 1 で .NET Core 3.0 WPF および Windows フォーム プロジェクトを開き、起動し、デバッグすることもできます。 現在、Visual Studio 2017 15.9 でこれらのプロジェクトを開くことはできますが、サポートされているシナリオではありません (また、[プレビューを有効にする](https://blogs.msdn.microsoft.com/dotnet/2018/11/13/net-core-tooling-update-for-visual-studio-2017-version-15-9/)必要があります)。

新しいプロジェクトは既存の .NET Core プロジェクトと同じですが、いくつかの追加もあります。 基本的な .NET Core コンソール プロジェクトと基本的な Windows フォームおよび WPF プロジェクトとの比較を次に示します。

.NET Core コンソール プロジェクトでは、`Microsoft.NET.Sdk` SDK が使用され、`netcoreapp3.0` ターゲット フレームワークを介して .NET Core 3.0 への依存関係が宣言されます。 Windows デスクトップ アプリを作成するには、`Microsoft.NET.Sdk.WindowsDesktop` SDK を使用し、使用する UI フレームワークを選択します。

```diff
-<Project Sdk="Microsoft.NET.Sdk">
+<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
+   <UseWPF>true</UseWPF>
  </PropertyGroup>
</Project>
```

WPF でなく Windows フォームを選択するには、`UseWPF` の代わりに `UseWindowsForms` を設定します。

```diff
<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
-   <UseWPF>true</UseWPF>
+   <UseWindowsForms>true</UseWindowsForms>
  </PropertyGroup>
</Project>
```

Windows フォーム ダイアログが WPF コントロールをホストしている場合など、アプリが両方のフレームワークを使用する場合は、`UseWPF` および `UseWindowsForms` の両方を `true` に設定できます。

[dotnet/winforms](https://github.com/dotnet/winforms/issues)、[dotnet/wpf](https://github.com/dotnet/wpf/issues)、[dotnet/core](https://github.com/dotnet/core/issues) リポジトリに関するフィードバックをお寄せください。

## <a name="fast-built-in-json-support"></a>高速な組み込み JSON のサポート

`System.Text.Json.Utf8JsonReader` は、UTF-8 でエンコードされた JSON テキスト用の高パフォーマンス、低割り当て、転送のみのリーダーです。`ReadOnlySpan<byte>` から読み取られます。 `Utf8JsonReader` は基本的で低レベルの型であり、カスタム パーサーとデシリアライザーを構築するために利用できます。 新しい `Utf8JsonReader` を使用して JSON ペイロードを読み取る処理は、[Json.NET](https://www.newtonsoft.com/json) のリーダーを使用する場合より 2 倍高速です。 JSON トークンを (UTF-16) 文字列として実現する必要が出てくるまでは割り当てられません。

この新しい API には、次のコンポーネントが含まれています。

* Preview 1:JSON リーダー (シーケンシャル アクセス)
* 次の予定:JSON ライター、DOM (ランダム アクセス)、poco シリアライザー、poco デシリアライザー

出発点として使用できる `Utf8JsonReader` の基本的なリーダー ループを次に示します。

```csharp
using System.Text.Json;

public static void Utf8JsonReaderLoop(ReadOnlySpan<byte> dataUtf8)
{
    var json = new Utf8JsonReader(dataUtf8, isFinalBlock: true, state: default);

    while (json.Read())
    {
        JsonTokenType tokenType = json.TokenType;
        ReadOnlySpan<byte> valueSpan = json.ValueSpan;
        switch (tokenType)
        {
            case JsonTokenType.StartObject:
            case JsonTokenType.EndObject:
                break;
            case JsonTokenType.StartArray:
            case JsonTokenType.EndArray:
                break;
            case JsonTokenType.PropertyName:
                break;
            case JsonTokenType.String:
                string valueString = json.GetStringValue();
                break;
            case JsonTokenType.Number:
                if (!json.TryGetInt32Value(out int valueInteger))
                {
                    throw new FormatException();
                }
                break;
            case JsonTokenType.True:
            case JsonTokenType.False:
                bool valueBool = json.GetBooleanValue();
                break;
            case JsonTokenType.Null:
                break;
            default:
                throw new ArgumentException();
        }
    }

    dataUtf8 = dataUtf8.Slice((int)json.BytesConsumed);
    JsonReaderState state = json.CurrentState;
}
```

.NET エコシステムは、[Json.NET](https://www.newtonsoft.com/json) や他のよく使われている JSON ライブラリに依存しています。これは今後も推奨されます。 JSON.NET では .NET の文字列が基本のデータ型 (内部的には UTF-16) として使用されます。 

.NET Core 2.1 および 3.0 では、`Span<T>` および UTF-8 文字列の使用に基づいて、必要なメモリがより少ない JSON API (`Utf8JsonReader` など) を記述することができる新しい API を追加しました。そのため、Kestrel、ASP.NET Core Web サーバーなどの高スループット アプリケーション開発のニーズに適しています。

## <a name="ranges-and-indices"></a>範囲とインデックス

新しい `Index` 型はインデックス作成に使用できます。 先頭からカウントする `int` か、末尾からカウントするプレフィックス `^` 演算子 (C#) を使用して作成することができます。

```csharp
Index i1 = 3;  // number 3 from beginning
Index i2 = ^4; // number 4 from end
int[] a = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
Console.WriteLine($"{a[i1]}, {a[i2]}"); // "3, 6"
```

また、`Range` 型もあります。これは開始値と終了値の 2 つの `Index` 値から構成され、`x..y` の範囲式 (C#) で記述できます。 これで、スライスを生成するために `Range` を使用してインデックスを作成することができます。

```csharp
var slice = a[i1..i2]; // { 3, 4, 5 }
```

> [!NOTE]
> [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) のみが `Range` および `Index` の構文をサポートしています。

## <a name="async-streams"></a>非同期ストリーム

`IAsyncEnumerable<T>` 型は、`IEnumerable<T>` の新しい非同期バージョンです。 この言語では、その要素を使用するためにこれらよりも `await foreach` を行い、要素を生成するために `yield return` を行うことができます。

非同期ストリームの生成の両方の使用例を次に示します。 `foreach` ステートメントは非同期であり、`yield return` を使用して呼び出し元の非同期ストリームを生成します。 (`yield return` を使用する) このパターンは、非同期ストリームを生成するモデルに推奨されます。

```csharp
async IAsyncEnumerable<int> GetBigResultsAsync()
{
    await foreach (var result in GetResultsAsync())
    {
        if (result > 20) yield return result; 
    }
}
```

> [!WARNING]
> 現在、.NET Core 3.0 Preview 1 の `await foreach` にはバグがあります。 代わりに、`GetEnumerator` および `MoveNext` を使用して要素を処理してください。 詳細については、[roslyn/#31268](https://github.com/dotnet/roslyn/issues/31268) を参照してください。

`await foreach` を実行できるだけでなく、非同期反復子を作成することもできます。たとえば、`await` と`yield` の両方を行うことができる `IAsyncEnumerable/IAsyncEnumerator` を返す反復子です。 破棄する必要があるオブジェクトの場合は、`Stream` や `Timer` など、さまざまな BCL 型が実装する `IAsyncDisposable` を使用できます。

> [!NOTE]
> [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) のみが `await foreach` の構文をサポートしています。

## <a name="type-sequencereader"></a>型:SequenceReader

.NET Core 3.0 には、`ReadOnlySequence<T>` のリーダーとして使用できる `System.Buffers.SequenceReader` が追加されました。 これにより、バッキング バッファーを複数回通過できる `System.IO.Pipelines` データの簡単、高パフォーマンスな、低割り当ての解析が可能になります。 

次の例では、入力 `Sequence` を有効な `CR/LF` 区切りの行に分割します。

```csharp
private static ReadOnlySpan<byte> CRLF => new byte[] { (byte)'\r', (byte)'\n' };

public static void ReadLines(ReadOnlySequence<byte> sequence)
{
    SequenceReader<byte> reader = new SequenceReader<byte>(sequence);

    while (!reader.End)
    {
        if (!reader.TryReadToAny(out ReadOnlySpan<byte> line, CRLF, advancePastDelimiter:false))
        {
            // Couldn't find another delimiter
            // ...
        }

        if (!reader.IsNext(CRLF, advancePast: true))
        {
            // Not a good CR/LF pair
            // ...
        }

        // line is valid, process
        ProcessLine(line);
    }
}
```

## <a name="type-metadataloadcontext"></a>型:MetadataLoadContext

呼び出し元のアプリケーション ドメインに影響を与えることなく、アセンブリ メタデータを読み取ることができる `MetadataLoadContext` 型が追加されました。 現在の運用環境とは異なるアーキテクチャおよびプラットフォーム向けに構築されたアセンブリなど、アセンブリはデータとして読み込まれます。 `MetadataLoadContext` は <xref:System.Reflection.Assembly.ReflectionOnlyLoad*> と重複しています。これは .NET Framework でのみ使用できます。

`MetdataLoadContext` は、[System.Reflection.MetadataLoadContext パッケージ](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext)で使用できます。 これは .NET Standard 2.0 パッケージです。

`MetadataLoadContext` は、<xref:System.Runtime.Loader.AssemblyLoadContext> 型に似ていますがその型に基づいていない API を公開しています。 <xref:System.Runtime.Loader.AssemblyLoadContext> と同様に、`MetadataLoadContext` を使用すると、分離したアセンブリの読み込み中にアセンブリを読み込むことができます。 `MetdataLoadContext` API から <xref:System.Reflection.Assembly> オブジェクトが返され、使い慣れたリフレクション API を使用できるようになります。 [MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127) などの実行指向の API は使用できず、InvalidOperationException がスローされます。

次のサンプルは、特定のインターフェイスを実装するアセンブリ内で具象型を検索する方法を示しています。

```csharp
var paths = new string[] {@"C:\myapp\mscorlib.dll", @"C:\myapp\myapp.dll"};
var resolver = new PathAssemblyResolver(paths);
using (var lc = new MetadataLoadContext(resolver))
{
    Assembly a = lc.LoadFromAssemblyName("myapp");
    Type myInterface = a.GetType("MyApp.IPluginInterface");
    foreach (Type t in a.GetTypes())
    {
        if (t.IsClass && myInterface.IsAssignableFrom(t))
            Console.WriteLine($"Class {t.FullName} implements IPluginInterface");
    }
}
```

`MetadataLoadContext` のシナリオには、一連のアセンブリをデータとして検査し、検査の実行後にすべてのファイル ロックとメモリを解放する必要がある、設計時の機能、ビルド時のツール、およびランタイムのライトアップ機能が含まれます。

`MetadataLoadContext` には、コンストラクターに渡されるリゾルバー クラスがあります。 リゾルバーのジョブは、`AssemblyName` が指定された `Assembly` の読み込みです。 リゾルバー クラスは、抽象 `MetadataAssemblyResolver` クラスから派生します。 パスベースのシナリオの場合、リゾルバーの実装は `PathAssemblyResolver` で提供されています。

[MetadataLoadContext テスト](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests)は多数のユース ケースを示しています。 [アセンブリ テスト](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs)から始めることをお勧めします。

## <a name="tls-13--openssl-111-on-linux"></a>Linux 上の TLS 1.3 と OpenSSL 1.1.1

現在、.NET Core では、特定の環境で使用できるようになったら、[OpenSSL 1.1.1 の TLS 1.3 のサポート](https://www.openssl.org/blog/blog/2018/09/11/release111/)を利用する予定です。 [OpenSSL チーム](https://www.openssl.org/blog/blog/2018/09/11/release111/)によると、TLS 1.3 には複数の利点があります。

* クライアントとサーバー間に必要なラウンド トリップ回数の減少による接続時間の改善。

* さまざまな非推奨で安全ではない暗号化アルゴリズムの削除と、より多くの接続ハンドシェイクの暗号化によるセキュリティの向上。

.NET Core 3.0 Preview 1 では、**OpenSSL 1.1.1**、**OpenSSL 1.1.0**、または **OpenSSL 1.0.2** を利用することができます (Linux システム上で検出された任意の最適なバージョン)。  **OpenSSL 1.1.1** を使用可能で、クライアントとサーバーの両方が **TLS 1.3** をサポートしている場合、`SslProtocols.None` (システムの既定のプロトコル) を使用するときに、SslStream 型と HttpClient 型は **TLS 1.3** を使用します。

次のサンプルは、<https://www.cloudflare.com> に接続している Ubuntu 18.10 上の .NET Core 3.0 Preview 1 を示しています。

```csharp
using System;
using System.Net.Security;
using System.Net.Sockets;
using System.Threading.Tasks;

namespace tlstest
{
    class Program
    {
        static async Task Main()
        {
            using (TcpClient tcpClient = new TcpClient())
            {
                string targetHost = "www.cloudflare.com";

                await tcpClient.ConnectAsync(targetHost, 443);

                using (SslStream sslStream = new SslStream(tcpClient.GetStream()))
                {
                    await sslStream.AuthenticateAsClientAsync(targetHost);
                    await Console.Out.WriteLineAsync($"Connected to {targetHost} with {sslStream.SslProtocol}");
                }
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/tlstest$ dotnet run
Connected to www.cloudflare.com with Tls13
user@comp-ubuntu1810:~/tlstest$ openssl version
OpenSSL 1.1.1  11 Sep 2018
```

>[!IMPORTANT]
>Windows と macOS はまだ **TLS 1.3** をサポートしていません。 サポートされるようになったら、.NET Core 3.0 はこれらのオペレーティング システムで **TLS 1.3** をサポートする予定です。

## <a name="cryptography"></a>暗号

`System.Security.Cryptography.AesGcm` および `System.Security.Cryptography.AesCcm` で実装された **AES-GCM** および **AES-CCM** 暗号のサポートが追加されました。 これらのアルゴリズムは、[Authenticated Encryption with Association Data (AEAD) アルゴリズム](https://en.wikipedia.org/wiki/Authenticated_encryption) であり、.NET Core に追加された最初の Authenticated Encryption (AE) アルゴリズムでもあります。

次のコードは、**AesGcm** 暗号を使用してランダム データの暗号化と復号化を行う例です。

**AesCcm** のコードは、ほぼ同じになります (クラスの変数名のみが異なります)。

```csharp
// key should be: pre-known, derived, or transported via another channel, such as RSA encryption
byte[] key = new byte[16];
RandomNumberGenerator.Fill(key);

byte[] nonce = new byte[12];
RandomNumberGenerator.Fill(nonce);

// normally this would be your data
byte[] dataToEncrypt = new byte[1234];
byte[] associatedData = new byte[333];
RandomNumberGenerator.Fill(dataToEncrypt);
RandomNumberGenerator.Fill(associatedData);

// these will be filled during the encryption
byte[] tag = new byte[16];
byte[] ciphertext = new byte[dataToEncrypt.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Encrypt(nonce, dataToEncrypt, ciphertext, tag, associatedData);
}

// tag, nonce, ciphertext, associatedData should be sent to the other part

byte[] decryptedData = new byte[ciphertext.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Decrypt(nonce, ciphertext, tag, decryptedData, associatedData);
}

// do something with the data
// this should always print that data is the same
Console.WriteLine($"AES-GCM: Decrypted data is{(dataToEncrypt.SequenceEqual(decryptedData) ? "the same as" : "different than")} original data.");
```

## <a name="cryptographic-key-importexport"></a>暗号化キーのインポート/エクスポート

.NET Core 3.0 Preview 1 は、標準形式からの非対称の公開キーと秘密キーのインポートとエクスポートをサポートしています。X.509 証明書を使用する必要はありません。

すべてのキーの種類 (RSA、DSA、ECDsa、ECDiffieHellman) は、公開キー用の **X.509 SubjectPublicKeyInfo** 形式と、秘密キー用の **PKCS#8 PrivateKeyInfo** および **PKCS#8 EncryptedPrivateKeyInfo** 形式をサポートしています。 RSA は、さらに **PKCS#1 RSAPublicKey** および **PKCS#1 RSAPrivateKey** をサポートしています。 いずれのエクスポートメソッドからも、DER でエンコードされたバイナリ データが生成され、インポート メソッドもそのようなデータを期待します。 キーがテキストに適した PEM 形式で格納されている場合、呼び出し元は import メソッドを呼び出す前にコンテンツを base64 でデコードする必要があります。

```csharp
using System;
using System.IO;
using System.Security.Cryptography;

namespace rsakeyprint
{
    class Program
    {
        static void Main(string[] args)
        {
            using (RSA rsa = RSA.Create())
            {
                byte[] keyBytes = File.ReadAllBytes(args[0]);
                rsa.ImportRSAPrivateKey(keyBytes, out int bytesRead);
 
                Console.WriteLine($"Read {bytesRead} bytes, {keyBytes.Length-bytesRead} extra byte(s) in file.");
                RSAParameters rsaParameters = rsa.ExportParameters(true);
                Console.WriteLine(BitConverter.ToString(rsaParameters.D));
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/rsakeyprint$ echo Making a small key to save on screen space.
Making a small key to save on screen space.
user@comp-ubuntu1810:~/rsakeyprint$ openssl genrsa 768 | openssl rsa -outform der -out rsa.key
Generating RSA private key, 768 bit long modulus (2 primes)
..+++++++
........+++++++
e is 65537 (0x010001)
writing RSA key
user@comp-ubuntu1810:~/rsakeyprint$ dotnet run rsa.key
Read 461 bytes, 0 extra byte(s) in file.
0F-D0-82-34-F8-13-38-4A-7F-C7-52-4A-F6-93-F8-FB-6D-98-7A-6A-04-3B-BC-35-8C-7D-AC-A5-A3-6E-AD-C1-66-30-81-2C-2A-DE-DA-60-03-6A-2C-D9-76-15-7F-61-97-57-
79-E1-6E-45-62-C3-83-04-97-CB-32-EF-C5-17-5F-99-60-92-AE-B6-34-6F-30-06-03-AC-BF-15-24-43-84-EB-83-60-EF-4D-3B-BD-D9-5D-56-26-F0-51-CE-F1
user@comp-ubuntu1810:~/rsakeyprint$ openssl rsa -in rsa.key -inform der -text -noout | grep -A7 private
privateExponent:
    0f:d0:82:34:f8:13:38:4a:7f:c7:52:4a:f6:93:f8:
    fb:6d:98:7a:6a:04:3b:bc:35:8c:7d:ac:a5:a3:6e:
    ad:c1:66:30:81:2c:2a:de:da:60:03:6a:2c:d9:76:
    15:7f:61:97:57:79:e1:6e:45:62:c3:83:04:97:cb:
    32:ef:c5:17:5f:99:60:92:ae:b6:34:6f:30:06:03:
    ac:bf:15:24:43:84:eb:83:60:ef:4d:3b:bd:d9:5d:
    56:26:f0:51:ce:f1
```

PKCS#8 ファイルは `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo` クラスで検査できます。

PFX/PKCS#12 ファイルは、それぞれ `System.Security.Cryptography.Pkcs.Pkcs12Info` および `System.Security.Cryptography.Pkcs.Pkcs12Builder` を使用して検査および操作できます。

## <a name="serialport-for-linux"></a>Linux 用 SerialPort

.NET Core 3.0 は Linux 上で <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType> をサポートするようになりました。

以前の .NET Core では、Windows 上の `SerialPort` 型の使用のみをサポートしていました。

## <a name="more-bcl-improvements"></a>その他の BCL の機能強化

.NET Core 2.1 で導入された `Span<T>`、`Memory<T>`、および関連する型は、.NET Core 3.0 で最適化されました。 スパン構築、スライス、解析、書式設定などの一般的な操作がより効率的になりました。 

さらに、`String` のような型が内部的に改善され、`Dictionary<TKey, TValue>` やその他のコレクションのキーとして使用した場合の効率が改善されました。 これらの機能強化を利用するためにコードを変更する必要はありません。

.NET Core 3 Preview 1 では、次の機能強化も追加されました。

* HttpClient に組み込まれた Brotli のサポート
* ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)
* Unsafe.Unbox
* CancellationToken.Unregister
* 複合算術演算子
* TCP のキープ アライブのためのソケット API
* StringBuilder.GetChunks
* IPEndPoint の解析
* RandomNumberGenerator.GetInt32

## <a name="tiered-compilation"></a>階層型コンパイル

.NET Core 3.0 では、[階層型コンパイル](https://blogs.msdn.microsoft.com/dotnet/2018/08/02/tiered-compilation-preview-in-net-core-2-1/)が既定で有効になりました。 起動時とスループットの最大化の両方でパフォーマンスを向上するために、状況に応じてランタイムが Just-In-Time (JIT) コンパイラを使用できるようにする機能です。

この機能は、[.NET Core 2.1](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) のオプトイン機能として追加され、[.NET Core 2.2 Preview 2](https://blogs.msdn.microsoft.com/dotnet/2018/09/12/announcing-net-core-2-2-preview-2/) で既定で有効になっています。 その後、.NET Core 2.2 リリースではオプトイン機能に戻りました。

## <a name="arm64-linux-support"></a>ARM64 Linux のサポート

今回のリリースでは、ARM64 for Linux のサポートが追加されています。 コンテキストのために、.NET Core 2.1 では ARM32 for Linux のサポート、.NET Core 2.2 では Windows のサポートを追加しました。 現在、ARM64 の主なユース ケースは、IoT シナリオを使用しています。

Alpine、Debian、Ubuntu [Docker イメージは .NET Core for ARM64](https://hub.docker.com/r/microsoft/dotnet/) で使用できます。

詳細については、「[.NET Core ARM64 Status](https://github.com/dotnet/announcements/issues/82)」(.NET Core Runtime ARM64 の状態) を確認してください。

>[!NOTE]
> **ARM64** Windows のサポートはまだ使用できません。
