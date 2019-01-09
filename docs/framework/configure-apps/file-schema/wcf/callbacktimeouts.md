---
title: '&lt;callbackTimeouts&gt;'
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: 85e7b1f0d009e27cbacd9f69b381e4f05984bf56
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149112"
---
# <a name="ltcallbacktimeoutsgt"></a><span data-ttu-id="0a70d-102">&lt;callbackTimeouts&gt;</span><span class="sxs-lookup"><span data-stu-id="0a70d-102">&lt;callbackTimeouts&gt;</span></span>
<span data-ttu-id="0a70d-103">双方向コールバック コントラクト シナリオでトランザクションをサーバーからクライアントに転送する際のタイムアウト値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0a70d-103">Specifies the timeout value when flowing transactions from server to client.in a duplex callback contract scenario.</span></span>  
  
 <span data-ttu-id="0a70d-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="0a70d-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="0a70d-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="0a70d-105">\<behaviors></span></span>  
<span data-ttu-id="0a70d-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="0a70d-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="0a70d-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="0a70d-107">\<behavior></span></span>  
<span data-ttu-id="0a70d-108">\<callbackTimeOuts ></span><span class="sxs-lookup"><span data-stu-id="0a70d-108">\<callbackTimeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a70d-109">構文</span><span class="sxs-lookup"><span data-stu-id="0a70d-109">Syntax</span></span>  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="0a70d-110">型</span><span class="sxs-lookup"><span data-stu-id="0a70d-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0a70d-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="0a70d-111">Attributes and Elements</span></span>  
 <span data-ttu-id="0a70d-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a70d-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0a70d-113">属性</span><span class="sxs-lookup"><span data-stu-id="0a70d-113">Attributes</span></span>  
  
|<span data-ttu-id="0a70d-114">属性</span><span class="sxs-lookup"><span data-stu-id="0a70d-114">Attribute</span></span>|<span data-ttu-id="0a70d-115">説明</span><span class="sxs-lookup"><span data-stu-id="0a70d-115">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="0a70d-116">トランザクションが完了する必要があるまたは自動的に終了される必要がある制限時間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="0a70d-116">A <xref:System.TimeSpan> value that specifies the interval of time within which transactions must complete or be automatically terminated.</span></span> <span data-ttu-id="0a70d-117">既定値は"00: 00:00"。</span><span class="sxs-lookup"><span data-stu-id="0a70d-117">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0a70d-118">子要素</span><span class="sxs-lookup"><span data-stu-id="0a70d-118">Child Elements</span></span>  
 <span data-ttu-id="0a70d-119">なし。</span><span class="sxs-lookup"><span data-stu-id="0a70d-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0a70d-120">親要素</span><span class="sxs-lookup"><span data-stu-id="0a70d-120">Parent Elements</span></span>  
  
|<span data-ttu-id="0a70d-121">要素</span><span class="sxs-lookup"><span data-stu-id="0a70d-121">Element</span></span>|<span data-ttu-id="0a70d-122">説明</span><span class="sxs-lookup"><span data-stu-id="0a70d-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0a70d-123">\<behavior></span><span class="sxs-lookup"><span data-stu-id="0a70d-123">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="0a70d-124">エンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0a70d-124">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0a70d-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a70d-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
