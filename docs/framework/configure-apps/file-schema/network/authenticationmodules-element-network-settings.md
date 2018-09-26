---
title: '&lt;authenticationModules&gt;要素 (ネットワーク設定)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#authenticationModules
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/authenticationModules
helpviewer_keywords:
- authenticationModules element
- <authenticationModules> element
ms.assetid: 10fcfaad-82ef-4692-871a-0aec9dfbe75e
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 394a686fe07036d6c3ac2bc51fb3503e1ee4a9e6
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47170809"
---
# <a name="ltauthenticationmodulesgt-element-network-settings"></a><span data-ttu-id="ea649-102">&lt;authenticationModules&gt;要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="ea649-102">&lt;authenticationModules&gt; Element (Network Settings)</span></span>
<span data-ttu-id="ea649-103">ネットワーク要求の認証に使用されるモジュールを指定します。</span><span class="sxs-lookup"><span data-stu-id="ea649-103">Specifies modules used to authenticate network requests.</span></span>  
  
 <span data-ttu-id="ea649-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="ea649-104">\<configuration></span></span>  
<span data-ttu-id="ea649-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="ea649-105">\<system.net></span></span>  
<span data-ttu-id="ea649-106">\<authenticationModules ></span><span class="sxs-lookup"><span data-stu-id="ea649-106">\<authenticationModules></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea649-107">構文</span><span class="sxs-lookup"><span data-stu-id="ea649-107">Syntax</span></span>  
  
```xml  
<authenticationModules>   
</authenticationModules>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ea649-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="ea649-108">Attributes and Elements</span></span>  
 <span data-ttu-id="ea649-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="ea649-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ea649-110">属性</span><span class="sxs-lookup"><span data-stu-id="ea649-110">Attributes</span></span>  
 <span data-ttu-id="ea649-111">なし。</span><span class="sxs-lookup"><span data-stu-id="ea649-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="ea649-112">子要素</span><span class="sxs-lookup"><span data-stu-id="ea649-112">Child Elements</span></span>  
  
|<span data-ttu-id="ea649-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="ea649-113">**Element**</span></span>|<span data-ttu-id="ea649-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea649-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="ea649-115">add</span><span class="sxs-lookup"><span data-stu-id="ea649-115">add</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-authenticationmodules-network-settings.md)|<span data-ttu-id="ea649-116">アプリケーションに認証モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="ea649-116">Adds an authentication module to the application.</span></span>|  
|[<span data-ttu-id="ea649-117">clear</span><span class="sxs-lookup"><span data-stu-id="ea649-117">clear</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-authenticationmodules-network-settings.md)|<span data-ttu-id="ea649-118">アプリケーションからのすべての認証モジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="ea649-118">Clears all authentication modules from the application.</span></span>|  
|[<span data-ttu-id="ea649-119">remove</span><span class="sxs-lookup"><span data-stu-id="ea649-119">remove</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-authenticationmodules-network-settings.md)|<span data-ttu-id="ea649-120">アプリケーションから認証モジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="ea649-120">Removes an authentication module from the application.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ea649-121">親要素</span><span class="sxs-lookup"><span data-stu-id="ea649-121">Parent Elements</span></span>  
  
|<span data-ttu-id="ea649-122">**要素**</span><span class="sxs-lookup"><span data-stu-id="ea649-122">**Element**</span></span>|<span data-ttu-id="ea649-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea649-123">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="ea649-124">system.net</span><span class="sxs-lookup"><span data-stu-id="ea649-124">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="ea649-125">.NET Framework がネットワークに接続する方法を指定するための設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ea649-125">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ea649-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="ea649-126">Remarks</span></span>  
 <span data-ttu-id="ea649-127">`authenticationModule`要素は、サーバーと認証プロセスを実行する認証モジュールを指定します。</span><span class="sxs-lookup"><span data-stu-id="ea649-127">The `authenticationModule` element specifies the authentication modules that conduct the authentication process with a server.</span></span> <span data-ttu-id="ea649-128">認証モジュールを実装する必要があります、<xref:System.Net.IAuthenticationModule>インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="ea649-128">An authentication module must implement the <xref:System.Net.IAuthenticationModule> interface.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="ea649-129">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="ea649-129">Configuration Files</span></span>  
 <span data-ttu-id="ea649-130">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ea649-130">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ea649-131">例</span><span class="sxs-lookup"><span data-stu-id="ea649-131">Example</span></span>  
 <span data-ttu-id="ea649-132">次の例では、認証モジュールを有効します。</span><span class="sxs-lookup"><span data-stu-id="ea649-132">The following example enables an authentication module.</span></span> <span data-ttu-id="ea649-133">指定したモジュールの正しい値で、バージョンおよび PublicKeyToken の値を置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea649-133">You should replace the values for Version and PublicKeyToken with the correct values for the specified module.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <add type="System.Net.DigestClient, System, Version=2.0.3600.0,  
                 Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
    </authenticationModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ea649-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="ea649-134">See Also</span></span>  
 <xref:System.Net.IAuthenticationModule>  
 <xref:System.Net.AuthenticationManager>  
 [<span data-ttu-id="ea649-135">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="ea649-135">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
