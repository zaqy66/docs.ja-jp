---
title: '&lt;serviceAuthenticationManager&gt;'
ms.date: 03/30/2017
ms.assetid: 5d69e64f-f325-4d55-8e2d-0fb30f222dda
ms.openlocfilehash: fd04b10c0ac0bef4087daa1012a1b8bd3a5880e6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54493639"
---
# <a name="ltserviceauthenticationmanagergt"></a><span data-ttu-id="4a240-102">&lt;serviceAuthenticationManager&gt;</span><span class="sxs-lookup"><span data-stu-id="4a240-102">&lt;serviceAuthenticationManager&gt;</span></span>
<span data-ttu-id="4a240-103">サービス レベルで転送、メッセージ、または送信元の有効性を確立するワークフロー構成要素を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a240-103">Provides a workflow configuration element that establishes at the service level the validity of a transmission, message, or originator.</span></span>  
  
<span data-ttu-id="4a240-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="4a240-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="4a240-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="4a240-105">\<behaviors></span></span>  
<span data-ttu-id="4a240-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="4a240-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="4a240-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4a240-107">\<behavior></span></span>  
<span data-ttu-id="4a240-108">\<serviceAuthenticationManager></span><span class="sxs-lookup"><span data-stu-id="4a240-108">\<serviceAuthenticationManager></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a240-109">構文</span><span class="sxs-lookup"><span data-stu-id="4a240-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <serviceAuthenticationManager serviceAuthenticationManagerType="String" />
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4a240-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="4a240-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4a240-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="4a240-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4a240-112">属性</span><span class="sxs-lookup"><span data-stu-id="4a240-112">Attributes</span></span>  
  
|<span data-ttu-id="4a240-113">属性</span><span class="sxs-lookup"><span data-stu-id="4a240-113">Attribute</span></span>|<span data-ttu-id="4a240-114">説明</span><span class="sxs-lookup"><span data-stu-id="4a240-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4a240-115">serviceAuthenticationManagerType</span><span class="sxs-lookup"><span data-stu-id="4a240-115">serviceAuthenticationManagerType</span></span>|<span data-ttu-id="4a240-116">現在の動作の認証ポリシーの種類を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="4a240-116">A string that specifies the type of the authentication policy for the current behavior.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4a240-117">子要素</span><span class="sxs-lookup"><span data-stu-id="4a240-117">Child Elements</span></span>  
 <span data-ttu-id="4a240-118">なし。</span><span class="sxs-lookup"><span data-stu-id="4a240-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4a240-119">親要素</span><span class="sxs-lookup"><span data-stu-id="4a240-119">Parent Elements</span></span>  
  
|<span data-ttu-id="4a240-120">要素</span><span class="sxs-lookup"><span data-stu-id="4a240-120">Element</span></span>|<span data-ttu-id="4a240-121">説明</span><span class="sxs-lookup"><span data-stu-id="4a240-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4a240-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4a240-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="4a240-123">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a240-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4a240-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="4a240-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServiceAuthenticationElement>
