---
title: '&lt;smtp&gt;要素 (ネットワーク設定)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings/smtp
- http://schemas.microsoft.com/.NetConfiguration/v2.0#smtp
helpviewer_keywords:
- <smtp> element
- smtp element
ms.assetid: 220b0329-e384-4e0c-86b4-0945ad17efd9
ms.openlocfilehash: 362c5ba479c845a8183fe705e72ea3a12fb7a94c
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50195646"
---
# <a name="ltsmtpgt-element-network-settings"></a><span data-ttu-id="8c1e3-102">&lt;smtp&gt;要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="8c1e3-102">&lt;smtp&gt; Element (Network Settings)</span></span>
<span data-ttu-id="8c1e3-103">構成の配信形式、配信方法、および送信者の電子メールを送信するためのアドレス。</span><span class="sxs-lookup"><span data-stu-id="8c1e3-103">Configures the delivery format, delivery method, and from address for sending emails.</span></span>  
  
 <span data-ttu-id="8c1e3-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="8c1e3-104">\<configuration></span></span>  
<span data-ttu-id="8c1e3-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="8c1e3-105">\<system.net></span></span>  
<span data-ttu-id="8c1e3-106">\<mailSettings></span><span class="sxs-lookup"><span data-stu-id="8c1e3-106">\<mailSettings></span></span>  
<span data-ttu-id="8c1e3-107">\<smtp></span><span class="sxs-lookup"><span data-stu-id="8c1e3-107">\<smtp></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8c1e3-108">構文</span><span class="sxs-lookup"><span data-stu-id="8c1e3-108">Syntax</span></span>  
  
```xml  
      <smtp  
        deliveryFormat="format"   
        deliveryMethod="method"   
        from="from address">
          <specifiedPickupDirectory> … </ specifiedPickupDirectory >  
          <network> … </network>  
      </smtp>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8c1e3-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="8c1e3-109">Attributes and Elements</span></span>  
 <span data-ttu-id="8c1e3-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="8c1e3-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8c1e3-111">属性</span><span class="sxs-lookup"><span data-stu-id="8c1e3-111">Attributes</span></span>  
  
|<span data-ttu-id="8c1e3-112">属性</span><span class="sxs-lookup"><span data-stu-id="8c1e3-112">Attribute</span></span>|<span data-ttu-id="8c1e3-113">説明</span><span class="sxs-lookup"><span data-stu-id="8c1e3-113">Description</span></span>|  
|---------------|-----------------|  
|`deliveryFormat`|<span data-ttu-id="8c1e3-114">送信電子メールの配信形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="8c1e3-114">Specifies the delivery format for outgoing emails.</span></span> <span data-ttu-id="8c1e3-115">指定できる値は SevenBit および International です。</span><span class="sxs-lookup"><span data-stu-id="8c1e3-115">Acceptable values are SevenBit and International.</span></span>|  
|`deliveryMethod`|<span data-ttu-id="8c1e3-116">電子メールの配信方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="8c1e3-116">Specifies the delivery method for emails.</span></span> <span data-ttu-id="8c1e3-117">使用可能な値は、Network、PickupDirectoryFromIis、および specifiedpickupdirectory です。</span><span class="sxs-lookup"><span data-stu-id="8c1e3-117">Acceptable values are Network, PickupDirectoryFromIis, and SpecifiedPickupDirectory.</span></span>|  
|`from`|<span data-ttu-id="8c1e3-118">指定します、送信電子メールの差出人アドレス。</span><span class="sxs-lookup"><span data-stu-id="8c1e3-118">Specifies the from address for outgoing emails.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8c1e3-119">子要素</span><span class="sxs-lookup"><span data-stu-id="8c1e3-119">Child Elements</span></span>  
  
|<span data-ttu-id="8c1e3-120">属性</span><span class="sxs-lookup"><span data-stu-id="8c1e3-120">Attribute</span></span>|<span data-ttu-id="8c1e3-121">説明</span><span class="sxs-lookup"><span data-stu-id="8c1e3-121">Description</span></span>|  
|---------------|-----------------|  
|`specifiedPickupDirectory`|<span data-ttu-id="8c1e3-122">SMTP (Simple Mail Transport Protocol) サーバー用のローカル ディレクトリを設定します。</span><span class="sxs-lookup"><span data-stu-id="8c1e3-122">Configures the local directory for a Simple Mail Transport Protocol (SMTP) server.</span></span>|  
|`network`|<span data-ttu-id="8c1e3-123">外部 SMTP サーバー用のネットワーク オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="8c1e3-123">Configures the network options for an external SMTP server.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8c1e3-124">親要素</span><span class="sxs-lookup"><span data-stu-id="8c1e3-124">Parent Elements</span></span>  
  
|<span data-ttu-id="8c1e3-125">**要素**</span><span class="sxs-lookup"><span data-stu-id="8c1e3-125">**Element**</span></span>|<span data-ttu-id="8c1e3-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="8c1e3-126">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="8c1e3-127">\<mailSettings> 要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="8c1e3-127">\<mailSettings> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/mailsettings-element-network-settings.md)|<span data-ttu-id="8c1e3-128">電子メールの送信オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="8c1e3-128">Configures mail sending options.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="8c1e3-129">例</span><span class="sxs-lookup"><span data-stu-id="8c1e3-129">Example</span></span>  
 <span data-ttu-id="8c1e3-130">次の例では、既定のネットワーク資格情報を使用して電子メールを送信する適切な SMTP パラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="8c1e3-130">The following example specifies the appropriate SMTP parameters to send email using the default network credentials.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="Network" deliveryFormat="SevenBit"  from="ben@contoso.com">  
        <network  
          host="localhost"  
          port="25"  
          defaultCredentials="true"  
        />  
      </smtp>  
    </mailSettings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="8c1e3-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c1e3-131">See Also</span></span>  
- <xref:System.Net.Configuration.SmtpSection?displayProperty=nameWithType>  
- <xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType>  
- <xref:System.Net.Mail.SmtpDeliveryFormat>  
- <xref:System.Net.Mail.SmtpDeliveryMethod>  
- [<span data-ttu-id="8c1e3-132">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="8c1e3-132">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
