---
title: '&lt;resolver&gt;'
ms.date: 03/30/2017
ms.assetid: 0c00200c-f135-4e5c-a024-76b72bcbc021
ms.openlocfilehash: 48b6b6ca315f7ab63a8f7a64b97167fa04fe1e4e
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43804095"
---
# <a name="ltresolvergt"></a><span data-ttu-id="0edf0-102">&lt;resolver&gt;</span><span class="sxs-lookup"><span data-stu-id="0edf0-102">&lt;resolver&gt;</span></span>
<span data-ttu-id="0edf0-103">ピア メッシュ ID を解決してメッシュに参加する複数ノードを表すピア アドレス セットを取得するためにピア リゾルバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="0edf0-103">Specifies a peer resolver that is used to resolve a peer mesh ID to a set of peer node addresses that represents several nodes that participate in the mesh.</span></span>  
  
 <span data-ttu-id="0edf0-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="0edf0-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="0edf0-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="0edf0-105">\<bindings></span></span>  
<span data-ttu-id="0edf0-106">\<netPeerBinding></span><span class="sxs-lookup"><span data-stu-id="0edf0-106">\<netPeerBinding></span></span>  
<span data-ttu-id="0edf0-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="0edf0-107">\<binding></span></span>  
<span data-ttu-id="0edf0-108">\<resolver></span><span class="sxs-lookup"><span data-stu-id="0edf0-108">\<resolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0edf0-109">構文</span><span class="sxs-lookup"><span data-stu-id="0edf0-109">Syntax</span></span>  
  
```xml  
<resolver mode="Auto/Custom/Pnrp"  
   referralPolicy="DoNotShare/Service/Share">  
</resolver>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0edf0-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="0edf0-110">Attributes and Elements</span></span>  
 <span data-ttu-id="0edf0-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="0edf0-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0edf0-112">属性</span><span class="sxs-lookup"><span data-stu-id="0edf0-112">Attributes</span></span>  
  
|<span data-ttu-id="0edf0-113">属性</span><span class="sxs-lookup"><span data-stu-id="0edf0-113">Attribute</span></span>|<span data-ttu-id="0edf0-114">説明</span><span class="sxs-lookup"><span data-stu-id="0edf0-114">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="0edf0-115">このサービスに関連付けられるピア リゾルバー インスタンスが PNRP 固有、カスタム リゾルバー、自動的に決定されるのいずれであるかを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="0edf0-115">A string that specifies whether the peer resolver instance associated with this service is either PNRP-specific, a custom resolver, or automatically determined.</span></span> <span data-ttu-id="0edf0-116">この属性は <xref:System.ServiceModel.PeerResolvers.PeerResolverMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="0edf0-116">This attribute is of type <xref:System.ServiceModel.PeerResolvers.PeerResolverMode>.</span></span>|  
|`referralPolicy`|<span data-ttu-id="0edf0-117">ピア間で参照を共有する方法を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="0edf0-117">A string that specifies the way referrals are shared among peers.</span></span> <span data-ttu-id="0edf0-118">この属性は <xref:System.ServiceModel.PeerResolvers.PeerReferralPolicy> 型です。</span><span class="sxs-lookup"><span data-stu-id="0edf0-118">This attribute is of type <xref:System.ServiceModel.PeerResolvers.PeerReferralPolicy>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0edf0-119">子要素</span><span class="sxs-lookup"><span data-stu-id="0edf0-119">Child Elements</span></span>  
  
|<span data-ttu-id="0edf0-120">要素</span><span class="sxs-lookup"><span data-stu-id="0edf0-120">Element</span></span>|<span data-ttu-id="0edf0-121">説明</span><span class="sxs-lookup"><span data-stu-id="0edf0-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0edf0-122">\<headers></span><span class="sxs-lookup"><span data-stu-id="0edf0-122">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers.md)|<span data-ttu-id="0edf0-123">ユーザー設定のピア リゾルバー サービスの設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="0edf0-123">Specifies settings for a custom peer resolver service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0edf0-124">親要素</span><span class="sxs-lookup"><span data-stu-id="0edf0-124">Parent Elements</span></span>  
  
|<span data-ttu-id="0edf0-125">要素</span><span class="sxs-lookup"><span data-stu-id="0edf0-125">Element</span></span>|<span data-ttu-id="0edf0-126">説明</span><span class="sxs-lookup"><span data-stu-id="0edf0-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0edf0-127">\<binding></span><span class="sxs-lookup"><span data-stu-id="0edf0-127">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="0edf0-128">すべてのバインド機能を定義、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="0edf0-128">Defines all binding capabilities of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0edf0-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="0edf0-129">Remarks</span></span>  
 <span data-ttu-id="0edf0-130">ピア名リゾルバーは、ピア メッシュに参加するピア ノードを検索するためにピア チャネルにより使用される探索サービスです。</span><span class="sxs-lookup"><span data-stu-id="0edf0-130">A peer name resolver is a discovery service used by peer channels to find peer nodes that participate in a peer mesh.</span></span> <span data-ttu-id="0edf0-131">またピア名リゾルバーは、ノードをピア メッシュに登録するために使用されます。ピア メッシュは、ピア メッシュからピア ノードを認識し、使用可能にするための機構です。</span><span class="sxs-lookup"><span data-stu-id="0edf0-131">It is also used to "register" a node with a peer mesh, the mechanism by which the peer node becomes known and available from the peer mesh.</span></span> <span data-ttu-id="0edf0-132">ピア リゾルバーの詳細については、次を参照してください。[ピア リゾルバー](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)します。</span><span class="sxs-lookup"><span data-stu-id="0edf0-132">For more information on peer resolvers, see [Peer Resolvers](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0edf0-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="0edf0-133">See Also</span></span>  
 <xref:System.ServiceModel.PeerResolver>  
 <xref:System.ServiceModel.PeerResolvers.PeerResolverSettings>  
 <xref:System.ServiceModel.NetPeerTcpBinding.Resolver%2A>  
 <xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement.Resolver%2A>  
 <xref:System.ServiceModel.Configuration.PeerResolverElement>  
 [<span data-ttu-id="0edf0-134">ピア リゾルバー</span><span class="sxs-lookup"><span data-stu-id="0edf0-134">Peer Resolvers</span></span>](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)  
 [<span data-ttu-id="0edf0-135">PeerChannel アプリケーションへのカスタム競合回避モジュールの追加</span><span class="sxs-lookup"><span data-stu-id="0edf0-135">Adding a Custom Resolver to a PeerChannel Application</span></span>](https://msdn.microsoft.com/library/12aa3787-2962-439c-ad27-46523c8b0419)
