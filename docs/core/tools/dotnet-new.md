---
title: dotnet new コマンド - .NET Core CLI
description: dotnet new コマンドは、指定されたテンプレートに基づいて新しい .NET Core プロジェクトを作成します。
author: mairaw
ms.author: mairaw
ms.date: 07/31/2018
ms.openlocfilehash: 396c4ddf09854fa4582226bdb1422f8c929e459b
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2018
ms.locfileid: "47208634"
---
# <a name="dotnet-new"></a><span data-ttu-id="15337-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="15337-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="15337-104">name</span><span class="sxs-lookup"><span data-stu-id="15337-104">Name</span></span>

<span data-ttu-id="15337-105">`dotnet new` - 指定したテンプレートに基づいて、新しいプロジェクト、構成ファイル、またはソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="15337-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="15337-106">構文</span><span class="sxs-lookup"><span data-stu-id="15337-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="15337-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="15337-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="15337-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="15337-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="15337-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="15337-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="15337-110">説明</span><span class="sxs-lookup"><span data-stu-id="15337-110">Description</span></span>

<span data-ttu-id="15337-111">`dotnet new` コマンドは、有効な .NET Core プロジェクトを初期化する便利な手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="15337-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="15337-112">このコマンドは、[テンプレート エンジン](https://github.com/dotnet/templating)を呼び出し、指定されたテンプレートとオプションに基づいて、ディスク上に成果物を作成します。</span><span class="sxs-lookup"><span data-stu-id="15337-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="15337-113">引数</span><span class="sxs-lookup"><span data-stu-id="15337-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="15337-114">コマンドが呼び出されたときにインスタンス化するテンプレート。</span><span class="sxs-lookup"><span data-stu-id="15337-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="15337-115">各テンプレートには、渡すことができるオプションが存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="15337-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="15337-116">詳細については、[テンプレートのオプション](#template-options)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="15337-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="15337-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="15337-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="15337-118">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="15337-118">The command contains a default list of templates.</span></span> <span data-ttu-id="15337-119">使用可能なテンプレートの一覧を取得するには、`dotnet new -l` を使います。</span><span class="sxs-lookup"><span data-stu-id="15337-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="15337-120">次の表は、.NET Core SDK 2.1.300 にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="15337-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="15337-121">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="15337-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="15337-122">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="15337-122">Template description</span></span>                          | <span data-ttu-id="15337-123">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="15337-123">Template name</span></span>   | <span data-ttu-id="15337-124">言語</span><span class="sxs-lookup"><span data-stu-id="15337-124">Languages</span></span>     |
|----------------------------------------------|-----------------|---------------|
| <span data-ttu-id="15337-125">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="15337-125">Console application</span></span>                          | `console`       | <span data-ttu-id="15337-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="15337-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="15337-127">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="15337-127">Class library</span></span>                                | `classlib`      | <span data-ttu-id="15337-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="15337-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="15337-129">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="15337-129">Unit test project</span></span>                            | `mstest`        | <span data-ttu-id="15337-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="15337-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="15337-131">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="15337-131">xUnit test project</span></span>                           | `xunit`         | <span data-ttu-id="15337-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="15337-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="15337-133">Razor ページ</span><span class="sxs-lookup"><span data-stu-id="15337-133">Razor page</span></span>                                   | `page`          | <span data-ttu-id="15337-134">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-134">[C#]</span></span>          |
| <span data-ttu-id="15337-135">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="15337-135">MVC ViewImports</span></span>                              | `viewimports`   | <span data-ttu-id="15337-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-136">[C#]</span></span>          |
| <span data-ttu-id="15337-137">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="15337-137">MVC ViewStart</span></span>                                | `viewstart`     | <span data-ttu-id="15337-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-138">[C#]</span></span>          |
| <span data-ttu-id="15337-139">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="15337-139">ASP.NET Core empty</span></span>                           | `web`           | <span data-ttu-id="15337-140">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="15337-140">[C#], F#</span></span>      |
| <span data-ttu-id="15337-141">ASP.NET Core Web アプリ (モデル ビュー コントローラー)</span><span class="sxs-lookup"><span data-stu-id="15337-141">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`           | <span data-ttu-id="15337-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="15337-142">[C#], F#</span></span>      |
| <span data-ttu-id="15337-143">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="15337-143">ASP.NET Core Web App</span></span>                         | `razor`         | <span data-ttu-id="15337-144">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-144">[C#]</span></span>          |
| <span data-ttu-id="15337-145">Angular 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="15337-145">ASP.NET Core with Angular</span></span>                    | `angular`       | <span data-ttu-id="15337-146">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-146">[C#]</span></span>          |
| <span data-ttu-id="15337-147">React.js 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="15337-147">ASP.NET Core with React.js</span></span>                   | `react`         | <span data-ttu-id="15337-148">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-148">[C#]</span></span>          |
| <span data-ttu-id="15337-149">React.js および Redux 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="15337-149">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`    | <span data-ttu-id="15337-150">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-150">[C#]</span></span>          |
| <span data-ttu-id="15337-151">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="15337-151">ASP.NET Core Web API</span></span>                         | `webapi`        | <span data-ttu-id="15337-152">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="15337-152">[C#], F#</span></span>      |
| <span data-ttu-id="15337-153">Razor クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="15337-153">Razor class library</span></span>                          | `razorclasslib` | <span data-ttu-id="15337-154">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-154">[C#]</span></span>          |
| <span data-ttu-id="15337-155">global.json file</span><span class="sxs-lookup"><span data-stu-id="15337-155">global.json file</span></span>                             | `globaljson`    |               |
| <span data-ttu-id="15337-156">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="15337-156">NuGet config</span></span>                                 | `nugetconfig`   |               |
| <span data-ttu-id="15337-157">Web 構成</span><span class="sxs-lookup"><span data-stu-id="15337-157">Web config</span></span>                                   | `webconfig`     |               |
| <span data-ttu-id="15337-158">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="15337-158">Solution file</span></span>                                | `sln`           |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="15337-159">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="15337-159">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="15337-160">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="15337-160">The command contains a default list of templates.</span></span> <span data-ttu-id="15337-161">使用可能なテンプレートの一覧を取得するには、`dotnet new -l` を使います。</span><span class="sxs-lookup"><span data-stu-id="15337-161">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="15337-162">次の表は、.NET Core SDK 2.0 にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="15337-162">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="15337-163">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="15337-163">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="15337-164">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="15337-164">Template description</span></span>                          | <span data-ttu-id="15337-165">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="15337-165">Template name</span></span> | <span data-ttu-id="15337-166">言語</span><span class="sxs-lookup"><span data-stu-id="15337-166">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="15337-167">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="15337-167">Console application</span></span>                          | `console`     | <span data-ttu-id="15337-168">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="15337-168">[C#], F#, VB</span></span>  |
| <span data-ttu-id="15337-169">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="15337-169">Class library</span></span>                                | `classlib`    | <span data-ttu-id="15337-170">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="15337-170">[C#], F#, VB</span></span>  |
| <span data-ttu-id="15337-171">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="15337-171">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="15337-172">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="15337-172">[C#], F#, VB</span></span>  |
| <span data-ttu-id="15337-173">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="15337-173">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="15337-174">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="15337-174">[C#], F#, VB</span></span>  |
| <span data-ttu-id="15337-175">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="15337-175">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="15337-176">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="15337-176">[C#], F#</span></span>      |
| <span data-ttu-id="15337-177">ASP.NET Core Web アプリ (モデル ビュー コントローラー)</span><span class="sxs-lookup"><span data-stu-id="15337-177">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="15337-178">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="15337-178">[C#], F#</span></span>      |
| <span data-ttu-id="15337-179">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="15337-179">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="15337-180">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-180">[C#]</span></span>          |
| <span data-ttu-id="15337-181">Angular 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="15337-181">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="15337-182">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-182">[C#]</span></span>          |
| <span data-ttu-id="15337-183">React.js 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="15337-183">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="15337-184">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-184">[C#]</span></span>          |
| <span data-ttu-id="15337-185">React.js および Redux 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="15337-185">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="15337-186">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-186">[C#]</span></span>          |
| <span data-ttu-id="15337-187">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="15337-187">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="15337-188">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="15337-188">[C#], F#</span></span>      |
| <span data-ttu-id="15337-189">global.json file</span><span class="sxs-lookup"><span data-stu-id="15337-189">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="15337-190">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="15337-190">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="15337-191">Web 構成</span><span class="sxs-lookup"><span data-stu-id="15337-191">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="15337-192">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="15337-192">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="15337-193">Razor ページ</span><span class="sxs-lookup"><span data-stu-id="15337-193">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="15337-194">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="15337-194">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="15337-195">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="15337-195">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="15337-196">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="15337-196">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="15337-197">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="15337-197">The command contains a default list of templates.</span></span> <span data-ttu-id="15337-198">使用可能なテンプレートの一覧を取得するには、`dotnet new -all` を使います。</span><span class="sxs-lookup"><span data-stu-id="15337-198">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="15337-199">次の表は、.NET Core SDK 1.x にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="15337-199">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="15337-200">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="15337-200">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="15337-201">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="15337-201">Template description</span></span>  | <span data-ttu-id="15337-202">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="15337-202">Template name</span></span> | <span data-ttu-id="15337-203">言語</span><span class="sxs-lookup"><span data-stu-id="15337-203">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="15337-204">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="15337-204">Console application</span></span>  | `console`     | <span data-ttu-id="15337-205">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="15337-205">[C#], F#</span></span>  |
| <span data-ttu-id="15337-206">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="15337-206">Class library</span></span>        | `classlib`    | <span data-ttu-id="15337-207">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="15337-207">[C#], F#</span></span>  |
| <span data-ttu-id="15337-208">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="15337-208">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="15337-209">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="15337-209">[C#], F#</span></span>  |
| <span data-ttu-id="15337-210">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="15337-210">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="15337-211">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="15337-211">[C#], F#</span></span>  |
| <span data-ttu-id="15337-212">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="15337-212">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="15337-213">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-213">[C#]</span></span>      |
| <span data-ttu-id="15337-214">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="15337-214">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="15337-215">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="15337-215">[C#], F#</span></span>  |
| <span data-ttu-id="15337-216">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="15337-216">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="15337-217">[C#]</span><span class="sxs-lookup"><span data-stu-id="15337-217">[C#]</span></span>      |
| <span data-ttu-id="15337-218">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="15337-218">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="15337-219">Web 構成</span><span class="sxs-lookup"><span data-stu-id="15337-219">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="15337-220">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="15337-220">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="15337-221">オプション</span><span class="sxs-lookup"><span data-stu-id="15337-221">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="15337-222">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="15337-222">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="15337-223">既存のファイルを変更する場合でも、コンテンツが強制的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="15337-223">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="15337-224">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="15337-224">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="15337-225">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="15337-225">Prints out help for the command.</span></span> <span data-ttu-id="15337-226">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="15337-226">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="15337-227">指定された `PATH` または `NUGET_ID` からソース パックまたはテンプレート パックをインストールします。</span><span class="sxs-lookup"><span data-stu-id="15337-227">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="15337-228">テンプレート パッケージのプレリリース版をインストールする場合は、`<package-name>::<package-version>` の形式でバージョンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15337-228">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="15337-229">既定では、`dotnet new` は、バージョンに対して \* を渡します。これは最後の安定したパッケージのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="15337-229">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="15337-230">「[使用例](#examples)」のセクションで、例をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="15337-230">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="15337-231">カスタム テンプレートの作成方法については、[「dotnet new のカスタム テンプレート」](custom-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="15337-231">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="15337-232">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="15337-232">Lists templates containing the specified name.</span></span> <span data-ttu-id="15337-233">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="15337-233">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="15337-234">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="15337-234">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="15337-235">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="15337-235">The language of the template to create.</span></span> <span data-ttu-id="15337-236">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="15337-236">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="15337-237">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="15337-237">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="15337-238">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="15337-238">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="15337-239">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="15337-239">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="15337-240">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="15337-240">The name for the created output.</span></span> <span data-ttu-id="15337-241">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-241">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="15337-242">インストール中に使用する NuGet ソースを 1 つ指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-242">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="15337-243">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="15337-243">Location to place the generated output.</span></span> <span data-ttu-id="15337-244">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="15337-244">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="15337-245">使用可能な種類に基づいて、テンプレートをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="15337-245">Filters templates based on available types.</span></span> <span data-ttu-id="15337-246">定義済みの値は、"project"、"item"、または "other" です。</span><span class="sxs-lookup"><span data-stu-id="15337-246">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="15337-247">指定された `PATH` または `NUGET_ID` で、ソース パックまたはテンプレート パックをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="15337-247">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="15337-248">`PATH` を使用してテンプレートをアンインストールするには、完全修飾パスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15337-248">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="15337-249">たとえば、*C:/Users/\<ユーザー>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* は有効ですが、*./GarciaSoftware.ConsoleTemplate.CSharp* が含まれるフォルダーから、そのパスを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="15337-249">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="15337-250">また、テンプレートのパスの最後にある終端ディレクトリのスラッシュは含めないでください。</span><span class="sxs-lookup"><span data-stu-id="15337-250">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="15337-251">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="15337-251">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="15337-252">既存のファイルを変更する場合でも、コンテンツが強制的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="15337-252">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="15337-253">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="15337-253">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="15337-254">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="15337-254">Prints out help for the command.</span></span> <span data-ttu-id="15337-255">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="15337-255">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="15337-256">指定された `PATH` または `NUGET_ID` からソース パックまたはテンプレート パックをインストールします。</span><span class="sxs-lookup"><span data-stu-id="15337-256">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="15337-257">テンプレート パッケージのプレリリース版をインストールする場合は、`<package-name>::<package-version>` の形式でバージョンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15337-257">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="15337-258">既定では、`dotnet new` は、バージョンに対して \* を渡します。これは最後の安定したパッケージのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="15337-258">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="15337-259">「[使用例](#examples)」のセクションで、例をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="15337-259">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="15337-260">カスタム テンプレートの作成方法については、[「dotnet new のカスタム テンプレート」](custom-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="15337-260">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="15337-261">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="15337-261">Lists templates containing the specified name.</span></span> <span data-ttu-id="15337-262">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="15337-262">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="15337-263">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="15337-263">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="15337-264">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="15337-264">The language of the template to create.</span></span> <span data-ttu-id="15337-265">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="15337-265">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="15337-266">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="15337-266">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="15337-267">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="15337-267">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="15337-268">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="15337-268">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="15337-269">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="15337-269">The name for the created output.</span></span> <span data-ttu-id="15337-270">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-270">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="15337-271">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="15337-271">Location to place the generated output.</span></span> <span data-ttu-id="15337-272">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="15337-272">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="15337-273">使用可能な種類に基づいて、テンプレートをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="15337-273">Filters templates based on available types.</span></span> <span data-ttu-id="15337-274">定義済みの値は、"project"、"item"、または "other" です。</span><span class="sxs-lookup"><span data-stu-id="15337-274">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="15337-275">指定された `PATH` または `NUGET_ID` で、ソース パックまたはテンプレート パックをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="15337-275">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="15337-276">ソース `PATH` を使用してテンプレートをアンインストールするには、完全修飾パスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15337-276">To uninstall a template using a source `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="15337-277">たとえば、*C:/Users/\<ユーザー>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* は有効ですが、*./GarciaSoftware.ConsoleTemplate.CSharp* が含まれるフォルダーから、そのパスを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="15337-277">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span> <span data-ttu-id="15337-278">また、テンプレートのパスの最後にある終端ディレクトリのスラッシュは含めないでください。</span><span class="sxs-lookup"><span data-stu-id="15337-278">Additionally, do not include a final terminating directory slash on your template path.</span></span>
> 
> <span data-ttu-id="15337-279">テンプレートのアンインストールに必要な `PATH` または `NUGET_ID` 引数を決定できない場合、引数なしで `dotnet new --uninstall` を実行するとインストールされているすべてのテンプレートと、それをアンインストールするために必要な引数が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="15337-279">If you are unable to determine the `PATH` or `NUGET_ID` argument needed to uninstall a template, running `dotnet new --uninstall` without an argument will list all installed templates and the argument required to uninstall them.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="15337-280">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="15337-280">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="15337-281">`dotnet new` コマンドのコンテキストでのみ実行すると、特定の種類のプロジェクトに対するすべてのテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="15337-281">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="15337-282">`dotnet new web -all` など、特定のテンプレートのコンテキストで実行すると、`-all` は強制作成フラグとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="15337-282">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="15337-283">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="15337-283">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="15337-284">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="15337-284">Prints out help for the command.</span></span> <span data-ttu-id="15337-285">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="15337-285">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="15337-286">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="15337-286">Lists templates containing the specified name.</span></span> <span data-ttu-id="15337-287">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="15337-287">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="15337-288">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="15337-288">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="15337-289">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="15337-289">The language of the template to create.</span></span> <span data-ttu-id="15337-290">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="15337-290">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="15337-291">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="15337-291">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="15337-292">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="15337-292">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="15337-293">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="15337-293">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="15337-294">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="15337-294">The name for the created output.</span></span> <span data-ttu-id="15337-295">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-295">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="15337-296">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="15337-296">Location to place the generated output.</span></span> <span data-ttu-id="15337-297">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="15337-297">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="15337-298">テンプレート オプション</span><span class="sxs-lookup"><span data-stu-id="15337-298">Template options</span></span>

<span data-ttu-id="15337-299">プロジェクト テンプレートはそれぞれ、追加のオプションが与えられている場合があります。</span><span class="sxs-lookup"><span data-stu-id="15337-299">Each project template may have additional options available.</span></span> <span data-ttu-id="15337-300">コア テンプレートの場合、次のオプションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="15337-300">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="15337-301">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="15337-301">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="15337-302">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="15337-302">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="15337-303">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-303">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-304">**classlib**</span><span class="sxs-lookup"><span data-stu-id="15337-304">**classlib**</span></span>

<span data-ttu-id="15337-305">`-f|--framework <FRAMEWORK>` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-305">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="15337-306">値: .NET Core クラス ライブラリを作成するには `netcoreapp2.0`、.NET 標準クラス ライブラリを作成するには `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="15337-306">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="15337-307">既定値は `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="15337-307">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="15337-308">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-308">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-309">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="15337-309">**mstest, xunit**</span></span>

<span data-ttu-id="15337-310">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md) を使用してプロジェクトのパッケージ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="15337-310">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="15337-311">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-311">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-312">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="15337-312">**globaljson**</span></span>

<span data-ttu-id="15337-313">`--sdk-version <VERSION_NUMBER>` - *global.json* ファイル内で使用する .NET Core SDK のバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-313">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="15337-314">**web**</span><span class="sxs-lookup"><span data-stu-id="15337-314">**web**</span></span>

<span data-ttu-id="15337-315">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="15337-315">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="15337-316">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-316">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-317">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="15337-317">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="15337-318">このオプションは、`IndividualAuth` または `OrganizationalAuth` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-318">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="15337-319">**webapi**</span><span class="sxs-lookup"><span data-stu-id="15337-319">**webapi**</span></span>

<span data-ttu-id="15337-320">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="15337-320">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="15337-321">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="15337-321">The possible values are:</span></span>

- <span data-ttu-id="15337-322">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="15337-322">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="15337-323">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="15337-323">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="15337-324">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="15337-324">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="15337-325">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="15337-325">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="15337-326">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="15337-326">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="15337-327">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-327">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="15337-328">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="15337-328">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="15337-329">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-329">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="15337-330">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-330">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-331">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="15337-331">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="15337-332">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-332">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="15337-333">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="15337-333">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="15337-334">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-334">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="15337-335">`IndividualB2C` 認証または `SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-335">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="15337-336">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="15337-336">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="15337-337">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="15337-337">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="15337-338">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-338">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="15337-339">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="15337-339">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="15337-340">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-340">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="15337-341">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-341">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="15337-342">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="15337-342">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="15337-343">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="15337-343">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="15337-344">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-344">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="15337-345">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="15337-345">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="15337-346">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-346">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="15337-347">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-347">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-348">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-348">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-349">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="15337-349">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="15337-350">`app.UseHsts` と `app.UseHttpsRedirection` は `Startup.Configure` に追加されません。</span><span class="sxs-lookup"><span data-stu-id="15337-350">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="15337-351">このオプションは、`Individual`、`IndividualB2C`、`SingleOrg`、または `MultiOrg` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-351">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="15337-352">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="15337-352">**mvc, razor**</span></span>

<span data-ttu-id="15337-353">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="15337-353">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="15337-354">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="15337-354">The possible values are:</span></span>

- <span data-ttu-id="15337-355">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="15337-355">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="15337-356">`Individual` - 個別認証です。</span><span class="sxs-lookup"><span data-stu-id="15337-356">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="15337-357">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="15337-357">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="15337-358">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="15337-358">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="15337-359">`MultiOrg` - 複数のテナントに対する組織認証です。</span><span class="sxs-lookup"><span data-stu-id="15337-359">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="15337-360">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="15337-360">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="15337-361">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="15337-361">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="15337-362">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-362">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="15337-363">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="15337-363">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="15337-364">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-364">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="15337-365">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-365">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-366">`-rp|--reset-password-policy-id <ID>` - このプロジェクトのリセット パスワード ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-366">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="15337-367">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-367">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-368">`-ep|--edit-profile-policy-id <ID>` - このプロジェクトの編集プロファイル ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-368">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="15337-369">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-369">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-370">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="15337-370">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="15337-371">`SingleOrg` 認証または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-371">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="15337-372">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="15337-372">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="15337-373">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-373">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="15337-374">`IndividualB2C` 認証、`SingleOrg` 認証、または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-374">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="15337-375">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="15337-375">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="15337-376">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="15337-376">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="15337-377">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-377">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="15337-378">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="15337-378">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="15337-379">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-379">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="15337-380">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-380">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="15337-381">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="15337-381">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="15337-382">`--callback-path <PATH>` - リダイレクト URI のアプリケーションの基本パス内の要求パスです。</span><span class="sxs-lookup"><span data-stu-id="15337-382">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="15337-383">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-383">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="15337-384">既定値は `/signin-oidc` です。</span><span class="sxs-lookup"><span data-stu-id="15337-384">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="15337-385">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="15337-385">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="15337-386">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-386">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="15337-387">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="15337-387">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="15337-388">`--use-browserlink` - プロジェクトに BrowserLink を含めます。</span><span class="sxs-lookup"><span data-stu-id="15337-388">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="15337-389">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-389">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="15337-390">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-390">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-391">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-391">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-392">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="15337-392">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="15337-393">`app.UseHsts` と `app.UseHttpsRedirection` は `Startup.Configure` に追加されません。</span><span class="sxs-lookup"><span data-stu-id="15337-393">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="15337-394">このオプションは、`Individual`、`IndividualB2C`、`SingleOrg`、または `MultiOrg` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-394">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="15337-395">**page**</span><span class="sxs-lookup"><span data-stu-id="15337-395">**page**</span></span>

<span data-ttu-id="15337-396">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="15337-396">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="15337-397">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="15337-397">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="15337-398">`-np|--no-pagemodel` - PageModel なしでページを作成します。</span><span class="sxs-lookup"><span data-stu-id="15337-398">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="15337-399">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="15337-399">**viewimports**</span></span>

<span data-ttu-id="15337-400">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="15337-400">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="15337-401">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="15337-401">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="15337-402">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="15337-402">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="15337-403">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="15337-403">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="15337-404">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-404">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-405">**classlib**</span><span class="sxs-lookup"><span data-stu-id="15337-405">**classlib**</span></span>

<span data-ttu-id="15337-406">`-f|--framework <FRAMEWORK>` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-406">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="15337-407">値: .NET Core クラス ライブラリを作成するには `netcoreapp2.0`、.NET 標準クラス ライブラリを作成するには `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="15337-407">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="15337-408">既定値は `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="15337-408">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="15337-409">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-409">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-410">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="15337-410">**mstest, xunit**</span></span>

<span data-ttu-id="15337-411">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md) を使用してプロジェクトのパッケージ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="15337-411">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="15337-412">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-412">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-413">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="15337-413">**globaljson**</span></span>

<span data-ttu-id="15337-414">`--sdk-version <VERSION_NUMBER>` - *global.json* ファイル内で使用する .NET Core SDK のバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-414">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="15337-415">**web**</span><span class="sxs-lookup"><span data-stu-id="15337-415">**web**</span></span>

<span data-ttu-id="15337-416">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="15337-416">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="15337-417">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-417">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-418">**webapi**</span><span class="sxs-lookup"><span data-stu-id="15337-418">**webapi**</span></span>

<span data-ttu-id="15337-419">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="15337-419">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="15337-420">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="15337-420">The possible values are:</span></span>

- <span data-ttu-id="15337-421">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="15337-421">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="15337-422">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="15337-422">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="15337-423">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="15337-423">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="15337-424">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="15337-424">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="15337-425">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="15337-425">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="15337-426">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-426">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="15337-427">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="15337-427">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="15337-428">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-428">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="15337-429">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-429">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-430">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="15337-430">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="15337-431">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-431">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="15337-432">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="15337-432">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="15337-433">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-433">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="15337-434">`IndividualB2C` 認証または `SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-434">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="15337-435">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="15337-435">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="15337-436">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="15337-436">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="15337-437">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-437">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="15337-438">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="15337-438">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="15337-439">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-439">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="15337-440">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-440">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="15337-441">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="15337-441">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="15337-442">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="15337-442">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="15337-443">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-443">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="15337-444">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="15337-444">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="15337-445">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-445">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="15337-446">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-446">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-447">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-447">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-448">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="15337-448">**mvc, razor**</span></span>

<span data-ttu-id="15337-449">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="15337-449">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="15337-450">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="15337-450">The possible values are:</span></span>

- <span data-ttu-id="15337-451">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="15337-451">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="15337-452">`Individual` - 個別認証です。</span><span class="sxs-lookup"><span data-stu-id="15337-452">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="15337-453">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="15337-453">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="15337-454">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="15337-454">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="15337-455">`MultiOrg` - 複数のテナントに対する組織認証です。</span><span class="sxs-lookup"><span data-stu-id="15337-455">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="15337-456">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="15337-456">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="15337-457">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="15337-457">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="15337-458">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-458">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="15337-459">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="15337-459">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="15337-460">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-460">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="15337-461">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-461">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-462">`-rp|--reset-password-policy-id <ID>` - このプロジェクトのリセット パスワード ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-462">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="15337-463">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-463">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-464">`-ep|--edit-profile-policy-id <ID>` - このプロジェクトの編集プロファイル ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-464">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="15337-465">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-465">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-466">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="15337-466">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="15337-467">`SingleOrg` 認証または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-467">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="15337-468">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="15337-468">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="15337-469">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-469">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="15337-470">`IndividualB2C` 認証、`SingleOrg` 認証、または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-470">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="15337-471">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="15337-471">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="15337-472">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="15337-472">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="15337-473">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-473">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="15337-474">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="15337-474">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="15337-475">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="15337-475">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="15337-476">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-476">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="15337-477">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="15337-477">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="15337-478">`--callback-path <PATH>` - リダイレクト URI のアプリケーションの基本パス内の要求パスです。</span><span class="sxs-lookup"><span data-stu-id="15337-478">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="15337-479">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="15337-479">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="15337-480">既定値は `/signin-oidc` です。</span><span class="sxs-lookup"><span data-stu-id="15337-480">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="15337-481">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="15337-481">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="15337-482">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-482">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="15337-483">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="15337-483">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="15337-484">`--use-browserlink` - プロジェクトに BrowserLink を含めます。</span><span class="sxs-lookup"><span data-stu-id="15337-484">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="15337-485">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-485">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="15337-486">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15337-486">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="15337-487">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="15337-487">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="15337-488">**page**</span><span class="sxs-lookup"><span data-stu-id="15337-488">**page**</span></span>

<span data-ttu-id="15337-489">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="15337-489">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="15337-490">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="15337-490">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="15337-491">`-np|--no-pagemodel` - PageModel なしでページを作成します。</span><span class="sxs-lookup"><span data-stu-id="15337-491">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="15337-492">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="15337-492">**viewimports**</span></span>

<span data-ttu-id="15337-493">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="15337-493">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="15337-494">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="15337-494">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="15337-495">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="15337-495">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="15337-496">**console、xunit、mstest、web、webapi**</span><span class="sxs-lookup"><span data-stu-id="15337-496">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="15337-497">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-497">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="15337-498">値: `netcoreapp1.0` または `netcoreapp1.1` です。</span><span class="sxs-lookup"><span data-stu-id="15337-498">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="15337-499">既定値は `netcoreapp1.0` です。</span><span class="sxs-lookup"><span data-stu-id="15337-499">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="15337-500">**classlib**</span><span class="sxs-lookup"><span data-stu-id="15337-500">**classlib**</span></span>

<span data-ttu-id="15337-501">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-501">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="15337-502">値: `netcoreapp1.0`、`netcoreapp1.1`、または `netstandard1.0` から `netstandard1.6` です。</span><span class="sxs-lookup"><span data-stu-id="15337-502">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="15337-503">既定値は `netstandard1.4` です。</span><span class="sxs-lookup"><span data-stu-id="15337-503">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="15337-504">**mvc**</span><span class="sxs-lookup"><span data-stu-id="15337-504">**mvc**</span></span>

<span data-ttu-id="15337-505">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-505">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="15337-506">値: `netcoreapp1.0` または `netcoreapp1.1` です。</span><span class="sxs-lookup"><span data-stu-id="15337-506">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="15337-507">既定値は `netcoreapp1.0` です。</span><span class="sxs-lookup"><span data-stu-id="15337-507">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="15337-508">`-au|--auth` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="15337-508">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="15337-509">値: `None` または `Individual` です。</span><span class="sxs-lookup"><span data-stu-id="15337-509">Values: `None` or `Individual`.</span></span> <span data-ttu-id="15337-510">既定値は `None` です。</span><span class="sxs-lookup"><span data-stu-id="15337-510">The default value is `None`.</span></span>

<span data-ttu-id="15337-511">`-uld|--use-local-db` - SQLite の代わりに LocalDB を使うかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="15337-511">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="15337-512">値: `true` または `false` です。</span><span class="sxs-lookup"><span data-stu-id="15337-512">Values: `true` or `false`.</span></span> <span data-ttu-id="15337-513">既定値は `false` です。</span><span class="sxs-lookup"><span data-stu-id="15337-513">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="15337-514">使用例</span><span class="sxs-lookup"><span data-stu-id="15337-514">Examples</span></span>

<span data-ttu-id="15337-515">現在のディレクトリに、F# コンソール アプリケーション プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="15337-515">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="15337-516">指定したディレクトリ内に .NET 標準クラス ライブラリ プロジェクトを作成します (.NET Core SDK 2.0 またはそれ以降のバージョンでのみ使用可能)。</span><span class="sxs-lookup"><span data-stu-id="15337-516">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="15337-517">認証なしで、現在のディレクトリに新しい ASP.NET Core C# MVC アプリケーション プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="15337-517">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="15337-518">新しい xUnit アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="15337-518">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="15337-519">MVC に利用できるすべてのテンプレートを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="15337-519">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="15337-520">ASP.NET Core のシングル ページ アプリケーション テンプレートのバージョン 2.0 をインストールします (コマンド オプションは .NET Core SDK 1.1 以降のバージョンでのみ使用できます):</span><span class="sxs-lookup"><span data-stu-id="15337-520">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="15337-521">SDK バージョン 2.0.0 (.NET Core SDK 2.0 以降のバージョンでのみ使用できます) を設定している現在のディレクトリ内に *global.json* を作成します。</span><span class="sxs-lookup"><span data-stu-id="15337-521">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="15337-522">関連項目</span><span class="sxs-lookup"><span data-stu-id="15337-522">See also</span></span>

* [<span data-ttu-id="15337-523">dotnet new のカスタム テンプレート</span><span class="sxs-lookup"><span data-stu-id="15337-523">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="15337-524">dotnet new のカスタム テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="15337-524">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* [<span data-ttu-id="15337-525">dotnet/dotnet-template-samples GitHub リポジトリ</span><span class="sxs-lookup"><span data-stu-id="15337-525">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)  
* [<span data-ttu-id="15337-526">dotnet new で使用できるテンプレート</span><span class="sxs-lookup"><span data-stu-id="15337-526">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
