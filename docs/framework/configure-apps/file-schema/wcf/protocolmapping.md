---
title: '&lt;protocolMapping&gt;'
ms.date: 03/30/2017
ms.assetid: 5076644b-1f33-4f26-9488-87de9fcda04c
ms.openlocfilehash: a376f1eaa7c8790cf2174335749ed3001b403967
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147305"
---
# <a name="ltprotocolmappinggt"></a><span data-ttu-id="30397-102">&lt;protocolMapping&gt;</span><span class="sxs-lookup"><span data-stu-id="30397-102">&lt;protocolMapping&gt;</span></span>
<span data-ttu-id="30397-103">トランスポート プロトコル スキーム (など、http、net.tcp、net.pipe など) と WCF バインディング間の既定のプロトコル マッピングのセットを定義する構成セクションを表します。</span><span class="sxs-lookup"><span data-stu-id="30397-103">Represents a configuration section for defining a set of default protocol mapping between transport protocol schemes (e.g., http, net.tcp, net.pipe, etc.) and WCF bindings.</span></span> <span data-ttu-id="30397-104">実行時に既定のエンドポイントを作成するときに、Windows Communication Foundation (WCF) が構成済みのマッピングではされ、特定に使用するバインディングをベース アドレスを決定します。</span><span class="sxs-lookup"><span data-stu-id="30397-104">When creating default endpoints at runtime, Windows Communication Foundation (WCF) looks at the configured mappings and decides on which binding to use for a particular based address.</span></span>  
  
[<span data-ttu-id="30397-105">**\<system.serviceModel >**</span><span class="sxs-lookup"><span data-stu-id="30397-105">**\<system.serviceModel>**</span></span>](system-servicemodel.md)  
<span data-ttu-id="30397-106">&nbsp;&nbsp;**\<protocolMapping >**</span><span class="sxs-lookup"><span data-stu-id="30397-106">&nbsp;&nbsp;**\<protocolMapping>**</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30397-107">構文</span><span class="sxs-lookup"><span data-stu-id="30397-107">Syntax</span></span>  
  
```xml  
<protocolMapping>
  <add binding="String"
       bindingConfiguration="String"
       scheme="http/net.msmq/net.pipe/net.tcp" />
</protocolMapping>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="30397-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="30397-108">Attributes and Elements</span></span>  
 <span data-ttu-id="30397-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="30397-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="30397-110">属性</span><span class="sxs-lookup"><span data-stu-id="30397-110">Attributes</span></span>  
 <span data-ttu-id="30397-111">なし。</span><span class="sxs-lookup"><span data-stu-id="30397-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="30397-112">子要素</span><span class="sxs-lookup"><span data-stu-id="30397-112">Child Elements</span></span>  
  
|<span data-ttu-id="30397-113">要素</span><span class="sxs-lookup"><span data-stu-id="30397-113">Element</span></span>|<span data-ttu-id="30397-114">説明</span><span class="sxs-lookup"><span data-stu-id="30397-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="30397-115">\<フィルター ></span><span class="sxs-lookup"><span data-stu-id="30397-115">\<filters></span></span>](filters-of-routing.md)|<span data-ttu-id="30397-116">トランスポート プロトコル スキーム (など、http、net.tcp、net.pipe など) と WCF バインディング間の既定のプロトコル マッピングが含まれています。</span><span class="sxs-lookup"><span data-stu-id="30397-116">Contains a default protocol mapping between a transport protocol scheme (e.g., http, net.tcp, net.pipe, etc.) and a WCF binding.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="30397-117">親要素</span><span class="sxs-lookup"><span data-stu-id="30397-117">Parent Elements</span></span>  
  
|<span data-ttu-id="30397-118">要素</span><span class="sxs-lookup"><span data-stu-id="30397-118">Element</span></span>|<span data-ttu-id="30397-119">説明</span><span class="sxs-lookup"><span data-stu-id="30397-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="30397-120">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="30397-120">\<system.serviceModel></span></span>](system-servicemodel.md)|<span data-ttu-id="30397-121">すべての WCF 構成要素のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="30397-121">The root element of all WCF configuration elements.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="30397-122">例</span><span class="sxs-lookup"><span data-stu-id="30397-122">Example</span></span>  
 <span data-ttu-id="30397-123">次の構成例は、machine.config ファイル内の既定のプロトコル マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="30397-123">The following configuration example shows the default protocol mapping in the machine.config file.</span></span> <span data-ttu-id="30397-124">machine.config ファイルを変更することで、既定のマッピングをコンピューター レベルでオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="30397-124">You can override this default mapping at the machine level by modifying the machine.config file.</span></span> <span data-ttu-id="30397-125">または、アプリケーションのスコープ内だけでオーバーライドする場合は、アプリケーション構成ファイルのこのセクションをオーバーライドし、各プロトコル スキームのマッピングを変更できます。</span><span class="sxs-lookup"><span data-stu-id="30397-125">Or if you would only like to override it within the scope of an application, you can override this section within your application configuration file and change the mapping for individual protocol schemes.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="30397-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="30397-126">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ProtocolMappingSection?displayProperty=nameWithType>       
 <xref:System.ServiceModel.Configuration.ProtocolMappingElement?displayProperty=nameWithType>    
