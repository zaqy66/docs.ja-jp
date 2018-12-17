---
title: dotnet add package コマンド - .NET Core CLI
description: "'dotnet add package' コマンドは、NuGet パッケージ参照をプロジェクトに追加する便利なオプションを提供します。"
ms.date: 12/04/2018
ms.openlocfilehash: 8227e5a86a888f850304e8b94f46c7d31779653f
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53150824"
---
# <a name="dotnet-add-package"></a><span data-ttu-id="e655a-103">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="e655a-103">dotnet add package</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="e655a-104">name</span><span class="sxs-lookup"><span data-stu-id="e655a-104">Name</span></span>

<span data-ttu-id="e655a-105">`dotnet add package` - プロジェクト ファイルにパッケージ参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="e655a-105">`dotnet add package` - Adds a package reference to a project file.</span></span>

## <a name="synopsis"></a><span data-ttu-id="e655a-106">構文</span><span class="sxs-lookup"><span data-stu-id="e655a-106">Synopsis</span></span>

`dotnet add [<PROJECT>] package <PACKAGE_NAME> [-h|--help] [-f|--framework] [--interactive] [-n|--no-restore] [--package-directory] [-s|--source] [-v|--version]`

## <a name="description"></a><span data-ttu-id="e655a-107">説明</span><span class="sxs-lookup"><span data-stu-id="e655a-107">Description</span></span>

<span data-ttu-id="e655a-108">`dotnet add package` コマンドは、プロジェクト ファイルにパッケージ参照を追加する便利なオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="e655a-108">The `dotnet add package` command provides a convenient option to add a package reference to a project file.</span></span> <span data-ttu-id="e655a-109">このコマンドの実行後に、パッケージがプロジェクト内のフレームワークと互換性があることを確認する互換性チェックがあります。</span><span class="sxs-lookup"><span data-stu-id="e655a-109">After running the command, there's a compatibility check to ensure the package is compatible with the frameworks in the project.</span></span> <span data-ttu-id="e655a-110">互換性チェックに合格すると、`<PackageReference>` 要素がプロジェクト ファイルに追加されて、[dotnet restore](dotnet-restore.md) が実行されます。</span><span class="sxs-lookup"><span data-stu-id="e655a-110">If the check passes, a `<PackageReference>` element is added to the project file and [dotnet restore](dotnet-restore.md) is run.</span></span>

[!INCLUDE[DotNet Restore Note](../../../includes/dotnet-restore-note.md)]

<span data-ttu-id="e655a-111">たとえば、`Newtonsoft.Json` を *ToDo.csproj* に追加すると、次のような出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="e655a-111">For example, adding `Newtonsoft.Json` to *ToDo.csproj* produces output similar to the following example:</span></span>

```console
  Writing C:\Users\mairaw\AppData\Local\Temp\tmp95A8.tmp
info : Adding PackageReference for package 'Newtonsoft.Json' into project 'C:\projects\ToDo\ToDo.csproj'.
log  : Restoring packages for C:\Temp\projects\consoleproj\consoleproj.csproj...
info :   GET https://api.nuget.org/v3-flatcontainer/newtonsoft.json/index.json
info :   OK https://api.nuget.org/v3-flatcontainer/newtonsoft.json/index.json 79ms
info :   GET https://api.nuget.org/v3-flatcontainer/newtonsoft.json/12.0.1/newtonsoft.json.12.0.1.nupkg
info :   OK https://api.nuget.org/v3-flatcontainer/newtonsoft.json/12.0.1/newtonsoft.json.12.0.1.nupkg 232ms
log  : Installing Newtonsoft.Json 12.0.1.
info : Package 'Newtonsoft.Json' is compatible with all the specified frameworks in project 'C:\projects\ToDo\ToDo.csproj'.
info : PackageReference for package 'Newtonsoft.Json' version '12.0.1' added to file 'C:\projects\ToDo\ToDo.csproj'.
```

<span data-ttu-id="e655a-112">この *ToDo.csproj* ファイルには、参照されるパッケージの [`<PackageReference>`](/nuget/consume-packages/package-references-in-project-files) 要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e655a-112">The *ToDo.csproj* file now contains a [`<PackageReference>`](/nuget/consume-packages/package-references-in-project-files) element for the referenced package.</span></span>

```xml
<PackageReference Include="Newtonsoft.Json" Version="12.0.1" />
```

## <a name="arguments"></a><span data-ttu-id="e655a-113">引数</span><span class="sxs-lookup"><span data-stu-id="e655a-113">Arguments</span></span>

* **`PROJECT`**

  <span data-ttu-id="e655a-114">プロジェクト ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="e655a-114">Specifies the project file.</span></span> <span data-ttu-id="e655a-115">指定されていない場合、現在のディレクトリで検索されます。</span><span class="sxs-lookup"><span data-stu-id="e655a-115">If not specified, the command searches the current directory for one.</span></span>

* **`PACKAGE_NAME`**

  <span data-ttu-id="e655a-116">追加するパッケージ参照。</span><span class="sxs-lookup"><span data-stu-id="e655a-116">The package reference to add.</span></span>

## <a name="options"></a><span data-ttu-id="e655a-117">オプション</span><span class="sxs-lookup"><span data-stu-id="e655a-117">Options</span></span>

* **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="e655a-118">特定の[フレームワーク](../../standard/frameworks.md)を対象にしている場合にのみ、パッケージ参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="e655a-118">Adds a package reference only when targeting a specific [framework](../../standard/frameworks.md).</span></span>

* **`-h|--help`**

  <span data-ttu-id="e655a-119">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="e655a-119">Prints out a short help for the command.</span></span>

* **`--interactive`**

  <span data-ttu-id="e655a-120">コマンドを停止して、ユーザーの入力または操作を待機させることができます (たとえば、認証を完了する場合)。</span><span class="sxs-lookup"><span data-stu-id="e655a-120">Allows the command to stop and wait for user input or action (for example to complete authentication).</span></span> <span data-ttu-id="e655a-121">.NET Core 2.1 SDK バージョン 2.1.400 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="e655a-121">Available since .NET Core 2.1 SDK, version 2.1.400 or later.</span></span>

* **`-n|--no-restore`**

  <span data-ttu-id="e655a-122">復元のプレビューと互換性チェックを実行せずにパッケージ参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="e655a-122">Adds a package reference without performing a restore preview and compatibility check.</span></span>

* **`--package-directory <PACKAGE_DIRECTORY>`**

  <span data-ttu-id="e655a-123">指定したディレクトリにパッケージを復元します。</span><span class="sxs-lookup"><span data-stu-id="e655a-123">Restores the package to the specified directory.</span></span>

* **`-s|--source <SOURCE>`**

  <span data-ttu-id="e655a-124">復元操作の間に特定の NuGet パッケージのソースを使います。</span><span class="sxs-lookup"><span data-stu-id="e655a-124">Uses a specific NuGet package source during the restore operation.</span></span>

* **`-v|--version <VERSION>`**

  <span data-ttu-id="e655a-125">パッケージのバージョン。</span><span class="sxs-lookup"><span data-stu-id="e655a-125">Version of the package.</span></span>

## <a name="examples"></a><span data-ttu-id="e655a-126">使用例</span><span class="sxs-lookup"><span data-stu-id="e655a-126">Examples</span></span>

* <span data-ttu-id="e655a-127">`Newtonsoft.Json` NuGet パッケージをプロジェクトに追加する:</span><span class="sxs-lookup"><span data-stu-id="e655a-127">Add `Newtonsoft.Json` NuGet package to a project:</span></span>

  ```console
  dotnet add package Newtonsoft.Json
  ```

* <span data-ttu-id="e655a-128">特定バージョンのパッケージをプロジェクトに追加する:</span><span class="sxs-lookup"><span data-stu-id="e655a-128">Add a specific version of a package to a project:</span></span>

  ```console
  dotnet add ToDo.csproj package Microsoft.Azure.DocumentDB.Core -v 1.0.0
  ```

* <span data-ttu-id="e655a-129">特定の NuGet ソースを使用してパッケージを追加する:</span><span class="sxs-lookup"><span data-stu-id="e655a-129">Add a package using a specific NuGet source:</span></span>

  ```console
  dotnet add package Microsoft.AspNetCore.StaticFiles -s https://dotnet.myget.org/F/dotnet-core/api/v3/index.json
  ```