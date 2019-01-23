---
title: '&lt;endToEndTracing&gt;'
ms.date: 03/30/2017
ms.assetid: 5034f5de-bb60-4157-9ad4-58aaade094e0
ms.openlocfilehash: c2f5e33eff4fdc6dfa85bcc10b59a7c1436cabb6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54519387"
---
# <a name="ltendtoendtracinggt"></a><span data-ttu-id="76406-102">&lt;endToEndTracing&gt;</span><span class="sxs-lookup"><span data-stu-id="76406-102">&lt;endToEndTracing&gt;</span></span>
<span data-ttu-id="76406-103">サービス アプリケーションの実行中にエンドツーエンドのトレースのさまざまな側面を有効または無効にするための構成要素。</span><span class="sxs-lookup"><span data-stu-id="76406-103">A configuration element that allows you to enable and disable different aspects of end-to-end tracing during the running of a service application.</span></span>  
  
 <span data-ttu-id="76406-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="76406-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="76406-105">\<診断 ></span><span class="sxs-lookup"><span data-stu-id="76406-105">\<diagnostic></span></span>  
<span data-ttu-id="76406-106">\<endToEndTracing ></span><span class="sxs-lookup"><span data-stu-id="76406-106">\<endToEndTracing></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76406-107">構文</span><span class="sxs-lookup"><span data-stu-id="76406-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <diagnostics>
    <endToEndTracing activityTracing="Boolean"
                     messageFlowTracing="Boolean"
                     propagateActivity="Boolean" />
  </diagnostics>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="76406-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="76406-108">Attributes and Elements</span></span>  
 <span data-ttu-id="76406-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="76406-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="76406-110">属性</span><span class="sxs-lookup"><span data-stu-id="76406-110">Attributes</span></span>  
  
|<span data-ttu-id="76406-111">属性</span><span class="sxs-lookup"><span data-stu-id="76406-111">Attribute</span></span>|<span data-ttu-id="76406-112">説明</span><span class="sxs-lookup"><span data-stu-id="76406-112">Description</span></span>|  
|---------------|-----------------|  
|`activityTracing`|<span data-ttu-id="76406-113">アクティビティのトレースが有効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="76406-113">A Boolean value that specifies whether activity tracing is enabled.</span></span>|  
|`messageFlowTracing`|<span data-ttu-id="76406-114">メッセージ フローのトレースが有効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="76406-114">A Boolean value that specifies whether message flow tracing in enabled.</span></span>|  
|`propagateActivity`|<span data-ttu-id="76406-115">伝達属性が true に設定されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="76406-115">A Boolean value that specifies whether the propagate attribute is set to true.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="76406-116">子要素</span><span class="sxs-lookup"><span data-stu-id="76406-116">Child Elements</span></span>  
 <span data-ttu-id="76406-117">なし。</span><span class="sxs-lookup"><span data-stu-id="76406-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="76406-118">親要素</span><span class="sxs-lookup"><span data-stu-id="76406-118">Parent Elements</span></span>  
  
|<span data-ttu-id="76406-119">要素</span><span class="sxs-lookup"><span data-stu-id="76406-119">Element</span></span>|<span data-ttu-id="76406-120">説明</span><span class="sxs-lookup"><span data-stu-id="76406-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="76406-121">\<diagnostics></span><span class="sxs-lookup"><span data-stu-id="76406-121">\<diagnostics></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/diagnostics.md)|<span data-ttu-id="76406-122">管理者が行うランタイムの検査と管理の WCF 設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="76406-122">Defines WCF settings for runtime inspection and control for the administrator.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="76406-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="76406-123">See also</span></span>
- <xref:System.ServiceModel.Configuration.DiagnosticSection>
- <xref:System.ServiceModel.Diagnostics>
- <xref:System.ServiceModel.Configuration.DiagnosticSection.EndToEndTracing%2A>
- <xref:System.ServiceModel.Configuration.EndToEndTracingElement>
- [<span data-ttu-id="76406-124">エンドツーエンドのトレース</span><span class="sxs-lookup"><span data-stu-id="76406-124">End-to-End Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/end-to-end-tracing.md)
