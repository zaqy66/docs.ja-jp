---
title: コマンド ライン ツールの F# の概要します。
description: 任意のオペレーティング システム (Windows、macOs または Linux) で .NET Core CLI を使用した F# で簡単なマルチ プロジェクト ソリューションを構築する方法について説明します。
ms.date: 03/26/2018
ms.openlocfilehash: 8a82970f33c8bbe1b8cdd8fb6499b59b16d3cbf3
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "45673910"
---
# <a name="get-started-with-f-with-the-net-core-cli"></a><span data-ttu-id="aa641-103">.NET Core CLI を使用した F# の概要します。</span><span class="sxs-lookup"><span data-stu-id="aa641-103">Get started with F# with the .NET Core CLI</span></span>

<span data-ttu-id="aa641-104">この記事では、どのできますを開始する F# .NET Core CLI を使用したオペレーティング システム (Windows、macOS、または Linux) でについて説明します。</span><span class="sxs-lookup"><span data-stu-id="aa641-104">This article covers how you can get started with F# on any operating system (Windows, macOS, or Linux) with the .NET Core CLI.</span></span> <span data-ttu-id="aa641-105">コンソール アプリケーションによって呼び出されるクラス ライブラリを使用したマルチ プロジェクト ソリューションを構築する経由になります。</span><span class="sxs-lookup"><span data-stu-id="aa641-105">It goes through building a multi-project solution with a class library that is called by a console application.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="aa641-106">必須コンポーネント</span><span class="sxs-lookup"><span data-stu-id="aa641-106">Prerequisites</span></span>

<span data-ttu-id="aa641-107">を開始するには、、の最新バージョンをインストールする必要があります[.NET Core SDK](https://www.microsoft.com/net/download/)します。</span><span class="sxs-lookup"><span data-stu-id="aa641-107">To begin, you must install the latest [.NET Core SDK](https://www.microsoft.com/net/download/).</span></span>

<span data-ttu-id="aa641-108">この記事では、方法を知っているコマンドラインを使用して、任意のテキスト エディターを前提としています。</span><span class="sxs-lookup"><span data-stu-id="aa641-108">This article assumes that you know how to use a command line and have a preferred text editor.</span></span> <span data-ttu-id="aa641-109">それを既に使用しない場合[Visual Studio Code](get-started-vscode.md) F# 用のテキスト エディターとして便利なオプションです。</span><span class="sxs-lookup"><span data-stu-id="aa641-109">If you don't already use it, [Visual Studio Code](get-started-vscode.md) is a great option as a text editor for F#.</span></span>

## <a name="build-a-simple-multi-project-solution"></a><span data-ttu-id="aa641-110">単純なマルチ プロジェクト ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="aa641-110">Build a simple multi-project solution</span></span>

<span data-ttu-id="aa641-111">コマンド プロンプト/ターミナルを開きを使用して、[新しい dotnet](../../core/tools/dotnet-new.md)という新しいソリューション ファイルを作成するコマンド`FSNetCore`:</span><span class="sxs-lookup"><span data-stu-id="aa641-111">Open a command prompt/terminal and use the [dotnet new](../../core/tools/dotnet-new.md) command to create new solution file called `FSNetCore`:</span></span>

```console
dotnet new sln -o FSNetCore
```

<span data-ttu-id="aa641-112">前のコマンドを実行した後は、次のディレクトリ構造が生成されます。</span><span class="sxs-lookup"><span data-stu-id="aa641-112">The following directory structure is produced after running the previous command:</span></span>

```console
FSNetCore
    ├── FSNetCore.sln
```

### <a name="write-a-class-library"></a><span data-ttu-id="aa641-113">クラス ライブラリを作成します。</span><span class="sxs-lookup"><span data-stu-id="aa641-113">Write a class library</span></span>

<span data-ttu-id="aa641-114">ディレクトリに移動*FSNetCore*します。</span><span class="sxs-lookup"><span data-stu-id="aa641-114">Change directories to *FSNetCore*.</span></span>

<span data-ttu-id="aa641-115">使用して、`dotnet new`コマンド、クラス ライブラリ プロジェクトを作成、 **src**ライブラリという名前のフォルダー。</span><span class="sxs-lookup"><span data-stu-id="aa641-115">Use the `dotnet new` command, create a class library project in the **src** folder named Library.</span></span>

```console
dotnet new classlib -lang F# -o src/Library
```

<span data-ttu-id="aa641-116">前のコマンドを実行した後は、次のディレクトリ構造が生成されます。</span><span class="sxs-lookup"><span data-stu-id="aa641-116">The following directory structure is produced after running the previous command:</span></span>

```console
└── FSNetCore
    ├── FSNetCore.sln
    └── src
        └── Library
            ├── Library.fs
            └── Library.fsproj
```

<span data-ttu-id="aa641-117">内容を置き換える`Library.fs`を次のコード。</span><span class="sxs-lookup"><span data-stu-id="aa641-117">Replace the contents of `Library.fs` with the following code:</span></span>

```fsharp
module Library

open Newtonsoft.Json

let getJsonNetJson value =
    sprintf "I used to be %s but now I'm %s thanks to JSON.NET!" value (JsonConvert.SerializeObject(value))
```

<span data-ttu-id="aa641-118">ライブラリ プロジェクトに Newtonsoft.Json NuGet パッケージを追加します。</span><span class="sxs-lookup"><span data-stu-id="aa641-118">Add the Newtonsoft.Json NuGet package to the Library project.</span></span>

```console
dotnet add src/Library/Library.fsproj package Newtonsoft.Json
```

<span data-ttu-id="aa641-119">追加、`Library`プロジェクトを`FSNetCore`ソリューションを使用して、 [dotnet sln 追加](../../core/tools/dotnet-sln.md)コマンド。</span><span class="sxs-lookup"><span data-stu-id="aa641-119">Add the `Library` project to the `FSNetCore` solution using the [dotnet sln add](../../core/tools/dotnet-sln.md) command:</span></span>

```console
dotnet sln add src/Library/Library.fsproj
```

<span data-ttu-id="aa641-120">実行`dotnet build`プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="aa641-120">Run `dotnet build` to build the project.</span></span> <span data-ttu-id="aa641-121">作成するときに、未解決の依存関係が復元されます。</span><span class="sxs-lookup"><span data-stu-id="aa641-121">Unresolved dependencies will be restored when building.</span></span>

### <a name="write-a-console-application-that-consumes-the-class-library"></a><span data-ttu-id="aa641-122">クラス ライブラリを使用するコンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="aa641-122">Write a console application that consumes the class library</span></span>

<span data-ttu-id="aa641-123">使用して、`dotnet new`コマンド、コンソール アプリケーションを作成、 **src**アプリという名前のフォルダー。</span><span class="sxs-lookup"><span data-stu-id="aa641-123">Use the `dotnet new` command, create a console application in the **src** folder named App.</span></span>

```console
dotnet new console -lang F# -o src/App
```

<span data-ttu-id="aa641-124">前のコマンドを実行した後は、次のディレクトリ構造が生成されます。</span><span class="sxs-lookup"><span data-stu-id="aa641-124">The following directory structure is produced after running the previous command:</span></span>

```console
└── FSNetCore
    ├── FSNetCore.sln
    └── src
        ├── App
        │   ├── App.fsproj
        │   ├── Program.fs
        └── Library
            ├── Library.fs
            └── Library.fsproj
```

<span data-ttu-id="aa641-125">内容を置き換える、`Program.fs`を次のコード ファイル。</span><span class="sxs-lookup"><span data-stu-id="aa641-125">Replace the contents of the `Program.fs` file with the following code:</span></span>

```fsharp
open System
open Library

[<EntryPoint>]
let main argv =
    printfn "Nice command-line arguments! Here's what JSON.NET has to say about them:"

    argv
    |> Array.map getJsonNetJson
    |> Array.iter (printfn "%s")

    0 // return an integer exit code
```

<span data-ttu-id="aa641-126">参照を追加、`Library`プロジェクトを使用して[dotnet 参照の追加](../../core/tools/dotnet-add-reference.md)します。</span><span class="sxs-lookup"><span data-stu-id="aa641-126">Add a reference to the `Library` project using [dotnet add reference](../../core/tools/dotnet-add-reference.md).</span></span>

```console
dotnet add src/App/App.fsproj reference src/Library/Library.fsproj
```

<span data-ttu-id="aa641-127">追加、`App`プロジェクトを`FSNetCore`ソリューションを使用して、`dotnet sln add`コマンド。</span><span class="sxs-lookup"><span data-stu-id="aa641-127">Add the `App` project to the `FSNetCore` solution using the `dotnet sln add` command:</span></span>

```console
dotnet sln add src/App/App.fsproj
```

<span data-ttu-id="aa641-128">NuGet の依存関係を復元`dotnet restore`([注を参照してください。](#dotnet-restore-note)) を実行し`dotnet build`プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="aa641-128">Restore the NuGet dependencies, `dotnet restore` ([see note](#dotnet-restore-note)) and run `dotnet build` to build the project.</span></span>

<span data-ttu-id="aa641-129">ディレクトリに、`src/App`コンソール プロジェクトとプロジェクトを渡すことを実行`Hello World`引数として。</span><span class="sxs-lookup"><span data-stu-id="aa641-129">Change directory to the `src/App` console project and run the project passing `Hello World` as arguments:</span></span>

```console
cd src/App
dotnet run Hello World
```

<span data-ttu-id="aa641-130">次の結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa641-130">You should see the following results:</span></span>

```console
Nice command-line arguments! Here's what JSON.NET has to say about them:

I used to be Hello but now I'm ""Hello"" thanks to JSON.NET!
I used to be World but now I'm ""World"" thanks to JSON.NET!
```

## <a name="next-steps"></a><span data-ttu-id="aa641-131">次の手順</span><span class="sxs-lookup"><span data-stu-id="aa641-131">Next steps</span></span>

<span data-ttu-id="aa641-132">次に、チェック アウト、 [F# のツアー](../tour.md)を F# のさまざまな機能の詳細を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa641-132">Next, check out the [Tour of F#](../tour.md) to learn more about different F# features.</span></span>
