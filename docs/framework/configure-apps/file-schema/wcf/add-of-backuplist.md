---
title: '&lt;backupList&gt; の &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: bc5939fc-314a-4ea4-a533-c96958da7173
ms.openlocfilehash: 4a8eb3df9be6b6b5bfe43aee330f3174ddca66ab
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151476"
---
# <a name="ltaddgt-of-ltbackuplistgt"></a><span data-ttu-id="39d1f-102">&lt;backupList&gt; の &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="39d1f-102">&lt;add&gt; of &lt;backupList&gt;</span></span>
<span data-ttu-id="39d1f-103">バックアップ エンドポイント要素を定義する構成要素を表します。</span><span class="sxs-lookup"><span data-stu-id="39d1f-103">Represents a configuration element that defines a backup endpoint element.</span></span>  
  
 <span data-ttu-id="39d1f-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="39d1f-104">\<system.serviceModel></span></span>  
<span data-ttu-id="39d1f-105">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="39d1f-105">\<routing></span></span>  
<span data-ttu-id="39d1f-106">\<backupLists ></span><span class="sxs-lookup"><span data-stu-id="39d1f-106">\<backupLists></span></span>  
<span data-ttu-id="39d1f-107">\<backupList ></span><span class="sxs-lookup"><span data-stu-id="39d1f-107">\<backupList></span></span>  
<span data-ttu-id="39d1f-108">\<add></span><span class="sxs-lookup"><span data-stu-id="39d1f-108">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39d1f-109">構文</span><span class="sxs-lookup"><span data-stu-id="39d1f-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="39d1f-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="39d1f-110">Attributes and Elements</span></span>  
 <span data-ttu-id="39d1f-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="39d1f-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="39d1f-112">属性</span><span class="sxs-lookup"><span data-stu-id="39d1f-112">Attributes</span></span>  
  
|<span data-ttu-id="39d1f-113">属性</span><span class="sxs-lookup"><span data-stu-id="39d1f-113">Attribute</span></span>|<span data-ttu-id="39d1f-114">説明</span><span class="sxs-lookup"><span data-stu-id="39d1f-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="39d1f-115">name</span><span class="sxs-lookup"><span data-stu-id="39d1f-115">name</span></span>|<span data-ttu-id="39d1f-116">バックアップ エンドポイントの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="39d1f-116">A string that specifies the name of the backup endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="39d1f-117">子要素</span><span class="sxs-lookup"><span data-stu-id="39d1f-117">Child Elements</span></span>  
 <span data-ttu-id="39d1f-118">なし。</span><span class="sxs-lookup"><span data-stu-id="39d1f-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="39d1f-119">親要素</span><span class="sxs-lookup"><span data-stu-id="39d1f-119">Parent Elements</span></span>  
  
|<span data-ttu-id="39d1f-120">要素</span><span class="sxs-lookup"><span data-stu-id="39d1f-120">Element</span></span>|<span data-ttu-id="39d1f-121">説明</span><span class="sxs-lookup"><span data-stu-id="39d1f-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="39d1f-122">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="39d1f-122">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="39d1f-123">プライマリ エンドポイントに接続できない場合に使用するルーティング サービスが希望されるエンドポイントの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="39d1f-123">Contains a list of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="39d1f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="39d1f-124">See Also</span></span>  
 <xref:System.ServiceModel.Routing.Configuration.BackupEndpointElement?displayProperty=nameWithType> 
