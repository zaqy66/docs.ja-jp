---
title: <add> の <backupList>
ms.date: 03/30/2017
ms.assetid: bc5939fc-314a-4ea4-a533-c96958da7173
ms.openlocfilehash: e61ee275a7e98f13370504f5f15fdbe62a8221bd
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55285793"
---
# <a name="add-of-backuplist"></a><span data-ttu-id="52b83-102">\<add> of \<backupList></span><span class="sxs-lookup"><span data-stu-id="52b83-102">\<add> of \<backupList></span></span>
<span data-ttu-id="52b83-103">バックアップ エンドポイント要素を定義する構成要素を表します。</span><span class="sxs-lookup"><span data-stu-id="52b83-103">Represents a configuration element that defines a backup endpoint element.</span></span>  
  
 <span data-ttu-id="52b83-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="52b83-104">\<system.serviceModel></span></span>  
<span data-ttu-id="52b83-105">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="52b83-105">\<routing></span></span>  
<span data-ttu-id="52b83-106">\<backupLists ></span><span class="sxs-lookup"><span data-stu-id="52b83-106">\<backupLists></span></span>  
<span data-ttu-id="52b83-107">\<backupList></span><span class="sxs-lookup"><span data-stu-id="52b83-107">\<backupList></span></span>  
<span data-ttu-id="52b83-108">\<add></span><span class="sxs-lookup"><span data-stu-id="52b83-108">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52b83-109">構文</span><span class="sxs-lookup"><span data-stu-id="52b83-109">Syntax</span></span>  
  
```xml  
<routing>
  <backupLists>
    <backupList name="String">
      <add endpointName="String" />
    </backupList>
  </backupLists>
</routing>
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="52b83-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="52b83-110">Attributes and Elements</span></span>  
 <span data-ttu-id="52b83-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="52b83-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="52b83-112">属性</span><span class="sxs-lookup"><span data-stu-id="52b83-112">Attributes</span></span>  
  
|<span data-ttu-id="52b83-113">属性</span><span class="sxs-lookup"><span data-stu-id="52b83-113">Attribute</span></span>|<span data-ttu-id="52b83-114">説明</span><span class="sxs-lookup"><span data-stu-id="52b83-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="52b83-115">name</span><span class="sxs-lookup"><span data-stu-id="52b83-115">name</span></span>|<span data-ttu-id="52b83-116">バックアップ エンドポイントの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="52b83-116">A string that specifies the name of the backup endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="52b83-117">子要素</span><span class="sxs-lookup"><span data-stu-id="52b83-117">Child Elements</span></span>  
 <span data-ttu-id="52b83-118">なし。</span><span class="sxs-lookup"><span data-stu-id="52b83-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="52b83-119">親要素</span><span class="sxs-lookup"><span data-stu-id="52b83-119">Parent Elements</span></span>  
  
|<span data-ttu-id="52b83-120">要素</span><span class="sxs-lookup"><span data-stu-id="52b83-120">Element</span></span>|<span data-ttu-id="52b83-121">説明</span><span class="sxs-lookup"><span data-stu-id="52b83-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="52b83-122">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="52b83-122">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="52b83-123">プライマリ エンドポイントに接続できない場合に使用するルーティング サービスが希望されるエンドポイントの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="52b83-123">Contains a list of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="52b83-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="52b83-124">See also</span></span>
- <xref:System.ServiceModel.Routing.Configuration.BackupEndpointElement?displayProperty=nameWithType>
