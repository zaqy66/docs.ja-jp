---
title: <diagnostics> アクティブ化
ms.date: 03/30/2017
ms.assetid: 1486e0eb-fe2a-46c3-b584-c924889477dd
ms.openlocfilehash: ac235b9a3c125cd3fe63ccd899e2ff92d4d3f31b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278453"
---
# <a name="diagnostics-for-activation"></a><span data-ttu-id="70172-102">\<診断 > アクティブ化</span><span class="sxs-lookup"><span data-stu-id="70172-102">\<diagnostics> for Activation</span></span>
<span data-ttu-id="70172-103">Windows Communication Foundation (WCF) リスナーの診断機能を構成します。</span><span class="sxs-lookup"><span data-stu-id="70172-103">Configures Windows Communication Foundation (WCF) listener's diagnostics functionalities.</span></span>  
  
 <span data-ttu-id="70172-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="70172-104">\<system.serviceModel.activation></span></span>  
<span data-ttu-id="70172-105">\<diagnostics></span><span class="sxs-lookup"><span data-stu-id="70172-105">\<diagnostics></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70172-106">構文</span><span class="sxs-lookup"><span data-stu-id="70172-106">Syntax</span></span>  
  
```xml  
<configuration>
  <system.serviceModel.activation>
    <diagnostics performanceCountersEnabled="Boolean" />
  </system.serviceModel.activation>
</configuration>
```  
  
## <a name="type"></a><span data-ttu-id="70172-107">型</span><span class="sxs-lookup"><span data-stu-id="70172-107">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="70172-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="70172-108">Attributes and Elements</span></span>  
 <span data-ttu-id="70172-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="70172-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="70172-110">属性</span><span class="sxs-lookup"><span data-stu-id="70172-110">Attributes</span></span>  
  
|<span data-ttu-id="70172-111">属性</span><span class="sxs-lookup"><span data-stu-id="70172-111">Attribute</span></span>|<span data-ttu-id="70172-112">説明</span><span class="sxs-lookup"><span data-stu-id="70172-112">Description</span></span>|  
|---------------|-----------------|  
|`performanceCountersEnabled`|<span data-ttu-id="70172-113">診断用パフォーマンス カウンターが有効であるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="70172-113">A Boolean value that indicates whether performance counters are enabled for diagnostic purposes.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="70172-114">子要素</span><span class="sxs-lookup"><span data-stu-id="70172-114">Child Elements</span></span>  
 <span data-ttu-id="70172-115">なし。</span><span class="sxs-lookup"><span data-stu-id="70172-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="70172-116">親要素</span><span class="sxs-lookup"><span data-stu-id="70172-116">Parent Elements</span></span>  
  
|<span data-ttu-id="70172-117">要素</span><span class="sxs-lookup"><span data-stu-id="70172-117">Element</span></span>|<span data-ttu-id="70172-118">説明</span><span class="sxs-lookup"><span data-stu-id="70172-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="70172-119">\<system.serviceModel.activation ></span><span class="sxs-lookup"><span data-stu-id="70172-119">\<system.serviceModel.activation></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel-activation.md)|<span data-ttu-id="70172-120">リスナー プロセス SMSvcHost.exe の設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="70172-120">Contains configuration settings for the listener process SMSvcHost.exe.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="70172-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="70172-121">See also</span></span>
- <xref:System.ServiceModel.Activation.Configuration.DiagnosticSection>
