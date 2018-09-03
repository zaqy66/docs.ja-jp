---
title: '&lt;httpDigest&gt; 要素'
ms.date: 03/30/2017
ms.assetid: 3da4f276-dfd9-4247-8c07-01d83618727c
ms.openlocfilehash: 4f3edb4a525429bfc55c4e4cfaffbfc5726dcef8
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43477959"
---
# <a name="lthttpdigestgt-element"></a><span data-ttu-id="4ba2a-102">&lt;httpDigest&gt; 要素</span><span class="sxs-lookup"><span data-stu-id="4ba2a-102">&lt;httpDigest&gt; Element</span></span>
<span data-ttu-id="4ba2a-103">サービスに対するクライアントの認証時に使用されるダイジェスト型の資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-103">Specifies a digest type credential used when authenticating the client to a service.</span></span>  
  
 <span data-ttu-id="4ba2a-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="4ba2a-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="4ba2a-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="4ba2a-105">\<behaviors></span></span>  
<span data-ttu-id="4ba2a-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="4ba2a-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="4ba2a-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4ba2a-107">\<behavior></span></span>  
<span data-ttu-id="4ba2a-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="4ba2a-108">\<clientCredentials></span></span>  
<span data-ttu-id="4ba2a-109">\<httpDigest ></span><span class="sxs-lookup"><span data-stu-id="4ba2a-109">\<httpDigest></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ba2a-110">構文</span><span class="sxs-lookup"><span data-stu-id="4ba2a-110">Syntax</span></span>  
  
```xml  
<digest impersonationLevel="Identification/Impersonation/Delegation/Anonymous/None" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4ba2a-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="4ba2a-111">Attributes and Elements</span></span>  
 <span data-ttu-id="4ba2a-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4ba2a-113">属性</span><span class="sxs-lookup"><span data-stu-id="4ba2a-113">Attributes</span></span>  
  
|<span data-ttu-id="4ba2a-114">属性</span><span class="sxs-lookup"><span data-stu-id="4ba2a-114">Attribute</span></span>|<span data-ttu-id="4ba2a-115">説明</span><span class="sxs-lookup"><span data-stu-id="4ba2a-115">Description</span></span>|  
|---------------|-----------------|  
|`impersonationLevel`|<span data-ttu-id="4ba2a-116">クライアントがサーバーと通信する偽装設定を設定します。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-116">Sets the impersonation preference that the client communicates to the server.</span></span> <span data-ttu-id="4ba2a-117">クライアントが選択する偽装モードは、サーバーでは適用されません。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-117">The impersonation mode that the client selects is not enforced on the server.</span></span> <span data-ttu-id="4ba2a-118">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-118">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="4ba2a-119">識別: サーバーは、id およびクライアントの権限を取得できますが、クライアントを偽装できません。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-119">-   Identification: The server can get the identity and privileges of the client, but cannot impersonate the client.</span></span><br /><span data-ttu-id="4ba2a-120">-Impersonation: サーバーは、ローカル システム上のクライアントのセキュリティ コンテキストを偽装できます。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-120">-   Impersonation: The server can impersonate the client's security context on the local system.</span></span><br /><span data-ttu-id="4ba2a-121">委任: サーバーは、リモート システム上のクライアントのセキュリティ コンテキストを偽装することができます。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-121">-   Delegation: The server can impersonate the client's security context on remote systems.</span></span><br /><span data-ttu-id="4ba2a-122">-Anonymous: サーバーことはできませんの権限を借用またはクライアントを識別します。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-122">-   Anonymous: The server cannot impersonate or identify the client.</span></span><br /><span data-ttu-id="4ba2a-123">-None: 偽装レベルが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-123">-   None: An impersonation level is not assigned.</span></span><br /><br /> <span data-ttu-id="4ba2a-124">既定値は Identification です。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-124">The default is Identification.</span></span> <span data-ttu-id="4ba2a-125">この属性は <xref:System.Security.Principal.TokenImpersonationLevel> 型です。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-125">This attribute is of type <xref:System.Security.Principal.TokenImpersonationLevel>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4ba2a-126">子要素</span><span class="sxs-lookup"><span data-stu-id="4ba2a-126">Child Elements</span></span>  
 <span data-ttu-id="4ba2a-127">なし</span><span class="sxs-lookup"><span data-stu-id="4ba2a-127">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4ba2a-128">親要素</span><span class="sxs-lookup"><span data-stu-id="4ba2a-128">Parent Elements</span></span>  
  
|<span data-ttu-id="4ba2a-129">要素</span><span class="sxs-lookup"><span data-stu-id="4ba2a-129">Element</span></span>|<span data-ttu-id="4ba2a-130">説明</span><span class="sxs-lookup"><span data-stu-id="4ba2a-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4ba2a-131">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="4ba2a-131">\<clientCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|<span data-ttu-id="4ba2a-132">サービスに対するクライアントの認証に使用される資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-132">Specifies the credentials used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4ba2a-133">Remarks</span><span class="sxs-lookup"><span data-stu-id="4ba2a-133">Remarks</span></span>  
 <span data-ttu-id="4ba2a-134">ダイジェストは、アルゴリズムと入力セットを使用して決定されるハッシュです。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-134">A digest is a hash determined by using an algorithm and a set of inputs.</span></span> <span data-ttu-id="4ba2a-135">認証する側と認証される側はアルゴリズムに同意し、入力として使用されるデータを交換します。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-135">The authenticator and the authenticated agree upon an algorithm and exchange the data used as inputs.</span></span> <span data-ttu-id="4ba2a-136">クライアントはハッシュを計算して、サービスに送信できます。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-136">The client can calculate the hash and send it to the service.</span></span> <span data-ttu-id="4ba2a-137">また、サービスもハッシュを計算して、値を比較します。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-137">The service also calculates the hash and compares the values.</span></span> <span data-ttu-id="4ba2a-138">一致すると、クライアントが検証されます。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-138">A match validates the client.</span></span>  
  
 <span data-ttu-id="4ba2a-139">この機能は、Windows の Active Directory およびインターネット インフォメーション サービス (IIS) と共に有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-139">This feature must be enabled with Active Directory on Windows and Internet Information Services (IIS).</span></span> <span data-ttu-id="4ba2a-140">詳細については、次を参照してください。 [Digest Authentication in IIS 6.0](https://go.microsoft.com/fwlink/?LinkId=88443)します。</span><span class="sxs-lookup"><span data-stu-id="4ba2a-140">For more information, see [Digest Authentication in IIS 6.0](https://go.microsoft.com/fwlink/?LinkId=88443).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ba2a-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ba2a-141">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ClientCredentialsElement>  
 <xref:System.ServiceModel.Configuration.ClientCredentialsElement.HttpDigest%2A>  
 <xref:System.ServiceModel.Description.ClientCredentials>  
 <xref:System.ServiceModel.Description.ClientCredentials.HttpDigest%2A>  
 <xref:System.ServiceModel.Configuration.HttpDigestClientElement>  
 <xref:System.ServiceModel.Security.HttpDigestClientCredential>  
 [<span data-ttu-id="4ba2a-142">セキュリティ動作</span><span class="sxs-lookup"><span data-stu-id="4ba2a-142">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)  
 [<span data-ttu-id="4ba2a-143">クライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="4ba2a-143">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)  
 [<span data-ttu-id="4ba2a-144">証明書の使用</span><span class="sxs-lookup"><span data-stu-id="4ba2a-144">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [<span data-ttu-id="4ba2a-145">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="4ba2a-145">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
