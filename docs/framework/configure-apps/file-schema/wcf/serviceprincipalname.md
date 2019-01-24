---
title: '&lt;servicePrincipalName&gt;'
ms.date: 03/30/2017
ms.assetid: 3f3b85d3-20f2-4cd8-8a6a-ee18befbd165
ms.openlocfilehash: 5d65b5956491e30066ece54a48374f1d7014552e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54657592"
---
# <a name="ltserviceprincipalnamegt"></a><span data-ttu-id="89ac3-102">&lt;servicePrincipalName&gt;</span><span class="sxs-lookup"><span data-stu-id="89ac3-102">&lt;servicePrincipalName&gt;</span></span>
<span data-ttu-id="89ac3-103">サービスの ID をサービス プリンシパル名 (SPN) により指定します。</span><span class="sxs-lookup"><span data-stu-id="89ac3-103">Specifies the identity of a service by its Service Principal Name (SPN).</span></span>  
  
 <span data-ttu-id="89ac3-104">SPN を設定する方法についての詳細については、次を参照してください。[サービス Id と認証](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)します。</span><span class="sxs-lookup"><span data-stu-id="89ac3-104">For more information about setting the SPN, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
 <span data-ttu-id="89ac3-105">\<identity></span><span class="sxs-lookup"><span data-stu-id="89ac3-105">\<identity></span></span>  
<span data-ttu-id="89ac3-106">\<servicePrincipalName></span><span class="sxs-lookup"><span data-stu-id="89ac3-106">\<servicePrincipalName></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="89ac3-107">構文</span><span class="sxs-lookup"><span data-stu-id="89ac3-107">Syntax</span></span>  
  
```xml  
<servicePrincipalName value="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="89ac3-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="89ac3-108">Attributes and Elements</span></span>  
 <span data-ttu-id="89ac3-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="89ac3-109">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="89ac3-110">属性</span><span class="sxs-lookup"><span data-stu-id="89ac3-110">Attributes</span></span>  
  
|<span data-ttu-id="89ac3-111">属性</span><span class="sxs-lookup"><span data-stu-id="89ac3-111">Attribute</span></span>|<span data-ttu-id="89ac3-112">説明</span><span class="sxs-lookup"><span data-stu-id="89ac3-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="89ac3-113">value</span><span class="sxs-lookup"><span data-stu-id="89ac3-113">value</span></span>|<span data-ttu-id="89ac3-114">クライアントがサービスのインスタンスを一意に識別する名前です。</span><span class="sxs-lookup"><span data-stu-id="89ac3-114">The name by which a client uniquely identifies an instance of a service.</span></span> <span data-ttu-id="89ac3-115">フォレストの複数のコンピューターに 1 つのサービスの複数のインスタンスをインストールする場合、各インスタンスには独自の SPN が必要です。</span><span class="sxs-lookup"><span data-stu-id="89ac3-115">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="89ac3-116">クライアントが認証に使用できる複数の名前がある場合は、指定したサービス インスタンスに複数の SPN を設定できます。</span><span class="sxs-lookup"><span data-stu-id="89ac3-116">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="89ac3-117">子要素</span><span class="sxs-lookup"><span data-stu-id="89ac3-117">Child Elements</span></span>  
 <span data-ttu-id="89ac3-118">なし。</span><span class="sxs-lookup"><span data-stu-id="89ac3-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="89ac3-119">親要素</span><span class="sxs-lookup"><span data-stu-id="89ac3-119">Parent Elements</span></span>  
  
|<span data-ttu-id="89ac3-120">要素</span><span class="sxs-lookup"><span data-stu-id="89ac3-120">Element</span></span>|<span data-ttu-id="89ac3-121">説明</span><span class="sxs-lookup"><span data-stu-id="89ac3-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="89ac3-122">\<identity></span><span class="sxs-lookup"><span data-stu-id="89ac3-122">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="89ac3-123">クライアントで認証するサービスの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="89ac3-123">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="89ac3-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="89ac3-124">Remarks</span></span>  
 <span data-ttu-id="89ac3-125">この id を持つエンドポイントに接続するセキュリティで保護された Windows Communication Foundation (WCF) クライアントは、エンドポイントの SSPI 認証を実行するときに SPN を使用します。</span><span class="sxs-lookup"><span data-stu-id="89ac3-125">A secure Windows Communication Foundation (WCF) client that connects to an endpoint with this identity uses the SPN when performing SSPI authentication with the endpoint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="89ac3-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="89ac3-126">See also</span></span>
- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- <xref:System.ServiceModel.SpnEndpointIdentity>
- [<span data-ttu-id="89ac3-127">サービス ID と認証</span><span class="sxs-lookup"><span data-stu-id="89ac3-127">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="89ac3-128">\<identity></span><span class="sxs-lookup"><span data-stu-id="89ac3-128">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
