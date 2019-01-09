---
title: '&lt;system.runtime.serialization&gt; の &lt;dataContractSerializer&gt;'
ms.date: 03/30/2017
ms.assetid: d9b3d625-be3f-4768-8e0d-1b7e6929f6a8
ms.openlocfilehash: f31dd8479f3bd6b36915b3ff00ff53babe3c0248
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150176"
---
# <a name="ltdatacontractserializergt-of-ltsystemruntimeserializationgt"></a><span data-ttu-id="84fc6-102">&lt;system.runtime.serialization&gt; の &lt;dataContractSerializer&gt;</span><span class="sxs-lookup"><span data-stu-id="84fc6-102">&lt;dataContractSerializer&gt; of &lt;system.runtime.serialization&gt;</span></span>
<span data-ttu-id="84fc6-103"><xref:System.Runtime.Serialization.DataContractSerializer> 用の設定データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="84fc6-103">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="84fc6-104">\<system.runtime.serialization ></span><span class="sxs-lookup"><span data-stu-id="84fc6-104">\<system.runtime.serialization></span></span>  
<span data-ttu-id="84fc6-105">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="84fc6-105">\<dataContractSerializer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84fc6-106">構文</span><span class="sxs-lookup"><span data-stu-id="84fc6-106">Syntax</span></span>  
  
```xml  
<configuration>
  <system.runtime.serialization>
    <dataContractSerializer ignoreExtensionDataObject="Boolean"
                            maxItemsInObjectGraph="Integer">
      <declaredTypes>
        <add type="String">
          <knownType type="String">
            <parameter index="Integer"
                       type="String" />
          </knownType>
        </add>
      </declaredTypes>
    <dataContractSerializer>
  </system.runtime.serialization>
</configuration>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="84fc6-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="84fc6-107">Attributes and Elements</span></span>  
 <span data-ttu-id="84fc6-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="84fc6-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="84fc6-109">属性</span><span class="sxs-lookup"><span data-stu-id="84fc6-109">Attributes</span></span>  
  
|<span data-ttu-id="84fc6-110">要素</span><span class="sxs-lookup"><span data-stu-id="84fc6-110">Element</span></span>|<span data-ttu-id="84fc6-111">説明</span><span class="sxs-lookup"><span data-stu-id="84fc6-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="84fc6-112">ignoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="84fc6-112">ignoreExtensionDataObject</span></span>|<span data-ttu-id="84fc6-113">エンドポイントがシリアル化または逆シリアル化されているときに、そのエンドポイントにより提供されるデータを無視するかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="84fc6-113">A Boolean value that specifies whether to ignore data supplied by the endpoint when it is being serialized or deserialized.</span></span> <span data-ttu-id="84fc6-114">この属性は、`<dataContractSerializer>` 要素の下の `<behavior>` でのみ設定可能です。</span><span class="sxs-lookup"><span data-stu-id="84fc6-114">This attribute is settable only on the `<dataContractSerializer>` under the `<behavior>` element.</span></span>|  
|<span data-ttu-id="84fc6-115">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="84fc6-115">maxItemsInObjectGraph</span></span>|<span data-ttu-id="84fc6-116">シリアル化または逆シリアル化する項目の最大数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="84fc6-116">An integer that specifies the maximum number of items to serialize or deserialize.</span></span> <span data-ttu-id="84fc6-117">この属性は 65536 です。</span><span class="sxs-lookup"><span data-stu-id="84fc6-117">This attribute is 65536.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="84fc6-118">子要素</span><span class="sxs-lookup"><span data-stu-id="84fc6-118">Child Elements</span></span>  
  
|<span data-ttu-id="84fc6-119">要素</span><span class="sxs-lookup"><span data-stu-id="84fc6-119">Element</span></span>|<span data-ttu-id="84fc6-120">説明</span><span class="sxs-lookup"><span data-stu-id="84fc6-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="84fc6-121">\<declaredTypes ></span><span class="sxs-lookup"><span data-stu-id="84fc6-121">\<declaredTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/declaredtypes.md)|<span data-ttu-id="84fc6-122">逆シリアル化時に <xref:System.Runtime.Serialization.DataContractSerializer> が使用する既知の型が含まれています。</span><span class="sxs-lookup"><span data-stu-id="84fc6-122">Contains the known types that the <xref:System.Runtime.Serialization.DataContractSerializer> uses when deserializing.</span></span><br /><br /> <span data-ttu-id="84fc6-123">データ コントラクトと既知の型の詳細については、次を参照してください。 [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)します。</span><span class="sxs-lookup"><span data-stu-id="84fc6-123">For more information about data contracts and known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="84fc6-124">親要素</span><span class="sxs-lookup"><span data-stu-id="84fc6-124">Parent Elements</span></span>  
  
|<span data-ttu-id="84fc6-125">要素</span><span class="sxs-lookup"><span data-stu-id="84fc6-125">Element</span></span>|<span data-ttu-id="84fc6-126">説明</span><span class="sxs-lookup"><span data-stu-id="84fc6-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="84fc6-127">\<system.runtime.serialization ></span><span class="sxs-lookup"><span data-stu-id="84fc6-127">\<system.runtime.serialization></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)|<span data-ttu-id="84fc6-128"><xref:System.Runtime.Serialization> 名前空間セクションのルート要素を表し、<xref:System.Runtime.Serialization.DataContractSerializer> のオプションを設定するための要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="84fc6-128">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="84fc6-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="84fc6-129">Remarks</span></span>  
 <span data-ttu-id="84fc6-130">既知の型の詳細については、次を参照してください。<xref:System.Runtime.Serialization.DataContractSerializer>と[Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)します。</span><span class="sxs-lookup"><span data-stu-id="84fc6-130">For more information about known types, see <xref:System.Runtime.Serialization.DataContractSerializer> and [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84fc6-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="84fc6-131">See Also</span></span>  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
 <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>  
 [<span data-ttu-id="84fc6-132">既知のデータ コントラクト型</span><span class="sxs-lookup"><span data-stu-id="84fc6-132">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
