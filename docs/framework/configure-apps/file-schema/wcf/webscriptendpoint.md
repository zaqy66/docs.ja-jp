---
title: '&lt;webScriptEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: 85cb5ecf-351b-45f3-aa29-aa2e4b64bcdd
ms.openlocfilehash: beb17d4ccc39bcca30e97d4f0df47c797cde6216
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148774"
---
# <a name="ltwebscriptendpointgt"></a><span data-ttu-id="8cf49-102">&lt;webScriptEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="8cf49-102">&lt;webScriptEndpoint&gt;</span></span>
<span data-ttu-id="8cf49-103">この構成要素は、固定の標準エンドポイントを定義します。 [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)を自動的にバインドを追加、 [ \<enableWebScript >](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md)動作します。</span><span class="sxs-lookup"><span data-stu-id="8cf49-103">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) binding that automatically adds the [\<enableWebScript>](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md) behavior.</span></span> <span data-ttu-id="8cf49-104">このエンドポイントは、ASP.NET AJAX アプリケーションから呼び出されるサービスを作成する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="8cf49-104">Use this endpoint when you are writing a service that is called from an ASP.NET AJAX application.</span></span>  
  
<span data-ttu-id="8cf49-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="8cf49-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="8cf49-106">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="8cf49-106">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8cf49-107">構文</span><span class="sxs-lookup"><span data-stu-id="8cf49-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <webScriptEndpoint>
      <standardEndpoint webEndpointType="String" />
    </webScriptEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8cf49-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="8cf49-108">Attributes and Elements</span></span>  
 <span data-ttu-id="8cf49-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="8cf49-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8cf49-110">属性</span><span class="sxs-lookup"><span data-stu-id="8cf49-110">Attributes</span></span>  
  
|<span data-ttu-id="8cf49-111">属性</span><span class="sxs-lookup"><span data-stu-id="8cf49-111">Attribute</span></span>|<span data-ttu-id="8cf49-112">説明</span><span class="sxs-lookup"><span data-stu-id="8cf49-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8cf49-113">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="8cf49-113">webEndpointType</span></span>|<span data-ttu-id="8cf49-114">エンドポイントの種類を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="8cf49-114">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8cf49-115">子要素</span><span class="sxs-lookup"><span data-stu-id="8cf49-115">Child Elements</span></span>  
 <span data-ttu-id="8cf49-116">なし。</span><span class="sxs-lookup"><span data-stu-id="8cf49-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8cf49-117">親要素</span><span class="sxs-lookup"><span data-stu-id="8cf49-117">Parent Elements</span></span>  
  
|<span data-ttu-id="8cf49-118">要素</span><span class="sxs-lookup"><span data-stu-id="8cf49-118">Element</span></span>|<span data-ttu-id="8cf49-119">説明</span><span class="sxs-lookup"><span data-stu-id="8cf49-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8cf49-120">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="8cf49-120">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="8cf49-121">1 つ以上のプロパティ (アドレス、バインディング、コントラクト) が固定されている、あらかじめ定義されたエンドポイントである標準エンドポイントのコレクション。</span><span class="sxs-lookup"><span data-stu-id="8cf49-121">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8cf49-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="8cf49-122">See Also</span></span>  
 <xref:System.ServiceModel.Description.WebScriptEndpoint>  
 <xref:System.ServiceModel.Configuration.WebScriptEndpointElement>
