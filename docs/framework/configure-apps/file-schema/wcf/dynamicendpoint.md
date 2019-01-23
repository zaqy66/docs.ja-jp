---
title: '&lt;dynamicEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: 929f223d-176d-4205-9505-234ddb6dbff4
ms.openlocfilehash: dcb52143c874b14c9241940f9b326a07b3fa6a82
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54540254"
---
# <a name="ltdynamicendpointgt"></a><span data-ttu-id="42b64-102">&lt;dynamicEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="42b64-102">&lt;dynamicEndpoint&gt;</span></span>
<span data-ttu-id="42b64-103">この構成要素は、アプリケーションが、実行時に動的にエンドポイント アドレスを検索するクライアント プログラムとして機能するための情報を格納する標準エンドポイントを定義します。</span><span class="sxs-lookup"><span data-stu-id="42b64-103">This configuration element defines a standard endpoint that contains information to enable an application to function as a client program that can find the endpoint address dynamically at runtime.</span></span>  
  
<span data-ttu-id="42b64-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="42b64-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="42b64-105">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="42b64-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42b64-106">構文</span><span class="sxs-lookup"><span data-stu-id="42b64-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <dynamicEndpoint>
      <standardEndpoint>
        <discoveryClientSettings discoveryEndpoint="String">
          <findCriteria duration="TimeSpan"
                        maxResults="Integer"
                        scopeMatchBy="Uri">
            <contractTypeNames>
              <add name="String"
                   namespace="String" />
            <contractTypeNames>
            <extensions />
            <scopes>
              <add scope="URI" />
            </scopes>
          </findCriteria>
        </discoveryClientSettings>
      <standardEndpoint>
    </dynamicEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="42b64-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="42b64-107">Attributes and Elements</span></span>  
 <span data-ttu-id="42b64-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="42b64-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="42b64-109">属性</span><span class="sxs-lookup"><span data-stu-id="42b64-109">Attributes</span></span>  
 <span data-ttu-id="42b64-110">なし。</span><span class="sxs-lookup"><span data-stu-id="42b64-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="42b64-111">子要素</span><span class="sxs-lookup"><span data-stu-id="42b64-111">Child Elements</span></span>  
  
|<span data-ttu-id="42b64-112">要素</span><span class="sxs-lookup"><span data-stu-id="42b64-112">Element</span></span>|<span data-ttu-id="42b64-113">説明</span><span class="sxs-lookup"><span data-stu-id="42b64-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="42b64-114">\<discoveryClientSettings></span><span class="sxs-lookup"><span data-stu-id="42b64-114">\<discoveryClientSettings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryclientsettings.md)|<span data-ttu-id="42b64-115">サービス探索プロセスにクライアントとして参加するためにアプリケーションが必要とする設定を格納します。</span><span class="sxs-lookup"><span data-stu-id="42b64-115">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="42b64-116">親要素</span><span class="sxs-lookup"><span data-stu-id="42b64-116">Parent Elements</span></span>  
  
|<span data-ttu-id="42b64-117">要素</span><span class="sxs-lookup"><span data-stu-id="42b64-117">Element</span></span>|<span data-ttu-id="42b64-118">説明</span><span class="sxs-lookup"><span data-stu-id="42b64-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="42b64-119">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="42b64-119">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="42b64-120">1 つ以上のプロパティ (アドレス、バインディング、コントラクト) が固定されている、あらかじめ定義されたエンドポイントである標準エンドポイントのコレクション。</span><span class="sxs-lookup"><span data-stu-id="42b64-120">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="42b64-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="42b64-121">See also</span></span>
- <xref:System.ServiceModel.Discovery.DynamicEndpoint>
- <xref:System.ServiceModel.Discovery.Configuration.DynamicEndpointElement>
