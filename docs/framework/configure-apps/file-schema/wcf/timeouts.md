---
title: <timeOuts>
ms.date: 03/30/2017
ms.assetid: 7fccd436-b326-48ec-8de1-c16817a09e0d
ms.openlocfilehash: 8a8a352380fe6eedb41ead089405e7b79fad29fe
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55272778"
---
# <a name="timeouts"></a><span data-ttu-id="6586b-101">\<timeOuts></span><span class="sxs-lookup"><span data-stu-id="6586b-101">\<timeOuts></span></span>
<span data-ttu-id="6586b-102">サービス ホストを開くまたは閉じるまでに待機できる期間を指定する構成要素を表します。</span><span class="sxs-lookup"><span data-stu-id="6586b-102">Represents a configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>  
  
 <span data-ttu-id="6586b-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="6586b-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="6586b-104">\<client></span><span class="sxs-lookup"><span data-stu-id="6586b-104">\<client></span></span>  
<span data-ttu-id="6586b-105">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="6586b-105">\<endpoint></span></span>  
<span data-ttu-id="6586b-106">\<host></span><span class="sxs-lookup"><span data-stu-id="6586b-106">\<host></span></span>  
<span data-ttu-id="6586b-107">\<timeOuts></span><span class="sxs-lookup"><span data-stu-id="6586b-107">\<timeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6586b-108">構文</span><span class="sxs-lookup"><span data-stu-id="6586b-108">Syntax</span></span>  
  
```xml  
<timeOuts closeTimeout="TimeSpan"
          openTimeout="TimeSpan" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6586b-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="6586b-109">Attributes and Elements</span></span>  
 <span data-ttu-id="6586b-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6586b-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6586b-111">属性</span><span class="sxs-lookup"><span data-stu-id="6586b-111">Attributes</span></span>  
  
|<span data-ttu-id="6586b-112">属性</span><span class="sxs-lookup"><span data-stu-id="6586b-112">Attribute</span></span>|<span data-ttu-id="6586b-113">説明</span><span class="sxs-lookup"><span data-stu-id="6586b-113">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="6586b-114">サービス ホストを閉じるまでに待機できる期間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="6586b-114">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to close.</span></span>|  
|`openTimeout`|<span data-ttu-id="6586b-115">サービス ホストを開くまでに待機できる期間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="6586b-115">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to open.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6586b-116">子要素</span><span class="sxs-lookup"><span data-stu-id="6586b-116">Child Elements</span></span>  
 <span data-ttu-id="6586b-117">なし。</span><span class="sxs-lookup"><span data-stu-id="6586b-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6586b-118">親要素</span><span class="sxs-lookup"><span data-stu-id="6586b-118">Parent Elements</span></span>  
  
|<span data-ttu-id="6586b-119">要素</span><span class="sxs-lookup"><span data-stu-id="6586b-119">Element</span></span>|<span data-ttu-id="6586b-120">説明</span><span class="sxs-lookup"><span data-stu-id="6586b-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6586b-121">\<host></span><span class="sxs-lookup"><span data-stu-id="6586b-121">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="6586b-122">サービス ホストの設定を指定する構成要素です。</span><span class="sxs-lookup"><span data-stu-id="6586b-122">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6586b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="6586b-123">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [<span data-ttu-id="6586b-124">ホスティング</span><span class="sxs-lookup"><span data-stu-id="6586b-124">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
