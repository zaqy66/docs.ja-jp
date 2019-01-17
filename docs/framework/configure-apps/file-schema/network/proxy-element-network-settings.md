---
title: '&lt;proxy&gt;要素 (ネットワーク設定)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/proxy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#proxy
helpviewer_keywords:
- <proxy> element
- proxy element
ms.assetid: 37a548d8-fade-4ac5-82ec-b49b6c6cb22a
ms.openlocfilehash: 3a6d5b080c74fbd3f6ebca9882c1667951cfcb91
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50183674"
---
# <a name="ltproxygt-element-network-settings"></a><span data-ttu-id="3a54d-102">&lt;proxy&gt;要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="3a54d-102">&lt;proxy&gt; Element (Network Settings)</span></span>
<span data-ttu-id="3a54d-103">プロキシ サーバーを定義します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-103">Defines a proxy server.</span></span>  
  
 <span data-ttu-id="3a54d-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="3a54d-104">\<configuration></span></span>  
<span data-ttu-id="3a54d-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="3a54d-105">\<system.net></span></span>  
<span data-ttu-id="3a54d-106">\<defaultProxy></span><span class="sxs-lookup"><span data-stu-id="3a54d-106">\<defaultProxy></span></span>  
<span data-ttu-id="3a54d-107">\<proxy></span><span class="sxs-lookup"><span data-stu-id="3a54d-107">\<proxy></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a54d-108">構文</span><span class="sxs-lookup"><span data-stu-id="3a54d-108">Syntax</span></span>  
  
```xml  
<proxy
  autoDetect="true|false|unspecified" 
  bypassonlocal="true|false|unspecified"
  proxyaddress="uriString"
  scriptLocation="uriString"
  usesystemdefault="true|false|unspecified"
/>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3a54d-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="3a54d-109">Attributes and Elements</span></span>  
 <span data-ttu-id="3a54d-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3a54d-111">属性</span><span class="sxs-lookup"><span data-stu-id="3a54d-111">Attributes</span></span>  
  
|<span data-ttu-id="3a54d-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="3a54d-112">**Attribute**</span></span>|<span data-ttu-id="3a54d-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="3a54d-113">**Description**</span></span>|  
|-------------------|---------------------|  
|`autoDetect`|<span data-ttu-id="3a54d-114">プロキシが自動的に検出されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-114">Specifies whether the proxy is automatically detected.</span></span> <span data-ttu-id="3a54d-115">既定値は `unspecified` です。</span><span class="sxs-lookup"><span data-stu-id="3a54d-115">The default value is `unspecified`.</span></span>|  
|`bypassonlocal`|<span data-ttu-id="3a54d-116">ローカル リソースに対してプロキシをバイパスするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-116">Specifies whether the proxy is bypassed for local resources.</span></span> <span data-ttu-id="3a54d-117">ローカル リソースには、ローカル サーバーが含まれます (`http://localhost`、 `http://loopback`、または`http://127.0.0.1`) とピリオドが付かないの URI (`http://webserver`)。</span><span class="sxs-lookup"><span data-stu-id="3a54d-117">Local resources include the local server (`http://localhost`, `http://loopback`, or `http://127.0.0.1`) and a URI without a period (`http://webserver`).</span></span> <span data-ttu-id="3a54d-118">既定値は `unspecified` です。</span><span class="sxs-lookup"><span data-stu-id="3a54d-118">The default value is `unspecified`.</span></span>|  
|`proxyaddress`|<span data-ttu-id="3a54d-119">プロキシに使用する URI を指定します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-119">Specifies the proxy URI to use.</span></span>|  
|`scriptLocation`|<span data-ttu-id="3a54d-120">構成スクリプトの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-120">Specifies the location of the configuration script.</span></span> <span data-ttu-id="3a54d-121">使用しないでください、`bypassonlocal`この属性を持つ属性です。</span><span class="sxs-lookup"><span data-stu-id="3a54d-121">Do not use the `bypassonlocal` attribute with this attribute.</span></span> |  
|`usesystemdefault`|<span data-ttu-id="3a54d-122">Internet Explorer のプロキシ設定を使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-122">Specifies whether to use Internet Explorer proxy settings.</span></span> <span data-ttu-id="3a54d-123">場合設定`true`、後続する属性は、Internet Explorer のプロキシ設定を上書きします。</span><span class="sxs-lookup"><span data-stu-id="3a54d-123">If set to `true`, subsequent attributes will override Internet Explorer proxy settings.</span></span> <span data-ttu-id="3a54d-124">既定値は `unspecified` です。</span><span class="sxs-lookup"><span data-stu-id="3a54d-124">The default value is `unspecified`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3a54d-125">子要素</span><span class="sxs-lookup"><span data-stu-id="3a54d-125">Child Elements</span></span>  
 <span data-ttu-id="3a54d-126">なし。</span><span class="sxs-lookup"><span data-stu-id="3a54d-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3a54d-127">親要素</span><span class="sxs-lookup"><span data-stu-id="3a54d-127">Parent Elements</span></span>  
  
|<span data-ttu-id="3a54d-128">**要素**</span><span class="sxs-lookup"><span data-stu-id="3a54d-128">**Element**</span></span>|<span data-ttu-id="3a54d-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="3a54d-129">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="3a54d-130">defaultProxy</span><span class="sxs-lookup"><span data-stu-id="3a54d-130">defaultProxy</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/defaultproxy-element-network-settings.md)|<span data-ttu-id="3a54d-131">ハイパーテキスト転送プロトコル (HTTP: Hypertext Transfer Protocol) プロキシ サーバーを構成します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-131">Configures the Hypertext Transfer Protocol (HTTP) proxy server.</span></span>|  
  
## <a name="text-value"></a><span data-ttu-id="3a54d-132">テキスト値</span><span class="sxs-lookup"><span data-stu-id="3a54d-132">Text Value</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3a54d-133">Remarks</span><span class="sxs-lookup"><span data-stu-id="3a54d-133">Remarks</span></span>  
 <span data-ttu-id="3a54d-134">`proxy`要素は、アプリケーションのプロキシ サーバーを定義します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-134">The `proxy` element defines a proxy server for an application.</span></span> <span data-ttu-id="3a54d-135">構成ファイルからこの要素が不足している場合は、.NET Framework は Internet Explorer でプロキシ設定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3a54d-135">If this element is missing from the configuration file, then the .NET Framework will use the proxy settings in Internet Explorer.</span></span>  
  
 <span data-ttu-id="3a54d-136">値、`proxyaddress`属性が整形式 Uniform Resource Indicator (URI) にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a54d-136">The value for the `proxyaddress` attribute should be a well-formed Uniform Resource Indicator (URI).</span></span>  
  
 <span data-ttu-id="3a54d-137">`scriptLocation`属性はプロキシ構成スクリプトの自動検出を参照します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-137">The `scriptLocation` attribute refers to the automatic detection of proxy configuration scripts.</span></span> <span data-ttu-id="3a54d-138"><xref:System.Net.WebProxy>クラスはときに、構成スクリプト (通常は名前付き Wpad.dat) を検出しようとしています、**自動構成スクリプトを使用して、** Internet Explorer でオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-138">The <xref:System.Net.WebProxy> class will attempt to locate a configuration script (usually named Wpad.dat) when the **Use automatic configuration script** option is selected in Internet Explorer.</span></span> <span data-ttu-id="3a54d-139">場合`bypassonlocal`任意の値に設定されている`scriptLocation`は無視されます。</span><span class="sxs-lookup"><span data-stu-id="3a54d-139">If `bypassonlocal` is set to any value, `scriptLocation` is ignored.</span></span>
  
 <span data-ttu-id="3a54d-140">使用して、`usesystemdefault`バージョン 2.0 に移行しようとする .NET Framework version 1.1 アプリケーション用の属性。</span><span class="sxs-lookup"><span data-stu-id="3a54d-140">Use the `usesystemdefault` attribute for .NET Framework version 1.1 applications that are migrating to version 2.0.</span></span>  
  
 <span data-ttu-id="3a54d-141">場合、例外がスローされます、`proxyaddress`属性が、無効な既定のプロキシを指定します。</span><span class="sxs-lookup"><span data-stu-id="3a54d-141">An exception is thrown if the `proxyaddress` attribute specifies an invalid default proxy.</span></span> <span data-ttu-id="3a54d-142">例外の <xref:System.Exception.InnerException%2A> プロパティに、このエラーの根本原因に関する詳細情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3a54d-142">The <xref:System.Exception.InnerException%2A> property on the exception should have more information about the root cause of the error.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="3a54d-143">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="3a54d-143">Configuration Files</span></span>  
 <span data-ttu-id="3a54d-144">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3a54d-144">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="3a54d-145">例</span><span class="sxs-lookup"><span data-stu-id="3a54d-145">Example</span></span>  
 <span data-ttu-id="3a54d-146">次の例は、既定値を Internet Explorer のプロキシを使用して、プロキシ アドレスを指定し、ローカル アクセスでプロキシをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="3a54d-146">The following example uses the defaults from the Internet Explorer proxy, specifies the proxy address, and bypasses the proxy for local access.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <proxy  
        usesystemdefault="true"  
        proxyaddress="http://192.168.1.10:3128"  
        bypassonlocal="true"  
      />  
    </defaultProxy>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="3a54d-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a54d-147">See Also</span></span>  
- <xref:System.Net.WebProxy?displayProperty=nameWithType>  
- [<span data-ttu-id="3a54d-148">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="3a54d-148">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
