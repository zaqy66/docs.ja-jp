---
title: '&lt;pnrpPeerResolver&gt;'
ms.date: 03/30/2017
ms.assetid: c1b34f3b-68e5-4911-a367-de49fb61dbc6
ms.openlocfilehash: 882974ea29804c7218d4c6c21da2b9ddd7551c54
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150150"
---
# <a name="ltpnrppeerresolvergt"></a><span data-ttu-id="a20b8-102">&lt;pnrpPeerResolver&gt;</span><span class="sxs-lookup"><span data-stu-id="a20b8-102">&lt;pnrpPeerResolver&gt;</span></span>
<span data-ttu-id="a20b8-103">リゾルバーとして PNRP (Peer Name Resolution Protocol) リゾルバーを使用することを指定します。</span><span class="sxs-lookup"><span data-stu-id="a20b8-103">Specifies that the PNRP (Peer Name Resolution Protocol) resolver is to be used as a resolver.</span></span> <span data-ttu-id="a20b8-104">PNRP は既定のリゾルバーであるため、この要素は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="a20b8-104">This element is optional because PNRP is the default resolver.</span></span>  
  
 <span data-ttu-id="a20b8-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="a20b8-105">\<system.serviceModel></span></span>  
<span data-ttu-id="a20b8-106">\<bindings></span><span class="sxs-lookup"><span data-stu-id="a20b8-106">\<bindings></span></span>  
<span data-ttu-id="a20b8-107">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="a20b8-107">\<customBinding></span></span>  
<span data-ttu-id="a20b8-108">\<binding></span><span class="sxs-lookup"><span data-stu-id="a20b8-108">\<binding></span></span>  
<span data-ttu-id="a20b8-109">\<pnrpResolver ></span><span class="sxs-lookup"><span data-stu-id="a20b8-109">\<pnrpResolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a20b8-110">構文</span><span class="sxs-lookup"><span data-stu-id="a20b8-110">Syntax</span></span>  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a20b8-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a20b8-111">Attributes and Elements</span></span>  
 <span data-ttu-id="a20b8-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a20b8-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a20b8-113">属性</span><span class="sxs-lookup"><span data-stu-id="a20b8-113">Attributes</span></span>  
  
|<span data-ttu-id="a20b8-114">属性</span><span class="sxs-lookup"><span data-stu-id="a20b8-114">Attribute</span></span>|<span data-ttu-id="a20b8-115">説明</span><span class="sxs-lookup"><span data-stu-id="a20b8-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a20b8-116">resolverType</span><span class="sxs-lookup"><span data-stu-id="a20b8-116">resolverType</span></span>|<span data-ttu-id="a20b8-117">使用されるリゾルバーを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="a20b8-117">A string that specifies the resolver to be used.</span></span> <span data-ttu-id="a20b8-118">この属性は省略できます。</span><span class="sxs-lookup"><span data-stu-id="a20b8-118">This attribute is optional.</span></span> <span data-ttu-id="a20b8-119">設定されていない場合、または空の文字列に設定されている場合は、PNRP が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a20b8-119">If it is not set, or if it is set to an empty string, PNRP is used.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a20b8-120">子要素</span><span class="sxs-lookup"><span data-stu-id="a20b8-120">Child Elements</span></span>  
 <span data-ttu-id="a20b8-121">なし</span><span class="sxs-lookup"><span data-stu-id="a20b8-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a20b8-122">親要素</span><span class="sxs-lookup"><span data-stu-id="a20b8-122">Parent Elements</span></span>  
  
|<span data-ttu-id="a20b8-123">要素</span><span class="sxs-lookup"><span data-stu-id="a20b8-123">Element</span></span>|<span data-ttu-id="a20b8-124">説明</span><span class="sxs-lookup"><span data-stu-id="a20b8-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a20b8-125">\<binding></span><span class="sxs-lookup"><span data-stu-id="a20b8-125">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="a20b8-126">カスタム バインドのすべてのバインド機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="a20b8-126">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="a20b8-127">例</span><span class="sxs-lookup"><span data-stu-id="a20b8-127">Example</span></span>  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="see-also"></a><span data-ttu-id="a20b8-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a20b8-128">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PnrpPeerResolverElement>  
 <xref:System.ServiceModel.Channels.PnrpPeerResolverBindingElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="a20b8-129">バインディング</span><span class="sxs-lookup"><span data-stu-id="a20b8-129">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="a20b8-130">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="a20b8-130">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="a20b8-131">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="a20b8-131">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="a20b8-132">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="a20b8-132">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)  
 [<span data-ttu-id="a20b8-133">ピア リゾルバー</span><span class="sxs-lookup"><span data-stu-id="a20b8-133">Peer Resolvers</span></span>](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)
