---
title: dotnet test コマンド - .NET Core CLI
description: dotnet test コマンドは、指定されたプロジェクトで単体テストを実行する場合に使用されます。
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: e80ba874ec8d0fbc49858719dc3b9b6e02254c78
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2018
ms.locfileid: "46696457"
---
# <a name="dotnet-test"></a><span data-ttu-id="b4331-103">dotnet test</span><span class="sxs-lookup"><span data-stu-id="b4331-103">dotnet test</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="b4331-104">name</span><span class="sxs-lookup"><span data-stu-id="b4331-104">Name</span></span>

<span data-ttu-id="b4331-105">`dotnet test` - 単体テストを実行するために使用される .NET テスト ドライバー。</span><span class="sxs-lookup"><span data-stu-id="b4331-105">`dotnet test` - .NET test driver used to execute unit tests.</span></span>

## <a name="synopsis"></a><span data-ttu-id="b4331-106">構文</span><span class="sxs-lookup"><span data-stu-id="b4331-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="b4331-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="b4331-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [--blame] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="b4331-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="b4331-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="b4331-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="b4331-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [-d|--diag] [-f|--framework] [--filter] [-l|--logger] [--no-build] [-o|--output] [-s|--settings] [-t|--list-tests]  [-v|--verbosity]
dotnet test [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="b4331-110">説明</span><span class="sxs-lookup"><span data-stu-id="b4331-110">Description</span></span>

<span data-ttu-id="b4331-111">`dotnet test` コマンドは、指定されたプロジェクトで単体テストを実行する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b4331-111">The `dotnet test` command is used to execute unit tests in a given project.</span></span> <span data-ttu-id="b4331-112">`dotnet test` コマンドは、プロジェクト用に指定されたテスト ランナーのコンソール アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="b4331-112">The `dotnet test` command launches the test runner console application specified for a project.</span></span> <span data-ttu-id="b4331-113">テスト ランナーでは、単体テスト フレームワーク (MSTest、NUnit、xUnit など) 用に定義されたテストを実行し、各テストの成功または失敗をレポートします。</span><span class="sxs-lookup"><span data-stu-id="b4331-113">The test runner executes the tests defined for a unit test framework (for example, MSTest, NUnit, or xUnit) and reports the success or failure of each test.</span></span> <span data-ttu-id="b4331-114">すべてのテストが成功した場合、テスト ランナーは 0 の終了コードを返します。それ以外の、いずれかのテストに失敗した場合は、1 を返します。</span><span class="sxs-lookup"><span data-stu-id="b4331-114">If all tests are successful, the test runner returns 0 as an exit code; otherwise if any test fails, it returns 1.</span></span> <span data-ttu-id="b4331-115">テスト ランナーと単体テスト ライブラリは、NuGet パッケージとしてパッケージ化され、プロジェクトの通常の依存関係として復元されます。</span><span class="sxs-lookup"><span data-stu-id="b4331-115">The test runner and the unit test library are packaged as NuGet packages and are restored as ordinary dependencies for the project.</span></span>

<span data-ttu-id="b4331-116">テスト プロジェクトでは、通常の `<PackageReference>` 要素を使用してテスト ランナーを指定します。次のサンプル プロジェクト ファイルのようになります。</span><span class="sxs-lookup"><span data-stu-id="b4331-116">Test projects specify the test runner using an ordinary `<PackageReference>` element, as seen in the following sample project file:</span></span>

[!code-xml[XUnit Basic Template](../../../samples/snippets/csharp/xunit-test/xunit-test.csproj)]

## <a name="arguments"></a><span data-ttu-id="b4331-117">引数</span><span class="sxs-lookup"><span data-stu-id="b4331-117">Arguments</span></span>

`PROJECT`

<span data-ttu-id="b4331-118">テスト プロジェクトへのパス。</span><span class="sxs-lookup"><span data-stu-id="b4331-118">Path to the test project.</span></span> <span data-ttu-id="b4331-119">指定しない場合は、既定で現在のディレクトリに設定されます。</span><span class="sxs-lookup"><span data-stu-id="b4331-119">If not specified, it defaults to current directory.</span></span>

## <a name="options"></a><span data-ttu-id="b4331-120">オプション</span><span class="sxs-lookup"><span data-stu-id="b4331-120">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="b4331-121">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="b4331-121">.NET Core 2.1</span></span>](#tab/netcore21)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="b4331-122">テスト実行で指定されたパスからカスタムのテスト アダプターを使用します。</span><span class="sxs-lookup"><span data-stu-id="b4331-122">Use the custom test adapters from the specified path in the test run.</span></span>

`--blame`

<span data-ttu-id="b4331-123">変更履歴モードでテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="b4331-123">Runs the tests in blame mode.</span></span> <span data-ttu-id="b4331-124">このオプションは、テスト ホストのクラッシュを引き起こす問題のあるテストを分離するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b4331-124">This option is helpful in isolating the problematic tests causing test host to crash.</span></span> <span data-ttu-id="b4331-125">これは、現在のディレクトリ内に出力ファイルを *Sequence.xml* として作成します。このファイルは、クラッシュ前にテストの実行順序をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="b4331-125">It creates an output file in the current directory as *Sequence.xml* that captures the order of tests execution before the crash.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="b4331-126">ビルド構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="b4331-126">Defines the build configuration.</span></span> <span data-ttu-id="b4331-127">既定値は `Debug` ですが、プロジェクトの構成がこの既定の SDK 設定をオーバーライドする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b4331-127">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="b4331-128">テストの実行のためのデータ コレクターを有効にします。</span><span class="sxs-lookup"><span data-stu-id="b4331-128">Enables data collector for the test run.</span></span> <span data-ttu-id="b4331-129">詳細については、[「Monitor and analyze test run」](https://aka.ms/vstest-collect) (テストの実行のモニターと分析) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4331-129">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="b4331-130">テスト プラットフォームの診断モードを有効にし、指定したファイルに診断メッセージを出力します。</span><span class="sxs-lookup"><span data-stu-id="b4331-130">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="b4331-131">特定の[フレームワーク](../../standard/frameworks.md)のテスト バイナリを検索します。</span><span class="sxs-lookup"><span data-stu-id="b4331-131">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="b4331-132">指定された式を使用して、現在のプロジェクト内のテストを除外します。</span><span class="sxs-lookup"><span data-stu-id="b4331-132">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="b4331-133">詳細については、「[フィルター オプションの詳細](#filter-option-details)」セクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b4331-133">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="b4331-134">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b4331-134">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="b4331-135">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="b4331-135">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="b4331-136">テスト結果のロガーを指定します。</span><span class="sxs-lookup"><span data-stu-id="b4331-136">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="b4331-137">実行前にテスト プロジェクトをビルドしません。</span><span class="sxs-lookup"><span data-stu-id="b4331-137">Doesn't build the test project before running it.</span></span> <span data-ttu-id="b4331-138">また、`--no-restore` フラグを暗黙的に設定します。</span><span class="sxs-lookup"><span data-stu-id="b4331-138">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="b4331-139">コマンドを実行するときに、暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="b4331-139">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="b4331-140">実行するバイナリを検索するディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="b4331-140">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="b4331-141">テスト結果が配置されるディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="b4331-141">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="b4331-142">指定されたディレクトリが存在しない場合は、作成されます。</span><span class="sxs-lookup"><span data-stu-id="b4331-142">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="b4331-143">テストの実行時に使用される設定です。</span><span class="sxs-lookup"><span data-stu-id="b4331-143">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="b4331-144">現在のプロジェクトで検出されたすべてのテストを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b4331-144">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="b4331-145">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="b4331-145">Sets the verbosity level of the command.</span></span> <span data-ttu-id="b4331-146">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="b4331-146">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="b4331-147">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="b4331-147">.NET Core 2.0</span></span>](#tab/netcore20)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="b4331-148">テスト実行で指定されたパスからカスタムのテスト アダプターを使用します。</span><span class="sxs-lookup"><span data-stu-id="b4331-148">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="b4331-149">ビルド構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="b4331-149">Defines the build configuration.</span></span> <span data-ttu-id="b4331-150">既定値は `Debug` ですが、プロジェクトの構成がこの既定の SDK 設定をオーバーライドする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b4331-150">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="b4331-151">テストの実行のためのデータ コレクターを有効にします。</span><span class="sxs-lookup"><span data-stu-id="b4331-151">Enables data collector for the test run.</span></span> <span data-ttu-id="b4331-152">詳細については、[「Monitor and analyze test run」](https://aka.ms/vstest-collect) (テストの実行のモニターと分析) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4331-152">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="b4331-153">テスト プラットフォームの診断モードを有効にし、指定したファイルに診断メッセージを出力します。</span><span class="sxs-lookup"><span data-stu-id="b4331-153">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="b4331-154">特定の[フレームワーク](../../standard/frameworks.md)のテスト バイナリを検索します。</span><span class="sxs-lookup"><span data-stu-id="b4331-154">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="b4331-155">指定された式を使用して、現在のプロジェクト内のテストを除外します。</span><span class="sxs-lookup"><span data-stu-id="b4331-155">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="b4331-156">詳細については、「[フィルター オプションの詳細](#filter-option-details)」セクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b4331-156">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="b4331-157">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b4331-157">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="b4331-158">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="b4331-158">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="b4331-159">テスト結果のロガーを指定します。</span><span class="sxs-lookup"><span data-stu-id="b4331-159">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="b4331-160">実行前にテスト プロジェクトをビルドしません。</span><span class="sxs-lookup"><span data-stu-id="b4331-160">Doesn't build the test project before running it.</span></span> <span data-ttu-id="b4331-161">また、`--no-restore` フラグを暗黙的に設定します。</span><span class="sxs-lookup"><span data-stu-id="b4331-161">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="b4331-162">コマンドを実行するときに、暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="b4331-162">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="b4331-163">実行するバイナリを検索するディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="b4331-163">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="b4331-164">テスト結果が配置されるディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="b4331-164">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="b4331-165">指定されたディレクトリが存在しない場合は、作成されます。</span><span class="sxs-lookup"><span data-stu-id="b4331-165">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="b4331-166">テストの実行時に使用される設定です。</span><span class="sxs-lookup"><span data-stu-id="b4331-166">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="b4331-167">現在のプロジェクトで検出されたすべてのテストを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b4331-167">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="b4331-168">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="b4331-168">Sets the verbosity level of the command.</span></span> <span data-ttu-id="b4331-169">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="b4331-169">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="b4331-170">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="b4331-170">.NET Core 1.x</span></span>](#tab/netcore1x)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="b4331-171">テスト実行で指定されたパスからカスタムのテスト アダプターを使用します。</span><span class="sxs-lookup"><span data-stu-id="b4331-171">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="b4331-172">ビルド構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="b4331-172">Defines the build configuration.</span></span> <span data-ttu-id="b4331-173">既定値は `Debug` ですが、プロジェクトの構成がこの既定の SDK 設定をオーバーライドする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b4331-173">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="b4331-174">テスト プラットフォームの診断モードを有効にし、指定したファイルに診断メッセージを出力します。</span><span class="sxs-lookup"><span data-stu-id="b4331-174">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="b4331-175">特定の[フレームワーク](../../standard/frameworks.md)のテスト バイナリを検索します。</span><span class="sxs-lookup"><span data-stu-id="b4331-175">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="b4331-176">指定された式を使用して、現在のプロジェクト内のテストを除外します。</span><span class="sxs-lookup"><span data-stu-id="b4331-176">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="b4331-177">詳細については、「[フィルター オプションの詳細](#filter-option-details)」セクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b4331-177">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="b4331-178">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b4331-178">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="b4331-179">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="b4331-179">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="b4331-180">テスト結果のロガーを指定します。</span><span class="sxs-lookup"><span data-stu-id="b4331-180">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="b4331-181">実行前にテスト プロジェクトをビルドしません。</span><span class="sxs-lookup"><span data-stu-id="b4331-181">Doesn't build the test project before running it.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="b4331-182">実行するバイナリを検索するディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="b4331-182">Directory in which to find the binaries to run.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="b4331-183">テストの実行時に使用される設定です。</span><span class="sxs-lookup"><span data-stu-id="b4331-183">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="b4331-184">現在のプロジェクトで検出されたすべてのテストを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b4331-184">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="b4331-185">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="b4331-185">Sets the verbosity level of the command.</span></span> <span data-ttu-id="b4331-186">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="b4331-186">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="b4331-187">使用例</span><span class="sxs-lookup"><span data-stu-id="b4331-187">Examples</span></span>

<span data-ttu-id="b4331-188">現在のディレクトリのプロジェクトでテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="b4331-188">Run the tests in the project in the current directory:</span></span>

`dotnet test`

<span data-ttu-id="b4331-189">`test1` プロジェクトでテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="b4331-189">Run the tests in the `test1` project:</span></span>

`dotnet test ~/projects/test1/test1.csproj`

<span data-ttu-id="b4331-190">現在のディレクトリでプロジェクトのテストを実行し、trx 形式でテスト結果ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="b4331-190">Run the tests in the project in the current directory and generate a test results file in the trx format:</span></span>

`dotnet test --logger:trx`

## <a name="filter-option-details"></a><span data-ttu-id="b4331-191">フィルター オプションの詳細</span><span class="sxs-lookup"><span data-stu-id="b4331-191">Filter option details</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="b4331-192">`<Expression>` の形式は `<property><operator><value>[|&<Expression>]` です。</span><span class="sxs-lookup"><span data-stu-id="b4331-192">`<Expression>` has the format `<property><operator><value>[|&<Expression>]`.</span></span>

<span data-ttu-id="b4331-193">`<property>` は `Test Case` の属性です。</span><span class="sxs-lookup"><span data-stu-id="b4331-193">`<property>` is an attribute of the `Test Case`.</span></span> <span data-ttu-id="b4331-194">よく利用される単体テスト フレームワークでサポートされるプロパティは以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="b4331-194">The following are the properties supported by popular unit test frameworks:</span></span>

| <span data-ttu-id="b4331-195">テスト フレームワーク</span><span class="sxs-lookup"><span data-stu-id="b4331-195">Test Framework</span></span> | <span data-ttu-id="b4331-196">サポートされるプロパティ</span><span class="sxs-lookup"><span data-stu-id="b4331-196">Supported properties</span></span>                                                                                      |
| -------------- | --------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="b4331-197">MSTest</span><span class="sxs-lookup"><span data-stu-id="b4331-197">MSTest</span></span>         | <ul><li><span data-ttu-id="b4331-198">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="b4331-198">FullyQualifiedName</span></span></li><li><span data-ttu-id="b4331-199">name</span><span class="sxs-lookup"><span data-stu-id="b4331-199">Name</span></span></li><li><span data-ttu-id="b4331-200">ClassName</span><span class="sxs-lookup"><span data-stu-id="b4331-200">ClassName</span></span></li><li><span data-ttu-id="b4331-201">優先度</span><span class="sxs-lookup"><span data-stu-id="b4331-201">Priority</span></span></li><li><span data-ttu-id="b4331-202">TestCategory</span><span class="sxs-lookup"><span data-stu-id="b4331-202">TestCategory</span></span></li></ul> |
| <span data-ttu-id="b4331-203">xUnit</span><span class="sxs-lookup"><span data-stu-id="b4331-203">xUnit</span></span>          | <ul><li><span data-ttu-id="b4331-204">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="b4331-204">FullyQualifiedName</span></span></li><li><span data-ttu-id="b4331-205">DisplayName</span><span class="sxs-lookup"><span data-stu-id="b4331-205">DisplayName</span></span></li><li><span data-ttu-id="b4331-206">Traits</span><span class="sxs-lookup"><span data-stu-id="b4331-206">Traits</span></span></li></ul>                                   |

<span data-ttu-id="b4331-207">`<operator>` は、プロパティと値の関係を示します。</span><span class="sxs-lookup"><span data-stu-id="b4331-207">The `<operator>` describes the relationship between the property and the value:</span></span>

| <span data-ttu-id="b4331-208">演算子</span><span class="sxs-lookup"><span data-stu-id="b4331-208">Operator</span></span> | <span data-ttu-id="b4331-209">関数</span><span class="sxs-lookup"><span data-stu-id="b4331-209">Function</span></span>        |
| :------: | --------------- |
| `=`      | <span data-ttu-id="b4331-210">完全一致</span><span class="sxs-lookup"><span data-stu-id="b4331-210">Exact match</span></span>     |
| `!=`     | <span data-ttu-id="b4331-211">完全一致ではない</span><span class="sxs-lookup"><span data-stu-id="b4331-211">Not exact match</span></span> |
| `~`      | <span data-ttu-id="b4331-212">内容</span><span class="sxs-lookup"><span data-stu-id="b4331-212">Contains</span></span>        |

<span data-ttu-id="b4331-213">`<value>` は文字列です。</span><span class="sxs-lookup"><span data-stu-id="b4331-213">`<value>` is a string.</span></span> <span data-ttu-id="b4331-214">すべての参照で大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="b4331-214">All the lookups are case insensitive.</span></span>

<span data-ttu-id="b4331-215">`<operator>` を含まない式は、自動的に `FullyQualifiedName` プロパティの `contains` とみなされます (たとえば、`dotnet test --filter xyz` は `dotnet test --filter FullyQualifiedName~xyz` と同じです)。</span><span class="sxs-lookup"><span data-stu-id="b4331-215">An expression without an `<operator>` is automatically considered as a `contains` on `FullyQualifiedName` property (for example, `dotnet test --filter xyz` is same as `dotnet test --filter FullyQualifiedName~xyz`).</span></span>

<span data-ttu-id="b4331-216">式は条件演算子を使用して結合できます。</span><span class="sxs-lookup"><span data-stu-id="b4331-216">Expressions can be joined with conditional operators:</span></span>

| <span data-ttu-id="b4331-217">演算子</span><span class="sxs-lookup"><span data-stu-id="b4331-217">Operator</span></span>            | <span data-ttu-id="b4331-218">関数</span><span class="sxs-lookup"><span data-stu-id="b4331-218">Function</span></span> |
| ------------------- | -------- |
| <code>&#124;</code> | <span data-ttu-id="b4331-219">OR</span><span class="sxs-lookup"><span data-stu-id="b4331-219">OR</span></span>       |
| `&`                 | <span data-ttu-id="b4331-220">AND</span><span class="sxs-lookup"><span data-stu-id="b4331-220">AND</span></span>      |

<span data-ttu-id="b4331-221">条件演算子を使用する場合は、式をかっこで囲みます (例: `(Name~TestMethod1) | (Name~TestMethod2)`)。</span><span class="sxs-lookup"><span data-stu-id="b4331-221">You can enclose expressions in parenthesis when using conditional operators (for example, `(Name~TestMethod1) | (Name~TestMethod2)`).</span></span>

<span data-ttu-id="b4331-222">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b4331-222">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b4331-223">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4331-223">See also</span></span>

* [<span data-ttu-id="b4331-224">フレームワークとターゲット</span><span class="sxs-lookup"><span data-stu-id="b4331-224">Frameworks and Targets</span></span>](../../standard/frameworks.md)  
* [<span data-ttu-id="b4331-225">.NET Core のランタイム識別子 (RID) のカタログ</span><span class="sxs-lookup"><span data-stu-id="b4331-225">.NET Core Runtime IDentifier (RID) catalog</span></span>](../rid-catalog.md)
