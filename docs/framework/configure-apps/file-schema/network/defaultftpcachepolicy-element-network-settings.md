---
title: '&lt;defaultFtpCachePolicy&gt;要素 (ネットワーク設定)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#defaultFtpCachePolicy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/requestCaching/defaultFtpCachePolicy
helpviewer_keywords:
- <defaultFtpCachePolicy> element
- defaultFtpCachePolicy element
ms.assetid: 0eb0c5cb-dd97-484d-8614-785e88877abb
ms.openlocfilehash: a8c71551adc2b88b5300994134eaec329a083709
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188288"
---
# <a name="ltdefaultftpcachepolicygt-element-network-settings"></a><span data-ttu-id="a8e7c-102">&lt;defaultFtpCachePolicy&gt;要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="a8e7c-102">&lt;defaultFtpCachePolicy&gt; Element (Network Settings)</span></span>
<span data-ttu-id="a8e7c-103">FTP キャッシュがアクティブでかどうかし、既定のキャッシュ ポリシーを記述について説明します。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-103">Describes whether FTP caching is active and describes the default caching policy.</span></span>  
  
 <span data-ttu-id="a8e7c-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="a8e7c-104">\<configuration></span></span>  
<span data-ttu-id="a8e7c-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="a8e7c-105">\<system.net></span></span>  
<span data-ttu-id="a8e7c-106">\<requestCaching ></span><span class="sxs-lookup"><span data-stu-id="a8e7c-106">\<requestCaching></span></span>  
<span data-ttu-id="a8e7c-107">\<defaultFtpCachePolicy ></span><span class="sxs-lookup"><span data-stu-id="a8e7c-107">\<defaultFtpCachePolicy></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8e7c-108">構文</span><span class="sxs-lookup"><span data-stu-id="a8e7c-108">Syntax</span></span>  
  
```xml  
<defaultFtpCachePolicy  
  policyLevel="BypassCache|Default|CacheOnly|CacheIfAvailable|Revalidate|Reload|NoCacheNoStore|Revalidate"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a8e7c-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a8e7c-109">Attributes and Elements</span></span>  
 <span data-ttu-id="a8e7c-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a8e7c-111">属性</span><span class="sxs-lookup"><span data-stu-id="a8e7c-111">Attributes</span></span>  
  
|<span data-ttu-id="a8e7c-112">属性</span><span class="sxs-lookup"><span data-stu-id="a8e7c-112">Attribute</span></span>|<span data-ttu-id="a8e7c-113">説明</span><span class="sxs-lookup"><span data-stu-id="a8e7c-113">Description</span></span>|  
|---------------|-----------------|  
|`policyLevel`|<span data-ttu-id="a8e7c-114">FTP キャッシュ ポリシーを指定します。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-114">Specifies the FTP caching policy.</span></span> <span data-ttu-id="a8e7c-115">既定値は `Default` です。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-115">The default value is `Default`.</span></span>|  
  
## <a name="policylevel-attribute"></a><span data-ttu-id="a8e7c-116">policyLevel 属性</span><span class="sxs-lookup"><span data-stu-id="a8e7c-116">policyLevel Attribute</span></span>  
  
|<span data-ttu-id="a8e7c-117">[値]</span><span class="sxs-lookup"><span data-stu-id="a8e7c-117">Value</span></span>|<span data-ttu-id="a8e7c-118">説明</span><span class="sxs-lookup"><span data-stu-id="a8e7c-118">Description</span></span>|  
|-----------|-----------------|  
|`Default`|<span data-ttu-id="a8e7c-119">リソースに新しいもコンテンツの長さは正確では、有効期限、変更、およびコンテンツの長さの属性が存在する場合は、キャッシュされたリソースを返します。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-119">Returns the cached resource if the resource is fresh, the content length is accurate, and the expiration, modification, and content length attributes are present.</span></span>|  
|`BypassCache`|<span data-ttu-id="a8e7c-120">サーバーからリソースを返します。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-120">Returns the resource from the server.</span></span>|  
|`CacheOnly`|<span data-ttu-id="a8e7c-121">コンテンツの長さが存在し、エントリのサイズと一致する場合は、キャッシュされたリソースを返します。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-121">Returns the cached resource if the content length is present and matches the entry size.</span></span>|  
|`CacheIfAvailable`|<span data-ttu-id="a8e7c-122">コンテンツの長さが指定されたエントリのサイズと一致する場合、キャッシュされたリソースを返しますそれ以外の場合、リソースはサーバーからダウンロードされ、呼び出し元に返されます。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-122">Returns the cached resource if the content length is provided and matches the entry size; otherwise, the resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="a8e7c-123">キャッシュされたリソースのタイムスタンプが、サーバー上のリソースのタイムスタンプと同じである場合、キャッシュされたリソースを返しますそれ以外の場合、リソースに、サーバーからダウンロード、キャッシュに格納されている、呼び出し元に返されます。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-123">Returns the cached resource if the timestamp of the cached resource is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, stored in the cache, and returned to the caller.</span></span>|  
|`Reload`|<span data-ttu-id="a8e7c-124">サーバーからリソースをダウンロード、キャッシュに格納およびリソースを呼び出し元に返します。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-124">Downloads the resource from the server, stores it in the cache, and returns the resource to the caller.</span></span>|  
|`NoCacheNoStore`|<span data-ttu-id="a8e7c-125">キャッシュされたリソースが存在する場合は削除されます。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-125">If a cached resource exists, it is deleted.</span></span> <span data-ttu-id="a8e7c-126">リソースは、サーバーからがダウンロードされ、呼び出し元に返されます。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-126">The resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="a8e7c-127">タイムスタンプが、サーバー上のリソースのタイムスタンプと同じである場合は、リソースのキャッシュされたコピーを使用して、要求に応じます。それ以外の場合、リソースにサーバーからダウンロード、呼び出し元に表示される、キャッシュに格納します。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-127">Satisfies a request by using the cached copy of the resource if the timestamp is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, presented to the caller, and stored in the cache.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a8e7c-128">子要素</span><span class="sxs-lookup"><span data-stu-id="a8e7c-128">Child Elements</span></span>  
 <span data-ttu-id="a8e7c-129">なし。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-129">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a8e7c-130">親要素</span><span class="sxs-lookup"><span data-stu-id="a8e7c-130">Parent Elements</span></span>  
  
|<span data-ttu-id="a8e7c-131">要素</span><span class="sxs-lookup"><span data-stu-id="a8e7c-131">Element</span></span>|<span data-ttu-id="a8e7c-132">説明</span><span class="sxs-lookup"><span data-stu-id="a8e7c-132">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a8e7c-133">requestCaching</span><span class="sxs-lookup"><span data-stu-id="a8e7c-133">requestCaching</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/requestcaching-element-network-settings.md)|<span data-ttu-id="a8e7c-134">ネットワーク要求のキャッシュ メカニズムを制御します。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-134">Controls the caching mechanism for network requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a8e7c-135">Remarks</span><span class="sxs-lookup"><span data-stu-id="a8e7c-135">Remarks</span></span>  
  
## <a name="example"></a><span data-ttu-id="a8e7c-136">例</span><span class="sxs-lookup"><span data-stu-id="a8e7c-136">Example</span></span>  
 <span data-ttu-id="a8e7c-137">次の例は、FTP キャッシュのポリシーを指定する方法を示します`NoCacheNoStore`します。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-137">The following example shows how to specify an FTP caching policy of `NoCacheNoStore`.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <requestCaching>  
      <defaultFtpCachePolicy  
        policyLevel="NoCacheNoStore">  
      </defaultFtpCachePolicy>  
    </requestCaching>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a8e7c-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8e7c-138">See Also</span></span>  
- <xref:System.Net.Cache>  
- <xref:System.Net.WebRequest>  
- <xref:System.Net.Cache.RequestCacheLevel>  
- [<span data-ttu-id="a8e7c-139">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="a8e7c-139">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
