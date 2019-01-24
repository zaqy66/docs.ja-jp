---
title: '&lt;clientVia&gt;'
ms.date: 03/30/2017
ms.assetid: c27ee94e-babd-459b-9574-2a6d67d11314
ms.openlocfilehash: 6491411d8cfe5c7a5a944f3b1cd728c9f0a4b852
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54641214"
---
# <a name="ltclientviagt"></a><span data-ttu-id="23cb7-102">&lt;clientVia&gt;</span><span class="sxs-lookup"><span data-stu-id="23cb7-102">&lt;clientVia&gt;</span></span>
<span data-ttu-id="23cb7-103">トランスポート チャネルの作成対象となる URI を指定します。</span><span class="sxs-lookup"><span data-stu-id="23cb7-103">Specifies the URI for which the transport channel should be created.</span></span> <span data-ttu-id="23cb7-104">詳細については、「 <xref:System.ServiceModel.Description.ClientViaBehavior> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23cb7-104">For more information, see <xref:System.ServiceModel.Description.ClientViaBehavior>.</span></span>  
  
 <span data-ttu-id="23cb7-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="23cb7-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="23cb7-106">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="23cb7-106">\<behaviors></span></span>  
<span data-ttu-id="23cb7-107">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="23cb7-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="23cb7-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="23cb7-108">\<behavior></span></span>  
<span data-ttu-id="23cb7-109">\<clientVia></span><span class="sxs-lookup"><span data-stu-id="23cb7-109">\<clientVia></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="23cb7-110">構文</span><span class="sxs-lookup"><span data-stu-id="23cb7-110">Syntax</span></span>  
  
```xml  
<clientVia viaUri="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="23cb7-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="23cb7-111">Attributes and Elements</span></span>  
 <span data-ttu-id="23cb7-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="23cb7-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="23cb7-113">属性</span><span class="sxs-lookup"><span data-stu-id="23cb7-113">Attributes</span></span>  
  
|<span data-ttu-id="23cb7-114">属性</span><span class="sxs-lookup"><span data-stu-id="23cb7-114">Attribute</span></span>|<span data-ttu-id="23cb7-115">説明</span><span class="sxs-lookup"><span data-stu-id="23cb7-115">Description</span></span>|  
|---------------|-----------------|  
|`viaUri`|<span data-ttu-id="23cb7-116">メッセージの経路を示す URI を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="23cb7-116">A string that specifies a URI that indicates the route a message should take.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="23cb7-117">子要素</span><span class="sxs-lookup"><span data-stu-id="23cb7-117">Child Elements</span></span>  
 <span data-ttu-id="23cb7-118">なし</span><span class="sxs-lookup"><span data-stu-id="23cb7-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="23cb7-119">親要素</span><span class="sxs-lookup"><span data-stu-id="23cb7-119">Parent Elements</span></span>  
  
|<span data-ttu-id="23cb7-120">要素</span><span class="sxs-lookup"><span data-stu-id="23cb7-120">Element</span></span>|<span data-ttu-id="23cb7-121">説明</span><span class="sxs-lookup"><span data-stu-id="23cb7-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="23cb7-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="23cb7-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="23cb7-123">エンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="23cb7-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="23cb7-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="23cb7-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.ClientViaElement>
- <xref:System.ServiceModel.Description.ClientViaBehavior>
