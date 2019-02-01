---
title: dotnet コマンド
description: dotnet コマンド (.NET Core CLI ツールの一般的なドライバー) とその使用法について説明します。
ms.date: 06/04/2018
ms.openlocfilehash: 53eb96ee6fe809b2e6e42eec4e7e9b5f7c5edf2a
ms.sourcegitcommit: d9a0071d0fd490ae006c816f78a563b9946e269a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2019
ms.locfileid: "55066442"
---
# <a name="dotnet-command"></a><span data-ttu-id="88c06-103">dotnet コマンド</span><span class="sxs-lookup"><span data-stu-id="88c06-103">dotnet command</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="88c06-104">name</span><span class="sxs-lookup"><span data-stu-id="88c06-104">Name</span></span>

<span data-ttu-id="88c06-105">`dotnet` - .NET のソース コードとバイナリを管理するためのツール。</span><span class="sxs-lookup"><span data-stu-id="88c06-105">`dotnet` - A tool for managing .NET source code and binaries.</span></span>

## <a name="synopsis"></a><span data-ttu-id="88c06-106">構文</span><span class="sxs-lookup"><span data-stu-id="88c06-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="88c06-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="88c06-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [--list-runtimes] [--list-sdks] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="88c06-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="88c06-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics]
    [--fx-version] [-h|--help] [--info] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="88c06-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="88c06-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet [command] [arguments] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [-v|--verbosity] [--version]
```
---

## <a name="description"></a><span data-ttu-id="88c06-110">説明</span><span class="sxs-lookup"><span data-stu-id="88c06-110">Description</span></span>

<span data-ttu-id="88c06-111">`dotnet` は .NET のソース コードとバイナリを管理するためのツールです。</span><span class="sxs-lookup"><span data-stu-id="88c06-111">`dotnet` is a tool for managing .NET source code and binaries.</span></span> <span data-ttu-id="88c06-112">[`dotnet build`](dotnet-build.md) や [`dotnet run`](dotnet-run.md) のような特定のタスクを実行するコマンドを公開します。</span><span class="sxs-lookup"><span data-stu-id="88c06-112">It exposes commands that perform specific tasks, such as [`dotnet build`](dotnet-build.md) and [`dotnet run`](dotnet-run.md).</span></span> <span data-ttu-id="88c06-113">各コマンドによって、それ自体の引数が定義されます。</span><span class="sxs-lookup"><span data-stu-id="88c06-113">Each command defines its own arguments.</span></span> <span data-ttu-id="88c06-114">各コマンドの後ろに `--help` と入力すると、短いヘルプ ドキュメントにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="88c06-114">Type `--help` after each command to access brief help documentation.</span></span>

<span data-ttu-id="88c06-115">`dotnet` は、`dotnet myapp.dll` など、アプリケーション DLL を指定することで、アプリケーションを実行するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="88c06-115">`dotnet` can be used to run applications, by specifying an application DLL, such as `dotnet myapp.dll`.</span></span> <span data-ttu-id="88c06-116">展開オプションについては、「[.NET Core アプリケーションの展開](../deploying/index.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88c06-116">See [.NET Core application deployment](../deploying/index.md) for to learn about deployment options.</span></span>

## <a name="options"></a><span data-ttu-id="88c06-117">オプション</span><span class="sxs-lookup"><span data-stu-id="88c06-117">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="88c06-118">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="88c06-118">.NET Core 2.1</span></span>](#tab/netcore21)

`--additional-deps <PATH>`

<span data-ttu-id="88c06-119">追加の *deps.json* ファイルへのパスです。</span><span class="sxs-lookup"><span data-stu-id="88c06-119">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="88c06-120">プローブ ポリシーとプローブするアセンブリを含むパスです。</span><span class="sxs-lookup"><span data-stu-id="88c06-120">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="88c06-121">診断出力を有効にします。</span><span class="sxs-lookup"><span data-stu-id="88c06-121">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="88c06-122">アプリケーションを実行するために使用する .NET Core ランタイムのバージョン。</span><span class="sxs-lookup"><span data-stu-id="88c06-122">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="88c06-123">`dotnet build --help` など、特定のコマンドのドキュメントを出力します。</span><span class="sxs-lookup"><span data-stu-id="88c06-123">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="88c06-124">`dotnet --help` では、使用できるコマンドの一覧が出力されます。</span><span class="sxs-lookup"><span data-stu-id="88c06-124">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="88c06-125">現在のオペレーティング システムや .NET Core バージョンのコミット SHA など、.NET Core インストールとコンピューター環境に関する詳細を出力します。</span><span class="sxs-lookup"><span data-stu-id="88c06-125">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--list-runtimes`

<span data-ttu-id="88c06-126">インストールされている .NET Core ランタイムを表示します。</span><span class="sxs-lookup"><span data-stu-id="88c06-126">Displays the installed .NET Core runtimes.</span></span>

`--list-sdks`

<span data-ttu-id="88c06-127">インストールされている .NET Core SDK を表示します。</span><span class="sxs-lookup"><span data-stu-id="88c06-127">Displays the installed .NET Core SDKs.</span></span>

`--roll-forward-on-no-candidate-fx <N>`

<span data-ttu-id="88c06-128">必要な共有フレームワークが利用できない場合の動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="88c06-128">Defines behavior when the required shared framework is not available.</span></span> <span data-ttu-id="88c06-129">`N` には以下があります。</span><span class="sxs-lookup"><span data-stu-id="88c06-129">`N` can be:</span></span>
 * <span data-ttu-id="88c06-130">`0` - マイナー バージョンのロールフォワードでも無効にします。</span><span class="sxs-lookup"><span data-stu-id="88c06-130">`0` - Disable even minor version roll forward.</span></span>
 * <span data-ttu-id="88c06-131">`1` - マイナー バージョンはロール フォワードしますが、メジャー バージョンはしません。</span><span class="sxs-lookup"><span data-stu-id="88c06-131">`1` - Roll forward on minor version, but not on major version.</span></span> <span data-ttu-id="88c06-132">これが既定の動作です。</span><span class="sxs-lookup"><span data-stu-id="88c06-132">This is the default behavior.</span></span>
 * <span data-ttu-id="88c06-133">`2` - マイナー バージョンとメジャー バージョンをロール フォワードします。</span><span class="sxs-lookup"><span data-stu-id="88c06-133">`2` - Roll forward on minor and major versions.</span></span>

 <span data-ttu-id="88c06-134">詳細については、「[Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward)」(ロールフォワード) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88c06-134">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="88c06-135">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="88c06-135">Sets the verbosity level of the command.</span></span> <span data-ttu-id="88c06-136">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="88c06-136">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="88c06-137">一部のコマンドではサポートされていません。このオプションが使用可能かどうかを判断するには、対象のコマンドのページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88c06-137">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="88c06-138">使用中の .NET Core SDK のバージョンを印刷します。</span><span class="sxs-lookup"><span data-stu-id="88c06-138">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="88c06-139">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="88c06-139">.NET Core 2.0</span></span>](#tab/netcore20)

`--additional-deps <PATH>`

<span data-ttu-id="88c06-140">追加の *deps.json* ファイルへのパスです。</span><span class="sxs-lookup"><span data-stu-id="88c06-140">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="88c06-141">プローブ ポリシーとプローブするアセンブリを含むパスです。</span><span class="sxs-lookup"><span data-stu-id="88c06-141">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="88c06-142">診断出力を有効にします。</span><span class="sxs-lookup"><span data-stu-id="88c06-142">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="88c06-143">アプリケーションを実行するために使用する .NET Core ランタイムのバージョン。</span><span class="sxs-lookup"><span data-stu-id="88c06-143">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="88c06-144">`dotnet build --help` など、特定のコマンドのドキュメントを出力します。</span><span class="sxs-lookup"><span data-stu-id="88c06-144">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="88c06-145">`dotnet --help` では、使用できるコマンドの一覧が出力されます。</span><span class="sxs-lookup"><span data-stu-id="88c06-145">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="88c06-146">現在のオペレーティング システムや .NET Core バージョンのコミット SHA など、.NET Core インストールとコンピューター環境に関する詳細を出力します。</span><span class="sxs-lookup"><span data-stu-id="88c06-146">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="88c06-147">`0` に設定されている場合、マイナー バージョンのロールフォワードを無効にします。</span><span class="sxs-lookup"><span data-stu-id="88c06-147">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="88c06-148">詳細については、「[Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward)」(ロールフォワード) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88c06-148">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="88c06-149">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="88c06-149">Sets the verbosity level of the command.</span></span> <span data-ttu-id="88c06-150">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="88c06-150">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="88c06-151">一部のコマンドではサポートされていません。このオプションが使用可能かどうかを判断するには、対象のコマンドのページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88c06-151">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="88c06-152">使用中の .NET Core SDK のバージョンを印刷します。</span><span class="sxs-lookup"><span data-stu-id="88c06-152">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="88c06-153">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="88c06-153">.NET Core 1.x</span></span>](#tab/netcore1x)

`--additionalprobingpath <PATH>`

<span data-ttu-id="88c06-154">プローブ ポリシーとプローブするアセンブリを含むパスです。</span><span class="sxs-lookup"><span data-stu-id="88c06-154">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="88c06-155">診断出力を有効にします。</span><span class="sxs-lookup"><span data-stu-id="88c06-155">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="88c06-156">アプリケーションを実行するために使用する .NET Core ランタイムのバージョン。</span><span class="sxs-lookup"><span data-stu-id="88c06-156">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="88c06-157">`dotnet build --help` など、特定のコマンドのドキュメントを出力します。</span><span class="sxs-lookup"><span data-stu-id="88c06-157">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="88c06-158">`dotnet --help` では、使用できるコマンドの一覧が出力されます。</span><span class="sxs-lookup"><span data-stu-id="88c06-158">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="88c06-159">現在のオペレーティング システムや .NET Core バージョンのコミット SHA など、.NET Core インストールとコンピューター環境に関する詳細を出力します。</span><span class="sxs-lookup"><span data-stu-id="88c06-159">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="88c06-160">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="88c06-160">Sets the verbosity level of the command.</span></span> <span data-ttu-id="88c06-161">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="88c06-161">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="88c06-162">一部のコマンドではサポートされていません。このオプションが使用可能かどうかを判断するには、対象のコマンドのページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88c06-162">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="88c06-163">使用中の .NET Core SDK のバージョンを印刷します。</span><span class="sxs-lookup"><span data-stu-id="88c06-163">Prints out the version of the .NET Core SDK in use.</span></span>

---

## <a name="dotnet-commands"></a><span data-ttu-id="88c06-164">dotnet コマンド</span><span class="sxs-lookup"><span data-stu-id="88c06-164">dotnet commands</span></span>

### <a name="general"></a><span data-ttu-id="88c06-165">全般</span><span class="sxs-lookup"><span data-stu-id="88c06-165">General</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="88c06-166">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="88c06-166">.NET Core 2.1</span></span>](#tab/netcore21)

| <span data-ttu-id="88c06-167">コマンド</span><span class="sxs-lookup"><span data-stu-id="88c06-167">Command</span></span>                                       | <span data-ttu-id="88c06-168">関数</span><span class="sxs-lookup"><span data-stu-id="88c06-168">Function</span></span>                                                            |
| --------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="88c06-169">dotnet build</span><span class="sxs-lookup"><span data-stu-id="88c06-169">dotnet build</span></span>](dotnet-build.md)               | <span data-ttu-id="88c06-170">.NET Core アプリケーションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="88c06-170">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="88c06-171">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="88c06-171">dotnet build-server</span></span>](dotnet-build-server.md) | <span data-ttu-id="88c06-172">ビルドによって起動されたサーバーとやり取りします。</span><span class="sxs-lookup"><span data-stu-id="88c06-172">Interacts with servers started by a build.</span></span>                          |
| [<span data-ttu-id="88c06-173">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="88c06-173">dotnet clean</span></span>](dotnet-clean.md)               | <span data-ttu-id="88c06-174">クリーン ビルド出力です。</span><span class="sxs-lookup"><span data-stu-id="88c06-174">Clean build outputs.</span></span>                                                |
| [<span data-ttu-id="88c06-175">dotnet help</span><span class="sxs-lookup"><span data-stu-id="88c06-175">dotnet help</span></span>](dotnet-help.md)                 | <span data-ttu-id="88c06-176">コマンドのより詳細なドキュメントをオンラインで表示します。</span><span class="sxs-lookup"><span data-stu-id="88c06-176">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="88c06-177">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="88c06-177">dotnet migrate</span></span>](dotnet-migrate.md)           | <span data-ttu-id="88c06-178">有効な Preview 2 プロジェクトを .NET Core SDK 1.0 プロジェクトに移行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-178">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="88c06-179">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="88c06-179">dotnet msbuild</span></span>](dotnet-msbuild.md)           | <span data-ttu-id="88c06-180">MSBuild コマンド ラインへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="88c06-180">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="88c06-181">dotnet new</span><span class="sxs-lookup"><span data-stu-id="88c06-181">dotnet new</span></span>](dotnet-new.md)                   | <span data-ttu-id="88c06-182">指定されたテンプレートの C# または F# プロジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="88c06-182">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="88c06-183">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="88c06-183">dotnet pack</span></span>](dotnet-pack.md)                 | <span data-ttu-id="88c06-184">コードの NuGet パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="88c06-184">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="88c06-185">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="88c06-185">dotnet publish</span></span>](dotnet-publish.md)           | <span data-ttu-id="88c06-186">.NET Framework に依存するアプリケーションまたは自己完結型アプリケーションを発行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-186">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="88c06-187">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="88c06-187">dotnet restore</span></span>](dotnet-restore.md)           | <span data-ttu-id="88c06-188">指定されたアプリケーションの依存関係を復元します。</span><span class="sxs-lookup"><span data-stu-id="88c06-188">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="88c06-189">dotnet run</span><span class="sxs-lookup"><span data-stu-id="88c06-189">dotnet run</span></span>](dotnet-run.md)                   | <span data-ttu-id="88c06-190">ソースからアプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-190">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="88c06-191">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="88c06-191">dotnet sln</span></span>](dotnet-sln.md)                   | <span data-ttu-id="88c06-192">ソリューション ファイルのプロジェクトを追加、削除、一覧表示するオプション。</span><span class="sxs-lookup"><span data-stu-id="88c06-192">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="88c06-193">dotnet store</span><span class="sxs-lookup"><span data-stu-id="88c06-193">dotnet store</span></span>](dotnet-store.md)               | <span data-ttu-id="88c06-194">ランタイム パッケージ ストアにアセンブリを格納します。</span><span class="sxs-lookup"><span data-stu-id="88c06-194">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="88c06-195">dotnet test</span><span class="sxs-lookup"><span data-stu-id="88c06-195">dotnet test</span></span>](dotnet-test.md)                 | <span data-ttu-id="88c06-196">テスト ランナーを使用してテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-196">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="88c06-197">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="88c06-197">.NET Core 2.0</span></span>](#tab/netcore20)

| <span data-ttu-id="88c06-198">コマンド</span><span class="sxs-lookup"><span data-stu-id="88c06-198">Command</span></span>                             | <span data-ttu-id="88c06-199">関数</span><span class="sxs-lookup"><span data-stu-id="88c06-199">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="88c06-200">dotnet build</span><span class="sxs-lookup"><span data-stu-id="88c06-200">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="88c06-201">.NET Core アプリケーションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="88c06-201">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="88c06-202">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="88c06-202">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="88c06-203">クリーン ビルド出力です。</span><span class="sxs-lookup"><span data-stu-id="88c06-203">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="88c06-204">dotnet help</span><span class="sxs-lookup"><span data-stu-id="88c06-204">dotnet help</span></span>](dotnet-help.md)       | <span data-ttu-id="88c06-205">コマンドのより詳細なドキュメントをオンラインで表示します。</span><span class="sxs-lookup"><span data-stu-id="88c06-205">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="88c06-206">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="88c06-206">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="88c06-207">有効な Preview 2 プロジェクトを .NET Core SDK 1.0 プロジェクトに移行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-207">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="88c06-208">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="88c06-208">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="88c06-209">MSBuild コマンド ラインへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="88c06-209">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="88c06-210">dotnet new</span><span class="sxs-lookup"><span data-stu-id="88c06-210">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="88c06-211">指定されたテンプレートの C# または F# プロジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="88c06-211">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="88c06-212">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="88c06-212">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="88c06-213">コードの NuGet パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="88c06-213">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="88c06-214">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="88c06-214">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="88c06-215">.NET Framework に依存するアプリケーションまたは自己完結型アプリケーションを発行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-215">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="88c06-216">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="88c06-216">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="88c06-217">指定されたアプリケーションの依存関係を復元します。</span><span class="sxs-lookup"><span data-stu-id="88c06-217">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="88c06-218">dotnet run</span><span class="sxs-lookup"><span data-stu-id="88c06-218">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="88c06-219">ソースからアプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-219">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="88c06-220">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="88c06-220">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="88c06-221">ソリューション ファイルのプロジェクトを追加、削除、一覧表示するオプション。</span><span class="sxs-lookup"><span data-stu-id="88c06-221">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="88c06-222">dotnet store</span><span class="sxs-lookup"><span data-stu-id="88c06-222">dotnet store</span></span>](dotnet-store.md)     | <span data-ttu-id="88c06-223">ランタイム パッケージ ストアにアセンブリを格納します。</span><span class="sxs-lookup"><span data-stu-id="88c06-223">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="88c06-224">dotnet test</span><span class="sxs-lookup"><span data-stu-id="88c06-224">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="88c06-225">テスト ランナーを使用してテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-225">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="88c06-226">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="88c06-226">.NET Core 1.x</span></span>](#tab/netcore1x)

| <span data-ttu-id="88c06-227">コマンド</span><span class="sxs-lookup"><span data-stu-id="88c06-227">Command</span></span>                             | <span data-ttu-id="88c06-228">関数</span><span class="sxs-lookup"><span data-stu-id="88c06-228">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="88c06-229">dotnet build</span><span class="sxs-lookup"><span data-stu-id="88c06-229">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="88c06-230">.NET Core アプリケーションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="88c06-230">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="88c06-231">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="88c06-231">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="88c06-232">クリーン ビルド出力です。</span><span class="sxs-lookup"><span data-stu-id="88c06-232">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="88c06-233">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="88c06-233">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="88c06-234">有効な Preview 2 プロジェクトを .NET Core SDK 1.0 プロジェクトに移行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-234">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="88c06-235">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="88c06-235">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="88c06-236">MSBuild コマンド ラインへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="88c06-236">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="88c06-237">dotnet new</span><span class="sxs-lookup"><span data-stu-id="88c06-237">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="88c06-238">指定されたテンプレートの C# または F# プロジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="88c06-238">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="88c06-239">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="88c06-239">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="88c06-240">コードの NuGet パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="88c06-240">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="88c06-241">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="88c06-241">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="88c06-242">.NET Framework に依存するアプリケーションまたは自己完結型アプリケーションを発行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-242">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="88c06-243">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="88c06-243">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="88c06-244">指定されたアプリケーションの依存関係を復元します。</span><span class="sxs-lookup"><span data-stu-id="88c06-244">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="88c06-245">dotnet run</span><span class="sxs-lookup"><span data-stu-id="88c06-245">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="88c06-246">ソースからアプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-246">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="88c06-247">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="88c06-247">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="88c06-248">ソリューション ファイルのプロジェクトを追加、削除、一覧表示するオプション。</span><span class="sxs-lookup"><span data-stu-id="88c06-248">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="88c06-249">dotnet test</span><span class="sxs-lookup"><span data-stu-id="88c06-249">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="88c06-250">テスト ランナーを使用してテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-250">Runs tests using a test runner.</span></span>                                     |

---

### <a name="project-references"></a><span data-ttu-id="88c06-251">プロジェクト参照</span><span class="sxs-lookup"><span data-stu-id="88c06-251">Project references</span></span>

<span data-ttu-id="88c06-252">コマンド</span><span class="sxs-lookup"><span data-stu-id="88c06-252">Command</span></span> | <span data-ttu-id="88c06-253">関数</span><span class="sxs-lookup"><span data-stu-id="88c06-253">Function</span></span>
--- | ---
[<span data-ttu-id="88c06-254">dotnet add reference</span><span class="sxs-lookup"><span data-stu-id="88c06-254">dotnet add reference</span></span>](dotnet-add-reference.md) | <span data-ttu-id="88c06-255">プロジェクト参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="88c06-255">Adds a project reference.</span></span>
[<span data-ttu-id="88c06-256">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="88c06-256">dotnet list reference</span></span>](dotnet-list-reference.md) | <span data-ttu-id="88c06-257">プロジェクト参照をリストします。</span><span class="sxs-lookup"><span data-stu-id="88c06-257">Lists project references.</span></span>
[<span data-ttu-id="88c06-258">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="88c06-258">dotnet remove reference</span></span>](dotnet-remove-reference.md) | <span data-ttu-id="88c06-259">プロジェクト参照を削除します。</span><span class="sxs-lookup"><span data-stu-id="88c06-259">Removes a project reference.</span></span>

### <a name="nuget-packages"></a><span data-ttu-id="88c06-260">NuGet パッケージ</span><span class="sxs-lookup"><span data-stu-id="88c06-260">NuGet packages</span></span>

<span data-ttu-id="88c06-261">コマンド</span><span class="sxs-lookup"><span data-stu-id="88c06-261">Command</span></span> | <span data-ttu-id="88c06-262">関数</span><span class="sxs-lookup"><span data-stu-id="88c06-262">Function</span></span>
--- | ---
[<span data-ttu-id="88c06-263">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="88c06-263">dotnet add package</span></span>](dotnet-add-package.md) | <span data-ttu-id="88c06-264">NuGet パッケージを追加します。</span><span class="sxs-lookup"><span data-stu-id="88c06-264">Adds a NuGet package.</span></span>
[<span data-ttu-id="88c06-265">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="88c06-265">dotnet remove package</span></span>](dotnet-remove-package.md) | <span data-ttu-id="88c06-266">NuGet パッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="88c06-266">Removes a NuGet package.</span></span>

### <a name="nuget-commands"></a><span data-ttu-id="88c06-267">NuGet コマンド</span><span class="sxs-lookup"><span data-stu-id="88c06-267">NuGet commands</span></span>

<span data-ttu-id="88c06-268">コマンド</span><span class="sxs-lookup"><span data-stu-id="88c06-268">Command</span></span> | <span data-ttu-id="88c06-269">関数</span><span class="sxs-lookup"><span data-stu-id="88c06-269">Function</span></span>
--- | ---
[<span data-ttu-id="88c06-270">dotnet nuget delete</span><span class="sxs-lookup"><span data-stu-id="88c06-270">dotnet nuget delete</span></span>](dotnet-nuget-delete.md) | <span data-ttu-id="88c06-271">サーバーからパッケージを削除または一覧から削除します。</span><span class="sxs-lookup"><span data-stu-id="88c06-271">Deletes or unlists a package from the server.</span></span>
[<span data-ttu-id="88c06-272">dotnet nuget locals</span><span class="sxs-lookup"><span data-stu-id="88c06-272">dotnet nuget locals</span></span>](dotnet-nuget-locals.md) | <span data-ttu-id="88c06-273">HTTP 要求キャッシュ、一時的なキャッシュ、コンピューター全体のグローバル パッケージ フォルダーなどのローカルの NuGet リソースをクリアまたは一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="88c06-273">Clears or lists local NuGet resources such as http-request cache, temporary cache, or machine-wide global packages folder.</span></span>
[<span data-ttu-id="88c06-274">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="88c06-274">dotnet nuget push</span></span>](dotnet-nuget-push.md) | <span data-ttu-id="88c06-275">パッケージをサーバーにプッシュして発行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-275">Pushes a package to the server and publishes it.</span></span>

### <a name="global-tools-commands"></a><span data-ttu-id="88c06-276">グローバル ツール コマンド</span><span class="sxs-lookup"><span data-stu-id="88c06-276">Global Tools commands</span></span>

<span data-ttu-id="88c06-277">[.NET Core グローバル ツール](global-tools.md)は .NET Core SDK 2.1.300 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="88c06-277">[.NET Core Global Tools](global-tools.md) are available starting with .NET Core SDK 2.1.300:</span></span>

<span data-ttu-id="88c06-278">コマンド</span><span class="sxs-lookup"><span data-stu-id="88c06-278">Command</span></span> | <span data-ttu-id="88c06-279">関数</span><span class="sxs-lookup"><span data-stu-id="88c06-279">Function</span></span>
--- | ---
[<span data-ttu-id="88c06-280">dotnet tool install</span><span class="sxs-lookup"><span data-stu-id="88c06-280">dotnet tool install</span></span>](dotnet-tool-install.md) | <span data-ttu-id="88c06-281">グローバル ツールをマシンにインストールします。</span><span class="sxs-lookup"><span data-stu-id="88c06-281">Installs a Global Tool on your machine.</span></span>
[<span data-ttu-id="88c06-282">dotnet tool list</span><span class="sxs-lookup"><span data-stu-id="88c06-282">dotnet tool list</span></span>](dotnet-tool-list.md) | <span data-ttu-id="88c06-283">マシン上の既定のディレクトリまたは指定したパスに現在インストールされているすべてのグローバル ツールを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="88c06-283">Lists all Global Tools currently installed in the default directory on your machine or in the specified path.</span></span>
[<span data-ttu-id="88c06-284">dotnet tool uninstall</span><span class="sxs-lookup"><span data-stu-id="88c06-284">dotnet tool uninstall</span></span>](dotnet-tool-uninstall.md) | <span data-ttu-id="88c06-285">グローバル ツールをマシンからアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="88c06-285">Uninstalls a Global Tool from your machine.</span></span>
[<span data-ttu-id="88c06-286">dotnet tool update</span><span class="sxs-lookup"><span data-stu-id="88c06-286">dotnet tool update</span></span>](dotnet-tool-update.md) | <span data-ttu-id="88c06-287">マシン上のグローバル ツールを更新します。</span><span class="sxs-lookup"><span data-stu-id="88c06-287">Updates a Global Tool on your machine.</span></span>

### <a name="additional-tools"></a><span data-ttu-id="88c06-288">その他のツール</span><span class="sxs-lookup"><span data-stu-id="88c06-288">Additional tools</span></span>

<span data-ttu-id="88c06-289">.NET Core SDK 2.1.300 以降では、`DotnetCliToolReference` を使用してプロジェクト単位でのみ入手可能であった複数のツールを .NET Core SDK の一部として入手できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="88c06-289">Starting with .NET Core SDK 2.1.300, a number of tools that were available only on a per project basis using `DotnetCliToolReference` are now available as part of the .NET Core SDK.</span></span> <span data-ttu-id="88c06-290">これらのツールを次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="88c06-290">These tools are listed in the following table:</span></span>

| <span data-ttu-id="88c06-291">ツール</span><span class="sxs-lookup"><span data-stu-id="88c06-291">Tool</span></span>                                              | <span data-ttu-id="88c06-292">関数</span><span class="sxs-lookup"><span data-stu-id="88c06-292">Function</span></span>                                                     |
| ------------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="88c06-293">dev-certs</span><span class="sxs-lookup"><span data-stu-id="88c06-293">dev-certs</span></span>                                         | <span data-ttu-id="88c06-294">開発証明書を作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="88c06-294">Creates and manages development certificates.</span></span>                |
| [<span data-ttu-id="88c06-295">ef</span><span class="sxs-lookup"><span data-stu-id="88c06-295">ef</span></span>](/ef/core/miscellaneous/cli/dotnet)           | <span data-ttu-id="88c06-296">Entity Framework Core コマンドライン ツールです。</span><span class="sxs-lookup"><span data-stu-id="88c06-296">Entity Framework Core command-line tools.</span></span>                    |
| <span data-ttu-id="88c06-297">sql-cache</span><span class="sxs-lookup"><span data-stu-id="88c06-297">sql-cache</span></span>                                         | <span data-ttu-id="88c06-298">SQL Server キャッシュ コマンドライン ツールです。</span><span class="sxs-lookup"><span data-stu-id="88c06-298">SQL Server cache command-line tools.</span></span>                         |
| [<span data-ttu-id="88c06-299">user-secrets</span><span class="sxs-lookup"><span data-stu-id="88c06-299">user-secrets</span></span>](/aspnet/core/security/app-secrets) | <span data-ttu-id="88c06-300">開発ユーザーのシークレットを管理します。</span><span class="sxs-lookup"><span data-stu-id="88c06-300">Manages development user secrets.</span></span>                            |
| [<span data-ttu-id="88c06-301">watch</span><span class="sxs-lookup"><span data-stu-id="88c06-301">watch</span></span>](/aspnet/core/tutorials/dotnet-watch)      | <span data-ttu-id="88c06-302">ファイルが変化するとコマンドを実行するファイル ウォッチャーを起動します。</span><span class="sxs-lookup"><span data-stu-id="88c06-302">Starts a file watcher that runs a command when files change.</span></span> |

<span data-ttu-id="88c06-303">各ツールの詳細については、`dotnet <tool-name> --help` と入力してください。</span><span class="sxs-lookup"><span data-stu-id="88c06-303">For more information about each tool, type `dotnet <tool-name> --help`.</span></span>

## <a name="examples"></a><span data-ttu-id="88c06-304">使用例</span><span class="sxs-lookup"><span data-stu-id="88c06-304">Examples</span></span>

<span data-ttu-id="88c06-305">新しい .NET Core コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="88c06-305">Creates a new .NET Core console application:</span></span>

`dotnet new console`

<span data-ttu-id="88c06-306">指定されたアプリケーションの依存関係を復元します。</span><span class="sxs-lookup"><span data-stu-id="88c06-306">Restore dependencies for a given application:</span></span>

`dotnet restore`

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

<span data-ttu-id="88c06-307">指定されたディレクトリにプロジェクトとその依存関係をビルドします。</span><span class="sxs-lookup"><span data-stu-id="88c06-307">Build a project and its dependencies in a given directory:</span></span>

`dotnet build`

<span data-ttu-id="88c06-308">`myapp.dll` など、アプリケーション DLL を実行します。</span><span class="sxs-lookup"><span data-stu-id="88c06-308">Run an application DLL, such as `myapp.dll`:</span></span>

`dotnet myapp.dll`

## <a name="environment-variables"></a><span data-ttu-id="88c06-309">環境変数</span><span class="sxs-lookup"><span data-stu-id="88c06-309">Environment variables</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="88c06-310">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="88c06-310">.NET Core 2.1</span></span>](#tab/netcore21)

`DOTNET_PACKAGES`

<span data-ttu-id="88c06-311">プライマリ パッケージのキャッシュです。</span><span class="sxs-lookup"><span data-stu-id="88c06-311">The primary package cache.</span></span> <span data-ttu-id="88c06-312">設定されていない場合は、既定で `$HOME/.nuget/packages` (Unix の場合) または `%HOME%\NuGet\Packages` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="88c06-312">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="88c06-313">ランタイムの読み込み時に共有ホストで使用するサービス インデックスの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="88c06-313">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="88c06-314">.NET Core ツールの使用に関するデータを収集し、Microsoft に送信するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="88c06-314">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="88c06-315">`true` に設定するとテレメトリ機能が無効になります (指定できる値は `true`、`1`、または `yes` です)。</span><span class="sxs-lookup"><span data-stu-id="88c06-315">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="88c06-316">それ以外の場合は `false` に設定します。この場合、テレメトリ機能が有効になります (指定できる値は `false`、`0`、または `no` です)。</span><span class="sxs-lookup"><span data-stu-id="88c06-316">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="88c06-317">設定されていない場合、既定で `false` になり、テレメトリ機能はアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="88c06-317">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="88c06-318">.NET Core ランタイム、共有フレームワーク、または SDK がグローバルな場所から解決されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="88c06-318">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="88c06-319">設定されていない場合は、既定で `true` になります。</span><span class="sxs-lookup"><span data-stu-id="88c06-319">If not set, it defaults to `true`.</span></span> <span data-ttu-id="88c06-320">`false` に設定すると、グローバルな場所から解決されず、.NET Core インストールが分離されます (値 `0` または `false` が受け入れられます)。</span><span class="sxs-lookup"><span data-stu-id="88c06-320">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="88c06-321">複数レベルのルックアップの詳細については、「[Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md)」 (複数レベルの SharedFX ルックアップ) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88c06-321">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

`DOTNET_ROLL_FORWARD_ON_NO_CANDIDATE_FX`

<span data-ttu-id="88c06-322">`0` に設定されている場合、マイナー バージョンのロールフォワードを無効にします。</span><span class="sxs-lookup"><span data-stu-id="88c06-322">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="88c06-323">詳細については、「[Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward)」(ロールフォワード) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88c06-323">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="88c06-324">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="88c06-324">.NET Core 2.0</span></span>](#tab/netcore20)

`DOTNET_PACKAGES`

<span data-ttu-id="88c06-325">プライマリ パッケージのキャッシュです。</span><span class="sxs-lookup"><span data-stu-id="88c06-325">The primary package cache.</span></span> <span data-ttu-id="88c06-326">設定されていない場合は、既定で `$HOME/.nuget/packages` (Unix の場合) または `%HOME%\NuGet\Packages` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="88c06-326">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="88c06-327">ランタイムの読み込み時に共有ホストで使用するサービス インデックスの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="88c06-327">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="88c06-328">.NET Core ツールの使用に関するデータを収集し、Microsoft に送信するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="88c06-328">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="88c06-329">`true` に設定するとテレメトリ機能が無効になります (指定できる値は `true`、`1`、または `yes` です)。</span><span class="sxs-lookup"><span data-stu-id="88c06-329">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="88c06-330">それ以外の場合は `false` に設定します。この場合、テレメトリ機能が有効になります (指定できる値は `false`、`0`、または `no` です)。</span><span class="sxs-lookup"><span data-stu-id="88c06-330">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="88c06-331">設定されていない場合、既定で `false` になり、テレメトリ機能はアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="88c06-331">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="88c06-332">.NET Core ランタイム、共有フレームワーク、または SDK がグローバルな場所から解決されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="88c06-332">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="88c06-333">設定されていない場合は、既定で `true` になります。</span><span class="sxs-lookup"><span data-stu-id="88c06-333">If not set, it defaults to `true`.</span></span> <span data-ttu-id="88c06-334">`false` に設定すると、グローバルな場所から解決されず、.NET Core インストールが分離されます (値 `0` または `false` が受け入れられます)。</span><span class="sxs-lookup"><span data-stu-id="88c06-334">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="88c06-335">複数レベルのルックアップの詳細については、「[Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md)」 (複数レベルの SharedFX ルックアップ) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88c06-335">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="88c06-336">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="88c06-336">.NET Core 1.x</span></span>](#tab/netcore1x)

`DOTNET_PACKAGES`

<span data-ttu-id="88c06-337">プライマリ パッケージのキャッシュです。</span><span class="sxs-lookup"><span data-stu-id="88c06-337">The primary package cache.</span></span> <span data-ttu-id="88c06-338">設定されていない場合は、既定で `$HOME/.nuget/packages` (Unix の場合) または `%HOME%\NuGet\Packages` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="88c06-338">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="88c06-339">ランタイムの読み込み時に共有ホストで使用するサービス インデックスの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="88c06-339">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="88c06-340">.NET Core ツールの使用に関するデータを収集し、Microsoft に送信するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="88c06-340">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="88c06-341">`true` に設定するとテレメトリ機能が無効になります (指定できる値は `true`、`1`、または `yes` です)。</span><span class="sxs-lookup"><span data-stu-id="88c06-341">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="88c06-342">それ以外の場合は `false` に設定します。この場合、テレメトリ機能が有効になります (指定できる値は `false`、`0`、または `no` です)。</span><span class="sxs-lookup"><span data-stu-id="88c06-342">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="88c06-343">設定されていない場合、既定で `false` になり、テレメトリ機能はアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="88c06-343">If not set, the default is `false` and the telemetry feature is active.</span></span>

---
