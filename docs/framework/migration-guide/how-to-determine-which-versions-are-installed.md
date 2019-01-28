---
title: '方法: インストールされている .NET Framework バージョンを確認する'
ms.date: 04/10/2018
dev_langs:
- csharp
- vb
ms.custom: updateeachrelease
helpviewer_keywords:
- versions, determining for .NET Framework
- .NET Framework, determining version
ms.assetid: 40a67826-e4df-4f59-a651-d9eb0fdc755d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 31200b72cb551c91791e2e14332aacab8e7f0519
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672007"
---
# <a name="how-to-determine-which-net-framework-versions-are-installed"></a><span data-ttu-id="2f559-102">方法: インストールされている .NET Framework バージョンを確認する</span><span class="sxs-lookup"><span data-stu-id="2f559-102">How to: Determine which .NET Framework versions are installed</span></span>

<span data-ttu-id="2f559-103">ユーザーはコンピューターに複数のバージョンの .NET Framework をインストールして実行できます。</span><span class="sxs-lookup"><span data-stu-id="2f559-103">Users can install and run multiple versions of the .NET Framework on their computers.</span></span> <span data-ttu-id="2f559-104">アプリを開発または配置する場合、どのバージョンの .NET Framework がユーザーのコンピューターにインストールされているかを確認しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="2f559-104">When you develop or deploy your app, you might need to know which .NET Framework versions are installed on the user’s computer.</span></span> <span data-ttu-id="2f559-105">.NET Framework は、個別にバージョン管理される 2 つの主要コンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="2f559-105">Note that the .NET Framework consists of two main components, which are versioned separately:</span></span>  
  
-   <span data-ttu-id="2f559-106">アプリに機能を提供する型やリソースのコレクションである一連のアセンブリ。</span><span class="sxs-lookup"><span data-stu-id="2f559-106">A set of assemblies, which are collections of types and resources that provide the functionality for your apps.</span></span> <span data-ttu-id="2f559-107">.NET Framework とアセンブリは同じバージョン番号を共有します。</span><span class="sxs-lookup"><span data-stu-id="2f559-107">The .NET Framework and assemblies share the same version number.</span></span>  
  
-   <span data-ttu-id="2f559-108">アプリのコードを管理および実行する共通言語ランタイム (CLR)。</span><span class="sxs-lookup"><span data-stu-id="2f559-108">The common language runtime (CLR), which manages and executes your app's code.</span></span> <span data-ttu-id="2f559-109">CLR は独自のバージョン番号で識別されます (「[バージョンおよび依存関係](~/docs/framework/migration-guide/versions-and-dependencies.md)」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="2f559-109">The CLR is identified by its own version number (see [Versions and Dependencies](~/docs/framework/migration-guide/versions-and-dependencies.md)).</span></span>  
  
 <span data-ttu-id="2f559-110">コンピューターにインストールされている .NET Framework バージョンの正確な一覧を取得するには、レジストリを表示するか、コードでレジストリを照会することができます。</span><span class="sxs-lookup"><span data-stu-id="2f559-110">To get an accurate list of the .NET Framework versions installed on a computer, you can view the registry or query the registry in code:</span></span>  
  
 [<span data-ttu-id="2f559-111">レジストリの表示 (バージョン 1 ～ 4)</span><span class="sxs-lookup"><span data-stu-id="2f559-111">Viewing the registry (versions 1-4)</span></span>](#net_a)  
 [<span data-ttu-id="2f559-112">レジストリの表示 (バージョン 4.5 以降)</span><span class="sxs-lookup"><span data-stu-id="2f559-112">Viewing the registry (version 4.5 and later)</span></span>](#net_b)  
 [<span data-ttu-id="2f559-113">コードによるレジストリの照会 (バージョン 1 ～ 4)</span><span class="sxs-lookup"><span data-stu-id="2f559-113">Using code to query the registry (versions 1-4)</span></span>](#net_c)  
 [<span data-ttu-id="2f559-114">コードによるレジストリの照会 (バージョン 4.5 以降)</span><span class="sxs-lookup"><span data-stu-id="2f559-114">Using code to query the registry (version 4.5 and later)</span></span>](#net_d)  
 [<span data-ttu-id="2f559-115">PowerShell を使用したレジストリの照会 (バージョン 4.5 以降)</span><span class="sxs-lookup"><span data-stu-id="2f559-115">Using PowerShell to query the registry (version 4.5 and later)</span></span>](#ps_a)  
  
 <span data-ttu-id="2f559-116">CLR のバージョンを検索するには、ツールまたはコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f559-116">To find the CLR version, you can use a tool or code:</span></span>  
  
 [<span data-ttu-id="2f559-117">Clrver ツールの使用</span><span class="sxs-lookup"><span data-stu-id="2f559-117">Using the Clrver tool</span></span>](#clr_a)  
 [<span data-ttu-id="2f559-118">コードによる System.Environment クラスの照会</span><span class="sxs-lookup"><span data-stu-id="2f559-118">Using code to query the System.Environment class</span></span>](#clr_b)  
  
 <span data-ttu-id="2f559-119">.NET Framework の各バージョン用にインストールされている更新プログラムの検出については、「[方法:インストールされている .NET Framework の更新プログラムを確認する](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f559-119">For information about detecting the installed updates for each version of the .NET Framework, see [How to: Determine Which .NET Framework Updates Are Installed](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md).</span></span> <span data-ttu-id="2f559-120">.NET Framework のインストールの詳細については、「[開発者向けの .NET Framework のインストール](../../../docs/framework/install/guide-for-developers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f559-120">For information about installing the .NET Framework, see [Install the .NET Framework for developers](../../../docs/framework/install/guide-for-developers.md).</span></span>  
  
<a name="net_a"></a>   
## <a name="to-find-net-framework-versions-by-viewing-the-registry-net-framework-1-4"></a><span data-ttu-id="2f559-121">レジストリを表示して .NET Framework のバージョンを検索するには (.NET Framework 1 ～ 4)</span><span class="sxs-lookup"><span data-stu-id="2f559-121">To find .NET Framework versions by viewing the registry (.NET Framework 1-4)</span></span>  
  
1.  <span data-ttu-id="2f559-122">**[スタート]** ボタンをクリックし、**[ファイル名を指定して実行]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f559-122">On the **Start** menu, choose **Run**.</span></span>  
  
2.  <span data-ttu-id="2f559-123">**[開く]** ボックスに「**regedit.exe**」と入力します。</span><span class="sxs-lookup"><span data-stu-id="2f559-123">In the **Open** box, enter **regedit.exe**.</span></span>  
  
     <span data-ttu-id="2f559-124">regedit.exe を実行するには、管理特権が必要です。</span><span class="sxs-lookup"><span data-stu-id="2f559-124">You must have administrative credentials to run regedit.exe.</span></span>  
  
3.  <span data-ttu-id="2f559-125">レジストリ エディターで、次のサブキーを開きます。</span><span class="sxs-lookup"><span data-stu-id="2f559-125">In the Registry Editor, open the following subkey:</span></span>  
  
     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP`  
  
     <span data-ttu-id="2f559-126">インストールされているバージョンは NDP のサブキーの下に一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="2f559-126">The installed versions are listed under the NDP subkey.</span></span> <span data-ttu-id="2f559-127">バージョン番号は、**Version** エントリに格納されています。</span><span class="sxs-lookup"><span data-stu-id="2f559-127">The version number is stored in the **Version** entry.</span></span> <span data-ttu-id="2f559-128">[!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)] では、**Version** エントリは、Client サブキーまたは Full サブキー (NDP の下)、または両方のサブキーの下にあります。</span><span class="sxs-lookup"><span data-stu-id="2f559-128">For the [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)] the **Version** entry is under the Client or Full subkey (under NDP), or under both subkeys.</span></span>  
  

    > [!NOTE]
    > <span data-ttu-id="2f559-129">レジストリの ".NET Framework セットアップ" フォルダーの先頭はピリオドではありません。</span><span class="sxs-lookup"><span data-stu-id="2f559-129">The "NET Framework Setup" folder in the registry does not begin with a period.</span></span>

<a name="net_b"></a> 
## <a name="to-find-net-framework-versions-by-viewing-the-registry-net-framework-45-and-later"></a><span data-ttu-id="2f559-130">レジストリを表示して .NET Framework のバージョンを検索するには (.NET Framework 4.5 以降)</span><span class="sxs-lookup"><span data-stu-id="2f559-130">To find .NET Framework versions by viewing the registry (.NET Framework 4.5 and later)</span></span>

1. <span data-ttu-id="2f559-131">**[スタート]** ボタンをクリックし、**[ファイル名を指定して実行]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f559-131">On the **Start** menu, choose **Run**.</span></span>

2. <span data-ttu-id="2f559-132">**[開く]** ボックスに「**regedit.exe**」と入力します。</span><span class="sxs-lookup"><span data-stu-id="2f559-132">In the **Open** box, enter **regedit.exe**.</span></span>

     <span data-ttu-id="2f559-133">regedit.exe を実行するには、管理特権が必要です。</span><span class="sxs-lookup"><span data-stu-id="2f559-133">You must have administrative credentials to run regedit.exe.</span></span>

3. <span data-ttu-id="2f559-134">レジストリ エディターで、次のサブキーを開きます。</span><span class="sxs-lookup"><span data-stu-id="2f559-134">In the Registry Editor, open the following subkey:</span></span>

     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full`

     <span data-ttu-id="2f559-135">`Full` サブキーへのパスに `.NET Framework` ではなく `Net Framework` サブキーが含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2f559-135">Note that the path to the `Full` subkey includes the subkey `Net Framework` rather than `.NET Framework`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f559-136">`Full` サブキーが存在しない場合は、.NET Framework 4.5 以降がインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="2f559-136">If the `Full` subkey is not present, then you do not have the .NET Framework 4.5 or later installed.</span></span>

     <span data-ttu-id="2f559-137">`Release` という名前の DWORD 値を確認します。</span><span class="sxs-lookup"><span data-stu-id="2f559-137">Check for a DWORD value named `Release`.</span></span> <span data-ttu-id="2f559-138">`Release` DWORD がある場合は、[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 以降がコンピューターにインストールされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2f559-138">The existence of the `Release` DWORD indicates that the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or newer has been installed on that computer.</span></span>

     <span data-ttu-id="2f559-139">![.NET Framework 4.5 のレジストリ エントリ。](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")</span><span class="sxs-lookup"><span data-stu-id="2f559-139">![The registry entry for the .NET Framework 4.5.](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")</span></span>

     <span data-ttu-id="2f559-140">`Release` の値は、インストールされている .NET Framework のバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="2f559-140">The value of the `Release` DWORD indicates which version of the .NET Framework is installed.</span></span>

    [!INCLUDE[Release key values note](~/includes/version-keys-note.md)]

    |<span data-ttu-id="2f559-141">Release DWORD の値</span><span class="sxs-lookup"><span data-stu-id="2f559-141">Value of the Release DWORD</span></span>|<span data-ttu-id="2f559-142">Version</span><span class="sxs-lookup"><span data-stu-id="2f559-142">Version</span></span>|
    |--------------------------------|-------------|
    |<span data-ttu-id="2f559-143">378389</span><span class="sxs-lookup"><span data-stu-id="2f559-143">378389</span></span>|<span data-ttu-id="2f559-144">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="2f559-144">.NET Framework 4.5</span></span>|
    |<span data-ttu-id="2f559-145">378675</span><span class="sxs-lookup"><span data-stu-id="2f559-145">378675</span></span>|<span data-ttu-id="2f559-146">Windows 8.1 または Windows Server 2012 R2 でインストールされた .NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="2f559-146">.NET Framework 4.5.1 installed with Windows 8.1 or Windows Server 2012 R2</span></span>|
    |<span data-ttu-id="2f559-147">378758</span><span class="sxs-lookup"><span data-stu-id="2f559-147">378758</span></span>|<span data-ttu-id="2f559-148">Windows 8、Windows 7 SP1、または Windows Vista SP2 上でインストールされた .NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="2f559-148">.NET Framework 4.5.1 installed on Windows 8, Windows 7 SP1, or Windows Vista SP2</span></span>|
    |<span data-ttu-id="2f559-149">379893</span><span class="sxs-lookup"><span data-stu-id="2f559-149">379893</span></span>|<span data-ttu-id="2f559-150">.NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="2f559-150">.NET Framework 4.5.2</span></span>|
    |<span data-ttu-id="2f559-151">Windows 10 システムのみ:393295</span><span class="sxs-lookup"><span data-stu-id="2f559-151">On Windows 10 systems only: 393295</span></span><br /><br /> <span data-ttu-id="2f559-152">その他のすべての OS バージョン:393297</span><span class="sxs-lookup"><span data-stu-id="2f559-152">On all other OS versions: 393297</span></span>|[!INCLUDE[net_v46](../../../includes/net-v46-md.md)]|
    |<span data-ttu-id="2f559-153">Windows 10 の 11 月更新版のシステムのみ:394254</span><span class="sxs-lookup"><span data-stu-id="2f559-153">On Windows 10 November Update systems only: 394254</span></span><br /><br /> <span data-ttu-id="2f559-154">その他のすべての OS バージョン:394271</span><span class="sxs-lookup"><span data-stu-id="2f559-154">On all other OS versions: 394271</span></span>|[!INCLUDE[net_v461](../../../includes/net-v461-md.md)]|
    |<span data-ttu-id="2f559-155">Windows 10 Anniversary Update および Windows Server 2016 の場合:394802</span><span class="sxs-lookup"><span data-stu-id="2f559-155">On Windows 10 Anniversary Update and Windows Server 2016: 394802</span></span><br /><br /> <span data-ttu-id="2f559-156">その他のすべての OS バージョン:394806</span><span class="sxs-lookup"><span data-stu-id="2f559-156">On all other OS versions: 394806</span></span>|[!INCLUDE[net_v462](../../../includes/net-v462-md.md)]| 
    |<span data-ttu-id="2f559-157">Windows 10 Creators Update のみ:460798</span><span class="sxs-lookup"><span data-stu-id="2f559-157">On Windows 10 Creators Update only: 460798</span></span><br/><br/> <span data-ttu-id="2f559-158">その他のすべての OS バージョン:460805</span><span class="sxs-lookup"><span data-stu-id="2f559-158">On all other OS versions: 460805</span></span> | <span data-ttu-id="2f559-159">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="2f559-159">.NET Framework 4.7</span></span> |
    |<span data-ttu-id="2f559-160">Windows 10 Fall Creators Update のみ:461308</span><span class="sxs-lookup"><span data-stu-id="2f559-160">On Windows 10 Fall Creators Update only: 461308</span></span><br/><br/> <span data-ttu-id="2f559-161">その他のすべての OS バージョン:461310</span><span class="sxs-lookup"><span data-stu-id="2f559-161">On all other OS versions: 461310</span></span> | <span data-ttu-id="2f559-162">.NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="2f559-162">.NET Framework 4.7.1</span></span> |
    |<span data-ttu-id="2f559-163">Windows 10 April 2018 Update のみ:461808</span><span class="sxs-lookup"><span data-stu-id="2f559-163">On Windows 10 April 2018 Update only: 461808</span></span><br/><br/> <span data-ttu-id="2f559-164">Windows 10 October 2018 Update を含むその他すべての OS バージョン:461814</span><span class="sxs-lookup"><span data-stu-id="2f559-164">On all other OS versions, including Windows 10 October 2018 Update: 461814</span></span>| <span data-ttu-id="2f559-165">.NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="2f559-165">.NET Framework 4.7.2</span></span> |
    
<a name="net_c"></a> 
## <a name="to-find-net-framework-versions-by-querying-the-registry-in-code-net-framework-1-4"></a><span data-ttu-id="2f559-166">コードでレジストリを照会して .NET Framework のバージョンを検索するには (.NET Framework 1 ～ 4)</span><span class="sxs-lookup"><span data-stu-id="2f559-166">To find .NET Framework versions by querying the registry in code (.NET Framework 1-4)</span></span>

- <span data-ttu-id="2f559-167"><xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> クラスを使用して、Windows レジストリの HKEY_LOCAL_MACHINE の下にある Software\Microsoft\NET Framework Setup\NDP\ サブキーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2f559-167">Use the <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> class to access the Software\Microsoft\NET Framework Setup\NDP\ subkey under HKEY_LOCAL_MACHINE in the Windows registry.</span></span>

     <span data-ttu-id="2f559-168">このクエリの例を次のコードに示します。</span><span class="sxs-lookup"><span data-stu-id="2f559-168">The following code shows an example of this query.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f559-169">このコードは [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 以降を検出する方法を示すコードではありません。</span><span class="sxs-lookup"><span data-stu-id="2f559-169">This code does not show how to detect the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or later.</span></span> <span data-ttu-id="2f559-170">前のセクションで説明したように、これらのバージョンを検出するには、`Release` DWORD を確認してください。</span><span class="sxs-lookup"><span data-stu-id="2f559-170">Check the `Release` DWORD to detect those versions, as described in the previous section.</span></span> <span data-ttu-id="2f559-171">[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 以降のバージョンを検出するコードについては、この記事の次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f559-171">For code that does detect the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or later versions, see the next section in this article.</span></span>

     [!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed1.cs)]
     [!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed1.vb)]

     <span data-ttu-id="2f559-172">この例では次のような出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="2f559-172">The example produces output that's similar to the following:</span></span>

    ```
    v2.0.50727  2.0.50727.4016  SP2
    v3.0  3.0.30729.4037  SP2
    v3.5  3.5.30729.01  SP1
    v4
      Client  4.0.30319
      Full  4.0.30319
    ```

<a name="net_d"></a> 
## <a name="to-find-net-framework-versions-by-querying-the-registry-in-code-net-framework-45-and-later"></a><span data-ttu-id="2f559-173">コードでレジストリを照会して .NET Framework のバージョンを検索するには (.NET Framework 4.5 以降)</span><span class="sxs-lookup"><span data-stu-id="2f559-173">To find .NET Framework versions by querying the registry in code (.NET Framework 4.5 and later)</span></span>

1. <span data-ttu-id="2f559-174">`Release` DWORD がある場合は、.NET Framework 4.5 以降がコンピューターにインストールされています。</span><span class="sxs-lookup"><span data-stu-id="2f559-174">The existence of the `Release` DWORD indicates that the .NET Framework 4.5 or later has been installed on a computer.</span></span> <span data-ttu-id="2f559-175">キーワードの値はインストールされているバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="2f559-175">The value of the keyword indicates the installed version.</span></span> <span data-ttu-id="2f559-176">このキーワードを確認するには、<xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> クラスの <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A> メソッドと <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A> メソッドを使って、Windows レジストリの HKEY_LOCAL_MACHINE の下にある Software\Microsoft\NET Framework Setup\NDP\v4\Full サブキーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2f559-176">To check this keyword, use the <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A> and <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A> methods of the <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> class to access the Software\Microsoft\NET Framework Setup\NDP\v4\Full subkey under HKEY_LOCAL_MACHINE in the Windows registry.</span></span>

2. <span data-ttu-id="2f559-177">`Release` キーワードの値を確認して、インストールされているバージョンを決定します。</span><span class="sxs-lookup"><span data-stu-id="2f559-177">Check the value of the `Release` keyword to determine the installed version.</span></span> <span data-ttu-id="2f559-178">上位互換性を確認するには、テーブルに示されている値以上の値があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f559-178">To be forward-compatible, you can check for a value greater than or equal to the values listed in the table.</span></span> <span data-ttu-id="2f559-179">.NET Framework のバージョンと関連付けられた `Release` キーワードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="2f559-179">Here are the .NET Framework versions and associated `Release` keywords.</span></span>

    [!INCLUDE[Release key values note](~/includes/version-keys-note.md)]

    |<span data-ttu-id="2f559-180">Version</span><span class="sxs-lookup"><span data-stu-id="2f559-180">Version</span></span>|<span data-ttu-id="2f559-181">Release DWORD の値</span><span class="sxs-lookup"><span data-stu-id="2f559-181">Value of the Release DWORD</span></span>|
    |-------------|--------------------------------|
    |<span data-ttu-id="2f559-182">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="2f559-182">.NET Framework 4.5</span></span>|<span data-ttu-id="2f559-183">378389</span><span class="sxs-lookup"><span data-stu-id="2f559-183">378389</span></span>|
    |<span data-ttu-id="2f559-184">Windows 8.1 でインストールされた .NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="2f559-184">.NET Framework 4.5.1 installed with Windows 8.1</span></span>|<span data-ttu-id="2f559-185">378675</span><span class="sxs-lookup"><span data-stu-id="2f559-185">378675</span></span>|
    |<span data-ttu-id="2f559-186">Windows 8、Windows 7 SP1、または Windows Vista SP2 上でインストールされた .NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="2f559-186">.NET Framework 4.5.1 installed on Windows 8, Windows 7 SP1, or Windows Vista SP2</span></span>|<span data-ttu-id="2f559-187">378758</span><span class="sxs-lookup"><span data-stu-id="2f559-187">378758</span></span>|
    |<span data-ttu-id="2f559-188">.NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="2f559-188">.NET Framework 4.5.2</span></span>|<span data-ttu-id="2f559-189">379893</span><span class="sxs-lookup"><span data-stu-id="2f559-189">379893</span></span>|
    |<span data-ttu-id="2f559-190">Windows 10 でインストールされた .NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="2f559-190">.NET Framework 4.6 installed with Windows 10</span></span>|<span data-ttu-id="2f559-191">393295</span><span class="sxs-lookup"><span data-stu-id="2f559-191">393295</span></span>|
    |<span data-ttu-id="2f559-192">その他のすべての Windows OS バージョンにインストールされた .NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="2f559-192">.NET Framework 4.6 installed on all other Windows OS versions</span></span>|<span data-ttu-id="2f559-193">393297</span><span class="sxs-lookup"><span data-stu-id="2f559-193">393297</span></span>|
    |<span data-ttu-id="2f559-194">Windows 10 にインストールされた .NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="2f559-194">.NET Framework 4.6.1 installed on Windows 10</span></span>|<span data-ttu-id="2f559-195">394254</span><span class="sxs-lookup"><span data-stu-id="2f559-195">394254</span></span>|
    |<span data-ttu-id="2f559-196">その他のすべての Windows OS バージョンにインストールされた .NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="2f559-196">.NET Framework 4.6.1 installed on all other Windows OS versions</span></span>|<span data-ttu-id="2f559-197">394271</span><span class="sxs-lookup"><span data-stu-id="2f559-197">394271</span></span>|
    |<span data-ttu-id="2f559-198">Windows 10 Anniversary Update および Windows Server 2016 にインストールされた .NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="2f559-198">.NET Framework 4.6.2 installed on Windows 10 Anniversary Update and Windows Server 2016</span></span>|<span data-ttu-id="2f559-199">394802</span><span class="sxs-lookup"><span data-stu-id="2f559-199">394802</span></span>|
    |<span data-ttu-id="2f559-200">その他のすべての Windows OS バージョンにインストールされた .NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="2f559-200">.NET Framework 4.6.2 installed on all other Windows OS versions</span></span>|<span data-ttu-id="2f559-201">394806</span><span class="sxs-lookup"><span data-stu-id="2f559-201">394806</span></span>|
    |<span data-ttu-id="2f559-202">Windows 10 Creators Update にインストールされた .NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="2f559-202">.NET Framework 4.7 installed on Windows 10 Creators Update</span></span>|<span data-ttu-id="2f559-203">460798</span><span class="sxs-lookup"><span data-stu-id="2f559-203">460798</span></span>|
    |<span data-ttu-id="2f559-204">その他のすべての Windows OS バージョンにインストールされた .NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="2f559-204">.NET Framework 4.7 installed on all other Windows OS versions</span></span>|<span data-ttu-id="2f559-205">460805</span><span class="sxs-lookup"><span data-stu-id="2f559-205">460805</span></span>|
    |<span data-ttu-id="2f559-206">Windows 10 Fall Creators Update にインストールされた .NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="2f559-206">.NET Framework 4.7.1 installed on Windows 10 Fall Creators Update</span></span>|<span data-ttu-id="2f559-207">461308</span><span class="sxs-lookup"><span data-stu-id="2f559-207">461308</span></span>|
    |<span data-ttu-id="2f559-208">その他のすべての Windows OS バージョンにインストールされた .NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="2f559-208">.NET Framework 4.7.1 installed on all other Windows OS versions</span></span>|<span data-ttu-id="2f559-209">461310</span><span class="sxs-lookup"><span data-stu-id="2f559-209">461310</span></span>|
    |<span data-ttu-id="2f559-210">Windows 10 October 2018 Update にインストールされた .NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="2f559-210">.NET Framework 4.7.2 installed on Windows 10 October 2018 Update</span></span>|<span data-ttu-id="2f559-211">461814</span><span class="sxs-lookup"><span data-stu-id="2f559-211">461814</span></span>|
    |<span data-ttu-id="2f559-212">Windows 10 April 2018 Update にインストールされた .NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="2f559-212">.NET Framework 4.7.2 installed on Windows 10 April 2018 Update</span></span>|<span data-ttu-id="2f559-213">461808</span><span class="sxs-lookup"><span data-stu-id="2f559-213">461808</span></span>|
    |<span data-ttu-id="2f559-214">Windows 10 Fall Creators Update 以前の OS バージョンにインストールされた .NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="2f559-214">.NET Framework 4.7.2 installed on Windows 10 Fall Creators Update and earlier OS versions</span></span>|<span data-ttu-id="2f559-215">461814</span><span class="sxs-lookup"><span data-stu-id="2f559-215">461814</span></span>|
    
     <span data-ttu-id="2f559-216">レジストリの `Release` 値を確認して [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 以降のバージョンの .NET Framework がインストールされているかどうかを判断する例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="2f559-216">The following example checks the `Release` value in the registry to determine whether the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or a later version of the .NET Framework is installed.</span></span>

     [!code-csharp[ListVersions#5](../../../samples/snippets/csharp/framework/migration-guide/versions-installed3.cs)]
     [!code-vb[ListVersions#5](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed3.vb)]

     <span data-ttu-id="2f559-217">この例では、バージョンのチェックで推奨されている方法に従います。</span><span class="sxs-lookup"><span data-stu-id="2f559-217">This example follows the recommended practice for version checking:</span></span>

    - <span data-ttu-id="2f559-218">`Release` エントリの値が既知のリリース キー値*以上*かどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="2f559-218">It checks whether the value of the `Release` entry is *greater than or equal to* the value of the known release keys.</span></span>

    - <span data-ttu-id="2f559-219">最新バージョンから最も古いバージョンの順にチェックします。</span><span class="sxs-lookup"><span data-stu-id="2f559-219">It checks in order from most recent version to earliest version.</span></span>

<a name="ps_a"></a> 
## <a name="to-check-for-a-minimum-required-net-framework-version-by-querying-the-registry-in-powershell-net-framework-45-and-later"></a><span data-ttu-id="2f559-220">PowerShell でレジストリを照会して .NET Framework の最低限必要なバージョンを確認するには(.NET Framework 4.5 以降)</span><span class="sxs-lookup"><span data-stu-id="2f559-220">To check for a minimum-required .NET Framework version by querying the registry in PowerShell (.NET Framework 4.5 and later)</span></span>

- <span data-ttu-id="2f559-221">次の例では、`Release` キーワードの値を確認して、Windows オペレーティング システムのバージョンに関係なく、.NET Framework 4.6.2 以降がインストールされているかどうかを判断します (インストールされている場合は `True` を返し、それ以外の場合は `False`を返します)。</span><span class="sxs-lookup"><span data-stu-id="2f559-221">The following example checks the value of the `Release` keyword to determine whether .NET Framework 4.6.2 or higher is installed, regardless of Windows OS version (returning `True` if it is and `False` otherwise).</span></span>

    ```PowerShell
    # PowerShell 5
    Get-ChildItem 'HKLM:\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full\' | Get-ItemPropertyValue -Name Release | Foreach-Object { $_ -ge 394802 } 
    ```

    ```PowerShell
    # PowerShell 4
    (Get-ItemProperty "HKLM:SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full").Release -gt 394802
    ```

    <span data-ttu-id="2f559-222">前の例で、`394802` を次の表の別の値に置き換えて、別の最低限必要な .NET Framework バージョンを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="2f559-222">You can replace `394802` in the previous example with another value from the following table to check for a different minimum-required .NET Framework version.</span></span>
  
    |<span data-ttu-id="2f559-223">Version</span><span class="sxs-lookup"><span data-stu-id="2f559-223">Version</span></span>|<span data-ttu-id="2f559-224">Release DWORD の最小値</span><span class="sxs-lookup"><span data-stu-id="2f559-224">Minimum value of the Release DWORD</span></span>|
    |-------------|--------------------------------|
    |<span data-ttu-id="2f559-225">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="2f559-225">.NET Framework 4.5</span></span>|<span data-ttu-id="2f559-226">378389</span><span class="sxs-lookup"><span data-stu-id="2f559-226">378389</span></span>|
    |<span data-ttu-id="2f559-227">.NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="2f559-227">.NET Framework 4.5.1</span></span>|<span data-ttu-id="2f559-228">378675</span><span class="sxs-lookup"><span data-stu-id="2f559-228">378675</span></span>|
    |<span data-ttu-id="2f559-229">.NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="2f559-229">.NET Framework 4.5.2</span></span>|<span data-ttu-id="2f559-230">379893</span><span class="sxs-lookup"><span data-stu-id="2f559-230">379893</span></span>|
    |[!INCLUDE[net_v46](../../../includes/net-v46-md.md)]|<span data-ttu-id="2f559-231">393295</span><span class="sxs-lookup"><span data-stu-id="2f559-231">393295</span></span>|
    |[!INCLUDE[net_v461](../../../includes/net-v461-md.md)]|<span data-ttu-id="2f559-232">394254</span><span class="sxs-lookup"><span data-stu-id="2f559-232">394254</span></span>|
    |[!INCLUDE[net_v462](../../../includes/net-v462-md.md)]|<span data-ttu-id="2f559-233">394802</span><span class="sxs-lookup"><span data-stu-id="2f559-233">394802</span></span>|
    |<span data-ttu-id="2f559-234">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="2f559-234">.NET Framework 4.7</span></span>|<span data-ttu-id="2f559-235">460798</span><span class="sxs-lookup"><span data-stu-id="2f559-235">460798</span></span>|
    |<span data-ttu-id="2f559-236">.NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="2f559-236">.NET Framework 4.7.1</span></span>|<span data-ttu-id="2f559-237">461308</span><span class="sxs-lookup"><span data-stu-id="2f559-237">461308</span></span>|
    |<span data-ttu-id="2f559-238">.NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="2f559-238">.NET Framework 4.7.2</span></span>|<span data-ttu-id="2f559-239">461808</span><span class="sxs-lookup"><span data-stu-id="2f559-239">461808</span></span>|

<a name="clr_a"></a> 
## <a name="to-find-the-current-runtime-version-by-using-the-clrver-tool"></a><span data-ttu-id="2f559-240">Clrver ツールを使用して現在のランタイムのバージョンを確認する方法</span><span class="sxs-lookup"><span data-stu-id="2f559-240">To find the current runtime version by using the Clrver tool</span></span>

- <span data-ttu-id="2f559-241">CLR バージョン ツール (Clrver.exe) を使用して、コンピューターにインストールされている共通言語ランタイムのバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f559-241">Use the CLR Version Tool (Clrver.exe) to determine which versions of the common language runtime are installed on a computer.</span></span>

     <span data-ttu-id="2f559-242">Visual Studio 用開発者コマンド プロンプトで「`clrver`」と入力します。</span><span class="sxs-lookup"><span data-stu-id="2f559-242">From a Developer Command Prompt for Visual Studio, enter `clrver`.</span></span> <span data-ttu-id="2f559-243">次のような出力が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f559-243">This command produces output similar to the following:</span></span>

    ```
    Versions installed on the machine:
    v2.0.50727
    v4.0.30319
    ```

     <span data-ttu-id="2f559-244">このツールの使用については、「[Clrver.exe (CLR Version Tool)](~/docs/framework/tools/clrver-exe-clr-version-tool.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f559-244">For more information about using this tool, see [Clrver.exe (CLR Version Tool)](~/docs/framework/tools/clrver-exe-clr-version-tool.md).</span></span>

<a name="clr_b"></a> 
## <a name="to-find-the-current-runtime-version-by-querying-the-environment-class-in-code"></a><span data-ttu-id="2f559-245">コードで Environment クラスを照会して現在のランタイム バージョンを確認するには</span><span class="sxs-lookup"><span data-stu-id="2f559-245">To find the current runtime version by querying the Environment class in code</span></span>

- <span data-ttu-id="2f559-246"><xref:System.Environment.Version%2A?displayProperty=nameWithType> プロパティを照会して <xref:System.Version> オブジェクトを取得し、現在コードを実行しているランタイムのバージョンを識別します。</span><span class="sxs-lookup"><span data-stu-id="2f559-246">Query the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property to retrieve a <xref:System.Version> object that identifies the version of the runtime that is currently executing the code.</span></span> <span data-ttu-id="2f559-247">メジャー リリースの識別子 (バージョン 4.0 の "4" など) を取得するには <xref:System.Version.Major%2A?displayProperty=nameWithType> プロパティを、マイナー リリースの識別子 (バージョン 4.0 の "0" など) を取得するには <xref:System.Version.Minor%2A?displayProperty=nameWithType> プロパティを、バージョン文字列全体 (次のコードに示すような "4.0.30319.18010" など) を取得するには <xref:System.Object.ToString%2A?displayProperty=nameWithType> メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f559-247">You can use the <xref:System.Version.Major%2A?displayProperty=nameWithType> property to get the major release identifier (for example, "4" for version 4.0), the <xref:System.Version.Minor%2A?displayProperty=nameWithType> property to get the minor release identifier (for example, "0" for version 4.0), or the <xref:System.Object.ToString%2A?displayProperty=nameWithType> method to get the entire version string (for example, "4.0.30319.18010", as shown in the following code).</span></span> <span data-ttu-id="2f559-248">このプロパティは、現在コードを実行しているランタイムのバージョンを表す単一の値を返しますが、アセンブリのバージョンやコンピューターにインストールされている可能性があるランタイムの他のバージョンは返しません。</span><span class="sxs-lookup"><span data-stu-id="2f559-248">This property returns a single value that reflects the version of the runtime that is currently executing the code; it does not return assembly versions or other versions of the runtime that may have been installed on the computer.</span></span>

     <span data-ttu-id="2f559-249">.NET Framework バージョン 4、4.5、4.5.1、および 4.5.2 の場合は、<xref:System.Environment.Version%2A?displayProperty=nameWithType> プロパティから返される <xref:System.Version> オブジェクトの文字列表現が `4.0.30319.xxxxx` という形式になっています。</span><span class="sxs-lookup"><span data-stu-id="2f559-249">For the .NET Framework Versions 4, 4.5, 4.5.1, and 4.5.2, the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property returns a <xref:System.Version> object whose string representation has the form `4.0.30319.xxxxx`.</span></span> <span data-ttu-id="2f559-250">.NET Framework 4.6 以降の場合は、`4.0.30319.42000` という形式です。</span><span class="sxs-lookup"><span data-stu-id="2f559-250">For the .NET Framework 4.6 and later, it has the form `4.0.30319.42000`.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2f559-251">[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 以降の場合、ランタイムのバージョンの検出に <xref:System.Environment.Version%2A?displayProperty=nameWithType> プロパティを使用することは推奨されません。</span><span class="sxs-lookup"><span data-stu-id="2f559-251">For the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] and later, we do not recommend using the  <xref:System.Environment.Version%2A?displayProperty=nameWithType> property to detect the version of the runtime.</span></span> <span data-ttu-id="2f559-252">代わりに、この記事で前述した「[コードでレジストリを照会して .NET Framework のバージョンを検索するには (.NET Framework 4.5 以降)](#net_d)」に従って、レジストリを紹介することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2f559-252">Instead, we recommend that you query the registry, as described in the [To find .NET Framework versions by querying the registry in code (.NET Framework 4.5 and later)](#net_d) section earlier in this article.</span></span>

     <span data-ttu-id="2f559-253">次に、<xref:System.Environment.Version%2A?displayProperty=nameWithType> プロパティを照会してランタイム バージョン情報を取得する例を示します。</span><span class="sxs-lookup"><span data-stu-id="2f559-253">Here's an example of querying the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property for runtime version information:</span></span>

     [!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed2.cs)]
     [!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed2.vb)]

     <span data-ttu-id="2f559-254">この例では次のような出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="2f559-254">The example produces output that's similar to the following:</span></span>

    ```
    Version: 4.0.30319.18010
    ```

## <a name="see-also"></a><span data-ttu-id="2f559-255">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f559-255">See also</span></span>

- [<span data-ttu-id="2f559-256">方法: インストールされている .NET Framework の更新プログラムを確認する</span><span class="sxs-lookup"><span data-stu-id="2f559-256">How to: Determine Which .NET Framework Updates Are Installed</span></span>](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)
- [<span data-ttu-id="2f559-257">開発者向けの .NET Framework のインストール</span><span class="sxs-lookup"><span data-stu-id="2f559-257">Install the .NET Framework for developers</span></span>](../../../docs/framework/install/guide-for-developers.md)
- [<span data-ttu-id="2f559-258">バージョンおよび依存関係</span><span class="sxs-lookup"><span data-stu-id="2f559-258">Versions and Dependencies</span></span>](~/docs/framework/migration-guide/versions-and-dependencies.md)
