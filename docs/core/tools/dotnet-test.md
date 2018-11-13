---
title: dotnet test コマンド - .NET Core CLI
description: dotnet test コマンドは、指定されたプロジェクトで単体テストを実行する場合に使用されます。
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 73b1d832b855798dd053187bbb24e8fb989fedf1
ms.sourcegitcommit: 3b1cb8467bd73dee854b604e306c0e7e3882d91a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "46696457"
---
# <a name="dotnet-test"></a><span data-ttu-id="0f700-103">dotnet test</span><span class="sxs-lookup"><span data-stu-id="0f700-103">dotnet test</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="0f700-104">name</span><span class="sxs-lookup"><span data-stu-id="0f700-104">Name</span></span>

<span data-ttu-id="0f700-105">`dotnet test` - 単体テストを実行するために使用される .NET テスト ドライバー。</span><span class="sxs-lookup"><span data-stu-id="0f700-105">`dotnet test` - .NET test driver used to execute unit tests.</span></span>

## <a name="synopsis"></a><span data-ttu-id="0f700-106">構文</span><span class="sxs-lookup"><span data-stu-id="0f700-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="0f700-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="0f700-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [--blame] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] 
    [-v|--verbosity] [-- <RunSettings arguments>]

dotnet test [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="0f700-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="0f700-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]

dotnet test [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="0f700-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="0f700-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [-d|--diag] [-f|--framework] [--filter] [-l|--logger] [--no-build] [-o|--output] [-s|--settings] [-t|--list-tests]  [-v|--verbosity]

dotnet test [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="0f700-110">説明</span><span class="sxs-lookup"><span data-stu-id="0f700-110">Description</span></span>

<span data-ttu-id="0f700-111">`dotnet test` コマンドは、指定されたプロジェクトで単体テストを実行する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f700-111">The `dotnet test` command is used to execute unit tests in a given project.</span></span> <span data-ttu-id="0f700-112">`dotnet test` コマンドは、プロジェクト用に指定されたテスト ランナーのコンソール アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="0f700-112">The `dotnet test` command launches the test runner console application specified for a project.</span></span> <span data-ttu-id="0f700-113">テスト ランナーでは、単体テスト フレームワーク (MSTest、NUnit、xUnit など) 用に定義されたテストを実行し、各テストの成功または失敗をレポートします。</span><span class="sxs-lookup"><span data-stu-id="0f700-113">The test runner executes the tests defined for a unit test framework (for example, MSTest, NUnit, or xUnit) and reports the success or failure of each test.</span></span> <span data-ttu-id="0f700-114">すべてのテストが成功した場合、テスト ランナーは 0 の終了コードを返します。それ以外の、いずれかのテストに失敗した場合は、1 を返します。</span><span class="sxs-lookup"><span data-stu-id="0f700-114">If all tests are successful, the test runner returns 0 as an exit code; otherwise if any test fails, it returns 1.</span></span> <span data-ttu-id="0f700-115">テスト ランナーと単体テスト ライブラリは、NuGet パッケージとしてパッケージ化され、プロジェクトの通常の依存関係として復元されます。</span><span class="sxs-lookup"><span data-stu-id="0f700-115">The test runner and the unit test library are packaged as NuGet packages and are restored as ordinary dependencies for the project.</span></span>

<span data-ttu-id="0f700-116">テスト プロジェクトでは、通常の `<PackageReference>` 要素を使用してテスト ランナーを指定します。次のサンプル プロジェクト ファイルのようになります。</span><span class="sxs-lookup"><span data-stu-id="0f700-116">Test projects specify the test runner using an ordinary `<PackageReference>` element, as seen in the following sample project file:</span></span>

[!code-xml[XUnit Basic Template](../../../samples/snippets/csharp/xunit-test/xunit-test.csproj)]

## <a name="arguments"></a><span data-ttu-id="0f700-117">引数</span><span class="sxs-lookup"><span data-stu-id="0f700-117">Arguments</span></span>

`PROJECT`

<span data-ttu-id="0f700-118">テスト プロジェクトへのパス。</span><span class="sxs-lookup"><span data-stu-id="0f700-118">Path to the test project.</span></span> <span data-ttu-id="0f700-119">指定しない場合は、既定で現在のディレクトリに設定されます。</span><span class="sxs-lookup"><span data-stu-id="0f700-119">If not specified, it defaults to current directory.</span></span>

## <a name="options"></a><span data-ttu-id="0f700-120">オプション</span><span class="sxs-lookup"><span data-stu-id="0f700-120">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="0f700-121">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="0f700-121">.NET Core 2.1</span></span>](#tab/netcore21)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="0f700-122">テスト実行で指定されたパスからカスタムのテスト アダプターを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f700-122">Use the custom test adapters from the specified path in the test run.</span></span>

`--blame`

<span data-ttu-id="0f700-123">変更履歴モードでテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="0f700-123">Runs the tests in blame mode.</span></span> <span data-ttu-id="0f700-124">このオプションは、テスト ホストのクラッシュを引き起こす問題のあるテストを分離するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0f700-124">This option is helpful in isolating the problematic tests causing test host to crash.</span></span> <span data-ttu-id="0f700-125">これは、現在のディレクトリ内に出力ファイルを *Sequence.xml* として作成します。このファイルは、クラッシュ前にテストの実行順序をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="0f700-125">It creates an output file in the current directory as *Sequence.xml* that captures the order of tests execution before the crash.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="0f700-126">ビルド構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="0f700-126">Defines the build configuration.</span></span> <span data-ttu-id="0f700-127">既定値は `Debug` ですが、プロジェクトの構成がこの既定の SDK 設定をオーバーライドする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0f700-127">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="0f700-128">テストの実行のためのデータ コレクターを有効にします。</span><span class="sxs-lookup"><span data-stu-id="0f700-128">Enables data collector for the test run.</span></span> <span data-ttu-id="0f700-129">詳細については、[「Monitor and analyze test run」](https://aka.ms/vstest-collect) (テストの実行のモニターと分析) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f700-129">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="0f700-130">テスト プラットフォームの診断モードを有効にし、指定したファイルに診断メッセージを出力します。</span><span class="sxs-lookup"><span data-stu-id="0f700-130">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="0f700-131">特定の[フレームワーク](../../standard/frameworks.md)のテスト バイナリを検索します。</span><span class="sxs-lookup"><span data-stu-id="0f700-131">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="0f700-132">指定された式を使用して、現在のプロジェクト内のテストを除外します。</span><span class="sxs-lookup"><span data-stu-id="0f700-132">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="0f700-133">詳細については、「[フィルター オプションの詳細](#filter-option-details)」セクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0f700-133">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="0f700-134">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0f700-134">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="0f700-135">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="0f700-135">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="0f700-136">テスト結果のロガーを指定します。</span><span class="sxs-lookup"><span data-stu-id="0f700-136">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="0f700-137">実行前にテスト プロジェクトをビルドしません。</span><span class="sxs-lookup"><span data-stu-id="0f700-137">Doesn't build the test project before running it.</span></span> <span data-ttu-id="0f700-138">また、`--no-restore` フラグを暗黙的に設定します。</span><span class="sxs-lookup"><span data-stu-id="0f700-138">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="0f700-139">コマンドを実行するときに、暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="0f700-139">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="0f700-140">実行するバイナリを検索するディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="0f700-140">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="0f700-141">テスト結果が配置されるディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="0f700-141">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="0f700-142">指定されたディレクトリが存在しない場合は、作成されます。</span><span class="sxs-lookup"><span data-stu-id="0f700-142">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="0f700-143">テストの実行時に使用される設定です。</span><span class="sxs-lookup"><span data-stu-id="0f700-143">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="0f700-144">現在のプロジェクトで検出されたすべてのテストを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="0f700-144">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="0f700-145">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="0f700-145">Sets the verbosity level of the command.</span></span> <span data-ttu-id="0f700-146">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="0f700-146">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

`RunSettings arguments`

<span data-ttu-id="0f700-147">テストの RunSettings 構成として渡される引数です。</span><span class="sxs-lookup"><span data-stu-id="0f700-147">Arguments passed as RunSettings configurations for the test.</span></span> <span data-ttu-id="0f700-148">引数は、"-- " に続く `[name]=[value]` のペアとして指定されます (-- の後ろのスペースに注意してください)。</span><span class="sxs-lookup"><span data-stu-id="0f700-148">Arguments are specified as `[name]=[value]` pairs after "-- " (note the space after --).</span></span> <span data-ttu-id="0f700-149">複数の `[name]=[value]` のペアを区切るにはスペースを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f700-149">A space is used to separate multiple `[name]=[value]` pairs.</span></span>

<span data-ttu-id="0f700-150">例 : `dotnet test -- MSTest.DeploymentEnabled=false MSTest.MapInconclusiveToFailed=True`</span><span class="sxs-lookup"><span data-stu-id="0f700-150">Example: `dotnet test -- MSTest.DeploymentEnabled=false MSTest.MapInconclusiveToFailed=True`</span></span>

<span data-ttu-id="0f700-151">RunSettings について詳しくは、[vstest.console.exe: RunSettings 引数渡し](https://github.com/Microsoft/vstest-docs/blob/master/docs/RunSettingsArguments.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0f700-151">For more information about RunSettings, see [vstest.console.exe: Passing RunSettings args](https://github.com/Microsoft/vstest-docs/blob/master/docs/RunSettingsArguments.md).</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="0f700-152">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="0f700-152">.NET Core 2.0</span></span>](#tab/netcore20)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="0f700-153">テスト実行で指定されたパスからカスタムのテスト アダプターを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f700-153">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="0f700-154">ビルド構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="0f700-154">Defines the build configuration.</span></span> <span data-ttu-id="0f700-155">既定値は `Debug` ですが、プロジェクトの構成がこの既定の SDK 設定をオーバーライドする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0f700-155">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="0f700-156">テストの実行のためのデータ コレクターを有効にします。</span><span class="sxs-lookup"><span data-stu-id="0f700-156">Enables data collector for the test run.</span></span> <span data-ttu-id="0f700-157">詳細については、[「Monitor and analyze test run」](https://aka.ms/vstest-collect) (テストの実行のモニターと分析) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f700-157">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="0f700-158">テスト プラットフォームの診断モードを有効にし、指定したファイルに診断メッセージを出力します。</span><span class="sxs-lookup"><span data-stu-id="0f700-158">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="0f700-159">特定の[フレームワーク](../../standard/frameworks.md)のテスト バイナリを検索します。</span><span class="sxs-lookup"><span data-stu-id="0f700-159">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="0f700-160">指定された式を使用して、現在のプロジェクト内のテストを除外します。</span><span class="sxs-lookup"><span data-stu-id="0f700-160">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="0f700-161">詳細については、「[フィルター オプションの詳細](#filter-option-details)」セクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0f700-161">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="0f700-162">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0f700-162">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="0f700-163">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="0f700-163">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="0f700-164">テスト結果のロガーを指定します。</span><span class="sxs-lookup"><span data-stu-id="0f700-164">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="0f700-165">実行前にテスト プロジェクトをビルドしません。</span><span class="sxs-lookup"><span data-stu-id="0f700-165">Doesn't build the test project before running it.</span></span> <span data-ttu-id="0f700-166">また、`--no-restore` フラグを暗黙的に設定します。</span><span class="sxs-lookup"><span data-stu-id="0f700-166">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="0f700-167">コマンドを実行するときに、暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="0f700-167">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="0f700-168">実行するバイナリを検索するディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="0f700-168">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="0f700-169">テスト結果が配置されるディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="0f700-169">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="0f700-170">指定されたディレクトリが存在しない場合は、作成されます。</span><span class="sxs-lookup"><span data-stu-id="0f700-170">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="0f700-171">テストの実行時に使用される設定です。</span><span class="sxs-lookup"><span data-stu-id="0f700-171">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="0f700-172">現在のプロジェクトで検出されたすべてのテストを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="0f700-172">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="0f700-173">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="0f700-173">Sets the verbosity level of the command.</span></span> <span data-ttu-id="0f700-174">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="0f700-174">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="0f700-175">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="0f700-175">.NET Core 1.x</span></span>](#tab/netcore1x)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="0f700-176">テスト実行で指定されたパスからカスタムのテスト アダプターを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f700-176">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="0f700-177">ビルド構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="0f700-177">Defines the build configuration.</span></span> <span data-ttu-id="0f700-178">既定値は `Debug` ですが、プロジェクトの構成がこの既定の SDK 設定をオーバーライドする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0f700-178">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="0f700-179">テスト プラットフォームの診断モードを有効にし、指定したファイルに診断メッセージを出力します。</span><span class="sxs-lookup"><span data-stu-id="0f700-179">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="0f700-180">特定の[フレームワーク](../../standard/frameworks.md)のテスト バイナリを検索します。</span><span class="sxs-lookup"><span data-stu-id="0f700-180">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="0f700-181">指定された式を使用して、現在のプロジェクト内のテストを除外します。</span><span class="sxs-lookup"><span data-stu-id="0f700-181">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="0f700-182">詳細については、「[フィルター オプションの詳細](#filter-option-details)」セクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0f700-182">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="0f700-183">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0f700-183">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="0f700-184">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="0f700-184">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="0f700-185">テスト結果のロガーを指定します。</span><span class="sxs-lookup"><span data-stu-id="0f700-185">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="0f700-186">実行前にテスト プロジェクトをビルドしません。</span><span class="sxs-lookup"><span data-stu-id="0f700-186">Doesn't build the test project before running it.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="0f700-187">実行するバイナリを検索するディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="0f700-187">Directory in which to find the binaries to run.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="0f700-188">テストの実行時に使用される設定です。</span><span class="sxs-lookup"><span data-stu-id="0f700-188">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="0f700-189">現在のプロジェクトで検出されたすべてのテストを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="0f700-189">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="0f700-190">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="0f700-190">Sets the verbosity level of the command.</span></span> <span data-ttu-id="0f700-191">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="0f700-191">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="0f700-192">使用例</span><span class="sxs-lookup"><span data-stu-id="0f700-192">Examples</span></span>

<span data-ttu-id="0f700-193">現在のディレクトリのプロジェクトでテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="0f700-193">Run the tests in the project in the current directory:</span></span>

`dotnet test`

<span data-ttu-id="0f700-194">`test1` プロジェクトでテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="0f700-194">Run the tests in the `test1` project:</span></span>

`dotnet test ~/projects/test1/test1.csproj`

<span data-ttu-id="0f700-195">現在のディレクトリでプロジェクトのテストを実行し、trx 形式でテスト結果ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="0f700-195">Run the tests in the project in the current directory and generate a test results file in the trx format:</span></span>

`dotnet test --logger:trx`

## <a name="filter-option-details"></a><span data-ttu-id="0f700-196">フィルター オプションの詳細</span><span class="sxs-lookup"><span data-stu-id="0f700-196">Filter option details</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="0f700-197">`<Expression>` の形式は `<property><operator><value>[|&<Expression>]` です。</span><span class="sxs-lookup"><span data-stu-id="0f700-197">`<Expression>` has the format `<property><operator><value>[|&<Expression>]`.</span></span>

<span data-ttu-id="0f700-198">`<property>` は `Test Case` の属性です。</span><span class="sxs-lookup"><span data-stu-id="0f700-198">`<property>` is an attribute of the `Test Case`.</span></span> <span data-ttu-id="0f700-199">よく利用される単体テスト フレームワークでサポートされるプロパティは以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="0f700-199">The following are the properties supported by popular unit test frameworks:</span></span>

| <span data-ttu-id="0f700-200">テスト フレームワーク</span><span class="sxs-lookup"><span data-stu-id="0f700-200">Test Framework</span></span> | <span data-ttu-id="0f700-201">サポートされるプロパティ</span><span class="sxs-lookup"><span data-stu-id="0f700-201">Supported properties</span></span>                                                                                      |
| -------------- | --------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="0f700-202">MSTest</span><span class="sxs-lookup"><span data-stu-id="0f700-202">MSTest</span></span>         | <ul><li><span data-ttu-id="0f700-203">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="0f700-203">FullyQualifiedName</span></span></li><li><span data-ttu-id="0f700-204">name</span><span class="sxs-lookup"><span data-stu-id="0f700-204">Name</span></span></li><li><span data-ttu-id="0f700-205">ClassName</span><span class="sxs-lookup"><span data-stu-id="0f700-205">ClassName</span></span></li><li><span data-ttu-id="0f700-206">優先度</span><span class="sxs-lookup"><span data-stu-id="0f700-206">Priority</span></span></li><li><span data-ttu-id="0f700-207">TestCategory</span><span class="sxs-lookup"><span data-stu-id="0f700-207">TestCategory</span></span></li></ul> |
| <span data-ttu-id="0f700-208">xUnit</span><span class="sxs-lookup"><span data-stu-id="0f700-208">xUnit</span></span>          | <ul><li><span data-ttu-id="0f700-209">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="0f700-209">FullyQualifiedName</span></span></li><li><span data-ttu-id="0f700-210">DisplayName</span><span class="sxs-lookup"><span data-stu-id="0f700-210">DisplayName</span></span></li><li><span data-ttu-id="0f700-211">Traits</span><span class="sxs-lookup"><span data-stu-id="0f700-211">Traits</span></span></li></ul>                                   |

<span data-ttu-id="0f700-212">`<operator>` は、プロパティと値の関係を示します。</span><span class="sxs-lookup"><span data-stu-id="0f700-212">The `<operator>` describes the relationship between the property and the value:</span></span>

| <span data-ttu-id="0f700-213">演算子</span><span class="sxs-lookup"><span data-stu-id="0f700-213">Operator</span></span> | <span data-ttu-id="0f700-214">関数</span><span class="sxs-lookup"><span data-stu-id="0f700-214">Function</span></span>        |
| :------: | --------------- |
| `=`      | <span data-ttu-id="0f700-215">完全一致</span><span class="sxs-lookup"><span data-stu-id="0f700-215">Exact match</span></span>     |
| `!=`     | <span data-ttu-id="0f700-216">完全一致ではない</span><span class="sxs-lookup"><span data-stu-id="0f700-216">Not exact match</span></span> |
| `~`      | <span data-ttu-id="0f700-217">内容</span><span class="sxs-lookup"><span data-stu-id="0f700-217">Contains</span></span>        |

<span data-ttu-id="0f700-218">`<value>` は文字列です。</span><span class="sxs-lookup"><span data-stu-id="0f700-218">`<value>` is a string.</span></span> <span data-ttu-id="0f700-219">すべての参照で大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="0f700-219">All the lookups are case insensitive.</span></span>

<span data-ttu-id="0f700-220">`<operator>` を含まない式は、自動的に `FullyQualifiedName` プロパティの `contains` とみなされます (たとえば、`dotnet test --filter xyz` は `dotnet test --filter FullyQualifiedName~xyz` と同じです)。</span><span class="sxs-lookup"><span data-stu-id="0f700-220">An expression without an `<operator>` is automatically considered as a `contains` on `FullyQualifiedName` property (for example, `dotnet test --filter xyz` is same as `dotnet test --filter FullyQualifiedName~xyz`).</span></span>

<span data-ttu-id="0f700-221">式は条件演算子を使用して結合できます。</span><span class="sxs-lookup"><span data-stu-id="0f700-221">Expressions can be joined with conditional operators:</span></span>

| <span data-ttu-id="0f700-222">演算子</span><span class="sxs-lookup"><span data-stu-id="0f700-222">Operator</span></span>            | <span data-ttu-id="0f700-223">関数</span><span class="sxs-lookup"><span data-stu-id="0f700-223">Function</span></span> |
| ------------------- | -------- |
| <code>&#124;</code> | <span data-ttu-id="0f700-224">OR</span><span class="sxs-lookup"><span data-stu-id="0f700-224">OR</span></span>       |
| `&`                 | <span data-ttu-id="0f700-225">AND</span><span class="sxs-lookup"><span data-stu-id="0f700-225">AND</span></span>      |

<span data-ttu-id="0f700-226">条件演算子を使用する場合は、式をかっこで囲みます (例: `(Name~TestMethod1) | (Name~TestMethod2)`)。</span><span class="sxs-lookup"><span data-stu-id="0f700-226">You can enclose expressions in parenthesis when using conditional operators (for example, `(Name~TestMethod1) | (Name~TestMethod2)`).</span></span>

<span data-ttu-id="0f700-227">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0f700-227">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0f700-228">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f700-228">See also</span></span>

* [<span data-ttu-id="0f700-229">フレームワークとターゲット</span><span class="sxs-lookup"><span data-stu-id="0f700-229">Frameworks and Targets</span></span>](../../standard/frameworks.md)  
* [<span data-ttu-id="0f700-230">.NET Core のランタイム識別子 (RID) のカタログ</span><span class="sxs-lookup"><span data-stu-id="0f700-230">.NET Core Runtime IDentifier (RID) catalog</span></span>](../rid-catalog.md)
