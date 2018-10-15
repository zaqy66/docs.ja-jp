---
title: dotnet new コマンド - .NET Core CLI
description: dotnet new コマンドは、指定されたテンプレートに基づいて新しい .NET Core プロジェクトを作成します。
author: mairaw
ms.author: mairaw
ms.date: 07/31/2018
ms.openlocfilehash: 2c82dda2d93225edb360316637e22964135cd5e4
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43512556"
---
# <a name="dotnet-new"></a><span data-ttu-id="6cc53-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="6cc53-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="6cc53-104">name</span><span class="sxs-lookup"><span data-stu-id="6cc53-104">Name</span></span>

<span data-ttu-id="6cc53-105">`dotnet new` - 指定したテンプレートに基づいて、新しいプロジェクト、構成ファイル、またはソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="6cc53-106">構文</span><span class="sxs-lookup"><span data-stu-id="6cc53-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="6cc53-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="6cc53-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="6cc53-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="6cc53-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="6cc53-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="6cc53-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="6cc53-110">説明</span><span class="sxs-lookup"><span data-stu-id="6cc53-110">Description</span></span>

<span data-ttu-id="6cc53-111">`dotnet new` コマンドは、有効な .NET Core プロジェクトを初期化する便利な手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="6cc53-112">このコマンドは、[テンプレート エンジン](https://github.com/dotnet/templating)を呼び出し、指定されたテンプレートとオプションに基づいて、ディスク上に成果物を作成します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="6cc53-113">引数</span><span class="sxs-lookup"><span data-stu-id="6cc53-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="6cc53-114">コマンドが呼び出されたときにインスタンス化するテンプレート。</span><span class="sxs-lookup"><span data-stu-id="6cc53-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="6cc53-115">各テンプレートには、渡すことができるオプションが存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="6cc53-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="6cc53-116">詳細については、[テンプレートのオプション](#template-options)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc53-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="6cc53-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="6cc53-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="6cc53-118">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6cc53-118">The command contains a default list of templates.</span></span> <span data-ttu-id="6cc53-119">使用可能なテンプレートの一覧を取得するには、`dotnet new -l` を使います。</span><span class="sxs-lookup"><span data-stu-id="6cc53-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="6cc53-120">次の表は、.NET Core SDK 2.1.300 にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="6cc53-121">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="6cc53-122">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="6cc53-122">Template description</span></span>                          | <span data-ttu-id="6cc53-123">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="6cc53-123">Template name</span></span>   | <span data-ttu-id="6cc53-124">言語</span><span class="sxs-lookup"><span data-stu-id="6cc53-124">Languages</span></span>     |
|----------------------------------------------|-----------------|---------------|
| <span data-ttu-id="6cc53-125">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6cc53-125">Console application</span></span>                          | `console`       | <span data-ttu-id="6cc53-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="6cc53-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="6cc53-127">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="6cc53-127">Class library</span></span>                                | `classlib`      | <span data-ttu-id="6cc53-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="6cc53-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="6cc53-129">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="6cc53-129">Unit test project</span></span>                            | `mstest`        | <span data-ttu-id="6cc53-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="6cc53-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="6cc53-131">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="6cc53-131">xUnit test project</span></span>                           | `xunit`         | <span data-ttu-id="6cc53-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="6cc53-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="6cc53-133">Razor ページ</span><span class="sxs-lookup"><span data-stu-id="6cc53-133">Razor page</span></span>                                   | `page`          | <span data-ttu-id="6cc53-134">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-134">[C#]</span></span>          |
| <span data-ttu-id="6cc53-135">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="6cc53-135">MVC ViewImports</span></span>                              | `viewimports`   | <span data-ttu-id="6cc53-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-136">[C#]</span></span>          |
| <span data-ttu-id="6cc53-137">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="6cc53-137">MVC ViewStart</span></span>                                | `viewstart`     | <span data-ttu-id="6cc53-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-138">[C#]</span></span>          |
| <span data-ttu-id="6cc53-139">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="6cc53-139">ASP.NET Core empty</span></span>                           | `web`           | <span data-ttu-id="6cc53-140">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="6cc53-140">[C#], F#</span></span>      |
| <span data-ttu-id="6cc53-141">ASP.NET Core Web アプリ (モデル ビュー コントローラー)</span><span class="sxs-lookup"><span data-stu-id="6cc53-141">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`           | <span data-ttu-id="6cc53-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="6cc53-142">[C#], F#</span></span>      |
| <span data-ttu-id="6cc53-143">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="6cc53-143">ASP.NET Core Web App</span></span>                         | `razor`         | <span data-ttu-id="6cc53-144">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-144">[C#]</span></span>          |
| <span data-ttu-id="6cc53-145">Angular 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="6cc53-145">ASP.NET Core with Angular</span></span>                    | `angular`       | <span data-ttu-id="6cc53-146">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-146">[C#]</span></span>          |
| <span data-ttu-id="6cc53-147">React.js 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="6cc53-147">ASP.NET Core with React.js</span></span>                   | `react`         | <span data-ttu-id="6cc53-148">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-148">[C#]</span></span>          |
| <span data-ttu-id="6cc53-149">React.js および Redux 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="6cc53-149">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`    | <span data-ttu-id="6cc53-150">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-150">[C#]</span></span>          |
| <span data-ttu-id="6cc53-151">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="6cc53-151">ASP.NET Core Web API</span></span>                         | `webapi`        | <span data-ttu-id="6cc53-152">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="6cc53-152">[C#], F#</span></span>      |
| <span data-ttu-id="6cc53-153">Razor クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="6cc53-153">Razor class library</span></span>                          | `razorclasslib` | <span data-ttu-id="6cc53-154">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-154">[C#]</span></span>          |
| <span data-ttu-id="6cc53-155">global.json file</span><span class="sxs-lookup"><span data-stu-id="6cc53-155">global.json file</span></span>                             | `globaljson`    |               |
| <span data-ttu-id="6cc53-156">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="6cc53-156">NuGet config</span></span>                                 | `nugetconfig`   |               |
| <span data-ttu-id="6cc53-157">Web 構成</span><span class="sxs-lookup"><span data-stu-id="6cc53-157">Web config</span></span>                                   | `webconfig`     |               |
| <span data-ttu-id="6cc53-158">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="6cc53-158">Solution file</span></span>                                | `sln`           |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="6cc53-159">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="6cc53-159">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="6cc53-160">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6cc53-160">The command contains a default list of templates.</span></span> <span data-ttu-id="6cc53-161">使用可能なテンプレートの一覧を取得するには、`dotnet new -l` を使います。</span><span class="sxs-lookup"><span data-stu-id="6cc53-161">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="6cc53-162">次の表は、.NET Core SDK 2.0 にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-162">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="6cc53-163">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-163">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="6cc53-164">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="6cc53-164">Template description</span></span>                          | <span data-ttu-id="6cc53-165">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="6cc53-165">Template name</span></span> | <span data-ttu-id="6cc53-166">言語</span><span class="sxs-lookup"><span data-stu-id="6cc53-166">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="6cc53-167">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6cc53-167">Console application</span></span>                          | `console`     | <span data-ttu-id="6cc53-168">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="6cc53-168">[C#], F#, VB</span></span>  |
| <span data-ttu-id="6cc53-169">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="6cc53-169">Class library</span></span>                                | `classlib`    | <span data-ttu-id="6cc53-170">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="6cc53-170">[C#], F#, VB</span></span>  |
| <span data-ttu-id="6cc53-171">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="6cc53-171">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="6cc53-172">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="6cc53-172">[C#], F#, VB</span></span>  |
| <span data-ttu-id="6cc53-173">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="6cc53-173">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="6cc53-174">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="6cc53-174">[C#], F#, VB</span></span>  |
| <span data-ttu-id="6cc53-175">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="6cc53-175">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="6cc53-176">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="6cc53-176">[C#], F#</span></span>      |
| <span data-ttu-id="6cc53-177">ASP.NET Core Web アプリ (モデル ビュー コントローラー)</span><span class="sxs-lookup"><span data-stu-id="6cc53-177">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="6cc53-178">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="6cc53-178">[C#], F#</span></span>      |
| <span data-ttu-id="6cc53-179">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="6cc53-179">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="6cc53-180">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-180">[C#]</span></span>          |
| <span data-ttu-id="6cc53-181">Angular 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="6cc53-181">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="6cc53-182">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-182">[C#]</span></span>          |
| <span data-ttu-id="6cc53-183">React.js 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="6cc53-183">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="6cc53-184">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-184">[C#]</span></span>          |
| <span data-ttu-id="6cc53-185">React.js および Redux 付きの ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="6cc53-185">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="6cc53-186">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-186">[C#]</span></span>          |
| <span data-ttu-id="6cc53-187">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="6cc53-187">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="6cc53-188">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="6cc53-188">[C#], F#</span></span>      |
| <span data-ttu-id="6cc53-189">global.json file</span><span class="sxs-lookup"><span data-stu-id="6cc53-189">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="6cc53-190">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="6cc53-190">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="6cc53-191">Web 構成</span><span class="sxs-lookup"><span data-stu-id="6cc53-191">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="6cc53-192">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="6cc53-192">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="6cc53-193">Razor ページ</span><span class="sxs-lookup"><span data-stu-id="6cc53-193">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="6cc53-194">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="6cc53-194">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="6cc53-195">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="6cc53-195">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="6cc53-196">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="6cc53-196">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="6cc53-197">このコマンドには、テンプレートの既定の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6cc53-197">The command contains a default list of templates.</span></span> <span data-ttu-id="6cc53-198">使用可能なテンプレートの一覧を取得するには、`dotnet new -all` を使います。</span><span class="sxs-lookup"><span data-stu-id="6cc53-198">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="6cc53-199">次の表は、.NET Core SDK 1.x にプレインストールされているテンプレートの一覧です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-199">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="6cc53-200">テンプレートの既定の言語は、角かっこで示されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-200">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="6cc53-201">テンプレートの説明</span><span class="sxs-lookup"><span data-stu-id="6cc53-201">Template description</span></span>  | <span data-ttu-id="6cc53-202">テンプレート名</span><span class="sxs-lookup"><span data-stu-id="6cc53-202">Template name</span></span> | <span data-ttu-id="6cc53-203">言語</span><span class="sxs-lookup"><span data-stu-id="6cc53-203">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="6cc53-204">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6cc53-204">Console application</span></span>  | `console`     | <span data-ttu-id="6cc53-205">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="6cc53-205">[C#], F#</span></span>  |
| <span data-ttu-id="6cc53-206">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="6cc53-206">Class library</span></span>        | `classlib`    | <span data-ttu-id="6cc53-207">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="6cc53-207">[C#], F#</span></span>  |
| <span data-ttu-id="6cc53-208">単体テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="6cc53-208">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="6cc53-209">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="6cc53-209">[C#], F#</span></span>  |
| <span data-ttu-id="6cc53-210">xUnit テスト プロジェクト</span><span class="sxs-lookup"><span data-stu-id="6cc53-210">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="6cc53-211">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="6cc53-211">[C#], F#</span></span>  |
| <span data-ttu-id="6cc53-212">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="6cc53-212">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="6cc53-213">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-213">[C#]</span></span>      |
| <span data-ttu-id="6cc53-214">ASP.NET Core Web アプリ</span><span class="sxs-lookup"><span data-stu-id="6cc53-214">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="6cc53-215">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="6cc53-215">[C#], F#</span></span>  |
| <span data-ttu-id="6cc53-216">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="6cc53-216">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="6cc53-217">[C#]</span><span class="sxs-lookup"><span data-stu-id="6cc53-217">[C#]</span></span>      |
| <span data-ttu-id="6cc53-218">NuGet 構成</span><span class="sxs-lookup"><span data-stu-id="6cc53-218">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="6cc53-219">Web 構成</span><span class="sxs-lookup"><span data-stu-id="6cc53-219">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="6cc53-220">ソリューション ファイル</span><span class="sxs-lookup"><span data-stu-id="6cc53-220">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="6cc53-221">オプション</span><span class="sxs-lookup"><span data-stu-id="6cc53-221">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="6cc53-222">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="6cc53-222">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="6cc53-223">既存のファイルを変更する場合でも、コンテンツが強制的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-223">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="6cc53-224">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-224">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="6cc53-225">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-225">Prints out help for the command.</span></span> <span data-ttu-id="6cc53-226">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-226">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="6cc53-227">指定された `PATH` または `NUGET_ID` からソース パックまたはテンプレート パックをインストールします。</span><span class="sxs-lookup"><span data-stu-id="6cc53-227">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="6cc53-228">テンプレート パッケージのプレリリース版をインストールする場合は、`<package-name>::<package-version>` の形式でバージョンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cc53-228">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="6cc53-229">既定では、`dotnet new` は、バージョンに対して \* を渡します。これは最後の安定したパッケージのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-229">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="6cc53-230">「[使用例](#examples)」のセクションで、例をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="6cc53-230">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="6cc53-231">カスタム テンプレートの作成方法については、[「dotnet new のカスタム テンプレート」](custom-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc53-231">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="6cc53-232">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-232">Lists templates containing the specified name.</span></span> <span data-ttu-id="6cc53-233">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-233">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="6cc53-234">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-234">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="6cc53-235">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="6cc53-235">The language of the template to create.</span></span> <span data-ttu-id="6cc53-236">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="6cc53-236">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="6cc53-237">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-237">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="6cc53-238">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-238">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="6cc53-239">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cc53-239">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="6cc53-240">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-240">The name for the created output.</span></span> <span data-ttu-id="6cc53-241">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-241">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="6cc53-242">インストール中に使用する NuGet ソースを 1 つ指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-242">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="6cc53-243">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="6cc53-243">Location to place the generated output.</span></span> <span data-ttu-id="6cc53-244">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-244">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="6cc53-245">使用可能な種類に基づいて、テンプレートをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-245">Filters templates based on available types.</span></span> <span data-ttu-id="6cc53-246">定義済みの値は、"project"、"item"、または "other" です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-246">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="6cc53-247">指定された `PATH` または `NUGET_ID` で、ソース パックまたはテンプレート パックをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="6cc53-247">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="6cc53-248">`PATH` を使用してテンプレートをアンインストールするには、完全修飾パスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cc53-248">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="6cc53-249">たとえば、*C:/Users/\<ユーザー>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* は有効ですが、*./GarciaSoftware.ConsoleTemplate.CSharp* が含まれるフォルダーから、そのパスを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-249">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="6cc53-250">また、テンプレートのパスの最後にある終端ディレクトリのスラッシュは含めないでください。</span><span class="sxs-lookup"><span data-stu-id="6cc53-250">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="6cc53-251">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="6cc53-251">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="6cc53-252">既存のファイルを変更する場合でも、コンテンツが強制的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-252">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="6cc53-253">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-253">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="6cc53-254">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-254">Prints out help for the command.</span></span> <span data-ttu-id="6cc53-255">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-255">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="6cc53-256">指定された `PATH` または `NUGET_ID` からソース パックまたはテンプレート パックをインストールします。</span><span class="sxs-lookup"><span data-stu-id="6cc53-256">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="6cc53-257">テンプレート パッケージのプレリリース版をインストールする場合は、`<package-name>::<package-version>` の形式でバージョンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cc53-257">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="6cc53-258">既定では、`dotnet new` は、バージョンに対して \* を渡します。これは最後の安定したパッケージのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-258">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="6cc53-259">「[使用例](#examples)」のセクションで、例をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="6cc53-259">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="6cc53-260">カスタム テンプレートの作成方法については、[「dotnet new のカスタム テンプレート」](custom-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cc53-260">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="6cc53-261">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-261">Lists templates containing the specified name.</span></span> <span data-ttu-id="6cc53-262">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-262">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="6cc53-263">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-263">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="6cc53-264">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="6cc53-264">The language of the template to create.</span></span> <span data-ttu-id="6cc53-265">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="6cc53-265">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="6cc53-266">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-266">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="6cc53-267">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-267">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="6cc53-268">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cc53-268">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="6cc53-269">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-269">The name for the created output.</span></span> <span data-ttu-id="6cc53-270">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-270">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="6cc53-271">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="6cc53-271">Location to place the generated output.</span></span> <span data-ttu-id="6cc53-272">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-272">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="6cc53-273">使用可能な種類に基づいて、テンプレートをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-273">Filters templates based on available types.</span></span> <span data-ttu-id="6cc53-274">定義済みの値は、"project"、"item"、または "other" です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-274">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="6cc53-275">指定された `PATH` または `NUGET_ID` で、ソース パックまたはテンプレート パックをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="6cc53-275">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="6cc53-276">`PATH` を使用してテンプレートをアンインストールするには、完全修飾パスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cc53-276">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="6cc53-277">たとえば、*C:/Users/\<ユーザー>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* は有効ですが、*./GarciaSoftware.ConsoleTemplate.CSharp* が含まれるフォルダーから、そのパスを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-277">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="6cc53-278">また、テンプレートのパスの最後にある終端ディレクトリのスラッシュは含めないでください。</span><span class="sxs-lookup"><span data-stu-id="6cc53-278">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="6cc53-279">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="6cc53-279">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="6cc53-280">`dotnet new` コマンドのコンテキストでのみ実行すると、特定の種類のプロジェクトに対するすべてのテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-280">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="6cc53-281">`dotnet new web -all` など、特定のテンプレートのコンテキストで実行すると、`-all` は強制作成フラグとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-281">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="6cc53-282">これは、出力ディレクトリに既にプロジェクトが含まれている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-282">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="6cc53-283">コマンドのヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-283">Prints out help for the command.</span></span> <span data-ttu-id="6cc53-284">`dotnet new` コマンド自体、または `dotnet new mvc --help` などの任意のテンプレートに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-284">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="6cc53-285">指定した名前を含むテンプレートを列挙します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-285">Lists templates containing the specified name.</span></span> <span data-ttu-id="6cc53-286">`dotnet new` コマンドに対して呼び出すと、指定されたディレクトリで使用できるテンプレートが列挙されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-286">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="6cc53-287">たとえば、ディレクトリに既にプロジェクトが含まれている場合、すべてのプロジェクト テンプレートは列挙されません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-287">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="6cc53-288">作成するテンプレートの言語。</span><span class="sxs-lookup"><span data-stu-id="6cc53-288">The language of the template to create.</span></span> <span data-ttu-id="6cc53-289">使用できる言語は、テンプレートによって異なります ([引数](#arguments)の既定値を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="6cc53-289">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="6cc53-290">一部のテンプレートでは無効です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-290">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="6cc53-291">一部のシェルは `#` を特殊文字として解釈します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-291">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="6cc53-292">そのような場合は、`dotnet new console -lang "F#"` などの言語パラメーター値を囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cc53-292">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="6cc53-293">作成される出力の名前です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-293">The name for the created output.</span></span> <span data-ttu-id="6cc53-294">名前が指定されていない場合、現在のディレクトリの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-294">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="6cc53-295">生成された出力を配置する場所。</span><span class="sxs-lookup"><span data-stu-id="6cc53-295">Location to place the generated output.</span></span> <span data-ttu-id="6cc53-296">既定値は、現在のディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-296">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="6cc53-297">テンプレート オプション</span><span class="sxs-lookup"><span data-stu-id="6cc53-297">Template options</span></span>

<span data-ttu-id="6cc53-298">プロジェクト テンプレートはそれぞれ、追加のオプションが与えられている場合があります。</span><span class="sxs-lookup"><span data-stu-id="6cc53-298">Each project template may have additional options available.</span></span> <span data-ttu-id="6cc53-299">コア テンプレートの場合、次のオプションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="6cc53-299">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="6cc53-300">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="6cc53-300">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="6cc53-301">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="6cc53-301">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="6cc53-302">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-302">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-303">**classlib**</span><span class="sxs-lookup"><span data-stu-id="6cc53-303">**classlib**</span></span>

<span data-ttu-id="6cc53-304">`-f|--framework <FRAMEWORK>` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-304">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="6cc53-305">値: .NET Core クラス ライブラリを作成するには `netcoreapp2.0`、.NET 標準クラス ライブラリを作成するには `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-305">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="6cc53-306">既定値は `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-306">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="6cc53-307">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-307">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-308">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="6cc53-308">**mstest, xunit**</span></span>

<span data-ttu-id="6cc53-309">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md) を使用してプロジェクトのパッケージ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="6cc53-309">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="6cc53-310">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-310">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-311">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="6cc53-311">**globaljson**</span></span>

<span data-ttu-id="6cc53-312">`--sdk-version <VERSION_NUMBER>` - *global.json* ファイル内で使用する .NET Core SDK のバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-312">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="6cc53-313">**web**</span><span class="sxs-lookup"><span data-stu-id="6cc53-313">**web**</span></span>

<span data-ttu-id="6cc53-314">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-314">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="6cc53-315">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-315">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-316">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-316">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="6cc53-317">このオプションは、`IndividualAuth` または `OrganizationalAuth` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-317">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="6cc53-318">**webapi**</span><span class="sxs-lookup"><span data-stu-id="6cc53-318">**webapi**</span></span>

<span data-ttu-id="6cc53-319">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="6cc53-319">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="6cc53-320">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-320">The possible values are:</span></span>

- <span data-ttu-id="6cc53-321">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="6cc53-321">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="6cc53-322">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-322">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="6cc53-323">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-323">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="6cc53-324">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-324">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="6cc53-325">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="6cc53-325">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="6cc53-326">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-326">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="6cc53-327">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-327">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="6cc53-328">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-328">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="6cc53-329">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-329">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-330">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-330">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="6cc53-331">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-331">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="6cc53-332">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-332">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="6cc53-333">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-333">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="6cc53-334">`IndividualB2C` 認証または `SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-334">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="6cc53-335">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-335">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="6cc53-336">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-336">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="6cc53-337">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-337">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="6cc53-338">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-338">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="6cc53-339">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-339">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="6cc53-340">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-340">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="6cc53-341">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-341">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="6cc53-342">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-342">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="6cc53-343">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-343">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="6cc53-344">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-344">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="6cc53-345">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-345">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="6cc53-346">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-346">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-347">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-347">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-348">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-348">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="6cc53-349">`app.UseHsts` と `app.UseHttpsRedirection` は `Startup.Configure` に追加されません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-349">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="6cc53-350">このオプションは、`Individual`、`IndividualB2C`、`SingleOrg`、または `MultiOrg` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-350">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="6cc53-351">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="6cc53-351">**mvc, razor**</span></span>

<span data-ttu-id="6cc53-352">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="6cc53-352">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="6cc53-353">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-353">The possible values are:</span></span>

- <span data-ttu-id="6cc53-354">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="6cc53-354">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="6cc53-355">`Individual` - 個別認証です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-355">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="6cc53-356">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-356">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="6cc53-357">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-357">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="6cc53-358">`MultiOrg` - 複数のテナントに対する組織認証です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-358">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="6cc53-359">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-359">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="6cc53-360">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="6cc53-360">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="6cc53-361">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-361">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="6cc53-362">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-362">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="6cc53-363">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-363">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="6cc53-364">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-364">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-365">`-rp|--reset-password-policy-id <ID>` - このプロジェクトのリセット パスワード ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-365">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="6cc53-366">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-366">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-367">`-ep|--edit-profile-policy-id <ID>` - このプロジェクトの編集プロファイル ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-367">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="6cc53-368">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-368">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-369">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-369">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="6cc53-370">`SingleOrg` 認証または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-370">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="6cc53-371">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-371">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="6cc53-372">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-372">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="6cc53-373">`IndividualB2C` 認証、`SingleOrg` 認証、または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-373">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="6cc53-374">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-374">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="6cc53-375">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-375">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="6cc53-376">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-376">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="6cc53-377">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-377">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="6cc53-378">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-378">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="6cc53-379">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-379">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="6cc53-380">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-380">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="6cc53-381">`--callback-path <PATH>` - リダイレクト URI のアプリケーションの基本パス内の要求パスです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-381">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="6cc53-382">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-382">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="6cc53-383">既定値は `/signin-oidc` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-383">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="6cc53-384">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-384">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="6cc53-385">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-385">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="6cc53-386">`--exclude-launch-settings` - 生成されたテンプレートから *launchSettings.json* を除外します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-386">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="6cc53-387">`--use-browserlink` - プロジェクトに BrowserLink を含めます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-387">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="6cc53-388">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-388">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="6cc53-389">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-389">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-390">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-390">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-391">`--no-https` - プロジェクトは HTTPS を必要としません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-391">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="6cc53-392">`app.UseHsts` と `app.UseHttpsRedirection` は `Startup.Configure` に追加されません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-392">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="6cc53-393">このオプションは、`Individual`、`IndividualB2C`、`SingleOrg`、または `MultiOrg` が使用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-393">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="6cc53-394">**page**</span><span class="sxs-lookup"><span data-stu-id="6cc53-394">**page**</span></span>

<span data-ttu-id="6cc53-395">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-395">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="6cc53-396">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-396">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="6cc53-397">`-np|--no-pagemodel` - PageModel なしでページを作成します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-397">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="6cc53-398">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="6cc53-398">**viewimports**</span></span>

<span data-ttu-id="6cc53-399">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-399">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="6cc53-400">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-400">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="6cc53-401">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="6cc53-401">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="6cc53-402">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="6cc53-402">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="6cc53-403">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-403">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-404">**classlib**</span><span class="sxs-lookup"><span data-stu-id="6cc53-404">**classlib**</span></span>

<span data-ttu-id="6cc53-405">`-f|--framework <FRAMEWORK>` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-405">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="6cc53-406">値: .NET Core クラス ライブラリを作成するには `netcoreapp2.0`、.NET 標準クラス ライブラリを作成するには `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-406">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="6cc53-407">既定値は `netstandard2.0` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-407">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="6cc53-408">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-408">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-409">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="6cc53-409">**mstest, xunit**</span></span>

<span data-ttu-id="6cc53-410">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md) を使用してプロジェクトのパッケージ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="6cc53-410">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="6cc53-411">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-411">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-412">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="6cc53-412">**globaljson**</span></span>

<span data-ttu-id="6cc53-413">`--sdk-version <VERSION_NUMBER>` - *global.json* ファイル内で使用する .NET Core SDK のバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-413">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="6cc53-414">**web**</span><span class="sxs-lookup"><span data-stu-id="6cc53-414">**web**</span></span>

<span data-ttu-id="6cc53-415">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-415">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="6cc53-416">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-416">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-417">**webapi**</span><span class="sxs-lookup"><span data-stu-id="6cc53-417">**webapi**</span></span>

<span data-ttu-id="6cc53-418">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="6cc53-418">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="6cc53-419">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-419">The possible values are:</span></span>

- <span data-ttu-id="6cc53-420">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="6cc53-420">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="6cc53-421">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-421">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="6cc53-422">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-422">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="6cc53-423">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-423">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="6cc53-424">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="6cc53-424">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="6cc53-425">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-425">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="6cc53-426">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-426">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="6cc53-427">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-427">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="6cc53-428">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-428">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-429">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-429">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="6cc53-430">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-430">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="6cc53-431">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-431">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="6cc53-432">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-432">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="6cc53-433">`IndividualB2C` 認証または `SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-433">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="6cc53-434">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-434">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="6cc53-435">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-435">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="6cc53-436">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-436">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="6cc53-437">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-437">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="6cc53-438">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-438">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="6cc53-439">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-439">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="6cc53-440">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-440">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="6cc53-441">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-441">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="6cc53-442">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-442">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="6cc53-443">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-443">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="6cc53-444">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-444">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="6cc53-445">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-445">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-446">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-446">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-447">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="6cc53-447">**mvc, razor**</span></span>

<span data-ttu-id="6cc53-448">`-au|--auth <AUTHENTICATION_TYPE>` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="6cc53-448">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="6cc53-449">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-449">The possible values are:</span></span>

- <span data-ttu-id="6cc53-450">`None` - 認証は行われません (既定)。</span><span class="sxs-lookup"><span data-stu-id="6cc53-450">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="6cc53-451">`Individual` - 個別認証です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-451">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="6cc53-452">`IndividualB2C` - Azure AD B2C での個別認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-452">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="6cc53-453">`SingleOrg` - 単一のテナントに対する組織認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-453">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="6cc53-454">`MultiOrg` - 複数のテナントに対する組織認証です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-454">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="6cc53-455">`Windows` - Windows 認証。</span><span class="sxs-lookup"><span data-stu-id="6cc53-455">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="6cc53-456">`--aad-b2c-instance <INSTANCE>` - 接続先の Azure Active Directory B2C インスタンス。</span><span class="sxs-lookup"><span data-stu-id="6cc53-456">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="6cc53-457">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-457">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="6cc53-458">既定値は `https://login.microsoftonline.com/tfp/` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-458">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="6cc53-459">`-ssp|--susi-policy-id <ID>` - このプロジェクト用のサインインおよびサインアップ ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-459">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="6cc53-460">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-460">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-461">`-rp|--reset-password-policy-id <ID>` - このプロジェクトのリセット パスワード ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-461">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="6cc53-462">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-462">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-463">`-ep|--edit-profile-policy-id <ID>` - このプロジェクトの編集プロファイル ポリシー ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-463">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="6cc53-464">`IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-464">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-465">`--aad-instance <INSTANCE>` - 接続先の Azure Active Directory インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-465">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="6cc53-466">`SingleOrg` 認証または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-466">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="6cc53-467">既定値は `https://login.microsoftonline.com/` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-467">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="6cc53-468">`--client-id <ID>` - このプロジェクトのクライアント ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-468">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="6cc53-469">`IndividualB2C` 認証、`SingleOrg` 認証、または `MultiOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-469">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="6cc53-470">既定値は `11111111-1111-1111-11111111111111111` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-470">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="6cc53-471">`--domain <DOMAIN>` - ディレクトリ テナントのドメインです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-471">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="6cc53-472">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-472">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="6cc53-473">既定値は `qualified.domain.name` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-473">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="6cc53-474">`--tenant-id <ID>` - 接続先のディレクトリの TenantId ID です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-474">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="6cc53-475">`SingleOrg` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-475">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="6cc53-476">既定値は `22222222-2222-2222-2222-222222222222` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-476">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="6cc53-477">`--callback-path <PATH>` - リダイレクト URI のアプリケーションの基本パス内の要求パスです。</span><span class="sxs-lookup"><span data-stu-id="6cc53-477">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="6cc53-478">`SingleOrg` 認証または `IndividualB2C` 認証で使用します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-478">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="6cc53-479">既定値は `/signin-oidc` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-479">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="6cc53-480">`-r|--org-read-access` - このアプリケーションにディレクトリへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-480">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="6cc53-481">`SingleOrg` 認証または `MultiOrg` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-481">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="6cc53-482">`--use-launch-settings` - 生成されたテンプレート出力に *launchSettings.json* を含めます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-482">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="6cc53-483">`--use-browserlink` - プロジェクトに BrowserLink を含めます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-483">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="6cc53-484">`-uld|--use-local-db` - SQLite ではなく LocalDB が使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-484">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="6cc53-485">`Individual` 認証または `IndividualB2C` 認証にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cc53-485">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="6cc53-486">`--no-restore` - プロジェクトの作成中には暗黙的な復元を実行しません。</span><span class="sxs-lookup"><span data-stu-id="6cc53-486">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="6cc53-487">**page**</span><span class="sxs-lookup"><span data-stu-id="6cc53-487">**page**</span></span>

<span data-ttu-id="6cc53-488">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-488">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="6cc53-489">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-489">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="6cc53-490">`-np|--no-pagemodel` - PageModel なしでページを作成します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-490">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="6cc53-491">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="6cc53-491">**viewimports**</span></span>

<span data-ttu-id="6cc53-492">`-na|--namespace <NAMESPACE_NAME>` - 生成するコードの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-492">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="6cc53-493">既定値は `MyApp.Namespace` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-493">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="6cc53-494">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="6cc53-494">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="6cc53-495">**console、xunit、mstest、web、webapi**</span><span class="sxs-lookup"><span data-stu-id="6cc53-495">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="6cc53-496">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-496">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="6cc53-497">値: `netcoreapp1.0` または `netcoreapp1.1` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-497">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="6cc53-498">既定値は `netcoreapp1.0` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-498">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="6cc53-499">**classlib**</span><span class="sxs-lookup"><span data-stu-id="6cc53-499">**classlib**</span></span>

<span data-ttu-id="6cc53-500">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-500">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="6cc53-501">値: `netcoreapp1.0`、`netcoreapp1.1`、または `netstandard1.0` から `netstandard1.6` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-501">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="6cc53-502">既定値は `netstandard1.4` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-502">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="6cc53-503">**mvc**</span><span class="sxs-lookup"><span data-stu-id="6cc53-503">**mvc**</span></span>

<span data-ttu-id="6cc53-504">`-f|--framework` - ターゲットにする[フレームワーク](../../standard/frameworks.md)を指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-504">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="6cc53-505">値: `netcoreapp1.0` または `netcoreapp1.1` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-505">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="6cc53-506">既定値は `netcoreapp1.0` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-506">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="6cc53-507">`-au|--auth` - 使う認証の種類。</span><span class="sxs-lookup"><span data-stu-id="6cc53-507">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="6cc53-508">値: `None` または `Individual` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-508">Values: `None` or `Individual`.</span></span> <span data-ttu-id="6cc53-509">既定値は `None` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-509">The default value is `None`.</span></span>

<span data-ttu-id="6cc53-510">`-uld|--use-local-db` - SQLite の代わりに LocalDB を使うかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-510">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="6cc53-511">値: `true` または `false` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-511">Values: `true` or `false`.</span></span> <span data-ttu-id="6cc53-512">既定値は `false` です。</span><span class="sxs-lookup"><span data-stu-id="6cc53-512">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="6cc53-513">使用例</span><span class="sxs-lookup"><span data-stu-id="6cc53-513">Examples</span></span>

<span data-ttu-id="6cc53-514">現在のディレクトリに、F# コンソール アプリケーション プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-514">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="6cc53-515">指定したディレクトリ内に .NET 標準クラス ライブラリ プロジェクトを作成します (.NET Core SDK 2.0 またはそれ以降のバージョンでのみ使用可能)。</span><span class="sxs-lookup"><span data-stu-id="6cc53-515">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="6cc53-516">認証なしで、現在のディレクトリに新しい ASP.NET Core C# MVC アプリケーション プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-516">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="6cc53-517">新しい xUnit アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-517">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="6cc53-518">MVC に利用できるすべてのテンプレートを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-518">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="6cc53-519">ASP.NET Core のシングル ページ アプリケーション テンプレートのバージョン 2.0 をインストールします (コマンド オプションは .NET Core SDK 1.1 以降のバージョンでのみ使用できます):</span><span class="sxs-lookup"><span data-stu-id="6cc53-519">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="6cc53-520">SDK バージョン 2.0.0 (.NET Core SDK 2.0 以降のバージョンでのみ使用できます) を設定している現在のディレクトリ内に *global.json* を作成します。</span><span class="sxs-lookup"><span data-stu-id="6cc53-520">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="6cc53-521">関連項目</span><span class="sxs-lookup"><span data-stu-id="6cc53-521">See also</span></span>

* [<span data-ttu-id="6cc53-522">dotnet new のカスタム テンプレート</span><span class="sxs-lookup"><span data-stu-id="6cc53-522">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="6cc53-523">dotnet new のカスタム テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="6cc53-523">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* [<span data-ttu-id="6cc53-524">dotnet/dotnet-template-samples GitHub リポジトリ</span><span class="sxs-lookup"><span data-stu-id="6cc53-524">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)  
* [<span data-ttu-id="6cc53-525">dotnet new で使用できるテンプレート</span><span class="sxs-lookup"><span data-stu-id="6cc53-525">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
