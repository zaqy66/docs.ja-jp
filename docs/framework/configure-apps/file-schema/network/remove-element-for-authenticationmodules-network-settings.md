---
title: authenticationModules の &lt;remove&gt; 要素 (ネットワーク設定)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/authenticationModules/remove
- http://schemas.microsoft.com/.NetConfiguration/v2.0#remove
helpviewer_keywords:
- remove element, authenticationModules
- <authenticationModules>, remove element
- <remove> element, authenticationModules
- authenticationModules, remove element
ms.assetid: abf79949-b05c-465a-b51c-bbeda9a74173
ms.openlocfilehash: 20d90c4554f9718651070456f6d4a14475d88bf6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54651579"
---
# <a name="ltremovegt-element-for-authenticationmodules-network-settings"></a><span data-ttu-id="20ee5-102">authenticationModules の &lt;remove&gt; 要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="20ee5-102">&lt;remove&gt; Element for authenticationModules (Network Settings)</span></span>
<span data-ttu-id="20ee5-103">アプリケーションから認証モジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="20ee5-103">Removes an authentication module from the application.</span></span>  
  
 <span data-ttu-id="20ee5-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="20ee5-104">\<configuration></span></span>  
<span data-ttu-id="20ee5-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="20ee5-105">\<system.net></span></span>  
<span data-ttu-id="20ee5-106">\<authenticationModules></span><span class="sxs-lookup"><span data-stu-id="20ee5-106">\<authenticationModules></span></span>  
<span data-ttu-id="20ee5-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="20ee5-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20ee5-108">構文</span><span class="sxs-lookup"><span data-stu-id="20ee5-108">Syntax</span></span>  
  
```xml  
<remove   
   type="authentication module name"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="20ee5-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="20ee5-109">Attributes and Elements</span></span>  
 <span data-ttu-id="20ee5-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="20ee5-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="20ee5-111">属性</span><span class="sxs-lookup"><span data-stu-id="20ee5-111">Attributes</span></span>  
  
|<span data-ttu-id="20ee5-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="20ee5-112">**Attribute**</span></span>|<span data-ttu-id="20ee5-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="20ee5-113">**Description**</span></span>|  
|-------------------|---------------------|  
|<span data-ttu-id="20ee5-114">**type**</span><span class="sxs-lookup"><span data-stu-id="20ee5-114">**type**</span></span>|<span data-ttu-id="20ee5-115">削除する認証モジュールの名前。</span><span class="sxs-lookup"><span data-stu-id="20ee5-115">The name of the authentication module to remove.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="20ee5-116">子要素</span><span class="sxs-lookup"><span data-stu-id="20ee5-116">Child Elements</span></span>  
 <span data-ttu-id="20ee5-117">なし。</span><span class="sxs-lookup"><span data-stu-id="20ee5-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="20ee5-118">親要素</span><span class="sxs-lookup"><span data-stu-id="20ee5-118">Parent Elements</span></span>  
  
|<span data-ttu-id="20ee5-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="20ee5-119">**Element**</span></span>|<span data-ttu-id="20ee5-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="20ee5-120">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="20ee5-121">authenticationModules</span><span class="sxs-lookup"><span data-stu-id="20ee5-121">authenticationModules</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/authenticationmodules-element-network-settings.md)|<span data-ttu-id="20ee5-122">ネットワーク要求の認証に使用されるモジュールを指定します。</span><span class="sxs-lookup"><span data-stu-id="20ee5-122">Specifies modules used to authenticate network requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="20ee5-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="20ee5-123">Remarks</span></span>  
 <span data-ttu-id="20ee5-124">`remove`要素は、構成ファイルで、または構成階層のより高いレベルで既に定義されている認証モジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="20ee5-124">The `remove` element removes authentication modules that were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>  
  
 <span data-ttu-id="20ee5-125">値、`type`属性が有効なクラス名にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ee5-125">The value for the `type` attribute should be a valid class name.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="20ee5-126">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="20ee5-126">Configuration Files</span></span>  
 <span data-ttu-id="20ee5-127">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="20ee5-127">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="20ee5-128">例</span><span class="sxs-lookup"><span data-stu-id="20ee5-128">Example</span></span>  
 <span data-ttu-id="20ee5-129">次の例では、認証モジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="20ee5-129">The following example removes an authentication module.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <remove type="System.Net.NtlmClient" />  
    </authenticationModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="20ee5-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="20ee5-130">See also</span></span>
- <xref:System.Net.IAuthenticationModule>
- <xref:System.Net.AuthenticationManager>
- [<span data-ttu-id="20ee5-131">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="20ee5-131">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
