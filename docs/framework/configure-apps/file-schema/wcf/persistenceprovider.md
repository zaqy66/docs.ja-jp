---
title: '&lt;persistenceProvider&gt;'
ms.date: 03/30/2017
ms.assetid: a37049c5-a7ea-4519-94f2-912eeb010380
ms.openlocfilehash: ba02977a7df44931ae195040949e9a8eb0c141b5
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152022"
---
# <a name="ltpersistenceprovidergt"></a><span data-ttu-id="93696-102">&lt;persistenceProvider&gt;</span><span class="sxs-lookup"><span data-stu-id="93696-102">&lt;persistenceProvider&gt;</span></span>
<span data-ttu-id="93696-103">使用する永続化プロバイダーの実装の型と、永続化操作に使用するタイムアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="93696-103">Specifies the type of the persistence provider implementation to use, as well as the time-out to use for persistence operations.</span></span>  
  
 <span data-ttu-id="93696-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="93696-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="93696-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="93696-105">\<behaviors></span></span>  
<span data-ttu-id="93696-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="93696-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="93696-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="93696-107">\<behavior></span></span>  
<span data-ttu-id="93696-108">\<persistenceProvider ></span><span class="sxs-lookup"><span data-stu-id="93696-108">\<persistenceProvider></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93696-109">構文</span><span class="sxs-lookup"><span data-stu-id="93696-109">Syntax</span></span>  
  
```xml  
<persistenceProvider persistenceOperationTimeout="TimeSpan"
                     type="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="93696-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="93696-110">Attributes and Elements</span></span>  
 <span data-ttu-id="93696-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="93696-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="93696-112">属性</span><span class="sxs-lookup"><span data-stu-id="93696-112">Attributes</span></span>  
  
|<span data-ttu-id="93696-113">属性</span><span class="sxs-lookup"><span data-stu-id="93696-113">Attribute</span></span>|<span data-ttu-id="93696-114">説明</span><span class="sxs-lookup"><span data-stu-id="93696-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="93696-115">persistenceOperationTimeout</span><span class="sxs-lookup"><span data-stu-id="93696-115">persistenceOperationTimeout</span></span>|<span data-ttu-id="93696-116">永続化動作に使用するタイムアウトを指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="93696-116">A <xref:System.TimeSpan> value that specifies the time-out used for persistence operations.</span></span> <span data-ttu-id="93696-117">既定値は"00: 00:30"。</span><span class="sxs-lookup"><span data-stu-id="93696-117">The default is "00:00:30".</span></span>|  
|<span data-ttu-id="93696-118">型</span><span class="sxs-lookup"><span data-stu-id="93696-118">type</span></span>|<span data-ttu-id="93696-119">使用する永続化プロバイダー ファクトリの型を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93696-119">A string that specifies the type of the persistence provider factory to use.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="93696-120">子要素</span><span class="sxs-lookup"><span data-stu-id="93696-120">Child Elements</span></span>  
 <span data-ttu-id="93696-121">なし。</span><span class="sxs-lookup"><span data-stu-id="93696-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="93696-122">親要素</span><span class="sxs-lookup"><span data-stu-id="93696-122">Parent Elements</span></span>  
  
|<span data-ttu-id="93696-123">要素</span><span class="sxs-lookup"><span data-stu-id="93696-123">Element</span></span>|<span data-ttu-id="93696-124">説明</span><span class="sxs-lookup"><span data-stu-id="93696-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="93696-125">\<behavior></span><span class="sxs-lookup"><span data-stu-id="93696-125">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="93696-126">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="93696-126">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="93696-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="93696-127">Remarks</span></span>  
 <span data-ttu-id="93696-128">この要素は、WCF サービスの状態をシリアル化するために使用される永続化プロバイダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="93696-128">This element specifies the persistence provider to be used to serialize the state of a WCF service.</span></span> <span data-ttu-id="93696-129">HTTP ヘッダーに状態情報を渡す `wsHttpContextBinding` と一緒に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93696-129">It should be used together with the `wsHttpContextBinding` which passes state information in HTTP headers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93696-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="93696-130">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PersistenceProviderElement>  
 <xref:System.ServiceModel.Persistence.PersistenceProvider>
