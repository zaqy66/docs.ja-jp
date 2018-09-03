---
title: dotnet test コマンド - .NET Core CLI
description: dotnet test コマンドは、指定されたプロジェクトで単体テストを実行する場合に使用されます。
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 2bee78ca44026f28c51fac3bcf87d976b53e48a7
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43390691"
---
# <a name="dotnet-test"></a><span data-ttu-id="76280-103">dotnet test</span><span class="sxs-lookup"><span data-stu-id="76280-103">dotnet test</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="76280-104">name</span><span class="sxs-lookup"><span data-stu-id="76280-104">Name</span></span>

<span data-ttu-id="76280-105">`dotnet test` - 単体テストを実行するために使用される .NET テスト ドライバー。</span><span class="sxs-lookup"><span data-stu-id="76280-105">`dotnet test` - .NET test driver used to execute unit tests.</span></span>

## <a name="synopsis"></a><span data-ttu-id="76280-106">構文</span><span class="sxs-lookup"><span data-stu-id="76280-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="76280-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="76280-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [--blame] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="76280-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="76280-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="76280-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="76280-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [-d|--diag] [-f|--framework] [--filter] [-l|--logger] [--no-build] [-o|--output] [-s|--settings] [-t|--list-tests]  [-v|--verbosity]
dotnet test [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="76280-110">説明</span><span class="sxs-lookup"><span data-stu-id="76280-110">Description</span></span>

<span data-ttu-id="76280-111">`dotnet test` コマンドは、指定されたプロジェクトで単体テストを実行する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="76280-111">The `dotnet test` command is used to execute unit tests in a given project.</span></span> <span data-ttu-id="76280-112">`dotnet test` コマンドは、プロジェクト用に指定されたテスト ランナーのコンソール アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="76280-112">The `dotnet test` command launches the test runner console application specified for a project.</span></span> <span data-ttu-id="76280-113">テスト ランナーでは、単体テスト フレームワーク (MSTest、NUnit、xUnit など) 用に定義されたテストを実行し、各テストの成功または失敗をレポートします。</span><span class="sxs-lookup"><span data-stu-id="76280-113">The test runner executes the tests defined for a unit test framework (for example, MSTest, NUnit, or xUnit) and reports the success or failure of each test.</span></span> <span data-ttu-id="76280-114">テスト ランナーと単体テスト ライブラリは、NuGet パッケージとしてパッケージ化され、プロジェクトの通常の依存関係として復元されます。</span><span class="sxs-lookup"><span data-stu-id="76280-114">The test runner and the unit test library are packaged as NuGet packages and are restored as ordinary dependencies for the project.</span></span>

<span data-ttu-id="76280-115">テスト プロジェクトでは、通常の `<PackageReference>` 要素を使用してテスト ランナーを指定します。次のサンプル プロジェクト ファイルのようになります。</span><span class="sxs-lookup"><span data-stu-id="76280-115">Test projects specify the test runner using an ordinary `<PackageReference>` element, as seen in the following sample project file:</span></span>

[!code-xml[XUnit Basic Template](../../../samples/snippets/csharp/xunit-test/xunit-test.csproj)]

## <a name="arguments"></a><span data-ttu-id="76280-116">引数</span><span class="sxs-lookup"><span data-stu-id="76280-116">Arguments</span></span>

`PROJECT`

<span data-ttu-id="76280-117">テスト プロジェクトへのパス。</span><span class="sxs-lookup"><span data-stu-id="76280-117">Path to the test project.</span></span> <span data-ttu-id="76280-118">指定しない場合は、既定で現在のディレクトリに設定されます。</span><span class="sxs-lookup"><span data-stu-id="76280-118">If not specified, it defaults to current directory.</span></span>

## <a name="options"></a><span data-ttu-id="76280-119">オプション</span><span class="sxs-lookup"><span data-stu-id="76280-119">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="76280-120">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="76280-120">.NET Core 2.1</span></span>](#tab/netcore21)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="76280-121">テスト実行で指定されたパスからカスタムのテスト アダプターを使用します。</span><span class="sxs-lookup"><span data-stu-id="76280-121">Use the custom test adapters from the specified path in the test run.</span></span>

`--blame`

<span data-ttu-id="76280-122">変更履歴モードでテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="76280-122">Runs the tests in blame mode.</span></span> <span data-ttu-id="76280-123">このオプションは、テスト ホストのクラッシュを引き起こす問題のあるテストを分離するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="76280-123">This option is helpful in isolating the problematic tests causing test host to crash.</span></span> <span data-ttu-id="76280-124">これは、現在のディレクトリ内に出力ファイルを *Sequence.xml* として作成します。このファイルは、クラッシュ前にテストの実行順序をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="76280-124">It creates an output file in the current directory as *Sequence.xml* that captures the order of tests execution before the crash.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="76280-125">ビルド構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="76280-125">Defines the build configuration.</span></span> <span data-ttu-id="76280-126">既定値は `Debug` ですが、プロジェクトの構成がこの既定の SDK 設定をオーバーライドする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="76280-126">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="76280-127">テストの実行のためのデータ コレクターを有効にします。</span><span class="sxs-lookup"><span data-stu-id="76280-127">Enables data collector for the test run.</span></span> <span data-ttu-id="76280-128">詳細については、[「Monitor and analyze test run」](https://aka.ms/vstest-collect) (テストの実行のモニターと分析) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76280-128">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="76280-129">テスト プラットフォームの診断モードを有効にし、指定したファイルに診断メッセージを出力します。</span><span class="sxs-lookup"><span data-stu-id="76280-129">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="76280-130">特定の[フレームワーク](../../standard/frameworks.md)のテスト バイナリを検索します。</span><span class="sxs-lookup"><span data-stu-id="76280-130">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="76280-131">指定された式を使用して、現在のプロジェクト内のテストを除外します。</span><span class="sxs-lookup"><span data-stu-id="76280-131">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="76280-132">詳細については、「[フィルター オプションの詳細](#filter-option-details)」セクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="76280-132">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="76280-133">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="76280-133">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="76280-134">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="76280-134">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="76280-135">テスト結果のロガーを指定します。</span><span class="sxs-lookup"><span data-stu-id="76280-135">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="76280-136">実行前にテスト プロジェクトをビルドしません。</span><span class="sxs-lookup"><span data-stu-id="76280-136">Doesn't build the test project before running it.</span></span> <span data-ttu-id="76280-137">また、`--no-restore` フラグを暗黙的に設定します。</span><span class="sxs-lookup"><span data-stu-id="76280-137">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="76280-138">コマンドを実行するときに、暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="76280-138">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="76280-139">実行するバイナリを検索するディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="76280-139">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="76280-140">テスト結果が配置されるディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="76280-140">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="76280-141">指定されたディレクトリが存在しない場合は、作成されます。</span><span class="sxs-lookup"><span data-stu-id="76280-141">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="76280-142">テストの実行時に使用される設定です。</span><span class="sxs-lookup"><span data-stu-id="76280-142">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="76280-143">現在のプロジェクトで検出されたすべてのテストを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="76280-143">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="76280-144">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="76280-144">Sets the verbosity level of the command.</span></span> <span data-ttu-id="76280-145">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="76280-145">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="76280-146">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="76280-146">.NET Core 2.0</span></span>](#tab/netcore20)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="76280-147">テスト実行で指定されたパスからカスタムのテスト アダプターを使用します。</span><span class="sxs-lookup"><span data-stu-id="76280-147">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="76280-148">ビルド構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="76280-148">Defines the build configuration.</span></span> <span data-ttu-id="76280-149">既定値は `Debug` ですが、プロジェクトの構成がこの既定の SDK 設定をオーバーライドする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="76280-149">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="76280-150">テストの実行のためのデータ コレクターを有効にします。</span><span class="sxs-lookup"><span data-stu-id="76280-150">Enables data collector for the test run.</span></span> <span data-ttu-id="76280-151">詳細については、[「Monitor and analyze test run」](https://aka.ms/vstest-collect) (テストの実行のモニターと分析) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76280-151">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="76280-152">テスト プラットフォームの診断モードを有効にし、指定したファイルに診断メッセージを出力します。</span><span class="sxs-lookup"><span data-stu-id="76280-152">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="76280-153">特定の[フレームワーク](../../standard/frameworks.md)のテスト バイナリを検索します。</span><span class="sxs-lookup"><span data-stu-id="76280-153">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="76280-154">指定された式を使用して、現在のプロジェクト内のテストを除外します。</span><span class="sxs-lookup"><span data-stu-id="76280-154">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="76280-155">詳細については、「[フィルター オプションの詳細](#filter-option-details)」セクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="76280-155">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="76280-156">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="76280-156">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="76280-157">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="76280-157">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="76280-158">テスト結果のロガーを指定します。</span><span class="sxs-lookup"><span data-stu-id="76280-158">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="76280-159">実行前にテスト プロジェクトをビルドしません。</span><span class="sxs-lookup"><span data-stu-id="76280-159">Doesn't build the test project before running it.</span></span> <span data-ttu-id="76280-160">また、`--no-restore` フラグを暗黙的に設定します。</span><span class="sxs-lookup"><span data-stu-id="76280-160">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="76280-161">コマンドを実行するときに、暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="76280-161">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="76280-162">実行するバイナリを検索するディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="76280-162">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="76280-163">テスト結果が配置されるディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="76280-163">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="76280-164">指定されたディレクトリが存在しない場合は、作成されます。</span><span class="sxs-lookup"><span data-stu-id="76280-164">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="76280-165">テストの実行時に使用される設定です。</span><span class="sxs-lookup"><span data-stu-id="76280-165">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="76280-166">現在のプロジェクトで検出されたすべてのテストを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="76280-166">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="76280-167">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="76280-167">Sets the verbosity level of the command.</span></span> <span data-ttu-id="76280-168">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="76280-168">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="76280-169">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="76280-169">.NET Core 1.x</span></span>](#tab/netcore1x)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="76280-170">テスト実行で指定されたパスからカスタムのテスト アダプターを使用します。</span><span class="sxs-lookup"><span data-stu-id="76280-170">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="76280-171">ビルド構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="76280-171">Defines the build configuration.</span></span> <span data-ttu-id="76280-172">既定値は `Debug` ですが、プロジェクトの構成がこの既定の SDK 設定をオーバーライドする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="76280-172">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="76280-173">テスト プラットフォームの診断モードを有効にし、指定したファイルに診断メッセージを出力します。</span><span class="sxs-lookup"><span data-stu-id="76280-173">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="76280-174">特定の[フレームワーク](../../standard/frameworks.md)のテスト バイナリを検索します。</span><span class="sxs-lookup"><span data-stu-id="76280-174">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="76280-175">指定された式を使用して、現在のプロジェクト内のテストを除外します。</span><span class="sxs-lookup"><span data-stu-id="76280-175">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="76280-176">詳細については、「[フィルター オプションの詳細](#filter-option-details)」セクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="76280-176">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="76280-177">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="76280-177">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="76280-178">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="76280-178">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="76280-179">テスト結果のロガーを指定します。</span><span class="sxs-lookup"><span data-stu-id="76280-179">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="76280-180">実行前にテスト プロジェクトをビルドしません。</span><span class="sxs-lookup"><span data-stu-id="76280-180">Doesn't build the test project before running it.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="76280-181">実行するバイナリを検索するディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="76280-181">Directory in which to find the binaries to run.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="76280-182">テストの実行時に使用される設定です。</span><span class="sxs-lookup"><span data-stu-id="76280-182">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="76280-183">現在のプロジェクトで検出されたすべてのテストを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="76280-183">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="76280-184">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="76280-184">Sets the verbosity level of the command.</span></span> <span data-ttu-id="76280-185">指定できる値は、`q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]`、および `diag[nostic]` です。</span><span class="sxs-lookup"><span data-stu-id="76280-185">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="76280-186">使用例</span><span class="sxs-lookup"><span data-stu-id="76280-186">Examples</span></span>

<span data-ttu-id="76280-187">現在のディレクトリのプロジェクトでテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="76280-187">Run the tests in the project in the current directory:</span></span>

`dotnet test`

<span data-ttu-id="76280-188">`test1` プロジェクトでテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="76280-188">Run the tests in the `test1` project:</span></span>

`dotnet test ~/projects/test1/test1.csproj`

## <a name="filter-option-details"></a><span data-ttu-id="76280-189">フィルター オプションの詳細</span><span class="sxs-lookup"><span data-stu-id="76280-189">Filter option details</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="76280-190">`<Expression>` の形式は `<property><operator><value>[|&<Expression>]` です。</span><span class="sxs-lookup"><span data-stu-id="76280-190">`<Expression>` has the format `<property><operator><value>[|&<Expression>]`.</span></span>

<span data-ttu-id="76280-191">`<property>` は `Test Case` の属性です。</span><span class="sxs-lookup"><span data-stu-id="76280-191">`<property>` is an attribute of the `Test Case`.</span></span> <span data-ttu-id="76280-192">よく利用される単体テスト フレームワークでサポートされるプロパティは以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="76280-192">The following are the properties supported by popular unit test frameworks:</span></span>

| <span data-ttu-id="76280-193">テスト フレームワーク</span><span class="sxs-lookup"><span data-stu-id="76280-193">Test Framework</span></span> | <span data-ttu-id="76280-194">サポートされるプロパティ</span><span class="sxs-lookup"><span data-stu-id="76280-194">Supported properties</span></span>                                                                                      |
| -------------- | --------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="76280-195">MSTest</span><span class="sxs-lookup"><span data-stu-id="76280-195">MSTest</span></span>         | <ul><li><span data-ttu-id="76280-196">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="76280-196">FullyQualifiedName</span></span></li><li><span data-ttu-id="76280-197">name</span><span class="sxs-lookup"><span data-stu-id="76280-197">Name</span></span></li><li><span data-ttu-id="76280-198">ClassName</span><span class="sxs-lookup"><span data-stu-id="76280-198">ClassName</span></span></li><li><span data-ttu-id="76280-199">優先度</span><span class="sxs-lookup"><span data-stu-id="76280-199">Priority</span></span></li><li><span data-ttu-id="76280-200">TestCategory</span><span class="sxs-lookup"><span data-stu-id="76280-200">TestCategory</span></span></li></ul> |
| <span data-ttu-id="76280-201">xUnit</span><span class="sxs-lookup"><span data-stu-id="76280-201">xUnit</span></span>          | <ul><li><span data-ttu-id="76280-202">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="76280-202">FullyQualifiedName</span></span></li><li><span data-ttu-id="76280-203">DisplayName</span><span class="sxs-lookup"><span data-stu-id="76280-203">DisplayName</span></span></li><li><span data-ttu-id="76280-204">Traits</span><span class="sxs-lookup"><span data-stu-id="76280-204">Traits</span></span></li></ul>                                   |

<span data-ttu-id="76280-205">`<operator>` は、プロパティと値の関係を示します。</span><span class="sxs-lookup"><span data-stu-id="76280-205">The `<operator>` describes the relationship between the property and the value:</span></span>

| <span data-ttu-id="76280-206">演算子</span><span class="sxs-lookup"><span data-stu-id="76280-206">Operator</span></span> | <span data-ttu-id="76280-207">関数</span><span class="sxs-lookup"><span data-stu-id="76280-207">Function</span></span>        |
| :------: | --------------- |
| `=`      | <span data-ttu-id="76280-208">完全一致</span><span class="sxs-lookup"><span data-stu-id="76280-208">Exact match</span></span>     |
| `!=`     | <span data-ttu-id="76280-209">完全一致ではない</span><span class="sxs-lookup"><span data-stu-id="76280-209">Not exact match</span></span> |
| `~`      | <span data-ttu-id="76280-210">内容</span><span class="sxs-lookup"><span data-stu-id="76280-210">Contains</span></span>        |

<span data-ttu-id="76280-211">`<value>` は文字列です。</span><span class="sxs-lookup"><span data-stu-id="76280-211">`<value>` is a string.</span></span> <span data-ttu-id="76280-212">すべての参照で大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="76280-212">All the lookups are case insensitive.</span></span>

<span data-ttu-id="76280-213">`<operator>` を含まない式は、自動的に `FullyQualifiedName` プロパティの `contains` とみなされます (たとえば、`dotnet test --filter xyz` は `dotnet test --filter FullyQualifiedName~xyz` と同じです)。</span><span class="sxs-lookup"><span data-stu-id="76280-213">An expression without an `<operator>` is automatically considered as a `contains` on `FullyQualifiedName` property (for example, `dotnet test --filter xyz` is same as `dotnet test --filter FullyQualifiedName~xyz`).</span></span>

<span data-ttu-id="76280-214">式は条件演算子を使用して結合できます。</span><span class="sxs-lookup"><span data-stu-id="76280-214">Expressions can be joined with conditional operators:</span></span>

| <span data-ttu-id="76280-215">演算子</span><span class="sxs-lookup"><span data-stu-id="76280-215">Operator</span></span>            | <span data-ttu-id="76280-216">関数</span><span class="sxs-lookup"><span data-stu-id="76280-216">Function</span></span> |
| ------------------- | -------- |
| <code>&#124;</code> | <span data-ttu-id="76280-217">OR</span><span class="sxs-lookup"><span data-stu-id="76280-217">OR</span></span>       |
| `&`                 | <span data-ttu-id="76280-218">AND</span><span class="sxs-lookup"><span data-stu-id="76280-218">AND</span></span>      |

<span data-ttu-id="76280-219">条件演算子を使用する場合は、式をかっこで囲みます (例: `(Name~TestMethod1) | (Name~TestMethod2)`)。</span><span class="sxs-lookup"><span data-stu-id="76280-219">You can enclose expressions in parenthesis when using conditional operators (for example, `(Name~TestMethod1) | (Name~TestMethod2)`).</span></span>

<span data-ttu-id="76280-220">選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](../testing/selective-unit-tests.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="76280-220">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="76280-221">関連項目</span><span class="sxs-lookup"><span data-stu-id="76280-221">See also</span></span>

* [<span data-ttu-id="76280-222">フレームワークとターゲット</span><span class="sxs-lookup"><span data-stu-id="76280-222">Frameworks and Targets</span></span>](../../standard/frameworks.md)  
* [<span data-ttu-id="76280-223">.NET Core のランタイム識別子 (RID) のカタログ</span><span class="sxs-lookup"><span data-stu-id="76280-223">.NET Core Runtime IDentifier (RID) catalog</span></span>](../rid-catalog.md)
