---
title: dotnet コマンド - .NET Core CLI
description: dotnet コマンド (.NET Core CLI ツールの一般的なドライバー) とその使用法について説明します。
author: mairaw
ms.author: mairaw
ms.date: 06/04/2018
ms.openlocfilehash: 53e8f8bab1cbaabaa7926aa68197c18843b0b637
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44079817"
---
# <a name="dotnet-command"></a><span data-ttu-id="7e2f1-103">dotnet コマンド</span><span class="sxs-lookup"><span data-stu-id="7e2f1-103">dotnet command</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="7e2f1-104">name</span><span class="sxs-lookup"><span data-stu-id="7e2f1-104">Name</span></span>

<span data-ttu-id="7e2f1-105">`dotnet` - .NET のソース コードとバイナリを管理するためのツール。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-105">`dotnet` - A tool for managing .NET source code and binaries.</span></span>

## <a name="synopsis"></a><span data-ttu-id="7e2f1-106">構文</span><span class="sxs-lookup"><span data-stu-id="7e2f1-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="7e2f1-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="7e2f1-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [--list-runtimes] [--list-sdks] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="7e2f1-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="7e2f1-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics]
    [--fx-version] [-h|--help] [--info] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="7e2f1-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="7e2f1-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet [command] [arguments] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [-v|--verbosity] [--version]
```
---

## <a name="description"></a><span data-ttu-id="7e2f1-110">説明</span><span class="sxs-lookup"><span data-stu-id="7e2f1-110">Description</span></span>

<span data-ttu-id="7e2f1-111">`dotnet` は .NET のソース コードとバイナリを管理するためのツールです。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-111">`dotnet` is a tool for managing .NET source code and binaries.</span></span> <span data-ttu-id="7e2f1-112">[`dotnet build`](dotnet-build.md) や [`dotnet run`](dotnet-run.md) のような特定のタスクを実行するコマンドを公開します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-112">It exposes commands that perform specific tasks, such as [`dotnet build`](dotnet-build.md) and [`dotnet run`](dotnet-run.md).</span></span> <span data-ttu-id="7e2f1-113">各コマンドによって、それ自体の引数が定義されます。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-113">Each command defines its own arguments.</span></span> <span data-ttu-id="7e2f1-114">各コマンドの後ろに `--help` と入力すると、短いヘルプ ドキュメントにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-114">Type `--help` after each command to access brief help documentation.</span></span>

<span data-ttu-id="7e2f1-115">`dotnet` は、`dotnet myapp.dll` など、アプリケーション DLL を指定することで、アプリケーションを実行するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-115">`dotnet` can be used to run applications, by specifying an application DLL, such as `dotnet myapp.dll`.</span></span> <span data-ttu-id="7e2f1-116">展開オプションについては、「[.NET Core アプリケーションの展開](../deploying/index.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-116">See [.NET Core application deployment](../deploying/index.md) for to learn about deployment options.</span></span>

## <a name="options"></a><span data-ttu-id="7e2f1-117">オプション</span><span class="sxs-lookup"><span data-stu-id="7e2f1-117">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="7e2f1-118">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="7e2f1-118">.NET Core 2.1</span></span>](#tab/netcore21)

`--additional-deps <PATH>`

<span data-ttu-id="7e2f1-119">追加の *deps.json* ファイルへのパスです。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-119">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="7e2f1-120">プローブ ポリシーとプローブするアセンブリを含むパスです。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-120">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="7e2f1-121">診断出力を有効にします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-121">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="7e2f1-122">アプリケーションを実行するために使用する .NET Core ランタイムのバージョン。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-122">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="7e2f1-123">`dotnet build --help` など、特定のコマンドのドキュメントを出力します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-123">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="7e2f1-124">`dotnet --help` では、使用できるコマンドの一覧が出力されます。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-124">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="7e2f1-125">現在のオペレーティング システムや .NET Core バージョンのコミット SHA など、.NET Core インストールとコンピューター環境に関する詳細を出力します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-125">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--list-runtimes`

<span data-ttu-id="7e2f1-126">インストールされている .NET Core ランタイムを表示します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-126">Displays the installed .NET Core runtimes.</span></span>

`--list-sdks`

<span data-ttu-id="7e2f1-127">インストールされている .NET Core SDK を表示します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-127">Displays the installed .NET Core SDKs.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="7e2f1-128">`0` に設定されている場合、マイナー バージョンのロールフォワードを無効にします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-128">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="7e2f1-129">詳細については、「[Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward)」(ロールフォワード) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-129">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="7e2f1-130">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-130">Sets the verbosity level of the command.</span></span> <span data-ttu-id="7e2f1-131">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-131">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="7e2f1-132">一部のコマンドではサポートされていません。このオプションが使用可能かどうかを判断するには、対象のコマンドのページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-132">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="7e2f1-133">使用中の .NET Core SDK のバージョンを印刷します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-133">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="7e2f1-134">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="7e2f1-134">.NET Core 2.0</span></span>](#tab/netcore20)

`--additional-deps <PATH>`

<span data-ttu-id="7e2f1-135">追加の *deps.json* ファイルへのパスです。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-135">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="7e2f1-136">プローブ ポリシーとプローブするアセンブリを含むパスです。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-136">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="7e2f1-137">診断出力を有効にします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-137">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="7e2f1-138">アプリケーションを実行するために使用する .NET Core ランタイムのバージョン。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-138">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="7e2f1-139">`dotnet build --help` など、特定のコマンドのドキュメントを出力します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-139">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="7e2f1-140">`dotnet --help` では、使用できるコマンドの一覧が出力されます。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-140">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="7e2f1-141">現在のオペレーティング システムや .NET Core バージョンのコミット SHA など、.NET Core インストールとコンピューター環境に関する詳細を出力します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-141">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="7e2f1-142">`0` に設定されている場合、マイナー バージョンのロールフォワードを無効にします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-142">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="7e2f1-143">詳細については、「[Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward)」(ロールフォワード) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-143">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="7e2f1-144">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-144">Sets the verbosity level of the command.</span></span> <span data-ttu-id="7e2f1-145">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-145">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="7e2f1-146">一部のコマンドではサポートされていません。このオプションが使用可能かどうかを判断するには、対象のコマンドのページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-146">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="7e2f1-147">使用中の .NET Core SDK のバージョンを印刷します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-147">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="7e2f1-148">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="7e2f1-148">.NET Core 1.x</span></span>](#tab/netcore1x)

`--additionalprobingpath <PATH>`

<span data-ttu-id="7e2f1-149">プローブ ポリシーとプローブするアセンブリを含むパスです。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-149">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="7e2f1-150">診断出力を有効にします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-150">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="7e2f1-151">アプリケーションを実行するために使用する .NET Core ランタイムのバージョン。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-151">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="7e2f1-152">`dotnet build --help` など、特定のコマンドのドキュメントを出力します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-152">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="7e2f1-153">`dotnet --help` では、使用できるコマンドの一覧が出力されます。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-153">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="7e2f1-154">現在のオペレーティング システムや .NET Core バージョンのコミット SHA など、.NET Core インストールとコンピューター環境に関する詳細を出力します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-154">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="7e2f1-155">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-155">Sets the verbosity level of the command.</span></span> <span data-ttu-id="7e2f1-156">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-156">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="7e2f1-157">一部のコマンドではサポートされていません。このオプションが使用可能かどうかを判断するには、対象のコマンドのページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-157">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="7e2f1-158">使用中の .NET Core SDK のバージョンを印刷します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-158">Prints out the version of the .NET Core SDK in use.</span></span>

---

## <a name="dotnet-commands"></a><span data-ttu-id="7e2f1-159">dotnet コマンド</span><span class="sxs-lookup"><span data-stu-id="7e2f1-159">dotnet commands</span></span>

### <a name="general"></a><span data-ttu-id="7e2f1-160">全般</span><span class="sxs-lookup"><span data-stu-id="7e2f1-160">General</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="7e2f1-161">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="7e2f1-161">.NET Core 2.1</span></span>](#tab/netcore21)

| <span data-ttu-id="7e2f1-162">コマンド</span><span class="sxs-lookup"><span data-stu-id="7e2f1-162">Command</span></span>                                       | <span data-ttu-id="7e2f1-163">関数</span><span class="sxs-lookup"><span data-stu-id="7e2f1-163">Function</span></span>                                                            |
| --------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="7e2f1-164">dotnet build</span><span class="sxs-lookup"><span data-stu-id="7e2f1-164">dotnet build</span></span>](dotnet-build.md)               | <span data-ttu-id="7e2f1-165">.NET Core アプリケーションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-165">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="7e2f1-166">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="7e2f1-166">dotnet build-server</span></span>](dotnet-build-server.md) | <span data-ttu-id="7e2f1-167">ビルドによって起動されたサーバーとやり取りします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-167">Interacts with servers started by a build.</span></span>                          |
| [<span data-ttu-id="7e2f1-168">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="7e2f1-168">dotnet clean</span></span>](dotnet-clean.md)               | <span data-ttu-id="7e2f1-169">クリーン ビルド出力です。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-169">Clean build outputs.</span></span>                                                |
| [<span data-ttu-id="7e2f1-170">dotnet help</span><span class="sxs-lookup"><span data-stu-id="7e2f1-170">dotnet help</span></span>](dotnet-help.md)                 | <span data-ttu-id="7e2f1-171">コマンドのより詳細なドキュメントをオンラインで表示します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-171">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="7e2f1-172">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="7e2f1-172">dotnet migrate</span></span>](dotnet-migrate.md)           | <span data-ttu-id="7e2f1-173">有効な Preview 2 プロジェクトを .NET Core SDK 1.0 プロジェクトに移行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-173">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="7e2f1-174">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="7e2f1-174">dotnet msbuild</span></span>](dotnet-msbuild.md)           | <span data-ttu-id="7e2f1-175">MSBuild コマンド ラインへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-175">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="7e2f1-176">dotnet new</span><span class="sxs-lookup"><span data-stu-id="7e2f1-176">dotnet new</span></span>](dotnet-new.md)                   | <span data-ttu-id="7e2f1-177">指定されたテンプレートの C# または F# プロジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-177">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="7e2f1-178">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="7e2f1-178">dotnet pack</span></span>](dotnet-pack.md)                 | <span data-ttu-id="7e2f1-179">コードの NuGet パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-179">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="7e2f1-180">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="7e2f1-180">dotnet publish</span></span>](dotnet-publish.md)           | <span data-ttu-id="7e2f1-181">.NET Framework に依存するアプリケーションまたは自己完結型アプリケーションを発行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-181">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="7e2f1-182">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="7e2f1-182">dotnet restore</span></span>](dotnet-restore.md)           | <span data-ttu-id="7e2f1-183">指定されたアプリケーションの依存関係を復元します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-183">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="7e2f1-184">dotnet run</span><span class="sxs-lookup"><span data-stu-id="7e2f1-184">dotnet run</span></span>](dotnet-run.md)                   | <span data-ttu-id="7e2f1-185">ソースからアプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-185">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="7e2f1-186">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="7e2f1-186">dotnet sln</span></span>](dotnet-sln.md)                   | <span data-ttu-id="7e2f1-187">ソリューション ファイルのプロジェクトを追加、削除、一覧表示するオプション。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-187">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="7e2f1-188">dotnet store</span><span class="sxs-lookup"><span data-stu-id="7e2f1-188">dotnet store</span></span>](dotnet-store.md)               | <span data-ttu-id="7e2f1-189">ランタイム パッケージ ストアにアセンブリを格納します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-189">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="7e2f1-190">dotnet test</span><span class="sxs-lookup"><span data-stu-id="7e2f1-190">dotnet test</span></span>](dotnet-test.md)                 | <span data-ttu-id="7e2f1-191">テスト ランナーを使用してテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-191">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="7e2f1-192">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="7e2f1-192">.NET Core 2.0</span></span>](#tab/netcore20)

| <span data-ttu-id="7e2f1-193">コマンド</span><span class="sxs-lookup"><span data-stu-id="7e2f1-193">Command</span></span>                             | <span data-ttu-id="7e2f1-194">関数</span><span class="sxs-lookup"><span data-stu-id="7e2f1-194">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="7e2f1-195">dotnet build</span><span class="sxs-lookup"><span data-stu-id="7e2f1-195">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="7e2f1-196">.NET Core アプリケーションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-196">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="7e2f1-197">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="7e2f1-197">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="7e2f1-198">クリーン ビルド出力です。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-198">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="7e2f1-199">dotnet help</span><span class="sxs-lookup"><span data-stu-id="7e2f1-199">dotnet help</span></span>](dotnet-help.md)       | <span data-ttu-id="7e2f1-200">コマンドのより詳細なドキュメントをオンラインで表示します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-200">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="7e2f1-201">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="7e2f1-201">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="7e2f1-202">有効な Preview 2 プロジェクトを .NET Core SDK 1.0 プロジェクトに移行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-202">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="7e2f1-203">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="7e2f1-203">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="7e2f1-204">MSBuild コマンド ラインへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-204">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="7e2f1-205">dotnet new</span><span class="sxs-lookup"><span data-stu-id="7e2f1-205">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="7e2f1-206">指定されたテンプレートの C# または F# プロジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-206">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="7e2f1-207">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="7e2f1-207">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="7e2f1-208">コードの NuGet パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-208">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="7e2f1-209">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="7e2f1-209">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="7e2f1-210">.NET Framework に依存するアプリケーションまたは自己完結型アプリケーションを発行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-210">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="7e2f1-211">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="7e2f1-211">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="7e2f1-212">指定されたアプリケーションの依存関係を復元します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-212">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="7e2f1-213">dotnet run</span><span class="sxs-lookup"><span data-stu-id="7e2f1-213">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="7e2f1-214">ソースからアプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-214">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="7e2f1-215">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="7e2f1-215">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="7e2f1-216">ソリューション ファイルのプロジェクトを追加、削除、一覧表示するオプション。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-216">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="7e2f1-217">dotnet store</span><span class="sxs-lookup"><span data-stu-id="7e2f1-217">dotnet store</span></span>](dotnet-store.md)     | <span data-ttu-id="7e2f1-218">ランタイム パッケージ ストアにアセンブリを格納します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-218">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="7e2f1-219">dotnet test</span><span class="sxs-lookup"><span data-stu-id="7e2f1-219">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="7e2f1-220">テスト ランナーを使用してテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-220">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="7e2f1-221">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="7e2f1-221">.NET Core 1.x</span></span>](#tab/netcore1x)

| <span data-ttu-id="7e2f1-222">コマンド</span><span class="sxs-lookup"><span data-stu-id="7e2f1-222">Command</span></span>                             | <span data-ttu-id="7e2f1-223">関数</span><span class="sxs-lookup"><span data-stu-id="7e2f1-223">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="7e2f1-224">dotnet build</span><span class="sxs-lookup"><span data-stu-id="7e2f1-224">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="7e2f1-225">.NET Core アプリケーションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-225">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="7e2f1-226">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="7e2f1-226">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="7e2f1-227">クリーン ビルド出力です。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-227">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="7e2f1-228">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="7e2f1-228">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="7e2f1-229">有効な Preview 2 プロジェクトを .NET Core SDK 1.0 プロジェクトに移行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-229">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="7e2f1-230">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="7e2f1-230">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="7e2f1-231">MSBuild コマンド ラインへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-231">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="7e2f1-232">dotnet new</span><span class="sxs-lookup"><span data-stu-id="7e2f1-232">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="7e2f1-233">指定されたテンプレートの C# または F# プロジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-233">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="7e2f1-234">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="7e2f1-234">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="7e2f1-235">コードの NuGet パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-235">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="7e2f1-236">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="7e2f1-236">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="7e2f1-237">.NET Framework に依存するアプリケーションまたは自己完結型アプリケーションを発行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-237">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="7e2f1-238">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="7e2f1-238">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="7e2f1-239">指定されたアプリケーションの依存関係を復元します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-239">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="7e2f1-240">dotnet run</span><span class="sxs-lookup"><span data-stu-id="7e2f1-240">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="7e2f1-241">ソースからアプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-241">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="7e2f1-242">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="7e2f1-242">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="7e2f1-243">ソリューション ファイルのプロジェクトを追加、削除、一覧表示するオプション。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-243">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="7e2f1-244">dotnet test</span><span class="sxs-lookup"><span data-stu-id="7e2f1-244">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="7e2f1-245">テスト ランナーを使用してテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-245">Runs tests using a test runner.</span></span>                                     |

---

### <a name="project-references"></a><span data-ttu-id="7e2f1-246">プロジェクト参照</span><span class="sxs-lookup"><span data-stu-id="7e2f1-246">Project references</span></span>

<span data-ttu-id="7e2f1-247">コマンド</span><span class="sxs-lookup"><span data-stu-id="7e2f1-247">Command</span></span> | <span data-ttu-id="7e2f1-248">関数</span><span class="sxs-lookup"><span data-stu-id="7e2f1-248">Function</span></span>
--- | ---
[<span data-ttu-id="7e2f1-249">dotnet add reference</span><span class="sxs-lookup"><span data-stu-id="7e2f1-249">dotnet add reference</span></span>](dotnet-add-reference.md) | <span data-ttu-id="7e2f1-250">プロジェクト参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-250">Adds a project reference.</span></span>
[<span data-ttu-id="7e2f1-251">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="7e2f1-251">dotnet list reference</span></span>](dotnet-list-reference.md) | <span data-ttu-id="7e2f1-252">プロジェクト参照をリストします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-252">Lists project references.</span></span>
[<span data-ttu-id="7e2f1-253">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="7e2f1-253">dotnet remove reference</span></span>](dotnet-remove-reference.md) | <span data-ttu-id="7e2f1-254">プロジェクト参照を削除します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-254">Removes a project reference.</span></span>

### <a name="nuget-packages"></a><span data-ttu-id="7e2f1-255">NuGet パッケージ</span><span class="sxs-lookup"><span data-stu-id="7e2f1-255">NuGet packages</span></span>

<span data-ttu-id="7e2f1-256">コマンド</span><span class="sxs-lookup"><span data-stu-id="7e2f1-256">Command</span></span> | <span data-ttu-id="7e2f1-257">関数</span><span class="sxs-lookup"><span data-stu-id="7e2f1-257">Function</span></span>
--- | ---
[<span data-ttu-id="7e2f1-258">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="7e2f1-258">dotnet add package</span></span>](dotnet-add-package.md) | <span data-ttu-id="7e2f1-259">NuGet パッケージを追加します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-259">Adds a NuGet package.</span></span>
[<span data-ttu-id="7e2f1-260">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="7e2f1-260">dotnet remove package</span></span>](dotnet-remove-package.md) | <span data-ttu-id="7e2f1-261">NuGet パッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-261">Removes a NuGet package.</span></span>

### <a name="nuget-commands"></a><span data-ttu-id="7e2f1-262">NuGet コマンド</span><span class="sxs-lookup"><span data-stu-id="7e2f1-262">NuGet commands</span></span>

<span data-ttu-id="7e2f1-263">コマンド</span><span class="sxs-lookup"><span data-stu-id="7e2f1-263">Command</span></span> | <span data-ttu-id="7e2f1-264">関数</span><span class="sxs-lookup"><span data-stu-id="7e2f1-264">Function</span></span>
--- | ---
[<span data-ttu-id="7e2f1-265">dotnet nuget delete</span><span class="sxs-lookup"><span data-stu-id="7e2f1-265">dotnet nuget delete</span></span>](dotnet-nuget-delete.md) | <span data-ttu-id="7e2f1-266">サーバーからパッケージを削除または一覧から削除します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-266">Deletes or unlists a package from the server.</span></span>
[<span data-ttu-id="7e2f1-267">dotnet nuget locals</span><span class="sxs-lookup"><span data-stu-id="7e2f1-267">dotnet nuget locals</span></span>](dotnet-nuget-locals.md) | <span data-ttu-id="7e2f1-268">HTTP 要求キャッシュ、一時的なキャッシュ、コンピューター全体のグローバル パッケージ フォルダーなどのローカルの NuGet リソースをクリアまたは一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-268">Clears or lists local NuGet resources such as http-request cache, temporary cache, or machine-wide global packages folder.</span></span>
[<span data-ttu-id="7e2f1-269">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="7e2f1-269">dotnet nuget push</span></span>](dotnet-nuget-push.md) | <span data-ttu-id="7e2f1-270">パッケージをサーバーにプッシュして発行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-270">Pushes a package to the server and publishes it.</span></span>

### <a name="global-tools-commands"></a><span data-ttu-id="7e2f1-271">グローバル ツール コマンド</span><span class="sxs-lookup"><span data-stu-id="7e2f1-271">Global Tools commands</span></span>

<span data-ttu-id="7e2f1-272">[.NET Core グローバル ツール](global-tools.md)は .NET Core SDK 2.1.300 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-272">[.NET Core Global Tools](global-tools.md) are available starting with .NET Core SDK 2.1.300:</span></span>

<span data-ttu-id="7e2f1-273">コマンド</span><span class="sxs-lookup"><span data-stu-id="7e2f1-273">Command</span></span> | <span data-ttu-id="7e2f1-274">関数</span><span class="sxs-lookup"><span data-stu-id="7e2f1-274">Function</span></span>
--- | ---
[<span data-ttu-id="7e2f1-275">dotnet tool install</span><span class="sxs-lookup"><span data-stu-id="7e2f1-275">dotnet tool install</span></span>](dotnet-tool-install.md) | <span data-ttu-id="7e2f1-276">グローバル ツールをマシンにインストールします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-276">Installs a Global Tool on your machine.</span></span>
[<span data-ttu-id="7e2f1-277">dotnet tool list</span><span class="sxs-lookup"><span data-stu-id="7e2f1-277">dotnet tool list</span></span>](dotnet-tool-list.md) | <span data-ttu-id="7e2f1-278">マシン上の既定のディレクトリまたは指定したパスに現在インストールされているすべてのグローバル ツールを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-278">Lists all Global Tools currently installed in the default directory on your machine or in the specified path.</span></span>
[<span data-ttu-id="7e2f1-279">dotnet tool uninstall</span><span class="sxs-lookup"><span data-stu-id="7e2f1-279">dotnet tool uninstall</span></span>](dotnet-tool-uninstall.md) | <span data-ttu-id="7e2f1-280">グローバル ツールをマシンからアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-280">Uninstalls a Global Tool from your machine.</span></span>
[<span data-ttu-id="7e2f1-281">dotnet tool update</span><span class="sxs-lookup"><span data-stu-id="7e2f1-281">dotnet tool update</span></span>](dotnet-tool-update.md) | <span data-ttu-id="7e2f1-282">マシン上のグローバル ツールを更新します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-282">Updates a Global Tool on your machine.</span></span>

### <a name="additional-tools"></a><span data-ttu-id="7e2f1-283">その他のツール</span><span class="sxs-lookup"><span data-stu-id="7e2f1-283">Additional tools</span></span>

<span data-ttu-id="7e2f1-284">.NET Core SDK 2.1.300 以降では、`DotnetCliToolReference` を使用してプロジェクト単位でのみ入手可能であった複数のツールを .NET Core SDK の一部として入手できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-284">Starting with .NET Core SDK 2.1.300, a number of tools that were available only on a per project basis using `DotnetCliToolReference` are now available as part of the .NET Core SDK.</span></span> <span data-ttu-id="7e2f1-285">これらのツールを次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-285">These tools are listed in the following table:</span></span>

| <span data-ttu-id="7e2f1-286">ツール</span><span class="sxs-lookup"><span data-stu-id="7e2f1-286">Tool</span></span>                                              | <span data-ttu-id="7e2f1-287">関数</span><span class="sxs-lookup"><span data-stu-id="7e2f1-287">Function</span></span>                                                     |
| ------------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="7e2f1-288">dev-certs</span><span class="sxs-lookup"><span data-stu-id="7e2f1-288">dev-certs</span></span>                                         | <span data-ttu-id="7e2f1-289">開発証明書を作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-289">Creates and manages development certificates.</span></span>                |
| [<span data-ttu-id="7e2f1-290">ef</span><span class="sxs-lookup"><span data-stu-id="7e2f1-290">ef</span></span>](/ef/core/miscellaneous/cli/dotnet)           | <span data-ttu-id="7e2f1-291">Entity Framework Core コマンドライン ツールです。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-291">Entity Framework Core command-line tools.</span></span>                    |
| <span data-ttu-id="7e2f1-292">sql-cache</span><span class="sxs-lookup"><span data-stu-id="7e2f1-292">sql-cache</span></span>                                         | <span data-ttu-id="7e2f1-293">SQL Server キャッシュ コマンドライン ツールです。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-293">SQL Server cache command-line tools.</span></span>                         |
| [<span data-ttu-id="7e2f1-294">user-secrets</span><span class="sxs-lookup"><span data-stu-id="7e2f1-294">user-secrets</span></span>](/aspnet/core/security/app-secrets) | <span data-ttu-id="7e2f1-295">開発ユーザーのシークレットを管理します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-295">Manages development user secrets.</span></span>                            |
| [<span data-ttu-id="7e2f1-296">watch</span><span class="sxs-lookup"><span data-stu-id="7e2f1-296">watch</span></span>](/aspnet/core/tutorials/dotnet-watch)      | <span data-ttu-id="7e2f1-297">ファイルが変化するとコマンドを実行するファイル ウォッチャーを起動します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-297">Starts a file watcher that runs a command when files change.</span></span> |

<span data-ttu-id="7e2f1-298">各ツールの詳細については、`dotnet <tool-name> --help` と入力してください。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-298">For more information about each tool, type `dotnet <tool-name> --help`.</span></span>

## <a name="examples"></a><span data-ttu-id="7e2f1-299">使用例</span><span class="sxs-lookup"><span data-stu-id="7e2f1-299">Examples</span></span>

<span data-ttu-id="7e2f1-300">新しい .NET Core コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-300">Creates a new .NET Core console application:</span></span>

`dotnet new console`

<span data-ttu-id="7e2f1-301">指定されたアプリケーションの依存関係を復元します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-301">Restore dependencies for a given application:</span></span>

`dotnet restore`

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

<span data-ttu-id="7e2f1-302">指定されたディレクトリにプロジェクトとその依存関係をビルドします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-302">Build a project and its dependencies in a given directory:</span></span>

`dotnet build`

<span data-ttu-id="7e2f1-303">`myapp.dll` など、アプリケーション DLL を実行します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-303">Run an application DLL, such as `myapp.dll`:</span></span>

`dotnet myapp.dll`

## <a name="environment-variables"></a><span data-ttu-id="7e2f1-304">環境変数</span><span class="sxs-lookup"><span data-stu-id="7e2f1-304">Environment variables</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="7e2f1-305">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="7e2f1-305">.NET Core 2.1</span></span>](#tab/netcore21)

`DOTNET_PACKAGES`

<span data-ttu-id="7e2f1-306">プライマリ パッケージのキャッシュです。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-306">The primary package cache.</span></span> <span data-ttu-id="7e2f1-307">設定されていない場合は、既定で `$HOME/.nuget/packages` (Unix の場合) または `%HOME%\NuGet\Packages` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-307">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="7e2f1-308">ランタイムの読み込み時に共有ホストで使用するサービス インデックスの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-308">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="7e2f1-309">.NET Core ツールの使用に関するデータを収集し、Microsoft に送信するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-309">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="7e2f1-310">`true` に設定するとテレメトリ機能が無効になります (指定できる値は `true`、`1`、または `yes` です)。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-310">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="7e2f1-311">それ以外の場合は `false` に設定します。この場合、テレメトリ機能が有効になります (指定できる値は `false`、`0`、または `no` です)。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-311">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="7e2f1-312">設定されていない場合、既定で `false` になり、テレメトリ機能はアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-312">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="7e2f1-313">.NET Core ランタイム、共有フレームワーク、または SDK がグローバルな場所から解決されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-313">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="7e2f1-314">設定されていない場合は、既定で `true` になります。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-314">If not set, it defaults to `true`.</span></span> <span data-ttu-id="7e2f1-315">`false` に設定すると、グローバルな場所から解決されず、.NET Core インストールが分離されます (値 `0` または `false` が受け入れられます)。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-315">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="7e2f1-316">複数レベルのルックアップの詳細については、「[Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md)」 (複数レベルの SharedFX ルックアップ) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-316">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

`DOTNET_ROLL_FORWARD_ON_NO_CANDIDATE_FX`

<span data-ttu-id="7e2f1-317">`0` に設定されている場合、マイナー バージョンのロールフォワードを無効にします。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-317">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="7e2f1-318">詳細については、「[Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward)」(ロールフォワード) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-318">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="7e2f1-319">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="7e2f1-319">.NET Core 2.0</span></span>](#tab/netcore20)

`DOTNET_PACKAGES`

<span data-ttu-id="7e2f1-320">プライマリ パッケージのキャッシュです。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-320">The primary package cache.</span></span> <span data-ttu-id="7e2f1-321">設定されていない場合は、既定で `$HOME/.nuget/packages` (Unix の場合) または `%HOME%\NuGet\Packages` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-321">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="7e2f1-322">ランタイムの読み込み時に共有ホストで使用するサービス インデックスの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-322">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="7e2f1-323">.NET Core ツールの使用に関するデータを収集し、Microsoft に送信するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-323">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="7e2f1-324">`true` に設定するとテレメトリ機能が無効になります (指定できる値は `true`、`1`、または `yes` です)。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-324">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="7e2f1-325">それ以外の場合は `false` に設定します。この場合、テレメトリ機能が有効になります (指定できる値は `false`、`0`、または `no` です)。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-325">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="7e2f1-326">設定されていない場合、既定で `false` になり、テレメトリ機能はアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-326">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="7e2f1-327">.NET Core ランタイム、共有フレームワーク、または SDK がグローバルな場所から解決されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-327">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="7e2f1-328">設定されていない場合は、既定で `true` になります。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-328">If not set, it defaults to `true`.</span></span> <span data-ttu-id="7e2f1-329">`false` に設定すると、グローバルな場所から解決されず、.NET Core インストールが分離されます (値 `0` または `false` が受け入れられます)。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-329">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="7e2f1-330">複数レベルのルックアップの詳細については、「[Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md)」 (複数レベルの SharedFX ルックアップ) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-330">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="7e2f1-331">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="7e2f1-331">.NET Core 1.x</span></span>](#tab/netcore1x)

`DOTNET_PACKAGES`

<span data-ttu-id="7e2f1-332">プライマリ パッケージのキャッシュです。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-332">The primary package cache.</span></span> <span data-ttu-id="7e2f1-333">設定されていない場合は、既定で `$HOME/.nuget/packages` (Unix の場合) または `%HOME%\NuGet\Packages` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-333">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="7e2f1-334">ランタイムの読み込み時に共有ホストで使用するサービス インデックスの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-334">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="7e2f1-335">.NET Core ツールの使用に関するデータを収集し、Microsoft に送信するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-335">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="7e2f1-336">`true` に設定するとテレメトリ機能が無効になります (指定できる値は `true`、`1`、または `yes` です)。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-336">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="7e2f1-337">それ以外の場合は `false` に設定します。この場合、テレメトリ機能が有効になります (指定できる値は `false`、`0`、または `no` です)。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-337">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="7e2f1-338">設定されていない場合、既定で `false` になり、テレメトリ機能はアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="7e2f1-338">If not set, the default is `false` and the telemetry feature is active.</span></span>

---
