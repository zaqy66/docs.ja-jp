---
title: '&lt;ServiceCertificate&gt;'
ms.date: 03/30/2017
ms.assetid: 42c7f291-2ec3-43c5-8872-35897ff3c660
author: BrucePerlerMS
ms.openlocfilehash: 008d2269a72759117658e27ec130cc8cf62cfdfa
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2018
ms.locfileid: "47400414"
---
# <a name="ltservicecertificategt"></a><span data-ttu-id="1d37c-102">&lt;ServiceCertificate&gt;</span><span class="sxs-lookup"><span data-stu-id="1d37c-102">&lt;serviceCertificate&gt;</span></span>
<span data-ttu-id="1d37c-103">暗号化し、トークン暗号化解除に使用される X.509 証明書を構成します。</span><span class="sxs-lookup"><span data-stu-id="1d37c-103">Configures the X.509 certificate that is used to encrypt and decrypt tokens.</span></span>  
  
 <span data-ttu-id="1d37c-104">\<system.identityModel.services ></span><span class="sxs-lookup"><span data-stu-id="1d37c-104">\<system.identityModel.services></span></span>  
<span data-ttu-id="1d37c-105">\<federationConfiguration ></span><span class="sxs-lookup"><span data-stu-id="1d37c-105">\<federationConfiguration></span></span>  
<span data-ttu-id="1d37c-106">\<serviceCertificate ></span><span class="sxs-lookup"><span data-stu-id="1d37c-106">\<serviceCertificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1d37c-107">構文</span><span class="sxs-lookup"><span data-stu-id="1d37c-107">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <serviceCertificate>  
    </serviceCertificate>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1d37c-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="1d37c-108">Attributes and Elements</span></span>  
 <span data-ttu-id="1d37c-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="1d37c-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1d37c-110">属性</span><span class="sxs-lookup"><span data-stu-id="1d37c-110">Attributes</span></span>  
 <span data-ttu-id="1d37c-111">なし</span><span class="sxs-lookup"><span data-stu-id="1d37c-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1d37c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1d37c-112">Child Elements</span></span>  
  
|<span data-ttu-id="1d37c-113">要素</span><span class="sxs-lookup"><span data-stu-id="1d37c-113">Element</span></span>|<span data-ttu-id="1d37c-114">説明</span><span class="sxs-lookup"><span data-stu-id="1d37c-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1d37c-115">\<certificateReference ></span><span class="sxs-lookup"><span data-stu-id="1d37c-115">\<certificateReference></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatereference.md)|<span data-ttu-id="1d37c-116">検索して、証明書ストアに X.509 証明書の検証に使用される設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="1d37c-116">Specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1d37c-117">親要素</span><span class="sxs-lookup"><span data-stu-id="1d37c-117">Parent Elements</span></span>  
  
|<span data-ttu-id="1d37c-118">要素</span><span class="sxs-lookup"><span data-stu-id="1d37c-118">Element</span></span>|<span data-ttu-id="1d37c-119">説明</span><span class="sxs-lookup"><span data-stu-id="1d37c-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1d37c-120">\<federationConfiguration></span><span class="sxs-lookup"><span data-stu-id="1d37c-120">\<federationConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md)|<span data-ttu-id="1d37c-121">構成設定が含まれています、 <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) と<xref:System.IdentityModel.Services.SessionAuthenticationModule>(SAM)。</span><span class="sxs-lookup"><span data-stu-id="1d37c-121">Contains the settings that configure the <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) and the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="1d37c-122">例</span><span class="sxs-lookup"><span data-stu-id="1d37c-122">Example</span></span>  
 <span data-ttu-id="1d37c-123">次の XML の使用を示しています、 \<serviceCertificate > 要素。</span><span class="sxs-lookup"><span data-stu-id="1d37c-123">The following XML shows the use of the \<serviceCertificate> element.</span></span> <span data-ttu-id="1d37c-124">XML から取得されますが、`CustomToken`サンプル。</span><span class="sxs-lookup"><span data-stu-id="1d37c-124">The XML is taken from the `CustomToken` sample.</span></span>  
  
```xml  
<serviceCertificate>  
  <certificateReference x509FindType="FindBySubjectName" findValue="localhost" storeLocation="LocalMachine" storeName="My"/>  
</serviceCertificate>  
```
