---
title: '&lt;タイムアウト&gt;'
ms.date: 03/30/2017
ms.assetid: 7fccd436-b326-48ec-8de1-c16817a09e0d
ms.openlocfilehash: e39deeb251865b87eb7734e4447088ca2f221d1d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148332"
---
# <a name="lttimeoutsgt"></a><span data-ttu-id="eec95-102">&lt;タイムアウト&gt;</span><span class="sxs-lookup"><span data-stu-id="eec95-102">&lt;timeOuts&gt;</span></span>
<span data-ttu-id="eec95-103">サービス ホストを開くまたは閉じるまでに待機できる期間を指定する構成要素を表します。</span><span class="sxs-lookup"><span data-stu-id="eec95-103">Represents a configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>  
  
 <span data-ttu-id="eec95-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="eec95-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="eec95-105">\<client></span><span class="sxs-lookup"><span data-stu-id="eec95-105">\<client></span></span>  
<span data-ttu-id="eec95-106">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="eec95-106">\<endpoint></span></span>  
<span data-ttu-id="eec95-107">\<ホスト ></span><span class="sxs-lookup"><span data-stu-id="eec95-107">\<host></span></span>  
<span data-ttu-id="eec95-108">\<タイムアウト ></span><span class="sxs-lookup"><span data-stu-id="eec95-108">\<timeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eec95-109">構文</span><span class="sxs-lookup"><span data-stu-id="eec95-109">Syntax</span></span>  
  
```xml  
<timeOuts closeTimeout="TimeSpan"
          openTimeout="TimeSpan" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="eec95-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="eec95-110">Attributes and Elements</span></span>  
 <span data-ttu-id="eec95-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="eec95-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="eec95-112">属性</span><span class="sxs-lookup"><span data-stu-id="eec95-112">Attributes</span></span>  
  
|<span data-ttu-id="eec95-113">属性</span><span class="sxs-lookup"><span data-stu-id="eec95-113">Attribute</span></span>|<span data-ttu-id="eec95-114">説明</span><span class="sxs-lookup"><span data-stu-id="eec95-114">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="eec95-115">サービス ホストを閉じるまでに待機できる期間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="eec95-115">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to close.</span></span>|  
|`openTimeout`|<span data-ttu-id="eec95-116">サービス ホストを開くまでに待機できる期間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="eec95-116">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to open.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="eec95-117">子要素</span><span class="sxs-lookup"><span data-stu-id="eec95-117">Child Elements</span></span>  
 <span data-ttu-id="eec95-118">なし。</span><span class="sxs-lookup"><span data-stu-id="eec95-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="eec95-119">親要素</span><span class="sxs-lookup"><span data-stu-id="eec95-119">Parent Elements</span></span>  
  
|<span data-ttu-id="eec95-120">要素</span><span class="sxs-lookup"><span data-stu-id="eec95-120">Element</span></span>|<span data-ttu-id="eec95-121">説明</span><span class="sxs-lookup"><span data-stu-id="eec95-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="eec95-122">\<ホスト ></span><span class="sxs-lookup"><span data-stu-id="eec95-122">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="eec95-123">サービス ホストの設定を指定する構成要素です。</span><span class="sxs-lookup"><span data-stu-id="eec95-123">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="eec95-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="eec95-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.HostElement>  
 <xref:System.ServiceModel.ServiceHost>  
 [<span data-ttu-id="eec95-125">ホスティング</span><span class="sxs-lookup"><span data-stu-id="eec95-125">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
