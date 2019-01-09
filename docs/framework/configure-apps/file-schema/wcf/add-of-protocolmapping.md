---
title: '&lt;protocolMapping&gt; の &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: 08e62249-1641-41d1-91b1-66d7b46244e4
ms.openlocfilehash: e21c3ca665d6a75394d70da43ec2044e00f16429
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145485"
---
# <a name="ltaddgt-of-ltprotocolmappinggt"></a><span data-ttu-id="76953-102">&lt;protocolMapping&gt; の &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="76953-102">&lt;add&gt; of &lt;protocolMapping&gt;</span></span>
<span data-ttu-id="76953-103">トランスポート プロトコル スキーム (など、http、net.tcp、net.pipe など) と Windows Communication Foundation (WCF) バインドの間の既定のプロトコル マッピングを表します。</span><span class="sxs-lookup"><span data-stu-id="76953-103">Represents a default protocol mapping between a transport protocol scheme (e.g., http, net.tcp, net.pipe, etc.) and a Windows Communication Foundation (WCF) binding.</span></span> <span data-ttu-id="76953-104">実行時に既定のエンドポイントを作成するときに、WCF は構成済みのマッピングではされ、特定に使用するバインディングをベース アドレスを決定します。</span><span class="sxs-lookup"><span data-stu-id="76953-104">When creating default endpoints at runtime, WCF looks at the configured mappings and decides on which binding to use for a particular based address.</span></span>  
  
 <span data-ttu-id="76953-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="76953-105">\<system.serviceModel></span></span>  
<span data-ttu-id="76953-106">\<protocolMapping ></span><span class="sxs-lookup"><span data-stu-id="76953-106">\<protocolMapping></span></span>  
<span data-ttu-id="76953-107">\<add></span><span class="sxs-lookup"><span data-stu-id="76953-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76953-108">構文</span><span class="sxs-lookup"><span data-stu-id="76953-108">Syntax</span></span>  
  
```xml  
<protocolMapping>
  <add binding="String"
       bindingConfiguration="String"
       scheme="http/net.msmq/net.pipe/net.tcp" />
</protocolMapping>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="76953-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="76953-109">Attributes and Elements</span></span>  
 <span data-ttu-id="76953-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="76953-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="76953-111">属性</span><span class="sxs-lookup"><span data-stu-id="76953-111">Attributes</span></span>  
  
|<span data-ttu-id="76953-112">要素</span><span class="sxs-lookup"><span data-stu-id="76953-112">Element</span></span>|<span data-ttu-id="76953-113">説明</span><span class="sxs-lookup"><span data-stu-id="76953-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="76953-114">バインド</span><span class="sxs-lookup"><span data-stu-id="76953-114">binding</span></span>|<span data-ttu-id="76953-115">既定のエンドポイントを作成するときにエンドポイントに使用されるバインディングの種類を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="76953-115">A string that specifies the type of binding to be used for an endpoint during default endpoint creation.</span></span>|  
|<span data-ttu-id="76953-116">bindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="76953-116">bindingConfiguration</span></span>|<span data-ttu-id="76953-117">参照されるバインディング構成セクションの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="76953-117">A string that specifies the name of the binding configuration section to be referenced.</span></span>|  
|<span data-ttu-id="76953-118">scheme</span><span class="sxs-lookup"><span data-stu-id="76953-118">scheme</span></span>|<span data-ttu-id="76953-119">既定のエンドポイントに使用されるトランスポート プロトコル スキーム。</span><span class="sxs-lookup"><span data-stu-id="76953-119">The transport protocol scheme to be used for the default endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="76953-120">子要素</span><span class="sxs-lookup"><span data-stu-id="76953-120">Child Elements</span></span>  
 <span data-ttu-id="76953-121">なし。</span><span class="sxs-lookup"><span data-stu-id="76953-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="76953-122">親要素</span><span class="sxs-lookup"><span data-stu-id="76953-122">Parent Elements</span></span>  
  
|<span data-ttu-id="76953-123">要素</span><span class="sxs-lookup"><span data-stu-id="76953-123">Element</span></span>|<span data-ttu-id="76953-124">説明</span><span class="sxs-lookup"><span data-stu-id="76953-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="76953-125">\<protocolMapping ></span><span class="sxs-lookup"><span data-stu-id="76953-125">\<protocolMapping></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/protocolmapping.md)|<span data-ttu-id="76953-126">トランスポート プロトコル スキーム (など、http、net.tcp、net.pipe など) と Windows Communication Foundation (WCF) バインドの間の既定のプロトコル マッピングを定義するための構成セクションを表します。</span><span class="sxs-lookup"><span data-stu-id="76953-126">Represents a configuration section for defining default protocol mappings between transport protocol schemes (e.g., http, net.tcp, net.pipe, etc.) and Windows Communication Foundation (WCF) bindings.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="76953-127">例</span><span class="sxs-lookup"><span data-stu-id="76953-127">Example</span></span>  
 <span data-ttu-id="76953-128">次の構成例は、machine.config ファイル内の既定のプロトコル マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="76953-128">The following configuration example shows the default protocol mapping in the machine.config file.</span></span> <span data-ttu-id="76953-129">machine.config ファイルを変更することで、既定のマッピングをコンピューター レベルでオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="76953-129">You can override this default mapping at the machine level by modifying the machine.config file.</span></span> <span data-ttu-id="76953-130">または、アプリケーションのスコープ内だけでオーバーライドする場合は、アプリケーション構成ファイルのこのセクションをオーバーライドし、各プロトコル スキームのマッピングを変更できます。</span><span class="sxs-lookup"><span data-stu-id="76953-130">Or if you would only like to override it within the scope of an application, you can override this section within your application configuration file and change the mapping for individual protocol schemes.</span></span>  
  
```xml  
<protocolMapping>
  <add scheme="http"
       binding="basicHttpBinding" />
  <add scheme="net.tcp"
       binding="netTcpBinding" />
  <add scheme="net.pipe"
       binding="netNamedPipeBinding" />
  <add scheme="net.msmq"
       binding="netMsmqBinding" />
</protocolMapping>
```  
  
## <a name="see-also"></a><span data-ttu-id="76953-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="76953-131">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ProtocolMappingSection?displayProperty=nameWithType>      
 <xref:System.ServiceModel.Configuration.ProtocolMappingElement?displayProperty=nameWithType>    
