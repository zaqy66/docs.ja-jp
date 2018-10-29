---
title: '&lt;オフ&gt;connectionManagement (ネットワーク設定) の要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/connectionManagement/clear
- http://schemas.microsoft.com/.NetConfiguration/v2.0#clear
helpviewer_keywords:
- <clear> element, connectionManagement
- connectionManagement, clear element
- clear element, connectionManagement
- <connectionManagement>, clear element
ms.assetid: fb259282-84c4-4dc4-a226-78d904a6edc3
ms.openlocfilehash: dba05128220b34bed34da4309a4994cbc4e1bd40
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2018
ms.locfileid: "50205101"
---
# <a name="ltcleargt-element-for-connectionmanagement-network-settings"></a><span data-ttu-id="1e711-102">&lt;オフ&gt;connectionManagement (ネットワーク設定) の要素</span><span class="sxs-lookup"><span data-stu-id="1e711-102">&lt;clear&gt; Element for connectionManagement (Network Settings)</span></span>
<span data-ttu-id="1e711-103">接続の管理の一覧をクリアします。</span><span class="sxs-lookup"><span data-stu-id="1e711-103">Clears the connection management list.</span></span>  
  
 <span data-ttu-id="1e711-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="1e711-104">\<configuration></span></span>  
<span data-ttu-id="1e711-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="1e711-105">\<system.net></span></span>  
<span data-ttu-id="1e711-106">\<connectionManagement ></span><span class="sxs-lookup"><span data-stu-id="1e711-106">\<connectionManagement></span></span>  
<span data-ttu-id="1e711-107">\<クリア ></span><span class="sxs-lookup"><span data-stu-id="1e711-107">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e711-108">構文</span><span class="sxs-lookup"><span data-stu-id="1e711-108">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1e711-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="1e711-109">Attributes and Elements</span></span>  
 <span data-ttu-id="1e711-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="1e711-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1e711-111">属性</span><span class="sxs-lookup"><span data-stu-id="1e711-111">Attributes</span></span>  
 <span data-ttu-id="1e711-112">なし。</span><span class="sxs-lookup"><span data-stu-id="1e711-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1e711-113">子要素</span><span class="sxs-lookup"><span data-stu-id="1e711-113">Child Elements</span></span>  
 <span data-ttu-id="1e711-114">なし。</span><span class="sxs-lookup"><span data-stu-id="1e711-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1e711-115">親要素</span><span class="sxs-lookup"><span data-stu-id="1e711-115">Parent Elements</span></span>  
  
|<span data-ttu-id="1e711-116">**要素**</span><span class="sxs-lookup"><span data-stu-id="1e711-116">**Element**</span></span>|<span data-ttu-id="1e711-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="1e711-117">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="1e711-118">connectionManagement</span><span class="sxs-lookup"><span data-stu-id="1e711-118">connectionManagement</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/connectionmanagement-element-network-settings.md)|<span data-ttu-id="1e711-119">ネットワーク ホストへの接続の最大数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1e711-119">Specifies the maximum number of connections to a network host.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1e711-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="1e711-120">Remarks</span></span>  
 <span data-ttu-id="1e711-121">`clear`要素の接続管理の一覧からすべてのエントリをクリアします。</span><span class="sxs-lookup"><span data-stu-id="1e711-121">The `clear` element clears all entries from the connection management list.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="1e711-122">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="1e711-122">Configuration Files</span></span>  
 <span data-ttu-id="1e711-123">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="1e711-123">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1e711-124">例</span><span class="sxs-lookup"><span data-stu-id="1e711-124">Example</span></span>  
 <span data-ttu-id="1e711-125">次の例は、接続管理の一覧をクリアし、サーバーの接続管理エントリを追加し、`www.contoso.com`およびその他のすべてのネットワーク ホスト。</span><span class="sxs-lookup"><span data-stu-id="1e711-125">The following example clears the connection management list and then adds new connection management entries for the server `www.contoso.com` and all other network hosts.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <connectionManagement>  
      <clear/>  
      <add address = "http://www.contoso.com" maxconnection = "4" />  
      <add address = "*" maxconnection = "2" />  
    </connectionManagement>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1e711-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e711-126">See Also</span></span>  
- <xref:System.Net.ServicePoint>  
- <xref:System.Net.ServicePointManager>  
- [<span data-ttu-id="1e711-127">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="1e711-127">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
