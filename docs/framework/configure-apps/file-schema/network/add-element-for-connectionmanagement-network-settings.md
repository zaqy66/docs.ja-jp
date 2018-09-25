---
title: '&lt;追加&gt;connectionManagement (ネットワーク設定) の要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#add
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/connectionManagement/add
helpviewer_keywords:
- <add> element, connectionManagement
- <connectionManagement>, add element
- add element, connectionManagement
- connectionManagement, add element
ms.assetid: 856bf57d-1c63-46c7-a178-03d97b0a4149
author: mcleblanc
ms.author: markl
ms.openlocfilehash: cdc7e8501f7cf3f5cff4c29ca5b2d004ce7cd5c6
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47080326"
---
# <a name="ltaddgt-element-for-connectionmanagement-network-settings"></a><span data-ttu-id="dce66-102">&lt;追加&gt;connectionManagement (ネットワーク設定) の要素</span><span class="sxs-lookup"><span data-stu-id="dce66-102">&lt;add&gt; Element for connectionManagement (Network Settings)</span></span>
<span data-ttu-id="dce66-103">IP アドレスまたは DNS 名を接続管理リストに追加します。</span><span class="sxs-lookup"><span data-stu-id="dce66-103">Adds an IP address or DNS name to the connection management list.</span></span>  
  
 <span data-ttu-id="dce66-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="dce66-104">\<configuration></span></span>  
<span data-ttu-id="dce66-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="dce66-105">\<system.net></span></span>  
<span data-ttu-id="dce66-106">\<connectionManagement ></span><span class="sxs-lookup"><span data-stu-id="dce66-106">\<connectionManagement></span></span>  
<span data-ttu-id="dce66-107">\<add></span><span class="sxs-lookup"><span data-stu-id="dce66-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dce66-108">構文</span><span class="sxs-lookup"><span data-stu-id="dce66-108">Syntax</span></span>  
  
```xml  
<add   
  address="address expression"   
  maxconnection="integer"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dce66-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="dce66-109">Attributes and Elements</span></span>  
 <span data-ttu-id="dce66-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="dce66-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dce66-111">属性</span><span class="sxs-lookup"><span data-stu-id="dce66-111">Attributes</span></span>  
  
|<span data-ttu-id="dce66-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="dce66-112">**Attribute**</span></span>|<span data-ttu-id="dce66-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="dce66-113">**Description**</span></span>|  
|-------------------|---------------------|  
|`address`|<span data-ttu-id="dce66-114">IP アドレスまたは DNS 名を記述する文字列。</span><span class="sxs-lookup"><span data-stu-id="dce66-114">A string describing an IP address or DNS name.</span></span>|  
|`maxconnection`|<span data-ttu-id="dce66-115">サーバーに対して許可される接続の最大数。</span><span class="sxs-lookup"><span data-stu-id="dce66-115">The maximum number of connections allowed to a server.</span></span> <span data-ttu-id="dce66-116">値が指定されていない場合、既定値は 2 です。</span><span class="sxs-lookup"><span data-stu-id="dce66-116">If not supplied, the default is 2.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dce66-117">子要素</span><span class="sxs-lookup"><span data-stu-id="dce66-117">Child Elements</span></span>  
 <span data-ttu-id="dce66-118">なし。</span><span class="sxs-lookup"><span data-stu-id="dce66-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dce66-119">親要素</span><span class="sxs-lookup"><span data-stu-id="dce66-119">Parent Elements</span></span>  
  
|<span data-ttu-id="dce66-120">**要素**</span><span class="sxs-lookup"><span data-stu-id="dce66-120">**Element**</span></span>|<span data-ttu-id="dce66-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="dce66-121">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="dce66-122">connectionManagement</span><span class="sxs-lookup"><span data-stu-id="dce66-122">connectionManagement</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/connectionmanagement-element-network-settings.md)|<span data-ttu-id="dce66-123">ネットワーク ホストへの接続の最大数を指定します。</span><span class="sxs-lookup"><span data-stu-id="dce66-123">Specifies the maximum number of connections to a network host.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dce66-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="dce66-124">Remarks</span></span>  
 <span data-ttu-id="dce66-125">`address` 属性の値は、すべての接続を示すアスタリスク、または形式が `<schema>://<idn_hostname>[:<port>]` の文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="dce66-125">The value of the `address` attribute should be either an asterisk to indicate all connections, or a string of the form `<schema>://<idn_hostname>[:<port>]`.</span></span>  
  
 <span data-ttu-id="dce66-126">HTTP API に渡される URI に Unicode が含まれる場合、punicode 文字列を返す可能性がある <xref:System.Uri.DnsSafeHost%2A> を使用して名前が内部的に変換されます (動作は現行 IDN 構成によって異なる)。</span><span class="sxs-lookup"><span data-stu-id="dce66-126">If the URI passed to any HTTP APIs contains Unicode, the name will be converted internally using <xref:System.Uri.DnsSafeHost%2A> which might return a punicode string (behavior dependent on the current IDN configuration).</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="dce66-127">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="dce66-127">Configuration Files</span></span>  
 <span data-ttu-id="dce66-128">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="dce66-128">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="dce66-129">例</span><span class="sxs-lookup"><span data-stu-id="dce66-129">Example</span></span>  
 <span data-ttu-id="dce66-130">次の例では、サーバー www.contoso.com への 4 つの接続とその他のすべてのサーバーに 2 つの接続を使用するアプリケーションを構成します。</span><span class="sxs-lookup"><span data-stu-id="dce66-130">The following example configures an application to use four connections to the server www.contoso.com and two connections to all other servers.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <connectionManagement>  
      <add address="http://www.contoso.com" maxconnection="4" />  
      <add address="*" maxconnection="2" />  
    </connectionManagement>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="dce66-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="dce66-131">See Also</span></span>  
 <xref:System.Net.ServicePoint>  
 <xref:System.Net.ServicePointManager>  
 [<span data-ttu-id="dce66-132">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="dce66-132">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
