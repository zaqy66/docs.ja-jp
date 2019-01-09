---
title: '&lt;serviceAuthenticationManager&gt;'
ms.date: 03/30/2017
ms.assetid: 5d69e64f-f325-4d55-8e2d-0fb30f222dda
ms.openlocfilehash: 3456ffa952372b014d579b5c420f7c44222fdad5
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145355"
---
# <a name="ltserviceauthenticationmanagergt"></a><span data-ttu-id="c0ee0-102">&lt;serviceAuthenticationManager&gt;</span><span class="sxs-lookup"><span data-stu-id="c0ee0-102">&lt;serviceAuthenticationManager&gt;</span></span>
<span data-ttu-id="c0ee0-103">サービス レベルで転送、メッセージ、または送信元の有効性を確立するワークフロー構成要素を提供します。</span><span class="sxs-lookup"><span data-stu-id="c0ee0-103">Provides a workflow configuration element that establishes at the service level the validity of a transmission, message, or originator.</span></span>  
  
<span data-ttu-id="c0ee0-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="c0ee0-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="c0ee0-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="c0ee0-105">\<behaviors></span></span>  
<span data-ttu-id="c0ee0-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="c0ee0-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="c0ee0-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="c0ee0-107">\<behavior></span></span>  
<span data-ttu-id="c0ee0-108">\<serviceAuthenticationManager ></span><span class="sxs-lookup"><span data-stu-id="c0ee0-108">\<serviceAuthenticationManager></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0ee0-109">構文</span><span class="sxs-lookup"><span data-stu-id="c0ee0-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <serviceAuthenticationManager serviceAuthenticationManagerType="String" />
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c0ee0-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="c0ee0-110">Attributes and Elements</span></span>  
 <span data-ttu-id="c0ee0-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="c0ee0-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c0ee0-112">属性</span><span class="sxs-lookup"><span data-stu-id="c0ee0-112">Attributes</span></span>  
  
|<span data-ttu-id="c0ee0-113">属性</span><span class="sxs-lookup"><span data-stu-id="c0ee0-113">Attribute</span></span>|<span data-ttu-id="c0ee0-114">説明</span><span class="sxs-lookup"><span data-stu-id="c0ee0-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c0ee0-115">serviceAuthenticationManagerType</span><span class="sxs-lookup"><span data-stu-id="c0ee0-115">serviceAuthenticationManagerType</span></span>|<span data-ttu-id="c0ee0-116">現在の動作の認証ポリシーの種類を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="c0ee0-116">A string that specifies the type of the authentication policy for the current behavior.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c0ee0-117">子要素</span><span class="sxs-lookup"><span data-stu-id="c0ee0-117">Child Elements</span></span>  
 <span data-ttu-id="c0ee0-118">なし。</span><span class="sxs-lookup"><span data-stu-id="c0ee0-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c0ee0-119">親要素</span><span class="sxs-lookup"><span data-stu-id="c0ee0-119">Parent Elements</span></span>  
  
|<span data-ttu-id="c0ee0-120">要素</span><span class="sxs-lookup"><span data-stu-id="c0ee0-120">Element</span></span>|<span data-ttu-id="c0ee0-121">説明</span><span class="sxs-lookup"><span data-stu-id="c0ee0-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c0ee0-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="c0ee0-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="c0ee0-123">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="c0ee0-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c0ee0-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0ee0-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceAuthenticationElement>
