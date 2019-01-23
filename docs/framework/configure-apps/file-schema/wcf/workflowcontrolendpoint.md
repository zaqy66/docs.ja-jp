---
title: '&lt;workflowControlEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: 6c89e76c-643b-4b6a-9b25-628f753d7027
ms.openlocfilehash: 9c641d4081d88b059e1d778f6383f85c064af7f0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54558671"
---
# <a name="ltworkflowcontrolendpointgt"></a><span data-ttu-id="61ce0-102">&lt;workflowControlEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="61ce0-102">&lt;workflowControlEndpoint&gt;</span></span>
<span data-ttu-id="61ce0-103">この構成要素は、ワークフロー インスタンスの実行の制御 (作成、実行、保留、終了など) に使用する標準エンドポイントを定義します。</span><span class="sxs-lookup"><span data-stu-id="61ce0-103">This configuration element defines a standard endpoint for controlling the execution of workflow instances (create, run, suspend, terminate, etc).</span></span>  
  
<span data-ttu-id="61ce0-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="61ce0-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="61ce0-105">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="61ce0-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61ce0-106">構文</span><span class="sxs-lookup"><span data-stu-id="61ce0-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <workflowControlEndpoint>
      <standardEndpoint name="String" />
    </workflowControlEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="61ce0-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="61ce0-107">Attributes and Elements</span></span>  
 <span data-ttu-id="61ce0-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="61ce0-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="61ce0-109">属性</span><span class="sxs-lookup"><span data-stu-id="61ce0-109">Attributes</span></span>  
  
|<span data-ttu-id="61ce0-110">属性</span><span class="sxs-lookup"><span data-stu-id="61ce0-110">Attribute</span></span>|<span data-ttu-id="61ce0-111">説明</span><span class="sxs-lookup"><span data-stu-id="61ce0-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="61ce0-112">name</span><span class="sxs-lookup"><span data-stu-id="61ce0-112">name</span></span>|<span data-ttu-id="61ce0-113">標準エンドポイントの構成名を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="61ce0-113">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="61ce0-114">この名前は、サービス エンドポイントの `endpointConfiguration` 属性で使用され、標準エンドポイントと構成を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="61ce0-114">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="61ce0-115">子要素</span><span class="sxs-lookup"><span data-stu-id="61ce0-115">Child Elements</span></span>  
 <span data-ttu-id="61ce0-116">なし。</span><span class="sxs-lookup"><span data-stu-id="61ce0-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="61ce0-117">親要素</span><span class="sxs-lookup"><span data-stu-id="61ce0-117">Parent Elements</span></span>  
  
|<span data-ttu-id="61ce0-118">要素</span><span class="sxs-lookup"><span data-stu-id="61ce0-118">Element</span></span>|<span data-ttu-id="61ce0-119">説明</span><span class="sxs-lookup"><span data-stu-id="61ce0-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="61ce0-120">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="61ce0-120">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="61ce0-121">1 つ以上のプロパティ (アドレス、バインディング、コントラクト) が固定されている、あらかじめ定義されたエンドポイントである標準エンドポイントのコレクション。</span><span class="sxs-lookup"><span data-stu-id="61ce0-121">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="61ce0-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="61ce0-122">See also</span></span>
- <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>
