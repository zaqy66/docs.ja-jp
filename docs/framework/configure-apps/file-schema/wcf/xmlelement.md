---
title: '&lt;xmlElement&gt;'
ms.date: 03/30/2017
ms.assetid: 395205c2-d8c0-4a5e-90f3-7ce3c085fccd
ms.openlocfilehash: 40703bdf62e8c69ac7e09a0d715e2a2f99408680
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54612282"
---
# <a name="ltxmlelementgt"></a><span data-ttu-id="b07c5-102">&lt;xmlElement&gt;</span><span class="sxs-lookup"><span data-stu-id="b07c5-102">&lt;xmlElement&gt;</span></span>
<span data-ttu-id="b07c5-103">トークンの要求時にセキュリティ トークン サービスへのメッセージ本文で送信される XML 要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="b07c5-103">Specifies an XML element that is sent in the message body to the Security Token Service when requesting a token.</span></span>  
  
 <span data-ttu-id="b07c5-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="b07c5-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="b07c5-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="b07c5-105">\<bindings></span></span>  
<span data-ttu-id="b07c5-106">\<wsFederatedBinding></span><span class="sxs-lookup"><span data-stu-id="b07c5-106">\<wsFederatedBinding></span></span>  
<span data-ttu-id="b07c5-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="b07c5-107">\<binding></span></span>  
<span data-ttu-id="b07c5-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="b07c5-108">\<security></span></span>  
<span data-ttu-id="b07c5-109">\<message></span><span class="sxs-lookup"><span data-stu-id="b07c5-109">\<message></span></span>  
<span data-ttu-id="b07c5-110">\<tokenRequestParameters></span><span class="sxs-lookup"><span data-stu-id="b07c5-110">\<tokenRequestParameters></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b07c5-111">構文</span><span class="sxs-lookup"><span data-stu-id="b07c5-111">Syntax</span></span>  
  
```xml  
<tokenRequestParameters>
  <xmlElement xmlElement="String" />
</tokenRequestParameters>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b07c5-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="b07c5-112">Attributes and Elements</span></span>  
 <span data-ttu-id="b07c5-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="b07c5-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b07c5-114">属性</span><span class="sxs-lookup"><span data-stu-id="b07c5-114">Attributes</span></span>  
  
|<span data-ttu-id="b07c5-115">属性</span><span class="sxs-lookup"><span data-stu-id="b07c5-115">Attribute</span></span>|<span data-ttu-id="b07c5-116">説明</span><span class="sxs-lookup"><span data-stu-id="b07c5-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b07c5-117">xmlElement</span><span class="sxs-lookup"><span data-stu-id="b07c5-117">xmlElement</span></span>|<span data-ttu-id="b07c5-118">トークンの要求時にセキュリティ トークン サービスへのメッセージ本文で送信される XML 要素を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="b07c5-118">A string specifying an XML element that is sent in the message body to the Security Token Service when requesting a token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b07c5-119">子要素</span><span class="sxs-lookup"><span data-stu-id="b07c5-119">Child Elements</span></span>  
 <span data-ttu-id="b07c5-120">なし。</span><span class="sxs-lookup"><span data-stu-id="b07c5-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b07c5-121">親要素</span><span class="sxs-lookup"><span data-stu-id="b07c5-121">Parent Elements</span></span>  
  
|<span data-ttu-id="b07c5-122">要素</span><span class="sxs-lookup"><span data-stu-id="b07c5-122">Element</span></span>|<span data-ttu-id="b07c5-123">説明</span><span class="sxs-lookup"><span data-stu-id="b07c5-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b07c5-124">\<tokenRequestParameters></span><span class="sxs-lookup"><span data-stu-id="b07c5-124">\<tokenRequestParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/tokenrequestparameters.md)|<span data-ttu-id="b07c5-125">トークン要求パラメーターのコレクション。</span><span class="sxs-lookup"><span data-stu-id="b07c5-125">A collection of token request parameters.</span></span> <span data-ttu-id="b07c5-126">各パラメーターは、XML 要素です。</span><span class="sxs-lookup"><span data-stu-id="b07c5-126">Each parameter is an XML element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b07c5-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="b07c5-127">See also</span></span>
- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.TokenRequestParameters%2A>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.TokenRequestParameters%2A>
- [<span data-ttu-id="b07c5-128">サービス ID と認証</span><span class="sxs-lookup"><span data-stu-id="b07c5-128">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="b07c5-129">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="b07c5-129">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="b07c5-130">カスタム バインドを使用したセキュリティ機能</span><span class="sxs-lookup"><span data-stu-id="b07c5-130">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="b07c5-131">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="b07c5-131">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="b07c5-132">バインディング</span><span class="sxs-lookup"><span data-stu-id="b07c5-132">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
