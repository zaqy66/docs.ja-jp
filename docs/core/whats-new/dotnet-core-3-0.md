---
title: .NET Core 3.0 の新機能
description: .NET Core 3.0 の新機能について説明します。
dev_langs:
- csharp
- vb
author: thraka
ms.author: adegeo
ms.date: 12/04/2018
ms.openlocfilehash: 3ca833031eb8bb0f43a334f833f2e0075842d57d
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53156670"
---
# <a name="whats-new-in-net-core-30-preview-1"></a><span data-ttu-id="97645-103">.NET Core 3.0 (Preview 1) の新機能</span><span class="sxs-lookup"><span data-stu-id="97645-103">What's new in .NET Core 3.0 (Preview 1)</span></span>

<span data-ttu-id="97645-104">この記事では、.NET Core 3.0 (Preview 1) の新機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="97645-104">This article describes what is new in .NET Core 3.0 (preview 1).</span></span> <span data-ttu-id="97645-105">最も大きな強化点の 1 つは、Windows デスクトップ アプリケーションのサポートです (Windows のみ)。</span><span class="sxs-lookup"><span data-stu-id="97645-105">One of the biggest enhancements is support for Windows desktop applications (Windows only).</span></span> <span data-ttu-id="97645-106">Windows デスクトップという .NET Core 3.0 コンポーネントを利用して、Windows フォーム Windows Presentation Foundation (WPF) アプリケーションを移植することができます。</span><span class="sxs-lookup"><span data-stu-id="97645-106">By utilizing a .NET Core 3.0 component called Windows Desktop, you can port your Windows Forms Windows Presentation Foundation (WPF) applications.</span></span> <span data-ttu-id="97645-107">誤解のないように言うと、Windows Desktop コンポーネントは Windows でのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="97645-107">To be clear, the Windows Desktop component is only supported on Windows.</span></span> <span data-ttu-id="97645-108">詳細については、以下の「[Windows デスクトップ](#windows-desktop)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="97645-108">For more information, see the section [Windows desktop](#windows-desktop) below.</span></span>

<span data-ttu-id="97645-109">.NET Core 3.0 では C# 8.0 のサポートが追加されています。</span><span class="sxs-lookup"><span data-stu-id="97645-109">.NET Core 3.0 adds support for C# 8.0.</span></span>

<span data-ttu-id="97645-110">[.NET Core 3 Preview 1 を今すぐダウンロード](https://aka.ms/netcore3download)して Windows、Mac、Linux 上で使い始めましょう。</span><span class="sxs-lookup"><span data-stu-id="97645-110">[Download and get started with .NET Core 3 Preview 1](https://aka.ms/netcore3download) right now on Windows, Mac and Linux.</span></span> <span data-ttu-id="97645-111">リリースの詳細については、[.NET Core 3 Preview 1 のリリース ノート](https://aka.ms/netcore3releasenotes)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="97645-111">You can see complete details of the release in the [.NET Core 3 Preview 1 release notes](https://aka.ms/netcore3releasenotes).</span></span>

<span data-ttu-id="97645-112">詳細については、[.NET Core 3.0 Preview 1 のお知らせ](https://blogs.msdn.microsoft.com/dotnet/2018/12/04/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="97645-112">For more information, see the [.NET Core 3.0 Preview 1 announcement](https://blogs.msdn.microsoft.com/dotnet/2018/12/04/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/).</span></span>

## <a name="net-standard-21"></a><span data-ttu-id="97645-113">.NET Standard 2.1</span><span class="sxs-lookup"><span data-stu-id="97645-113">.NET Standard 2.1</span></span>

<span data-ttu-id="97645-114">.NET core 3.0 では .NET Standard 2.1 も実装されます。</span><span class="sxs-lookup"><span data-stu-id="97645-114">.NET Core 3.0 implements .NET Standard 2.1.</span></span>

## <a name="default-executables"></a><span data-ttu-id="97645-115">既定の実行可能ファイル</span><span class="sxs-lookup"><span data-stu-id="97645-115">Default executables</span></span>

<span data-ttu-id="97645-116">.NET Core の既定で実行可能ファイルがビルドされるようになります。</span><span class="sxs-lookup"><span data-stu-id="97645-116">.NET Core will now build executables by default.</span></span> <span data-ttu-id="97645-117">これは、グローバルにインストールされているバージョンの .NET Core を使用するアプリケーションの新機能です。</span><span class="sxs-lookup"><span data-stu-id="97645-117">This is new for applications that use a globally installed version of .NET Core.</span></span> <span data-ttu-id="97645-118">これまでは、[自己完結型の展開](../deploying/index.md#self-contained-deployments-scd)のみが実行可能ファイルを持っていました。</span><span class="sxs-lookup"><span data-stu-id="97645-118">Until now, only [self-contained deployments](../deploying/index.md#self-contained-deployments-scd) had executables.</span></span>

<span data-ttu-id="97645-119">`dotnet build` または `dotnet publish` の実行中に、使用している SDK の環境およびプラットフォームと一致する実行可能ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="97645-119">During `dotnet build` or `dotnet publish`, an executable is created provided that matches the environment and platform of the SDK you are using.</span></span> <span data-ttu-id="97645-120">これらの実行可能ファイルでは、次のような他のネイティブ実行可能ファイルと同じことを期待できます。</span><span class="sxs-lookup"><span data-stu-id="97645-120">You can expect the same things with these executables as you would other native executables, such as:</span></span>

* <span data-ttu-id="97645-121">実行可能ファイルはダブルクリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="97645-121">You can double-click on the executable.</span></span>
* <span data-ttu-id="97645-122">Windows では `myapp.exe`、Linux と macOS では`./myapp` など、コマンド プロンプトからアプリケーションを直接起動できます。</span><span class="sxs-lookup"><span data-stu-id="97645-122">You can launch the application from a command prompt directly, such as `myapp.exe` on Windows, and `./myapp` on Linux and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="97645-123">他のランタイム環境では、`dotnet publish -r` または `dotnet build -r` 引数を使用して特定のランタイムを指定することはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="97645-123">Specifying a specific runtime with `dotnet publish -r` or `dotnet build -r` arguments for other runtime environments isn't supported.</span></span>

## <a name="build-copies-dependencies"></a><span data-ttu-id="97645-124">ビルドによる依存関係のコピー</span><span class="sxs-lookup"><span data-stu-id="97645-124">Build copies dependencies</span></span>

<span data-ttu-id="97645-125">`dotnet build` で、アプリケーションの NuGet 依存関係が NuGet キャッシュからビルド出力フォルダーにコピーされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="97645-125">`dotnet build` now copies NuGet dependencies for your application from the NuGet cache to the build output folder.</span></span> <span data-ttu-id="97645-126">以前は、依存関係のコピーは `dotnet publish` の一部としてのみ行われていました。</span><span class="sxs-lookup"><span data-stu-id="97645-126">Previously, dependencies were only copied as part of `dotnet publish`.</span></span> 

<span data-ttu-id="97645-127">リンクや razor ページの発行など、まだ発行が必要な操作がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="97645-127">There are some operations, like linking and razor page publishing that will still require publishing.</span></span>


## <a name="local-dotnet-tools"></a><span data-ttu-id="97645-128">ローカルの dotnet ツール</span><span class="sxs-lookup"><span data-stu-id="97645-128">Local dotnet tools</span></span>

<span data-ttu-id="97645-129">.NET Core 2.1 はグローバル ツールをサポートしていましたが、.NET Core 3.0 にはローカル ツールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="97645-129">While .NET Core 2.1 supported global tools, .NET Core 3.0 now has local tools.</span></span> <span data-ttu-id="97645-130">ローカル ツールはグローバル ツールに似ていますが、ディスク上の特定の場所に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="97645-130">Local tools are similar to global tools but are associated with a particular location on disk.</span></span> <span data-ttu-id="97645-131">これで、プロジェクト単位およびリポジトリ単位のツールが可能になります。</span><span class="sxs-lookup"><span data-stu-id="97645-131">This enables per-project and per-repository tooling.</span></span> <span data-ttu-id="97645-132">ローカルにインストールされたツールはいずれも、グローバルでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="97645-132">Any tool installed locally isn't available globally.</span></span>

<span data-ttu-id="97645-133">ローカル ツールは、現在のディレクトリ内のマニフェスト ファイル名 `dotnet-tools.json` に依存しています。</span><span class="sxs-lookup"><span data-stu-id="97645-133">Local tools rely on a manifest file name `dotnet-tools.json` in your current directory.</span></span> <span data-ttu-id="97645-134">このマニフェスト ファイルでは、使用できるツールを定義します。</span><span class="sxs-lookup"><span data-stu-id="97645-134">This manifest file defines the tools to be available.</span></span> <span data-ttu-id="97645-135">リポジトリのルートにこのマニフェスト ファイルを作成することで、コードを複製したすべての人が、コードを正常に処理するために必要なツールを復元し、使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="97645-135">By creating this manifest file at the root of your repository, you ensure anyone cloning your code can restore and use the tools that are needed to successfully work with your code.</span></span>

<span data-ttu-id="97645-136">ローカル ツール マニフェスト ファイルを使用できる場合は、次のコマンドを使用して、自動的にこれらのツールをローカルにダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="97645-136">When the local tools manifest file is available, use the following command to automatically download and install those tools locally:</span></span>

```console
dotnet tool restore
```

<span data-ttu-id="97645-137">次のコマンドでローカル ツールを実行します。</span><span class="sxs-lookup"><span data-stu-id="97645-137">Run a local tool with the following command:</span></span>

```console
dotnet tool run <tool-command-name>
```

<span data-ttu-id="97645-138">ローカル ツールが呼び出されると、dotnet でそのディレクトリ構造内のマニフェストが検索されます。</span><span class="sxs-lookup"><span data-stu-id="97645-138">When a local tool is called, dotnet searches for a manifest up the directory structure.</span></span> <span data-ttu-id="97645-139">ツール マニフェスト ファイルが見つかると、要求されたツールが検索されます。</span><span class="sxs-lookup"><span data-stu-id="97645-139">When a tool manifest file is found, it is searched for the requested tool.</span></span> <span data-ttu-id="97645-140">ツールが見つかった場合は、NuGet グローバル パッケージの場所にあるツールを見つけるために必要な情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="97645-140">If the tool is found, it includes the information needed to find the tool in the NuGet global packages location.</span></span> 

<span data-ttu-id="97645-141">キャッシュではなくマニフェスト内にツールが見つかった場合、ユーザーはエラーを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="97645-141">If the tool is found in the manifest, but not the cache, the user receives an error.</span></span> <span data-ttu-id="97645-142">Preview 1 の後に、ユーザーが `dotnet tool restore` を実行することを要求するようにメッセージが改善される予定です。</span><span class="sxs-lookup"><span data-stu-id="97645-142">The message will be improved after Preview 1 to request the user run `dotnet tool restore`.</span></span>

<span data-ttu-id="97645-143">ディレクトリにローカル ツールを追加するには、まずツール マニフェスト ファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97645-143">To add local tools to a directory, you need to first create the tool manifest file.</span></span> <span data-ttu-id="97645-144">Preview 1 の後に、dotnet の新しいテンプレートなど、ツール マニフェスト ファイルを作成するためのメカニズムを提供する予定です。</span><span class="sxs-lookup"><span data-stu-id="97645-144">After Preview 1, we will offer a mechanism for creating tool manifest files, such as a dotnet new template.</span></span> <span data-ttu-id="97645-145">Preview 1 では、`dotnet-tools.json` という次の内容のファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97645-145">For Preview 1 you must create the file named `dotnet-tools.json` with the following contents:</span></span>

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {}
}
```

<span data-ttu-id="97645-146">マニフェストが作成されたら、次を使用してマニフェストにローカル ツールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="97645-146">Once the manifest is created, you can add local tools to it using:</span></span>

```console
dotnet tool install <toolPackageId>
```

<span data-ttu-id="97645-147">別のバージョンが指定されていない場合、このコマンドでツールの最新バージョンがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="97645-147">This command installs the latest version of the tool, unless another version is specified.</span></span>  <span data-ttu-id="97645-148">最新のバージョンが自動的に選択された場合でも、ツールのマニフェスト ファイルにツールのバージョンを書き込み、正しいバージョンのツールを復元または実行することができます。</span><span class="sxs-lookup"><span data-stu-id="97645-148">Even if the latest version was automatically chosen, the version of the tool is written into the tool manifest file to allow the correct version of the tool to be restored or run.</span></span>

<span data-ttu-id="97645-149">ツール マニフェスト ファイルは、手動で編集できるように設計されています。そのため、リポジトリを操作するために必要なバージョンを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="97645-149">The tool manifest file is designed to allow hand editing – which you might do to update the required version for working with the repository.</span></span>

<span data-ttu-id="97645-150">`dotnet-tools.json` ファイルの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="97645-150">Here is an example `dotnet-tools.json` file:</span></span>

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {
    "dotnetsay": {
      "version": "2.1.4",
      "commands": [
        "dotnetsay"
      ]
    },
    "t-rex": {
      "version": "1.0.103",
      "commands": [
        "t-rex"
      ]
    }
  }
}
```

<span data-ttu-id="97645-151">ツール マニフェスト ファイルからツールを削除するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="97645-151">To remove a tool from the tool manifest file, run the following command:</span></span>

```console
dotnet tool uninstall <toolPackageId>
```

<span data-ttu-id="97645-152">グローバル ツールとローカル ツールの両方で、ランタイムの互換バージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="97645-152">For both global and local tools, a compatible version of the runtime is required.</span></span> <span data-ttu-id="97645-153">現在 NuGet.org 上にある多くのツールは、.NET Core Runtime 2.1 をターゲットとしています。</span><span class="sxs-lookup"><span data-stu-id="97645-153">Many tools currently on NuGet.org target .NET Core Runtime 2.1.</span></span> <span data-ttu-id="97645-154">グローバルにまたはローカルにそれらをインストールするには、[NET Core 2.1 ランタイム](https://dotnet.microsoft.com/download/dotnet-core/2.1)をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="97645-154">To install those globally or locally, you would still need to install the [NET Core 2.1 Runtime](https://dotnet.microsoft.com/download/dotnet-core/2.1).</span></span>

<span data-ttu-id="97645-155">詳細については、[Local Tools Early Preview のドキュメント](https://github.com/dotnet/cli/issues/10288)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="97645-155">For more information, see [Local Tools Early Preview Documentation](https://github.com/dotnet/cli/issues/10288).</span></span>

## <a name="windows-desktop"></a><span data-ttu-id="97645-156">Windows デスクトップ</span><span class="sxs-lookup"><span data-stu-id="97645-156">Windows desktop</span></span>

<span data-ttu-id="97645-157">.NET Core 3.0 Preview 1 以降では、WPF および Windows フォームを使用して Windows デスクトップ アプリケーションを構築できます。</span><span class="sxs-lookup"><span data-stu-id="97645-157">Starting with .NET Core 3.0 Preview 1, you can build Windows desktop applications using WPF and Windows Forms.</span></span> <span data-ttu-id="97645-158">これらのフレームワークでは、Windows UI XAML ライブラリ (WinUI) の最新のコントロールと Fluent スタイルを [XAML Islands](/windows/uwp/xaml-platform/xaml-host-controls) 経由で使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="97645-158">These frameworks also support using modern controls and Fluent styling from the Windows UI XAML Library (WinUI) via [XAML islands](/windows/uwp/xaml-platform/xaml-host-controls).</span></span>

<span data-ttu-id="97645-159">Windows デスクトップ コンポーネントは、Windows .NET Core 3.0 SDK の一部です。</span><span class="sxs-lookup"><span data-stu-id="97645-159">The Windows Desktop component is part of the Windows .NET Core 3.0 SDK.</span></span>

<span data-ttu-id="97645-160">次の `dotnet` コマンドを使用して、新しい WPF または Windows フォーム アプリケーションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="97645-160">You can create a new WPF or Windows Forms app with the following `dotnet` commands:</span></span>

```console
dotnet new wpf
dotnet new winforms
```

<span data-ttu-id="97645-161">また、Visual Studio 2019 Preview 1 で .NET Core 3.0 WPF および Windows フォーム プロジェクトを開き、起動し、デバッグすることもできます。</span><span class="sxs-lookup"><span data-stu-id="97645-161">You can also open, launch, and debug .NET Core 3.0 WPF and Windows Forms projects in Visual Studio 2019 Preview 1.</span></span> <span data-ttu-id="97645-162">現在、Visual Studio 2017 15.9 でこれらのプロジェクトを開くことはできますが、サポートされているシナリオではありません (また、[プレビューを有効にする](https://blogs.msdn.microsoft.com/dotnet/2018/11/13/net-core-tooling-update-for-visual-studio-2017-version-15-9/)必要があります)。</span><span class="sxs-lookup"><span data-stu-id="97645-162">It's currently possible to open these projects in Visual Studio 2017 15.9, however, it isn't a supported scenario (and you need to [enable previews](https://blogs.msdn.microsoft.com/dotnet/2018/11/13/net-core-tooling-update-for-visual-studio-2017-version-15-9/)).</span></span>

<span data-ttu-id="97645-163">新しいプロジェクトは既存の .NET Core プロジェクトと同じですが、いくつかの追加もあります。</span><span class="sxs-lookup"><span data-stu-id="97645-163">The new projects are the same as existing .NET Core projects, with a couple additions.</span></span> <span data-ttu-id="97645-164">基本的な .NET Core コンソール プロジェクトと基本的な Windows フォームおよび WPF プロジェクトとの比較を次に示します。</span><span class="sxs-lookup"><span data-stu-id="97645-164">Here is the comparison of the basic .NET Core console project and a basic Windows Forms and WPF project.</span></span>

<span data-ttu-id="97645-165">.NET Core コンソール プロジェクトでは、`Microsoft.NET.Sdk` SDK が使用され、`netcoreapp3.0` ターゲット フレームワークを介して .NET Core 3.0 への依存関係が宣言されます。</span><span class="sxs-lookup"><span data-stu-id="97645-165">In a .NET Core console project, the project uses the `Microsoft.NET.Sdk` SDK and declares a dependency on .NET Core 3.0 via the `netcoreapp3.0` target framework.</span></span> <span data-ttu-id="97645-166">Windows デスクトップ アプリを作成するには、`Microsoft.NET.Sdk.WindowsDesktop` SDK を使用し、使用する UI フレームワークを選択します。</span><span class="sxs-lookup"><span data-stu-id="97645-166">To create a Windows Desktop app, use the `Microsoft.NET.Sdk.WindowsDesktop` SDK and choose which UI framework to use:</span></span>

```diff
-<Project Sdk="Microsoft.NET.Sdk">
+<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
+   <UseWPF>true</UseWPF>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="97645-167">WPF でなく Windows フォームを選択するには、`UseWPF` の代わりに `UseWindowsForms` を設定します。</span><span class="sxs-lookup"><span data-stu-id="97645-167">To choose Windows Forms over WPF, set `UseWindowsForms` instead of `UseWPF`:</span></span>

```diff
<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
-   <UseWPF>true</UseWPF>
+   <UseWindowsForms>true</UseWindowsForms>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="97645-168">Windows フォーム ダイアログが WPF コントロールをホストしている場合など、アプリが両方のフレームワークを使用する場合は、`UseWPF` および `UseWindowsForms` の両方を `true` に設定できます。</span><span class="sxs-lookup"><span data-stu-id="97645-168">Both `UseWPF` and `UseWindowsForms` can be set to `true` if the app uses both frameworks, for example when a Windows Forms dialog is hosting a WPF control.</span></span>

<span data-ttu-id="97645-169">[dotnet/winforms](https://github.com/dotnet/winforms/issues)、[dotnet/wpf](https://github.com/dotnet/wpf/issues)、[dotnet/core](https://github.com/dotnet/core/issues) リポジトリに関するフィードバックをお寄せください。</span><span class="sxs-lookup"><span data-stu-id="97645-169">Please share your feedback on the [dotnet/winforms](https://github.com/dotnet/winforms/issues),  [dotnet/wpf](https://github.com/dotnet/wpf/issues) and [dotnet/core](https://github.com/dotnet/core/issues) repos.</span></span>

## <a name="fast-built-in-json-support"></a><span data-ttu-id="97645-170">高速な組み込み JSON のサポート</span><span class="sxs-lookup"><span data-stu-id="97645-170">Fast built-in JSON support</span></span>

<span data-ttu-id="97645-171">`System.Text.Json.Utf8JsonReader` は、UTF-8 でエンコードされた JSON テキスト用の高パフォーマンス、低割り当て、転送のみのリーダーです。`ReadOnlySpan<byte>` から読み取られます。</span><span class="sxs-lookup"><span data-stu-id="97645-171">`System.Text.Json.Utf8JsonReader` is a high-performance, low allocation, forward-only reader for UTF-8 encoded JSON text, read from a `ReadOnlySpan<byte>`.</span></span> <span data-ttu-id="97645-172">`Utf8JsonReader` は基本的で低レベルの型であり、カスタム パーサーとデシリアライザーを構築するために利用できます。</span><span class="sxs-lookup"><span data-stu-id="97645-172">The `Utf8JsonReader` is a foundational, low-level type, that can be leveraged to build custom parsers and deserializers.</span></span> <span data-ttu-id="97645-173">新しい `Utf8JsonReader` を使用して JSON ペイロードを読み取る処理は、[Json.NET](https://www.newtonsoft.com/json) のリーダーを使用する場合より 2 倍高速です。</span><span class="sxs-lookup"><span data-stu-id="97645-173">Reading through a JSON payload using the new `Utf8JsonReader` is 2x faster than using the reader from [Json.NET](https://www.newtonsoft.com/json).</span></span> <span data-ttu-id="97645-174">JSON トークンを (UTF-16) 文字列として実現する必要が出てくるまでは割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="97645-174">It does not allocate until you need to actualize JSON tokens as (UTF-16) strings.</span></span>

<span data-ttu-id="97645-175">この新しい API には、次のコンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="97645-175">This new API will include the following components:</span></span>

* <span data-ttu-id="97645-176">Preview 1: JSON リーダー (シーケンシャル アクセス)</span><span class="sxs-lookup"><span data-stu-id="97645-176">In Preview 1: JSON reader (sequential access)</span></span>
* <span data-ttu-id="97645-177">次の予定: JSON ライター、DOM (ランダム アクセス)、poco シリアライザー、poco デシリアライザー</span><span class="sxs-lookup"><span data-stu-id="97645-177">Coming next: JSON writer, DOM (random access), poco serializer, poco deserializer</span></span>

<span data-ttu-id="97645-178">出発点として使用できる `Utf8JsonReader` の基本的なリーダー ループを次に示します。</span><span class="sxs-lookup"><span data-stu-id="97645-178">Here is the basic reader loop for the `Utf8JsonReader` that can be used as a starting point:</span></span>

```csharp
using System.Text.Json;

public static void Utf8JsonReaderLoop(ReadOnlySpan<byte> dataUtf8)
{
    var json = new Utf8JsonReader(dataUtf8, isFinalBlock: true, state: default);

    while (json.Read())
    {
        JsonTokenType tokenType = json.TokenType;
        ReadOnlySpan<byte> valueSpan = json.ValueSpan;
        switch (tokenType)
        {
            case JsonTokenType.StartObject:
            case JsonTokenType.EndObject:
                break;
            case JsonTokenType.StartArray:
            case JsonTokenType.EndArray:
                break;
            case JsonTokenType.PropertyName:
                break;
            case JsonTokenType.String:
                string valueString = json.GetStringValue();
                break;
            case JsonTokenType.Number:
                if (!json.TryGetInt32Value(out int valueInteger))
                {
                    throw new FormatException();
                }
                break;
            case JsonTokenType.True:
            case JsonTokenType.False:
                bool valueBool = json.GetBooleanValue();
                break;
            case JsonTokenType.Null:
                break;
            default:
                throw new ArgumentException();
        }
    }

    dataUtf8 = dataUtf8.Slice((int)json.BytesConsumed);
    JsonReaderState state = json.CurrentState;
}
```

<span data-ttu-id="97645-179">.NET エコシステムは、[Json.NET](https://www.newtonsoft.com/json) や他のよく使われている JSON ライブラリに依存しています。これは今後も推奨されます。</span><span class="sxs-lookup"><span data-stu-id="97645-179">The .NET ecosystem has relied on [Json.NET](https://www.newtonsoft.com/json) and other popular JSON libraries, which continue to be good choices.</span></span> <span data-ttu-id="97645-180">JSON.NET では .NET の文字列が基本のデータ型 (内部的には UTF-16) として使用されます。</span><span class="sxs-lookup"><span data-stu-id="97645-180">JSON.NET uses .NET strings as its base datatype, which are UTF-16 under the hood.</span></span> 

<span data-ttu-id="97645-181">.NET Core 2.1 および 3.0 では、`Span<T>` および UTF-8 文字列の使用に基づいて、必要なメモリがより少ない JSON API (`Utf8JsonReader` など) を記述することができる新しい API を追加しました。そのため、Kestrel、ASP.NET Core Web サーバーなどの高スループット アプリケーション開発のニーズに適しています。</span><span class="sxs-lookup"><span data-stu-id="97645-181">In .NET Core 2.1 and 3.0, we added new APIs that makes it possible to write JSON APIs (such as `Utf8JsonReader`) that require much less memory, based on using `Span<T>` and UTF-8 strings, and better serve the needs of high-throughput applications like Kestrel, ASP.NET Core web server.</span></span>

## <a name="ranges-and-indices"></a><span data-ttu-id="97645-182">範囲とインデックス</span><span class="sxs-lookup"><span data-stu-id="97645-182">Ranges and indices</span></span>

<span data-ttu-id="97645-183">新しい `Index` 型はインデックス作成に使用できます。</span><span class="sxs-lookup"><span data-stu-id="97645-183">The new `Index` type can be used for indexing.</span></span> <span data-ttu-id="97645-184">先頭からカウントする `int` か、末尾からカウントするプレフィックス `^` 演算子 (C#) を使用して作成することができます。</span><span class="sxs-lookup"><span data-stu-id="97645-184">You can create one from an `int` that counts from the beginning, or with a prefix `^` operator (C#) that counts from the end:</span></span>

```csharp
Index i1 = 3;  // number 3 from beginning
Index i2 = ^4; // number 4 from end
int[] a = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
Console.WriteLine($"{a[i1]}, {a[i2]}"); // "3, 6"
```

<span data-ttu-id="97645-185">また、`Range` 型もあります。これは開始値と終了値の 2 つの `Index` 値から構成され、`x..y` の範囲式 (C#) で記述できます。</span><span class="sxs-lookup"><span data-stu-id="97645-185">There is also a `Range` type, which consists of two `Index` values, one for the start and one for the end, and can be written with a `x..y` range expression (C#).</span></span> <span data-ttu-id="97645-186">これで、スライスを生成するために `Range` を使用してインデックスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="97645-186">You can then index with a `Range` in order to produce a slice:</span></span>

```csharp
var slice = a[i1..i2]; // { 3, 4, 5 }
```

> [!NOTE]
> <span data-ttu-id="97645-187">[C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) のみが `Range` および `Index` の構文をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="97645-187">Only [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) supports syntax for `Range` and `Index`.</span></span>

## <a name="async-streams"></a><span data-ttu-id="97645-188">非同期ストリーム</span><span class="sxs-lookup"><span data-stu-id="97645-188">Async streams</span></span>

<span data-ttu-id="97645-189">`IAsyncEnumerable<T>` 型は、`IEnumerable<T>` の新しい非同期バージョンです。</span><span class="sxs-lookup"><span data-stu-id="97645-189">The `IAsyncEnumerable<T>` type is a new asynchronous version of `IEnumerable<T>`.</span></span> <span data-ttu-id="97645-190">この言語では、その要素を使用するためにこれらよりも `await foreach` を行い、要素を生成するために `yield return` を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="97645-190">The language lets you `await foreach` over these to consume their elements, and `yield return` to them to produce elements.</span></span>

<span data-ttu-id="97645-191">非同期ストリームの生成の両方の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="97645-191">The following example demonstrates both production and consumption of async streams.</span></span> <span data-ttu-id="97645-192">`foreach` ステートメントは非同期であり、`yield return` を使用して呼び出し元の非同期ストリームを生成します。</span><span class="sxs-lookup"><span data-stu-id="97645-192">The `foreach` statement is async and itself uses `yield return` to produce an async stream for callers.</span></span> <span data-ttu-id="97645-193">(`yield return` を使用する) このパターンは、非同期ストリームを生成するモデルに推奨されます。</span><span class="sxs-lookup"><span data-stu-id="97645-193">This pattern (using `yield return`) is the recommended model for producing async streams.</span></span>

```csharp
async IAsyncEnumerable<int> GetBigResultsAsync()
{
    await foreach (var result in GetResultsAsync())
    {
        if (result > 20) yield return result; 
    }
}
```

> [!WARNING]
> <span data-ttu-id="97645-194">現在、.NET Core 3.0 Preview 1 の `await foreach` にはバグがあります。</span><span class="sxs-lookup"><span data-stu-id="97645-194">.NET Core 3.0 Preview 1 currently has a bug with `await foreach`.</span></span> <span data-ttu-id="97645-195">代わりに、`GetEnumerator` および `MoveNext` を使用して要素を処理してください。</span><span class="sxs-lookup"><span data-stu-id="97645-195">Instead, use `GetEnumerator` and `MoveNext` to process elements.</span></span> <span data-ttu-id="97645-196">詳細については、[roslyn/#31268](https://github.com/dotnet/roslyn/issues/31268) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="97645-196">For more information, see [roslyn/#31268](https://github.com/dotnet/roslyn/issues/31268).</span></span>

<span data-ttu-id="97645-197">`await foreach` を実行できるだけでなく、非同期反復子を作成することもできます。たとえば、`await` と`yield` の両方を行うことができる `IAsyncEnumerable/IAsyncEnumerator` を返す反復子です。</span><span class="sxs-lookup"><span data-stu-id="97645-197">In addition to being able to `await foreach`, you can also create async iterators, for example, an iterator that returns an `IAsyncEnumerable/IAsyncEnumerator` that you can both `await` and `yield` in.</span></span> <span data-ttu-id="97645-198">破棄する必要があるオブジェクトの場合は、`Stream` や `Timer` など、さまざまな BCL 型が実装する `IAsyncDisposable` を使用できます。</span><span class="sxs-lookup"><span data-stu-id="97645-198">For objects that need to be disposed, you can use `IAsyncDisposable`, which various BCL types implement, such as `Stream` and `Timer`.</span></span>

> [!NOTE]
> <span data-ttu-id="97645-199">[C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) のみが `await foreach` の構文をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="97645-199">Only [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) supports `await foreach` syntax.</span></span>

## <a name="type-sequencereader"></a><span data-ttu-id="97645-200">型: SequenceReader</span><span class="sxs-lookup"><span data-stu-id="97645-200">Type: SequenceReader</span></span>

<span data-ttu-id="97645-201">.NET Core 3.0 には、`ReadOnlySequence<T>` のリーダーとして使用できる `System.Buffers.SequenceReader` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="97645-201">In .NET Core 3.0, `System.Buffers.SequenceReader` has been added which can be used as a reader for `ReadOnlySequence<T>`.</span></span> <span data-ttu-id="97645-202">これにより、バッキング バッファーを複数回通過できる `System.IO.Pipelines` データの簡単、高パフォーマンスな、低割り当ての解析が可能になります。</span><span class="sxs-lookup"><span data-stu-id="97645-202">This allows easy, high performance, low allocation parsing of `System.IO.Pipelines` data that can cross multiple backing buffers.</span></span> 

<span data-ttu-id="97645-203">次の例では、入力 `Sequence` を有効な `CR/LF` 区切りの行に分割します。</span><span class="sxs-lookup"><span data-stu-id="97645-203">The following example breaks an input `Sequence` into valid `CR/LF` delimited lines:</span></span>

```csharp
private static ReadOnlySpan<byte> CRLF => new byte[] { (byte)'\r', (byte)'\n' };

public static void ReadLines(ReadOnlySequence<byte> sequence)
{
    SequenceReader<byte> reader = new SequenceReader<byte>(sequence);

    while (!reader.End)
    {
        if (!reader.TryReadToAny(out ReadOnlySpan<byte> line, CRLF, advancePastDelimiter:false))
        {
            // Couldn't find another delimiter
            // ...
        }

        if (!reader.IsNext(CRLF, advancePast: true))
        {
            // Not a good CR/LF pair
            // ...
        }

        // line is valid, process
        ProcessLine(line);
    }
}
```

## <a name="type-metadataloadcontext"></a><span data-ttu-id="97645-204">型: MetadataLoadContext</span><span class="sxs-lookup"><span data-stu-id="97645-204">Type: MetadataLoadContext</span></span>

<span data-ttu-id="97645-205">呼び出し元のアプリケーション ドメインに影響を与えることなく、アセンブリ メタデータを読み取ることができる `MetadataLoadContext` 型が追加されました。</span><span class="sxs-lookup"><span data-stu-id="97645-205">The `MetadataLoadContext` type has been added that enables reading assembly metadata without affecting the caller’s application domain.</span></span> <span data-ttu-id="97645-206">現在の運用環境とは異なるアーキテクチャおよびプラットフォーム向けに構築されたアセンブリなど、アセンブリはデータとして読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="97645-206">Assemblies are read as data, including assemblies built for different architectures and platforms than the current runtime environment.</span></span> <span data-ttu-id="97645-207">`MetadataLoadContext` は <xref:System.Reflection.Assembly.ReflectionOnlyLoad*> と重複しています。これは .NET Framework でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="97645-207">`MetadataLoadContext` overlaps with the <xref:System.Reflection.Assembly.ReflectionOnlyLoad*>, which is only available in the .NET Framework.</span></span>

<span data-ttu-id="97645-208">`MetdataLoadContext` は、[System.Reflection.MetadataLoadContext パッケージ](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext)で使用できます。</span><span class="sxs-lookup"><span data-stu-id="97645-208">`MetdataLoadContext` is available in the [System.Reflection.MetadataLoadContext package](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext).</span></span> <span data-ttu-id="97645-209">これは .NET Standard 2.0 パッケージです。</span><span class="sxs-lookup"><span data-stu-id="97645-209">It is a .NET Standard 2.0 package.</span></span>

<span data-ttu-id="97645-210">`MetadataLoadContext` は、<xref:System.Runtime.Loader.AssemblyLoadContext> 型に似ていますがその型に基づいていない API を公開しています。</span><span class="sxs-lookup"><span data-stu-id="97645-210">The `MetadataLoadContext` exposes APIs similar to the <xref:System.Runtime.Loader.AssemblyLoadContext> type, but is not based on that type.</span></span> <span data-ttu-id="97645-211"><xref:System.Runtime.Loader.AssemblyLoadContext> と同様に、`MetadataLoadContext` を使用すると、分離したアセンブリの読み込み中にアセンブリを読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="97645-211">Much like <xref:System.Runtime.Loader.AssemblyLoadContext>, the `MetadataLoadContext` enables loading assemblies within an isolated assembly loading universe.</span></span> <span data-ttu-id="97645-212">`MetdataLoadContext` API から <xref:System.Reflection.Assembly> オブジェクトが返され、使い慣れたリフレクション API を使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="97645-212">`MetdataLoadContext` APIs return <xref:System.Reflection.Assembly> objects, enabling the use of familiar reflection APIs.</span></span> <span data-ttu-id="97645-213">[MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127) などの実行指向の API は使用できず、InvalidOperationException がスローされます。</span><span class="sxs-lookup"><span data-stu-id="97645-213">Execution-oriented APIs, such as [MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127), are not allowed and will throw InvalidOperationException.</span></span>

<span data-ttu-id="97645-214">次のサンプルは、特定のインターフェイスを実装するアセンブリ内で具象型を検索する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="97645-214">The following sample demonstrates how to find concrete types in an assembly that implements a given interface:</span></span>

```csharp
var paths = new string[] {@"C:\myapp\mscorlib.dll", @"C:\myapp\myapp.dll"};
var resolver = new PathAssemblyResolver(paths);
using (var lc = new MetadataLoadContext(resolver))
{
    Assembly a = lc.LoadFromAssemblyName("myapp");
    Type myInterface = a.GetType("MyApp.IPluginInterface");
    foreach (Type t in a.GetTypes())
    {
        if (t.IsClass && myInterface.IsAssignableFrom(t))
            Console.WriteLine($"Class {t.FullName} implements IPluginInterface");
    }
}
```

<span data-ttu-id="97645-215">`MetadataLoadContext` のシナリオには、一連のアセンブリをデータとして検査し、検査の実行後にすべてのファイル ロックとメモリを解放する必要がある、設計時の機能、ビルド時のツール、およびランタイムのライトアップ機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="97645-215">Scenarios for `MetadataLoadContext` include design-time features, build-time tooling, and runtime light-up features that need to inspect a set of assemblies as data and have all file locks and memory freed after inspection is performed.</span></span>

<span data-ttu-id="97645-216">`MetadataLoadContext` には、コンストラクターに渡されるリゾルバー クラスがあります。</span><span class="sxs-lookup"><span data-stu-id="97645-216">The `MetadataLoadContext` has a resolver class passed to its constructor.</span></span> <span data-ttu-id="97645-217">リゾルバーのジョブは、`AssemblyName` が指定された `Assembly` の読み込みです。</span><span class="sxs-lookup"><span data-stu-id="97645-217">The resolver's job is to load an `Assembly` given its `AssemblyName`.</span></span> <span data-ttu-id="97645-218">リゾルバー クラスは、抽象 `MetadataAssemblyResolver` クラスから派生します。</span><span class="sxs-lookup"><span data-stu-id="97645-218">The resolver class derives from the abstract `MetadataAssemblyResolver` class.</span></span> <span data-ttu-id="97645-219">パスベースのシナリオの場合、リゾルバーの実装は `PathAssemblyResolver` で提供されています。</span><span class="sxs-lookup"><span data-stu-id="97645-219">An implementation of the resolver for path-based scenarios is provided with `PathAssemblyResolver`.</span></span>

<span data-ttu-id="97645-220">[MetadataLoadContext テスト](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests)は多数のユース ケースを示しています。</span><span class="sxs-lookup"><span data-stu-id="97645-220">The [MetadataLoadContext tests](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests) demonstrate many use cases.</span></span> <span data-ttu-id="97645-221">[アセンブリ テスト](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs)から始めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="97645-221">The [Assembly tests](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs) are a good place to start.</span></span>

## <a name="tls-13--openssl-111-on-linux"></a><span data-ttu-id="97645-222">Linux 上の TLS 1.3 と OpenSSL 1.1.1</span><span class="sxs-lookup"><span data-stu-id="97645-222">TLS 1.3 & OpenSSL 1.1.1 on Linux</span></span>

<span data-ttu-id="97645-223">現在、.NET Core では、特定の環境で使用できるようになったら、[OpenSSL 1.1.1 の TLS 1.3 のサポート](https://www.openssl.org/blog/blog/2018/09/11/release111/)を利用する予定です。</span><span class="sxs-lookup"><span data-stu-id="97645-223">.NET Core will now take advantage of [TLS 1.3 support in OpenSSL 1.1.1](https://www.openssl.org/blog/blog/2018/09/11/release111/), when it is available in a given environment.</span></span> <span data-ttu-id="97645-224">[OpenSSL チーム](https://www.openssl.org/blog/blog/2018/09/11/release111/)によると、TLS 1.3 には複数の利点があります。</span><span class="sxs-lookup"><span data-stu-id="97645-224">There are multiple benefits of TLS 1.3, per the [OpenSSL team](https://www.openssl.org/blog/blog/2018/09/11/release111/):</span></span>

* <span data-ttu-id="97645-225">クライアントとサーバー間に必要なラウンド トリップ回数の減少による接続時間の改善。</span><span class="sxs-lookup"><span data-stu-id="97645-225">Improved connection times due to a reduction in the number of round trips required between the client and server.</span></span>

* <span data-ttu-id="97645-226">さまざまな非推奨で安全ではない暗号化アルゴリズムの削除と、より多くの接続ハンドシェイクの暗号化によるセキュリティの向上。</span><span class="sxs-lookup"><span data-stu-id="97645-226">Improved security due to the removal of various obsolete and insecure cryptographic algorithms and encryption of more of the connection handshake.</span></span>

<span data-ttu-id="97645-227">.NET Core 3.0 Preview 1 では、**OpenSSL 1.1.1**、**OpenSSL 1.1.0**、または **OpenSSL 1.0.2** を利用することができます (Linux システム上で検出された任意の最適なバージョン)。</span><span class="sxs-lookup"><span data-stu-id="97645-227">.NET Core 3.0 Preview 1 is capable of utilizing **OpenSSL 1.1.1**, **OpenSSL 1.1.0**, or **OpenSSL 1.0.2** (whatever the best version found is, on a Linux system).</span></span>  <span data-ttu-id="97645-228">**OpenSSL 1.1.1** を使用可能で、クライアントとサーバーの両方が **TLS 1.3** をサポートしている場合、`SslProtocols.None` (システムの既定のプロトコル) を使用するときに、SslStream 型と HttpClient 型は **TLS 1.3** を使用します。</span><span class="sxs-lookup"><span data-stu-id="97645-228">When **OpenSSL 1.1.1** is available the SslStream and HttpClient types will use **TLS 1.3** when using `SslProtocols.None` (system default protocols), assuming both the client and server support **TLS 1.3**.</span></span>

<span data-ttu-id="97645-229">次のサンプルは、<https://www.cloudflare.com> に接続している Ubuntu 18.10 上の .NET Core 3.0 Preview 1 を示しています。</span><span class="sxs-lookup"><span data-stu-id="97645-229">The following sample demonstrates .NET Core 3.0 Preview 1 on Ubuntu 18.10 connecting to <https://www.cloudflare.com>:</span></span>

```csharp
using System;
using System.Net.Security;
using System.Net.Sockets;
using System.Threading.Tasks;

namespace tlstest
{
    class Program
    {
        static async Task Main()
        {
            using (TcpClient tcpClient = new TcpClient())
            {
                string targetHost = "www.cloudflare.com";

                await tcpClient.ConnectAsync(targetHost, 443);

                using (SslStream sslStream = new SslStream(tcpClient.GetStream()))
                {
                    await sslStream.AuthenticateAsClientAsync(targetHost);
                    await Console.Out.WriteLineAsync($"Connected to {targetHost} with {sslStream.SslProtocol}");
                }
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/tlstest$ dotnet run
Connected to www.cloudflare.com with Tls13
user@comp-ubuntu1810:~/tlstest$ openssl version
OpenSSL 1.1.1  11 Sep 2018
```

>[!IMPORTANT]
><span data-ttu-id="97645-230">Windows と macOS はまだ **TLS 1.3** をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="97645-230">Windows and macOS do not yet support **TLS 1.3**.</span></span> <span data-ttu-id="97645-231">サポートされるようになったら、.NET Core 3.0 はこれらのオペレーティング システムで **TLS 1.3** をサポートする予定です。</span><span class="sxs-lookup"><span data-stu-id="97645-231">.NET Core 3.0 will support **TLS 1.3** on these operating systems when support becomes available.</span></span>

## <a name="cryptography"></a><span data-ttu-id="97645-232">暗号</span><span class="sxs-lookup"><span data-stu-id="97645-232">Cryptography</span></span>

<span data-ttu-id="97645-233">`System.Security.Cryptography.AesGcm` および `System.Security.Cryptography.AesCcm` で実装された **AES-GCM** および **AES-CCM** 暗号のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="97645-233">Support has been added for **AES-GCM** and **AES-CCM** ciphers, implemented via `System.Security.Cryptography.AesGcm` and `System.Security.Cryptography.AesCcm`.</span></span> <span data-ttu-id="97645-234">これらのアルゴリズムは、[Authenticated Encryption with Association Data (AEAD) アルゴリズム](https://en.wikipedia.org/wiki/Authenticated_encryption) であり、.NET Core に追加された最初の Authenticated Encryption (AE) アルゴリズムでもあります。</span><span class="sxs-lookup"><span data-stu-id="97645-234">These algorithms are both [Authenticated Encryption with Association Data (AEAD) algorithms](https://en.wikipedia.org/wiki/Authenticated_encryption), and the first Authenticated Encryption (AE) algorithms added to .NET Core.</span></span>

<span data-ttu-id="97645-235">次のコードは、**AesGcm** 暗号を使用してランダム データの暗号化と復号化を行う例です。</span><span class="sxs-lookup"><span data-stu-id="97645-235">The following code demonstrates using **AesGcm** cipher to encrypt and decrypt random data.</span></span>

<span data-ttu-id="97645-236">**AesCcm** のコードは、ほぼ同じになります (クラスの変数名のみが異なります)。</span><span class="sxs-lookup"><span data-stu-id="97645-236">The code for **AesCcm** would look almost identical (only the class variable names would be different).</span></span>

```csharp
// key should be: pre-known, derived, or transported via another channel, such as RSA encryption
byte[] key = new byte[16];
RandomNumberGenerator.Fill(key);

byte[] nonce = new byte[12];
RandomNumberGenerator.Fill(nonce);

// normally this would be your data
byte[] dataToEncrypt = new byte[1234];
byte[] associatedData = new byte[333];
RandomNumberGenerator.Fill(dataToEncrypt);
RandomNumberGenerator.Fill(associatedData);

// these will be filled during the encryption
byte[] tag = new byte[16];
byte[] ciphertext = new byte[dataToEncrypt.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Encrypt(nonce, dataToEncrypt, ciphertext, tag, associatedData);
}

// tag, nonce, ciphertext, associatedData should be sent to the other part

byte[] decryptedData = new byte[ciphertext.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Decrypt(nonce, ciphertext, tag, decryptedData, associatedData);
}

// do something with the data
// this should always print that data is the same
Console.WriteLine($"AES-GCM: Decrypted data is{(dataToEncrypt.SequenceEqual(decryptedData) ? "the same as" : "different than")} original data.");
```

## <a name="cryptographic-key-importexport"></a><span data-ttu-id="97645-237">暗号化キーのインポート/エクスポート</span><span class="sxs-lookup"><span data-stu-id="97645-237">Cryptographic Key Import/Export</span></span>

<span data-ttu-id="97645-238">.NET Core 3.0 Preview 1 は、標準形式からの非対称の公開キーと秘密キーのインポートとエクスポートをサポートしています。X.509 証明書を使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="97645-238">.NET Core 3.0 Preview 1 supports the import and export of asymmetric public and private keys from standard formats, without needing to use an X.509 certificate.</span></span>

<span data-ttu-id="97645-239">すべてのキーの種類 (RSA、DSA、ECDsa、ECDiffieHellman) は、公開キー用の **X.509 SubjectPublicKeyInfo** 形式と、秘密キー用の **PKCS#8 PrivateKeyInfo** および **PKCS#8 EncryptedPrivateKeyInfo** 形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="97645-239">All key types (RSA, DSA, ECDsa, ECDiffieHellman) support the **X.509 SubjectPublicKeyInfo** format for public keys, and the **PKCS#8 PrivateKeyInfo** and **PKCS#8 EncryptedPrivateKeyInfo** formats for private keys.</span></span> <span data-ttu-id="97645-240">RSA は、さらに **PKCS#1 RSAPublicKey** および **PKCS#1 RSAPrivateKey** をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="97645-240">RSA additionally supports **PKCS#1 RSAPublicKey** and **PKCS#1 RSAPrivateKey**.</span></span> <span data-ttu-id="97645-241">いずれのエクスポートメソッドからも、DER でエンコードされたバイナリ データが生成され、インポート メソッドもそのようなデータを期待します。</span><span class="sxs-lookup"><span data-stu-id="97645-241">The export methods all produce DER-encoded binary data, and the import methods expect the same.</span></span> <span data-ttu-id="97645-242">キーがテキストに適した PEM 形式で格納されている場合、呼び出し元は import メソッドを呼び出す前にコンテンツを base64 でデコードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="97645-242">If a key is stored in the text-friendly PEM format, the caller will need to base64-decode the content before calling an import method.</span></span>

```csharp
using System;
using System.IO;
using System.Security.Cryptography;

namespace rsakeyprint
{
    class Program
    {
        static void Main(string[] args)
        {
            using (RSA rsa = RSA.Create())
            {
                byte[] keyBytes = File.ReadAllBytes(args[0]);
                rsa.ImportRSAPrivateKey(keyBytes, out int bytesRead);
 
                Console.WriteLine($"Read {bytesRead} bytes, {keyBytes.Length-bytesRead} extra byte(s) in file.");
                RSAParameters rsaParameters = rsa.ExportParameters(true);
                Console.WriteLine(BitConverter.ToString(rsaParameters.D));
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/rsakeyprint$ echo Making a small key to save on screen space.
Making a small key to save on screen space.
user@comp-ubuntu1810:~/rsakeyprint$ openssl genrsa 768 | openssl rsa -outform der -out rsa.key
Generating RSA private key, 768 bit long modulus (2 primes)
..+++++++
........+++++++
e is 65537 (0x010001)
writing RSA key
user@comp-ubuntu1810:~/rsakeyprint$ dotnet run rsa.key
Read 461 bytes, 0 extra byte(s) in file.
0F-D0-82-34-F8-13-38-4A-7F-C7-52-4A-F6-93-F8-FB-6D-98-7A-6A-04-3B-BC-35-8C-7D-AC-A5-A3-6E-AD-C1-66-30-81-2C-2A-DE-DA-60-03-6A-2C-D9-76-15-7F-61-97-57-
79-E1-6E-45-62-C3-83-04-97-CB-32-EF-C5-17-5F-99-60-92-AE-B6-34-6F-30-06-03-AC-BF-15-24-43-84-EB-83-60-EF-4D-3B-BD-D9-5D-56-26-F0-51-CE-F1
user@comp-ubuntu1810:~/rsakeyprint$ openssl rsa -in rsa.key -inform der -text -noout | grep -A7 private
privateExponent:
    0f:d0:82:34:f8:13:38:4a:7f:c7:52:4a:f6:93:f8:
    fb:6d:98:7a:6a:04:3b:bc:35:8c:7d:ac:a5:a3:6e:
    ad:c1:66:30:81:2c:2a:de:da:60:03:6a:2c:d9:76:
    15:7f:61:97:57:79:e1:6e:45:62:c3:83:04:97:cb:
    32:ef:c5:17:5f:99:60:92:ae:b6:34:6f:30:06:03:
    ac:bf:15:24:43:84:eb:83:60:ef:4d:3b:bd:d9:5d:
    56:26:f0:51:ce:f1
```

<span data-ttu-id="97645-243">PKCS#8 ファイルは `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo` クラスで検査できます。</span><span class="sxs-lookup"><span data-stu-id="97645-243">PKCS#8 files can be inspected with the `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo` class.</span></span>

<span data-ttu-id="97645-244">PFX/PKCS#12 ファイルは、それぞれ `System.Security.Cryptography.Pkcs.Pkcs12Info` および `System.Security.Cryptography.Pkcs.Pkcs12Builder` を使用して検査および操作できます。</span><span class="sxs-lookup"><span data-stu-id="97645-244">PFX/PKCS#12 files can be inspected and manipulated with `System.Security.Cryptography.Pkcs.Pkcs12Info` and `System.Security.Cryptography.Pkcs.Pkcs12Builder`, respectively.</span></span>

## <a name="serialport-for-linux"></a><span data-ttu-id="97645-245">Linux 用 SerialPort</span><span class="sxs-lookup"><span data-stu-id="97645-245">SerialPort for Linux</span></span>

<span data-ttu-id="97645-246">.NET Core 3.0 は Linux 上で <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType> をサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="97645-246">.NET Core 3.0 now supports <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType> on Linux.</span></span>

<span data-ttu-id="97645-247">以前の .NET Core では、Windows 上の `SerialPort` 型の使用のみをサポートしていました。</span><span class="sxs-lookup"><span data-stu-id="97645-247">Previously, .NET Core only supported using the `SerialPort` type on Windows.</span></span>

## <a name="more-bcl-improvements"></a><span data-ttu-id="97645-248">その他の BCL の機能強化</span><span class="sxs-lookup"><span data-stu-id="97645-248">More BCL Improvements</span></span>

<span data-ttu-id="97645-249">.NET Core 2.1 で導入された `Span<T>`、`Memory<T>`、および関連する型は、.NET Core 3.0 で最適化されました。</span><span class="sxs-lookup"><span data-stu-id="97645-249">The `Span<T>`, `Memory<T>`, and related types that were introduced in .NET Core 2.1, have been optimized in .NET Core 3.0.</span></span> <span data-ttu-id="97645-250">スパン構築、スライス、解析、書式設定などの一般的な操作がより効率的になりました。</span><span class="sxs-lookup"><span data-stu-id="97645-250">Common operations such as span construction, slicing, parsing, and formatting now perform better.</span></span> 

<span data-ttu-id="97645-251">さらに、`String` のような型が内部的に改善され、`Dictionary<TKey, TValue>` やその他のコレクションのキーとして使用した場合の効率が改善されました。</span><span class="sxs-lookup"><span data-stu-id="97645-251">Additionally, types like `String` have seen under-the-cover improvements to make them more efficient when used as keys with `Dictionary<TKey, TValue>` and other collections.</span></span> <span data-ttu-id="97645-252">これらの機能強化を利用するためにコードを変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="97645-252">No code changes are required to benefit from these improvements.</span></span>

<span data-ttu-id="97645-253">.NET Core 3 Preview 1 では、次の機能強化も追加されました。</span><span class="sxs-lookup"><span data-stu-id="97645-253">The following improvements are also new in .NET Core 3 Preview 1:</span></span>

* <span data-ttu-id="97645-254">HttpClient に組み込まれた Brotli のサポート</span><span class="sxs-lookup"><span data-stu-id="97645-254">Brotli support built in to HttpClient</span></span>
* <span data-ttu-id="97645-255">ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)</span><span class="sxs-lookup"><span data-stu-id="97645-255">ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)</span></span>
* <span data-ttu-id="97645-256">Unsafe.Unbox</span><span class="sxs-lookup"><span data-stu-id="97645-256">Unsafe.Unbox</span></span>
* <span data-ttu-id="97645-257">CancellationToken.Unregister</span><span class="sxs-lookup"><span data-stu-id="97645-257">CancellationToken.Unregister</span></span>
* <span data-ttu-id="97645-258">複合算術演算子</span><span class="sxs-lookup"><span data-stu-id="97645-258">Complex arithmetic operators</span></span>
* <span data-ttu-id="97645-259">TCP のキープ アライブのためのソケット API</span><span class="sxs-lookup"><span data-stu-id="97645-259">Socket APIs for TCP keep alive</span></span>
* <span data-ttu-id="97645-260">StringBuilder.GetChunks</span><span class="sxs-lookup"><span data-stu-id="97645-260">StringBuilder.GetChunks</span></span>
* <span data-ttu-id="97645-261">IPEndPoint の解析</span><span class="sxs-lookup"><span data-stu-id="97645-261">IPEndPoint parsing</span></span>
* <span data-ttu-id="97645-262">RandomNumberGenerator.GetInt32</span><span class="sxs-lookup"><span data-stu-id="97645-262">RandomNumberGenerator.GetInt32</span></span>

## <a name="tiered-compilation"></a><span data-ttu-id="97645-263">階層型コンパイル</span><span class="sxs-lookup"><span data-stu-id="97645-263">Tiered compilation</span></span>

<span data-ttu-id="97645-264">.NET Core 3.0 では、[階層型コンパイル](https://blogs.msdn.microsoft.com/dotnet/2018/08/02/tiered-compilation-preview-in-net-core-2-1/)が既定で有効になりました。</span><span class="sxs-lookup"><span data-stu-id="97645-264">[Tiered compilation](https://blogs.msdn.microsoft.com/dotnet/2018/08/02/tiered-compilation-preview-in-net-core-2-1/) is on by default with .NET Core 3.0.</span></span> <span data-ttu-id="97645-265">起動時とスループットの最大化の両方でパフォーマンスを向上するために、状況に応じてランタイムが Just-In-Time (JIT) コンパイラを使用できるようにする機能です。</span><span class="sxs-lookup"><span data-stu-id="97645-265">It is a feature that enables the runtime to more adaptively use the Just-In-Time (JIT) compiler to get better performance, both at startup and to maximize throughput.</span></span>

<span data-ttu-id="97645-266">この機能は、[.NET Core 2.1](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) のオプトイン機能として追加され、[.NET Core 2.2 Preview 2](https://blogs.msdn.microsoft.com/dotnet/2018/09/12/announcing-net-core-2-2-preview-2/) で既定で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="97645-266">This feature was added as an opt-in feature in [.NET Core 2.1](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) and then was enabled by default in [.NET Core 2.2 Preview 2](https://blogs.msdn.microsoft.com/dotnet/2018/09/12/announcing-net-core-2-2-preview-2/).</span></span> <span data-ttu-id="97645-267">その後、.NET Core 2.2 リリースではオプトイン機能に戻りました。</span><span class="sxs-lookup"><span data-stu-id="97645-267">Subsequently, it has been reverted back to opt in with the .NET Core 2.2 release.</span></span>

## <a name="arm64-linux-support"></a><span data-ttu-id="97645-268">ARM64 Linux のサポート</span><span class="sxs-lookup"><span data-stu-id="97645-268">ARM64 Linux support</span></span>

<span data-ttu-id="97645-269">今回のリリースでは、ARM64 for Linux のサポートが追加されています。</span><span class="sxs-lookup"><span data-stu-id="97645-269">We are adding support for ARM64 for Linux this release.</span></span> <span data-ttu-id="97645-270">コンテキストのために、.NET Core 2.1 では ARM32 for Linux のサポート、.NET Core 2.2 では Windows のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="97645-270">For context, we added support for ARM32 for Linux with .NET Core 2.1 and Windows with .NET Core 2.2.</span></span> <span data-ttu-id="97645-271">現在、ARM64 の主なユース ケースは、IoT シナリオを使用しています。</span><span class="sxs-lookup"><span data-stu-id="97645-271">The primary use case for ARM64 is currently with IoT scenarios.</span></span>

<span data-ttu-id="97645-272">Alpine、Debian、Ubuntu [Docker イメージは .NET Core for ARM64](https://hub.docker.com/r/microsoft/dotnet/) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="97645-272">Alpine, Debian and Ubuntu [Docker images are available for .NET Core for ARM64](https://hub.docker.com/r/microsoft/dotnet/).</span></span>

<span data-ttu-id="97645-273">詳細については、「[.NET Core ARM64 Status](https://github.com/dotnet/announcements/issues/82)」(.NET Core Runtime ARM64 の状態) を確認してください。</span><span class="sxs-lookup"><span data-stu-id="97645-273">Please check [.NET Core ARM64 Status](https://github.com/dotnet/announcements/issues/82) for more information.</span></span>

>[!NOTE]
> <span data-ttu-id="97645-274">**ARM64** Windows のサポートはまだ使用できません。</span><span class="sxs-lookup"><span data-stu-id="97645-274">**ARM64** Windows support isn't yet available.</span></span>
