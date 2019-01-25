---
title: '方法: (Visual Basic) パターンとの比較の文字列と一致します。'
ms.date: 07/20/2015
helpviewer_keywords:
- comparison operators [Visual Basic], comparing strings
- pattern matching
- strings [Visual Basic], comparing
- string comparison [Visual Basic], operators
- Visual Basic code, operators
- pattern matching [Visual Basic], string comparison
- string comparison [Visual Basic]
- Like operator [Visual Basic], pattern matching
- pattern matching, empty strings
- operators [Visual Basic], comparison
ms.assetid: 19a83804-b5af-4739-928b-ac93e64e457f
ms.openlocfilehash: a4d5f12c5cf1ba89f7b505fb44c3f8fb19cb09d4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54669160"
---
# <a name="how-to-match-a-string-against-a-pattern-visual-basic"></a><span data-ttu-id="444f0-102">方法: (Visual Basic) パターンとの比較の文字列と一致します。</span><span class="sxs-lookup"><span data-stu-id="444f0-102">How to: Match a String against a Pattern (Visual Basic)</span></span>
<span data-ttu-id="444f0-103">式かどうかを検索する場合、[文字列データ型](../../../../visual-basic/language-reference/data-types/string-data-type.md)を使用して、パターンを満たす、 [Like 演算子](../../../../visual-basic/language-reference/operators/like-operator.md)します。</span><span class="sxs-lookup"><span data-stu-id="444f0-103">If you want to find out if an expression of the [String Data Type](../../../../visual-basic/language-reference/data-types/string-data-type.md) satisfies a pattern, then you can use the [Like Operator](../../../../visual-basic/language-reference/operators/like-operator.md).</span></span>  
  
 <span data-ttu-id="444f0-104">`Like` 2 つのオペランドを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="444f0-104">`Like` takes two operands.</span></span> <span data-ttu-id="444f0-105">左のオペランドは、文字列式であり、右のオペランドが照合に使用するパターンを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="444f0-105">The left operand is a string expression, and the right operand is a string containing the pattern to be used for matching.</span></span> <span data-ttu-id="444f0-106">`Like` 返します、`Boolean`文字列式が、パターンを満たすかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="444f0-106">`Like` returns a `Boolean` value indicating whether the string expression satisfies the pattern.</span></span>  
  
 <span data-ttu-id="444f0-107">特定の文字、ワイルドカード文字、文字のリスト、または文字の範囲に対して文字列式内の各文字と一致することができます。</span><span class="sxs-lookup"><span data-stu-id="444f0-107">You can match each character in the string expression against a specific character, a wildcard character, a character list, or a character range.</span></span> <span data-ttu-id="444f0-108">仕様パターン文字列内の位置は、文字列式に一致する文字の位置に対応します。</span><span class="sxs-lookup"><span data-stu-id="444f0-108">The positions of the specifications in the pattern string correspond to the positions of the characters to be matched in the string expression.</span></span>  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-specific-character"></a><span data-ttu-id="444f0-109">特定の文字の文字列式での文字と一致するには</span><span class="sxs-lookup"><span data-stu-id="444f0-109">To match a character in the string expression against a specific character</span></span>  
  
-   <span data-ttu-id="444f0-110">特定の文字をパターン文字列に直接配置します。</span><span class="sxs-lookup"><span data-stu-id="444f0-110">Put the specific character directly in the pattern string.</span></span> <span data-ttu-id="444f0-111">特定の特殊文字は、角かっこで囲む必要があります (`[ ]`)。</span><span class="sxs-lookup"><span data-stu-id="444f0-111">Certain special characters must be enclosed in brackets (`[ ]`).</span></span> <span data-ttu-id="444f0-112">詳細については、次を参照してください。 [Like 演算子](../../../../visual-basic/language-reference/operators/like-operator.md)します。</span><span class="sxs-lookup"><span data-stu-id="444f0-112">For more information, see [Like Operator](../../../../visual-basic/language-reference/operators/like-operator.md).</span></span>  
  
     <span data-ttu-id="444f0-113">次の例をテストするかどうか`myString`1 文字だけで構成されます`H`します。</span><span class="sxs-lookup"><span data-stu-id="444f0-113">The following example tests whether `myString` consists exactly of the single character `H`.</span></span>  
  
     [!code-vb[VbVbalrOperators#70](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-match-a-string-against-a-pattern_1.vb)]  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-wildcard-character"></a><span data-ttu-id="444f0-114">ワイルドカード文字の文字列式の文字と一致するには</span><span class="sxs-lookup"><span data-stu-id="444f0-114">To match a character in the string expression against a wildcard character</span></span>  
  
-   <span data-ttu-id="444f0-115">疑問符 () の配置 (`?`) パターン文字列にします。</span><span class="sxs-lookup"><span data-stu-id="444f0-115">Put a question mark (`?`) in the pattern string.</span></span> <span data-ttu-id="444f0-116">この位置に任意の有効な文字は、検索が成功します。</span><span class="sxs-lookup"><span data-stu-id="444f0-116">Any valid character in this position makes a successful match.</span></span>  
  
     <span data-ttu-id="444f0-117">次の例のテストするかどうか`myString`1 文字から成る`W`の後ろに任意の値の 2 つの文字。</span><span class="sxs-lookup"><span data-stu-id="444f0-117">The following example tests whether `myString` consists of the single character `W` followed by exactly two characters of any values.</span></span>  
  
     [!code-vb[VbVbalrOperators#71](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-match-a-string-against-a-pattern_2.vb)]  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-list-of-characters"></a><span data-ttu-id="444f0-118">文字の一覧に対して、文字列式での文字と一致するには</span><span class="sxs-lookup"><span data-stu-id="444f0-118">To match a character in the string expression against a list of characters</span></span>  
  
-   <span data-ttu-id="444f0-119">角かっこを配置 (`[ ]`) で、パターン文字列とかっこ文字の一覧に格納します。</span><span class="sxs-lookup"><span data-stu-id="444f0-119">Put brackets (`[ ]`) in the pattern string, and inside the brackets put the list of characters.</span></span> <span data-ttu-id="444f0-120">コンマまたはその他の任意の区切り記号の文字を分離されません。</span><span class="sxs-lookup"><span data-stu-id="444f0-120">Do not separate the characters with commas or any other separator.</span></span> <span data-ttu-id="444f0-121">任意の 1 文字の一覧では、検索が成功します。</span><span class="sxs-lookup"><span data-stu-id="444f0-121">Any single character in the list makes a successful match.</span></span>  
  
     <span data-ttu-id="444f0-122">次の例のテストかどうか`myString`続く文字を 1 つの有効な任意の文字から成る`A`、 `C`、または`E`します。</span><span class="sxs-lookup"><span data-stu-id="444f0-122">The following example tests whether `myString` consists of any valid character followed by exactly one of the characters `A`, `C`, or `E`.</span></span>  
  
     [!code-vb[VbVbalrOperators#72](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-match-a-string-against-a-pattern_3.vb)]  
  
     <span data-ttu-id="444f0-123">この照合の小文字が区別されるに注意してください。</span><span class="sxs-lookup"><span data-stu-id="444f0-123">Note that this match is case-sensitive.</span></span>  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-range-of-characters"></a><span data-ttu-id="444f0-124">文字の範囲に対して文字列式での文字と一致するには</span><span class="sxs-lookup"><span data-stu-id="444f0-124">To match a character in the string expression against a range of characters</span></span>  
  
-   <span data-ttu-id="444f0-125">角かっこを配置 (`[ ]`) パターン文字列、および最低と最高の文字の範囲に、かっこ内では、ハイフンで区切られた (`–`)。</span><span class="sxs-lookup"><span data-stu-id="444f0-125">Put brackets (`[ ]`) in the pattern string, and inside the brackets put the lowest and highest characters in the range, separated by a hyphen (`–`).</span></span> <span data-ttu-id="444f0-126">範囲内の任意の 1 文字では、成功した一致。</span><span class="sxs-lookup"><span data-stu-id="444f0-126">Any single character within the range makes a successful match.</span></span>  
  
     <span data-ttu-id="444f0-127">次の例のテストかどうか`myString`文字から成る`num`文字 1 個続く`i`、 `j`、 `k`、 `l`、 `m`、または`n`します。</span><span class="sxs-lookup"><span data-stu-id="444f0-127">The following example tests whether `myString` consists of the characters `num` followed by exactly one of the characters `i`, `j`, `k`, `l`, `m`, or `n`.</span></span>  
  
     [!code-vb[VbVbalrOperators#73](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-match-a-string-against-a-pattern_4.vb)]  
  
     <span data-ttu-id="444f0-128">この照合の小文字が区別されるに注意してください。</span><span class="sxs-lookup"><span data-stu-id="444f0-128">Note that this match is case-sensitive.</span></span>  
  
## <a name="matching-empty-strings"></a><span data-ttu-id="444f0-129">空の文字列に一致します。</span><span class="sxs-lookup"><span data-stu-id="444f0-129">Matching Empty Strings</span></span>  
 <span data-ttu-id="444f0-130">`Like` シーケンス処理`[]`長さ 0 の文字列として (`""`)。</span><span class="sxs-lookup"><span data-stu-id="444f0-130">`Like` treats the sequence `[]` as a zero-length string (`""`).</span></span> <span data-ttu-id="444f0-131">使用することができます`[]`文字列全体の式が空では、文字列式で特定の位置が空かどうかを使用することはできないかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="444f0-131">You can use `[]` to test whether the entire string expression is empty, but you cannot use it to test if a particular position in the string expression is empty.</span></span> <span data-ttu-id="444f0-132">空の位置が、オプションのいずれかである場合は、テストするには、使用できる必要があります。 `Like` 2 回以上。</span><span class="sxs-lookup"><span data-stu-id="444f0-132">If an empty position is one of the options you need to test for, you can use `Like` more than once.</span></span>  
  
#### <a name="to-match-a-character-in-the-string-expression-against-a-list-of-characters-or-no-character"></a><span data-ttu-id="444f0-133">文字または文字の一覧に対して、文字列式での文字と一致するには</span><span class="sxs-lookup"><span data-stu-id="444f0-133">To match a character in the string expression against a list of characters or no character</span></span>  
  
1.  <span data-ttu-id="444f0-134">呼び出す、`Like`演算子を 2 回に同じ文字列式、および 2 つの呼び出しのいずれかで接続、[または演算子](../../../../visual-basic/language-reference/operators/or-operator.md)または[OrElse 演算子](../../../../visual-basic/language-reference/operators/orelse-operator.md)します。</span><span class="sxs-lookup"><span data-stu-id="444f0-134">Call the `Like` operator twice on the same string expression, and connect the two calls with either the [Or Operator](../../../../visual-basic/language-reference/operators/or-operator.md) or the [OrElse Operator](../../../../visual-basic/language-reference/operators/orelse-operator.md).</span></span>  
  
2.  <span data-ttu-id="444f0-135">最初のパターン文字列に`Like`句では、角かっこで囲まれた、文字の一覧が含まれます (`[ ]`)。</span><span class="sxs-lookup"><span data-stu-id="444f0-135">In the pattern string for the first `Like` clause, include the character list, enclosed in brackets (`[ ]`).</span></span>  
  
3.  <span data-ttu-id="444f0-136">2 つ目のパターン文字列内`Like`句では、配置しない任意の文字位置にある問題です。</span><span class="sxs-lookup"><span data-stu-id="444f0-136">In the pattern string for the second `Like` clause, do not put any character at the position in question.</span></span>  
  
     <span data-ttu-id="444f0-137">次の例は、7 桁の電話番号をテスト`phoneNum`の 3 桁の数字の後にスペース、ハイフン (`–`)、ピリオド (`.`)、または文字、後ろにないに 4 桁の数値。</span><span class="sxs-lookup"><span data-stu-id="444f0-137">The following example tests the seven-digit telephone number `phoneNum` for exactly three numeric digits, followed by a space, a hyphen (`–`), a period (`.`), or no character at all, followed by exactly four numeric digits.</span></span>  
  
     [!code-vb[VbVbalrOperators#74](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-match-a-string-against-a-pattern_5.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="444f0-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="444f0-138">See also</span></span>
- [<span data-ttu-id="444f0-139">比較演算子</span><span class="sxs-lookup"><span data-stu-id="444f0-139">Comparison Operators</span></span>](../../../../visual-basic/language-reference/operators/comparison-operators.md)
- [<span data-ttu-id="444f0-140">演算子および式</span><span class="sxs-lookup"><span data-stu-id="444f0-140">Operators and Expressions</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
- [<span data-ttu-id="444f0-141">Like 演算子</span><span class="sxs-lookup"><span data-stu-id="444f0-141">Like Operator</span></span>](../../../../visual-basic/language-reference/operators/like-operator.md)
- [<span data-ttu-id="444f0-142">String データ型</span><span class="sxs-lookup"><span data-stu-id="444f0-142">String Data Type</span></span>](../../../../visual-basic/language-reference/data-types/string-data-type.md)
