---
title: '&lt;serviceMetadata&gt;'
ms.date: 03/30/2017
ms.assetid: 2b4c3b4c-31d4-4908-a9b7-5bb411c221f2
ms.openlocfilehash: a5f69093a8eca7bfbdfd3b0d933a2689b552ec8f
ms.sourcegitcommit: 2eb5ca4956231c1a0efd34b6a9cab6153a5438af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2018
ms.locfileid: "49086714"
---
# <a name="ltservicemetadatagt"></a><span data-ttu-id="42ea2-102">&lt;serviceMetadata&gt;</span><span class="sxs-lookup"><span data-stu-id="42ea2-102">&lt;serviceMetadata&gt;</span></span>
<span data-ttu-id="42ea2-103">サービス メタデータと関連情報の公開を指定します。</span><span class="sxs-lookup"><span data-stu-id="42ea2-103">Specifies the publication of service metadata and associated information.</span></span>  
  
<span data-ttu-id="42ea2-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="42ea2-104">\<system.serviceModel></span></span>  
<span data-ttu-id="42ea2-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="42ea2-105">\<behaviors></span></span>  
<span data-ttu-id="42ea2-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="42ea2-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="42ea2-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="42ea2-107">\<behavior></span></span>  
<span data-ttu-id="42ea2-108">\<serviceMetadata ></span><span class="sxs-lookup"><span data-stu-id="42ea2-108">\<serviceMetadata></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42ea2-109">構文</span><span class="sxs-lookup"><span data-stu-id="42ea2-109">Syntax</span></span>  
  
```xml
<serviceMetadata externalMetadataLocation="String"  
                 httpGetBinding="String" 
                 httpGetBindingConfiguration="String"  
                 httpGetEnabled="Boolean" 
                 httpGetUrl="String" 
                 httpsGetBinding="String" 
                 httpsGetBindingConfiguration="String"  
                 httpsGetEnabled="Boolean"   
                 httpsGetUrl="String"  
                 policyVersion="Policy12/Policy15" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="42ea2-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="42ea2-110">Attributes and Elements</span></span>  
 <span data-ttu-id="42ea2-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="42ea2-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="42ea2-112">属性</span><span class="sxs-lookup"><span data-stu-id="42ea2-112">Attributes</span></span>  
  
|<span data-ttu-id="42ea2-113">属性</span><span class="sxs-lookup"><span data-stu-id="42ea2-113">Attribute</span></span>|<span data-ttu-id="42ea2-114">説明</span><span class="sxs-lookup"><span data-stu-id="42ea2-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="42ea2-115">externalMetadataLocation</span><span class="sxs-lookup"><span data-stu-id="42ea2-115">externalMetadataLocation</span></span>|<span data-ttu-id="42ea2-116">WSDL ファイルの位置を含む URI。これは、自動生成される WSDL の代わりに、WSDL 要求および MEX 要求に応答してユーザーに返されます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-116">A Uri that contains the location of a WSDL file, which is returned to the user in response to WSDL and MEX requests instead of the auto-generated WSDL.</span></span> <span data-ttu-id="42ea2-117">この属性が設定されていない場合は、既定の WSDL が返されます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-117">When this attribute is not set, the default WSDL is returned.</span></span> <span data-ttu-id="42ea2-118">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="42ea2-118">The default is an empty string.</span></span>|  
|<span data-ttu-id="42ea2-119">httpGetBinding</span><span class="sxs-lookup"><span data-stu-id="42ea2-119">httpGetBinding</span></span>|<span data-ttu-id="42ea2-120">HTTP GET 経由でメタデータを取得する場合に使用するバインディングの種類を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="42ea2-120">A string that specifies the type of the binding that will be used for metadata retrieval via HTTP GET.</span></span> <span data-ttu-id="42ea2-121">この設定は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="42ea2-121">This setting is optional.</span></span> <span data-ttu-id="42ea2-122">指定しない場合、既定のバインディングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-122">If it is not specified, the default bindings will be used.</span></span><br /><br /> <span data-ttu-id="42ea2-123"><xref:System.ServiceModel.Channels.IReplyChannel> をサポートする内部バインディング要素を使用したバインディングでのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-123">Only bindings with inner binding elements that support <xref:System.ServiceModel.Channels.IReplyChannel> will be supported.</span></span> <span data-ttu-id="42ea2-124">さらに、バインディングの <xref:System.ServiceModel.Channels.MessageVersion> プロパティが <xref:System.ServiceModel.Channels.MessageVersion.None%2A> である必要があります。</span><span class="sxs-lookup"><span data-stu-id="42ea2-124">Additionally, the <xref:System.ServiceModel.Channels.MessageVersion> property of the binding must be <xref:System.ServiceModel.Channels.MessageVersion.None%2A>.</span></span>|  
|<span data-ttu-id="42ea2-125">httpGetBindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="42ea2-125">httpGetBindingConfiguration</span></span>|<span data-ttu-id="42ea2-126">このバインディングの追加の構成情報を参照する `httpGetBinding` 属性に指定されるバインディングの名前を設定する文字列。</span><span class="sxs-lookup"><span data-stu-id="42ea2-126">A string that sets the name of the binding that is specified in the `httpGetBinding` attribute, which references to the additional configuration information of this binding.</span></span> <span data-ttu-id="42ea2-127">同じ名前を `<bindings>` セクションに定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42ea2-127">The same name must be defined in the `<bindings>` section.</span></span>|  
|<span data-ttu-id="42ea2-128">httpGetEnabled</span><span class="sxs-lookup"><span data-stu-id="42ea2-128">httpGetEnabled</span></span>|<span data-ttu-id="42ea2-129">HTTP/Get 要求を使用した取得用にサービス メタデータを公開するかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="42ea2-129">A Boolean value that specifies whether to publish service metadata for retrieval using an HTTP/Get request.</span></span> <span data-ttu-id="42ea2-130">既定値は、`false` です。</span><span class="sxs-lookup"><span data-stu-id="42ea2-130">The default is `false`.</span></span><br /><br /> <span data-ttu-id="42ea2-131">httpGetUrl 属性が指定されていない場合、メタデータが公開されるアドレスは、サービス アドレスに "?wsdl" を加えたものになります。</span><span class="sxs-lookup"><span data-stu-id="42ea2-131">If the httpGetUrl attribute is not specified, the address at which the metadata is published is the service address plus a "?wsdl".</span></span> <span data-ttu-id="42ea2-132">たとえば、サービス アドレスが"http://localhost:8080/CalculatorService「,、Http/get メタデータ アドレスは」 http://localhost:8080/CalculatorService?wsdl"。</span><span class="sxs-lookup"><span data-stu-id="42ea2-132">For example, if the service address is "http://localhost:8080/CalculatorService", the HTTP/Get metadata address is "http://localhost:8080/CalculatorService?wsdl".</span></span><br /><br /> <span data-ttu-id="42ea2-133">場合、このプロパティは`false`サービスのアドレスが HTTP または HTTPS に基づいていない、または"? wsdl"は無視されます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-133">If this property is `false`, or the address of the service is not based on HTTP or HTTPS, "?wsdl" is ignored.</span></span>|  
|<span data-ttu-id="42ea2-134">httpGetUrl</span><span class="sxs-lookup"><span data-stu-id="42ea2-134">httpGetUrl</span></span>|<span data-ttu-id="42ea2-135">HTTP/Get 要求を使用した取得用にメタデータが公開されるアドレスを指定する URI。</span><span class="sxs-lookup"><span data-stu-id="42ea2-135">A Uri that specifies the address at which the metadata is published for retrieval using an HTTP/Get request.</span></span> <span data-ttu-id="42ea2-136">相対 URI を指定した場合、サービスのベース アドレスに対する相対として処理されます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-136">If a relative Uri is specified it will be treated as relative to the service’s base address.</span></span>|  
|<span data-ttu-id="42ea2-137">httpsGetBinding</span><span class="sxs-lookup"><span data-stu-id="42ea2-137">httpsGetBinding</span></span>|<span data-ttu-id="42ea2-138">HTTPS GET 経由でメタデータを取得する場合に使用するバインディングの種類を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="42ea2-138">A string that specifies the type of the binding that will be used for metadata retrieval via HTTPS GET.</span></span> <span data-ttu-id="42ea2-139">この設定は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="42ea2-139">This setting is optional.</span></span> <span data-ttu-id="42ea2-140">指定しない場合、既定のバインディングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-140">If it is not specified, the default bindings will be used.</span></span><br /><br /> <span data-ttu-id="42ea2-141"><xref:System.ServiceModel.Channels.IReplyChannel> をサポートする内部バインディング要素を使用したバインディングでのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-141">Only bindings with inner binding elements that support <xref:System.ServiceModel.Channels.IReplyChannel> will be supported.</span></span> <span data-ttu-id="42ea2-142">さらに、バインディングの <xref:System.ServiceModel.Channels.MessageVersion> プロパティが <xref:System.ServiceModel.Channels.MessageVersion.None%2A> である必要があります。</span><span class="sxs-lookup"><span data-stu-id="42ea2-142">Additionally, the <xref:System.ServiceModel.Channels.MessageVersion> property of the binding must be <xref:System.ServiceModel.Channels.MessageVersion.None%2A>.</span></span>|  
|<span data-ttu-id="42ea2-143">httpsGetBindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="42ea2-143">httpsGetBindingConfiguration</span></span>|<span data-ttu-id="42ea2-144">このバインディングの追加の構成情報を参照する `httpsGetBinding` 属性に指定されるバインディングの名前を設定する文字列。</span><span class="sxs-lookup"><span data-stu-id="42ea2-144">A string that sets the name of the binding that is specified in the `httpsGetBinding` attribute, which references to the additional configuration information of this binding.</span></span> <span data-ttu-id="42ea2-145">同じ名前を `<bindings>` セクションに定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42ea2-145">The same name must be defined in the `<bindings>` section.</span></span>|  
|<span data-ttu-id="42ea2-146">httpsGetEnabled</span><span class="sxs-lookup"><span data-stu-id="42ea2-146">httpsGetEnabled</span></span>|<span data-ttu-id="42ea2-147">HTTPS/Get 要求を使用した取得用にサービス メタデータを公開するかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="42ea2-147">A Boolean value that specifies whether to publish service metadata for retrieval using an HTTPS/Get request.</span></span> <span data-ttu-id="42ea2-148">既定値は、`false` です。</span><span class="sxs-lookup"><span data-stu-id="42ea2-148">The default is `false`.</span></span><br /><br /> <span data-ttu-id="42ea2-149">httpsGetUrl 属性が指定されていない場合、メタデータが公開されるアドレスは、サービス アドレスに "?wsdl" を加えたものになります。</span><span class="sxs-lookup"><span data-stu-id="42ea2-149">If the httpsGetUrl attribute is not specified, the address at which the metadata is published is the service address plus a "?wsdl".</span></span> <span data-ttu-id="42ea2-150">たとえば、サービス アドレスが"https://localhost:8080/CalculatorService「,、Http/get メタデータ アドレスは」 https://localhost:8080/CalculatorService?wsdl"。</span><span class="sxs-lookup"><span data-stu-id="42ea2-150">For example, if the service address is "https://localhost:8080/CalculatorService", the HTTP/Get metadata address is "https://localhost:8080/CalculatorService?wsdl".</span></span><br /><br /> <span data-ttu-id="42ea2-151">場合、このプロパティは`false`サービスのアドレスが HTTP または HTTPS に基づいていない、または"? wsdl"は無視されます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-151">If this property is `false`, or the address of the service is not based on HTTP or HTTPS, "?wsdl" is ignored.</span></span>|  
|<span data-ttu-id="42ea2-152">httpsGetUrl</span><span class="sxs-lookup"><span data-stu-id="42ea2-152">httpsGetUrl</span></span>|<span data-ttu-id="42ea2-153">HTTPS/Get 要求を使用した取得用にメタデータが公開されるアドレスを指定する URI。</span><span class="sxs-lookup"><span data-stu-id="42ea2-153">A Uri that specifies the address at which the metadata is published for retrieval using an HTTPS/Get request.</span></span>|  
|<span data-ttu-id="42ea2-154">policyVersion</span><span class="sxs-lookup"><span data-stu-id="42ea2-154">policyVersion</span></span>|<span data-ttu-id="42ea2-155">使用する WS-Policy 仕様のバージョンを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="42ea2-155">A string that specifies the version of the WS-Policy specification being used.</span></span> <span data-ttu-id="42ea2-156">この属性は <xref:System.ServiceModel.Description.PolicyVersion> 型です。</span><span class="sxs-lookup"><span data-stu-id="42ea2-156">This attribute is of type <xref:System.ServiceModel.Description.PolicyVersion>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="42ea2-157">子要素</span><span class="sxs-lookup"><span data-stu-id="42ea2-157">Child Elements</span></span>  
 <span data-ttu-id="42ea2-158">なし</span><span class="sxs-lookup"><span data-stu-id="42ea2-158">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="42ea2-159">親要素</span><span class="sxs-lookup"><span data-stu-id="42ea2-159">Parent Elements</span></span>  
  
|<span data-ttu-id="42ea2-160">要素</span><span class="sxs-lookup"><span data-stu-id="42ea2-160">Element</span></span>|<span data-ttu-id="42ea2-161">説明</span><span class="sxs-lookup"><span data-stu-id="42ea2-161">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="42ea2-162">\<behavior></span><span class="sxs-lookup"><span data-stu-id="42ea2-162">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="42ea2-163">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="42ea2-163">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="42ea2-164">Remarks</span><span class="sxs-lookup"><span data-stu-id="42ea2-164">Remarks</span></span>  
 <span data-ttu-id="42ea2-165">この構成要素を使用すると、サービスのメタデータ公開機能を制御できます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-165">This configuration element allows you to control the metadata publishing features of a service.</span></span> <span data-ttu-id="42ea2-166">可能性のある機密性の高いサービス メタデータが誤って漏洩を防ぐためには、Windows Communication Foundation (WCF) サービスの既定の構成ではメタデータの公開を無効にします。</span><span class="sxs-lookup"><span data-stu-id="42ea2-166">To prevent unintentional disclosure of potentially sensitive service metadata, the default configuration for Windows Communication Foundation (WCF) services disables metadata publishing.</span></span> <span data-ttu-id="42ea2-167">この動作は、既定の設定ではセキュリティで保護されますが、同時に、サービスの構成の中でメタデータ発行の動作が明示的に有効化されない限り、サービスの呼び出しに必要なクライアント コードをメタデータ インポート ツール (Svcutil.exe など) を使用して生成できないことも意味します。</span><span class="sxs-lookup"><span data-stu-id="42ea2-167">This behavior is secure by default, but also means that you cannot use a metadata import tool (such as Svcutil.exe) to generate the client code required to call the service unless the service’s metadata publishing behavior is explicitly enabled in configuration.</span></span> <span data-ttu-id="42ea2-168">この構成要素を使用すると、サービスのこの公開動作を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-168">Using this configuration element, you can enable this publishing behavior for your service.</span></span>  
  
 <span data-ttu-id="42ea2-169">この動作の構成の詳細な例を参照してください。[メタデータ公開動作](../../../../../docs/framework/wcf/samples/metadata-publishing-behavior.md)します。</span><span class="sxs-lookup"><span data-stu-id="42ea2-169">For a detailed example of configuring this behavior, see [Metadata Publishing Behavior](../../../../../docs/framework/wcf/samples/metadata-publishing-behavior.md).</span></span>  
  
 <span data-ttu-id="42ea2-170">オプションの `httpGetBinding` 属性および `httpsGetBinding` 属性を使用すると、HTTP GET または HTTPS GET を介してメタデータを取得するバインディングを構成できます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-170">The optional `httpGetBinding` and `httpsGetBinding` attributes allow you to configure the bindings used for metadata retrieval via HTTP GET (or HTTPS GET).</span></span> <span data-ttu-id="42ea2-171">これらの属性を指定しない場合、メタデータの取得には、適切な既定のバインディグ (HTTP の場合は `HttpTransportBindingElement`、HTTPS の場合は `HttpsTransportBindingElement`) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-171">If they are not specified, the default bindings (`HttpTransportBindingElement`, in the case of HTTP and `HttpsTransportBindingElement`, in the case of HTTPS) are used for metadata retrieval as appropriate.</span></span> <span data-ttu-id="42ea2-172">これらの属性は、組み込みの WCF バインディングでは使用できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="42ea2-172">Notice that you cannot use these attributes with the built-in WCF bindings.</span></span> <span data-ttu-id="42ea2-173"><xref:System.ServiceModel.Channels.IReplyChannel> をサポートする内部バインディング要素を使用したバインディングでのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-173">Only bindings with inner binding elements that support <xref:System.ServiceModel.Channels.IReplyChannel> will be supported.</span></span> <span data-ttu-id="42ea2-174">さらに、バインディングの <xref:System.ServiceModel.Channels.MessageVersion> プロパティが <xref:System.ServiceModel.Channels.MessageVersion.None%2A> である必要があります。</span><span class="sxs-lookup"><span data-stu-id="42ea2-174">Additionally, the <xref:System.ServiceModel.Channels.MessageVersion> property of the binding must be <xref:System.ServiceModel.Channels.MessageVersion.None%2A>.</span></span>  
  
 <span data-ttu-id="42ea2-175">サービスが悪意のあるユーザーに公開されないようにするために、SSL over HTTP (HTTPS) 機構を使用して転送をセキュリティで保護できます。</span><span class="sxs-lookup"><span data-stu-id="42ea2-175">To reduce the exposure of a service to malicious users, it is possible to secure the transfer using the SSL over HTTP (HTTPS) mechanism.</span></span> <span data-ttu-id="42ea2-176">転送を保護するには、まず、サービスをホストしているコンピューターの特定のポートに適切な X.509 証明書をバインドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="42ea2-176">To do so, you must first bind a suitable X.509 certificate to a specific port on the computer that is hosting the service.</span></span> <span data-ttu-id="42ea2-177">(詳細については、次を参照してください[Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)。)。次に、この要素をサービス構成に追加し、`httpsGetEnabled` 属性を `true` に設定します。</span><span class="sxs-lookup"><span data-stu-id="42ea2-177">(For more information, see [Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md).) Second, add this element to the service configuration and set the `httpsGetEnabled` attribute to `true`.</span></span> <span data-ttu-id="42ea2-178">最後に、次の例に示すように、`httpsGetUrl` 属性をサービス メタデータ エンドポイントの URL に設定します。</span><span class="sxs-lookup"><span data-stu-id="42ea2-178">Finally, set the `httpsGetUrl` attribute to the URL of the service metadata endpoint, as shown in the following example.</span></span>  
  
```xml
<behaviors>  
  <serviceBehaviors>  
    <behavior name="NewBehavior">  
      <serviceMetadata httpsGetEnabled="true"   
                       httpsGetUrl="https://myComputerName/myEndpoint" />  
    </behavior>  
  </serviceBehaviors>  
</behaviors>  
```  
  
## <a name="example"></a><span data-ttu-id="42ea2-179">例</span><span class="sxs-lookup"><span data-stu-id="42ea2-179">Example</span></span>  
 <span data-ttu-id="42ea2-180">次の例では、構成を使用してメタデータを公開するサービスを\<serviceMetadata > 要素。</span><span class="sxs-lookup"><span data-stu-id="42ea2-180">The following example configure a service to expose metadata by using the \<serviceMetadata> element.</span></span> <span data-ttu-id="42ea2-181">さらに、`IMetadataExchange` コントラクトを WS-MetadataExchange (MEX) プロトコルの実装として公開するエンドポイントも構成します。</span><span class="sxs-lookup"><span data-stu-id="42ea2-181">It also configures an endpoint to expose the `IMetadataExchange` contract as an implementation of a WS-MetadataExchange (MEX) protocol.</span></span> <span data-ttu-id="42ea2-182">この例では、`mexHttpBinding` を使用します。これは使いやすい標準バインドで、セキュリティ モードが `wsHttpBinding` に設定されている `None` と同等です。</span><span class="sxs-lookup"><span data-stu-id="42ea2-182">The example uses the `mexHttpBinding`, which is a convenience standard binding that is equivalent to the `wsHttpBinding` with the security mode set to `None`.</span></span> <span data-ttu-id="42ea2-183">相対アドレスの"mex"が使用されるエンドポイントには、どのに対して解決とサービスのベース アドレスのエンドポイント アドレス `http://localhost/servicemodelsamples/service.svc/mex` です。</span><span class="sxs-lookup"><span data-stu-id="42ea2-183">A relative address of "mex" is used in the endpoint, which when resolved against the services base address results in an endpoint address of `http://localhost/servicemodelsamples/service.svc/mex`.</span></span>  
  
```xml
<configuration>  
  <system.serviceModel>  
    <services>  
      <service name="Microsoft.ServiceModel.Samples.CalculatorService" 
               behaviorConfiguration="CalculatorServiceBehavior">  
        <!-- This endpoint is exposed at the base address provided by the host: http://localhost/servicemodelsamples/service.svc -->  
        <endpoint address=""  
                  binding="wsHttpBinding"  
                  contract="Microsoft.ServiceModel.Samples.ICalculator" />  
        <!-- The mex endpoint is exposed at http://localhost/servicemodelsamples/service.svc/mex   
             To expose the IMetadataExchange contract, you must enable the serviceMetadata behavior as demonstrated below. -->  
        <endpoint address="mex"  
                  binding="mexHttpBinding"  
                  contract="IMetadataExchange" />  
      </service>  
    </services>  

    <!--For debugging purposes set the includeExceptionDetailInFaults attribute to true-->  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="CalculatorServiceBehavior">  
          <!-- The serviceMetadata behavior publishes metadata through   
               the IMetadataExchange contract. When this behavior is   
               present, you can expose this contract through an endpoint   
               as shown above. Setting httpGetEnabled to true publishes   
               the service's WSDL at the <baseaddress>?wsdl  
               eg. http://localhost/servicemodelsamples/service.svc?wsdl -->  
          <serviceMetadata httpGetEnabled="True"/>  
          <serviceDebug includeExceptionDetailInFaults="False" />  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="42ea2-184">関連項目</span><span class="sxs-lookup"><span data-stu-id="42ea2-184">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceMetadataPublishingElement>  
 <xref:System.ServiceModel.Description.ServiceMetadataBehavior>  
 [<span data-ttu-id="42ea2-185">セキュリティ動作</span><span class="sxs-lookup"><span data-stu-id="42ea2-185">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)  
 [<span data-ttu-id="42ea2-186">メタデータ公開動作</span><span class="sxs-lookup"><span data-stu-id="42ea2-186">Metadata Publishing Behavior</span></span>](../../../../../docs/framework/wcf/samples/metadata-publishing-behavior.md)
