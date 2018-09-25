---
title: '方法: 自動バインディング リダイレクトを有効/無効にする'
ms.date: 09/12/2018
helpviewer_keywords:
- side-by-side execution, assembly binding redirection
- assemblies [.NET Framework], binding redirection
ms.assetid: 5fca42f3-bdce-4b81-a704-61e42c89d3ba
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 9b9c9cbdb89ccf67942dcccee37ea410c6fa39a5
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47079544"
---
# <a name="how-to-enable-and-disable-automatic-binding-redirection"></a><span data-ttu-id="20104-102">方法: 自動バインディング リダイレクトを有効/無効にする</span><span class="sxs-lookup"><span data-stu-id="20104-102">How to: Enable and Disable Automatic Binding Redirection</span></span>

<span data-ttu-id="20104-103">Visual studio を対象とするアプリをコンパイルするときに、[!INCLUDE[net_v451](../../../includes/net-v451-md.md)]以降のバージョンでバインド リダイレクトが自動的にアセンブリの統一をオーバーライドするアプリの構成ファイルに追加するとします。</span><span class="sxs-lookup"><span data-stu-id="20104-103">When you compile apps in Visual Studio that target the [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] and later versions, binding redirects may be automatically added to the app configuration file to override assembly unification.</span></span> <span data-ttu-id="20104-104">アプリの構成ファイルで手動でバインド リダイレクトを指定している場合でも、アプリまたはそのコンポーネントが同じアセンブリの複数バージョンを参照している場合、バインド リダイレクトが追加されます。</span><span class="sxs-lookup"><span data-stu-id="20104-104">Binding redirects are added if your app or its components reference more than one version of the same assembly, even if you manually specify binding redirects in the configuration file for your app.</span></span> <span data-ttu-id="20104-105">自動バインド リダイレクトの機能に影響を与えます従来のデスクトップ アプリと web アプリを対象とする、[!INCLUDE[net_v451](../../../includes/net-v451-md.md)]以降のバージョンの動作は、web アプリに少しずつ異なります。</span><span class="sxs-lookup"><span data-stu-id="20104-105">The automatic binding redirection feature affects traditional desktop apps and web apps that target the [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] or a later version, although the behavior is slightly different for a web app.</span></span> <span data-ttu-id="20104-106">以前のバージョンの .NET Framework を対象とする既存のアプリがある場合は、自動バインド リダイレクトを有効にできます。また、手動で作成したバインド リダイレクトを保持する場合は、この機能を無効にできます。</span><span class="sxs-lookup"><span data-stu-id="20104-106">You can enable automatic binding redirection if you have existing apps that target previous versions of the .NET Framework, or you can disable this feature if you want to keep manually authored binding redirects.</span></span>

## <a name="disable-automatic-binding-redirects-in-desktop-apps"></a><span data-ttu-id="20104-107">デスクトップ アプリで自動バインド リダイレクトを無効にします。</span><span class="sxs-lookup"><span data-stu-id="20104-107">Disable automatic binding redirects in desktop apps</span></span>

<span data-ttu-id="20104-108">自動バインド リダイレクトは、[!INCLUDE[net_v451](../../../includes/net-v451-md.md)] 以上のバージョンを対象とする従来のデスクトップ アプリで、既定で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="20104-108">Automatic binding redirects are enabled by default for traditional desktop apps that target the [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] and later versions.</span></span> <span data-ttu-id="20104-109">バインド リダイレクトは、アプリケーションがコンパイルされ、発生する可能性のあるアセンブリの統一をオーバーライドするときに、出力構成ファイル (app.config) に追加されます。</span><span class="sxs-lookup"><span data-stu-id="20104-109">The binding redirects are added to the output configuration (app.config) file when the app is compiled and overrides the assembly unification that might otherwise take place.</span></span> <span data-ttu-id="20104-110">ソース app.config ファイルは変更されません。</span><span class="sxs-lookup"><span data-stu-id="20104-110">The source app.config file is not modified.</span></span> <span data-ttu-id="20104-111">アプリのプロジェクト ファイルを変更して、この機能を無効にできます。</span><span class="sxs-lookup"><span data-stu-id="20104-111">You can disable this feature by modifying the project file for the app.</span></span>

1. <span data-ttu-id="20104-112">次のメソッドのいずれかを使用して編集するためのプロジェクト ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="20104-112">Open the project file for editing using one of the following methods:</span></span>

   - <span data-ttu-id="20104-113">Visual studio でプロジェクトを選択**ソリューション エクスプ ローラー**を選び、**ファイル エクスプ ローラーでフォルダーを開く**ショートカット メニューから。</span><span class="sxs-lookup"><span data-stu-id="20104-113">In Visual Studio, select the project in **Solution Explorer**, and then choose **Open Folder in File Explorer** from the shortcut menu.</span></span> <span data-ttu-id="20104-114">ファイル エクスプ ローラーでプロジェクト (.csproj または .vbproj) ファイルを検索し、メモ帳で開きます。</span><span class="sxs-lookup"><span data-stu-id="20104-114">In File Explorer, find the project (.csproj or .vbproj) file and open it in Notepad.</span></span>
   - <span data-ttu-id="20104-115">Visual Studio での**ソリューション エクスプ ローラー**でプロジェクトを右クリックし、選択**プロジェクトのアンロード**します。</span><span class="sxs-lookup"><span data-stu-id="20104-115">In Visual Studio, in **Solution Explorer**, right-click the project and choose **Unload Project**.</span></span> <span data-ttu-id="20104-116">ここでも、アンロードされたプロジェクトを右クリックして **編集 [projectname.csproj]** します。</span><span class="sxs-lookup"><span data-stu-id="20104-116">Right-click the unloaded project again, and then choose **Edit [projectname.csproj]**.</span></span>

2. <span data-ttu-id="20104-117">プロジェクト ファイルで、次のプロパティ エントリを検索します。</span><span class="sxs-lookup"><span data-stu-id="20104-117">In the project file, find the following property entry:</span></span>

   ```xml
   <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
   ```

3. <span data-ttu-id="20104-118">`true` を `false` に変更します。</span><span class="sxs-lookup"><span data-stu-id="20104-118">Change `true` to `false`:</span></span>

   ```xml
   <AutoGenerateBindingRedirects>false</AutoGenerateBindingRedirects>
   ```

## <a name="enable-automatic-binding-redirects-manually"></a><span data-ttu-id="20104-119">自動バインド リダイレクトを手動で有効にします。</span><span class="sxs-lookup"><span data-stu-id="20104-119">Enable automatic binding redirects manually</span></span>

<span data-ttu-id="20104-120">旧バージョンを対象を自動的に求められたら、リダイレクトを追加する場合や、.NET Framework の既存のアプリで自動バインド リダイレクトを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="20104-120">You can enable automatic binding redirects in existing apps that target older versions of the .NET Framework, or in cases where you're not automatically prompted to add a redirect.</span></span> <span data-ttu-id="20104-121">新しいバージョンの framework を対象としているリダイレクトの追加を自動的に求められません場合は、ビルド出力アセンブリを再マップすることを示す可能性がありますが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20104-121">If you're targeting a newer version of the framework but do not get automatically prompted to add a redirect, you'll likely get build output that suggests you remap assemblies.</span></span>

1. <span data-ttu-id="20104-122">次のメソッドのいずれかを使用して編集するためのプロジェクト ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="20104-122">Open the project file for editing using one of the following methods:</span></span>

   - <span data-ttu-id="20104-123">Visual studio でプロジェクトを選択**ソリューション エクスプ ローラー**を選び、**ファイル エクスプ ローラーでフォルダーを開く**ショートカット メニューから。</span><span class="sxs-lookup"><span data-stu-id="20104-123">In Visual Studio, select the project in **Solution Explorer**, and then choose **Open Folder in File Explorer** from the shortcut menu.</span></span> <span data-ttu-id="20104-124">ファイル エクスプ ローラーでプロジェクト (.csproj または .vbproj) ファイルを検索し、メモ帳で開きます。</span><span class="sxs-lookup"><span data-stu-id="20104-124">In File Explorer, find the project (.csproj or .vbproj) file and open it in Notepad.</span></span>
   - <span data-ttu-id="20104-125">Visual Studio での**ソリューション エクスプ ローラー**でプロジェクトを右クリックし、選択**プロジェクトのアンロード**します。</span><span class="sxs-lookup"><span data-stu-id="20104-125">In Visual Studio, in **Solution Explorer**, right-click the project and choose **Unload Project**.</span></span> <span data-ttu-id="20104-126">ここでも、アンロードされたプロジェクトを右クリックして **編集 [projectname.csproj]** します。</span><span class="sxs-lookup"><span data-stu-id="20104-126">Right-click the unloaded project again, and then choose **Edit [projectname.csproj]**.</span></span>

2. <span data-ttu-id="20104-127">最初の構成プロパティ グループに次の要素を追加 (で、 \<PropertyGroup > タグ)。</span><span class="sxs-lookup"><span data-stu-id="20104-127">Add the following element to the first configuration property group (under the \<PropertyGroup> tag):</span></span>

   ```xml
   <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
   ```

   <span data-ttu-id="20104-128">次の要素が挿入されたプロジェクト ファイルの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="20104-128">The following shows an example project file with the element inserted:</span></span>

   ```xml
   <?xml version="1.0" encoding="utf-8"?>
   <Project ToolsVersion="12.0" DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
     <Import Project="$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props" Condition="Exists('$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props')" />
       <PropertyGroup>
         <Configuration Condition=" '$(Configuration)' == ''     ">Debug</Configuration>
         <Platform Condition=" '$(Platform)' == '' ">AnyCPU</Platform>
         <ProjectGuid>{123334}</ProjectGuid>
         ...
         <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
       </PropertyGroup>
     ...
   </Project>
   ```

3. <span data-ttu-id="20104-129">アプリをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="20104-129">Compile your app.</span></span>

## <a name="enable-automatic-binding-redirects-in-web-apps"></a><span data-ttu-id="20104-130">Web apps での自動バインド リダイレクトを有効にします。</span><span class="sxs-lookup"><span data-stu-id="20104-130">Enable automatic binding redirects in web apps</span></span>

<span data-ttu-id="20104-131">自動バインド リダイレクトは、Web アプリでは異なる方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="20104-131">Automatic binding redirects are implemented differently for web apps.</span></span> <span data-ttu-id="20104-132">ソースの構成 (web.config) ファイルを Web アプリ用に変更する必要があるため、バインド リダイレクトは構成ファイルに自動的に追加されません。</span><span class="sxs-lookup"><span data-stu-id="20104-132">Because the source configuration (web.config) file must be modified for web apps, binding redirects are not automatically added to the configuration file.</span></span> <span data-ttu-id="20104-133">ただし、Visual Studio によってバインドの競合が通知されるため、バインド リダイレクトを追加して競合を解決できます。</span><span class="sxs-lookup"><span data-stu-id="20104-133">However, Visual Studio notifies you of binding conflicts, and you can add binding redirects to resolve the conflicts.</span></span> <span data-ttu-id="20104-134">常にバインド リダイレクトを追加する指示に従い、ため、web アプリに対してこの機能を明示的に無効にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="20104-134">Because you're always prompted to add binding redirects, you don't need to explicitly disable this feature for a web app.</span></span>

<span data-ttu-id="20104-135">Web.config ファイルにバインド リダイレクトを追加するには</span><span class="sxs-lookup"><span data-stu-id="20104-135">To add binding redirects to a web.config file:</span></span>

1. <span data-ttu-id="20104-136">Visual Studio で、アプリをコンパイルし、ビルドの警告を確認します。</span><span class="sxs-lookup"><span data-stu-id="20104-136">In Visual Studio, compile the app, and check for build warnings.</span></span>

   <span data-ttu-id="20104-137">![ビルドのアセンブリ参照の競合の警告](../../../docs/framework/configure-apps/media/clr-assemblyrefwarning.png "CLR_AssemblyRefWarning")</span><span class="sxs-lookup"><span data-stu-id="20104-137">![Build warning for assembly reference conflicts](../../../docs/framework/configure-apps/media/clr-assemblyrefwarning.png "CLR_AssemblyRefWarning")</span></span>

2. <span data-ttu-id="20104-138">アセンブリ バインドの競合がある場合、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="20104-138">If there are assembly binding conflicts, a warning appears.</span></span> <span data-ttu-id="20104-139">警告をダブルクリックするか、警告とキーを押して選択**Enter**します。</span><span class="sxs-lookup"><span data-stu-id="20104-139">Double-click the warning, or select the warning and press **Enter**.</span></span>

   <span data-ttu-id="20104-140">自動的にソース web.config ファイルに必要なバインド リダイレクトを追加できるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20104-140">A dialog box that enables you to automatically add the necessary binding redirects to the source web.config file appears.</span></span>

   <span data-ttu-id="20104-141">![バインド リダイレクトのアクセス許可ダイアログ](../../../docs/framework/configure-apps/media/clr-addbindingredirect.png "CLR_AddBindingRedirect")</span><span class="sxs-lookup"><span data-stu-id="20104-141">![Binding redirect permission dialog](../../../docs/framework/configure-apps/media/clr-addbindingredirect.png "CLR_AddBindingRedirect")</span></span>

## <a name="see-also"></a><span data-ttu-id="20104-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="20104-142">See also</span></span>

- [<span data-ttu-id="20104-143">\<bindingRedirect > 要素</span><span class="sxs-lookup"><span data-stu-id="20104-143">\<bindingRedirect> Element</span></span>](../../../docs/framework/configure-apps/file-schema/runtime/bindingredirect-element.md)
- [<span data-ttu-id="20104-144">アセンブリ バージョンのリダイレクト</span><span class="sxs-lookup"><span data-stu-id="20104-144">Redirecting Assembly Versions</span></span>](../../../docs/framework/configure-apps/redirect-assembly-versions.md)
