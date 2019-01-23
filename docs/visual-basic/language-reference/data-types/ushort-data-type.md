---
title: UShort 型 (Visual Basic)
ms.date: 01/31/2018
f1_keywords:
- vb.ushort
helpviewer_keywords:
- numbers [Visual Basic], whole
- literal type characters [Visual Basic], US
- whole numbers
- integral data types [Visual Basic]
- integer numbers
- numbers [Visual Basic], integer
- integers [Visual Basic], data types
- integers [Visual Basic], types
- data types [Visual Basic], integral
- UShort data type
- US literal type characters [Visual Basic]
ms.assetid: 138db892-665d-4ba8-9cae-d8d91c4a8f39
ms.openlocfilehash: 4b21624ea31fd0e11e598bab435b9f3c6f6d9b9c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54512841"
---
# <a name="ushort-data-type-visual-basic"></a><span data-ttu-id="fd7c3-102">UShort データ型 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fd7c3-102">UShort data type (Visual Basic)</span></span>

<span data-ttu-id="fd7c3-103">保留符号なし 16 ビット (2 バイト) 整数 0 から 65,535 までの範囲します。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-103">Holds unsigned 16-bit (2-byte) integers ranging in value from 0 through 65,535.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fd7c3-104">Remarks</span><span class="sxs-lookup"><span data-stu-id="fd7c3-104">Remarks</span></span>

 <span data-ttu-id="fd7c3-105">使用して、`UShort`データ型に対して大きすぎますバイナリ データを格納する`Byte`します。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-105">Use the `UShort` data type to contain binary data too large for `Byte`.</span></span>  
  
 <span data-ttu-id="fd7c3-106">`UShort` の既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-106">The default value of `UShort` is 0.</span></span>  

## <a name="literal-assignments"></a><span data-ttu-id="fd7c3-107">リテラルの割り当て</span><span class="sxs-lookup"><span data-stu-id="fd7c3-107">Literal assignments</span></span>

<span data-ttu-id="fd7c3-108">宣言し、初期化を`UShort`10 進リテラル、16 進リテラル、8 進数のリテラルを割り当てることや (Visual Basic 2017 以降) バイナリ リテラルでは、変数。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-108">You can declare and initialize a `UShort` variable by assigning it a decimal literal, a hexadecimal literal, an octal literal, or (starting with Visual Basic 2017) a binary literal.</span></span> <span data-ttu-id="fd7c3-109">整数リテラルが `UShort` の範囲外にある場合 (つまり、<xref:System.UInt16.MinValue?displayProperty=nameWithType> より小さいか、<xref:System.UInt16.MaxValue?displayProperty=nameWithType> より大きい場合)、コンパイル エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-109">If the integer literal is outside the range of `UShort` (that is, if it is less than <xref:System.UInt16.MinValue?displayProperty=nameWithType> or greater than <xref:System.UInt16.MaxValue?displayProperty=nameWithType>, a compilation error occurs.</span></span>

<span data-ttu-id="fd7c3-110">次の例では、整数が 16 進数、10 進数として表される 65, 034 を等しくなりに割り当てられているバイナリ リテラル`UShort`値。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-110">In the following example, integers equal to 65,034 that are represented as decimal, hexadecimal, and binary literals are assigned to `UShort` values.</span></span>
  
[!code-vb[UShort](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#UShort)]

> [!NOTE]
> <span data-ttu-id="fd7c3-111">プレフィックスを使用する`&h`または`&H`を 16 進リテラル、プレフィックスを示すために`&b`または`&B`、バイナリ リテラル、およびプレフィックスを示すために`&o`または`&O`を 8 進数のリテラルを示すためにします。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-111">You use the prefix `&h` or `&H` to denote a hexadecimal literal, the prefix `&b` or `&B` to denote a binary literal, and the prefix `&o` or `&O` to denote an octal literal.</span></span> <span data-ttu-id="fd7c3-112">10 進リテラルには、プレフィックスはありません。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-112">Decimal literals have no prefix.</span></span>

<span data-ttu-id="fd7c3-113">Visual Basic 2017 から始めて、使用することできますも、アンダー スコア文字`_`、読みやすさを強化するために、桁区切り記号として次の例として示します。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-113">Starting with Visual Basic 2017, you can also use the underscore character, `_`, as a digit separator to enhance readability, as the following example shows.</span></span>

[!code-vb[UShort](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#UShortS)]

<span data-ttu-id="fd7c3-114">Visual Basic 15.5 以降では、使用することできますもアンダー スコア文字 (`_`) プレフィックスと 16 進数、バイナリ、または 8 進数の桁の間の先頭の区切り記号として。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-114">Starting with Visual Basic 15.5, you can also use the underscore character (`_`) as a leading separator between the prefix and the hexadecimal, binary, or octal digits.</span></span> <span data-ttu-id="fd7c3-115">例:</span><span class="sxs-lookup"><span data-stu-id="fd7c3-115">For example:</span></span>

```vb
Dim number As UShort = &H_FF8C
```

[!INCLUDE [supporting-underscores](../../../../includes/vb-separator-langversion.md)]

<span data-ttu-id="fd7c3-116">数値リテラルを含めることも、`US`または`us`[文字入力](../../programming-guide/language-features/data-types/type-characters.md)を示すために、`UShort`データ型は、次の例を示します。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-116">Numeric literals can also include the `US` or `us` [type character](../../programming-guide/language-features/data-types/type-characters.md) to denote the `UShort` data type, as the following example shows.</span></span>

```vb
Dim number = &H_5826us
```

## <a name="programming-tips"></a><span data-ttu-id="fd7c3-117">プログラミングのヒント</span><span class="sxs-lookup"><span data-stu-id="fd7c3-117">Programming tips</span></span>
  
-   <span data-ttu-id="fd7c3-118">**負の数。**</span><span class="sxs-lookup"><span data-stu-id="fd7c3-118">**Negative Numbers.**</span></span> <span data-ttu-id="fd7c3-119">`UShort`符号なしの型は、負の数を表すことはできません。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-119">Because `UShort` is an unsigned type, it cannot represent a negative number.</span></span> <span data-ttu-id="fd7c3-120">単項マイナスを使用する場合 (`-`) 型に評価される式で演算子`UShort`、Visual Basic の式を変換する`Integer`最初。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-120">If you use the unary minus (`-`) operator on an expression that evaluates to type `UShort`, Visual Basic converts the expression to `Integer` first.</span></span>  
  
-   <span data-ttu-id="fd7c3-121">**CLS 準拠です。**</span><span class="sxs-lookup"><span data-stu-id="fd7c3-121">**CLS Compliance.**</span></span> <span data-ttu-id="fd7c3-122">`UShort`データ型がの一部、[共通言語仕様](https://www.ecma-international.org/publications/standards/Ecma-335.htm)(CLS) に CLS 準拠コードがそれを使用するコンポーネントを使用できないようにします。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-122">The `UShort` data type is not part of the [Common Language Specification](https://www.ecma-international.org/publications/standards/Ecma-335.htm) (CLS), so CLS-compliant code cannot consume a component that uses it.</span></span>
  
-   <span data-ttu-id="fd7c3-123">**拡大します。**</span><span class="sxs-lookup"><span data-stu-id="fd7c3-123">**Widening.**</span></span> <span data-ttu-id="fd7c3-124">`UShort`拡大変換後のデータ型`Integer`、 `UInteger`、 `Long`、 `ULong`、 `Decimal`、 `Single`、および`Double`します。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-124">The `UShort` data type widens to `Integer`, `UInteger`, `Long`, `ULong`, `Decimal`, `Single`, and `Double`.</span></span> <span data-ttu-id="fd7c3-125">つまり、変換できる`UShort`遭遇することがなくこれらの型のいずれにも、<xref:System.OverflowException?displayProperty=nameWithType>エラー。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-125">This means you can convert `UShort` to any of these types without encountering a <xref:System.OverflowException?displayProperty=nameWithType> error.</span></span>  
  
-   <span data-ttu-id="fd7c3-126">**型宣言文字。**</span><span class="sxs-lookup"><span data-stu-id="fd7c3-126">**Type Characters.**</span></span> <span data-ttu-id="fd7c3-127">リテラルの型文字を付加`US`リテラルに強制的に、`UShort`データ型。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-127">Appending the literal type characters `US` to a literal forces it to the `UShort` data type.</span></span> <span data-ttu-id="fd7c3-128">`UShort` 識別子の型文字がありません。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-128">`UShort` has no identifier type character.</span></span>  
  
-   <span data-ttu-id="fd7c3-129">**フレームワークの型。**</span><span class="sxs-lookup"><span data-stu-id="fd7c3-129">**Framework Type.**</span></span> <span data-ttu-id="fd7c3-130">.NET Framework において対応する型は、<xref:System.UInt16?displayProperty=nameWithType> 構造体です。</span><span class="sxs-lookup"><span data-stu-id="fd7c3-130">The corresponding type in the .NET Framework is the <xref:System.UInt16?displayProperty=nameWithType> structure.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd7c3-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd7c3-131">See also</span></span>
- <xref:System.UInt16>
- [<span data-ttu-id="fd7c3-132">データの種類</span><span class="sxs-lookup"><span data-stu-id="fd7c3-132">Data Types</span></span>](../../../visual-basic/language-reference/data-types/index.md)
- [<span data-ttu-id="fd7c3-133">データ型変換関数</span><span class="sxs-lookup"><span data-stu-id="fd7c3-133">Type Conversion Functions</span></span>](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [<span data-ttu-id="fd7c3-134">変換の概要</span><span class="sxs-lookup"><span data-stu-id="fd7c3-134">Conversion Summary</span></span>](../../../visual-basic/language-reference/keywords/conversion-summary.md)
- [<span data-ttu-id="fd7c3-135">方法: 符号なしの型を使用する Windows の機能を呼び出す</span><span class="sxs-lookup"><span data-stu-id="fd7c3-135">How to: Call a Windows Function that Takes Unsigned Types</span></span>](../../../visual-basic/programming-guide/com-interop/how-to-call-a-windows-function-that-takes-unsigned-types.md)
- [<span data-ttu-id="fd7c3-136">データ型の有効な使用方法</span><span class="sxs-lookup"><span data-stu-id="fd7c3-136">Efficient Use of Data Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
