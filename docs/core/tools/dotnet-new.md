---
title: dotnet new コマンド - .NET Core CLI
description: dotnet new コマンドは、指定されたテンプレートに基づいて新しい .NET Core プロジェクトを作成します。
author: mairaw
ms.author: mairaw
ms.date: 10/24/2018
ms.openlocfilehash: a8d486f569f31d68d5659ac6a80d615474ef2506
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53131483"
---
# <a name="dotnet-new"></a><span data-ttu-id="f0664-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="f0664-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="f0664-104">name</span><span class="sxs-lookup"><span data-stu-id="f0664-104">Name</span></span>

<span data-ttu-id="f0664-105">`dotnet new` - 指定したテンプレートに基づいて、新しいプロジェクト、構成ファイル、またはソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="f0664-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="f0664-106">構文</span><span class="sxs-lookup"><span data-stu-id="f0664-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="f0664-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="f0664-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="f0664-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="f0664-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="f0664-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="f0664-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="f0664-110">説明</span><span class="sxs-lookup"><span data-stu-id="f0664-110">Description</span></span>

<span data-ttu-id="f0664-111">`dotnet new` コマンドは、有効な .NET Core プロジェクトを初期化する便利な手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="f0664-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="f0664-112">このコマンドは、[テンプレート エンジン](https://github.com/dotnet/templating)を呼び出し、指定されたテンプレートとオプションに基づいて、ディスク上に成果物を作成します。</span><span class="sxs-lookup"><span data-stu-id="f0664-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="f0664-113">引数</span><span class="sxs-lookup"><span data-stu-id="f0664-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="f0664-114">コマンドが呼び出されたときにインスタンス化するテンプレート。</span><span class="sxs-lookup"><span data-stu-id="f0664-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="f0664-115">各テンプレートには、渡すことができるオプションが存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="f0664-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="f0664-116">詳細については、[テンプレートのオプション](#template-options)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0664-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="f0664-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="f0664-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="f0664-118">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0664-118">The command contains a default list of templates.</span></span> <span data-ttu-id="f0664-119">使用可能なテンプレートの一覧を取得するには、`dotnet new -l` を使います。</span><span class="sxs-lookup"><span data-stu-id="f0664-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="f0664-120">次の表は、.NET Core SDK 2.1.300 にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="f0664-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="f0664-121">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="f0664-122">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="f0664-122">Template description</span></span>                          | <span data-ttu-id="f0664-123">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="f0664-123">Template name</span></span>    | <span data-ttu-id="f0664-124">言語</span><span class="sxs-lookup"><span data-stu-id="f0664-124">Languages</span></span>     |
|----------------------------------------------|------------------|---------------|
| <span data-ttu-id="f0664-125">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="f0664-125">Console application</span></span>                          | `console`        | <span data-ttu-id="f0664-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="f0664-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="f0664-127">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="f0664-127">Class library</span></span>                                | `classlib`       | <span data-ttu-id="f0664-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="f0664-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="f0664-129">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="f0664-129">Unit test project</span></span>                            | `mstest`         | <span data-ttu-id="f0664-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="f0664-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="f0664-131">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="f0664-131">xUnit test project</span></span>                           | `xunit`          | <span data-ttu-id="f0664-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="f0664-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="f0664-133">NUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="f0664-133">NUnit test project</span></span>                           | `nunit`          | <span data-ttu-id="f0664-134">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="f0664-134">[C#], F#, VB</span></span>  |
| <span data-ttu-id="f0664-135">Razor ページ</span><span class="sxs-lookup"><span data-stu-id="f0664-135">Razor page</span></span>                                   | `page`           | <span data-ttu-id="f0664-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-136">[C#]</span></span>          |
| <span data-ttu-id="f0664-137">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="f0664-137">MVC ViewImports</span></span>                              | `viewimports`    | <span data-ttu-id="f0664-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-138">[C#]</span></span>          |
| <span data-ttu-id="f0664-139">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="f0664-139">MVC ViewStart</span></span>                                | `viewstart`      | <span data-ttu-id="f0664-140">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-140">[C#]</span></span>          |
| <span data-ttu-id="f0664-141">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="f0664-141">ASP.NET Core empty</span></span>                           | `web`            | <span data-ttu-id="f0664-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="f0664-142">[C#], F#</span></span>      |
| <span data-ttu-id="f0664-143">ASP.NET Core Web アプリ (モデル ビュー コントローラー)</span><span class="sxs-lookup"><span data-stu-id="f0664-143">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`            | <span data-ttu-id="f0664-144">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="f0664-144">[C#], F#</span></span>      |
| <span data-ttu-id="f0664-145">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="f0664-145">ASP.NET Core Web App</span></span>                         | <span data-ttu-id="f0664-146">`razor`、 `webapp`</span><span class="sxs-lookup"><span data-stu-id="f0664-146">`razor`, `webapp`</span></span>| <span data-ttu-id="f0664-147">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-147">[C#]</span></span>          |
| <span data-ttu-id="f0664-148">Angular 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="f0664-148">ASP.NET Core with Angular</span></span>                    | `angular`        | <span data-ttu-id="f0664-149">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-149">[C#]</span></span>          |
| <span data-ttu-id="f0664-150">React.js 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="f0664-150">ASP.NET Core with React.js</span></span>                   | `react`          | <span data-ttu-id="f0664-151">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-151">[C#]</span></span>          |
| <span data-ttu-id="f0664-152">React.js および Redux 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="f0664-152">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`     | <span data-ttu-id="f0664-153">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-153">[C#]</span></span>          |
| <span data-ttu-id="f0664-154">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="f0664-154">ASP.NET Core Web API</span></span>                         | `webapi`         | <span data-ttu-id="f0664-155">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="f0664-155">[C#], F#</span></span>      |
| <span data-ttu-id="f0664-156">Razor クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="f0664-156">Razor class library</span></span>                          | `razorclasslib`  | <span data-ttu-id="f0664-157">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-157">[C#]</span></span>          |
| <span data-ttu-id="f0664-158">global.json file</span><span class="sxs-lookup"><span data-stu-id="f0664-158">global.json file</span></span>                             | `globaljson`     |               |
| <span data-ttu-id="f0664-159">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="f0664-159">NuGet config</span></span>                                 | `nugetconfig`    |               |
| <span data-ttu-id="f0664-160">Web 構成</span><span class="sxs-lookup"><span data-stu-id="f0664-160">Web config</span></span>                                   | `webconfig`      |               |
| <span data-ttu-id="f0664-161">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="f0664-161">Solution file</span></span>                                | `sln`            |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="f0664-162">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="f0664-162">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="f0664-163">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0664-163">The command contains a default list of templates.</span></span> <span data-ttu-id="f0664-164">使用可能なテンプレートの一覧を取得するには、`dotnet new -l` を使います。</span><span class="sxs-lookup"><span data-stu-id="f0664-164">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="f0664-165">次の表は、.NET Core SDK 2.0 にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="f0664-165">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="f0664-166">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-166">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="f0664-167">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="f0664-167">Template description</span></span>                          | <span data-ttu-id="f0664-168">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="f0664-168">Template name</span></span> | <span data-ttu-id="f0664-169">言語</span><span class="sxs-lookup"><span data-stu-id="f0664-169">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="f0664-170">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="f0664-170">Console application</span></span>                          | `console`     | <span data-ttu-id="f0664-171">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="f0664-171">[C#], F#, VB</span></span>  |
| <span data-ttu-id="f0664-172">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="f0664-172">Class library</span></span>                                | `classlib`    | <span data-ttu-id="f0664-173">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="f0664-173">[C#], F#, VB</span></span>  |
| <span data-ttu-id="f0664-174">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="f0664-174">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="f0664-175">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="f0664-175">[C#], F#, VB</span></span>  |
| <span data-ttu-id="f0664-176">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="f0664-176">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="f0664-177">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="f0664-177">[C#], F#, VB</span></span>  |
| <span data-ttu-id="f0664-178">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="f0664-178">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="f0664-179">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="f0664-179">[C#], F#</span></span>      |
| <span data-ttu-id="f0664-180">ASP.NET Core Web アプリ (モデル ビュー コントローラー)</span><span class="sxs-lookup"><span data-stu-id="f0664-180">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="f0664-181">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="f0664-181">[C#], F#</span></span>      |
| <span data-ttu-id="f0664-182">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="f0664-182">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="f0664-183">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-183">[C#]</span></span>          |
| <span data-ttu-id="f0664-184">Angular 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="f0664-184">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="f0664-185">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-185">[C#]</span></span>          |
| <span data-ttu-id="f0664-186">React.js 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="f0664-186">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="f0664-187">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-187">[C#]</span></span>          |
| <span data-ttu-id="f0664-188">React.js および Redux 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="f0664-188">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="f0664-189">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-189">[C#]</span></span>          |
| <span data-ttu-id="f0664-190">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="f0664-190">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="f0664-191">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="f0664-191">[C#], F#</span></span>      |
| <span data-ttu-id="f0664-192">global.json file</span><span class="sxs-lookup"><span data-stu-id="f0664-192">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="f0664-193">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="f0664-193">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="f0664-194">Web 構成</span><span class="sxs-lookup"><span data-stu-id="f0664-194">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="f0664-195">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="f0664-195">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="f0664-196">Razor ページ</span><span class="sxs-lookup"><span data-stu-id="f0664-196">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="f0664-197">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="f0664-197">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="f0664-198">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="f0664-198">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="f0664-199">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="f0664-199">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="f0664-200">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0664-200">The command contains a default list of templates.</span></span> <span data-ttu-id="f0664-201">使用可能なテンプレートの一覧を取得するには、`dotnet new -all` を使います。</span><span class="sxs-lookup"><span data-stu-id="f0664-201">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="f0664-202">次の表は、.NET Core SDK 1.x にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="f0664-202">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="f0664-203">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-203">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="f0664-204">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="f0664-204">Template description</span></span>  | <span data-ttu-id="f0664-205">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="f0664-205">Template name</span></span> | <span data-ttu-id="f0664-206">言語</span><span class="sxs-lookup"><span data-stu-id="f0664-206">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="f0664-207">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="f0664-207">Console application</span></span>  | `console`     | <span data-ttu-id="f0664-208">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="f0664-208">[C#], F#</span></span>  |
| <span data-ttu-id="f0664-209">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="f0664-209">Class library</span></span>        | `classlib`    | <span data-ttu-id="f0664-210">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="f0664-210">[C#], F#</span></span>  |
| <span data-ttu-id="f0664-211">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="f0664-211">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="f0664-212">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="f0664-212">[C#], F#</span></span>  |
| <span data-ttu-id="f0664-213">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="f0664-213">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="f0664-214">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="f0664-214">[C#], F#</span></span>  |
| <span data-ttu-id="f0664-215">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="f0664-215">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="f0664-216">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-216">[C#]</span></span>      |
| <span data-ttu-id="f0664-217">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="f0664-217">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="f0664-218">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="f0664-218">[C#], F#</span></span>  |
| <span data-ttu-id="f0664-219">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="f0664-219">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="f0664-220">[C#]</span><span class="sxs-lookup"><span data-stu-id="f0664-220">[C#]</span></span>      |
| <span data-ttu-id="f0664-221">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="f0664-221">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="f0664-222">Web 構成</span><span class="sxs-lookup"><span data-stu-id="f0664-222">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="f0664-223">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="f0664-223">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="f0664-224">オプション</span><span class="sxs-lookup"><span data-stu-id="f0664-224">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="f0664-225">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="f0664-225">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="f0664-226">既存のファイルを変更する場合でも、コンテンツが強制的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-226">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="f0664-227">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="f0664-227">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="f0664-228">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="f0664-228">Prints out help for the command.</span></span> <span data-ttu-id="f0664-229">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="f0664-229">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="f0664-230">指定された `PATH` または `NUGET_ID` からソース パックまたはテンプレート パックをインストールします。</span><span class="sxs-lookup"><span data-stu-id="f0664-230">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="f0664-231">テンプレート パッケージのプレリリース版をインストールする場合は、`<package-name>::<package-version>` の形式でバージョンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0664-231">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="f0664-232">既定では、`dotnet new` は、バージョンに対して \* を渡します。これは最後の安定したパッケージのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="f0664-232">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="f0664-233">「[使用例](#examples)」のセクションで、例をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f0664-233">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="f0664-234">カスタム テンプレートの作成方法については、[「dotnet new のカスタム テンプレート」](custom-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0664-234">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="f0664-235">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="f0664-235">Lists templates containing the specified name.</span></span> <span data-ttu-id="f0664-236">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-236">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="f0664-237">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="f0664-237">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="f0664-238">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="f0664-238">The language of the template to create.</span></span> <span data-ttu-id="f0664-239">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="f0664-239">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="f0664-240">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="f0664-240">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="f0664-241">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="f0664-241">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="f0664-242">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0664-242">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="f0664-243">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="f0664-243">The name for the created output.</span></span> <span data-ttu-id="f0664-244">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-244">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="f0664-245">インストール中に使用する NuGet ソースを 1 つ指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-245">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="f0664-246">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="f0664-246">Location to place the generated output.</span></span> <span data-ttu-id="f0664-247">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="f0664-247">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="f0664-248">使用可能な種類に基づいて、テンプレートをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="f0664-248">Filters templates based on available types.</span></span> <span data-ttu-id="f0664-249">定義済みの値は、"project"、"item"、または "other" です。</span><span class="sxs-lookup"><span data-stu-id="f0664-249">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="f0664-250">指定された `PATH` または `NUGET_ID` で、ソース パックまたはテンプレート パックをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="f0664-250">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="f0664-251">`PATH` を使用してテンプレートをアンインストールするには、完全修飾パスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0664-251">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="f0664-252">たとえば、*C:/Users/\<ユーザー>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* は有効ですが、*./GarciaSoftware.ConsoleTemplate.CSharp* が含まれるフォルダーから、そのパスを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="f0664-252">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="f0664-253">また、テンプレートのパスの最後にある終端ディレクトリのスラッシュは含めないでください。</span><span class="sxs-lookup"><span data-stu-id="f0664-253">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="f0664-254">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="f0664-254">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="f0664-255">既存のファイルを変更する場合でも、コンテンツが強制的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-255">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="f0664-256">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="f0664-256">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="f0664-257">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="f0664-257">Prints out help for the command.</span></span> <span data-ttu-id="f0664-258">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="f0664-258">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="f0664-259">指定された `PATH` または `NUGET_ID` からソース パックまたはテンプレート パックをインストールします。</span><span class="sxs-lookup"><span data-stu-id="f0664-259">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="f0664-260">テンプレート パッケージのプレリリース版をインストールする場合は、`<package-name>::<package-version>` の形式でバージョンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0664-260">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="f0664-261">既定では、`dotnet new` は、バージョンに対して \* を渡します。これは最後の安定したパッケージのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="f0664-261">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="f0664-262">「[使用例](#examples)」のセクションで、例をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f0664-262">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="f0664-263">カスタム テンプレートの作成方法については、[「dotnet new のカスタム テンプレート」](custom-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0664-263">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="f0664-264">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="f0664-264">Lists templates containing the specified name.</span></span> <span data-ttu-id="f0664-265">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-265">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="f0664-266">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="f0664-266">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="f0664-267">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="f0664-267">The language of the template to create.</span></span> <span data-ttu-id="f0664-268">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="f0664-268">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="f0664-269">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="f0664-269">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="f0664-270">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="f0664-270">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="f0664-271">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0664-271">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="f0664-272">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="f0664-272">The name for the created output.</span></span> <span data-ttu-id="f0664-273">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-273">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="f0664-274">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="f0664-274">Location to place the generated output.</span></span> <span data-ttu-id="f0664-275">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="f0664-275">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="f0664-276">使用可能な種類に基づいて、テンプレートをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="f0664-276">Filters templates based on available types.</span></span> <span data-ttu-id="f0664-277">定義済みの値は、"project"、"item"、または "other" です。</span><span class="sxs-lookup"><span data-stu-id="f0664-277">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="f0664-278">指定された `PATH` または `NUGET_ID` で、ソース パックまたはテンプレート パックをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="f0664-278">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="f0664-279">ソース `PATH` を使用してテンプレートをアンインストールするには、完全修飾パスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0664-279">To uninstall a template using a source `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="f0664-280">たとえば、*C:/Users/\<ユーザー>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* は有効ですが、*./GarciaSoftware.ConsoleTemplate.CSharp* が含まれるフォルダーから、そのパスを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="f0664-280">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span> <span data-ttu-id="f0664-281">また、テンプレートのパスの最後にある終端ディレクトリのスラッシュは含めないでください。</span><span class="sxs-lookup"><span data-stu-id="f0664-281">Additionally, do not include a final terminating directory slash on your template path.</span></span>
> 
> <span data-ttu-id="f0664-282">テンプレートのアンインストールに必要な `PATH` または `NUGET_ID` 引数を決定できない場合、引数なしで `dotnet new --uninstall` を実行するとインストールされているすべてのテンプレートと、それをアンインストールするために必要な引数が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-282">If you are unable to determine the `PATH` or `NUGET_ID` argument needed to uninstall a template, running `dotnet new --uninstall` without an argument will list all installed templates and the argument required to uninstall them.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="f0664-283">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="f0664-283">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="f0664-284">`dotnet new` コマンドのコンテキストでのみ実行すると、特定の種類のプロジェクトに対するすべてのテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-284">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="f0664-285">`dotnet new web -all` など、特定のテンプレートのコンテキストで実行すると、`-all` は強制作成フラグとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-285">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="f0664-286">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="f0664-286">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="f0664-287">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="f0664-287">Prints out help for the command.</span></span> <span data-ttu-id="f0664-288">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="f0664-288">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="f0664-289">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="f0664-289">Lists templates containing the specified name.</span></span> <span data-ttu-id="f0664-290">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-290">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="f0664-291">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="f0664-291">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="f0664-292">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="f0664-292">The language of the template to create.</span></span> <span data-ttu-id="f0664-293">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="f0664-293">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="f0664-294">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="f0664-294">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="f0664-295">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="f0664-295">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="f0664-296">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0664-296">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="f0664-297">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="f0664-297">The name for the created output.</span></span> <span data-ttu-id="f0664-298">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-298">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="f0664-299">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="f0664-299">Location to place the generated output.</span></span> <span data-ttu-id="f0664-300">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="f0664-300">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="f0664-301">テンプレート オプション</span><span class="sxs-lookup"><span data-stu-id="f0664-301">Template options</span></span>

<span data-ttu-id="f0664-302">プロジェクト テンプレートはそれぞれ、追加のオプションが与えられている場合があります。</span><span class="sxs-lookup"><span data-stu-id="f0664-302">Each project template may have additional options available.</span></span> <span data-ttu-id="f0664-303">コア テンプレートの場合、次のオプションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="f0664-303">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="f0664-304">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="f0664-304">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="f0664-305">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="f0664-305">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="f0664-306">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-306">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-307">**classlib**</span><span class="sxs-lookup"><span data-stu-id="f0664-307">**classlib**</span></span>

<span data-ttu-id="f0664-308">`-f|--framework <FRAMEWORK>` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-308">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="f0664-309">値: .NET Core クラス ライブラリを作成するには `netcoreapp2.0`、.NET 標準クラス ライブラリを作成するには `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-309">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="f0664-310">既定値は `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-310">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="f0664-311">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-311">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-312">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="f0664-312">**mstest, xunit**</span></span>

<span data-ttu-id="f0664-313">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md) を使用してプロジェクトのパッケージ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f0664-313">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="f0664-314">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-314">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-315">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="f0664-315">**globaljson**</span></span>

<span data-ttu-id="f0664-316">`--sdk-version <VERSION_NUMBER>` - *global.json* ファイル内で使用する .NET Core SDK のバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-316">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="f0664-317">**web**</span><span class="sxs-lookup"><span data-stu-id="f0664-317">**web**</span></span>

<span data-ttu-id="f0664-318">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="f0664-318">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="f0664-319">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-319">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-320">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="f0664-320">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="f0664-321">このオプションは、`IndividualAuth` または `OrganizationalAuth` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-321">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="f0664-322">**webapi**</span><span class="sxs-lookup"><span data-stu-id="f0664-322">**webapi**</span></span>

<span data-ttu-id="f0664-323">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="f0664-323">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="f0664-324">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f0664-324">The possible values are:</span></span>

- <span data-ttu-id="f0664-325">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="f0664-325">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="f0664-326">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-326">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="f0664-327">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-327">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="f0664-328">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-328">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="f0664-329">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="f0664-329">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="f0664-330">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-330">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="f0664-331">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-331">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="f0664-332">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-332">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="f0664-333">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-333">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-334">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="f0664-334">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="f0664-335">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-335">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="f0664-336">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-336">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="f0664-337">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-337">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="f0664-338">`IndividualB2C` 認証または `SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-338">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="f0664-339">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-339">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="f0664-340">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="f0664-340">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="f0664-341">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-341">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="f0664-342">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-342">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="f0664-343">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-343">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="f0664-344">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-344">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="f0664-345">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-345">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="f0664-346">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="f0664-346">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="f0664-347">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-347">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="f0664-348">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="f0664-348">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="f0664-349">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-349">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="f0664-350">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-350">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-351">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-351">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-352">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="f0664-352">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="f0664-353">`app.UseHsts` と `app.UseHttpsRedirection` は `Startup.Configure` に追加されません。</span><span class="sxs-lookup"><span data-stu-id="f0664-353">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="f0664-354">このオプションは、`Individual`、`IndividualB2C`、`SingleOrg`、または `MultiOrg` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-354">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="f0664-355">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="f0664-355">**mvc, razor**</span></span>

<span data-ttu-id="f0664-356">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="f0664-356">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="f0664-357">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f0664-357">The possible values are:</span></span>

- <span data-ttu-id="f0664-358">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="f0664-358">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="f0664-359">`Individual` - 個別認証です。</span><span class="sxs-lookup"><span data-stu-id="f0664-359">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="f0664-360">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-360">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="f0664-361">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-361">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="f0664-362">`MultiOrg` - 複数のテナントに対する組織認証です。</span><span class="sxs-lookup"><span data-stu-id="f0664-362">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="f0664-363">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-363">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="f0664-364">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="f0664-364">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="f0664-365">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-365">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="f0664-366">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-366">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="f0664-367">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-367">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="f0664-368">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-368">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-369">`-rp|--reset-password-policy-id <ID>` - このプロジェクトのリセット パスワード ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-369">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="f0664-370">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-370">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-371">`-ep|--edit-profile-policy-id <ID>` - このプロジェクトの編集プロファイル ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-371">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="f0664-372">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-372">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-373">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="f0664-373">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="f0664-374">`SingleOrg` 認証または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-374">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="f0664-375">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-375">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="f0664-376">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-376">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="f0664-377">`IndividualB2C` 認証、`SingleOrg` 認証、または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-377">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="f0664-378">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-378">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="f0664-379">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="f0664-379">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="f0664-380">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-380">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="f0664-381">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-381">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="f0664-382">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-382">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="f0664-383">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-383">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="f0664-384">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-384">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="f0664-385">`--callback-path <PATH>` - リダイレクト URI のアプリケーションの基本パス内の要求パスです。</span><span class="sxs-lookup"><span data-stu-id="f0664-385">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="f0664-386">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-386">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="f0664-387">既定値は `/signin-oidc` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-387">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="f0664-388">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="f0664-388">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="f0664-389">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-389">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="f0664-390">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="f0664-390">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="f0664-391">`--use-browserlink` - プロジェクトに BrowserLink を含めます。</span><span class="sxs-lookup"><span data-stu-id="f0664-391">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="f0664-392">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-392">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="f0664-393">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-393">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-394">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-394">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-395">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="f0664-395">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="f0664-396">`app.UseHsts` と `app.UseHttpsRedirection` は `Startup.Configure` に追加されません。</span><span class="sxs-lookup"><span data-stu-id="f0664-396">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="f0664-397">このオプションは、`Individual`、`IndividualB2C`、`SingleOrg`、または `MultiOrg` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-397">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="f0664-398">**page**</span><span class="sxs-lookup"><span data-stu-id="f0664-398">**page**</span></span>

<span data-ttu-id="f0664-399">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="f0664-399">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="f0664-400">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-400">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="f0664-401">`-np|--no-pagemodel` - PageModel なしでページを作成します。</span><span class="sxs-lookup"><span data-stu-id="f0664-401">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="f0664-402">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="f0664-402">**viewimports**</span></span>

<span data-ttu-id="f0664-403">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="f0664-403">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="f0664-404">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-404">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="f0664-405">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="f0664-405">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="f0664-406">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="f0664-406">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="f0664-407">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-407">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-408">**classlib**</span><span class="sxs-lookup"><span data-stu-id="f0664-408">**classlib**</span></span>

<span data-ttu-id="f0664-409">`-f|--framework <FRAMEWORK>` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-409">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="f0664-410">値: .NET Core クラス ライブラリを作成するには `netcoreapp2.0`、.NET 標準クラス ライブラリを作成するには `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-410">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="f0664-411">既定値は `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-411">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="f0664-412">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-412">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-413">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="f0664-413">**mstest, xunit**</span></span>

<span data-ttu-id="f0664-414">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md) を使用してプロジェクトのパッケージ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f0664-414">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="f0664-415">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-415">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-416">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="f0664-416">**globaljson**</span></span>

<span data-ttu-id="f0664-417">`--sdk-version <VERSION_NUMBER>` - *global.json* ファイル内で使用する .NET Core SDK のバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-417">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="f0664-418">**web**</span><span class="sxs-lookup"><span data-stu-id="f0664-418">**web**</span></span>

<span data-ttu-id="f0664-419">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="f0664-419">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="f0664-420">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-420">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-421">**webapi**</span><span class="sxs-lookup"><span data-stu-id="f0664-421">**webapi**</span></span>

<span data-ttu-id="f0664-422">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="f0664-422">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="f0664-423">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f0664-423">The possible values are:</span></span>

- <span data-ttu-id="f0664-424">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="f0664-424">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="f0664-425">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-425">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="f0664-426">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-426">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="f0664-427">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-427">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="f0664-428">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="f0664-428">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="f0664-429">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-429">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="f0664-430">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-430">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="f0664-431">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-431">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="f0664-432">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-432">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-433">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="f0664-433">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="f0664-434">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-434">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="f0664-435">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-435">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="f0664-436">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-436">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="f0664-437">`IndividualB2C` 認証または `SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-437">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="f0664-438">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-438">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="f0664-439">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="f0664-439">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="f0664-440">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-440">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="f0664-441">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-441">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="f0664-442">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-442">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="f0664-443">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-443">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="f0664-444">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-444">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="f0664-445">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="f0664-445">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="f0664-446">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-446">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="f0664-447">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="f0664-447">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="f0664-448">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-448">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="f0664-449">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-449">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-450">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-450">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-451">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="f0664-451">**mvc, razor**</span></span>

<span data-ttu-id="f0664-452">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="f0664-452">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="f0664-453">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f0664-453">The possible values are:</span></span>

- <span data-ttu-id="f0664-454">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="f0664-454">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="f0664-455">`Individual` - 個別認証です。</span><span class="sxs-lookup"><span data-stu-id="f0664-455">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="f0664-456">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-456">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="f0664-457">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-457">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="f0664-458">`MultiOrg` - 複数のテナントに対する組織認証です。</span><span class="sxs-lookup"><span data-stu-id="f0664-458">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="f0664-459">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="f0664-459">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="f0664-460">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="f0664-460">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="f0664-461">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-461">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="f0664-462">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-462">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="f0664-463">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-463">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="f0664-464">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-464">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-465">`-rp|--reset-password-policy-id <ID>` - このプロジェクトのリセット パスワード ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-465">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="f0664-466">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-466">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-467">`-ep|--edit-profile-policy-id <ID>` - このプロジェクトの編集プロファイル ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-467">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="f0664-468">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-468">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-469">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="f0664-469">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="f0664-470">`SingleOrg` 認証または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-470">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="f0664-471">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-471">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="f0664-472">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-472">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="f0664-473">`IndividualB2C` 認証、`SingleOrg` 認証、または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-473">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="f0664-474">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-474">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="f0664-475">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="f0664-475">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="f0664-476">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-476">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="f0664-477">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-477">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="f0664-478">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="f0664-478">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="f0664-479">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-479">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="f0664-480">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-480">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="f0664-481">`--callback-path <PATH>` - リダイレクト URI のアプリケーションの基本パス内の要求パスです。</span><span class="sxs-lookup"><span data-stu-id="f0664-481">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="f0664-482">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="f0664-482">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="f0664-483">既定値は `/signin-oidc` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-483">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="f0664-484">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="f0664-484">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="f0664-485">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-485">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="f0664-486">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="f0664-486">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="f0664-487">`--use-browserlink` - プロジェクトに BrowserLink を含めます。</span><span class="sxs-lookup"><span data-stu-id="f0664-487">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="f0664-488">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-488">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="f0664-489">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0664-489">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="f0664-490">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="f0664-490">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="f0664-491">**page**</span><span class="sxs-lookup"><span data-stu-id="f0664-491">**page**</span></span>

<span data-ttu-id="f0664-492">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="f0664-492">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="f0664-493">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-493">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="f0664-494">`-np|--no-pagemodel` - PageModel なしでページを作成します。</span><span class="sxs-lookup"><span data-stu-id="f0664-494">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="f0664-495">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="f0664-495">**viewimports**</span></span>

<span data-ttu-id="f0664-496">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="f0664-496">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="f0664-497">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-497">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="f0664-498">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="f0664-498">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="f0664-499">**console、xunit、mstest、web、webapi**</span><span class="sxs-lookup"><span data-stu-id="f0664-499">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="f0664-500">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-500">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="f0664-501">値: `netcoreapp1.0` または `netcoreapp1.1` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-501">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="f0664-502">既定値は `netcoreapp1.0` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-502">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="f0664-503">**classlib**</span><span class="sxs-lookup"><span data-stu-id="f0664-503">**classlib**</span></span>

<span data-ttu-id="f0664-504">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-504">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="f0664-505">値: `netcoreapp1.0`、`netcoreapp1.1`、または `netstandard1.0` から `netstandard1.6` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-505">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="f0664-506">既定値は `netstandard1.4` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-506">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="f0664-507">**mvc**</span><span class="sxs-lookup"><span data-stu-id="f0664-507">**mvc**</span></span>

<span data-ttu-id="f0664-508">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-508">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="f0664-509">値: `netcoreapp1.0` または `netcoreapp1.1` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-509">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="f0664-510">既定値は `netcoreapp1.0` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-510">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="f0664-511">`-au|--auth` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="f0664-511">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="f0664-512">値: `None` または `Individual` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-512">Values: `None` or `Individual`.</span></span> <span data-ttu-id="f0664-513">既定値は `None` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-513">The default value is `None`.</span></span>

<span data-ttu-id="f0664-514">`-uld|--use-local-db` - SQLite の代わりに LocalDB を使うかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f0664-514">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="f0664-515">値: `true` または `false` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-515">Values: `true` or `false`.</span></span> <span data-ttu-id="f0664-516">既定値は `false` です。</span><span class="sxs-lookup"><span data-stu-id="f0664-516">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="f0664-517">使用例</span><span class="sxs-lookup"><span data-stu-id="f0664-517">Examples</span></span>

<span data-ttu-id="f0664-518">現在のディレクトリに、F# コンソール アプリケーション プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f0664-518">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="f0664-519">指定したディレクトリ内に .NET 標準クラス ライブラリ プロジェクトを作成します (.NET Core SDK 2.0 またはそれ以降のバージョンでのみ使用可能)。</span><span class="sxs-lookup"><span data-stu-id="f0664-519">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="f0664-520">認証なしで、現在のディレクトリに新しい ASP.NET Core C# MVC アプリケーション プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f0664-520">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="f0664-521">新しい xUnit アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="f0664-521">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="f0664-522">MVC に利用できるすべてのテンプレートを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="f0664-522">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="f0664-523">ASP.NET Core のシングル ページ アプリケーション テンプレートのバージョン 2.0 をインストールします (コマンド オプションは .NET Core SDK 1.1 以降のバージョンでのみ使用できます):</span><span class="sxs-lookup"><span data-stu-id="f0664-523">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="f0664-524">SDK バージョン 2.0.0 (.NET Core SDK 2.0 以降のバージョンでのみ使用できます) を設定している現在のディレクトリ内に *global.json* を作成します。</span><span class="sxs-lookup"><span data-stu-id="f0664-524">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="f0664-525">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0664-525">See also</span></span>

* [<span data-ttu-id="f0664-526">dotnet new のカスタム テンプレート</span><span class="sxs-lookup"><span data-stu-id="f0664-526">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="f0664-527">dotnet new のカスタム テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="f0664-527">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* [<span data-ttu-id="f0664-528">dotnet/dotnet-template-samples GitHub リポジトリ</span><span class="sxs-lookup"><span data-stu-id="f0664-528">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)  
* [<span data-ttu-id="f0664-529">dotnet new で使用できるテンプレート</span><span class="sxs-lookup"><span data-stu-id="f0664-529">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
