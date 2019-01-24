---
title: '&lt;connectionManagement&gt;要素 (ネットワーク設定)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/connectionManagement
- http://schemas.microsoft.com/.NetConfiguration/v2.0#connectionManagement
helpviewer_keywords:
- <connectionManagement> element
- connectionManagement element
ms.assetid: bedccaab-12a2-4511-8f67-e961f249aec6
ms.openlocfilehash: 28864de79e809968f7efa6f3b052cfd599961854
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54685027"
---
# <a name="ltconnectionmanagementgt-element-network-settings"></a><span data-ttu-id="070f2-102">&lt;connectionManagement&gt;要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="070f2-102">&lt;connectionManagement&gt; Element (Network Settings)</span></span>
<span data-ttu-id="070f2-103">ネットワーク ホストへの接続の最大数を指定します。</span><span class="sxs-lookup"><span data-stu-id="070f2-103">Specifies the maximum number of connections to a network host.</span></span>  
  
 <span data-ttu-id="070f2-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="070f2-104">\<configuration></span></span>  
<span data-ttu-id="070f2-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="070f2-105">\<system.net></span></span>  
<span data-ttu-id="070f2-106">\<connectionManagement></span><span class="sxs-lookup"><span data-stu-id="070f2-106">\<connectionManagement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="070f2-107">構文</span><span class="sxs-lookup"><span data-stu-id="070f2-107">Syntax</span></span>  
  
```xml  
<connectionManagement>   
</connectionManagement>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="070f2-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="070f2-108">Attributes and Elements</span></span>  
 <span data-ttu-id="070f2-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="070f2-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="070f2-110">属性</span><span class="sxs-lookup"><span data-stu-id="070f2-110">Attributes</span></span>  
 <span data-ttu-id="070f2-111">なし。</span><span class="sxs-lookup"><span data-stu-id="070f2-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="070f2-112">子要素</span><span class="sxs-lookup"><span data-stu-id="070f2-112">Child Elements</span></span>  
  
|<span data-ttu-id="070f2-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="070f2-113">**Element**</span></span>|<span data-ttu-id="070f2-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="070f2-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="070f2-115">add</span><span class="sxs-lookup"><span data-stu-id="070f2-115">add</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="070f2-116">IP アドレスまたは DNS 名を接続管理リストに追加します。</span><span class="sxs-lookup"><span data-stu-id="070f2-116">Adds an IP address or DNS name to the connection management list.</span></span>|  
|[<span data-ttu-id="070f2-117">clear</span><span class="sxs-lookup"><span data-stu-id="070f2-117">clear</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="070f2-118">接続の管理の一覧をクリアします。</span><span class="sxs-lookup"><span data-stu-id="070f2-118">Clears the connection management list.</span></span>|  
|[<span data-ttu-id="070f2-119">remove</span><span class="sxs-lookup"><span data-stu-id="070f2-119">remove</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="070f2-120">接続管理リストから IP アドレスまたは DNS 名を削除します。</span><span class="sxs-lookup"><span data-stu-id="070f2-120">Removes an IP address or DNS name from the connection management list.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="070f2-121">親要素</span><span class="sxs-lookup"><span data-stu-id="070f2-121">Parent Elements</span></span>  
  
|<span data-ttu-id="070f2-122">**要素**</span><span class="sxs-lookup"><span data-stu-id="070f2-122">**Element**</span></span>|<span data-ttu-id="070f2-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="070f2-123">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="070f2-124">system.net</span><span class="sxs-lookup"><span data-stu-id="070f2-124">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="070f2-125">.NET Framework がネットワークに接続する方法を指定するための設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="070f2-125">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="070f2-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="070f2-126">Remarks</span></span>  
 <span data-ttu-id="070f2-127">`connectionManagement`要素は、サーバーまたはサーバーのグループに接続の最大数を定義します。</span><span class="sxs-lookup"><span data-stu-id="070f2-127">The `connectionManagement` element defines the maximum number of connections to a server or group of servers.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="070f2-128">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="070f2-128">Configuration Files</span></span>  
 <span data-ttu-id="070f2-129">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="070f2-129">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="070f2-130">例</span><span class="sxs-lookup"><span data-stu-id="070f2-130">Example</span></span>  
 <span data-ttu-id="070f2-131">次の例では、サーバーに 4 つの接続を使用するアプリケーションの構成で`www.contoso.com`とその他のすべてのサーバーに 2 つの接続。</span><span class="sxs-lookup"><span data-stu-id="070f2-131">The following example configures an application to use four connections to the server `www.contoso.com` and two connections to all other servers.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <connectionManagement>  
      <add address = "http://www.contoso.com" maxconnection = "4" />  
      <add address = "*" maxconnection = "2" />  
    </connectionManagement>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="070f2-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="070f2-132">See also</span></span>
- <xref:System.Net.ServicePoint>
- <xref:System.Net.ServicePointManager>
- [<span data-ttu-id="070f2-133">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="070f2-133">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
