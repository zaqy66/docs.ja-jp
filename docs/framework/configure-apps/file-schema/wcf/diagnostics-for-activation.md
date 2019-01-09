---
title: アクティベーションの &lt;diagnostics&gt;
ms.date: 03/30/2017
ms.assetid: 1486e0eb-fe2a-46c3-b584-c924889477dd
ms.openlocfilehash: 28f051a7ab06dbc1b40f804c56071818eb37e88b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54144978"
---
# <a name="ltdiagnosticsgt-for-activation"></a><span data-ttu-id="bd3bc-102">アクティベーションの &lt;diagnostics&gt;</span><span class="sxs-lookup"><span data-stu-id="bd3bc-102">&lt;diagnostics&gt; for Activation</span></span>
<span data-ttu-id="bd3bc-103">Windows Communication Foundation (WCF) リスナーの診断機能を構成します。</span><span class="sxs-lookup"><span data-stu-id="bd3bc-103">Configures Windows Communication Foundation (WCF) listener's diagnostics functionalities.</span></span>  
  
 <span data-ttu-id="bd3bc-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="bd3bc-104">\<system.serviceModel.activation></span></span>  
<span data-ttu-id="bd3bc-105">\<診断 ></span><span class="sxs-lookup"><span data-stu-id="bd3bc-105">\<diagnostics></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd3bc-106">構文</span><span class="sxs-lookup"><span data-stu-id="bd3bc-106">Syntax</span></span>  
  
```xml  
<configuration>
  <system.serviceModel.activation>
    <diagnostics performanceCountersEnabled="Boolean" />
  </system.serviceModel.activation>
</configuration>
```  
  
## <a name="type"></a><span data-ttu-id="bd3bc-107">型</span><span class="sxs-lookup"><span data-stu-id="bd3bc-107">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bd3bc-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="bd3bc-108">Attributes and Elements</span></span>  
 <span data-ttu-id="bd3bc-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="bd3bc-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bd3bc-110">属性</span><span class="sxs-lookup"><span data-stu-id="bd3bc-110">Attributes</span></span>  
  
|<span data-ttu-id="bd3bc-111">属性</span><span class="sxs-lookup"><span data-stu-id="bd3bc-111">Attribute</span></span>|<span data-ttu-id="bd3bc-112">説明</span><span class="sxs-lookup"><span data-stu-id="bd3bc-112">Description</span></span>|  
|---------------|-----------------|  
|`performanceCountersEnabled`|<span data-ttu-id="bd3bc-113">診断用パフォーマンス カウンターが有効であるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="bd3bc-113">A Boolean value that indicates whether performance counters are enabled for diagnostic purposes.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bd3bc-114">子要素</span><span class="sxs-lookup"><span data-stu-id="bd3bc-114">Child Elements</span></span>  
 <span data-ttu-id="bd3bc-115">なし。</span><span class="sxs-lookup"><span data-stu-id="bd3bc-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bd3bc-116">親要素</span><span class="sxs-lookup"><span data-stu-id="bd3bc-116">Parent Elements</span></span>  
  
|<span data-ttu-id="bd3bc-117">要素</span><span class="sxs-lookup"><span data-stu-id="bd3bc-117">Element</span></span>|<span data-ttu-id="bd3bc-118">説明</span><span class="sxs-lookup"><span data-stu-id="bd3bc-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bd3bc-119">\<system.serviceModel.activation ></span><span class="sxs-lookup"><span data-stu-id="bd3bc-119">\<system.serviceModel.activation></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel-activation.md)|<span data-ttu-id="bd3bc-120">リスナー プロセス SMSvcHost.exe の設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bd3bc-120">Contains configuration settings for the listener process SMSvcHost.exe.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="bd3bc-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd3bc-121">See Also</span></span>  
 <xref:System.ServiceModel.Activation.Configuration.DiagnosticSection>
