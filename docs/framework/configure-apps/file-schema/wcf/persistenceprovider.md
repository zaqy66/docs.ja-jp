---
title: <persistenceProvider>
ms.date: 03/30/2017
ms.assetid: a37049c5-a7ea-4519-94f2-912eeb010380
ms.openlocfilehash: 054991687a54ecbf95cc18f58717a4ed3e36f050
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55260802"
---
# <a name="persistenceprovider"></a><span data-ttu-id="a58af-101">\<persistenceProvider ></span><span class="sxs-lookup"><span data-stu-id="a58af-101">\<persistenceProvider></span></span>
<span data-ttu-id="a58af-102">使用する永続化プロバイダーの実装の型と、永続化操作に使用するタイムアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="a58af-102">Specifies the type of the persistence provider implementation to use, as well as the time-out to use for persistence operations.</span></span>  
  
 <span data-ttu-id="a58af-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="a58af-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="a58af-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="a58af-104">\<behaviors></span></span>  
<span data-ttu-id="a58af-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="a58af-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="a58af-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="a58af-106">\<behavior></span></span>  
<span data-ttu-id="a58af-107">\<persistenceProvider ></span><span class="sxs-lookup"><span data-stu-id="a58af-107">\<persistenceProvider></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a58af-108">構文</span><span class="sxs-lookup"><span data-stu-id="a58af-108">Syntax</span></span>  
  
```xml  
<persistenceProvider persistenceOperationTimeout="TimeSpan"
                     type="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a58af-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a58af-109">Attributes and Elements</span></span>  
 <span data-ttu-id="a58af-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a58af-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a58af-111">属性</span><span class="sxs-lookup"><span data-stu-id="a58af-111">Attributes</span></span>  
  
|<span data-ttu-id="a58af-112">属性</span><span class="sxs-lookup"><span data-stu-id="a58af-112">Attribute</span></span>|<span data-ttu-id="a58af-113">説明</span><span class="sxs-lookup"><span data-stu-id="a58af-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a58af-114">persistenceOperationTimeout</span><span class="sxs-lookup"><span data-stu-id="a58af-114">persistenceOperationTimeout</span></span>|<span data-ttu-id="a58af-115">永続化動作に使用するタイムアウトを指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="a58af-115">A <xref:System.TimeSpan> value that specifies the time-out used for persistence operations.</span></span> <span data-ttu-id="a58af-116">既定値は"00: 00:30"。</span><span class="sxs-lookup"><span data-stu-id="a58af-116">The default is "00:00:30".</span></span>|  
|<span data-ttu-id="a58af-117">型</span><span class="sxs-lookup"><span data-stu-id="a58af-117">type</span></span>|<span data-ttu-id="a58af-118">使用する永続化プロバイダー ファクトリの型を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="a58af-118">A string that specifies the type of the persistence provider factory to use.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a58af-119">子要素</span><span class="sxs-lookup"><span data-stu-id="a58af-119">Child Elements</span></span>  
 <span data-ttu-id="a58af-120">なし。</span><span class="sxs-lookup"><span data-stu-id="a58af-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a58af-121">親要素</span><span class="sxs-lookup"><span data-stu-id="a58af-121">Parent Elements</span></span>  
  
|<span data-ttu-id="a58af-122">要素</span><span class="sxs-lookup"><span data-stu-id="a58af-122">Element</span></span>|<span data-ttu-id="a58af-123">説明</span><span class="sxs-lookup"><span data-stu-id="a58af-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a58af-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="a58af-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="a58af-125">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="a58af-125">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a58af-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="a58af-126">Remarks</span></span>  
 <span data-ttu-id="a58af-127">この要素は、WCF サービスの状態をシリアル化するために使用される永続化プロバイダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="a58af-127">This element specifies the persistence provider to be used to serialize the state of a WCF service.</span></span> <span data-ttu-id="a58af-128">HTTP ヘッダーに状態情報を渡す `wsHttpContextBinding` と一緒に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a58af-128">It should be used together with the `wsHttpContextBinding` which passes state information in HTTP headers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a58af-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a58af-129">See also</span></span>
- <xref:System.ServiceModel.Configuration.PersistenceProviderElement>
- <xref:System.ServiceModel.Persistence.PersistenceProvider>
