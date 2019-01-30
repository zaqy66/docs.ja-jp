---
title: <allowAccounts>
ms.date: 03/30/2017
ms.assetid: 166923a9-a8ac-478f-92f9-529d9667f3a6
ms.openlocfilehash: fd3121146577122446ba82528fc6e46dadbf5033
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255550"
---
# <a name="allowaccounts"></a><span data-ttu-id="00f6b-101">\<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="00f6b-101">\<allowAccounts></span></span>
<span data-ttu-id="00f6b-102">ユーザーがプロセスのアカウントをホストする Windows Communication Foundation (WCF) サービス、および共有サービスへの接続アクセスが許可を指定する構成要素のコレクションを含みます。</span><span class="sxs-lookup"><span data-stu-id="00f6b-102">Contains a collection of configuration elements that specify user accounts for processes that host Windows Communication Foundation (WCF) services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="00f6b-103">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="00f6b-103">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00f6b-104">構文</span><span class="sxs-lookup"><span data-stu-id="00f6b-104">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="00f6b-105">属性および要素</span><span class="sxs-lookup"><span data-stu-id="00f6b-105">Attributes and Elements</span></span>  
 <span data-ttu-id="00f6b-106">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="00f6b-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="00f6b-107">属性</span><span class="sxs-lookup"><span data-stu-id="00f6b-107">Attributes</span></span>  
 <span data-ttu-id="00f6b-108">なし。</span><span class="sxs-lookup"><span data-stu-id="00f6b-108">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="00f6b-109">子要素</span><span class="sxs-lookup"><span data-stu-id="00f6b-109">Child Elements</span></span>  
  
|<span data-ttu-id="00f6b-110">属性</span><span class="sxs-lookup"><span data-stu-id="00f6b-110">Attribute</span></span>|<span data-ttu-id="00f6b-111">説明</span><span class="sxs-lookup"><span data-stu-id="00f6b-111">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="00f6b-112">\<add></span><span class="sxs-lookup"><span data-stu-id="00f6b-112">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowaccounts.md)|<span data-ttu-id="00f6b-113">WCF サービスをホストし、共有サービスへの接続アクセスが許可されるプロセス用のユーザー アカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="00f6b-113">Adds a user account for processes that host WCF services, and are granted connection access to the sharing service</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="00f6b-114">親要素</span><span class="sxs-lookup"><span data-stu-id="00f6b-114">Parent Elements</span></span>  
  
|<span data-ttu-id="00f6b-115">要素</span><span class="sxs-lookup"><span data-stu-id="00f6b-115">Element</span></span>|<span data-ttu-id="00f6b-116">説明</span><span class="sxs-lookup"><span data-stu-id="00f6b-116">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="00f6b-117">[\<net.pipe >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md)または[ \<net.tcp >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span><span class="sxs-lookup"><span data-stu-id="00f6b-117">[\<net.pipe>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) or [\<net.tcp>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span></span>|<span data-ttu-id="00f6b-118">Net Pipe または TCP 共有サービスの構成設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="00f6b-118">Specifies configuration settings for the Net Pipe or TCP sharing services.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="00f6b-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="00f6b-119">See also</span></span>
- <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
