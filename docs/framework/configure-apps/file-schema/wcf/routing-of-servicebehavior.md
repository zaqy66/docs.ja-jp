---
title: <routing> の <serviceBehavior>
ms.date: 03/30/2017
ms.assetid: d8f9c844-4629-4a45-9599-856dc8f01794
ms.openlocfilehash: 3f23cbb45aa72b1aae18c845e68b426a4214d499
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261777"
---
# <a name="routing-of-servicebehavior"></a><span data-ttu-id="353e2-102">\<ルーティング > の\<serviceBehavior ></span><span class="sxs-lookup"><span data-stu-id="353e2-102">\<routing> of \<serviceBehavior></span></span>
<span data-ttu-id="353e2-103">ルーティング構成の動的な変更を可能にするルーティング サービスへの実行時アクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="353e2-103">Provides run-time access to the routing service to allow dynamic modification of the routing configuration.</span></span>  
  
 <span data-ttu-id="353e2-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="353e2-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="353e2-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="353e2-105">\<behaviors></span></span>  
<span data-ttu-id="353e2-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="353e2-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="353e2-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="353e2-107">\<behavior></span></span>  
<span data-ttu-id="353e2-108">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="353e2-108">\<routing></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="353e2-109">構文</span><span class="sxs-lookup"><span data-stu-id="353e2-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <routing filterTable="String"
               routeOnHeadersOnly="Boolean"
               SoapProcessingEnabled="Boolean" />
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="353e2-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="353e2-110">Attributes and Elements</span></span>  
 <span data-ttu-id="353e2-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="353e2-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="353e2-112">属性</span><span class="sxs-lookup"><span data-stu-id="353e2-112">Attributes</span></span>  
  
|<span data-ttu-id="353e2-113">属性</span><span class="sxs-lookup"><span data-stu-id="353e2-113">Attribute</span></span>|<span data-ttu-id="353e2-114">説明</span><span class="sxs-lookup"><span data-stu-id="353e2-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="353e2-115">filterTable</span><span class="sxs-lookup"><span data-stu-id="353e2-115">filterTable</span></span>|<span data-ttu-id="353e2-116">ルーティング サービスによって評価されるフィルターを含むルーティング テーブルの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="353e2-116">A string that specifies the name of the routing table that contains filters to be evaluated by the routing service.</span></span> <span data-ttu-id="353e2-117">この値に一致する必要があります、`name`の属性を[ \<filterTable >](../../../../../docs/framework/configure-apps/file-schema/wcf/filtertable.md)内の要素、 [ \<filterTables >](../../../../../docs/framework/configure-apps/file-schema/wcf/filtertables.md)セクション。</span><span class="sxs-lookup"><span data-stu-id="353e2-117">This value must match the `name` attribute of a [\<filterTable>](../../../../../docs/framework/configure-apps/file-schema/wcf/filtertable.md) element in the [\<filterTables>](../../../../../docs/framework/configure-apps/file-schema/wcf/filtertables.md) section.</span></span>|  
|<span data-ttu-id="353e2-118">routeOnHeaderOnly</span><span class="sxs-lookup"><span data-stu-id="353e2-118">routeOnHeaderOnly</span></span>|<span data-ttu-id="353e2-119">フィルターがメッセージの本文とヘッダーの両方を調べるか、ヘッダーのみを調べるかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="353e2-119">A Boolean value that specifies whether the filter will examine both the message body and the header, or the header only.</span></span> <span data-ttu-id="353e2-120">既定値は `true` です。</span><span class="sxs-lookup"><span data-stu-id="353e2-120">The default is `true`.</span></span>|  
|<span data-ttu-id="353e2-121">soapProcessingEnabled</span><span class="sxs-lookup"><span data-stu-id="353e2-121">soapProcessingEnabled</span></span>|<span data-ttu-id="353e2-122">SOAP 処理を実行するかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="353e2-122">A Boolean value that specifies whether SOAP processing should occur.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="353e2-123">子要素</span><span class="sxs-lookup"><span data-stu-id="353e2-123">Child Elements</span></span>  
 <span data-ttu-id="353e2-124">なし。</span><span class="sxs-lookup"><span data-stu-id="353e2-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="353e2-125">親要素</span><span class="sxs-lookup"><span data-stu-id="353e2-125">Parent Elements</span></span>  
  
|<span data-ttu-id="353e2-126">要素</span><span class="sxs-lookup"><span data-stu-id="353e2-126">Element</span></span>|<span data-ttu-id="353e2-127">説明</span><span class="sxs-lookup"><span data-stu-id="353e2-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="353e2-128">\<behavior></span><span class="sxs-lookup"><span data-stu-id="353e2-128">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="353e2-129">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="353e2-129">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="353e2-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="353e2-130">Remarks</span></span>  
 <span data-ttu-id="353e2-131">サービスの動作構成に追加すると、この構成要素により、サービスのルーティングが有効になります。</span><span class="sxs-lookup"><span data-stu-id="353e2-131">When added to the service’s behavior configuration, this configuration element enables routing for the service.</span></span> <span data-ttu-id="353e2-132">この要素には、サービスで使用される実際のルーティング テーブルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="353e2-132">You can specify the actual routing table to be used by the service in this element.</span></span>  
  
 <span data-ttu-id="353e2-133">この構成セクションを使用すると、配置パターンの変更時にルーティング設定を変更できます。</span><span class="sxs-lookup"><span data-stu-id="353e2-133">Using this configuration section, you can change your routing settings on the fly when your deployment pattern changes.</span></span> <span data-ttu-id="353e2-134">実行時には、新しいルーティング設定を使用した独自のルーティング拡張を登録できます。ルーティング サービスは (開始時に適用されていた規則に関係なく) 更新済みの構成情報を使用して新たなメッセージとセッションにサービスを提供します。ただし、インフライトのメッセージやセッションには以前の規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="353e2-134">At runtime, you can register your own routing extension with new routing settings and the routing service will begin using the updated configuration information for new messages and sessions, while leaving in-flight messages/sessions using whatever rules were in place when they started.</span></span>  <span data-ttu-id="353e2-135">このようにして、実行時において、セッション セーフでリサイクルの程度を抑えた状態でのルーティング サービスの再構成が可能となります。</span><span class="sxs-lookup"><span data-stu-id="353e2-135">This gives you the ability to do session-safe, recycle-less reconfiguration of the Routing Service during runtime.</span></span>  
  
