---
title: '&lt;webHttpEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: ecaaeb6f-ebd0-411d-8b53-92477cd45347
ms.openlocfilehash: ee14ce23370675782f4c25385c1786fdce11eba0
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151970"
---
# <a name="ltwebhttpendpointgt"></a><span data-ttu-id="3dc9b-102">&lt;webHttpEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="3dc9b-102">&lt;webHttpEndpoint&gt;</span></span>
<span data-ttu-id="3dc9b-103">この構成要素は、固定の標準エンドポイントを定義します。 [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)を自動的にバインドを追加、 [ \<webHttp >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md)動作します。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-103">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) binding that automatically adds the [\<webHttp>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md) behavior.</span></span> <span data-ttu-id="3dc9b-104">このエンドポイントは、REST サービスを作成する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-104">Use this endpoint when writing a REST service.</span></span>  
  
<span data-ttu-id="3dc9b-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="3dc9b-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="3dc9b-106">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="3dc9b-106">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3dc9b-107">構文</span><span class="sxs-lookup"><span data-stu-id="3dc9b-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <webHttpEndpoint>
      <standardEndpoint automaticFormatSelectionEnabled="String"
                        defaultOutgoingResponseFormat="Xml/Json"
                        helpEnabled="Boolean"
                        webEndpointType="String" />
    </webHttpEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3dc9b-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="3dc9b-108">Attributes and Elements</span></span>  
 <span data-ttu-id="3dc9b-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3dc9b-110">属性</span><span class="sxs-lookup"><span data-stu-id="3dc9b-110">Attributes</span></span>  
  
|<span data-ttu-id="3dc9b-111">属性</span><span class="sxs-lookup"><span data-stu-id="3dc9b-111">Attribute</span></span>|<span data-ttu-id="3dc9b-112">説明</span><span class="sxs-lookup"><span data-stu-id="3dc9b-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3dc9b-113">automaticFormatSelectionEnabled</span><span class="sxs-lookup"><span data-stu-id="3dc9b-113">automaticFormatSelectionEnabled</span></span>|<span data-ttu-id="3dc9b-114">形式の自動選択が有効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-114">A Boolean value that indicates whether automatic format selection is enabled.</span></span><br /><br /> <span data-ttu-id="3dc9b-115">形式の自動選択が有効な場合、インフラストラクチャが要求メッセージの `Accept` ヘッダーを解析し、最適な応答形式を判断します。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-115">When automatic format selection is enabled, the infrastructure parses the `Accept` header of the request message and determines the most appropriate response format.</span></span> <span data-ttu-id="3dc9b-116">適切な応答形式が `Accept` ヘッダーに指定されていなかった場合は、要求メッセージの `Content-Type` または操作の既定の応答形式がインフラストラクチャによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-116">If the `Accept` header does not specify a suitable response format, the infrastructure uses the `Content-Type` of the request message or the default response format of the operation.</span></span>|  
|<span data-ttu-id="3dc9b-117">defaultOutgoingResponseFormat</span><span class="sxs-lookup"><span data-stu-id="3dc9b-117">defaultOutgoingResponseFormat</span></span>|<span data-ttu-id="3dc9b-118">既定の送信応答形式を指定する属性。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-118">An attribute that specifies the default outgoing response format.</span></span> <span data-ttu-id="3dc9b-119">この属性は <xref:System.ServiceModel.Web.WebMessageFormat> 型です。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-119">This attribute is of the <xref:System.ServiceModel.Web.WebMessageFormat> type</span></span>|  
|<span data-ttu-id="3dc9b-120">helpEnabled</span><span class="sxs-lookup"><span data-stu-id="3dc9b-120">helpEnabled</span></span>|<span data-ttu-id="3dc9b-121">エンドポイントに対して HTTP ヘルプ ページが有効になっているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-121">A Boolean value that indicates whether the HTTP help page is enabled for the endpoint.</span></span>|  
|<span data-ttu-id="3dc9b-122">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="3dc9b-122">webEndpointType</span></span>|<span data-ttu-id="3dc9b-123">エンドポイントの種類を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-123">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3dc9b-124">子要素</span><span class="sxs-lookup"><span data-stu-id="3dc9b-124">Child Elements</span></span>  
 <span data-ttu-id="3dc9b-125">なし。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-125">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3dc9b-126">親要素</span><span class="sxs-lookup"><span data-stu-id="3dc9b-126">Parent Elements</span></span>  
  
|<span data-ttu-id="3dc9b-127">要素</span><span class="sxs-lookup"><span data-stu-id="3dc9b-127">Element</span></span>|<span data-ttu-id="3dc9b-128">説明</span><span class="sxs-lookup"><span data-stu-id="3dc9b-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3dc9b-129">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="3dc9b-129">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="3dc9b-130">1 つ以上のプロパティ (アドレス、バインディング、コントラクト) が固定されている、あらかじめ定義されたエンドポイントである標準エンドポイントのコレクション。</span><span class="sxs-lookup"><span data-stu-id="3dc9b-130">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3dc9b-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="3dc9b-131">See Also</span></span>  
 <xref:System.ServiceModel.Description.WebHttpEndpoint>  
 <xref:System.ServiceModel.Configuration.WebHttpEndpointElement>
