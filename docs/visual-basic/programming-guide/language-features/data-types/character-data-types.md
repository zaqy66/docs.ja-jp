---
title: 文字データ型 (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- data types [Visual Basic], character
- String data type [Visual Basic], character data types
- character data types [Visual Basic]
- Char data type [Visual Basic], character data types
- data types [Visual Basic], choosing
ms.assetid: 902479ef-1679-47fc-9911-0c1c5008226c
ms.openlocfilehash: 3b031c6e3dc04637128f95ca8e922d3298981287
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43863204"
---
# <a name="character-data-types-visual-basic"></a><span data-ttu-id="a0add-102">文字データ型 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a0add-102">Character Data Types (Visual Basic)</span></span>
<span data-ttu-id="a0add-103">Visual Basic では*文字データ型*文字や表示可能な文字を処理します。</span><span class="sxs-lookup"><span data-stu-id="a0add-103">Visual Basic provides *character data types* to deal with printable and displayable characters.</span></span> <span data-ttu-id="a0add-104">Unicode 文字の場合は、どちらも、処理中に`Char`は単一の文字を保持`String`不特定数文字にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a0add-104">While they both deal with Unicode characters, `Char` holds a single character whereas `String` contains an indefinite number of characters.</span></span>  
  
 <span data-ttu-id="a0add-105">Visual Basic のデータ型のサイド バイ サイドで比較を表示するテーブルを参照してください[データ型](../../../../visual-basic/language-reference/data-types/index.md)します。</span><span class="sxs-lookup"><span data-stu-id="a0add-105">For a table that displays a side-by-side comparison of the Visual Basic data types, see [Data Types](../../../../visual-basic/language-reference/data-types/index.md).</span></span>  
  
## <a name="char-type"></a><span data-ttu-id="a0add-106">Char 型</span><span class="sxs-lookup"><span data-stu-id="a0add-106">Char Type</span></span>  
 <span data-ttu-id="a0add-107">`Char`データ型が 1 つ 2 バイト (16 ビット) の Unicode 文字。</span><span class="sxs-lookup"><span data-stu-id="a0add-107">The `Char` data type is a single two-byte (16-bit) Unicode character.</span></span> <span data-ttu-id="a0add-108">変数は、常に正確に 1 つの文字を保存する場合の宣言として`Char`します。</span><span class="sxs-lookup"><span data-stu-id="a0add-108">If a variable always stores exactly one character, declare it as `Char`.</span></span> <span data-ttu-id="a0add-109">例えば:</span><span class="sxs-lookup"><span data-stu-id="a0add-109">For example:</span></span>  
  
 [!code-vb[VbVbalrCharTypes#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrchartypes/vb/module1.vb#1)]
  
 <span data-ttu-id="a0add-110">使用可能な各値を`Char`または`String`変数は、*コード ポイント*、または Unicode 文字セット内の文字コード。</span><span class="sxs-lookup"><span data-stu-id="a0add-110">Each possible value in a `Char` or `String` variable is a *code point*, or character code, in the Unicode character set.</span></span> <span data-ttu-id="a0add-111">Unicode 文字には、基本的な ASCII 文字セット、さまざまな他のアルファベット文字、アクセント記号、通貨記号、分数、分音記号、および数学的、技術的な記号が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a0add-111">Unicode characters include the basic ASCII character set, various other alphabet letters, accents, currency symbols, fractions, diacritics, and mathematical and technical symbols.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a0add-112">Unicode 文字セットは、コード ポイント D800 ~ DFFF (55296 55551 経由) の*サロゲート ペア*、1 つのコード ポイントを表す 2 つの 16 ビット値を必要とします。</span><span class="sxs-lookup"><span data-stu-id="a0add-112">The Unicode character set reserves the code points D800 through DFFF (55296 through 55551 decimal) for *surrogate pairs*, which require two 16-bit values to represent a single code point.</span></span> <span data-ttu-id="a0add-113">A`Char`変数は、サロゲート ペアを保持できない、 `String` 2 つの位置を使用して、このようなペアを保持します。</span><span class="sxs-lookup"><span data-stu-id="a0add-113">A `Char` variable cannot hold a surrogate pair, and a `String` uses two positions to hold such a pair.</span></span>  
  
 <span data-ttu-id="a0add-114">詳細については、次を参照してください。 [Char データ型](../../../../visual-basic/language-reference/data-types/char-data-type.md)します。</span><span class="sxs-lookup"><span data-stu-id="a0add-114">For more information, see [Char Data Type](../../../../visual-basic/language-reference/data-types/char-data-type.md).</span></span>  
  
## <a name="string-type"></a><span data-ttu-id="a0add-115">文字列型</span><span class="sxs-lookup"><span data-stu-id="a0add-115">String Type</span></span>  
 <span data-ttu-id="a0add-116">`String`データ型は 0 個以上の 2 バイト (16 ビット) の Unicode 文字のシーケンスです。</span><span class="sxs-lookup"><span data-stu-id="a0add-116">The `String` data type is a sequence of zero or more two-byte (16-bit) Unicode characters.</span></span> <span data-ttu-id="a0add-117">場合は、変数には、不特定数の文字を含めることができます、宣言として`String`します。</span><span class="sxs-lookup"><span data-stu-id="a0add-117">If a variable can contain an indefinite number of characters, declare it as `String`.</span></span> <span data-ttu-id="a0add-118">例えば:</span><span class="sxs-lookup"><span data-stu-id="a0add-118">For example:</span></span>  
  
 [!code-vb[VbVbalrCharTypes#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrchartypes/vb/module1.vb#2)]
  
 <span data-ttu-id="a0add-119">詳細については、次を参照してください。[文字列データ型](../../../../visual-basic/language-reference/data-types/string-data-type.md)します。</span><span class="sxs-lookup"><span data-stu-id="a0add-119">For more information, see [String Data Type](../../../../visual-basic/language-reference/data-types/string-data-type.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0add-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0add-120">See Also</span></span>  
 [<span data-ttu-id="a0add-121">基本データ型</span><span class="sxs-lookup"><span data-stu-id="a0add-121">Elementary Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)  
 [<span data-ttu-id="a0add-122">複合データ型</span><span class="sxs-lookup"><span data-stu-id="a0add-122">Composite Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)  
 [<span data-ttu-id="a0add-123">Visual Basic におけるジェネリック型</span><span class="sxs-lookup"><span data-stu-id="a0add-123">Generic Types in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)  
 [<span data-ttu-id="a0add-124">値型と参照型</span><span class="sxs-lookup"><span data-stu-id="a0add-124">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)  
 [<span data-ttu-id="a0add-125">Visual Basic における型変換</span><span class="sxs-lookup"><span data-stu-id="a0add-125">Type Conversions in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)  
 [<span data-ttu-id="a0add-126">トラブルシューティング (データ型)</span><span class="sxs-lookup"><span data-stu-id="a0add-126">Troubleshooting Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)  
 [<span data-ttu-id="a0add-127">型文字</span><span class="sxs-lookup"><span data-stu-id="a0add-127">Type Characters</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/type-characters.md)
