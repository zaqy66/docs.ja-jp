---
title: '&lt;オフ&gt;authenticationModules (ネットワーク設定) の要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/authenticationModules/clear
- http://schemas.microsoft.com/.NetConfiguration/v2.0#clear
helpviewer_keywords:
- clear element, authenticationModules
- <authenticationModules>, clear element
- <clear> element, authenticationModules
- authenticationModules, clear element
ms.assetid: dc522c45-4a80-4831-8955-f7b68a47edfd
ms.openlocfilehash: 42fa6a44891e012300f61f1a11a47537c6739e2c
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2018
ms.locfileid: "50205192"
---
# <a name="ltcleargt-element-for-authenticationmodules-network-settings"></a><span data-ttu-id="08887-102">&lt;オフ&gt;authenticationModules (ネットワーク設定) の要素</span><span class="sxs-lookup"><span data-stu-id="08887-102">&lt;clear&gt; Element for authenticationModules (Network Settings)</span></span>
<span data-ttu-id="08887-103">アプリケーションからのすべての認証モジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="08887-103">Clears all authentication modules from the application.</span></span>  
  
 <span data-ttu-id="08887-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="08887-104">\<configuration></span></span>  
<span data-ttu-id="08887-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="08887-105">\<system.net></span></span>  
<span data-ttu-id="08887-106">\<authenticationModules ></span><span class="sxs-lookup"><span data-stu-id="08887-106">\<authenticationModules></span></span>  
<span data-ttu-id="08887-107">\<クリア ></span><span class="sxs-lookup"><span data-stu-id="08887-107">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08887-108">構文</span><span class="sxs-lookup"><span data-stu-id="08887-108">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="08887-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="08887-109">Attributes and Elements</span></span>  
 <span data-ttu-id="08887-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="08887-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="08887-111">属性</span><span class="sxs-lookup"><span data-stu-id="08887-111">Attributes</span></span>  
 <span data-ttu-id="08887-112">なし。</span><span class="sxs-lookup"><span data-stu-id="08887-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="08887-113">子要素</span><span class="sxs-lookup"><span data-stu-id="08887-113">Child Elements</span></span>  
 <span data-ttu-id="08887-114">なし。</span><span class="sxs-lookup"><span data-stu-id="08887-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="08887-115">親要素</span><span class="sxs-lookup"><span data-stu-id="08887-115">Parent Elements</span></span>  
  
|<span data-ttu-id="08887-116">**要素**</span><span class="sxs-lookup"><span data-stu-id="08887-116">**Element**</span></span>|<span data-ttu-id="08887-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="08887-117">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="08887-118">authenticationModules</span><span class="sxs-lookup"><span data-stu-id="08887-118">authenticationModules</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/authenticationmodules-element-network-settings.md)|<span data-ttu-id="08887-119">ネットワーク要求の認証に使用されるモジュールを指定します。</span><span class="sxs-lookup"><span data-stu-id="08887-119">Specifies modules used to authenticate network requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="08887-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="08887-120">Remarks</span></span>  
 <span data-ttu-id="08887-121">`clear`要素は、構成ファイルで、または構成階層のより高いレベルで既に定義されているすべての認証モジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="08887-121">The `clear` element removes all authentication modules that were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="08887-122">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="08887-122">Configuration Files</span></span>  
 <span data-ttu-id="08887-123">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="08887-123">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="08887-124">例</span><span class="sxs-lookup"><span data-stu-id="08887-124">Example</span></span>  
 <span data-ttu-id="08887-125">次の例では、すべての構成済み認証モジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="08887-125">The following example removes all configured authentication modules.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <clear/>  
    </authenticationModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="08887-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="08887-126">See Also</span></span>  
- <xref:System.Net.IAuthenticationModule>  
- <xref:System.Net.AuthenticationManager>  
- [<span data-ttu-id="08887-127">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="08887-127">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
