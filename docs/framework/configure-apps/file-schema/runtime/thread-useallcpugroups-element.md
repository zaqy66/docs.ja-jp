---
title: '&lt;Thread_UseAllCpuGroups&gt;要素'
ms.date: 03/30/2017
ms.assetid: d30fe7c5-8469-46e2-b804-e3eec7b24256
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 80f67502c61df13b17cfb3b75564d710e5fad2f9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54579942"
---
# <a name="ltthreaduseallcpugroupsgt-element"></a><span data-ttu-id="fbb53-102">&lt;Thread_UseAllCpuGroups&gt;要素</span><span class="sxs-lookup"><span data-stu-id="fbb53-102">&lt;Thread_UseAllCpuGroups&gt; Element</span></span>
<span data-ttu-id="fbb53-103">ランタイムによって、すべての CPU グループにマネージド スレッドを分散するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="fbb53-103">Specifies whether the runtime distributes managed threads across all CPU groups.</span></span>  
  
 <span data-ttu-id="fbb53-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="fbb53-104">\<configuration></span></span>  
<span data-ttu-id="fbb53-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="fbb53-105">\<runtime></span></span>  
<span data-ttu-id="fbb53-106"><Thread_UseAllCpuGroups></span><span class="sxs-lookup"><span data-stu-id="fbb53-106"><Thread_UseAllCpuGroups></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fbb53-107">構文</span><span class="sxs-lookup"><span data-stu-id="fbb53-107">Syntax</span></span>  
  
```xml
<Thread_UseAllCpuGroups    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fbb53-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="fbb53-108">Attributes and Elements</span></span>  
 <span data-ttu-id="fbb53-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="fbb53-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fbb53-110">属性</span><span class="sxs-lookup"><span data-stu-id="fbb53-110">Attributes</span></span>  
  
|<span data-ttu-id="fbb53-111">属性</span><span class="sxs-lookup"><span data-stu-id="fbb53-111">Attribute</span></span>|<span data-ttu-id="fbb53-112">説明</span><span class="sxs-lookup"><span data-stu-id="fbb53-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="fbb53-113">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="fbb53-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="fbb53-114">ランタイムによって、すべての CPU グループにマネージド スレッドを分散するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="fbb53-114">Specifies whether the runtime distributes managed threads across all CPU groups.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="fbb53-115">enabled 属性</span><span class="sxs-lookup"><span data-stu-id="fbb53-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="fbb53-116">値</span><span class="sxs-lookup"><span data-stu-id="fbb53-116">Value</span></span>|<span data-ttu-id="fbb53-117">説明</span><span class="sxs-lookup"><span data-stu-id="fbb53-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="fbb53-118">ランタイムは、複数の CPU グループにマネージド スレッドを分散しません。</span><span class="sxs-lookup"><span data-stu-id="fbb53-118">The runtime does not distribute managed threads across multiple CPU groups.</span></span> <span data-ttu-id="fbb53-119">既定値です。</span><span class="sxs-lookup"><span data-stu-id="fbb53-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="fbb53-120">コンピューターに複数の CPU グループがある場合、ランタイムが複数の CPU グループ全体でマネージ スレッドを分散し、 [ \<GCCpuGroup >](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md)要素が有効にします。</span><span class="sxs-lookup"><span data-stu-id="fbb53-120">The runtime distributes managed threads across multiple CPU groups, if the computer has multiple CPU groups and the [\<GCCpuGroup>](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md) element is enabled.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fbb53-121">子要素</span><span class="sxs-lookup"><span data-stu-id="fbb53-121">Child Elements</span></span>  
 <span data-ttu-id="fbb53-122">なし。</span><span class="sxs-lookup"><span data-stu-id="fbb53-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fbb53-123">親要素</span><span class="sxs-lookup"><span data-stu-id="fbb53-123">Parent Elements</span></span>  
  
|<span data-ttu-id="fbb53-124">要素</span><span class="sxs-lookup"><span data-stu-id="fbb53-124">Element</span></span>|<span data-ttu-id="fbb53-125">説明</span><span class="sxs-lookup"><span data-stu-id="fbb53-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="fbb53-126">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="fbb53-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="fbb53-127">アセンブリのバインディングとガベージ コレクションに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fbb53-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fbb53-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="fbb53-128">Remarks</span></span>  
 <span data-ttu-id="fbb53-129">コンピューターに複数の CPU グループがある場合、この要素を有効にすると、ランタイムは、すべての CPU グループにマネージド スレッドを分散します。</span><span class="sxs-lookup"><span data-stu-id="fbb53-129">When a computer has multiple CPU groups, enabling this element causes the runtime to distribute managed threads across all CPU groups.</span></span> <span data-ttu-id="fbb53-130">この機能を使用する必要がありますも有効にする、 [ \<GCCpuGroup >](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md)要素は、すべての CPU グループにガベージ コレクションを拡張するものを作成して、ヒープを分散するときにすべてのコアになります。</span><span class="sxs-lookup"><span data-stu-id="fbb53-130">To use this feature, you must also enable the [\<GCCpuGroup>](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md) element, which extends garbage collection to all CPU groups and takes all cores into account when creating and balancing heaps.</span></span> <span data-ttu-id="fbb53-131">有効にすると、 [ \<GCCpuGroup >](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md)要素は、有効にする必要があります、 [ \<gcServer >](../../../../../docs/framework/configure-apps/file-schema/runtime/gcserver-element.md)要素。</span><span class="sxs-lookup"><span data-stu-id="fbb53-131">Enabling the [\<GCCpuGroup>](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md) element requires enabling the [\<gcServer>](../../../../../docs/framework/configure-apps/file-schema/runtime/gcserver-element.md) element.</span></span> <span data-ttu-id="fbb53-132">これらの要素が有効でない場合、`<Thread_UseAllCpuGroups>` 要素を有効にしても効力はありません。</span><span class="sxs-lookup"><span data-stu-id="fbb53-132">If these elements are not enabled, enabling the `<Thread_UseAllCpuGroups>` element has no effect.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fbb53-133">例</span><span class="sxs-lookup"><span data-stu-id="fbb53-133">Example</span></span>  
 <span data-ttu-id="fbb53-134">次の例は、複数の CPU グループのサポートを有効にする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fbb53-134">The following example shows how to enable support for multiple CPU groups.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <Thread_UseAllCpuGroups enabled="true"/>  
      <GCCpuGroup enabled="true"/>  
      <gcServer enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="fbb53-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="fbb53-135">See also</span></span>
- [<span data-ttu-id="fbb53-136">ランタイム設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="fbb53-136">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="fbb53-137">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="fbb53-137">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="fbb53-138">\<GCCpuGroup > 要素</span><span class="sxs-lookup"><span data-stu-id="fbb53-138">\<GCCpuGroup> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/gccpugroup-element.md)
