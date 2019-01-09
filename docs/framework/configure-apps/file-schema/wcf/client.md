---
title: '&lt;client&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.ServiceModel/client
- http://schemas.microsoft.com/.NetConfiguration/v2.0#client
ms.assetid: bf0f7031-76c8-4e7e-a6c6-9ad9119134be
ms.openlocfilehash: 24defe7e01603f1b1be3023d07854091335d6c60
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148644"
---
# <a name="ltclientgt"></a><span data-ttu-id="4f15c-102">&lt;client&gt;</span><span class="sxs-lookup"><span data-stu-id="4f15c-102">&lt;client&gt;</span></span>
<span data-ttu-id="4f15c-103">`client` 要素は、クライアントが接続可能なエンドポイントの一覧を定義します。</span><span class="sxs-lookup"><span data-stu-id="4f15c-103">The `client` element defines a list of endpoints that a client can connect to.</span></span>  
  
 <span data-ttu-id="4f15c-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="4f15c-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="4f15c-105">\<client></span><span class="sxs-lookup"><span data-stu-id="4f15c-105">\<client></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f15c-106">構文</span><span class="sxs-lookup"><span data-stu-id="4f15c-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <client>
    <endpoint>
    </endpoint>
    <metadata>
    </metadata>
  </client>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4f15c-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="4f15c-107">Attributes and Elements</span></span>  
 <span data-ttu-id="4f15c-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f15c-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4f15c-109">属性</span><span class="sxs-lookup"><span data-stu-id="4f15c-109">Attributes</span></span>  
 <span data-ttu-id="4f15c-110">なし</span><span class="sxs-lookup"><span data-stu-id="4f15c-110">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4f15c-111">子要素</span><span class="sxs-lookup"><span data-stu-id="4f15c-111">Child Elements</span></span>  
  
|<span data-ttu-id="4f15c-112">要素</span><span class="sxs-lookup"><span data-stu-id="4f15c-112">Element</span></span>|<span data-ttu-id="4f15c-113">説明</span><span class="sxs-lookup"><span data-stu-id="4f15c-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4f15c-114">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="4f15c-114">\<endpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-of-client.md)|<span data-ttu-id="4f15c-115">このクライアントが接続可能なエンドポイントを指定するエンドポイント要素のコレクションを含みます。</span><span class="sxs-lookup"><span data-stu-id="4f15c-115">Contains a collection of endpoint elements, that specify the endpoints that this client can connect to.</span></span>|  
|[<span data-ttu-id="4f15c-116">\<metadata ></span><span class="sxs-lookup"><span data-stu-id="4f15c-116">\<metadata></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/metadata.md)|<span data-ttu-id="4f15c-117">メタデータを処理するための設定を含みます。</span><span class="sxs-lookup"><span data-stu-id="4f15c-117">Contains settings for processing metadata.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4f15c-118">親要素</span><span class="sxs-lookup"><span data-stu-id="4f15c-118">Parent Elements</span></span>  
  
|<span data-ttu-id="4f15c-119">要素</span><span class="sxs-lookup"><span data-stu-id="4f15c-119">Element</span></span>|<span data-ttu-id="4f15c-120">説明</span><span class="sxs-lookup"><span data-stu-id="4f15c-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4f15c-121">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4f15c-121">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="4f15c-122">すべての Windows Communication Foundation (WCF) 構成要素のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="4f15c-122">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4f15c-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="4f15c-123">Remarks</span></span>  
 <span data-ttu-id="4f15c-124">`client` セクションは、クライアントが接続可能なエンドポイントの一覧を定義します。</span><span class="sxs-lookup"><span data-stu-id="4f15c-124">The `client` section defines a list of endpoints that a client can connect to.</span></span> <span data-ttu-id="4f15c-125">クライアント セクションに示される各エンドポイントは、独自のバインディング、動作、およびコントラクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="4f15c-125">Each endpoint listed in the client section defines its own binding, behavior, and contract.</span></span> <span data-ttu-id="4f15c-126">各エンドポイントは、`name` 属性と `contract` 属性の組み合わせで一意に識別されます。</span><span class="sxs-lookup"><span data-stu-id="4f15c-126">It is uniquely identified by the combination of the `name` and `contract` attributes.</span></span> <span data-ttu-id="4f15c-127">クライアント コードは、クライアントが実装するサービスのエンドポイントに接続するための `name` を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f15c-127">The client code specifies the `name` to connect to an endpoint for the service that the client implements.</span></span> <span data-ttu-id="4f15c-128">`name` 属性が省略されている場合、クライアントが実装するコントラクトのエンドポイントが既定のエンドポイントとして機能します。</span><span class="sxs-lookup"><span data-stu-id="4f15c-128">If the `name` attribute is omitted, the endpoint acts as the default endpoint for the contract it implements.</span></span>  
  
 <span data-ttu-id="4f15c-129">さらに、このセクションはメタデータを処理するための設定も指定します。</span><span class="sxs-lookup"><span data-stu-id="4f15c-129">In addition, this section also specifies settings for processing metadata.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4f15c-130">例</span><span class="sxs-lookup"><span data-stu-id="4f15c-130">Example</span></span>  
  
```xml  
<client>
  <endpoint address="/HelloWorld/"
            bindingConfiguration="usingDefaults"
            name="MyBinding"
            binding="customBinding"
            contract="HelloWorld">
    <addressProperties actingAs="http://www.microsoft.com/TestActor"
                       identityData="BasicReadWrite"
                       identityType="Spn"
                       isAddressPrivate="false">
  </endpoint>
</client>
```  
  
## <a name="see-also"></a><span data-ttu-id="4f15c-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f15c-131">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ClientSection>  
 <xref:System.ServiceModel.Configuration.MetadataElement>  
 [<span data-ttu-id="4f15c-132">WCF クライアントの構成</span><span class="sxs-lookup"><span data-stu-id="4f15c-132">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)  
 [<span data-ttu-id="4f15c-133">クライアント</span><span class="sxs-lookup"><span data-stu-id="4f15c-133">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
