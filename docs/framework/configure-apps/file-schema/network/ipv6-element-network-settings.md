---
title: '&lt;ipv6&gt;要素 (ネットワーク設定)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/ipv6
- http://schemas.microsoft.com/.NetConfiguration/v2.0#ipv6
helpviewer_keywords:
- <ipv6> element
- ipv6 element
ms.assetid: 10b79aef-327b-4718-a892-e11f55e4d169
ms.openlocfilehash: 1ca1bb6a0b1a9c3deab9cb3ba15e9b3b2c29f1f7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54531890"
---
# <a name="ltipv6gt-element-network-settings"></a><span data-ttu-id="2e990-102">&lt;ipv6&gt;要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="2e990-102">&lt;ipv6&gt; Element (Network Settings)</span></span>
<span data-ttu-id="2e990-103">により、インターネット プロトコル バージョン 6 (IPv6) の廃止されたメンバーからの応答、<xref:System.Net.Dns>クラス。</span><span class="sxs-lookup"><span data-stu-id="2e990-103">Enables Internet Protocol version 6 (IPv6) responses from obsolete members of the <xref:System.Net.Dns> class.</span></span>  
  
 <span data-ttu-id="2e990-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="2e990-104">\<configuration></span></span>  
<span data-ttu-id="2e990-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="2e990-105">\<system.net></span></span>  
<span data-ttu-id="2e990-106">\<settings></span><span class="sxs-lookup"><span data-stu-id="2e990-106">\<settings></span></span>  
<span data-ttu-id="2e990-107">\<ipv6 ></span><span class="sxs-lookup"><span data-stu-id="2e990-107">\<ipv6></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2e990-108">構文</span><span class="sxs-lookup"><span data-stu-id="2e990-108">Syntax</span></span>  
  
```xml  
<ipv6  
  enabled="true|false"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2e990-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="2e990-109">Attributes and Elements</span></span>  
 <span data-ttu-id="2e990-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="2e990-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2e990-111">属性</span><span class="sxs-lookup"><span data-stu-id="2e990-111">Attributes</span></span>  
  
|<span data-ttu-id="2e990-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="2e990-112">**Attribute**</span></span>|<span data-ttu-id="2e990-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="2e990-113">**Description**</span></span>|  
|-------------------|---------------------|  
|`enabled`|<span data-ttu-id="2e990-114">指定するかどうかのメンバー、<xref:System.Net.Dns>クラスは、インターネット プロトコル バージョン 6 (IPv6) アドレスを返します。</span><span class="sxs-lookup"><span data-stu-id="2e990-114">Specifies whether members of the <xref:System.Net.Dns> class return Internet Protocol version 6 (IPv6) addresses.</span></span> <span data-ttu-id="2e990-115">既定値は `false` です。</span><span class="sxs-lookup"><span data-stu-id="2e990-115">The default value is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2e990-116">子要素</span><span class="sxs-lookup"><span data-stu-id="2e990-116">Child Elements</span></span>  
 <span data-ttu-id="2e990-117">なし。</span><span class="sxs-lookup"><span data-stu-id="2e990-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2e990-118">親要素</span><span class="sxs-lookup"><span data-stu-id="2e990-118">Parent Elements</span></span>  
  
|<span data-ttu-id="2e990-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="2e990-119">**Element**</span></span>|<span data-ttu-id="2e990-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="2e990-120">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="2e990-121">settings</span><span class="sxs-lookup"><span data-stu-id="2e990-121">settings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|<span data-ttu-id="2e990-122"><xref:System.Net> 名前空間の基本的なネットワーク オプションを構成します。</span><span class="sxs-lookup"><span data-stu-id="2e990-122">Configures basic network options for the <xref:System.Net> namespace.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2e990-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="2e990-123">Remarks</span></span>  
 <span data-ttu-id="2e990-124">この設定により、IPv6 のサポートの廃止されたメンバーの<xref:System.Net.Dns>クラス: <xref:System.Net.Dns.BeginGetHostByName%2A>、 <xref:System.Net.Dns.BeginResolve%2A>、 <xref:System.Net.Dns.EndGetHostByName%2A>、 <xref:System.Net.Dns.EndResolve%2A>、 <xref:System.Net.Dns.GetHostByAddress%2A>、 <xref:System.Net.Dns.GetHostByName%2A>、および<xref:System.Net.Dns.Resolve%2A>します。</span><span class="sxs-lookup"><span data-stu-id="2e990-124">This setting enables IPv6 support for the obsolete members of the <xref:System.Net.Dns> class: <xref:System.Net.Dns.BeginGetHostByName%2A>, <xref:System.Net.Dns.BeginResolve%2A>, <xref:System.Net.Dns.EndGetHostByName%2A>, <xref:System.Net.Dns.EndResolve%2A>, <xref:System.Net.Dns.GetHostByAddress%2A>, <xref:System.Net.Dns.GetHostByName%2A>, and <xref:System.Net.Dns.Resolve%2A>.</span></span> <span data-ttu-id="2e990-125">他のメンバー、<xref:System.Net?displayProperty=nameWithType>名前空間、IPv6 アドレスが表示されるオペレーティング システムで IPv6 が有効になっている場合。</span><span class="sxs-lookup"><span data-stu-id="2e990-125">For other members of the <xref:System.Net?displayProperty=nameWithType> namespace, IPv6 addresses may be returned if IPv6 is enabled in the operating system.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="2e990-126">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="2e990-126">Configuration Files</span></span>  
 <span data-ttu-id="2e990-127">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="2e990-127">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2e990-128">例</span><span class="sxs-lookup"><span data-stu-id="2e990-128">Example</span></span>  
 <span data-ttu-id="2e990-129">次の例の IPv6 サポートを有効にする方法を示しています、<xref:System.Net.Dns>クラス。</span><span class="sxs-lookup"><span data-stu-id="2e990-129">The following example shows how to enable IPv6 support for the <xref:System.Net.Dns> class.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <settings>  
      <ipv6 enabled="true"/>  
    </settings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="2e990-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e990-130">See also</span></span>
- <xref:System.Net?displayProperty=nameWithType>
- <xref:System.Net.Dns?displayProperty=nameWithType>
- <xref:System.Net.Sockets.Socket.OSSupportsIPv6%2A?displayProperty=nameWithType>
- [<span data-ttu-id="2e990-131">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="2e990-131">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
