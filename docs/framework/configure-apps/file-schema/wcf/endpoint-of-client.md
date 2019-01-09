---
title: '&lt;client&gt; の &lt;endpoint&gt;'
ms.date: 03/30/2017
ms.assetid: de6238ae-bbf8-48e9-a1b5-e24c0bea8afa
ms.openlocfilehash: 47b3599ed2d0868fcbc4a04a28936bcfe1c9c3f1
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147006"
---
# <a name="ltendpointgt-of-ltclientgt"></a><span data-ttu-id="291ef-102">&lt;client&gt; の &lt;endpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="291ef-102">&lt;endpoint&gt; of &lt;client&gt;</span></span>
<span data-ttu-id="291ef-103">サーバーのサービス エンドポイントに接続するためにクライアントによって使用されるチャネル エンドポイントのコントラクト、バインディング、およびアドレスのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="291ef-103">Specifies contract, binding, and address properties of the channel endpoint, which is used by clients to connect to service endpoints on the server.</span></span>  
  
 <span data-ttu-id="291ef-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="291ef-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="291ef-105">\<client></span><span class="sxs-lookup"><span data-stu-id="291ef-105">\<client></span></span>  
<span data-ttu-id="291ef-106">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="291ef-106">\<endpoint></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="291ef-107">構文</span><span class="sxs-lookup"><span data-stu-id="291ef-107">Syntax</span></span>  
  
```xml  
<endpoint address="String"
          behaviorConfiguration="String"
          binding="String"
          bindingConfiguration="String"
          contract="String"
          endpointConfiguration="String"
          kind="String"
          name="String">
</endpoint>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="291ef-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="291ef-108">Attributes and Elements</span></span>  
 <span data-ttu-id="291ef-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="291ef-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="291ef-110">属性</span><span class="sxs-lookup"><span data-stu-id="291ef-110">Attributes</span></span>  
  
|<span data-ttu-id="291ef-111">属性</span><span class="sxs-lookup"><span data-stu-id="291ef-111">Attribute</span></span>|<span data-ttu-id="291ef-112">説明</span><span class="sxs-lookup"><span data-stu-id="291ef-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="291ef-113">address</span><span class="sxs-lookup"><span data-stu-id="291ef-113">address</span></span>|<span data-ttu-id="291ef-114">必須の文字列属性です。</span><span class="sxs-lookup"><span data-stu-id="291ef-114">Required string attribute.</span></span><br /><br /> <span data-ttu-id="291ef-115">エンドポイントのアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="291ef-115">Specifies the address of the endpoint.</span></span> <span data-ttu-id="291ef-116">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="291ef-116">The default is an empty string.</span></span> <span data-ttu-id="291ef-117">アドレスは、絶対 URI にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="291ef-117">The address must be an absolute URI.</span></span>|  
|<span data-ttu-id="291ef-118">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="291ef-118">behaviorConfiguration</span></span>|<span data-ttu-id="291ef-119">エンドポイントのインスタンス化に使用される動作の動作名を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="291ef-119">A string that contains the behavior name of the behavior to be used to instantiate the endpoint.</span></span> <span data-ttu-id="291ef-120">動作名は、サービスが定義される時点でスコープ内にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="291ef-120">The behavior name must be in scope at the point the service is defined.</span></span> <span data-ttu-id="291ef-121">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="291ef-121">The default is an empty string.</span></span>|  
|<span data-ttu-id="291ef-122">バインド</span><span class="sxs-lookup"><span data-stu-id="291ef-122">binding</span></span>|<span data-ttu-id="291ef-123">必須の文字列属性です。</span><span class="sxs-lookup"><span data-stu-id="291ef-123">Required string attribute.</span></span><br /><br /> <span data-ttu-id="291ef-124">使用するバインディングの種類を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="291ef-124">A string that indicates the type of binding to use.</span></span> <span data-ttu-id="291ef-125">参照できるようにするには、種類は登録された構成セクションを持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="291ef-125">The type must have a registered configuration section in order to be referenced.</span></span> <span data-ttu-id="291ef-126">種類は、バインディングの種類の名前ではなくセクション名で登録されます。</span><span class="sxs-lookup"><span data-stu-id="291ef-126">The type is registered by section name, instead of by the type name of the binding.</span></span>|  
|<span data-ttu-id="291ef-127">bindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="291ef-127">bindingConfiguration</span></span>|<span data-ttu-id="291ef-128">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="291ef-128">Optional.</span></span> <span data-ttu-id="291ef-129">エンドポイントがインスタンス化されるときに使用するバインディング構成の名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="291ef-129">A string that contains the name of the binding configuration to be used when the endpoint is instantiated.</span></span> <span data-ttu-id="291ef-130">バインディング構成は、エンドポイントが定義される時点でスコープ内にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="291ef-130">The binding configuration must be in scope at the point the endpoint is defined.</span></span> <span data-ttu-id="291ef-131">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="291ef-131">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="291ef-132">この属性は、構成ファイル内の特定のバインディング構成を参照するために、`binding` と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="291ef-132">This attribute is used in conjunction with `binding` to reference a specific binding configuration in the configuration file.</span></span> <span data-ttu-id="291ef-133">カスタム バインディングを使用しようとする場合にこの属性を設定します。</span><span class="sxs-lookup"><span data-stu-id="291ef-133">Set this attribute if you are attempting to use a custom binding.</span></span> <span data-ttu-id="291ef-134">そうでない場合は、例外がスローされることがあります。</span><span class="sxs-lookup"><span data-stu-id="291ef-134">Otherwise, an exception may be thrown.</span></span>|  
|<span data-ttu-id="291ef-135">コントラクト</span><span class="sxs-lookup"><span data-stu-id="291ef-135">contract</span></span>|<span data-ttu-id="291ef-136">必須の文字列属性です。</span><span class="sxs-lookup"><span data-stu-id="291ef-136">Required string attribute.</span></span><br /><br /> <span data-ttu-id="291ef-137">このエンドポイントが公開するコントラクトを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="291ef-137">A string that indicates which contract this endpoint is exposing.</span></span> <span data-ttu-id="291ef-138">アセンブリは、コントラクト型を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="291ef-138">The assembly must implement the contract type.</span></span>|  
|<span data-ttu-id="291ef-139">endpointConfiguration</span><span class="sxs-lookup"><span data-stu-id="291ef-139">endpointConfiguration</span></span>|<span data-ttu-id="291ef-140">この標準エンドポイントの追加の構成情報を参照する `kind` 属性によって設定される標準エンドポイントの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="291ef-140">A string that specifies the name of the standard endpoint that is set by the `kind` attribute, which references to the additional configuration information of this standard endpoint.</span></span> <span data-ttu-id="291ef-141">同じ名前を `<standardEndpoints>` セクションに定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="291ef-141">The same name must be defined in the `<standardEndpoints>` section.</span></span>|  
|<span data-ttu-id="291ef-142">kind</span><span class="sxs-lookup"><span data-stu-id="291ef-142">kind</span></span>|<span data-ttu-id="291ef-143">適用する標準エンドポイントの種類を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="291ef-143">A string that specifies the type of standard endpoint applied.</span></span> <span data-ttu-id="291ef-144">種類は `<extensions>` セクションまたは machine.config に登録する必要があります。何も指定されていない場合は、共通のチャネル エンドポイントが作成されます。</span><span class="sxs-lookup"><span data-stu-id="291ef-144">The type must be registered in the `<extensions>` section or in machine.config. If nothing is specified, a common channel endpoint is created.</span></span>|  
|<span data-ttu-id="291ef-145">name</span><span class="sxs-lookup"><span data-stu-id="291ef-145">name</span></span>|<span data-ttu-id="291ef-146">省略可能な文字列属性。</span><span class="sxs-lookup"><span data-stu-id="291ef-146">Optional string attribute.</span></span> <span data-ttu-id="291ef-147">この属性は、特定のコントラクトのエンドポイントを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="291ef-147">This attribute uniquely identifies an endpoint for a given contract.</span></span> <span data-ttu-id="291ef-148">特定のコントラクトの種類に、複数のクライアントを定義できます。</span><span class="sxs-lookup"><span data-stu-id="291ef-148">You can define multiple clients for a given Contract type.</span></span> <span data-ttu-id="291ef-149">それぞれの定義は、一意の構成名で区別できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="291ef-149">Each definition must be differentiated by a unique configuration name.</span></span> <span data-ttu-id="291ef-150">この属性が省略されている場合、指定されたコントラクトの種類に関連する既定のエンドポイントとして、対応するエンドポイントが使用されます。</span><span class="sxs-lookup"><span data-stu-id="291ef-150">If this attribute is omitted, the corresponding endpoint is used as the default endpoint associated with the specified Contract type.</span></span> <span data-ttu-id="291ef-151">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="291ef-151">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="291ef-152">バインディングの `name` 属性は、WSDL を介した定義エクスポートに使用されます。</span><span class="sxs-lookup"><span data-stu-id="291ef-152">The `name` attribute of a binding is used for definition export through WSDL.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="291ef-153">子要素</span><span class="sxs-lookup"><span data-stu-id="291ef-153">Child Elements</span></span>  
  
|<span data-ttu-id="291ef-154">要素</span><span class="sxs-lookup"><span data-stu-id="291ef-154">Element</span></span>|<span data-ttu-id="291ef-155">説明</span><span class="sxs-lookup"><span data-stu-id="291ef-155">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="291ef-156">\<headers></span><span class="sxs-lookup"><span data-stu-id="291ef-156">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers.md)|<span data-ttu-id="291ef-157">アドレス ヘッダーのコレクション。</span><span class="sxs-lookup"><span data-stu-id="291ef-157">A collection of address headers.</span></span>|  
|[<span data-ttu-id="291ef-158">\<identity></span><span class="sxs-lookup"><span data-stu-id="291ef-158">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="291ef-159">メッセージを交換する他のエンドポイントによるエンドポイントの認証を可能にする ID です。</span><span class="sxs-lookup"><span data-stu-id="291ef-159">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="291ef-160">親要素</span><span class="sxs-lookup"><span data-stu-id="291ef-160">Parent Elements</span></span>  
  
|<span data-ttu-id="291ef-161">要素</span><span class="sxs-lookup"><span data-stu-id="291ef-161">Element</span></span>|<span data-ttu-id="291ef-162">説明</span><span class="sxs-lookup"><span data-stu-id="291ef-162">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="291ef-163">\<クライアント ></span><span class="sxs-lookup"><span data-stu-id="291ef-163">\<client></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/client.md)|<span data-ttu-id="291ef-164">クライアントが接続可能なエンドポイントの一覧を定義する設定セクションです。</span><span class="sxs-lookup"><span data-stu-id="291ef-164">A configuration section that defines a list of endpoints that a client can connect to.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="291ef-165">例</span><span class="sxs-lookup"><span data-stu-id="291ef-165">Example</span></span>  
 <span data-ttu-id="291ef-166">これはチャネル エンドポイントの構成の例です。</span><span class="sxs-lookup"><span data-stu-id="291ef-166">This is an example of a channel endpoint configuration.</span></span>  
  
```xml  
<endpoint address="/HelloWorld/"
          bindingConfiguration="usingDefaults"
          name="MyBinding"
          binding="customBinding"
          contract="HelloWorld">
</endpoint>
```  
  
## <a name="see-also"></a><span data-ttu-id="291ef-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="291ef-167">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ChannelEndpointElement>  
 <xref:System.ServiceModel.Configuration.ClientSection>  
 <xref:System.ServiceModel.Configuration.ChannelEndpointElementCollection>  
 <xref:System.ServiceModel.Configuration.ClientSection.Endpoints%2A>  
 <xref:System.ServiceModel.Configuration.ChannelEndpointElement>  
 [<span data-ttu-id="291ef-168">WCF クライアントの構成</span><span class="sxs-lookup"><span data-stu-id="291ef-168">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)  
 [<span data-ttu-id="291ef-169">クライアント</span><span class="sxs-lookup"><span data-stu-id="291ef-169">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
