---
title: bypasslist の &lt;clear&gt; 要素 (ネットワーク設定)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist/clear
- http://schemas.microsoft.com/.NetConfiguration/v2.0#clear
helpviewer_keywords:
- clear element, bypasslist
- <clear> element, bypasslist
- <bypasslist>, clear element
- bypasslist, clear element
ms.assetid: 301584ca-a914-4100-b180-3b288d3b099e
ms.openlocfilehash: 840833f2752115cb5f5639a25daf05bcbff3d452
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720916"
---
# <a name="ltcleargt-element-for-bypasslist-network-settings"></a><span data-ttu-id="4f697-102">bypasslist の &lt;clear&gt; 要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="4f697-102">&lt;clear&gt; Element for bypasslist (Network Settings)</span></span>
<span data-ttu-id="4f697-103">プロキシ バイ パスの一覧をクリアします。</span><span class="sxs-lookup"><span data-stu-id="4f697-103">Clears the proxy bypass list.</span></span>  
  
 <span data-ttu-id="4f697-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="4f697-104">\<configuration></span></span>  
<span data-ttu-id="4f697-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="4f697-105">\<system.net></span></span>  
<span data-ttu-id="4f697-106">\<defaultProxy></span><span class="sxs-lookup"><span data-stu-id="4f697-106">\<defaultProxy></span></span>  
<span data-ttu-id="4f697-107">\<bypasslist></span><span class="sxs-lookup"><span data-stu-id="4f697-107">\<bypasslist></span></span>  
<span data-ttu-id="4f697-108">\<clear></span><span class="sxs-lookup"><span data-stu-id="4f697-108">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f697-109">構文</span><span class="sxs-lookup"><span data-stu-id="4f697-109">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4f697-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="4f697-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4f697-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f697-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4f697-112">属性</span><span class="sxs-lookup"><span data-stu-id="4f697-112">Attributes</span></span>  
 <span data-ttu-id="4f697-113">なし。</span><span class="sxs-lookup"><span data-stu-id="4f697-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4f697-114">子要素</span><span class="sxs-lookup"><span data-stu-id="4f697-114">Child Elements</span></span>  
 <span data-ttu-id="4f697-115">なし。</span><span class="sxs-lookup"><span data-stu-id="4f697-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4f697-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4f697-116">Parent Elements</span></span>  
  
|<span data-ttu-id="4f697-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4f697-117">**Element**</span></span>|<span data-ttu-id="4f697-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="4f697-118">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="4f697-119">bypasslist</span><span class="sxs-lookup"><span data-stu-id="4f697-119">bypasslist</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/bypasslist-element-network-settings.md)|<span data-ttu-id="4f697-120">一連のプロキシを使用しないアドレスを記述する正規表現を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f697-120">Provides a set of regular expressions that describe addresses that do not use a proxy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4f697-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="4f697-121">Remarks</span></span>  
 <span data-ttu-id="4f697-122">`clear`要素がバイパス リストからすべてのエントリをクリアします。</span><span class="sxs-lookup"><span data-stu-id="4f697-122">The `clear` element clears all entries from the bypass list.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="4f697-123">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="4f697-123">Configuration Files</span></span>  
 <span data-ttu-id="4f697-124">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f697-124">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="4f697-125">例</span><span class="sxs-lookup"><span data-stu-id="4f697-125">Example</span></span>  
 <span data-ttu-id="4f697-126">次の例では、バイパス一覧をクリアし、バイパス リストに 2 つのアドレスを追加します。</span><span class="sxs-lookup"><span data-stu-id="4f697-126">The following example clears the bypass list and then adds two addresses to the bypass list.</span></span> <span data-ttu-id="4f697-127">1 つ目は、contoso.com ドメイン内のすべてのサーバーでプロキシをバイパスします。2 つ目は、192.168 で IP アドレスが始まるすべてのサーバーでプロキシをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="4f697-127">The first bypasses the proxy for all servers in the contoso.com domain; the second bypasses the proxy for all servers whose IP address begins with 192.168.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <bypasslist>  
         <clear/>  
        <add address="[a-z]+\.contoso\.com$" />  
        <add address="192\.168\.\d{1,3}\.\d{1,3}" />  
      </bypasslist>  
    </defaultProxy>  
  </system.net>  
</configuration>   
```  
  
## <a name="see-also"></a><span data-ttu-id="4f697-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f697-128">See also</span></span>
- <xref:System.Net.WebProxy?displayProperty=nameWithType>
- [<span data-ttu-id="4f697-129">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="4f697-129">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
