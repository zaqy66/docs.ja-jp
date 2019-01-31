---
title: <callbackDebug>
ms.date: 03/30/2017
ms.assetid: 4073feda-1857-4be4-9947-227afb847ced
ms.openlocfilehash: 62ce1bc179c7215d4988e4c6bda08025c3d3e5de
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55286313"
---
# <a name="callbackdebug"></a><span data-ttu-id="d51a4-101">\<callbackDebug></span><span class="sxs-lookup"><span data-stu-id="d51a4-101">\<callbackDebug></span></span>
<span data-ttu-id="d51a4-102">Windows Communication Foundation (WCF) コールバック オブジェクトのサービス デバッグを指定します。</span><span class="sxs-lookup"><span data-stu-id="d51a4-102">Specifies service debugging for a Windows Communication Foundation (WCF) callback object.</span></span>  
  
 <span data-ttu-id="d51a4-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="d51a4-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="d51a4-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="d51a4-104">\<behaviors></span></span>  
<span data-ttu-id="d51a4-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="d51a4-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="d51a4-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="d51a4-106">\<behavior></span></span>  
<span data-ttu-id="d51a4-107">\<callbackDebug></span><span class="sxs-lookup"><span data-stu-id="d51a4-107">\<callbackDebug></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d51a4-108">構文</span><span class="sxs-lookup"><span data-stu-id="d51a4-108">Syntax</span></span>  
  
```xml  
<callbackDebug includeExceptionDetailInFaults="Boolean" />
```  
  
## <a name="type"></a><span data-ttu-id="d51a4-109">型</span><span class="sxs-lookup"><span data-stu-id="d51a4-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d51a4-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="d51a4-110">Attributes and Elements</span></span>  
 <span data-ttu-id="d51a4-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="d51a4-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d51a4-112">属性</span><span class="sxs-lookup"><span data-stu-id="d51a4-112">Attributes</span></span>  
  
|<span data-ttu-id="d51a4-113">属性</span><span class="sxs-lookup"><span data-stu-id="d51a4-113">Attribute</span></span>|<span data-ttu-id="d51a4-114">説明</span><span class="sxs-lookup"><span data-stu-id="d51a4-114">Description</span></span>|  
|---------------|-----------------|  
|`includeExceptionDetailInFaults`|<span data-ttu-id="d51a4-115">クライアント コールバック オブジェクトが SOAP エラー内のマネージド例外情報をサービスに返すかどうかを指定する値。</span><span class="sxs-lookup"><span data-stu-id="d51a4-115">A value that specifies whether client callback objects return managed exception information in SOAP faults back to the service.</span></span><br /><br /> <span data-ttu-id="d51a4-116">プログラムでこの属性を `true` に設定すると、デバッグするために、クライアント コールバック オブジェクト内のマネージド例外情報がサービスに戻るフローを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="d51a4-116">If you set this attribute to `true` programmatically, you can enable the flow of managed exception information in a client callback object back to the service for debugging purposes.</span></span> <span data-ttu-id="d51a4-117">**注意:** マネージド例外情報をクライアントに返すことは、セキュリティ リスクになり得ます。</span><span class="sxs-lookup"><span data-stu-id="d51a4-117">**Caution:**  Returning managed exception information to clients can be a security risk.</span></span> <span data-ttu-id="d51a4-118">これは、例外の詳細が、認証されていないクライアントによって使用可能な内部サービスの実装に関する情報を公開するためです。</span><span class="sxs-lookup"><span data-stu-id="d51a4-118">This is because exception details expose information about the internal service implementation that could be used by unauthorized clients.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d51a4-119">子要素</span><span class="sxs-lookup"><span data-stu-id="d51a4-119">Child Elements</span></span>  
 <span data-ttu-id="d51a4-120">なし。</span><span class="sxs-lookup"><span data-stu-id="d51a4-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d51a4-121">親要素</span><span class="sxs-lookup"><span data-stu-id="d51a4-121">Parent Elements</span></span>  
  
|<span data-ttu-id="d51a4-122">要素</span><span class="sxs-lookup"><span data-stu-id="d51a4-122">Element</span></span>|<span data-ttu-id="d51a4-123">説明</span><span class="sxs-lookup"><span data-stu-id="d51a4-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d51a4-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="d51a4-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="d51a4-125">エンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d51a4-125">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d51a4-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="d51a4-126">See also</span></span>
- <xref:System.ServiceModel.Configuration.CallbackDebugElement>
- <xref:System.ServiceModel.Description.CallbackDebugBehavior>
