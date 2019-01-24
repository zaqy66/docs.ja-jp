---
title: '&lt;&lt;= 演算子 (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.<<=
helpviewer_keywords:
- operator <<=
- assignment statements [Visual Basic], compound
- <<= operator [Visual Basic]
- statements [Visual Basic], compound assignment
- operator<<=
- compound assignment statements [Visual Basic]
ms.assetid: 8ad26613-faff-4e2f-89ee-63feee33bfda
ms.openlocfilehash: 9d4f367506c847ddf2478dd1ea07e28332cc62a2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54677772"
---
# <a name="ltlt-operator-visual-basic"></a><span data-ttu-id="ceb50-102">&lt;&lt;= 演算子 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ceb50-102">&lt;&lt;= Operator (Visual Basic)</span></span>
<span data-ttu-id="ceb50-103">変数またはプロパティの値に算術左シフトを実行し、結果を変数またはプロパティに代入します。</span><span class="sxs-lookup"><span data-stu-id="ceb50-103">Performs an arithmetic left shift on the value of a variable or property and assigns the result back to the variable or property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ceb50-104">構文</span><span class="sxs-lookup"><span data-stu-id="ceb50-104">Syntax</span></span>  
  
```  
variableorproperty <<= amount  
```  
  
## <a name="parts"></a><span data-ttu-id="ceb50-105">指定項目</span><span class="sxs-lookup"><span data-stu-id="ceb50-105">Parts</span></span>  
 `variableorproperty`  
 <span data-ttu-id="ceb50-106">必須。</span><span class="sxs-lookup"><span data-stu-id="ceb50-106">Required.</span></span> <span data-ttu-id="ceb50-107">整数型の変数またはプロパティ (`SByte`、 `Byte`、 `Short`、 `UShort`、 `Integer`、 `UInteger`、 `Long`、または`ULong`)。</span><span class="sxs-lookup"><span data-stu-id="ceb50-107">Variable or property of an integral type (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, or `ULong`).</span></span>  
  
 `amount`  
 <span data-ttu-id="ceb50-108">必須。</span><span class="sxs-lookup"><span data-stu-id="ceb50-108">Required.</span></span> <span data-ttu-id="ceb50-109">拡大変換後のデータ型の数値式`Integer`します。</span><span class="sxs-lookup"><span data-stu-id="ceb50-109">Numeric expression of a data type that widens to `Integer`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ceb50-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="ceb50-110">Remarks</span></span>  
 <span data-ttu-id="ceb50-111">左側にある要素、`<<=`演算子は、単純なスカラー変数、プロパティ、または配列の要素。</span><span class="sxs-lookup"><span data-stu-id="ceb50-111">The element on the left side of the `<<=` operator can be a simple scalar variable, a property, or an element of an array.</span></span> <span data-ttu-id="ceb50-112">変数またはプロパティにすることはできません[ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md)します。</span><span class="sxs-lookup"><span data-stu-id="ceb50-112">The variable or property cannot be [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span>  
  
 <span data-ttu-id="ceb50-113">`<<=`演算子は、変数またはプロパティの値の算術左シフトをまず実行します。</span><span class="sxs-lookup"><span data-stu-id="ceb50-113">The `<<=` operator first performs an arithmetic left shift on the value of the variable or property.</span></span> <span data-ttu-id="ceb50-114">演算子は、その変数またはプロパティに、その操作の結果を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ceb50-114">The operator then assigns the result of that operation back to that variable or property.</span></span>  
  
 <span data-ttu-id="ceb50-115">算術シフトは循環、つまり、もう一方の端に結果の 1 つの端のシフトは行われません。</span><span class="sxs-lookup"><span data-stu-id="ceb50-115">Arithmetic shifts are not circular, which means the bits shifted off one end of the result are not reintroduced at the other end.</span></span> <span data-ttu-id="ceb50-116">算術左シフトでは、結果のデータ型の範囲を超えてシフトが破棄され、右側の空いたビット位置が 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="ceb50-116">In an arithmetic left shift, the bits shifted beyond the range of the result data type are discarded, and the bit positions vacated on the right are set to zero.</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="ceb50-117">オーバーロード</span><span class="sxs-lookup"><span data-stu-id="ceb50-117">Overloading</span></span>  
 <span data-ttu-id="ceb50-118">[<< 演算子](../../../visual-basic/language-reference/operators/left-shift-operator.md)できます*オーバー ロードされた*、つまり、ことクラスまたは構造体を再定義できますその動作はそのクラスまたは構造体の型。</span><span class="sxs-lookup"><span data-stu-id="ceb50-118">The [<< Operator](../../../visual-basic/language-reference/operators/left-shift-operator.md) can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="ceb50-119">オーバー ロード、`<<`演算子の動作に影響、`<<=`演算子。</span><span class="sxs-lookup"><span data-stu-id="ceb50-119">Overloading the `<<` operator affects the behavior of the `<<=` operator.</span></span> <span data-ttu-id="ceb50-120">コードで使用する場合`<<=`クラスまたは構造体をオーバー ロードで`<<`、再定義された動作を確認してください。</span><span class="sxs-lookup"><span data-stu-id="ceb50-120">If your code uses `<<=` on a class or structure that overloads `<<`, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="ceb50-121">詳細については、「 [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ceb50-121">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ceb50-122">例</span><span class="sxs-lookup"><span data-stu-id="ceb50-122">Example</span></span>  
 <span data-ttu-id="ceb50-123">次の例では、`<<=`のビット パターンをシフトする演算子、`Integer`変数に指定された量と割り当ての結果では変数のままです。</span><span class="sxs-lookup"><span data-stu-id="ceb50-123">The following example uses the `<<=` operator to shift the bit pattern of an `Integer` variable left by the specified amount and assign the result to the variable.</span></span>  
  
 [!code-vb[VbVbalrOperators#13](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/left-shift-assignment-operator_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="ceb50-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="ceb50-124">See also</span></span>
- [<span data-ttu-id="ceb50-125"><< 演算子</span><span class="sxs-lookup"><span data-stu-id="ceb50-125"><< Operator</span></span>](../../../visual-basic/language-reference/operators/left-shift-operator.md)
- [<span data-ttu-id="ceb50-126">代入演算子</span><span class="sxs-lookup"><span data-stu-id="ceb50-126">Assignment Operators</span></span>](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<span data-ttu-id="ceb50-127">ビット シフト演算子</span><span class="sxs-lookup"><span data-stu-id="ceb50-127">Bit Shift Operators</span></span>](../../../visual-basic/language-reference/operators/bit-shift-operators.md)
- [<span data-ttu-id="ceb50-128">Visual Basic における演算子の優先順位</span><span class="sxs-lookup"><span data-stu-id="ceb50-128">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="ceb50-129">機能別の演算子一覧</span><span class="sxs-lookup"><span data-stu-id="ceb50-129">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="ceb50-130">ステートメント</span><span class="sxs-lookup"><span data-stu-id="ceb50-130">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
