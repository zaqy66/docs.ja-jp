---
title: '&lt;callbackTimeouts&gt;'
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: 01932fe2b7b7e699311e2c65ec8adaf0aef82dc5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54557904"
---
# <a name="ltcallbacktimeoutsgt"></a><span data-ttu-id="2eb01-102">&lt;callbackTimeouts&gt;</span><span class="sxs-lookup"><span data-stu-id="2eb01-102">&lt;callbackTimeouts&gt;</span></span>
<span data-ttu-id="2eb01-103">双方向コールバック コントラクト シナリオでトランザクションをサーバーからクライアントに転送する際のタイムアウト値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2eb01-103">Specifies the timeout value when flowing transactions from server to client.in a duplex callback contract scenario.</span></span>  
  
 <span data-ttu-id="2eb01-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="2eb01-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="2eb01-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="2eb01-105">\<behaviors></span></span>  
<span data-ttu-id="2eb01-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="2eb01-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="2eb01-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="2eb01-107">\<behavior></span></span>  
<span data-ttu-id="2eb01-108">\<callbackTimeOuts></span><span class="sxs-lookup"><span data-stu-id="2eb01-108">\<callbackTimeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2eb01-109">構文</span><span class="sxs-lookup"><span data-stu-id="2eb01-109">Syntax</span></span>  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="2eb01-110">型</span><span class="sxs-lookup"><span data-stu-id="2eb01-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2eb01-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="2eb01-111">Attributes and Elements</span></span>  
 <span data-ttu-id="2eb01-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="2eb01-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2eb01-113">属性</span><span class="sxs-lookup"><span data-stu-id="2eb01-113">Attributes</span></span>  
  
|<span data-ttu-id="2eb01-114">属性</span><span class="sxs-lookup"><span data-stu-id="2eb01-114">Attribute</span></span>|<span data-ttu-id="2eb01-115">説明</span><span class="sxs-lookup"><span data-stu-id="2eb01-115">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="2eb01-116">トランザクションが完了する必要があるまたは自動的に終了される必要がある制限時間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="2eb01-116">A <xref:System.TimeSpan> value that specifies the interval of time within which transactions must complete or be automatically terminated.</span></span> <span data-ttu-id="2eb01-117">既定値は"00: 00:00"。</span><span class="sxs-lookup"><span data-stu-id="2eb01-117">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2eb01-118">子要素</span><span class="sxs-lookup"><span data-stu-id="2eb01-118">Child Elements</span></span>  
 <span data-ttu-id="2eb01-119">なし。</span><span class="sxs-lookup"><span data-stu-id="2eb01-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2eb01-120">親要素</span><span class="sxs-lookup"><span data-stu-id="2eb01-120">Parent Elements</span></span>  
  
|<span data-ttu-id="2eb01-121">要素</span><span class="sxs-lookup"><span data-stu-id="2eb01-121">Element</span></span>|<span data-ttu-id="2eb01-122">説明</span><span class="sxs-lookup"><span data-stu-id="2eb01-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2eb01-123">\<behavior></span><span class="sxs-lookup"><span data-stu-id="2eb01-123">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="2eb01-124">エンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2eb01-124">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2eb01-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="2eb01-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
