---
title: '&lt;dns&gt;'
ms.date: 03/30/2017
ms.assetid: 81819dae-4825-43b7-bccd-f16d2d3d2f06
ms.openlocfilehash: 68cbb25b79bbda301c29d72800a125c7a6ba0b6f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54616460"
---
# <a name="ltdnsgt"></a><span data-ttu-id="b4097-102">&lt;dns&gt;</span><span class="sxs-lookup"><span data-stu-id="b4097-102">&lt;dns&gt;</span></span>
<span data-ttu-id="b4097-103">予想されるサーバーの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4097-103">Specifies the expected identity of the server.</span></span> <span data-ttu-id="b4097-104">この ID は、同じ値を持つ DNS がサーバーの証明書に含まれていれば、X509 証明書の認証モードで有効です。</span><span class="sxs-lookup"><span data-stu-id="b4097-104">This identity is valid for X509 Certificate authentication mode if the server’s certificate contains a DNS with the same value.</span></span> <span data-ttu-id="b4097-105">さらに、SPN に同じ値があれば、Windows 認証モードでも有効です。</span><span class="sxs-lookup"><span data-stu-id="b4097-105">It is also valid for Windows authentication mode if the SPN has the same value.</span></span>  
  
 <span data-ttu-id="b4097-106">要素の値を設定する方法についての詳細については、次を参照してください。[サービス Id と認証](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)します。</span><span class="sxs-lookup"><span data-stu-id="b4097-106">For more information about setting the element value, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
 <span data-ttu-id="b4097-107">\<identity></span><span class="sxs-lookup"><span data-stu-id="b4097-107">\<identity></span></span>  
<span data-ttu-id="b4097-108">\<dns></span><span class="sxs-lookup"><span data-stu-id="b4097-108">\<dns></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b4097-109">構文</span><span class="sxs-lookup"><span data-stu-id="b4097-109">Syntax</span></span>  
  
```xml  
<dns value = "String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b4097-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="b4097-110">Attributes and Elements</span></span>  
 <span data-ttu-id="b4097-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="b4097-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b4097-112">属性</span><span class="sxs-lookup"><span data-stu-id="b4097-112">Attributes</span></span>  
  
|<span data-ttu-id="b4097-113">属性</span><span class="sxs-lookup"><span data-stu-id="b4097-113">Attribute</span></span>|<span data-ttu-id="b4097-114">説明</span><span class="sxs-lookup"><span data-stu-id="b4097-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b4097-115">value</span><span class="sxs-lookup"><span data-stu-id="b4097-115">value</span></span>|<span data-ttu-id="b4097-116">証明書の DNS です。</span><span class="sxs-lookup"><span data-stu-id="b4097-116">The DNS of the certificate.</span></span> <span data-ttu-id="b4097-117">DNS は、IP ベースのネットワーク上でコンピューターを特定するために使用される業界標準のプロトコルです。</span><span class="sxs-lookup"><span data-stu-id="b4097-117">DNS is an industry-standard protocol used to locate computers on an IP-based network.</span></span> <span data-ttu-id="b4097-118">ユーザーなど、表示名が覚え[ https://go.microsoft.com/fwlink/?prd=10929 ](https://go.microsoft.com/fwlink/?prd=10929)または[ https://go.microsoft.com/fwlink/?LinkID=96165 ](https://go.microsoft.com/fwlink/?LinkID=96165)、207.46.131.137 など、数値ベースのアドレスよりも簡単です。</span><span class="sxs-lookup"><span data-stu-id="b4097-118">Users can remember display names, such as [https://go.microsoft.com/fwlink/?prd=10929](https://go.microsoft.com/fwlink/?prd=10929) or [https://go.microsoft.com/fwlink/?LinkID=96165](https://go.microsoft.com/fwlink/?LinkID=96165), easier than number-based addresses, such as 207.46.131.137.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b4097-119">子要素</span><span class="sxs-lookup"><span data-stu-id="b4097-119">Child Elements</span></span>  
 <span data-ttu-id="b4097-120">なし。</span><span class="sxs-lookup"><span data-stu-id="b4097-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b4097-121">親要素</span><span class="sxs-lookup"><span data-stu-id="b4097-121">Parent Elements</span></span>  
  
|<span data-ttu-id="b4097-122">要素</span><span class="sxs-lookup"><span data-stu-id="b4097-122">Element</span></span>|<span data-ttu-id="b4097-123">説明</span><span class="sxs-lookup"><span data-stu-id="b4097-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b4097-124">\<identity></span><span class="sxs-lookup"><span data-stu-id="b4097-124">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="b4097-125">クライアントで認証するサービスの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4097-125">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="b4097-126">例</span><span class="sxs-lookup"><span data-stu-id="b4097-126">Example</span></span>  
 <span data-ttu-id="b4097-127">次の構成コードは、サーバーの認証に使用される X.509 証明書の DNS を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4097-127">The following configuration code specifies the DNS of an X.509 certificate that is used to authenticate a server.</span></span>  
  
```xml  
<identity>
  <dns value = "www.cohowinery.com" />
</identity>
```  
  
## <a name="see-also"></a><span data-ttu-id="b4097-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4097-128">See also</span></span>
- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- <xref:System.ServiceModel.DnsEndpointIdentity>
- [<span data-ttu-id="b4097-129">サービス ID と認証</span><span class="sxs-lookup"><span data-stu-id="b4097-129">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="b4097-130">\<identity></span><span class="sxs-lookup"><span data-stu-id="b4097-130">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
