---
title: '&lt;serviceCredential&gt; の &lt;secureConversationAuthentication&gt;'
ms.date: 03/30/2017
ms.assetid: 0bd3fac7-befd-4a45-ba51-c200b33be0fd
ms.openlocfilehash: 8433ac8f698f3e5569802a8d76f7dedaf22f53c3
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50180378"
---
# <a name="ltsecureconversationauthenticationgt-of-ltservicecredentialgt"></a><span data-ttu-id="2d18a-102">&lt;serviceCredential&gt; の &lt;secureConversationAuthentication&gt;</span><span class="sxs-lookup"><span data-stu-id="2d18a-102">&lt;secureConversationAuthentication&gt; of &lt;serviceCredential&gt;</span></span>
<span data-ttu-id="2d18a-103">安全な会話サービスの設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="2d18a-103">Specifies the settings for a secure conversation service.</span></span>  
  
 <span data-ttu-id="2d18a-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="2d18a-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="2d18a-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="2d18a-105">\<behaviors></span></span>  
<span data-ttu-id="2d18a-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="2d18a-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="2d18a-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="2d18a-107">\<behavior></span></span>  
<span data-ttu-id="2d18a-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="2d18a-108">\<serviceCredentials></span></span>  
<span data-ttu-id="2d18a-109">\<secureConversationAuthentication ></span><span class="sxs-lookup"><span data-stu-id="2d18a-109">\<secureConversationAuthentication></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d18a-110">構文</span><span class="sxs-lookup"><span data-stu-id="2d18a-110">Syntax</span></span>  
  
```xml  
<secureConversationAuthentication securityStateEncoderType="String" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2d18a-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="2d18a-111">Attributes and Elements</span></span>  
 <span data-ttu-id="2d18a-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="2d18a-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2d18a-113">属性</span><span class="sxs-lookup"><span data-stu-id="2d18a-113">Attributes</span></span>  
  
|<span data-ttu-id="2d18a-114">属性</span><span class="sxs-lookup"><span data-stu-id="2d18a-114">Attribute</span></span>|<span data-ttu-id="2d18a-115">説明</span><span class="sxs-lookup"><span data-stu-id="2d18a-115">Description</span></span>|  
|---------------|-----------------|  
|`securityStateEncoderType`|<span data-ttu-id="2d18a-116">使用される <xref:System.ServiceModel.Security.SecurityStateEncoder> の型を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="2d18a-116">A string that specifies the type of <xref:System.ServiceModel.Security.SecurityStateEncoder> to be used.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2d18a-117">子要素</span><span class="sxs-lookup"><span data-stu-id="2d18a-117">Child Elements</span></span>  
 <span data-ttu-id="2d18a-118">なし。</span><span class="sxs-lookup"><span data-stu-id="2d18a-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2d18a-119">親要素</span><span class="sxs-lookup"><span data-stu-id="2d18a-119">Parent Elements</span></span>  
  
|<span data-ttu-id="2d18a-120">要素</span><span class="sxs-lookup"><span data-stu-id="2d18a-120">Element</span></span>|<span data-ttu-id="2d18a-121">説明</span><span class="sxs-lookup"><span data-stu-id="2d18a-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2d18a-122">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="2d18a-122">\<serviceCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|<span data-ttu-id="2d18a-123">サービスの認証に使用される資格情報と、クライアントの資格情報検証関連の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="2d18a-123">Specifies the credential to be used in authenticating the service, and the client credential validation-related settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2d18a-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="2d18a-124">Remarks</span></span>  
 <span data-ttu-id="2d18a-125">この構成要素を使用して、セキュリティ コンテキスト トークン (SCT) クッキーのシリアル化のための既知のクレームの種類のリストと、クッキーの情報をエンコードしてセキュリティで保護するためのエンコーダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="2d18a-125">Use this configuration element to specify a list of known claim types for the Security Context Token (SCT) cookies serialization, as well as an encoder to encode and secure cookies information.</span></span> <span data-ttu-id="2d18a-126">SCT の詳細については、「<xref:System.ServiceModel.Security.SecureConversationServiceCredential>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d18a-126">For more information on SCT, see <xref:System.ServiceModel.Security.SecureConversationServiceCredential>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d18a-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="2d18a-127">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.SecureConversationServiceElement>  
 <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.SecureConversationAuthentication%2A>  
 <xref:System.ServiceModel.Description.ServiceCredentials.SecureConversationAuthentication%2A>  
 <xref:System.ServiceModel.Security.SecureConversationServiceCredential>
