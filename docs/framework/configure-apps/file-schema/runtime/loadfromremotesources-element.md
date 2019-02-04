---
title: <loadFromRemoteSources> 要素
ms.date: 05/24/2018
helpviewer_keywords:
- loadFromRemoteSources element
- <loadFromRemoteSources> element
ms.assetid: 006d1280-2ac3-4db6-a984-a3d4e275046a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7568129f30267b212737ec8aa688cf882e19bbff
ms.sourcegitcommit: b8ace47d839f943f785b89e2fff8092b0bf8f565
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2019
ms.locfileid: "55675310"
---
# <a name="loadfromremotesources-element"></a><span data-ttu-id="5fca1-102">\<loadFromRemoteSources > 要素</span><span class="sxs-lookup"><span data-stu-id="5fca1-102">\<loadFromRemoteSources> element</span></span>
<span data-ttu-id="5fca1-103">リモート ソースから読み込まれたアセンブリに対して、.NET Framework 4 以降の完全な信頼を付与するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5fca1-103">Specifies whether assemblies loaded from remote sources should be granted full trust in .NET Framework 4 and later.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="5fca1-104">場合は、Visual Studio プロジェクトのエラー一覧またはビルド エラーのエラー メッセージのため、この記事にダイレクトされたを参照してください。[方法。Visual Studio で Web からアセンブリを使用して](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee890038(v=vs.100))します。</span><span class="sxs-lookup"><span data-stu-id="5fca1-104">If you were directed to this article because of an error message in the Visual Studio project error list or a build error, see [How to: Use an Assembly from the Web in Visual Studio](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee890038(v=vs.100)).</span></span>  
  
 <span data-ttu-id="5fca1-105">\<configuration></span><span class="sxs-lookup"><span data-stu-id="5fca1-105">\<configuration></span></span>  
<span data-ttu-id="5fca1-106">\<runtime></span><span class="sxs-lookup"><span data-stu-id="5fca1-106">\<runtime></span></span>  
<span data-ttu-id="5fca1-107">\<loadFromRemoteSources></span><span class="sxs-lookup"><span data-stu-id="5fca1-107">\<loadFromRemoteSources></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5fca1-108">構文</span><span class="sxs-lookup"><span data-stu-id="5fca1-108">Syntax</span></span>  
  
```xml  
<loadFromRemoteSources    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5fca1-109">属性と要素</span><span class="sxs-lookup"><span data-stu-id="5fca1-109">Attributes and elements</span></span>
 <span data-ttu-id="5fca1-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="5fca1-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5fca1-111">属性</span><span class="sxs-lookup"><span data-stu-id="5fca1-111">Attributes</span></span>  
  
|<span data-ttu-id="5fca1-112">属性</span><span class="sxs-lookup"><span data-stu-id="5fca1-112">Attribute</span></span>|<span data-ttu-id="5fca1-113">説明</span><span class="sxs-lookup"><span data-stu-id="5fca1-113">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="5fca1-114">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="5fca1-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="5fca1-115">リモート ソースから読み込まれたアセンブリに対して、完全な信頼を付与する必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5fca1-115">Specifies whether an assembly that is loaded from a remote source should be granted full trust.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="5fca1-116">enabled 属性</span><span class="sxs-lookup"><span data-stu-id="5fca1-116">enabled attribute</span></span>  
  
|<span data-ttu-id="5fca1-117">[値]</span><span class="sxs-lookup"><span data-stu-id="5fca1-117">Value</span></span>|<span data-ttu-id="5fca1-118">説明</span><span class="sxs-lookup"><span data-stu-id="5fca1-118">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="5fca1-119">リモート ソースからアプリケーションに完全な信頼を付与しないでください。</span><span class="sxs-lookup"><span data-stu-id="5fca1-119">Do not grant full trust to applications from remote sources.</span></span> <span data-ttu-id="5fca1-120">既定値です。</span><span class="sxs-lookup"><span data-stu-id="5fca1-120">This is the default.</span></span>|  
|`true`|<span data-ttu-id="5fca1-121">リモート ソースからアプリケーションへの完全な信頼を付与します。</span><span class="sxs-lookup"><span data-stu-id="5fca1-121">Grant full trust to applications from remote sources.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5fca1-122">子要素</span><span class="sxs-lookup"><span data-stu-id="5fca1-122">Child elements</span></span>  
 <span data-ttu-id="5fca1-123">なし。</span><span class="sxs-lookup"><span data-stu-id="5fca1-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5fca1-124">親要素</span><span class="sxs-lookup"><span data-stu-id="5fca1-124">Parent elements</span></span>  
  
|<span data-ttu-id="5fca1-125">要素</span><span class="sxs-lookup"><span data-stu-id="5fca1-125">Element</span></span>|<span data-ttu-id="5fca1-126">説明</span><span class="sxs-lookup"><span data-stu-id="5fca1-126">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="5fca1-127">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="5fca1-127">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="5fca1-128">ランタイム初期化オプションに関する情報を含んでいます。</span><span class="sxs-lookup"><span data-stu-id="5fca1-128">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5fca1-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="5fca1-129">Remarks</span></span>

<span data-ttu-id="5fca1-130">.NET Framework 3.5 以前のバージョンで、リモートの場所からアセンブリを読み込む場合に、アセンブリ内のコードを読み込み元のゾーンに依存している許可セットで部分信頼で実行されます。</span><span class="sxs-lookup"><span data-stu-id="5fca1-130">In the .NET Framework 3.5 and earlier versions, if you load an assembly from a remote location, code in the assembly runs in partial trust with a grant set that depends on the zone from which it is loaded.</span></span> <span data-ttu-id="5fca1-131">たとえば、web サイトからアセンブリをロードする場合インターネット ゾーンに読み込まれ、インターネット アクセス許可のセットを許可は。</span><span class="sxs-lookup"><span data-stu-id="5fca1-131">For example, if you load an assembly from a website, it is loaded into the Internet zone and granted the Internet permission set.</span></span> <span data-ttu-id="5fca1-132">つまり、インターネットのサンド ボックス内で実行します。</span><span class="sxs-lookup"><span data-stu-id="5fca1-132">In other words, it executes in an Internet sandbox.</span></span>

<span data-ttu-id="5fca1-133">以降、.NET Framework 4 では、コード アクセス セキュリティ (CAS) ポリシーが無効になり、アセンブリが完全信頼で読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="5fca1-133">Starting with the .NET Framework 4, code access security (CAS) policy is disabled and assemblies are loaded in full trust.</span></span> <span data-ttu-id="5fca1-134">読み込まれたアセンブリに完全な信頼を付与これは通常、<xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType>サンド ボックス化された以前されていたメソッド。</span><span class="sxs-lookup"><span data-stu-id="5fca1-134">Ordinarily, this would grant full trust to assemblies loaded with the <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType> method that previously had been sandboxed.</span></span> <span data-ttu-id="5fca1-135">これを防ぐためには、リモート ソースから読み込まれるアセンブリでコードを実行する機能は既定で無効になります。</span><span class="sxs-lookup"><span data-stu-id="5fca1-135">To prevent this, the ability to run code in assemblies loaded from a remote source is disabled by default.</span></span> <span data-ttu-id="5fca1-136">リモートのアセンブリを読み込もうとした場合、既定で、<xref:System.IO.FileLoadException>次がスローされるように、例外メッセージ。</span><span class="sxs-lookup"><span data-stu-id="5fca1-136">By default, if you attempt to load a remote assembly, a <xref:System.IO.FileLoadException> with an exception message like the following is thrown:</span></span>

```text
System.IO.FileNotFoundException: Could not load file or assembly 'file:assem.dll' or one of its dependencies. Operation is not supported. 
(Exception from HRESULT: 0x80131515)
File name: 'file:assem.dll' ---> 
System.NotSupportedException: An attempt was made to load an assembly from a network location which would have caused the assembly 
to be sandboxed in previous versions of the .NET Framework. This release of the .NET Framework does not enable CAS policy by default, 
so this load may be dangerous. If this load is not intended to sandbox the assembly, please enable the loadFromRemoteSources switch. 
```

<span data-ttu-id="5fca1-137">アセンブリを読み込むし、そのコードを実行、する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="5fca1-137">To load the assembly and execute its code, you must either:</span></span>

- <span data-ttu-id="5fca1-138">アセンブリのサンド ボックスを明示的に作成 (を参照してください[方法。サンド ボックスで部分信頼コードを実行](../../../../../docs/framework/misc/how-to-run-partially-trusted-code-in-a-sandbox.md))。</span><span class="sxs-lookup"><span data-stu-id="5fca1-138">Explicitly create a sandbox for the assembly (see [How to: Run Partially Trusted Code in a Sandbox](../../../../../docs/framework/misc/how-to-run-partially-trusted-code-in-a-sandbox.md)).</span></span>

- <span data-ttu-id="5fca1-139">完全信頼でアセンブリのコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="5fca1-139">Run the assembly's code in full trust.</span></span> <span data-ttu-id="5fca1-140">構成することで、これを行う、`<loadFromRemoteSources>`要素。</span><span class="sxs-lookup"><span data-stu-id="5fca1-140">You do this by configuring the `<loadFromRemoteSources>` element.</span></span> <span data-ttu-id="5fca1-141">.NET Framework の以前のバージョンで部分信頼で実行するアセンブリが .NET Framework 4 およびそれ以降のバージョンで完全な信頼で実行されるように指定できます。</span><span class="sxs-lookup"><span data-stu-id="5fca1-141">It lets you specify that the assemblies that run in partial trust in earlier versions of the .NET Framework now run in full trust in the .NET Framework 4 and later versions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5fca1-142">アセンブリが完全信頼で実行されない場合は、この構成要素を設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="5fca1-142">If the assembly should not run in full trust, do not set this configuration element.</span></span> <span data-ttu-id="5fca1-143">代わりに、作成、セキュリティで保護された<xref:System.AppDomain>アセンブリの読み込み先となります。</span><span class="sxs-lookup"><span data-stu-id="5fca1-143">Instead, create a sandboxed <xref:System.AppDomain> in which to load the assembly.</span></span>

<span data-ttu-id="5fca1-144">`enabled`属性、`<loadFromRemoteSources>`要素は、コード アクセス セキュリティ (CAS) を無効にした場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="5fca1-144">The `enabled` attribute for the `<loadFromRemoteSources>` element is effective only when code access security (CAS) is disabled.</span></span> <span data-ttu-id="5fca1-145">既定では、.NET Framework 4 およびそれ以降のバージョンの CAS ポリシーが無効になります。</span><span class="sxs-lookup"><span data-stu-id="5fca1-145">By default, CAS policy is disabled in the .NET Framework 4 and later versions.</span></span> <span data-ttu-id="5fca1-146">設定した場合`enabled`に`true`、リモートのアセンブリに完全な信頼が与えられます。</span><span class="sxs-lookup"><span data-stu-id="5fca1-146">If you set `enabled` to `true`, remote assemblies are granted full trust.</span></span>

<span data-ttu-id="5fca1-147">場合`enabled`に設定されていない`true`、<xref:System.IO.FileLoadException>次の条件のいずれかでスローされます。</span><span class="sxs-lookup"><span data-stu-id="5fca1-147">If `enabled` is not set to `true`, a <xref:System.IO.FileLoadException> is thrown under the either of the following conditions:</span></span>

- <span data-ttu-id="5fca1-148">現在のドメインのサンド ボックス化動作は、.NET Framework 3.5 では、その動作からは異なります。</span><span class="sxs-lookup"><span data-stu-id="5fca1-148">The sandboxing behavior of the current domain is different from its behavior in the .NET Framework 3.5.</span></span> <span data-ttu-id="5fca1-149">これは、CAS ポリシーを無効にして、現在のドメインがサンド ボックス化が必要です。</span><span class="sxs-lookup"><span data-stu-id="5fca1-149">This requires CAS policy to be disabled, and the current domain not to be sandboxed.</span></span>

- <span data-ttu-id="5fca1-150">読み込まれるアセンブリでない、`MyComputer`ゾーン。</span><span class="sxs-lookup"><span data-stu-id="5fca1-150">The assembly being loaded is not from the `MyComputer` zone.</span></span>

<span data-ttu-id="5fca1-151">設定、`<loadFromRemoteSources>`要素`true`によりこの例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="5fca1-151">Setting the `<loadFromRemoteSources>` element to `true` prevents this exception from being thrown.</span></span> <span data-ttu-id="5fca1-152">これにより、ことをせず、サンド ボックスに、共通言語ランタイムのセキュリティを読み込まれたアセンブリを指定してで実行を許可することができます完全な信頼。</span><span class="sxs-lookup"><span data-stu-id="5fca1-152">It enables you to specify that you are not relying on the common language runtime to sandbox the loaded assemblies for security, and that they can be allowed to execute in full trust.</span></span>

## <a name="notes"></a><span data-ttu-id="5fca1-153">メモ</span><span class="sxs-lookup"><span data-stu-id="5fca1-153">Notes</span></span>

- <span data-ttu-id="5fca1-154">.NET Framework 4.5 以降のバージョンで、アセンブリをローカル ネットワーク共有に完全信頼で実行既定では有効にする必要はありません、`<loadFromRemoteSources>`要素。</span><span class="sxs-lookup"><span data-stu-id="5fca1-154">In the .NET Framework 4.5 and later versions, assemblies on local network shares run in full trust by default; you do not have to enable the `<loadFromRemoteSources>` element.</span></span>

- <span data-ttu-id="5fca1-155">アプリケーションが web サイトからコピーされた場合としてマークされている Windows で web アプリケーションでは、ローカル コンピューター上にある場合でもです。</span><span class="sxs-lookup"><span data-stu-id="5fca1-155">If an application has been copied from the web, it is flagged by Windows as being a web application, even if it resides on the local computer.</span></span> <span data-ttu-id="5fca1-156">その指定を変更するには、ファイルのプロパティを変更することで、または使用することができます、`<loadFromRemoteSources>`完全信頼のアセンブリに与える要素。</span><span class="sxs-lookup"><span data-stu-id="5fca1-156">You can change that designation by changing its file properties, or you can use the `<loadFromRemoteSources>` element to grant the assembly full trust.</span></span> <span data-ttu-id="5fca1-157">代わりに、使用することができます、<xref:System.Reflection.Assembly.UnsafeLoadFrom%2A>オペレーティング システムは、web から読み込まれたものとしてフラグが設定されるローカル アセンブリを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="5fca1-157">As an alternative, you can use the <xref:System.Reflection.Assembly.UnsafeLoadFrom%2A> method to load a local assembly that the operating system has flagged as having been loaded from the web.</span></span>

- <span data-ttu-id="5fca1-158">取得することがあります、 <xref:System.IO.FileLoadException> Windows Virtual PC アプリケーションで実行されているアプリケーションでします。</span><span class="sxs-lookup"><span data-stu-id="5fca1-158">You may get a <xref:System.IO.FileLoadException> in an application that is running in a Windows Virtual PC application.</span></span> <span data-ttu-id="5fca1-159">これは、ホスト コンピュータ上のリンクされたフォルダーからファイルをロードしようとするときに発生します。</span><span class="sxs-lookup"><span data-stu-id="5fca1-159">This can happen when you try to load a file from linked folders on the hosting computer.</span></span> <span data-ttu-id="5fca1-160">経由でリンクされているフォルダーからファイルをロードしようとするときに起こる可能性も[Remote Desktop Services](https://go.microsoft.com/fwlink/?LinkId=182775) (Terminal Services)。</span><span class="sxs-lookup"><span data-stu-id="5fca1-160">It can also occur when you try to load a file from a folder linked over [Remote Desktop Services](https://go.microsoft.com/fwlink/?LinkId=182775) (Terminal Services).</span></span> <span data-ttu-id="5fca1-161">例外を避けるためには、次のように設定します。`enabled`に`true`します。</span><span class="sxs-lookup"><span data-stu-id="5fca1-161">To avoid the exception, set `enabled` to `true`.</span></span>

## <a name="configuration-file"></a><span data-ttu-id="5fca1-162">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="5fca1-162">Configuration file</span></span>

<span data-ttu-id="5fca1-163">この要素では、通常は、アプリケーション構成ファイルで使用しますが、コンテキストに応じて他の構成ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="5fca1-163">This element is typically used in the application configuration file, but can be used in other configuration files depending upon the context.</span></span> <span data-ttu-id="5fca1-164">詳細については、この記事を参照してください。[詳細暗黙的な使用の CAS ポリシー: loadFromRemoteSources](https://go.microsoft.com/fwlink/p/?LinkId=266839) .NET セキュリティ ブログにします。</span><span class="sxs-lookup"><span data-stu-id="5fca1-164">For more information, see the article [More Implicit Uses of CAS Policy: loadFromRemoteSources](https://go.microsoft.com/fwlink/p/?LinkId=266839) in the .NET Security blog.</span></span>  

## <a name="example"></a><span data-ttu-id="5fca1-165">例</span><span class="sxs-lookup"><span data-stu-id="5fca1-165">Example</span></span>

<span data-ttu-id="5fca1-166">次の例では、リモート ソースから読み込まれたアセンブリに完全な信頼を付与する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5fca1-166">The following example shows how to grant full trust to assemblies loaded from remote sources.</span></span>

```xml
<configuration>  
   <runtime>  
      <loadFromRemoteSources enabled="true"/>  
   </runtime>  
</configuration>  
```

## <a name="see-also"></a><span data-ttu-id="5fca1-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="5fca1-167">See also</span></span>

- [<span data-ttu-id="5fca1-168">CAS ポリシーの暗黙的な複数の使用: loadFromRemoteSources</span><span class="sxs-lookup"><span data-stu-id="5fca1-168">More Implicit Uses of CAS Policy: loadFromRemoteSources</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=266839)
- [<span data-ttu-id="5fca1-169">方法: サンドボックスで部分信頼コードを実行する</span><span class="sxs-lookup"><span data-stu-id="5fca1-169">How to: Run Partially Trusted Code in a Sandbox</span></span>](../../../../../docs/framework/misc/how-to-run-partially-trusted-code-in-a-sandbox.md)
- [<span data-ttu-id="5fca1-170">ランタイム設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="5fca1-170">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="5fca1-171">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="5fca1-171">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType>
