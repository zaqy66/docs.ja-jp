---
title: '&lt;qualifyAssembly&gt;要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#qualifyAssembly
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/qualifyAssembly
helpviewer_keywords:
- container tags, <qualifyAssembly> element
- <qualifyAssembly> element
- qualifyAssembly element
ms.assetid: ad6442f6-1a9d-43b6-b733-04ac1b7f9b82
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 59e3f54f4d3ce0c191193ff63a3c2bce5b93a1bd
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43538032"
---
# <a name="ltqualifyassemblygt-element"></a><span data-ttu-id="e54ad-102">&lt;qualifyAssembly&gt;要素</span><span class="sxs-lookup"><span data-stu-id="e54ad-102">&lt;qualifyAssembly&gt; Element</span></span>
<span data-ttu-id="e54ad-103">部分名が使用された場合に動的に読み込む必要があるアセンブリの完全名を指定します。</span><span class="sxs-lookup"><span data-stu-id="e54ad-103">Specifies the full name of the assembly that should be dynamically loaded when a partial name is used.</span></span>  
  
 <span data-ttu-id="e54ad-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="e54ad-104">\<configuration></span></span>  
<span data-ttu-id="e54ad-105">\<ランタイム ></span><span class="sxs-lookup"><span data-stu-id="e54ad-105">\<runtime></span></span>  
<span data-ttu-id="e54ad-106">\<assemblyBinding></span><span class="sxs-lookup"><span data-stu-id="e54ad-106">\<assemblyBinding></span></span>  
<span data-ttu-id="e54ad-107">\<qualifyAssembly></span><span class="sxs-lookup"><span data-stu-id="e54ad-107">\<qualifyAssembly></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e54ad-108">構文</span><span class="sxs-lookup"><span data-stu-id="e54ad-108">Syntax</span></span>  
  
```xml  
      <qualifyAssembly partialName=  
      "PartialAssemblyName"  
                 fullName="FullAssemblyName"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e54ad-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="e54ad-109">Attributes and Elements</span></span>  
 <span data-ttu-id="e54ad-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e54ad-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e54ad-111">属性</span><span class="sxs-lookup"><span data-stu-id="e54ad-111">Attributes</span></span>  
  
|<span data-ttu-id="e54ad-112">属性</span><span class="sxs-lookup"><span data-stu-id="e54ad-112">Attribute</span></span>|<span data-ttu-id="e54ad-113">説明</span><span class="sxs-lookup"><span data-stu-id="e54ad-113">Description</span></span>|  
|---------------|-----------------|  
|`partialName`|<span data-ttu-id="e54ad-114">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="e54ad-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="e54ad-115">コードに表示されるアセンブリの部分的な名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e54ad-115">Specifies the partial name of the assembly as it appears in the code.</span></span>|  
|`fullName`|<span data-ttu-id="e54ad-116">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="e54ad-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="e54ad-117">グローバル アセンブリ キャッシュに表示されるアセンブリの完全な名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e54ad-117">Specifies the full name of the assembly as it appears in the global assembly cache.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e54ad-118">子要素</span><span class="sxs-lookup"><span data-stu-id="e54ad-118">Child Elements</span></span>  
 <span data-ttu-id="e54ad-119">なし。</span><span class="sxs-lookup"><span data-stu-id="e54ad-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e54ad-120">親要素</span><span class="sxs-lookup"><span data-stu-id="e54ad-120">Parent Elements</span></span>  
  
|<span data-ttu-id="e54ad-121">要素</span><span class="sxs-lookup"><span data-stu-id="e54ad-121">Element</span></span>|<span data-ttu-id="e54ad-122">説明</span><span class="sxs-lookup"><span data-stu-id="e54ad-122">Description</span></span>|  
|-------------|-----------------|  
|`assemblyBinding`|<span data-ttu-id="e54ad-123">アセンブリ バージョンのリダイレクトおよびアセンブリの位置に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e54ad-123">Contains information about assembly version redirection and the locations of assemblies.</span></span>|  
|`configuration`|<span data-ttu-id="e54ad-124">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="e54ad-124">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="e54ad-125">アセンブリのバインディングとガベージ コレクションに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e54ad-125">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e54ad-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="e54ad-126">Remarks</span></span>  
 <span data-ttu-id="e54ad-127">呼び出す、<xref:System.Reflection.Assembly.Load%2A?displayProperty=nameWithType>部分的なアセンブリ名を使用して、メソッドにより、共通言語ランタイム アプリケーション ベース ディレクトリのみでアセンブリを検索します。</span><span class="sxs-lookup"><span data-stu-id="e54ad-127">Calling the <xref:System.Reflection.Assembly.Load%2A?displayProperty=nameWithType> method using partial assembly names causes the common language runtime to look for the assembly only in the application base directory.</span></span> <span data-ttu-id="e54ad-128">使用して、  **\<qualifyAssembly >** (名前、バージョン、公開キー トークン、およびカルチャ) のアセンブリの完全な情報を入力し、検索する共通言語ランタイムが発生する、アプリケーション構成ファイル内の要素グローバル アセンブリ キャッシュ内のアセンブリ。</span><span class="sxs-lookup"><span data-stu-id="e54ad-128">Use the **\<qualifyAssembly>** element in your application configuration file to provide the full assembly information (name, version, public key token, and culture) and cause the common language runtime to search for the assembly in the global assembly cache.</span></span>  
  
 <span data-ttu-id="e54ad-129">**FullName**属性がアセンブリ id の 4 つのフィールドを含める必要があります。 名前、バージョン、公開キー トークン、およびカルチャ。</span><span class="sxs-lookup"><span data-stu-id="e54ad-129">The **fullName** attribute must include the four fields of assembly identity: name, version, public key token, and culture.</span></span> <span data-ttu-id="e54ad-130">**それよりも**属性は、アセンブリを参照部分的にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e54ad-130">The **partialName** attribute must partially reference an assembly.</span></span> <span data-ttu-id="e54ad-131">アセンブリのテキスト名 (最も一般的なケース) を少なくとも指定する必要がありますが、バージョン、公開キー トークン、またはカルチャ (または、4 つが、すべての 4 つの任意の組み合わせ) にも含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e54ad-131">You must specify at least the assembly's text name (the most common case), but you can also include version, public key token, or culture (or any combination of the four, but not all four).</span></span> <span data-ttu-id="e54ad-132">**それよりも**の呼び出しで指定された名前に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e54ad-132">The **partialName** must match the name specified in your call.</span></span> <span data-ttu-id="e54ad-133">たとえば、指定することはできません`"math"`として、**それよりも**、構成ファイルと呼び出し属性`Assembly.Load("math, Version=3.3.3.3")`コードにします。</span><span class="sxs-lookup"><span data-stu-id="e54ad-133">For example, you cannot specify `"math"` as the **partialName** attribute in your configuration file and call `Assembly.Load("math, Version=3.3.3.3")` in your code.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e54ad-134">例</span><span class="sxs-lookup"><span data-stu-id="e54ad-134">Example</span></span>  
 <span data-ttu-id="e54ad-135">次の例は、呼び出しを論理的にオンに`Assembly.Load("math")`に`Assembly.Load("math,version=1.0.0.0,publicKeyToken=a1690a5ea44bab32,culture=neutral")`します。</span><span class="sxs-lookup"><span data-stu-id="e54ad-135">The following example logically turns the call `Assembly.Load("math")` into `Assembly.Load("math,version=1.0.0.0,publicKeyToken=a1690a5ea44bab32,culture=neutral")`.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <qualifyAssembly partialName="math"   
                         fullName=  
"math,version=1.0.0.0,publicKeyToken=a1690a5ea44bab32,culture=neutral"/>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="e54ad-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="e54ad-136">See Also</span></span>  
 [<span data-ttu-id="e54ad-137">ランタイム設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="e54ad-137">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="e54ad-138">ランタイムがアセンブリを検索する方法</span><span class="sxs-lookup"><span data-stu-id="e54ad-138">How the Runtime Locates Assemblies</span></span>](../../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)  
 [<span data-ttu-id="e54ad-139">NIB: 部分アセンブリ参照</span><span class="sxs-lookup"><span data-stu-id="e54ad-139">NIB: Partial Assembly References</span></span>](https://msdn.microsoft.com/library/ec90f07a-398c-4306-9401-0fc5ff9cb59f)
