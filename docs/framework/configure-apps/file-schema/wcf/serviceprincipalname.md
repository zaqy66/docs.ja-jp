---
title: '&lt;サービス プリンシパル名&gt;'
ms.date: 03/30/2017
ms.assetid: 3f3b85d3-20f2-4cd8-8a6a-ee18befbd165
ms.openlocfilehash: a22a905744980d0b370023e6236734a9bb0d6357
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150644"
---
# <a name="ltserviceprincipalnamegt"></a><span data-ttu-id="a536a-102">&lt;サービス プリンシパル名&gt;</span><span class="sxs-lookup"><span data-stu-id="a536a-102">&lt;servicePrincipalName&gt;</span></span>
<span data-ttu-id="a536a-103">サービスの ID をサービス プリンシパル名 (SPN) により指定します。</span><span class="sxs-lookup"><span data-stu-id="a536a-103">Specifies the identity of a service by its Service Principal Name (SPN).</span></span>  
  
 <span data-ttu-id="a536a-104">SPN を設定する方法についての詳細については、次を参照してください。[サービス Id と認証](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)します。</span><span class="sxs-lookup"><span data-stu-id="a536a-104">For more information about setting the SPN, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
 <span data-ttu-id="a536a-105">\<identity></span><span class="sxs-lookup"><span data-stu-id="a536a-105">\<identity></span></span>  
<span data-ttu-id="a536a-106">\<サービス プリンシパル名 ></span><span class="sxs-lookup"><span data-stu-id="a536a-106">\<servicePrincipalName></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a536a-107">構文</span><span class="sxs-lookup"><span data-stu-id="a536a-107">Syntax</span></span>  
  
```xml  
<servicePrincipalName value="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a536a-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a536a-108">Attributes and Elements</span></span>  
 <span data-ttu-id="a536a-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a536a-109">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a536a-110">属性</span><span class="sxs-lookup"><span data-stu-id="a536a-110">Attributes</span></span>  
  
|<span data-ttu-id="a536a-111">属性</span><span class="sxs-lookup"><span data-stu-id="a536a-111">Attribute</span></span>|<span data-ttu-id="a536a-112">説明</span><span class="sxs-lookup"><span data-stu-id="a536a-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a536a-113">value</span><span class="sxs-lookup"><span data-stu-id="a536a-113">value</span></span>|<span data-ttu-id="a536a-114">クライアントがサービスのインスタンスを一意に識別する名前です。</span><span class="sxs-lookup"><span data-stu-id="a536a-114">The name by which a client uniquely identifies an instance of a service.</span></span> <span data-ttu-id="a536a-115">フォレストの複数のコンピューターに 1 つのサービスの複数のインスタンスをインストールする場合、各インスタンスには独自の SPN が必要です。</span><span class="sxs-lookup"><span data-stu-id="a536a-115">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="a536a-116">クライアントが認証に使用できる複数の名前がある場合は、指定したサービス インスタンスに複数の SPN を設定できます。</span><span class="sxs-lookup"><span data-stu-id="a536a-116">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a536a-117">子要素</span><span class="sxs-lookup"><span data-stu-id="a536a-117">Child Elements</span></span>  
 <span data-ttu-id="a536a-118">なし。</span><span class="sxs-lookup"><span data-stu-id="a536a-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a536a-119">親要素</span><span class="sxs-lookup"><span data-stu-id="a536a-119">Parent Elements</span></span>  
  
|<span data-ttu-id="a536a-120">要素</span><span class="sxs-lookup"><span data-stu-id="a536a-120">Element</span></span>|<span data-ttu-id="a536a-121">説明</span><span class="sxs-lookup"><span data-stu-id="a536a-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a536a-122">\<identity></span><span class="sxs-lookup"><span data-stu-id="a536a-122">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="a536a-123">クライアントで認証するサービスの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="a536a-123">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a536a-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="a536a-124">Remarks</span></span>  
 <span data-ttu-id="a536a-125">この id を持つエンドポイントに接続するセキュリティで保護された Windows Communication Foundation (WCF) クライアントは、エンドポイントの SSPI 認証を実行するときに SPN を使用します。</span><span class="sxs-lookup"><span data-stu-id="a536a-125">A secure Windows Communication Foundation (WCF) client that connects to an endpoint with this identity uses the SPN when performing SSPI authentication with the endpoint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a536a-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="a536a-126">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.IdentityElement>  
 <xref:System.ServiceModel.EndpointAddress>  
 <xref:System.ServiceModel.EndpointAddress.Identity%2A>  
 <xref:System.ServiceModel.SpnEndpointIdentity>  
 [<span data-ttu-id="a536a-127">サービス ID と認証</span><span class="sxs-lookup"><span data-stu-id="a536a-127">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="a536a-128">\<identity></span><span class="sxs-lookup"><span data-stu-id="a536a-128">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
