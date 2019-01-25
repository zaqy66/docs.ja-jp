---
title: '&lt;allowAccounts&gt; の &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: 763c7b1f-e7b0-4d99-a42c-4506fcb8da00
ms.openlocfilehash: 63f8e678b81838a25664180888e9e7a8eabd043d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722000"
---
# <a name="ltaddgt-of-ltallowaccountsgt"></a><span data-ttu-id="8b0b9-102">&lt;allowAccounts&gt; の &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="8b0b9-102">&lt;add&gt; of &lt;allowAccounts&gt;</span></span>
<span data-ttu-id="8b0b9-103">WCF サービスをホストし、共有サービスへの接続アクセスが許可されるプロセス用のユーザー アカウントを指定します。</span><span class="sxs-lookup"><span data-stu-id="8b0b9-103">Specifies a user account for processes that host WCF services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="8b0b9-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="8b0b9-104">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b0b9-105">構文</span><span class="sxs-lookup"><span data-stu-id="8b0b9-105">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8b0b9-106">属性および要素</span><span class="sxs-lookup"><span data-stu-id="8b0b9-106">Attributes and Elements</span></span>  
 <span data-ttu-id="8b0b9-107">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="8b0b9-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8b0b9-108">属性</span><span class="sxs-lookup"><span data-stu-id="8b0b9-108">Attributes</span></span>  
  
|<span data-ttu-id="8b0b9-109">属性</span><span class="sxs-lookup"><span data-stu-id="8b0b9-109">Attribute</span></span>|<span data-ttu-id="8b0b9-110">説明</span><span class="sxs-lookup"><span data-stu-id="8b0b9-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8b0b9-111">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="8b0b9-111">securityIdentifier</span></span>|<span data-ttu-id="8b0b9-112">ユーザー アカウントの識別に使用される一意の識別子を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="8b0b9-112">A string that specifies a unique identifier used to identify a user account.</span></span> <span data-ttu-id="8b0b9-113">既定値は LocalSystem、Administrators、NS、LS、および IIS_USRS です。</span><span class="sxs-lookup"><span data-stu-id="8b0b9-113">The default values are LocalSystem, Administrators, NS, LS, and IIS_USRS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8b0b9-114">子要素</span><span class="sxs-lookup"><span data-stu-id="8b0b9-114">Child Elements</span></span>  
 <span data-ttu-id="8b0b9-115">なし。</span><span class="sxs-lookup"><span data-stu-id="8b0b9-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8b0b9-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8b0b9-116">Parent Elements</span></span>  
  
|<span data-ttu-id="8b0b9-117">要素</span><span class="sxs-lookup"><span data-stu-id="8b0b9-117">Element</span></span>|<span data-ttu-id="8b0b9-118">説明</span><span class="sxs-lookup"><span data-stu-id="8b0b9-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8b0b9-119">\<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="8b0b9-119">\<allowAccounts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/allowaccounts.md)|<span data-ttu-id="8b0b9-120">格納する構成要素のコレクションを`securityIdentifier`属性を WCF サービスをホストし、共有サービスへの接続アクセスが許可されるプロセスのユーザー アカウントを指定します。</span><span class="sxs-lookup"><span data-stu-id="8b0b9-120">A collection of configuration elements that contain a `securityIdentifier` attribute to specify user accounts for processes that host WCF services, and are granted connection access to the sharing service.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="8b0b9-121">例</span><span class="sxs-lookup"><span data-stu-id="8b0b9-121">Example</span></span>  
 <span data-ttu-id="8b0b9-122">次の構成例は、このコレクションにユーザー アカウントの 5 つの既定の識別子を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b0b9-122">The following configuration example adds the five default identifiers for user accounts to this collection.</span></span>  
  
```xml  
<allowAccounts>
  <!-- LocalSystem account -->
  <add securityIdentifier="S-1-5-18" />
  <!-- LocalService account -->
  <add securityIdentifier="S-1-5-19" />
  <!-- Administrators account -->
  <add securityIdentifier="S-1-5-20" />
  <!-- Network Service account -->
  <add securityIdentifier="S-1-5-32-544" />
  <!-- IIS_IUSRS account (Vista only) -->
  <add securityIdentifier="S-1-5-32-568" />
</allowAccounts>
```  
  
## <a name="see-also"></a><span data-ttu-id="8b0b9-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="8b0b9-123">See also</span></span>
- <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
