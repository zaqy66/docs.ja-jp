---
title: '&lt;namespaceTable&gt; の &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: cf7b5b75-63bd-49a6-abac-4bfdab377e36
ms.openlocfilehash: ef4f1c46a0ee3b94e5548b752e4e0a6a759fd45b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149515"
---
# <a name="ltaddgt-of-ltnamespacetablegt"></a><span data-ttu-id="79b03-102">&lt;namespaceTable&gt; の &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="79b03-102">&lt;add&gt; of &lt;namespaceTable&gt;</span></span>
<span data-ttu-id="79b03-103">名前空間とプレフィックスのマッピングを含む構成要素を表します。これは、ルーティングの XPath フィルターで使用されます。</span><span class="sxs-lookup"><span data-stu-id="79b03-103">Represents a configuration element that contains a namespace to prefix mapping that can then be used in XPath filters for routing.</span></span>  
  
 <span data-ttu-id="79b03-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="79b03-104">\<system.serviceModel></span></span>  
<span data-ttu-id="79b03-105">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="79b03-105">\<routing></span></span>  
<span data-ttu-id="79b03-106">\<namespaceTable ></span><span class="sxs-lookup"><span data-stu-id="79b03-106">\<namespaceTable></span></span>  
<span data-ttu-id="79b03-107">\<add></span><span class="sxs-lookup"><span data-stu-id="79b03-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79b03-108">構文</span><span class="sxs-lookup"><span data-stu-id="79b03-108">Syntax</span></span>  
  
```xml  
<routing>
  <namespaceTable>
    <add namespace="String"
         prefix="String" />
  </namespaceTable>
</routing>
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="79b03-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="79b03-109">Attributes and Elements</span></span>  
 <span data-ttu-id="79b03-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="79b03-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="79b03-111">属性</span><span class="sxs-lookup"><span data-stu-id="79b03-111">Attributes</span></span>  
  
|<span data-ttu-id="79b03-112">属性</span><span class="sxs-lookup"><span data-stu-id="79b03-112">Attribute</span></span>|<span data-ttu-id="79b03-113">説明</span><span class="sxs-lookup"><span data-stu-id="79b03-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="79b03-114">namespace</span><span class="sxs-lookup"><span data-stu-id="79b03-114">namespace</span></span>|<span data-ttu-id="79b03-115">名前空間を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="79b03-115">A string containing the namespace.</span></span>|  
|<span data-ttu-id="79b03-116">prefix</span><span class="sxs-lookup"><span data-stu-id="79b03-116">prefix</span></span>|<span data-ttu-id="79b03-117">この名前空間のプレフィックスを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="79b03-117">A string containing the prefix for this namespace.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="79b03-118">子要素</span><span class="sxs-lookup"><span data-stu-id="79b03-118">Child Elements</span></span>  
 <span data-ttu-id="79b03-119">なし。</span><span class="sxs-lookup"><span data-stu-id="79b03-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="79b03-120">親要素</span><span class="sxs-lookup"><span data-stu-id="79b03-120">Parent Elements</span></span>  
  
|<span data-ttu-id="79b03-121">要素</span><span class="sxs-lookup"><span data-stu-id="79b03-121">Element</span></span>|<span data-ttu-id="79b03-122">説明</span><span class="sxs-lookup"><span data-stu-id="79b03-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="79b03-123">\<namespaceTable ></span><span class="sxs-lookup"><span data-stu-id="79b03-123">\<namespaceTable></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/namespacetable.md)|<span data-ttu-id="79b03-124">名前空間とプレフィックスのマッピングを含む要素セットを定義する構成セクションを表します。これは、ルーティングの XPath フィルターで使用されます。</span><span class="sxs-lookup"><span data-stu-id="79b03-124">Represents a configuration section for defining a set of elements that contain namespace to prefix mappings that can then be used in XPath filters for routing.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="79b03-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="79b03-125">See Also</span></span>  
 <xref:System.ServiceModel.Routing.Configuration.NamespaceElement?displayProperty=nameWithType>    
