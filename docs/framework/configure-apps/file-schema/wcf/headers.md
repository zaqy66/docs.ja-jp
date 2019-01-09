---
title: '&lt;header&gt;'
ms.date: 03/30/2017
ms.assetid: c79b897d-8ea3-40b5-a8b6-2471941f7ed3
ms.openlocfilehash: 84b9a9437d4b0dfae72a6e625b21f2b830eb28d8
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147864"
---
# <a name="ltheadersgt"></a><span data-ttu-id="72570-102">&lt;header&gt;</span><span class="sxs-lookup"><span data-stu-id="72570-102">&lt;headers&gt;</span></span>
<span data-ttu-id="72570-103">エンドポイントは、基本となる URI だけでなく、1 つ以上の SOAP ヘッダーによってアドレス指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="72570-103">An endpoint can be addressed by one or more SOAP headers in addition to its basic URI.</span></span> <span data-ttu-id="72570-104">これが役に立つのは、エンドポイントのクライアントに中継局を指す SOAP ヘッダーを含める必要がある、SOAP 中継局のシナリオの場合です。</span><span class="sxs-lookup"><span data-stu-id="72570-104">One set of scenarios where this is useful is a set of SOAP intermediary scenarios where an endpoint requires clients of that endpoint to include SOAP headers targeted at intermediaries.</span></span> <span data-ttu-id="72570-105">この構成要素を使用して、カスタムのアドレス ヘッダーを定義できます。</span><span class="sxs-lookup"><span data-stu-id="72570-105">This configuration element can be used to define such custom address headers.</span></span> <span data-ttu-id="72570-106">エンドポイント ヘッダー コレクション内のエントリは、ユーザー定義の XML 要素です。</span><span class="sxs-lookup"><span data-stu-id="72570-106">Entries in the endpoint header collection are user-defined XML elements.</span></span> <span data-ttu-id="72570-107">各要素は、正しい形式の XML である必要があります。</span><span class="sxs-lookup"><span data-stu-id="72570-107">Each element has to be well-formed XML.</span></span>  
  
 <span data-ttu-id="72570-108">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="72570-108">\<system.ServiceModel></span></span>  
<span data-ttu-id="72570-109">\<client></span><span class="sxs-lookup"><span data-stu-id="72570-109">\<client></span></span>  
<span data-ttu-id="72570-110">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="72570-110">\<endpoint></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72570-111">構文</span><span class="sxs-lookup"><span data-stu-id="72570-111">Syntax</span></span>  
  
```xml  
<headers>
  <region xmlns="Uri">"String"</region>
  <member xmlns="Uri">"String"</member>
</headers>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="72570-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="72570-112">Attributes and Elements</span></span>  
 <span data-ttu-id="72570-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="72570-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="72570-114">属性</span><span class="sxs-lookup"><span data-stu-id="72570-114">Attributes</span></span>  
 <span data-ttu-id="72570-115">なし。</span><span class="sxs-lookup"><span data-stu-id="72570-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="72570-116">子要素</span><span class="sxs-lookup"><span data-stu-id="72570-116">Child Elements</span></span>  
  
|<span data-ttu-id="72570-117">要素</span><span class="sxs-lookup"><span data-stu-id="72570-117">Element</span></span>|<span data-ttu-id="72570-118">説明</span><span class="sxs-lookup"><span data-stu-id="72570-118">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="72570-119">Region</span><span class="sxs-lookup"><span data-stu-id="72570-119">Region</span></span>||  
|<span data-ttu-id="72570-120">メンバー</span><span class="sxs-lookup"><span data-stu-id="72570-120">Member</span></span>||  
  
### <a name="parent-elements"></a><span data-ttu-id="72570-121">親要素</span><span class="sxs-lookup"><span data-stu-id="72570-121">Parent Elements</span></span>  
  
|<span data-ttu-id="72570-122">要素</span><span class="sxs-lookup"><span data-stu-id="72570-122">Element</span></span>|<span data-ttu-id="72570-123">説明</span><span class="sxs-lookup"><span data-stu-id="72570-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="72570-124">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="72570-124">\<endpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-of-client.md)|<span data-ttu-id="72570-125">さまざまなタイプのエンドポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="72570-125">Configures different types of endpoints.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="72570-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="72570-126">Remarks</span></span>  
 <span data-ttu-id="72570-127">オプション ヘッダーは、エンドポイントの識別または対話のために、より詳細なアドレス指定情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="72570-127">The optional headers provide more detailed addressing information to identify or interact with the endpoint.</span></span> <span data-ttu-id="72570-128">たとえば、ヘッダーを使用して、受信メッセージの処理方法や、エンドポイントからの応答メッセージの送信先を指定できるほか、複数のサービス インスタンスが使用できる場合に、特定ユーザーからの受信メッセージの処理に使用するインスタンスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="72570-128">For example, headers can indicate how to process an incoming message, where the endpoint should send a reply message, or which instance of a service to use to process an incoming message from a particular user when multiple instances are available.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72570-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="72570-129">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.IdentityElement>  
 <xref:System.ServiceModel.EndpointAddress>  
 <xref:System.ServiceModel.EndpointAddress.Headers%2A>  
 <xref:System.ServiceModel.Channels.AddressHeaderCollection>  
 [<span data-ttu-id="72570-130">エンドポイント:アドレス、バインディング、およびコントラクト</span><span class="sxs-lookup"><span data-stu-id="72570-130">Endpoints: Addresses, Bindings, and Contracts</span></span>](../../../../../docs/framework/wcf/feature-details/endpoints-addresses-bindings-and-contracts.md)
