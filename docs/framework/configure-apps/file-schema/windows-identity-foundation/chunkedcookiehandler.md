---
title: '&lt;chunkedCookieHandler&gt;'
ms.date: 03/30/2017
ms.assetid: 7220de45-1d14-4aec-a29e-4a2ea8ac861f
author: BrucePerlerMS
ms.openlocfilehash: f5592e0fd02d34b2882182196e0aa9425672a8fe
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2018
ms.locfileid: "48244939"
---
# <a name="ltchunkedcookiehandlergt"></a><span data-ttu-id="aa224-102">&lt;chunkedCookieHandler&gt;</span><span class="sxs-lookup"><span data-stu-id="aa224-102">&lt;chunkedCookieHandler&gt;</span></span>
<span data-ttu-id="aa224-103">構成、<xref:System.IdentityModel.Services.ChunkedCookieHandler>します。</span><span class="sxs-lookup"><span data-stu-id="aa224-103">Configures the <xref:System.IdentityModel.Services.ChunkedCookieHandler>.</span></span> <span data-ttu-id="aa224-104">この要素は存在のみ可能な場合、`mode`の属性、`<cookieHandler>`要素が"Default"または「チャンク」。</span><span class="sxs-lookup"><span data-stu-id="aa224-104">This element may only be present if the `mode` attribute of the `<cookieHandler>` element is "Default" or "Chunked".</span></span>  
  
 <span data-ttu-id="aa224-105">\<system.identityModel.services ></span><span class="sxs-lookup"><span data-stu-id="aa224-105">\<system.identityModel.services></span></span>  
<span data-ttu-id="aa224-106">\<federationConfiguration ></span><span class="sxs-lookup"><span data-stu-id="aa224-106">\<federationConfiguration></span></span>  
<span data-ttu-id="aa224-107">\<cookieHandler ></span><span class="sxs-lookup"><span data-stu-id="aa224-107">\<cookieHandler></span></span>  
<span data-ttu-id="aa224-108">\<chunkedCookieHandler ></span><span class="sxs-lookup"><span data-stu-id="aa224-108">\<chunkedCookieHandler></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aa224-109">構文</span><span class="sxs-lookup"><span data-stu-id="aa224-109">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <cookieHandler mode="Chunked||Default" >  
      <chunkedCookieHandler size=xs:int >  
      </chunkedCookieHandler>  
    </cookieHandler>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="aa224-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="aa224-110">Attributes and Elements</span></span>  
 <span data-ttu-id="aa224-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="aa224-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="aa224-112">属性</span><span class="sxs-lookup"><span data-stu-id="aa224-112">Attributes</span></span>  
  
|<span data-ttu-id="aa224-113">属性</span><span class="sxs-lookup"><span data-stu-id="aa224-113">Attribute</span></span>|<span data-ttu-id="aa224-114">説明</span><span class="sxs-lookup"><span data-stu-id="aa224-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="aa224-115">ChunkSize</span><span class="sxs-lookup"><span data-stu-id="aa224-115">chunkSize</span></span>|<span data-ttu-id="aa224-116">任意の 1 つの HTTP クッキーを HTTP cookie のデータの文字の最大サイズ。</span><span class="sxs-lookup"><span data-stu-id="aa224-116">The maximum size, in characters, of the HTTP cookie data for any one HTTP cookie.</span></span> <span data-ttu-id="aa224-117">チャンク サイズを調整する場合は注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa224-117">You must be careful when adjusting the chunk size.</span></span> <span data-ttu-id="aa224-118">Web ブラウザーでは、cookie とドメインごとに許可される数のサイズにさまざまな制限があります。</span><span class="sxs-lookup"><span data-stu-id="aa224-118">Web browsers have different limits on the size of cookies and number allowed per domain.</span></span> <span data-ttu-id="aa224-119">Netscape の元の仕様がこれらの制限を規定する例: (cookie の値だけでなく、メタデータを含む)、[cookie] ヘッダーあたり 4,096 バイトと 20 の cookie ドメインごと、300 cookie の合計します。</span><span class="sxs-lookup"><span data-stu-id="aa224-119">For example, the original Netscape specification stipulated these limits: 300 cookies total, 4096 bytes per cookie header (including metadata, not just the cookie value), and 20 cookies per domain.</span></span> <span data-ttu-id="aa224-120">既定値は 2000 です。</span><span class="sxs-lookup"><span data-stu-id="aa224-120">The default is 2000.</span></span> <span data-ttu-id="aa224-121">必須。</span><span class="sxs-lookup"><span data-stu-id="aa224-121">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="aa224-122">子要素</span><span class="sxs-lookup"><span data-stu-id="aa224-122">Child Elements</span></span>  
 <span data-ttu-id="aa224-123">なし</span><span class="sxs-lookup"><span data-stu-id="aa224-123">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="aa224-124">親要素</span><span class="sxs-lookup"><span data-stu-id="aa224-124">Parent Elements</span></span>  
  
|<span data-ttu-id="aa224-125">要素</span><span class="sxs-lookup"><span data-stu-id="aa224-125">Element</span></span>|<span data-ttu-id="aa224-126">説明</span><span class="sxs-lookup"><span data-stu-id="aa224-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="aa224-127">\<cookieHandler ></span><span class="sxs-lookup"><span data-stu-id="aa224-127">\<cookieHandler></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/cookiehandler.md)|<span data-ttu-id="aa224-128">構成、<xref:System.IdentityModel.Services.CookieHandler>を<xref:System.IdentityModel.Services.SessionAuthenticationModule>(SAM) を使用して cookie を読み書きします。</span><span class="sxs-lookup"><span data-stu-id="aa224-128">Configures the <xref:System.IdentityModel.Services.CookieHandler> that the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) uses to read and write cookies.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="aa224-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="aa224-129">Remarks</span></span>  
 <span data-ttu-id="aa224-130">指定した場合、<xref:System.IdentityModel.Services.ChunkedCookieHandler>を設定して、`mode`の属性、`<cookieHandler>`を"Default"または"Chunked"要素を含めることで cookie を読み書きするクッキー ハンドラーを使用するチャンクのサイズを指定できます、`<chunkedCookieHandler>`子要素と設定の`chunkSize`属性。</span><span class="sxs-lookup"><span data-stu-id="aa224-130">When you specify a <xref:System.IdentityModel.Services.ChunkedCookieHandler> by setting the `mode` attribute of the `<cookieHandler>` element to "Default" or "Chunked", you can specify the chunk size that the cookie handler uses to read and write cookies by including a `<chunkedCookieHandler>` child element and setting its `chunkSize` attribute.</span></span> <span data-ttu-id="aa224-131">場合、`<chunkedCookieHandler>`要素が存在しない、2000 バイトの既定のチャンク サイズが使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa224-131">If the `<chunkedCookieHandler>` element is not present, the default chunk size of 2000 bytes is used.</span></span> <span data-ttu-id="aa224-132">この要素にすることはできないときに指定された、`mode`属性が"Custom"に設定します。</span><span class="sxs-lookup"><span data-stu-id="aa224-132">This element cannot be specified when the `mode` attribute is set to "Custom".</span></span>  
  
 <span data-ttu-id="aa224-133">`<chunkedCookieHandler>`要素が表される、<xref:System.IdentityModel.Services.ChunkedCookieHandlerElement>クラス。</span><span class="sxs-lookup"><span data-stu-id="aa224-133">The `<chunkedCookieHandler>` element is represented by the <xref:System.IdentityModel.Services.ChunkedCookieHandlerElement> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="aa224-134">例</span><span class="sxs-lookup"><span data-stu-id="aa224-134">Example</span></span>  
 <span data-ttu-id="aa224-135">次の例では、3000 バイトのチャンク単位で cookie を書き込むチャンクされたクッキー ハンドラーを構成します。</span><span class="sxs-lookup"><span data-stu-id="aa224-135">The following example configures a chunked cookie handler that writes cookies in chunks of 3000 bytes.</span></span>  
  
```xml  
<cookieHandler mode="Chunked">  
    <chunkedCookieHandler chunkSize=3000/>  
</cookieHandler>  
```  
  
## <a name="see-also"></a><span data-ttu-id="aa224-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa224-136">See Also</span></span>  
 <xref:System.IdentityModel.Services.ChunkedCookieHandler>
