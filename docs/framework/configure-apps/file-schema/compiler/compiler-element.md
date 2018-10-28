---
title: '&lt;compiler&gt;要素'
ms.date: 08/14/2018
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#compiler
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.codedom/compilers/compiler
helpviewer_keywords:
- compiler configuration elements, <compiler> element
- <compiler> element
- compiler configuration attributes
- compiler element
ms.assetid: 7a151659-b803-4c27-b5ce-1c4aa0d5a823
author: mcleblanc
ms.author: markl
ms.openlocfilehash: e8c5021b00de503783adb3f1b1dc11964639afbf
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50193541"
---
# <a name="ltcompilergt-element"></a><span data-ttu-id="6bb32-102">&lt;compiler&gt;要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-102">&lt;compiler&gt; Element</span></span>

<span data-ttu-id="6bb32-103">言語プロバイダーのコンパイラ構成属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-103">Specifies the compiler configuration attributes for a language provider.</span></span>

<span data-ttu-id="6bb32-104">\<configuration 要素 > \<system.codedom 要素 > \<compilers 要素 >\<コンパイラ > 要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-104">\<configuration Element> \<system.codedom Element> \<compilers Element> \<compiler> Element</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb32-105">構文</span><span class="sxs-lookup"><span data-stu-id="6bb32-105">Syntax</span></span>

```xml
<compiler
  language="languageName[;...;...]"
  extension="fileExtension[;...;...]"
  type="typeName, assemblyName"
  warningLevel="number"
  compilerOptions="option1 option2"
/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="6bb32-106">属性および要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-106">Attributes and Elements</span></span>

<span data-ttu-id="6bb32-107">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="6bb32-108">属性</span><span class="sxs-lookup"><span data-stu-id="6bb32-108">Attributes</span></span>

|<span data-ttu-id="6bb32-109">属性</span><span class="sxs-lookup"><span data-stu-id="6bb32-109">Attribute</span></span>|<span data-ttu-id="6bb32-110">説明</span><span class="sxs-lookup"><span data-stu-id="6bb32-110">Description</span></span>|
|---------------|-----------------|
|`compilerOptions`|<span data-ttu-id="6bb32-111">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="6bb32-111">Optional attribute.</span></span><br /><br /> <span data-ttu-id="6bb32-112">コンパイルのコンパイラ固有の追加の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-112">Specifies additional compiler-specific arguments for compilation.</span></span> <span data-ttu-id="6bb32-113">値、`compilerOptions`属性は、コンパイラ オプションには、コンパイラのトピックの「通常挙げます。</span><span class="sxs-lookup"><span data-stu-id="6bb32-113">The values for the `compilerOptions` attribute are typically listed in a compiler options topic for the compiler.</span></span>|
|`extension`|<span data-ttu-id="6bb32-114">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="6bb32-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="6bb32-115">言語プロバイダーのソース ファイルによって使用されるファイル名拡張子のセミコロン区切りの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-115">Provides a semicolon-separated list of file name extensions used by source files for the language provider.</span></span> <span data-ttu-id="6bb32-116">たとえば、".cs"とします。</span><span class="sxs-lookup"><span data-stu-id="6bb32-116">For example, ".cs".</span></span>|
|`language`|<span data-ttu-id="6bb32-117">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="6bb32-117">Required attribute.</span></span><br /><br /> <span data-ttu-id="6bb32-118">言語プロバイダーがサポートする言語名のセミコロン区切りの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-118">Provides a semicolon-separated list of language names supported by the language provider.</span></span> <span data-ttu-id="6bb32-119">たとえば、「c#; cs; csharp」。</span><span class="sxs-lookup"><span data-stu-id="6bb32-119">For example, "c#;cs;csharp".</span></span>|
|`type`|<span data-ttu-id="6bb32-120">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="6bb32-120">Required attribute.</span></span><br /><br /> <span data-ttu-id="6bb32-121">プロバイダーの実装を含むアセンブリの名前を含む言語プロバイダーの型名を指定します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-121">Specifies the type name of the language provider, including the name of the assembly containing the provider implementation.</span></span> <span data-ttu-id="6bb32-122">型名で定義されている要件を満たす必要があります[完全修飾型名の指定](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-122">The type name must meet the requirements defined in [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|
|`warningLevel`|<span data-ttu-id="6bb32-123">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="6bb32-123">Optional attribute.</span></span><br /><br /> <span data-ttu-id="6bb32-124">既定のコンパイラ警告レベルを指定します言語プロバイダーがエラーとしてコンパイルの警告を扱いますが、レベルを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-124">Specifies the default compiler warning level; determines the level at which the language provider treats compilation warnings as errors.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="6bb32-125">子要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-125">Child Elements</span></span>

|<span data-ttu-id="6bb32-126">要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-126">Element</span></span>|<span data-ttu-id="6bb32-127">説明</span><span class="sxs-lookup"><span data-stu-id="6bb32-127">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="6bb32-128">\<providerOption > 要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-128">\<providerOption> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/provideroption-element.md)|<span data-ttu-id="6bb32-129">言語プロバイダーのコンパイラ バージョン属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-129">Specifies compiler version attributes for a language provider.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="6bb32-130">親要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-130">Parent Elements</span></span>

|<span data-ttu-id="6bb32-131">要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-131">Element</span></span>|<span data-ttu-id="6bb32-132">説明</span><span class="sxs-lookup"><span data-stu-id="6bb32-132">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="6bb32-133">\<configuration> 要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-133">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="6bb32-134">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="6bb32-134">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|[<span data-ttu-id="6bb32-135">\<system.codedom > 要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-135">\<system.codedom> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)|<span data-ttu-id="6bb32-136">使用可能な言語プロバイダーのコンパイラ構成設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-136">Specifies compiler configuration settings for available language providers.</span></span>|
|[<span data-ttu-id="6bb32-137">\<compilers> 要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-137">\<compilers> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)|<span data-ttu-id="6bb32-138">コンパイラ構成要素のコンテナー0 個以上含む`<compiler>`要素。</span><span class="sxs-lookup"><span data-stu-id="6bb32-138">Container for compiler configuration elements; contains zero or more `<compiler>` elements.</span></span>|

## <a name="remarks"></a><span data-ttu-id="6bb32-139">Remarks</span><span class="sxs-lookup"><span data-stu-id="6bb32-139">Remarks</span></span>

<span data-ttu-id="6bb32-140">各`<compiler>`要素は、特定の言語プロバイダーのコンパイラ構成属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-140">Each `<compiler>` element specifies the compiler configuration attributes for a specific language provider.</span></span> <span data-ttu-id="6bb32-141">プロバイダーでは、 <xref:System.CodeDom.Compiler.CodeDomProvider?displayProperty=nameWithType> ; 特定の言語のクラス、`<compiler>`要素は、コンパイラおよび言語プロバイダー用のコード ジェネレーターの設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-141">The provider extends the <xref:System.CodeDom.Compiler.CodeDomProvider?displayProperty=nameWithType> class for a specific language; the `<compiler>` element defines the compiler and code generator settings for the language provider.</span></span>

<span data-ttu-id="6bb32-142">.NET Framework は、マシン構成ファイル (Machine.config) 内でコンパイラの初期設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-142">The .NET Framework defines the initial compiler settings in the machine configuration file (Machine.config).</span></span> <span data-ttu-id="6bb32-143">開発者やコンパイラ ベンダーは、新しい <xref:System.CodeDom.Compiler.CodeDomProvider> の実装のために構成設定を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="6bb32-143">Developers and compiler vendors can add configuration settings for a new <xref:System.CodeDom.Compiler.CodeDomProvider> implementation.</span></span> <span data-ttu-id="6bb32-144"><xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> メソッドを使用して、プログラムによってコンピューターの言語プロバイダーとコンパイラ構成の設定を列挙します。</span><span class="sxs-lookup"><span data-stu-id="6bb32-144">Use the <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> method to programmatically enumerate language provider and compiler configuration settings on a computer.</span></span>

<span data-ttu-id="6bb32-145">アプリケーションまたは Web 構成ファイルで要素をコンパイラでは、補完したり、コンピューターの構成ファイルで設定を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="6bb32-145">Compiler elements in the application or Web configuration file can supplement or override the settings in the machine configuration file.</span></span> <span data-ttu-id="6bb32-146">同じ言語の名前または同じファイルの拡張機能の 1 つ以上のプロバイダーの実装を構成する場合、最後の一致する構成は、その言語名またはファイル拡張子の前の構成済みのプロバイダーをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="6bb32-146">If more than one provider implementation is configured for the same language name or the same file extension, the last matching configuration overrides any previous configured providers for that language name or file extension.</span></span>

## <a name="configuration-file"></a><span data-ttu-id="6bb32-147">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="6bb32-147">Configuration File</span></span>

<span data-ttu-id="6bb32-148">この要素は、マシン構成ファイルおよびアプリケーション構成ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="6bb32-148">This element can be used in the machine configuration file and the application configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="6bb32-149">例</span><span class="sxs-lookup"><span data-stu-id="6bb32-149">Example</span></span>

<span data-ttu-id="6bb32-150">次の例は、通常のコンパイラ構成要素を示しています。</span><span class="sxs-lookup"><span data-stu-id="6bb32-150">The following example illustrates a typical compiler configuration element:</span></span>

```xml
<configuration>
  <system.codedom>
    <compilers>
      <!-- zero or more compiler elements -->
      <compiler
        language="c#;cs;csharp"
        extension=".cs"
        type="Microsoft.CSharp.CSharpCodeProvider, System,
          Version=2.0.3600.0, Culture=neutral,
          PublicKeyToken=b77a5c561934e089"
        compilerOptions="/optimize"
        warningLevel="1" />
    </compilers>
  </system.codedom>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="6bb32-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="6bb32-151">See Also</span></span>

- <xref:System.CodeDom.Compiler.CompilerInfo>
- <xref:System.CodeDom.Compiler.CodeDomProvider>
- [<span data-ttu-id="6bb32-152">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="6bb32-152">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="6bb32-153">\<compilers> 要素</span><span class="sxs-lookup"><span data-stu-id="6bb32-153">\<compilers> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)
- [<span data-ttu-id="6bb32-154">完全修飾型名の指定</span><span class="sxs-lookup"><span data-stu-id="6bb32-154">Specifying Fully Qualified Type Names</span></span>](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)
- <span data-ttu-id="6bb32-155">[(ASP.NET 設定スキーマ) compilation の compilers の compiler 要素](https://msdn.microsoft.com/library/f7d6b078-5d42-4134-b3f7-62e1aba1df1e(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="6bb32-155">[compiler Element for compilers for compilation (ASP.NET Settings Schema)](https://msdn.microsoft.com/library/f7d6b078-5d42-4134-b3f7-62e1aba1df1e(v=vs.100))</span></span>
