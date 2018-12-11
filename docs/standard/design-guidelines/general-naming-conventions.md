---
title: 一般的な名前付け規則
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], conflicts
- type names, conflicts
- language-specific type names
- names [.NET Framework], about naming guidelines
- names [.NET Framework], abbreviations
- abbreviation naming guidelines
- acronym naming guidelines
- Hungarian notation
- names [.NET Framework], type names
- names [.NET Framework], acronyms
ms.assetid: d3a77ea1-75d2-4969-a8c3-3e1e3e1aaedc
author: KrzysztofCwalina
ms.openlocfilehash: 9febc7eed7d6dedad6655b51a96694b72b78711b
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53147282"
---
# <a name="general-naming-conventions"></a><span data-ttu-id="69237-102">一般的な名前付け規則</span><span class="sxs-lookup"><span data-stu-id="69237-102">General Naming Conventions</span></span>
<span data-ttu-id="69237-103">このセクションでは、一般的な名前付け規則、単語の選択に関連する言語固有の名前を使用しないようにする方法の省略形と頭字語、および推奨事項の使用に関するガイドラインについて説明します。</span><span class="sxs-lookup"><span data-stu-id="69237-103">This section describes general naming conventions that relate to word choice, guidelines on using abbreviations and acronyms, and recommendations on how to avoid using language-specific names.</span></span>  
  
## <a name="word-choice"></a><span data-ttu-id="69237-104">単語の選択</span><span class="sxs-lookup"><span data-stu-id="69237-104">Word Choice</span></span>  
 <span data-ttu-id="69237-105">**✓ DO** 読みやすい識別子の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="69237-105">**✓ DO** choose easily readable identifier names.</span></span>  
  
 <span data-ttu-id="69237-106">たとえば、という名前のプロパティ`HorizontalAlignment`英語 - よりも読みやすく、`AlignmentHorizontal`します。</span><span class="sxs-lookup"><span data-stu-id="69237-106">For example, a property named `HorizontalAlignment` is more English-readable than `AlignmentHorizontal`.</span></span>  
  
 <span data-ttu-id="69237-107">**✓ DO** 簡潔さよりも読みやすさを優先します。</span><span class="sxs-lookup"><span data-stu-id="69237-107">**✓ DO** favor readability over brevity.</span></span>  
  
 <span data-ttu-id="69237-108">プロパティ名`CanScrollHorizontally`よりは`ScrollableX`(x 軸にあいまいな参照)。</span><span class="sxs-lookup"><span data-stu-id="69237-108">The property name `CanScrollHorizontally` is better than `ScrollableX` (an obscure reference to the X-axis).</span></span>  
  
 <span data-ttu-id="69237-109">**X DO NOT** アンダー スコア、ハイフン、またはその他の英数字以外の文字を使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-109">**X DO NOT** use underscores, hyphens, or any other nonalphanumeric characters.</span></span>  
  
 <span data-ttu-id="69237-110">**X DO NOT** ハンガリアン記法を使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-110">**X DO NOT** use Hungarian notation.</span></span>  
  
 <span data-ttu-id="69237-111">**X AVOID** 広くのキーワードと競合する識別子を使用してプログラミング言語を使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-111">**X AVOID** using identifiers that conflict with keywords of widely used programming languages.</span></span>  
  
 <span data-ttu-id="69237-112">に従って規則 4 の共通言語仕様 (CLS) に準拠しているすべての言語はその言語のキーワードを識別子として使用する名前付きの項目へのアクセスを許可するメカニズムを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="69237-112">According to Rule 4 of the Common Language Specification (CLS), all compliant languages must provide a mechanism that allows access to named items that use a keyword of that language as an identifier.</span></span> <span data-ttu-id="69237-113">C# の場合は、たとえば、使用して、@ 記号にエスケープ メカニズムとして。</span><span class="sxs-lookup"><span data-stu-id="69237-113">C#, for example, uses the @ sign as an escape mechanism in this case.</span></span> <span data-ttu-id="69237-114">ただしはよりもなしで 1 つのエスケープ シーケンスでメソッドを使用するより難しいために、一般的なキーワードを回避することはお勧めもします。</span><span class="sxs-lookup"><span data-stu-id="69237-114">However, it is still a good idea to avoid common keywords because it is much more difficult to use a method with the escape sequence than one without it.</span></span>  
  
## <a name="using-abbreviations-and-acronyms"></a><span data-ttu-id="69237-115">省略形と頭字語を使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-115">Using Abbreviations and Acronyms</span></span>  
 <span data-ttu-id="69237-116">**X DO NOT** 識別子名の一部としての省略形または短縮形を使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-116">**X DO NOT** use abbreviations or contractions as part of identifier names.</span></span>  
  
 <span data-ttu-id="69237-117">たとえば、使用して`GetWindow`なく`GetWin`します。</span><span class="sxs-lookup"><span data-stu-id="69237-117">For example, use `GetWindow` rather than `GetWin`.</span></span>  
  
 <span data-ttu-id="69237-118">**X DO NOT** 広く受け入れられていると偶数の場合は、必要な場合にのみではない任意の頭字語を使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-118">**X DO NOT** use any acronyms that are not widely accepted, and even if they are, only when necessary.</span></span>  
  
## <a name="avoiding-language-specific-names"></a><span data-ttu-id="69237-119">言語固有の名前を回避します。</span><span class="sxs-lookup"><span data-stu-id="69237-119">Avoiding Language-Specific Names</span></span>  
 <span data-ttu-id="69237-120">**✓ DO** 型名に言語固有のキーワードではなく、意味的にわかりやすい名前を使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-120">**✓ DO** use semantically interesting names rather than language-specific keywords for type names.</span></span>  
  
 <span data-ttu-id="69237-121">たとえば、`GetLength`よりもよい名前は、`GetInt`します。</span><span class="sxs-lookup"><span data-stu-id="69237-121">For example, `GetLength` is a better name than `GetInt`.</span></span>  
  
 <span data-ttu-id="69237-122">**✓ DO** まれなケース識別子には、その型以外の意味があるない場合に言語固有の名前ではなく、汎用の CLR 型名を使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-122">**✓ DO** use a generic CLR type name, rather than a language-specific name, in the rare cases when an identifier has no semantic meaning beyond its type.</span></span>  
  
 <span data-ttu-id="69237-123">たとえば、メソッドに変換する<xref:System.Int64>名前を指定する必要があります`ToInt64`ではなく、 `ToLong` (ため<xref:System.Int64>(C#) CLR 名は、-固有のエイリアス`long`)。</span><span class="sxs-lookup"><span data-stu-id="69237-123">For example, a method converting to <xref:System.Int64> should be named `ToInt64`, not `ToLong` (because <xref:System.Int64> is a CLR name for the C#-specific alias `long`).</span></span> <span data-ttu-id="69237-124">次の表は、CLR の型名 (およびその c#、Visual Basic、および C++ の対応する型名) を使用していくつかの基本データ型を表示します。</span><span class="sxs-lookup"><span data-stu-id="69237-124">The following table presents several base data types using the CLR type names (as well as the corresponding type names for C#, Visual Basic, and C++).</span></span>  
  
|<span data-ttu-id="69237-125">C#</span><span class="sxs-lookup"><span data-stu-id="69237-125">C#</span></span>|<span data-ttu-id="69237-126">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="69237-126">Visual Basic</span></span>|<span data-ttu-id="69237-127">C++</span><span class="sxs-lookup"><span data-stu-id="69237-127">C++</span></span>|<span data-ttu-id="69237-128">CLR</span><span class="sxs-lookup"><span data-stu-id="69237-128">CLR</span></span>|  
|---------|------------------|-----------|---------|  
|<span data-ttu-id="69237-129">**sbyte**</span><span class="sxs-lookup"><span data-stu-id="69237-129">**sbyte**</span></span>|<span data-ttu-id="69237-130">**SByte**</span><span class="sxs-lookup"><span data-stu-id="69237-130">**SByte**</span></span>|<span data-ttu-id="69237-131">**char**</span><span class="sxs-lookup"><span data-stu-id="69237-131">**char**</span></span>|<span data-ttu-id="69237-132">**SByte**</span><span class="sxs-lookup"><span data-stu-id="69237-132">**SByte**</span></span>|  
|<span data-ttu-id="69237-133">**byte**</span><span class="sxs-lookup"><span data-stu-id="69237-133">**byte**</span></span>|<span data-ttu-id="69237-134">**Byte**</span><span class="sxs-lookup"><span data-stu-id="69237-134">**Byte**</span></span>|<span data-ttu-id="69237-135">**unsigned char**</span><span class="sxs-lookup"><span data-stu-id="69237-135">**unsigned char**</span></span>|<span data-ttu-id="69237-136">**Byte**</span><span class="sxs-lookup"><span data-stu-id="69237-136">**Byte**</span></span>|  
|<span data-ttu-id="69237-137">**short**</span><span class="sxs-lookup"><span data-stu-id="69237-137">**short**</span></span>|<span data-ttu-id="69237-138">**Short**</span><span class="sxs-lookup"><span data-stu-id="69237-138">**Short**</span></span>|<span data-ttu-id="69237-139">**short**</span><span class="sxs-lookup"><span data-stu-id="69237-139">**short**</span></span>|<span data-ttu-id="69237-140">**Int16**</span><span class="sxs-lookup"><span data-stu-id="69237-140">**Int16**</span></span>|  
|<span data-ttu-id="69237-141">**ushort**</span><span class="sxs-lookup"><span data-stu-id="69237-141">**ushort**</span></span>|<span data-ttu-id="69237-142">**UInt16**</span><span class="sxs-lookup"><span data-stu-id="69237-142">**UInt16**</span></span>|<span data-ttu-id="69237-143">**unsigned short**</span><span class="sxs-lookup"><span data-stu-id="69237-143">**unsigned short**</span></span>|<span data-ttu-id="69237-144">**UInt16**</span><span class="sxs-lookup"><span data-stu-id="69237-144">**UInt16**</span></span>|  
|<span data-ttu-id="69237-145">**int**</span><span class="sxs-lookup"><span data-stu-id="69237-145">**int**</span></span>|<span data-ttu-id="69237-146">**Integer**</span><span class="sxs-lookup"><span data-stu-id="69237-146">**Integer**</span></span>|<span data-ttu-id="69237-147">**int**</span><span class="sxs-lookup"><span data-stu-id="69237-147">**int**</span></span>|<span data-ttu-id="69237-148">**Int32**</span><span class="sxs-lookup"><span data-stu-id="69237-148">**Int32**</span></span>|  
|<span data-ttu-id="69237-149">**uint**</span><span class="sxs-lookup"><span data-stu-id="69237-149">**uint**</span></span>|<span data-ttu-id="69237-150">**UInt32**</span><span class="sxs-lookup"><span data-stu-id="69237-150">**UInt32**</span></span>|<span data-ttu-id="69237-151">**unsigned int**</span><span class="sxs-lookup"><span data-stu-id="69237-151">**unsigned int**</span></span>|<span data-ttu-id="69237-152">**UInt32**</span><span class="sxs-lookup"><span data-stu-id="69237-152">**UInt32**</span></span>|  
|<span data-ttu-id="69237-153">**long**</span><span class="sxs-lookup"><span data-stu-id="69237-153">**long**</span></span>|<span data-ttu-id="69237-154">**Long**</span><span class="sxs-lookup"><span data-stu-id="69237-154">**Long**</span></span>|<span data-ttu-id="69237-155">**__int64**</span><span class="sxs-lookup"><span data-stu-id="69237-155">**__int64**</span></span>|<span data-ttu-id="69237-156">**Int64**</span><span class="sxs-lookup"><span data-stu-id="69237-156">**Int64**</span></span>|  
|<span data-ttu-id="69237-157">**ulong**</span><span class="sxs-lookup"><span data-stu-id="69237-157">**ulong**</span></span>|<span data-ttu-id="69237-158">**UInt64**</span><span class="sxs-lookup"><span data-stu-id="69237-158">**UInt64**</span></span>|<span data-ttu-id="69237-159">**unsigned __int64**</span><span class="sxs-lookup"><span data-stu-id="69237-159">**unsigned __int64**</span></span>|<span data-ttu-id="69237-160">**UInt64**</span><span class="sxs-lookup"><span data-stu-id="69237-160">**UInt64**</span></span>|  
|<span data-ttu-id="69237-161">**float**</span><span class="sxs-lookup"><span data-stu-id="69237-161">**float**</span></span>|<span data-ttu-id="69237-162">**Single**</span><span class="sxs-lookup"><span data-stu-id="69237-162">**Single**</span></span>|<span data-ttu-id="69237-163">**float**</span><span class="sxs-lookup"><span data-stu-id="69237-163">**float**</span></span>|<span data-ttu-id="69237-164">**Single**</span><span class="sxs-lookup"><span data-stu-id="69237-164">**Single**</span></span>|  
|<span data-ttu-id="69237-165">**double**</span><span class="sxs-lookup"><span data-stu-id="69237-165">**double**</span></span>|<span data-ttu-id="69237-166">**Double**</span><span class="sxs-lookup"><span data-stu-id="69237-166">**Double**</span></span>|<span data-ttu-id="69237-167">**double**</span><span class="sxs-lookup"><span data-stu-id="69237-167">**double**</span></span>|<span data-ttu-id="69237-168">**Double**</span><span class="sxs-lookup"><span data-stu-id="69237-168">**Double**</span></span>|  
|<span data-ttu-id="69237-169">**bool**</span><span class="sxs-lookup"><span data-stu-id="69237-169">**bool**</span></span>|<span data-ttu-id="69237-170">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="69237-170">**Boolean**</span></span>|<span data-ttu-id="69237-171">**bool**</span><span class="sxs-lookup"><span data-stu-id="69237-171">**bool**</span></span>|<span data-ttu-id="69237-172">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="69237-172">**Boolean**</span></span>|  
|<span data-ttu-id="69237-173">**char**</span><span class="sxs-lookup"><span data-stu-id="69237-173">**char**</span></span>|<span data-ttu-id="69237-174">**Char**</span><span class="sxs-lookup"><span data-stu-id="69237-174">**Char**</span></span>|<span data-ttu-id="69237-175">**wchar_t**</span><span class="sxs-lookup"><span data-stu-id="69237-175">**wchar_t**</span></span>|<span data-ttu-id="69237-176">**Char**</span><span class="sxs-lookup"><span data-stu-id="69237-176">**Char**</span></span>|  
|<span data-ttu-id="69237-177">**string**</span><span class="sxs-lookup"><span data-stu-id="69237-177">**string**</span></span>|<span data-ttu-id="69237-178">**String**</span><span class="sxs-lookup"><span data-stu-id="69237-178">**String**</span></span>|<span data-ttu-id="69237-179">**String**</span><span class="sxs-lookup"><span data-stu-id="69237-179">**String**</span></span>|<span data-ttu-id="69237-180">**String**</span><span class="sxs-lookup"><span data-stu-id="69237-180">**String**</span></span>|  
|<span data-ttu-id="69237-181">**object**</span><span class="sxs-lookup"><span data-stu-id="69237-181">**object**</span></span>|<span data-ttu-id="69237-182">**Object**</span><span class="sxs-lookup"><span data-stu-id="69237-182">**Object**</span></span>|<span data-ttu-id="69237-183">**Object**</span><span class="sxs-lookup"><span data-stu-id="69237-183">**Object**</span></span>|<span data-ttu-id="69237-184">**Object**</span><span class="sxs-lookup"><span data-stu-id="69237-184">**Object**</span></span>|  
  
 <span data-ttu-id="69237-185">**✓ DO** など、共通名を使用して`value`または`item`、まれなケース識別子は特別な意味を持たないし、パラメーターの型が重要でないときに、型名を繰り返しではなくです。</span><span class="sxs-lookup"><span data-stu-id="69237-185">**✓ DO**  use a common name, such as `value` or `item`, rather than repeating the type name, in the rare cases when an identifier has no semantic meaning and the type of the parameter is not important.</span></span>  
  
## <a name="naming-new-versions-of-existing-apis"></a><span data-ttu-id="69237-186">既存の Api の新しいバージョンの名前を付ける</span><span class="sxs-lookup"><span data-stu-id="69237-186">Naming New Versions of Existing APIs</span></span>  
 <span data-ttu-id="69237-187">**✓ DO** 既存の API の新しいバージョンを作成するときに、古い API への名前を使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-187">**✓ DO** use a name similar to the old API when creating new versions of an existing API.</span></span>  
  
 <span data-ttu-id="69237-188">これにより、Api の間のリレーションシップを強調表示します。</span><span class="sxs-lookup"><span data-stu-id="69237-188">This helps to highlight the relationship between the APIs.</span></span>  
  
 <span data-ttu-id="69237-189">**✓ DO** を既存の API の新しいバージョンを示すプレフィックスではなく、サフィックスを追加することを希望します。</span><span class="sxs-lookup"><span data-stu-id="69237-189">**✓ DO** prefer adding a suffix rather than a prefix to indicate a new version of an existing API.</span></span>  
  
 <span data-ttu-id="69237-190">ドキュメントについてを参照するときに検出を支援はこれまたは IntelliSense を使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-190">This will assist discovery when browsing documentation, or using IntelliSense.</span></span> <span data-ttu-id="69237-191">古いバージョンの API はほとんどのブラウザーと IntelliSense は、アルファベット順に識別子を表示するための新しい Api の近くに編成します。</span><span class="sxs-lookup"><span data-stu-id="69237-191">The old version of the API will be organized close to the new APIs, because most browsers and IntelliSense show identifiers in alphabetical order.</span></span>  
  
 <span data-ttu-id="69237-192">**✓ CONSIDER** サフィックスまたはプリフィックスを追加する代わりに、まったく新しいが意味のある識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-192">**✓ CONSIDER** using a brand new, but meaningful identifier, instead of adding a suffix or a prefix.</span></span>  
  
 <span data-ttu-id="69237-193">**✓ DO** の数値のサフィックスを使用して、既存の API の新しいバージョンを指定する、API の既存の名前 (つまり、業界標準である) 場合は、意味のある唯一の名前は、どの意味を追加する場合は、サフィックス (または、名前を変更する) アプリの場合に特にropriate オプション。</span><span class="sxs-lookup"><span data-stu-id="69237-193">**✓ DO** use a numeric suffix to indicate a new version of an existing API, particularly if the existing name of the API is the only name that makes sense (i.e., if it is an industry standard) and if adding any meaningful suffix (or changing the name) is not an appropriate option.</span></span>  
  
 <span data-ttu-id="69237-194">**X DO NOT** "Ex"(または類似した) を使用して、同じ API の以前のバージョンと区別する識別子のサフィックスです。</span><span class="sxs-lookup"><span data-stu-id="69237-194">**X DO NOT** use the "Ex" (or a similar) suffix for an identifier to distinguish it from an earlier version of the same API.</span></span>  
  
 <span data-ttu-id="69237-195">**✓ DO** 32 ビット整数の代わりに 64 ビット整数 (長整数) で動作する Api のバージョンを導入するときに、「64」サフィックスを使用します。</span><span class="sxs-lookup"><span data-stu-id="69237-195">**✓ DO** use the "64" suffix when introducing versions of APIs that operate on a 64-bit integer (a long integer) instead of a 32-bit integer.</span></span> <span data-ttu-id="69237-196">既存の 32 ビットの API が存在する場合は、この手法を採用するだけで済みますしないため、64 ビット バージョンのみで新しい Api を行います。</span><span class="sxs-lookup"><span data-stu-id="69237-196">You only need to take this approach when the existing 32-bit API exists; don’t do it for brand new APIs with only a 64-bit version.</span></span>  
  
 <span data-ttu-id="69237-197">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="69237-197">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="69237-198">*Pearson Education, Inc. からのアクセス許可によって了承を得て転載[Framework デザイン ガイドライン。規則、手法、および再利用可能な .NET ライブラリの第 2 版のパターン](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)Krzysztof Cwalina、Brad 内容では、Microsoft Windows の開発シリーズの一部として、Addison-wesley Professional、2008 年 10 月 22日を公開します。*</span><span class="sxs-lookup"><span data-stu-id="69237-198">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="69237-199">関連項目</span><span class="sxs-lookup"><span data-stu-id="69237-199">See also</span></span>

- [<span data-ttu-id="69237-200">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="69237-200">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="69237-201">名前付けのガイドライン</span><span class="sxs-lookup"><span data-stu-id="69237-201">Naming Guidelines</span></span>](../../../docs/standard/design-guidelines/naming-guidelines.md)
