---
title: '&lt;CertificateReference&gt;'
ms.date: 03/30/2017
ms.assetid: 2ac8bc14-e9f1-48fb-b662-f5991558fbe4
author: BrucePerlerMS
ms.openlocfilehash: e04dc90134aadfb8af7b0800c7144963d267f513
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47206892"
---
# <a name="ltcertificatereferencegt"></a><span data-ttu-id="24512-102">&lt;CertificateReference&gt;</span><span class="sxs-lookup"><span data-stu-id="24512-102">&lt;certificateReference&gt;</span></span>
<span data-ttu-id="24512-103">検索して、証明書ストアに X.509 証明書の検証に使用される設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="24512-103">Specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span>  
  
 <span data-ttu-id="24512-104">\<system.identityModel.services ></span><span class="sxs-lookup"><span data-stu-id="24512-104">\<system.identityModel.services></span></span>  
<span data-ttu-id="24512-105">\<federationConfiguration ></span><span class="sxs-lookup"><span data-stu-id="24512-105">\<federationConfiguration></span></span>  
<span data-ttu-id="24512-106">\<serviceCertificate ></span><span class="sxs-lookup"><span data-stu-id="24512-106">\<serviceCertificate></span></span>  
<span data-ttu-id="24512-107">\<certificateReference ></span><span class="sxs-lookup"><span data-stu-id="24512-107">\<certificateReference></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24512-108">構文</span><span class="sxs-lookup"><span data-stu-id="24512-108">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <serviceCertificate>  
      <certificateReference   
        storeName="AddressBook||AuthRoot||CertificateAuthority||Disallowed||My||Root||TrustedPeople||TrustedPublisher"  
        storeLocation="CurrentUser||LocalMachine"  
        x509FindType="FindByThumbprint||FindBySubjectName||FindBySubjectDistinguishedName||FindByIssuerName||FindByIssuerDistinguishedName||FindBySerialNumber||FindByTimeValid||FindByTimeNotYetValid||FindByTimeExpired||FindByTemplateName||FindByApplicationPolicy||FindByCertificatePolicy||FindByExtension||FindByKeyUsage||FindBySubjectKeyIdentifier"  
        findValue=xs:String  
        isChainIncluded=xs:Boolean >  
      </certificateReference>  
    </serviceCertificate>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="24512-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="24512-109">Attributes and Elements</span></span>  
 <span data-ttu-id="24512-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="24512-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="24512-111">属性</span><span class="sxs-lookup"><span data-stu-id="24512-111">Attributes</span></span>  
  
|<span data-ttu-id="24512-112">属性</span><span class="sxs-lookup"><span data-stu-id="24512-112">Attribute</span></span>|<span data-ttu-id="24512-113">説明</span><span class="sxs-lookup"><span data-stu-id="24512-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="24512-114">storeName</span><span class="sxs-lookup"><span data-stu-id="24512-114">storeName</span></span>|<span data-ttu-id="24512-115">X.509 証明書ストアの名前。</span><span class="sxs-lookup"><span data-stu-id="24512-115">The name of the X.509 certificate store.</span></span> <span data-ttu-id="24512-116">既定値は"My"です。</span><span class="sxs-lookup"><span data-stu-id="24512-116">The default is "My".</span></span> <span data-ttu-id="24512-117">任意。</span><span class="sxs-lookup"><span data-stu-id="24512-117">Optional.</span></span>|  
|<span data-ttu-id="24512-118">storeLocation</span><span class="sxs-lookup"><span data-stu-id="24512-118">storeLocation</span></span>|<span data-ttu-id="24512-119">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> X.509 証明書ストアの場所を指定する値。</span><span class="sxs-lookup"><span data-stu-id="24512-119">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the location of the X.509 certificate store.</span></span> <span data-ttu-id="24512-120">既定値は、"LocalMachine"です。</span><span class="sxs-lookup"><span data-stu-id="24512-120">The default value is "LocalMachine".</span></span> <span data-ttu-id="24512-121">任意。</span><span class="sxs-lookup"><span data-stu-id="24512-121">Optional.</span></span>|  
|<span data-ttu-id="24512-122">x509FindType</span><span class="sxs-lookup"><span data-stu-id="24512-122">x509FindType</span></span>|<span data-ttu-id="24512-123"><xref:System.Security.Cryptography.X509Certificates.X509FindType>を実行する検索の種類を指定する値。</span><span class="sxs-lookup"><span data-stu-id="24512-123">An <xref:System.Security.Cryptography.X509Certificates.X509FindType> value that specifies the type of search that is to be executed.</span></span> <span data-ttu-id="24512-124">既定値は、「findbysubjectdistinguishedname です」です。</span><span class="sxs-lookup"><span data-stu-id="24512-124">The default is "FindBySubjectDistinguishedName".</span></span> <span data-ttu-id="24512-125">任意。</span><span class="sxs-lookup"><span data-stu-id="24512-125">Optional.</span></span>|  
|<span data-ttu-id="24512-126">findValue</span><span class="sxs-lookup"><span data-stu-id="24512-126">findValue</span></span>|<span data-ttu-id="24512-127">X.509 証明書ストアで検索する値。</span><span class="sxs-lookup"><span data-stu-id="24512-127">The value to search for in the X.509 certificate store.</span></span> <span data-ttu-id="24512-128">任意。</span><span class="sxs-lookup"><span data-stu-id="24512-128">Optional.</span></span>|  
|<span data-ttu-id="24512-129">isChainIncluded</span><span class="sxs-lookup"><span data-stu-id="24512-129">isChainIncluded</span></span>|<span data-ttu-id="24512-130">証明書チェーンを使用して検証を実行するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="24512-130">Specifies whether validation should be performed by using the certificate chain.</span></span> <span data-ttu-id="24512-131">既定値は"true"になります。証明書チェーンを使用して検証します。</span><span class="sxs-lookup"><span data-stu-id="24512-131">The default is "true"; validation is performed by using the certificate chain.</span></span> <span data-ttu-id="24512-132">任意。</span><span class="sxs-lookup"><span data-stu-id="24512-132">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="24512-133">子要素</span><span class="sxs-lookup"><span data-stu-id="24512-133">Child Elements</span></span>  
 <span data-ttu-id="24512-134">なし</span><span class="sxs-lookup"><span data-stu-id="24512-134">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="24512-135">親要素</span><span class="sxs-lookup"><span data-stu-id="24512-135">Parent Elements</span></span>  
  
|<span data-ttu-id="24512-136">要素</span><span class="sxs-lookup"><span data-stu-id="24512-136">Element</span></span>|<span data-ttu-id="24512-137">説明</span><span class="sxs-lookup"><span data-stu-id="24512-137">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="24512-138">\<serviceCertificate ></span><span class="sxs-lookup"><span data-stu-id="24512-138">\<serviceCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/servicecertificate.md)|<span data-ttu-id="24512-139">暗号化し、トークン暗号化解除に使用される証明書を構成します。</span><span class="sxs-lookup"><span data-stu-id="24512-139">Configures the certificate that is used to encrypt and decrypt tokens.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="24512-140">Remarks</span><span class="sxs-lookup"><span data-stu-id="24512-140">Remarks</span></span>  
 <span data-ttu-id="24512-141">`<certificateReference>`要素を検索し、証明書ストアに X.509 証明書の検証に使用される設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="24512-141">The `<certificateReference>` element specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span> <span data-ttu-id="24512-142">子要素として指定されている場合、`<serviceCertficate>`の暗号化し、トークン暗号化解除に使用される X.509 証明書の場所と検証の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="24512-142">When it is specified as the child element of the `<serviceCertficate>` element, it specifies the location and verification settings of the X.509 certificate that is used to encrypt and decrypt tokens.</span></span> <span data-ttu-id="24512-143">`<certificateReference>`要素が表される、<xref:System.ServiceModel.Configuration.CertificateReferenceElement>クラス。</span><span class="sxs-lookup"><span data-stu-id="24512-143">The `<certificateReference>` element is represented by the <xref:System.ServiceModel.Configuration.CertificateReferenceElement> class.</span></span>
