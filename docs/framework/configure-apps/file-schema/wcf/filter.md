---
title: <filter>
ms.date: 03/30/2017
ms.assetid: 3266700b-904b-44e4-93a7-e06a1a445100
ms.openlocfilehash: bff19f106d86c73dea80b8b57bb73442eaa2cf9f
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278786"
---
# <a name="filter"></a><span data-ttu-id="650e5-101">\<フィルター ></span><span class="sxs-lookup"><span data-stu-id="650e5-101">\<filter></span></span>

<span data-ttu-id="650e5-102">Windows Communication Foundation (WCF) の型を決定するルーティング フィルターを定義します。<xref:System.ServiceModel.Dispatcher.MessageFilter>も任意のサポート データまたはフィルターに必要なパラメーターとして、受信メッセージを評価するときに使用します。</span><span class="sxs-lookup"><span data-stu-id="650e5-102">Defines a routing filter, which determines the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well any supporting data or parameters required by the filter.</span></span>

<span data-ttu-id="650e5-103">\<system.serviceModel> \<routing> \<filters> \<filter></span><span class="sxs-lookup"><span data-stu-id="650e5-103">\<system.serviceModel> \<routing> \<filters> \<filter></span></span>
  
## <a name="syntax"></a><span data-ttu-id="650e5-104">構文</span><span class="sxs-lookup"><span data-stu-id="650e5-104">Syntax</span></span>  
  
```xml  
<routing>
  <filters>
    <filter customType="String"
            filterData="String"
            filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
            name="String" />
  </filters>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="650e5-105">属性と要素</span><span class="sxs-lookup"><span data-stu-id="650e5-105">Attributes and elements</span></span>

<span data-ttu-id="650e5-106">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="650e5-106">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="650e5-107">属性</span><span class="sxs-lookup"><span data-stu-id="650e5-107">Attributes</span></span>

| <span data-ttu-id="650e5-108">属性</span><span class="sxs-lookup"><span data-stu-id="650e5-108">Attribute</span></span>  | <span data-ttu-id="650e5-109">説明</span><span class="sxs-lookup"><span data-stu-id="650e5-109">Description</span></span> |
| ---------- | ----------- |
| <span data-ttu-id="650e5-110">customType</span><span class="sxs-lookup"><span data-stu-id="650e5-110">customType</span></span> | <span data-ttu-id="650e5-111">フィルターとして使用されるカスタム型の完全修飾型名を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="650e5-111">A string containing the fully qualified type name of the custom type to be used as a filter.</span></span> <span data-ttu-id="650e5-112">場合`filterType`に設定されている`custom`、この属性には作成するクラスの完全修飾型名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="650e5-112">If `filterType` is set to `custom`, this attribute contains the fully qualified type name of the class to create.</span></span>  <span data-ttu-id="650e5-113">`filterData` カスタム型フィルターの評価時に使用する値を含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="650e5-113">`filterData` may also contain values to be used during evaluation of the custom type filter.</span></span> |
| <span data-ttu-id="650e5-114">filterData</span><span class="sxs-lookup"><span data-stu-id="650e5-114">filterData</span></span> | <span data-ttu-id="650e5-115">フィルター データを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="650e5-115">A string containing the filter data.</span></span> <span data-ttu-id="650e5-116">この属性を指定する方法の詳細については、「<xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="650e5-116">For more information on how to specify this attribute, see <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span></span> |
| <span data-ttu-id="650e5-117">filterType</span><span class="sxs-lookup"><span data-stu-id="650e5-117">filterType</span></span> | <span data-ttu-id="650e5-118">フィルターの種類を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="650e5-118">A string containing the filter type.</span></span> <span data-ttu-id="650e5-119">この属性は <xref:System.ServiceModel.Routing.Configuration.FilterType> 型です。</span><span class="sxs-lookup"><span data-stu-id="650e5-119">This attribute is of <xref:System.ServiceModel.Routing.Configuration.FilterType> type.</span></span>  <span data-ttu-id="650e5-120">`filterData` 属性を使用する方法の詳細については、「<xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="650e5-120">For more information on how this works with the `filterData` attribute, see <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span></span> |
| <span data-ttu-id="650e5-121">name</span><span class="sxs-lookup"><span data-stu-id="650e5-121">name</span></span>       | <span data-ttu-id="650e5-122">フィルター要素の一意の名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="650e5-122">A string containing the unique name of this filter element.</span></span> |

### <a name="child-elements"></a><span data-ttu-id="650e5-123">子要素</span><span class="sxs-lookup"><span data-stu-id="650e5-123">Child elements</span></span>

<span data-ttu-id="650e5-124">なし。</span><span class="sxs-lookup"><span data-stu-id="650e5-124">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="650e5-125">親要素</span><span class="sxs-lookup"><span data-stu-id="650e5-125">Parent elements</span></span>

| <span data-ttu-id="650e5-126">要素</span><span class="sxs-lookup"><span data-stu-id="650e5-126">Element</span></span> | <span data-ttu-id="650e5-127">説明</span><span class="sxs-lookup"><span data-stu-id="650e5-127">Description</span></span> |
| ------- | ----------- |
| [<span data-ttu-id="650e5-128">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="650e5-128">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md) | <span data-ttu-id="650e5-129">Windows Communication Foundation (WCF) の種類を指定するルーティング フィルター セットを定義する構成セクション<xref:System.ServiceModel.Dispatcher.MessageFilter>受信メッセージを評価するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="650e5-129">A configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages.</span></span> |

## <a name="see-also"></a><span data-ttu-id="650e5-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="650e5-130">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.FilterElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterType?displayProperty=nameWithType>
