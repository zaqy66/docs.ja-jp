---
title: dotnet clean コマンド
description: dotnet clean コマンドは現在のディレクトリを消去します。
ms.date: 12/04/2018
ms.openlocfilehash: a25b7930794795e3dff5051a8ca1dd1b9c261dfd
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169860"
---
# <a name="dotnet-clean"></a><span data-ttu-id="8cb92-103">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="8cb92-103">dotnet clean</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="8cb92-104">name</span><span class="sxs-lookup"><span data-stu-id="8cb92-104">Name</span></span>

<span data-ttu-id="8cb92-105">`dotnet clean` - プロジェクトの出力を消去します。</span><span class="sxs-lookup"><span data-stu-id="8cb92-105">`dotnet clean` - Cleans the output of a project.</span></span>

## <a name="synopsis"></a><span data-ttu-id="8cb92-106">構文</span><span class="sxs-lookup"><span data-stu-id="8cb92-106">Synopsis</span></span>

```
dotnet clean [<PROJECT>] [-c|--configuration] [-f|--framework] [-o|--output] [-r|--runtime] [-v|--verbosity]
dotnet clean [-h|--help]
```

## <a name="description"></a><span data-ttu-id="8cb92-107">説明</span><span class="sxs-lookup"><span data-stu-id="8cb92-107">Description</span></span>

<span data-ttu-id="8cb92-108">`dotnet clean` コマンドは、以前のビルドの出力を消去します。</span><span class="sxs-lookup"><span data-stu-id="8cb92-108">The `dotnet clean` command cleans the output of the previous build.</span></span> <span data-ttu-id="8cb92-109">[MSBuild ターゲット](/visualstudio/msbuild/msbuild-targets)として実装されます。そのため、コマンドの実行時にプロジェクトが評価されます。</span><span class="sxs-lookup"><span data-stu-id="8cb92-109">It's implemented as an [MSBuild target](/visualstudio/msbuild/msbuild-targets), so the project is evaluated when the command is run.</span></span> <span data-ttu-id="8cb92-110">ビルド中に作成された出力のみが消去されます。</span><span class="sxs-lookup"><span data-stu-id="8cb92-110">Only the outputs created during the build are cleaned.</span></span> <span data-ttu-id="8cb92-111">中間 (*obj*) と最終出力 (*bin*) フォルダーの両方が消去されます。</span><span class="sxs-lookup"><span data-stu-id="8cb92-111">Both intermediate (*obj*) and final output (*bin*) folders are cleaned.</span></span>

## <a name="arguments"></a><span data-ttu-id="8cb92-112">引数</span><span class="sxs-lookup"><span data-stu-id="8cb92-112">Arguments</span></span>

`PROJECT`

<span data-ttu-id="8cb92-113">消去する MSBuild プロジェクトです。</span><span class="sxs-lookup"><span data-stu-id="8cb92-113">The MSBuild project to clean.</span></span> <span data-ttu-id="8cb92-114">プロジェクト ファイルを指定しない場合、MSBuild は、現在の作業ディレクトリから *proj* で終わるファイル名拡張子を検索し、そのファイルを使います。</span><span class="sxs-lookup"><span data-stu-id="8cb92-114">If a project file is not specified, MSBuild searches the current working directory for a file that has a file extension that ends in *proj* and uses that file.</span></span>

## <a name="options"></a><span data-ttu-id="8cb92-115">オプション</span><span class="sxs-lookup"><span data-stu-id="8cb92-115">Options</span></span>

* **`-c|--configuration {Debug|Release}`**

  <span data-ttu-id="8cb92-116">ビルド構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="8cb92-116">Defines the build configuration.</span></span> <span data-ttu-id="8cb92-117">既定値は `Debug` です。</span><span class="sxs-lookup"><span data-stu-id="8cb92-117">The default value is `Debug`.</span></span> <span data-ttu-id="8cb92-118">このオプションは、ビルド時に指定した場合にのみ、消去時にも必要です。</span><span class="sxs-lookup"><span data-stu-id="8cb92-118">This option is only required when cleaning if you specified it during build time.</span></span>

* **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="8cb92-119">ビルド時に指定された[フレームワーク](../../standard/frameworks.md)です。</span><span class="sxs-lookup"><span data-stu-id="8cb92-119">The [framework](../../standard/frameworks.md) that was specified at build time.</span></span> <span data-ttu-id="8cb92-120">フレームワークは、[プロジェクト ファイル](csproj.md)で定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8cb92-120">The framework must be defined in the [project file](csproj.md).</span></span> <span data-ttu-id="8cb92-121">ビルド時にフレームワークを指定した場合は、消去時にフレームワークを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8cb92-121">If you specified the framework at build time, you must specify the framework when cleaning.</span></span>

* **`-h|--help`**

  <span data-ttu-id="8cb92-122">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="8cb92-122">Prints out a short help for the command.</span></span>

* **`-o|--output <OUTPUT_DIRECTORY>`**

  <span data-ttu-id="8cb92-123">ビルド出力が配置されたディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="8cb92-123">Directory in which the build outputs are placed.</span></span> <span data-ttu-id="8cb92-124">プロジェクトのビルド時にフレームワークを指定した場合、出力ディレクトリ スイッチと共に `-f|--framework <FRAMEWORK>` スイッチを指定します。</span><span class="sxs-lookup"><span data-stu-id="8cb92-124">Specify the `-f|--framework <FRAMEWORK>` switch with the output directory switch if you specified the framework when the project was built.</span></span>

* **`-r|--runtime <RUNTIME_IDENTIFIER>`**

  <span data-ttu-id="8cb92-125">指定したランタイムの出力フォルダーをクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="8cb92-125">Cleans the output folder of the specified runtime.</span></span> <span data-ttu-id="8cb92-126">これは、[自己完結型の展開](../deploying/index.md#self-contained-deployments-scd)が作成された場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8cb92-126">This is used when a [self-contained deployment](../deploying/index.md#self-contained-deployments-scd) was created.</span></span> <span data-ttu-id="8cb92-127">.NET Core 2.0 SDK 以降、使用できるオプションです。</span><span class="sxs-lookup"><span data-stu-id="8cb92-127">Option available since .NET Core 2.0 SDK.</span></span>

* **`-v|--verbosity <LEVEL>`**

  <span data-ttu-id="8cb92-128">コマンドの詳細レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="8cb92-128">Sets the verbosity level of the command.</span></span> <span data-ttu-id="8cb92-129">指定できるレベルは、q[uiet]、m[inimal]、n[ormal]、d[etailed]、diag[nostic] です。</span><span class="sxs-lookup"><span data-stu-id="8cb92-129">Allowed levels are q[uiet], m[inimal], n[ormal], d[etailed], and diag[nostic].</span></span>

## <a name="examples"></a><span data-ttu-id="8cb92-130">使用例</span><span class="sxs-lookup"><span data-stu-id="8cb92-130">Examples</span></span>

* <span data-ttu-id="8cb92-131">プロジェクトの既定のビルドを消去します。</span><span class="sxs-lookup"><span data-stu-id="8cb92-131">Clean a default build of the project:</span></span>

  ```console
  dotnet clean
  ```

* <span data-ttu-id="8cb92-132">リリース構成を使用してビルドされたプロジェクトを消去します。</span><span class="sxs-lookup"><span data-stu-id="8cb92-132">Clean a project built using the Release configuration:</span></span>

  ```console
  dotnet clean --configuration Release
  ```