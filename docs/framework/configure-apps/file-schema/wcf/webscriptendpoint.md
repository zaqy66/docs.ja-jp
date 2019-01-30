---
title: <webScriptEndpoint>
ms.date: 03/30/2017
ms.assetid: 85cb5ecf-351b-45f3-aa29-aa2e4b64bcdd
ms.openlocfilehash: 3d95624c82388ed6219fc567dd2d3c17bedad7a1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255290"
---
# <a name="webscriptendpoint"></a><span data-ttu-id="449bc-101">\<webScriptEndpoint></span><span class="sxs-lookup"><span data-stu-id="449bc-101">\<webScriptEndpoint></span></span>
<span data-ttu-id="449bc-102">この構成要素は、固定の標準エンドポイントを定義します。 [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)を自動的にバインドを追加、 [ \<enableWebScript >](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md)動作します。</span><span class="sxs-lookup"><span data-stu-id="449bc-102">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) binding that automatically adds the [\<enableWebScript>](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md) behavior.</span></span> <span data-ttu-id="449bc-103">このエンドポイントは、ASP.NET AJAX アプリケーションから呼び出されるサービスを作成する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="449bc-103">Use this endpoint when you are writing a service that is called from an ASP.NET AJAX application.</span></span>  
  
<span data-ttu-id="449bc-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="449bc-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="449bc-105">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="449bc-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="449bc-106">構文</span><span class="sxs-lookup"><span data-stu-id="449bc-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <webScriptEndpoint>
      <standardEndpoint webEndpointType="String" />
    </webScriptEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="449bc-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="449bc-107">Attributes and Elements</span></span>  
 <span data-ttu-id="449bc-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="449bc-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="449bc-109">属性</span><span class="sxs-lookup"><span data-stu-id="449bc-109">Attributes</span></span>  
  
|<span data-ttu-id="449bc-110">属性</span><span class="sxs-lookup"><span data-stu-id="449bc-110">Attribute</span></span>|<span data-ttu-id="449bc-111">説明</span><span class="sxs-lookup"><span data-stu-id="449bc-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="449bc-112">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="449bc-112">webEndpointType</span></span>|<span data-ttu-id="449bc-113">エンドポイントの種類を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="449bc-113">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="449bc-114">子要素</span><span class="sxs-lookup"><span data-stu-id="449bc-114">Child Elements</span></span>  
 <span data-ttu-id="449bc-115">なし。</span><span class="sxs-lookup"><span data-stu-id="449bc-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="449bc-116">親要素</span><span class="sxs-lookup"><span data-stu-id="449bc-116">Parent Elements</span></span>  
  
|<span data-ttu-id="449bc-117">要素</span><span class="sxs-lookup"><span data-stu-id="449bc-117">Element</span></span>|<span data-ttu-id="449bc-118">説明</span><span class="sxs-lookup"><span data-stu-id="449bc-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="449bc-119">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="449bc-119">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="449bc-120">1 つ以上のプロパティ (アドレス、バインディング、コントラクト) が固定されている、あらかじめ定義されたエンドポイントである標準エンドポイントのコレクション。</span><span class="sxs-lookup"><span data-stu-id="449bc-120">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="449bc-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="449bc-121">See also</span></span>
- <xref:System.ServiceModel.Description.WebScriptEndpoint>
- <xref:System.ServiceModel.Configuration.WebScriptEndpointElement>
