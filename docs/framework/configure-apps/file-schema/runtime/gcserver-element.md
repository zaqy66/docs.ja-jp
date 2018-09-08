---
title: '&lt;gcServer&gt;要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/gcServer
- http://schemas.microsoft.com/.NetConfiguration/v2.0#gcServer
helpviewer_keywords:
- gcServer element
- <gcServer> element
ms.assetid: 8d25b80e-2581-4803-bd87-a59528e3cb03
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8bfe0db3d6fcbdbbcfb90ff488ab19cdbfaab75e
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44216146"
---
# <a name="ltgcservergt-element"></a><span data-ttu-id="55b67-102">&lt;gcServer&gt;要素</span><span class="sxs-lookup"><span data-stu-id="55b67-102">&lt;gcServer&gt; Element</span></span>
<span data-ttu-id="55b67-103">共通言語ランタイムがサーバーのガベージ コレクションを実行するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="55b67-103">Specifies whether the common language runtime runs server garbage collection.</span></span>  
  
 <span data-ttu-id="55b67-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="55b67-104">\<configuration></span></span>  
<span data-ttu-id="55b67-105">\<ランタイム ></span><span class="sxs-lookup"><span data-stu-id="55b67-105">\<runtime></span></span>  
<span data-ttu-id="55b67-106">\<gcServer></span><span class="sxs-lookup"><span data-stu-id="55b67-106">\<gcServer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55b67-107">構文</span><span class="sxs-lookup"><span data-stu-id="55b67-107">Syntax</span></span>  
  
```xml  
<gcServer    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="55b67-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="55b67-108">Attributes and Elements</span></span>  
 <span data-ttu-id="55b67-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="55b67-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="55b67-110">属性</span><span class="sxs-lookup"><span data-stu-id="55b67-110">Attributes</span></span>  
  
|<span data-ttu-id="55b67-111">属性</span><span class="sxs-lookup"><span data-stu-id="55b67-111">Attribute</span></span>|<span data-ttu-id="55b67-112">説明</span><span class="sxs-lookup"><span data-stu-id="55b67-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="55b67-113">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="55b67-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="55b67-114">ランタイムがサーバーのガベージ コレクションを実行するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="55b67-114">Specifies whether the runtime runs server garbage collection.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="55b67-115">enabled 属性</span><span class="sxs-lookup"><span data-stu-id="55b67-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="55b67-116">値</span><span class="sxs-lookup"><span data-stu-id="55b67-116">Value</span></span>|<span data-ttu-id="55b67-117">説明</span><span class="sxs-lookup"><span data-stu-id="55b67-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="55b67-118">サーバーのガベージ コレクションを実行しません。</span><span class="sxs-lookup"><span data-stu-id="55b67-118">Does not run server garbage collection.</span></span> <span data-ttu-id="55b67-119">既定値です。</span><span class="sxs-lookup"><span data-stu-id="55b67-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="55b67-120">サーバーのガベージ コレクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="55b67-120">Runs server garbage collection.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="55b67-121">子要素</span><span class="sxs-lookup"><span data-stu-id="55b67-121">Child Elements</span></span>  
 <span data-ttu-id="55b67-122">なし。</span><span class="sxs-lookup"><span data-stu-id="55b67-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="55b67-123">親要素</span><span class="sxs-lookup"><span data-stu-id="55b67-123">Parent Elements</span></span>  
  
|<span data-ttu-id="55b67-124">要素</span><span class="sxs-lookup"><span data-stu-id="55b67-124">Element</span></span>|<span data-ttu-id="55b67-125">説明</span><span class="sxs-lookup"><span data-stu-id="55b67-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="55b67-126">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="55b67-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="55b67-127">アセンブリのバインディングとガベージ コレクションに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="55b67-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="55b67-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="55b67-128">Remarks</span></span>  
 <span data-ttu-id="55b67-129">共通言語ランタイム (CLR) は、2 種類のガベージ コレクションをサポートしています。1 つはワークステーション ガベージ コレクションで、すべてのシステムで使用できるものです。もう 1 つはサーバー ガベージ コレクションで、マルチプロセッサ システムで使用できるものです。</span><span class="sxs-lookup"><span data-stu-id="55b67-129">The common language runtime (CLR) supports two types of garbage collection: workstation garbage collection, which is available on all systems, and server garbage collection, which is available on multiprocessor systems.</span></span> <span data-ttu-id="55b67-130">`<gcServer>` 要素を使用して、CLR によって実行されるガベージ コレクションの種類を制御します。</span><span class="sxs-lookup"><span data-stu-id="55b67-130">You use the `<gcServer>` element to control the type of garbage collection the CLR performs.</span></span> <span data-ttu-id="55b67-131"><xref:System.Runtime.GCSettings.IsServerGC%2A?displayProperty=nameWithType> プロパティを使用して、サーバー ガベージ コレクションが有効かどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="55b67-131">Use the <xref:System.Runtime.GCSettings.IsServerGC%2A?displayProperty=nameWithType> property to determine if server garbage collection is enabled.</span></span>  
  
 <span data-ttu-id="55b67-132">シングル プロセッサ コンピューターの場合、既定のワークステーション ガベージ コレクションが催促のオプションです。</span><span class="sxs-lookup"><span data-stu-id="55b67-132">For single-processor computers, the default workstation garbage collection should be the fastest option.</span></span> <span data-ttu-id="55b67-133">2 つのプロセッサを搭載するコンピューターで、ワークステーションかサーバーのいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="55b67-133">Either workstation or server can be used for two-processor computers.</span></span> <span data-ttu-id="55b67-134">3 つ以上のプロセッサでは、サーバー ガベージ コレクションが最速のオプションです。</span><span class="sxs-lookup"><span data-stu-id="55b67-134">Server garbage collection should be the fastest option for more than two processors.</span></span>  
  
 <span data-ttu-id="55b67-135">この要素は、アプリケーション構成ファイルでのみ使用できます。要素がマシン構成ファイルにある場合には無視されます。</span><span class="sxs-lookup"><span data-stu-id="55b67-135">This element can be used only in the application configuration file; it is ignored if it is in the machine configuration file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="55b67-136">.NET Framework 4 以前のバージョンでは、サーバー ガベージ コレクションを有効にすると同時実行ガベージ コレクションが使用できません。</span><span class="sxs-lookup"><span data-stu-id="55b67-136">In the .NET Framework 4 and earlier versions, concurrent garbage collection is not available when server garbage collection is enabled.</span></span> <span data-ttu-id="55b67-137">[!INCLUDE[net_v45](../../../../../includes/net-v45-md.md)] 以降では、サーバー ガベージ コレクションは同時実行されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="55b67-137">Starting with the [!INCLUDE[net_v45](../../../../../includes/net-v45-md.md)], server garbage collection is concurrent.</span></span> <span data-ttu-id="55b67-138">非同時実行サーバー ガベージ コレクションを使用する設定、`<gcServer>`要素`true`と[ \<gcConcurrent > 要素](../../../../../docs/framework/configure-apps/file-schema/runtime/gcconcurrent-element.md)に`false`します。</span><span class="sxs-lookup"><span data-stu-id="55b67-138">To use non-concurrent server garbage collection, set the `<gcServer>` element to `true` and the [\<gcConcurrent> element](../../../../../docs/framework/configure-apps/file-schema/runtime/gcconcurrent-element.md) to `false`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="55b67-139">例</span><span class="sxs-lookup"><span data-stu-id="55b67-139">Example</span></span>  
 <span data-ttu-id="55b67-140">サーバー ガベージ コレクションを有効にする方法を次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="55b67-140">The following example enables server garbage collection.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <gcServer enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="55b67-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="55b67-141">See Also</span></span>  
 <xref:System.Runtime.GCSettings.IsServerGC%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="55b67-142">ランタイム設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="55b67-142">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="55b67-143">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="55b67-143">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="55b67-144">方法: 同時実行ガベージ コレクションを無効にします。</span><span class="sxs-lookup"><span data-stu-id="55b67-144">How to: Disable Concurrent Garbage Collection</span></span>](https://msdn.microsoft.com/library/ba2c6c67-5778-497c-9fac-5f793b5500c7)
