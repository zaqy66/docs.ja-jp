---
title: dotnet new コマンド - .NET Core CLI
description: dotnet new コマンドは、指定されたテンプレートに基づいて新しい .NET Core プロジェクトを作成します。
author: mairaw
ms.author: mairaw
ms.date: 10/24/2018
ms.openlocfilehash: 56d76f1dd54097f9cf20129d74057235290c273c
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188204"
---
# <a name="dotnet-new"></a><span data-ttu-id="4ec00-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="4ec00-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="4ec00-104">name</span><span class="sxs-lookup"><span data-stu-id="4ec00-104">Name</span></span>

<span data-ttu-id="4ec00-105">`dotnet new` - 指定したテンプレートに基づいて、新しいプロジェクト、構成ファイル、またはソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="4ec00-106">構文</span><span class="sxs-lookup"><span data-stu-id="4ec00-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="4ec00-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="4ec00-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="4ec00-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="4ec00-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="4ec00-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="4ec00-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="4ec00-110">説明</span><span class="sxs-lookup"><span data-stu-id="4ec00-110">Description</span></span>

<span data-ttu-id="4ec00-111">`dotnet new` コマンドは、有効な .NET Core プロジェクトを初期化する便利な手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="4ec00-112">このコマンドは、[テンプレート エンジン](https://github.com/dotnet/templating)を呼び出し、指定されたテンプレートとオプションに基づいて、ディスク上に成果物を作成します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="4ec00-113">引数</span><span class="sxs-lookup"><span data-stu-id="4ec00-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="4ec00-114">コマンドが呼び出されたときにインスタンス化するテンプレート。</span><span class="sxs-lookup"><span data-stu-id="4ec00-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="4ec00-115">各テンプレートには、渡すことができるオプションが存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="4ec00-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="4ec00-116">詳細については、[テンプレートのオプション](#template-options)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ec00-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="4ec00-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="4ec00-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="4ec00-118">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4ec00-118">The command contains a default list of templates.</span></span> <span data-ttu-id="4ec00-119">使用可能なテンプレートの一覧を取得するには、`dotnet new -l` を使います。</span><span class="sxs-lookup"><span data-stu-id="4ec00-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="4ec00-120">次の表は、.NET Core SDK 2.1.300 にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="4ec00-121">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="4ec00-122">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="4ec00-122">Template description</span></span>                          | <span data-ttu-id="4ec00-123">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="4ec00-123">Template name</span></span>    | <span data-ttu-id="4ec00-124">言語</span><span class="sxs-lookup"><span data-stu-id="4ec00-124">Languages</span></span>     |
|----------------------------------------------|------------------|---------------|
| <span data-ttu-id="4ec00-125">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="4ec00-125">Console application</span></span>                          | `console`        | <span data-ttu-id="4ec00-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="4ec00-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="4ec00-127">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="4ec00-127">Class library</span></span>                                | `classlib`       | <span data-ttu-id="4ec00-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="4ec00-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="4ec00-129">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="4ec00-129">Unit test project</span></span>                            | `mstest`         | <span data-ttu-id="4ec00-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="4ec00-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="4ec00-131">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="4ec00-131">xUnit test project</span></span>                           | `xunit`          | <span data-ttu-id="4ec00-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="4ec00-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="4ec00-133">Razor ページ</span><span class="sxs-lookup"><span data-stu-id="4ec00-133">Razor page</span></span>                                   | `page`           | <span data-ttu-id="4ec00-134">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-134">[C#]</span></span>          |
| <span data-ttu-id="4ec00-135">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="4ec00-135">MVC ViewImports</span></span>                              | `viewimports`    | <span data-ttu-id="4ec00-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-136">[C#]</span></span>          |
| <span data-ttu-id="4ec00-137">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="4ec00-137">MVC ViewStart</span></span>                                | `viewstart`      | <span data-ttu-id="4ec00-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-138">[C#]</span></span>          |
| <span data-ttu-id="4ec00-139">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="4ec00-139">ASP.NET Core empty</span></span>                           | `web`            | <span data-ttu-id="4ec00-140">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="4ec00-140">[C#], F#</span></span>      |
| <span data-ttu-id="4ec00-141">ASP.NET Core Web アプリ (モデル ビュー コントローラー)</span><span class="sxs-lookup"><span data-stu-id="4ec00-141">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`            | <span data-ttu-id="4ec00-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="4ec00-142">[C#], F#</span></span>      |
| <span data-ttu-id="4ec00-143">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="4ec00-143">ASP.NET Core Web App</span></span>                         | <span data-ttu-id="4ec00-144">`razor`、 `webapp`</span><span class="sxs-lookup"><span data-stu-id="4ec00-144">`razor`, `webapp`</span></span>| <span data-ttu-id="4ec00-145">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-145">[C#]</span></span>          |
| <span data-ttu-id="4ec00-146">Angular 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="4ec00-146">ASP.NET Core with Angular</span></span>                    | `angular`        | <span data-ttu-id="4ec00-147">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-147">[C#]</span></span>          |
| <span data-ttu-id="4ec00-148">React.js 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="4ec00-148">ASP.NET Core with React.js</span></span>                   | `react`          | <span data-ttu-id="4ec00-149">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-149">[C#]</span></span>          |
| <span data-ttu-id="4ec00-150">React.js および Redux 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="4ec00-150">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`     | <span data-ttu-id="4ec00-151">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-151">[C#]</span></span>          |
| <span data-ttu-id="4ec00-152">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="4ec00-152">ASP.NET Core Web API</span></span>                         | `webapi`         | <span data-ttu-id="4ec00-153">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="4ec00-153">[C#], F#</span></span>      |
| <span data-ttu-id="4ec00-154">Razor クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="4ec00-154">Razor class library</span></span>                          | `razorclasslib`  | <span data-ttu-id="4ec00-155">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-155">[C#]</span></span>          |
| <span data-ttu-id="4ec00-156">global.json file</span><span class="sxs-lookup"><span data-stu-id="4ec00-156">global.json file</span></span>                             | `globaljson`     |               |
| <span data-ttu-id="4ec00-157">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="4ec00-157">NuGet config</span></span>                                 | `nugetconfig`    |               |
| <span data-ttu-id="4ec00-158">Web 構成</span><span class="sxs-lookup"><span data-stu-id="4ec00-158">Web config</span></span>                                   | `webconfig`      |               |
| <span data-ttu-id="4ec00-159">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="4ec00-159">Solution file</span></span>                                | `sln`            |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="4ec00-160">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="4ec00-160">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="4ec00-161">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4ec00-161">The command contains a default list of templates.</span></span> <span data-ttu-id="4ec00-162">使用可能なテンプレートの一覧を取得するには、`dotnet new -l` を使います。</span><span class="sxs-lookup"><span data-stu-id="4ec00-162">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="4ec00-163">次の表は、.NET Core SDK 2.0 にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-163">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="4ec00-164">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-164">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="4ec00-165">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="4ec00-165">Template description</span></span>                          | <span data-ttu-id="4ec00-166">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="4ec00-166">Template name</span></span> | <span data-ttu-id="4ec00-167">言語</span><span class="sxs-lookup"><span data-stu-id="4ec00-167">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="4ec00-168">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="4ec00-168">Console application</span></span>                          | `console`     | <span data-ttu-id="4ec00-169">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="4ec00-169">[C#], F#, VB</span></span>  |
| <span data-ttu-id="4ec00-170">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="4ec00-170">Class library</span></span>                                | `classlib`    | <span data-ttu-id="4ec00-171">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="4ec00-171">[C#], F#, VB</span></span>  |
| <span data-ttu-id="4ec00-172">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="4ec00-172">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="4ec00-173">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="4ec00-173">[C#], F#, VB</span></span>  |
| <span data-ttu-id="4ec00-174">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="4ec00-174">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="4ec00-175">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="4ec00-175">[C#], F#, VB</span></span>  |
| <span data-ttu-id="4ec00-176">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="4ec00-176">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="4ec00-177">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="4ec00-177">[C#], F#</span></span>      |
| <span data-ttu-id="4ec00-178">ASP.NET Core Web アプリ (モデル ビュー コントローラー)</span><span class="sxs-lookup"><span data-stu-id="4ec00-178">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="4ec00-179">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="4ec00-179">[C#], F#</span></span>      |
| <span data-ttu-id="4ec00-180">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="4ec00-180">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="4ec00-181">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-181">[C#]</span></span>          |
| <span data-ttu-id="4ec00-182">Angular 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="4ec00-182">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="4ec00-183">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-183">[C#]</span></span>          |
| <span data-ttu-id="4ec00-184">React.js 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="4ec00-184">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="4ec00-185">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-185">[C#]</span></span>          |
| <span data-ttu-id="4ec00-186">React.js および Redux 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="4ec00-186">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="4ec00-187">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-187">[C#]</span></span>          |
| <span data-ttu-id="4ec00-188">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="4ec00-188">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="4ec00-189">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="4ec00-189">[C#], F#</span></span>      |
| <span data-ttu-id="4ec00-190">global.json file</span><span class="sxs-lookup"><span data-stu-id="4ec00-190">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="4ec00-191">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="4ec00-191">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="4ec00-192">Web 構成</span><span class="sxs-lookup"><span data-stu-id="4ec00-192">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="4ec00-193">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="4ec00-193">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="4ec00-194">Razor ページ</span><span class="sxs-lookup"><span data-stu-id="4ec00-194">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="4ec00-195">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="4ec00-195">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="4ec00-196">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="4ec00-196">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="4ec00-197">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="4ec00-197">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="4ec00-198">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4ec00-198">The command contains a default list of templates.</span></span> <span data-ttu-id="4ec00-199">使用可能なテンプレートの一覧を取得するには、`dotnet new -all` を使います。</span><span class="sxs-lookup"><span data-stu-id="4ec00-199">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="4ec00-200">次の表は、.NET Core SDK 1.x にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-200">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="4ec00-201">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-201">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="4ec00-202">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="4ec00-202">Template description</span></span>  | <span data-ttu-id="4ec00-203">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="4ec00-203">Template name</span></span> | <span data-ttu-id="4ec00-204">言語</span><span class="sxs-lookup"><span data-stu-id="4ec00-204">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="4ec00-205">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="4ec00-205">Console application</span></span>  | `console`     | <span data-ttu-id="4ec00-206">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="4ec00-206">[C#], F#</span></span>  |
| <span data-ttu-id="4ec00-207">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="4ec00-207">Class library</span></span>        | `classlib`    | <span data-ttu-id="4ec00-208">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="4ec00-208">[C#], F#</span></span>  |
| <span data-ttu-id="4ec00-209">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="4ec00-209">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="4ec00-210">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="4ec00-210">[C#], F#</span></span>  |
| <span data-ttu-id="4ec00-211">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="4ec00-211">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="4ec00-212">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="4ec00-212">[C#], F#</span></span>  |
| <span data-ttu-id="4ec00-213">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="4ec00-213">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="4ec00-214">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-214">[C#]</span></span>      |
| <span data-ttu-id="4ec00-215">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="4ec00-215">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="4ec00-216">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="4ec00-216">[C#], F#</span></span>  |
| <span data-ttu-id="4ec00-217">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="4ec00-217">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="4ec00-218">[C#]</span><span class="sxs-lookup"><span data-stu-id="4ec00-218">[C#]</span></span>      |
| <span data-ttu-id="4ec00-219">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="4ec00-219">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="4ec00-220">Web 構成</span><span class="sxs-lookup"><span data-stu-id="4ec00-220">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="4ec00-221">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="4ec00-221">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="4ec00-222">オプション</span><span class="sxs-lookup"><span data-stu-id="4ec00-222">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="4ec00-223">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="4ec00-223">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="4ec00-224">既存のファイルを変更する場合でも、コンテンツが強制的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-224">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="4ec00-225">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-225">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="4ec00-226">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-226">Prints out help for the command.</span></span> <span data-ttu-id="4ec00-227">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-227">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="4ec00-228">指定された `PATH` または `NUGET_ID` からソース パックまたはテンプレート パックをインストールします。</span><span class="sxs-lookup"><span data-stu-id="4ec00-228">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="4ec00-229">テンプレート パッケージのプレリリース版をインストールする場合は、`<package-name>::<package-version>` の形式でバージョンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ec00-229">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="4ec00-230">既定では、`dotnet new` は、バージョンに対して \* を渡します。これは最後の安定したパッケージのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-230">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="4ec00-231">「[使用例](#examples)」のセクションで、例をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4ec00-231">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="4ec00-232">カスタム テンプレートの作成方法については、[「dotnet new のカスタム テンプレート」](custom-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ec00-232">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="4ec00-233">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-233">Lists templates containing the specified name.</span></span> <span data-ttu-id="4ec00-234">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-234">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="4ec00-235">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-235">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="4ec00-236">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="4ec00-236">The language of the template to create.</span></span> <span data-ttu-id="4ec00-237">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="4ec00-237">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="4ec00-238">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-238">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="4ec00-239">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-239">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="4ec00-240">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ec00-240">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="4ec00-241">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-241">The name for the created output.</span></span> <span data-ttu-id="4ec00-242">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-242">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="4ec00-243">インストール中に使用する NuGet ソースを 1 つ指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-243">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="4ec00-244">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="4ec00-244">Location to place the generated output.</span></span> <span data-ttu-id="4ec00-245">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-245">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="4ec00-246">使用可能な種類に基づいて、テンプレートをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-246">Filters templates based on available types.</span></span> <span data-ttu-id="4ec00-247">定義済みの値は、"project"、"item"、または "other" です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-247">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="4ec00-248">指定された `PATH` または `NUGET_ID` で、ソース パックまたはテンプレート パックをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="4ec00-248">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="4ec00-249">`PATH` を使用してテンプレートをアンインストールするには、完全修飾パスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ec00-249">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="4ec00-250">たとえば、*C:/Users/\<ユーザー>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* は有効ですが、*./GarciaSoftware.ConsoleTemplate.CSharp* が含まれるフォルダーから、そのパスを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-250">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="4ec00-251">また、テンプレートのパスの最後にある終端ディレクトリのスラッシュは含めないでください。</span><span class="sxs-lookup"><span data-stu-id="4ec00-251">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="4ec00-252">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="4ec00-252">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="4ec00-253">既存のファイルを変更する場合でも、コンテンツが強制的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-253">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="4ec00-254">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-254">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="4ec00-255">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-255">Prints out help for the command.</span></span> <span data-ttu-id="4ec00-256">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-256">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="4ec00-257">指定された `PATH` または `NUGET_ID` からソース パックまたはテンプレート パックをインストールします。</span><span class="sxs-lookup"><span data-stu-id="4ec00-257">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="4ec00-258">テンプレート パッケージのプレリリース版をインストールする場合は、`<package-name>::<package-version>` の形式でバージョンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ec00-258">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="4ec00-259">既定では、`dotnet new` は、バージョンに対して \* を渡します。これは最後の安定したパッケージのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-259">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="4ec00-260">「[使用例](#examples)」のセクションで、例をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4ec00-260">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="4ec00-261">カスタム テンプレートの作成方法については、[「dotnet new のカスタム テンプレート」](custom-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ec00-261">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="4ec00-262">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-262">Lists templates containing the specified name.</span></span> <span data-ttu-id="4ec00-263">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-263">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="4ec00-264">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-264">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="4ec00-265">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="4ec00-265">The language of the template to create.</span></span> <span data-ttu-id="4ec00-266">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="4ec00-266">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="4ec00-267">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-267">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="4ec00-268">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-268">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="4ec00-269">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ec00-269">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="4ec00-270">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-270">The name for the created output.</span></span> <span data-ttu-id="4ec00-271">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-271">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="4ec00-272">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="4ec00-272">Location to place the generated output.</span></span> <span data-ttu-id="4ec00-273">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-273">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="4ec00-274">使用可能な種類に基づいて、テンプレートをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-274">Filters templates based on available types.</span></span> <span data-ttu-id="4ec00-275">定義済みの値は、"project"、"item"、または "other" です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-275">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="4ec00-276">指定された `PATH` または `NUGET_ID` で、ソース パックまたはテンプレート パックをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="4ec00-276">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="4ec00-277">ソース `PATH` を使用してテンプレートをアンインストールするには、完全修飾パスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ec00-277">To uninstall a template using a source `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="4ec00-278">たとえば、*C:/Users/\<ユーザー>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* は有効ですが、*./GarciaSoftware.ConsoleTemplate.CSharp* が含まれるフォルダーから、そのパスを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-278">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span> <span data-ttu-id="4ec00-279">また、テンプレートのパスの最後にある終端ディレクトリのスラッシュは含めないでください。</span><span class="sxs-lookup"><span data-stu-id="4ec00-279">Additionally, do not include a final terminating directory slash on your template path.</span></span>
> 
> <span data-ttu-id="4ec00-280">テンプレートのアンインストールに必要な `PATH` または `NUGET_ID` 引数を決定できない場合、引数なしで `dotnet new --uninstall` を実行するとインストールされているすべてのテンプレートと、それをアンインストールするために必要な引数が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-280">If you are unable to determine the `PATH` or `NUGET_ID` argument needed to uninstall a template, running `dotnet new --uninstall` without an argument will list all installed templates and the argument required to uninstall them.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="4ec00-281">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="4ec00-281">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="4ec00-282">`dotnet new` コマンドのコンテキストでのみ実行すると、特定の種類のプロジェクトに対するすべてのテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-282">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="4ec00-283">`dotnet new web -all` など、特定のテンプレートのコンテキストで実行すると、`-all` は強制作成フラグとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-283">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="4ec00-284">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-284">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="4ec00-285">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-285">Prints out help for the command.</span></span> <span data-ttu-id="4ec00-286">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-286">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="4ec00-287">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-287">Lists templates containing the specified name.</span></span> <span data-ttu-id="4ec00-288">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-288">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="4ec00-289">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-289">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="4ec00-290">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="4ec00-290">The language of the template to create.</span></span> <span data-ttu-id="4ec00-291">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="4ec00-291">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="4ec00-292">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-292">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="4ec00-293">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-293">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="4ec00-294">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ec00-294">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="4ec00-295">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-295">The name for the created output.</span></span> <span data-ttu-id="4ec00-296">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-296">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="4ec00-297">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="4ec00-297">Location to place the generated output.</span></span> <span data-ttu-id="4ec00-298">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-298">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="4ec00-299">テンプレート オプション</span><span class="sxs-lookup"><span data-stu-id="4ec00-299">Template options</span></span>

<span data-ttu-id="4ec00-300">プロジェクト テンプレートはそれぞれ、追加のオプションが与えられている場合があります。</span><span class="sxs-lookup"><span data-stu-id="4ec00-300">Each project template may have additional options available.</span></span> <span data-ttu-id="4ec00-301">コア テンプレートの場合、次のオプションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="4ec00-301">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="4ec00-302">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="4ec00-302">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="4ec00-303">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="4ec00-303">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="4ec00-304">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-304">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-305">**classlib**</span><span class="sxs-lookup"><span data-stu-id="4ec00-305">**classlib**</span></span>

<span data-ttu-id="4ec00-306">`-f|--framework <FRAMEWORK>` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-306">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="4ec00-307">値: .NET Core クラス ライブラリを作成するには `netcoreapp2.0`、.NET 標準クラス ライブラリを作成するには `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-307">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="4ec00-308">既定値は `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-308">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="4ec00-309">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-309">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-310">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="4ec00-310">**mstest, xunit**</span></span>

<span data-ttu-id="4ec00-311">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md) を使用してプロジェクトのパッケージ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4ec00-311">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="4ec00-312">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-312">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-313">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="4ec00-313">**globaljson**</span></span>

<span data-ttu-id="4ec00-314">`--sdk-version <VERSION_NUMBER>` - *global.json* ファイル内で使用する .NET Core SDK のバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-314">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="4ec00-315">**web**</span><span class="sxs-lookup"><span data-stu-id="4ec00-315">**web**</span></span>

<span data-ttu-id="4ec00-316">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-316">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="4ec00-317">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-317">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-318">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-318">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="4ec00-319">このオプションは、`IndividualAuth` または `OrganizationalAuth` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-319">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="4ec00-320">**webapi**</span><span class="sxs-lookup"><span data-stu-id="4ec00-320">**webapi**</span></span>

<span data-ttu-id="4ec00-321">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="4ec00-321">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="4ec00-322">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-322">The possible values are:</span></span>

- <span data-ttu-id="4ec00-323">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="4ec00-323">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="4ec00-324">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-324">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="4ec00-325">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-325">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="4ec00-326">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-326">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="4ec00-327">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="4ec00-327">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="4ec00-328">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-328">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="4ec00-329">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-329">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="4ec00-330">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-330">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="4ec00-331">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-331">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-332">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-332">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="4ec00-333">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-333">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="4ec00-334">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-334">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="4ec00-335">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-335">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="4ec00-336">`IndividualB2C` 認証または `SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-336">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="4ec00-337">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-337">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="4ec00-338">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-338">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="4ec00-339">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-339">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="4ec00-340">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-340">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="4ec00-341">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-341">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="4ec00-342">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-342">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="4ec00-343">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-343">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="4ec00-344">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-344">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="4ec00-345">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-345">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="4ec00-346">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-346">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="4ec00-347">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-347">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="4ec00-348">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-348">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-349">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-349">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-350">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-350">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="4ec00-351">`app.UseHsts` と `app.UseHttpsRedirection` は `Startup.Configure` に追加されません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-351">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="4ec00-352">このオプションは、`Individual`、`IndividualB2C`、`SingleOrg`、または `MultiOrg` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-352">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="4ec00-353">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="4ec00-353">**mvc, razor**</span></span>

<span data-ttu-id="4ec00-354">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="4ec00-354">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="4ec00-355">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-355">The possible values are:</span></span>

- <span data-ttu-id="4ec00-356">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="4ec00-356">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="4ec00-357">`Individual` - 個別認証です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-357">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="4ec00-358">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-358">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="4ec00-359">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-359">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="4ec00-360">`MultiOrg` - 複数のテナントに対する組織認証です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-360">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="4ec00-361">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-361">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="4ec00-362">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="4ec00-362">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="4ec00-363">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-363">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="4ec00-364">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-364">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="4ec00-365">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-365">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="4ec00-366">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-366">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-367">`-rp|--reset-password-policy-id <ID>` - このプロジェクトのリセット パスワード ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-367">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="4ec00-368">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-368">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-369">`-ep|--edit-profile-policy-id <ID>` - このプロジェクトの編集プロファイル ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-369">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="4ec00-370">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-370">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-371">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-371">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="4ec00-372">`SingleOrg` 認証または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-372">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="4ec00-373">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-373">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="4ec00-374">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-374">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="4ec00-375">`IndividualB2C` 認証、`SingleOrg` 認証、または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-375">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="4ec00-376">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-376">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="4ec00-377">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-377">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="4ec00-378">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-378">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="4ec00-379">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-379">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="4ec00-380">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-380">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="4ec00-381">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-381">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="4ec00-382">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-382">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="4ec00-383">`--callback-path <PATH>` - リダイレクト URI のアプリケーションの基本パス内の要求パスです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-383">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="4ec00-384">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-384">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="4ec00-385">既定値は `/signin-oidc` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-385">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="4ec00-386">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-386">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="4ec00-387">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-387">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="4ec00-388">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-388">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="4ec00-389">`--use-browserlink` - プロジェクトに BrowserLink を含めます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-389">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="4ec00-390">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-390">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="4ec00-391">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-391">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-392">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-392">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-393">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-393">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="4ec00-394">`app.UseHsts` と `app.UseHttpsRedirection` は `Startup.Configure` に追加されません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-394">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="4ec00-395">このオプションは、`Individual`、`IndividualB2C`、`SingleOrg`、または `MultiOrg` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-395">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="4ec00-396">**page**</span><span class="sxs-lookup"><span data-stu-id="4ec00-396">**page**</span></span>

<span data-ttu-id="4ec00-397">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-397">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="4ec00-398">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-398">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="4ec00-399">`-np|--no-pagemodel` - PageModel なしでページを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-399">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="4ec00-400">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="4ec00-400">**viewimports**</span></span>

<span data-ttu-id="4ec00-401">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-401">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="4ec00-402">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-402">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="4ec00-403">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="4ec00-403">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="4ec00-404">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="4ec00-404">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="4ec00-405">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-405">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-406">**classlib**</span><span class="sxs-lookup"><span data-stu-id="4ec00-406">**classlib**</span></span>

<span data-ttu-id="4ec00-407">`-f|--framework <FRAMEWORK>` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-407">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="4ec00-408">値: .NET Core クラス ライブラリを作成するには `netcoreapp2.0`、.NET 標準クラス ライブラリを作成するには `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-408">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="4ec00-409">既定値は `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-409">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="4ec00-410">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-410">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-411">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="4ec00-411">**mstest, xunit**</span></span>

<span data-ttu-id="4ec00-412">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md) を使用してプロジェクトのパッケージ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4ec00-412">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="4ec00-413">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-413">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-414">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="4ec00-414">**globaljson**</span></span>

<span data-ttu-id="4ec00-415">`--sdk-version <VERSION_NUMBER>` - *global.json* ファイル内で使用する .NET Core SDK のバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-415">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="4ec00-416">**web**</span><span class="sxs-lookup"><span data-stu-id="4ec00-416">**web**</span></span>

<span data-ttu-id="4ec00-417">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-417">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="4ec00-418">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-418">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-419">**webapi**</span><span class="sxs-lookup"><span data-stu-id="4ec00-419">**webapi**</span></span>

<span data-ttu-id="4ec00-420">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="4ec00-420">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="4ec00-421">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-421">The possible values are:</span></span>

- <span data-ttu-id="4ec00-422">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="4ec00-422">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="4ec00-423">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-423">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="4ec00-424">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-424">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="4ec00-425">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-425">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="4ec00-426">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="4ec00-426">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="4ec00-427">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-427">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="4ec00-428">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-428">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="4ec00-429">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-429">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="4ec00-430">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-430">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-431">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-431">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="4ec00-432">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-432">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="4ec00-433">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-433">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="4ec00-434">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-434">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="4ec00-435">`IndividualB2C` 認証または `SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-435">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="4ec00-436">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-436">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="4ec00-437">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-437">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="4ec00-438">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-438">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="4ec00-439">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-439">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="4ec00-440">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-440">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="4ec00-441">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-441">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="4ec00-442">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-442">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="4ec00-443">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-443">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="4ec00-444">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-444">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="4ec00-445">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-445">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="4ec00-446">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-446">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="4ec00-447">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-447">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-448">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-448">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-449">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="4ec00-449">**mvc, razor**</span></span>

<span data-ttu-id="4ec00-450">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="4ec00-450">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="4ec00-451">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-451">The possible values are:</span></span>

- <span data-ttu-id="4ec00-452">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="4ec00-452">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="4ec00-453">`Individual` - 個別認証です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-453">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="4ec00-454">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-454">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="4ec00-455">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-455">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="4ec00-456">`MultiOrg` - 複数のテナントに対する組織認証です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-456">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="4ec00-457">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="4ec00-457">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="4ec00-458">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="4ec00-458">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="4ec00-459">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-459">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="4ec00-460">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-460">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="4ec00-461">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-461">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="4ec00-462">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-462">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-463">`-rp|--reset-password-policy-id <ID>` - このプロジェクトのリセット パスワード ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-463">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="4ec00-464">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-464">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-465">`-ep|--edit-profile-policy-id <ID>` - このプロジェクトの編集プロファイル ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-465">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="4ec00-466">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-466">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-467">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-467">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="4ec00-468">`SingleOrg` 認証または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-468">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="4ec00-469">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-469">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="4ec00-470">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-470">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="4ec00-471">`IndividualB2C` 認証、`SingleOrg` 認証、または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-471">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="4ec00-472">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-472">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="4ec00-473">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-473">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="4ec00-474">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-474">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="4ec00-475">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-475">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="4ec00-476">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-476">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="4ec00-477">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-477">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="4ec00-478">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-478">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="4ec00-479">`--callback-path <PATH>` - リダイレクト URI のアプリケーションの基本パス内の要求パスです。</span><span class="sxs-lookup"><span data-stu-id="4ec00-479">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="4ec00-480">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-480">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="4ec00-481">既定値は `/signin-oidc` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-481">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="4ec00-482">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-482">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="4ec00-483">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-483">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="4ec00-484">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-484">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="4ec00-485">`--use-browserlink` - プロジェクトに BrowserLink を含めます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-485">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="4ec00-486">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-486">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="4ec00-487">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4ec00-487">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="4ec00-488">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="4ec00-488">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="4ec00-489">**page**</span><span class="sxs-lookup"><span data-stu-id="4ec00-489">**page**</span></span>

<span data-ttu-id="4ec00-490">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-490">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="4ec00-491">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-491">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="4ec00-492">`-np|--no-pagemodel` - PageModel なしでページを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-492">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="4ec00-493">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="4ec00-493">**viewimports**</span></span>

<span data-ttu-id="4ec00-494">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-494">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="4ec00-495">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-495">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="4ec00-496">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="4ec00-496">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="4ec00-497">**console、xunit、mstest、web、webapi**</span><span class="sxs-lookup"><span data-stu-id="4ec00-497">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="4ec00-498">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-498">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="4ec00-499">値: `netcoreapp1.0` または `netcoreapp1.1` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-499">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="4ec00-500">既定値は `netcoreapp1.0` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-500">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="4ec00-501">**classlib**</span><span class="sxs-lookup"><span data-stu-id="4ec00-501">**classlib**</span></span>

<span data-ttu-id="4ec00-502">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-502">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="4ec00-503">値: `netcoreapp1.0`、`netcoreapp1.1`、または `netstandard1.0` から `netstandard1.6` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-503">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="4ec00-504">既定値は `netstandard1.4` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-504">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="4ec00-505">**mvc**</span><span class="sxs-lookup"><span data-stu-id="4ec00-505">**mvc**</span></span>

<span data-ttu-id="4ec00-506">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-506">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="4ec00-507">値: `netcoreapp1.0` または `netcoreapp1.1` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-507">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="4ec00-508">既定値は `netcoreapp1.0` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-508">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="4ec00-509">`-au|--auth` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="4ec00-509">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="4ec00-510">値: `None` または `Individual` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-510">Values: `None` or `Individual`.</span></span> <span data-ttu-id="4ec00-511">既定値は `None` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-511">The default value is `None`.</span></span>

<span data-ttu-id="4ec00-512">`-uld|--use-local-db` - SQLite の代わりに LocalDB を使うかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-512">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="4ec00-513">値: `true` または `false` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-513">Values: `true` or `false`.</span></span> <span data-ttu-id="4ec00-514">既定値は `false` です。</span><span class="sxs-lookup"><span data-stu-id="4ec00-514">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="4ec00-515">使用例</span><span class="sxs-lookup"><span data-stu-id="4ec00-515">Examples</span></span>

<span data-ttu-id="4ec00-516">現在のディレクトリに、F# コンソール アプリケーション プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-516">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="4ec00-517">指定したディレクトリ内に .NET 標準クラス ライブラリ プロジェクトを作成します (.NET Core SDK 2.0 またはそれ以降のバージョンでのみ使用可能)。</span><span class="sxs-lookup"><span data-stu-id="4ec00-517">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="4ec00-518">認証なしで、現在のディレクトリに新しい ASP.NET Core C# MVC アプリケーション プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-518">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="4ec00-519">新しい xUnit アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-519">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="4ec00-520">MVC に利用できるすべてのテンプレートを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-520">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="4ec00-521">ASP.NET Core のシングル ページ アプリケーション テンプレートのバージョン 2.0 をインストールします (コマンド オプションは .NET Core SDK 1.1 以降のバージョンでのみ使用できます):</span><span class="sxs-lookup"><span data-stu-id="4ec00-521">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="4ec00-522">SDK バージョン 2.0.0 (.NET Core SDK 2.0 以降のバージョンでのみ使用できます) を設定している現在のディレクトリ内に *global.json* を作成します。</span><span class="sxs-lookup"><span data-stu-id="4ec00-522">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="4ec00-523">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ec00-523">See also</span></span>

* [<span data-ttu-id="4ec00-524">dotnet new のカスタム テンプレート</span><span class="sxs-lookup"><span data-stu-id="4ec00-524">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="4ec00-525">dotnet new のカスタム テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="4ec00-525">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* [<span data-ttu-id="4ec00-526">dotnet/dotnet-template-samples GitHub リポジトリ</span><span class="sxs-lookup"><span data-stu-id="4ec00-526">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)  
* [<span data-ttu-id="4ec00-527">dotnet new で使用できるテンプレート</span><span class="sxs-lookup"><span data-stu-id="4ec00-527">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
