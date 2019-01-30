---
title: <services>
ms.date: 03/30/2017
ms.assetid: 80d76ba9-2058-48ad-9b91-5e4be7e5c113
ms.openlocfilehash: 4dc425fa97eaf99664f0d9bbbbc851c462cbf373
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55274964"
---
# <a name="services"></a><span data-ttu-id="27742-101">\<services></span><span class="sxs-lookup"><span data-stu-id="27742-101">\<services></span></span>
<span data-ttu-id="27742-102">サービスは、設定ファイルの `services` セクションで定義されます。</span><span class="sxs-lookup"><span data-stu-id="27742-102">Services are defined in the `services` section of the configuration file.</span></span> <span data-ttu-id="27742-103">各サービスには、独自の `service` 設定セクションがあります。</span><span class="sxs-lookup"><span data-stu-id="27742-103">Each service has its own `service` configuration section.</span></span>  
  
 <span data-ttu-id="27742-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="27742-104">\<system.ServiceModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="27742-105">構文</span><span class="sxs-lookup"><span data-stu-id="27742-105">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service>
    </service>
  </services>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="27742-106">属性および要素</span><span class="sxs-lookup"><span data-stu-id="27742-106">Attributes and Elements</span></span>  
 <span data-ttu-id="27742-107">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="27742-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="27742-108">属性</span><span class="sxs-lookup"><span data-stu-id="27742-108">Attributes</span></span>  
 <span data-ttu-id="27742-109">なし</span><span class="sxs-lookup"><span data-stu-id="27742-109">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="27742-110">子要素</span><span class="sxs-lookup"><span data-stu-id="27742-110">Child Elements</span></span>  
  
|<span data-ttu-id="27742-111">要素</span><span class="sxs-lookup"><span data-stu-id="27742-111">Element</span></span>|<span data-ttu-id="27742-112">説明</span><span class="sxs-lookup"><span data-stu-id="27742-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="27742-113">\<service></span><span class="sxs-lookup"><span data-stu-id="27742-113">\<service></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|<span data-ttu-id="27742-114">サービス コントラクト、動作、および特定のサービスのエンドポイントを定義します。</span><span class="sxs-lookup"><span data-stu-id="27742-114">Define the service contract, behavior, and endpoints of the particular service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="27742-115">親要素</span><span class="sxs-lookup"><span data-stu-id="27742-115">Parent Elements</span></span>  
  
|<span data-ttu-id="27742-116">要素</span><span class="sxs-lookup"><span data-stu-id="27742-116">Element</span></span>|<span data-ttu-id="27742-117">説明</span><span class="sxs-lookup"><span data-stu-id="27742-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="27742-118">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="27742-118">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="27742-119">すべての Windows Communication Foundation (WCF) 構成要素のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="27742-119">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="27742-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="27742-120">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServicesSection>
