---
title: char キーワード (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- char
- char_CSharpKeyword
helpviewer_keywords:
- char data type [C#]
ms.assetid: b51cf4fb-124c-4067-af48-afbac122b228
ms.openlocfilehash: 4d4e4719eabf7dbe31a59cc2e1e3d3d9019f080d
ms.sourcegitcommit: 3b1cb8467bd73dee854b604e306c0e7e3882d91a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "43742027"
---
# <a name="char-c-reference"></a><span data-ttu-id="4fb3b-102">char (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="4fb3b-102">char (C# Reference)</span></span>

<span data-ttu-id="4fb3b-103">`char` キーワードは、Unicode 文字を表すために .NET Framework によって使用される <xref:System.Char?displayProperty=nameWithType> 構造体のインスタンスを宣言するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="4fb3b-103">The `char` keyword is used to declare an instance of the <xref:System.Char?displayProperty=nameWithType> structure that the .NET Framework uses to represent a Unicode character.</span></span> <span data-ttu-id="4fb3b-104">`Char` オブジェクトの値は、16 ビット数 (序数) 値です。</span><span class="sxs-lookup"><span data-stu-id="4fb3b-104">The value of a `Char` object is a 16-bit numeric (ordinal) value.</span></span>

 <span data-ttu-id="4fb3b-105">Unicode 文字は、世界各国の文字言語の大半を表すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4fb3b-105">Unicode characters are used to represent most of the written languages throughout the world.</span></span>

|<span data-ttu-id="4fb3b-106">型</span><span class="sxs-lookup"><span data-stu-id="4fb3b-106">Type</span></span>|<span data-ttu-id="4fb3b-107">範囲</span><span class="sxs-lookup"><span data-stu-id="4fb3b-107">Range</span></span>|<span data-ttu-id="4fb3b-108">サイズ</span><span class="sxs-lookup"><span data-stu-id="4fb3b-108">Size</span></span>|<span data-ttu-id="4fb3b-109">.NET 型</span><span class="sxs-lookup"><span data-stu-id="4fb3b-109">.NET type</span></span>|
|----------|-----------|----------|-------------------------|
|`char`|<span data-ttu-id="4fb3b-110">U+0000 ～ U+FFFF</span><span class="sxs-lookup"><span data-stu-id="4fb3b-110">U+0000 to U+FFFF</span></span>|<span data-ttu-id="4fb3b-111">Unicode 16 ビット文字</span><span class="sxs-lookup"><span data-stu-id="4fb3b-111">Unicode 16-bit character</span></span>|<xref:System.Char?displayProperty=nameWithType>|

## <a name="literals"></a><span data-ttu-id="4fb3b-112">リテラル</span><span class="sxs-lookup"><span data-stu-id="4fb3b-112">Literals</span></span>

<span data-ttu-id="4fb3b-113">`char` 型の定数は、文字リテラル、16 進数のエスケープ シーケンス、または Unicode 表現として記述できます。</span><span class="sxs-lookup"><span data-stu-id="4fb3b-113">Constants of the `char` type can be written as character literals, hexadecimal escape sequence, or Unicode representation.</span></span> <span data-ttu-id="4fb3b-114">また、整数の文字コードをキャストすることもできます。</span><span class="sxs-lookup"><span data-stu-id="4fb3b-114">You can also cast the integral character codes.</span></span> <span data-ttu-id="4fb3b-115">次の例では、4 つの `char` 変数が `X` という同じ文字で初期化されています。</span><span class="sxs-lookup"><span data-stu-id="4fb3b-115">In the following example four `char` variables are initialized with the same character `X`:</span></span>

[!code-csharp[csrefKeywordsTypes#19](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#19)]

## <a name="conversions"></a><span data-ttu-id="4fb3b-116">変換</span><span class="sxs-lookup"><span data-stu-id="4fb3b-116">Conversions</span></span>

<span data-ttu-id="4fb3b-117">`char` は、[ushort](../../../csharp/language-reference/keywords/ushort.md)、[int](../../../csharp/language-reference/keywords/int.md)、[uint](../../../csharp/language-reference/keywords/uint.md)、[long](../../../csharp/language-reference/keywords/long.md)、[ulong](../../../csharp/language-reference/keywords/ulong.md)、[float](../../../csharp/language-reference/keywords/float.md)、[double](../../../csharp/language-reference/keywords/double.md)、または [decimal](../../../csharp/language-reference/keywords/decimal.md) に暗黙的に変換できます。</span><span class="sxs-lookup"><span data-stu-id="4fb3b-117">A `char` can be implicitly converted to [ushort](../../../csharp/language-reference/keywords/ushort.md), [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md), [ulong](../../../csharp/language-reference/keywords/ulong.md), [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md), or [decimal](../../../csharp/language-reference/keywords/decimal.md).</span></span> <span data-ttu-id="4fb3b-118">ただし、他の型から `char` 型へと暗黙的に変換することはできません。</span><span class="sxs-lookup"><span data-stu-id="4fb3b-118">However, there are no implicit conversions from other types to the `char` type.</span></span>

<span data-ttu-id="4fb3b-119"><xref:System.Char?displayProperty=nameWithType> 型では、`char` 値を操作するための静的メソッドがいくつか提供されています。</span><span class="sxs-lookup"><span data-stu-id="4fb3b-119">The <xref:System.Char?displayProperty=nameWithType> type provides several static methods for working with `char` values.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="4fb3b-120">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="4fb3b-120">C# language specification</span></span>  

<span data-ttu-id="4fb3b-121">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[整数型](~/_csharplang/spec/types.md#integral-types)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4fb3b-121">For more information, see [Integral types](~/_csharplang/spec/types.md#integral-types) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="4fb3b-122">言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。</span><span class="sxs-lookup"><span data-stu-id="4fb3b-122">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="4fb3b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="4fb3b-123">See also</span></span>

- <xref:System.Char>  
- [<span data-ttu-id="4fb3b-124">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="4fb3b-124">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="4fb3b-125">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="4fb3b-125">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="4fb3b-126">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="4fb3b-126">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="4fb3b-127">整数型の一覧表</span><span class="sxs-lookup"><span data-stu-id="4fb3b-127">Integral Types Table</span></span>](../../../csharp/language-reference/keywords/integral-types-table.md)  
- [<span data-ttu-id="4fb3b-128">組み込み型の一覧表</span><span class="sxs-lookup"><span data-stu-id="4fb3b-128">Built-In Types Table</span></span>](../../../csharp/language-reference/keywords/built-in-types-table.md)  
- [<span data-ttu-id="4fb3b-129">暗黙的な数値変換の一覧表</span><span class="sxs-lookup"><span data-stu-id="4fb3b-129">Implicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)  
- [<span data-ttu-id="4fb3b-130">明示的な数値変換の一覧表</span><span class="sxs-lookup"><span data-stu-id="4fb3b-130">Explicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)  
- [<span data-ttu-id="4fb3b-131">Null 許容型</span><span class="sxs-lookup"><span data-stu-id="4fb3b-131">Nullable Types</span></span>](../../../csharp/programming-guide/nullable-types/index.md)  
- [<span data-ttu-id="4fb3b-132">文字列</span><span class="sxs-lookup"><span data-stu-id="4fb3b-132">Strings</span></span>](../../../csharp/programming-guide/strings/index.md)