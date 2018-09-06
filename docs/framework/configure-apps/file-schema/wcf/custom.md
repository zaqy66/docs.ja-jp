---
title: '&lt;custom&gt;'
ms.date: 03/30/2017
ms.assetid: a6f65a00-bd1a-4d4a-955a-fe009ec02ab8
ms.openlocfilehash: 7d558be66b8a1e46d9743c5f8bf0bb9a8b4c349e
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43776224"
---
# <a name="ltcustomgt"></a><span data-ttu-id="48506-102">&lt;custom&gt;</span><span class="sxs-lookup"><span data-stu-id="48506-102">&lt;custom&gt;</span></span>
<span data-ttu-id="48506-103">ユーザー設定のピア リゾルバー サービスの設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="48506-103">Specifies settings for a custom peer resolver service.</span></span>  
  
<span data-ttu-id="48506-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="48506-104">\<system.serviceModel></span></span>  
<span data-ttu-id="48506-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="48506-105">\<bindings></span></span>  
<span data-ttu-id="48506-106">\<netPeerBinding></span><span class="sxs-lookup"><span data-stu-id="48506-106">\<netPeerBinding></span></span>  
<span data-ttu-id="48506-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="48506-107">\<binding></span></span>  
<span data-ttu-id="48506-108">\<resolver></span><span class="sxs-lookup"><span data-stu-id="48506-108">\<resolver></span></span>  
<span data-ttu-id="48506-109">\<custom></span><span class="sxs-lookup"><span data-stu-id="48506-109">\<custom></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="48506-110">構文</span><span class="sxs-lookup"><span data-stu-id="48506-110">Syntax</span></span>  
  
```xml
<custom address="Uri" 
        resolverType="String">  
  <headers/>  
  <identity/>  
</custom>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="48506-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="48506-111">Attributes and Elements</span></span>  
 <span data-ttu-id="48506-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="48506-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="48506-113">属性</span><span class="sxs-lookup"><span data-stu-id="48506-113">Attributes</span></span>  
  
|<span data-ttu-id="48506-114">属性</span><span class="sxs-lookup"><span data-stu-id="48506-114">Attribute</span></span>|<span data-ttu-id="48506-115">説明</span><span class="sxs-lookup"><span data-stu-id="48506-115">Description</span></span>|  
|---------------|-----------------|  
|`address`|<span data-ttu-id="48506-116">カスタム ピア リゾルバー サービスをホストするピア ノードのエンドポイント アドレスを指定する URI。</span><span class="sxs-lookup"><span data-stu-id="48506-116">A URI that specifies the endpoint address of the peer node that hosts the custom peer resolver service.</span></span>|  
|`resolverType`|<span data-ttu-id="48506-117">カスタム ピア リゾルバー サービスの種類を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="48506-117">A string that specifies the type of the custom peer resolver service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="48506-118">子要素</span><span class="sxs-lookup"><span data-stu-id="48506-118">Child Elements</span></span>  
  
|<span data-ttu-id="48506-119">要素</span><span class="sxs-lookup"><span data-stu-id="48506-119">Element</span></span>|<span data-ttu-id="48506-120">説明</span><span class="sxs-lookup"><span data-stu-id="48506-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="48506-121">\<identity></span><span class="sxs-lookup"><span data-stu-id="48506-121">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="48506-122">この要素を使用して構成されたカスタム ピア リゾルバーの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="48506-122">Specifies the identity for custom peer resolvers configured with this element.</span></span> <span data-ttu-id="48506-123">この要素は <xref:System.ServiceModel.Configuration.IdentityElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="48506-123">This element is of type <xref:System.ServiceModel.Configuration.IdentityElement>.</span></span>|  
|[<span data-ttu-id="48506-124">\<headers></span><span class="sxs-lookup"><span data-stu-id="48506-124">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="48506-125">カスタム ピア リゾルバーによって処理される SOAP メッセージに使用するアドレス ヘッダーのコレクション。</span><span class="sxs-lookup"><span data-stu-id="48506-125">A collection of address header used for SOAP messages handled by the custom peer resolver.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="48506-126">親要素</span><span class="sxs-lookup"><span data-stu-id="48506-126">Parent Elements</span></span>  
  
|<span data-ttu-id="48506-127">要素</span><span class="sxs-lookup"><span data-stu-id="48506-127">Element</span></span>|<span data-ttu-id="48506-128">説明</span><span class="sxs-lookup"><span data-stu-id="48506-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="48506-129">\<resolver></span><span class="sxs-lookup"><span data-stu-id="48506-129">\<resolver></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/resolver.md)|<span data-ttu-id="48506-130">ピア メッシュ ID を解決してメッシュに参加する複数ノードを表すピア ノード アドレスのセットを取得するために使用されるピア リゾルバー。</span><span class="sxs-lookup"><span data-stu-id="48506-130">A peer resolver that is used to resolve a peer mesh ID to a set of peer node addresses that represents several nodes that participate in the mesh.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="48506-131">Remarks</span><span class="sxs-lookup"><span data-stu-id="48506-131">Remarks</span></span>  
 <span data-ttu-id="48506-132">この要素は、サービスをホストするピアのエンドポイント アドレスや特定のバインディング設定など、カスタム ピア リゾルバー サービスの基本設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="48506-132">This element defines the basic settings for a custom peer resolver service, including the endpoint address of the peer hosting the service and any specific binding settings.</span></span> <span data-ttu-id="48506-133">カスタム競合回避モジュールを作成する方法の詳細については、次を参照してください。 [PeerChannel アプリケーションへのカスタム競合回避モジュールの追加](https://msdn.microsoft.com/library/12aa3787-2962-439c-ad27-46523c8b0419)します。</span><span class="sxs-lookup"><span data-stu-id="48506-133">For more information on creating a custom resolver, see [Adding a Custom Resolver to a PeerChannel Application](https://msdn.microsoft.com/library/12aa3787-2962-439c-ad27-46523c8b0419).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48506-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="48506-134">See Also</span></span>  
 <xref:System.ServiceModel.PeerResolvers.CustomPeerResolverService>  
 <xref:System.ServiceModel.PeerResolvers.PeerCustomResolverSettings>  
 <xref:System.ServiceModel.Configuration.PeerResolverElement.Custom%2A>  
 <xref:System.ServiceModel.Configuration.PeerCustomResolverElement>  
 [<span data-ttu-id="48506-135">ピア リゾルバー</span><span class="sxs-lookup"><span data-stu-id="48506-135">Peer Resolvers</span></span>](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)  
 [<span data-ttu-id="48506-136">PeerChannel アプリケーションへのカスタム競合回避モジュールの追加</span><span class="sxs-lookup"><span data-stu-id="48506-136">Adding a Custom Resolver to a PeerChannel Application</span></span>](https://msdn.microsoft.com/library/12aa3787-2962-439c-ad27-46523c8b0419)
