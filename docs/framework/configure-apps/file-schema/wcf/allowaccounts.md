---
title: '&lt;allowAccounts&gt;'
ms.date: 03/30/2017
ms.assetid: 166923a9-a8ac-478f-92f9-529d9667f3a6
ms.openlocfilehash: 61310d530cfec2862fb64155777cd0e88132f748
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145940"
---
# <a name="ltallowaccountsgt"></a><span data-ttu-id="24048-102">&lt;allowAccounts&gt;</span><span class="sxs-lookup"><span data-stu-id="24048-102">&lt;allowAccounts&gt;</span></span>
<span data-ttu-id="24048-103">ユーザーがプロセスのアカウントをホストする Windows Communication Foundation (WCF) サービス、および共有サービスへの接続アクセスが許可を指定する構成要素のコレクションを含みます。</span><span class="sxs-lookup"><span data-stu-id="24048-103">Contains a collection of configuration elements that specify user accounts for processes that host Windows Communication Foundation (WCF) services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="24048-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="24048-104">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24048-105">構文</span><span class="sxs-lookup"><span data-stu-id="24048-105">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="24048-106">属性および要素</span><span class="sxs-lookup"><span data-stu-id="24048-106">Attributes and Elements</span></span>  
 <span data-ttu-id="24048-107">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="24048-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="24048-108">属性</span><span class="sxs-lookup"><span data-stu-id="24048-108">Attributes</span></span>  
 <span data-ttu-id="24048-109">なし。</span><span class="sxs-lookup"><span data-stu-id="24048-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="24048-110">子要素</span><span class="sxs-lookup"><span data-stu-id="24048-110">Child Elements</span></span>  
  
|<span data-ttu-id="24048-111">属性</span><span class="sxs-lookup"><span data-stu-id="24048-111">Attribute</span></span>|<span data-ttu-id="24048-112">説明</span><span class="sxs-lookup"><span data-stu-id="24048-112">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="24048-113">\<add></span><span class="sxs-lookup"><span data-stu-id="24048-113">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowaccounts.md)|<span data-ttu-id="24048-114">WCF サービスをホストし、共有サービスへの接続アクセスが許可されるプロセス用のユーザー アカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="24048-114">Adds a user account for processes that host WCF services, and are granted connection access to the sharing service</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="24048-115">親要素</span><span class="sxs-lookup"><span data-stu-id="24048-115">Parent Elements</span></span>  
  
|<span data-ttu-id="24048-116">要素</span><span class="sxs-lookup"><span data-stu-id="24048-116">Element</span></span>|<span data-ttu-id="24048-117">説明</span><span class="sxs-lookup"><span data-stu-id="24048-117">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="24048-118">[\<net.pipe >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md)または[ \<net.tcp >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span><span class="sxs-lookup"><span data-stu-id="24048-118">[\<net.pipe>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) or [\<net.tcp>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span></span>|<span data-ttu-id="24048-119">Net Pipe または TCP 共有サービスの構成設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="24048-119">Specifies configuration settings for the Net Pipe or TCP sharing services.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="24048-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="24048-120">See Also</span></span>  
 <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
