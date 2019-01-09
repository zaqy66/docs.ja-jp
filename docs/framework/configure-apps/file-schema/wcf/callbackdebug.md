---
title: '&lt;callbackDebug&gt;'
ms.date: 03/30/2017
ms.assetid: 4073feda-1857-4be4-9947-227afb847ced
ms.openlocfilehash: 5bd2356c3bb798e948341cb3c4ba504ac886ed44
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145082"
---
# <a name="ltcallbackdebuggt"></a><span data-ttu-id="65f1c-102">&lt;callbackDebug&gt;</span><span class="sxs-lookup"><span data-stu-id="65f1c-102">&lt;callbackDebug&gt;</span></span>
<span data-ttu-id="65f1c-103">Windows Communication Foundation (WCF) コールバック オブジェクトのサービス デバッグを指定します。</span><span class="sxs-lookup"><span data-stu-id="65f1c-103">Specifies service debugging for a Windows Communication Foundation (WCF) callback object.</span></span>  
  
 <span data-ttu-id="65f1c-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="65f1c-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="65f1c-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="65f1c-105">\<behaviors></span></span>  
<span data-ttu-id="65f1c-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="65f1c-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="65f1c-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="65f1c-107">\<behavior></span></span>  
<span data-ttu-id="65f1c-108">\<callbackDebug ></span><span class="sxs-lookup"><span data-stu-id="65f1c-108">\<callbackDebug></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65f1c-109">構文</span><span class="sxs-lookup"><span data-stu-id="65f1c-109">Syntax</span></span>  
  
```xml  
<callbackDebug includeExceptionDetailInFaults="Boolean" />
```  
  
## <a name="type"></a><span data-ttu-id="65f1c-110">型</span><span class="sxs-lookup"><span data-stu-id="65f1c-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="65f1c-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="65f1c-111">Attributes and Elements</span></span>  
 <span data-ttu-id="65f1c-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="65f1c-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="65f1c-113">属性</span><span class="sxs-lookup"><span data-stu-id="65f1c-113">Attributes</span></span>  
  
|<span data-ttu-id="65f1c-114">属性</span><span class="sxs-lookup"><span data-stu-id="65f1c-114">Attribute</span></span>|<span data-ttu-id="65f1c-115">説明</span><span class="sxs-lookup"><span data-stu-id="65f1c-115">Description</span></span>|  
|---------------|-----------------|  
|`includeExceptionDetailInFaults`|<span data-ttu-id="65f1c-116">クライアント コールバック オブジェクトが SOAP エラー内のマネージド例外情報をサービスに返すかどうかを指定する値。</span><span class="sxs-lookup"><span data-stu-id="65f1c-116">A value that specifies whether client callback objects return managed exception information in SOAP faults back to the service.</span></span><br /><br /> <span data-ttu-id="65f1c-117">プログラムでこの属性を `true` に設定すると、デバッグするために、クライアント コールバック オブジェクト内のマネージド例外情報がサービスに戻るフローを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="65f1c-117">If you set this attribute to `true` programmatically, you can enable the flow of managed exception information in a client callback object back to the service for debugging purposes.</span></span> <span data-ttu-id="65f1c-118">**注意:** マネージド例外情報をクライアントに返すことは、セキュリティ リスクになり得ます。</span><span class="sxs-lookup"><span data-stu-id="65f1c-118">**Caution:**  Returning managed exception information to clients can be a security risk.</span></span> <span data-ttu-id="65f1c-119">これは、例外の詳細が、認証されていないクライアントによって使用可能な内部サービスの実装に関する情報を公開するためです。</span><span class="sxs-lookup"><span data-stu-id="65f1c-119">This is because exception details expose information about the internal service implementation that could be used by unauthorized clients.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="65f1c-120">子要素</span><span class="sxs-lookup"><span data-stu-id="65f1c-120">Child Elements</span></span>  
 <span data-ttu-id="65f1c-121">なし。</span><span class="sxs-lookup"><span data-stu-id="65f1c-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="65f1c-122">親要素</span><span class="sxs-lookup"><span data-stu-id="65f1c-122">Parent Elements</span></span>  
  
|<span data-ttu-id="65f1c-123">要素</span><span class="sxs-lookup"><span data-stu-id="65f1c-123">Element</span></span>|<span data-ttu-id="65f1c-124">説明</span><span class="sxs-lookup"><span data-stu-id="65f1c-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="65f1c-125">\<behavior></span><span class="sxs-lookup"><span data-stu-id="65f1c-125">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="65f1c-126">エンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="65f1c-126">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="65f1c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="65f1c-127">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.CallbackDebugElement>  
 <xref:System.ServiceModel.Description.CallbackDebugBehavior>
