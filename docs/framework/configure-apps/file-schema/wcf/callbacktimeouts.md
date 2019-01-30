---
title: <callbackTimeouts>
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: 269500324ad1beaa0b519fa17d251ee942276faa
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269069"
---
# <a name="callbacktimeouts"></a><span data-ttu-id="e2ff2-101">\<callbackTimeouts></span><span class="sxs-lookup"><span data-stu-id="e2ff2-101">\<callbackTimeouts></span></span>
<span data-ttu-id="e2ff2-102">双方向コールバック コントラクト シナリオでトランザクションをサーバーからクライアントに転送する際のタイムアウト値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2ff2-102">Specifies the timeout value when flowing transactions from server to client.in a duplex callback contract scenario.</span></span>  
  
 <span data-ttu-id="e2ff2-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="e2ff2-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="e2ff2-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="e2ff2-104">\<behaviors></span></span>  
<span data-ttu-id="e2ff2-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="e2ff2-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="e2ff2-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="e2ff2-106">\<behavior></span></span>  
<span data-ttu-id="e2ff2-107">\<callbackTimeOuts></span><span class="sxs-lookup"><span data-stu-id="e2ff2-107">\<callbackTimeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2ff2-108">構文</span><span class="sxs-lookup"><span data-stu-id="e2ff2-108">Syntax</span></span>  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="e2ff2-109">型</span><span class="sxs-lookup"><span data-stu-id="e2ff2-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e2ff2-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="e2ff2-110">Attributes and Elements</span></span>  
 <span data-ttu-id="e2ff2-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e2ff2-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e2ff2-112">属性</span><span class="sxs-lookup"><span data-stu-id="e2ff2-112">Attributes</span></span>  
  
|<span data-ttu-id="e2ff2-113">属性</span><span class="sxs-lookup"><span data-stu-id="e2ff2-113">Attribute</span></span>|<span data-ttu-id="e2ff2-114">説明</span><span class="sxs-lookup"><span data-stu-id="e2ff2-114">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="e2ff2-115">トランザクションが完了する必要があるまたは自動的に終了される必要がある制限時間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="e2ff2-115">A <xref:System.TimeSpan> value that specifies the interval of time within which transactions must complete or be automatically terminated.</span></span> <span data-ttu-id="e2ff2-116">既定値は"00: 00:00"。</span><span class="sxs-lookup"><span data-stu-id="e2ff2-116">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e2ff2-117">子要素</span><span class="sxs-lookup"><span data-stu-id="e2ff2-117">Child Elements</span></span>  
 <span data-ttu-id="e2ff2-118">なし。</span><span class="sxs-lookup"><span data-stu-id="e2ff2-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e2ff2-119">親要素</span><span class="sxs-lookup"><span data-stu-id="e2ff2-119">Parent Elements</span></span>  
  
|<span data-ttu-id="e2ff2-120">要素</span><span class="sxs-lookup"><span data-stu-id="e2ff2-120">Element</span></span>|<span data-ttu-id="e2ff2-121">説明</span><span class="sxs-lookup"><span data-stu-id="e2ff2-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e2ff2-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="e2ff2-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="e2ff2-123">エンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2ff2-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e2ff2-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2ff2-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
