---
title: '&lt;endToEndTracing&gt;'
ms.date: 03/30/2017
ms.assetid: 5034f5de-bb60-4157-9ad4-58aaade094e0
ms.openlocfilehash: 78a69256a391e97ff1962eea923f09115c4ebadd
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150111"
---
# <a name="ltendtoendtracinggt"></a><span data-ttu-id="a193a-102">&lt;endToEndTracing&gt;</span><span class="sxs-lookup"><span data-stu-id="a193a-102">&lt;endToEndTracing&gt;</span></span>
<span data-ttu-id="a193a-103">サービス アプリケーションの実行中にエンドツーエンドのトレースのさまざまな側面を有効または無効にするための構成要素。</span><span class="sxs-lookup"><span data-stu-id="a193a-103">A configuration element that allows you to enable and disable different aspects of end-to-end tracing during the running of a service application.</span></span>  
  
 <span data-ttu-id="a193a-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="a193a-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="a193a-105">\<診断 ></span><span class="sxs-lookup"><span data-stu-id="a193a-105">\<diagnostic></span></span>  
<span data-ttu-id="a193a-106">\<endToEndTracing ></span><span class="sxs-lookup"><span data-stu-id="a193a-106">\<endToEndTracing></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a193a-107">構文</span><span class="sxs-lookup"><span data-stu-id="a193a-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <diagnostics>
    <endToEndTracing activityTracing="Boolean"
                     messageFlowTracing="Boolean"
                     propagateActivity="Boolean" />
  </diagnostics>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a193a-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a193a-108">Attributes and Elements</span></span>  
 <span data-ttu-id="a193a-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a193a-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a193a-110">属性</span><span class="sxs-lookup"><span data-stu-id="a193a-110">Attributes</span></span>  
  
|<span data-ttu-id="a193a-111">属性</span><span class="sxs-lookup"><span data-stu-id="a193a-111">Attribute</span></span>|<span data-ttu-id="a193a-112">説明</span><span class="sxs-lookup"><span data-stu-id="a193a-112">Description</span></span>|  
|---------------|-----------------|  
|`activityTracing`|<span data-ttu-id="a193a-113">アクティビティのトレースが有効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a193a-113">A Boolean value that specifies whether activity tracing is enabled.</span></span>|  
|`messageFlowTracing`|<span data-ttu-id="a193a-114">メッセージ フローのトレースが有効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a193a-114">A Boolean value that specifies whether message flow tracing in enabled.</span></span>|  
|`propagateActivity`|<span data-ttu-id="a193a-115">伝達属性が true に設定されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a193a-115">A Boolean value that specifies whether the propagate attribute is set to true.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a193a-116">子要素</span><span class="sxs-lookup"><span data-stu-id="a193a-116">Child Elements</span></span>  
 <span data-ttu-id="a193a-117">なし。</span><span class="sxs-lookup"><span data-stu-id="a193a-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a193a-118">親要素</span><span class="sxs-lookup"><span data-stu-id="a193a-118">Parent Elements</span></span>  
  
|<span data-ttu-id="a193a-119">要素</span><span class="sxs-lookup"><span data-stu-id="a193a-119">Element</span></span>|<span data-ttu-id="a193a-120">説明</span><span class="sxs-lookup"><span data-stu-id="a193a-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a193a-121">\<診断 ></span><span class="sxs-lookup"><span data-stu-id="a193a-121">\<diagnostics></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/diagnostics.md)|<span data-ttu-id="a193a-122">管理者が行うランタイムの検査と管理の WCF 設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="a193a-122">Defines WCF settings for runtime inspection and control for the administrator.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a193a-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="a193a-123">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.DiagnosticSection>  
 <xref:System.ServiceModel.Diagnostics>  
 <xref:System.ServiceModel.Configuration.DiagnosticSection.EndToEndTracing%2A>  
 <xref:System.ServiceModel.Configuration.EndToEndTracingElement>  
 [<span data-ttu-id="a193a-124">エンドツーエンドのトレース</span><span class="sxs-lookup"><span data-stu-id="a193a-124">End-to-End Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/end-to-end-tracing.md)
