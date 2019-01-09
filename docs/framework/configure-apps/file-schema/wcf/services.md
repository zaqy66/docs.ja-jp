---
title: '&lt;サービス&gt;'
ms.date: 03/30/2017
ms.assetid: 80d76ba9-2058-48ad-9b91-5e4be7e5c113
ms.openlocfilehash: a48bd0ac30c1a85602122b2fd9213c2aa5159e91
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148098"
---
# <a name="ltservicesgt"></a><span data-ttu-id="7b3bb-102">&lt;サービス&gt;</span><span class="sxs-lookup"><span data-stu-id="7b3bb-102">&lt;services&gt;</span></span>
<span data-ttu-id="7b3bb-103">サービスは、設定ファイルの `services` セクションで定義されます。</span><span class="sxs-lookup"><span data-stu-id="7b3bb-103">Services are defined in the `services` section of the configuration file.</span></span> <span data-ttu-id="7b3bb-104">各サービスには、独自の `service` 設定セクションがあります。</span><span class="sxs-lookup"><span data-stu-id="7b3bb-104">Each service has its own `service` configuration section.</span></span>  
  
 <span data-ttu-id="7b3bb-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="7b3bb-105">\<system.ServiceModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b3bb-106">構文</span><span class="sxs-lookup"><span data-stu-id="7b3bb-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service>
    </service>
  </services>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7b3bb-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="7b3bb-107">Attributes and Elements</span></span>  
 <span data-ttu-id="7b3bb-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="7b3bb-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7b3bb-109">属性</span><span class="sxs-lookup"><span data-stu-id="7b3bb-109">Attributes</span></span>  
 <span data-ttu-id="7b3bb-110">なし</span><span class="sxs-lookup"><span data-stu-id="7b3bb-110">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="7b3bb-111">子要素</span><span class="sxs-lookup"><span data-stu-id="7b3bb-111">Child Elements</span></span>  
  
|<span data-ttu-id="7b3bb-112">要素</span><span class="sxs-lookup"><span data-stu-id="7b3bb-112">Element</span></span>|<span data-ttu-id="7b3bb-113">説明</span><span class="sxs-lookup"><span data-stu-id="7b3bb-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7b3bb-114">\<service></span><span class="sxs-lookup"><span data-stu-id="7b3bb-114">\<service></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|<span data-ttu-id="7b3bb-115">サービス コントラクト、動作、および特定のサービスのエンドポイントを定義します。</span><span class="sxs-lookup"><span data-stu-id="7b3bb-115">Define the service contract, behavior, and endpoints of the particular service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="7b3bb-116">親要素</span><span class="sxs-lookup"><span data-stu-id="7b3bb-116">Parent Elements</span></span>  
  
|<span data-ttu-id="7b3bb-117">要素</span><span class="sxs-lookup"><span data-stu-id="7b3bb-117">Element</span></span>|<span data-ttu-id="7b3bb-118">説明</span><span class="sxs-lookup"><span data-stu-id="7b3bb-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7b3bb-119">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="7b3bb-119">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="7b3bb-120">すべての Windows Communication Foundation (WCF) 構成要素のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="7b3bb-120">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7b3bb-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b3bb-121">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServicesSection>
