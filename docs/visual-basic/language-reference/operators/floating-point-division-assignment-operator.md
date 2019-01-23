---
title: /= 演算子 (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb./=
helpviewer_keywords:
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- /= operator [Visual Basic]
- operator /=
- compound assignment statements [Visual Basic]
ms.assetid: a1e22d0e-8380-4761-9da1-84fb51c34821
ms.openlocfilehash: 8507d81d3060192640bf9a84e67ad39111c455b3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54537570"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="f0538-102">/= 演算子 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f0538-102">/= Operator (Visual Basic)</span></span>
<span data-ttu-id="f0538-103">変数またはプロパティの値式の値で除算し、浮動小数点の結果を変数またはプロパティに代入します。</span><span class="sxs-lookup"><span data-stu-id="f0538-103">Divides the value of a variable or property by the value of an expression and assigns the floating-point result to the variable or property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0538-104">構文</span><span class="sxs-lookup"><span data-stu-id="f0538-104">Syntax</span></span>  
  
```  
variableorproperty /= expression  
```  
  
## <a name="parts"></a><span data-ttu-id="f0538-105">指定項目</span><span class="sxs-lookup"><span data-stu-id="f0538-105">Parts</span></span>  
 `variableorproperty`  
 <span data-ttu-id="f0538-106">必須。</span><span class="sxs-lookup"><span data-stu-id="f0538-106">Required.</span></span> <span data-ttu-id="f0538-107">任意の数値型の変数またはプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f0538-107">Any numeric variable or property.</span></span>  
  
 `expression`  
 <span data-ttu-id="f0538-108">必須。</span><span class="sxs-lookup"><span data-stu-id="f0538-108">Required.</span></span> <span data-ttu-id="f0538-109">任意の数式。</span><span class="sxs-lookup"><span data-stu-id="f0538-109">Any numeric expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f0538-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="f0538-110">Remarks</span></span>  
 <span data-ttu-id="f0538-111">左側にある要素、`/=`演算子は、単純なスカラー変数、プロパティ、または配列の要素。</span><span class="sxs-lookup"><span data-stu-id="f0538-111">The element on the left side of the `/=` operator can be a simple scalar variable, a property, or an element of an array.</span></span> <span data-ttu-id="f0538-112">変数またはプロパティにすることはできません[ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md)します。</span><span class="sxs-lookup"><span data-stu-id="f0538-112">The variable or property cannot be [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span>  
  
 <span data-ttu-id="f0538-113">`/=`演算子は、(演算子の右側にある) の式の値で変数または (演算子の左側にある) のプロパティの値を除算する最初。</span><span class="sxs-lookup"><span data-stu-id="f0538-113">The `/=` operator first divides the value of the variable or property (on the left-hand side of the operator) by the value of the expression (on the right-hand side of the operator).</span></span> <span data-ttu-id="f0538-114">演算子は、変数またはプロパティに、その操作の結果を浮動小数点を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f0538-114">The operator then assigns the floating-point result of that operation to the variable or property.</span></span>  
  
 <span data-ttu-id="f0538-115">このステートメントは、代入、`Double`変数または左のプロパティの値。</span><span class="sxs-lookup"><span data-stu-id="f0538-115">This statement assigns a `Double` value to the variable or property on the left.</span></span> <span data-ttu-id="f0538-116">場合`Option Strict`は`On`、`variableorproperty`必要があります、`Double`します。</span><span class="sxs-lookup"><span data-stu-id="f0538-116">If `Option Strict` is `On`, `variableorproperty` must be a `Double`.</span></span> <span data-ttu-id="f0538-117">場合`Option Strict`は`Off`、Visual Basic の暗黙的な変換を実行します。 および、その結果の値を割り当てます`variableorproperty`、実行時に可能性のあるエラーとします。</span><span class="sxs-lookup"><span data-stu-id="f0538-117">If `Option Strict` is `Off`, Visual Basic performs an implicit conversion and assigns the resulting value to `variableorproperty`, with a possible error at run time.</span></span> <span data-ttu-id="f0538-118">詳細については、次を参照してください。 [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)と[Option Strict ステートメント](../../../visual-basic/language-reference/statements/option-strict-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="f0538-118">For more information, see [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md) and [Option Strict Statement](../../../visual-basic/language-reference/statements/option-strict-statement.md).</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="f0538-119">オーバーロード</span><span class="sxs-lookup"><span data-stu-id="f0538-119">Overloading</span></span>  
 <span data-ttu-id="f0538-120">[/演算子 (Visual Basic)](../../../visual-basic/language-reference/operators/floating-point-division-operator.md)できます*オーバー ロードされた*、つまり、ことクラスまたは構造体を再定義できますその動作はそのクラスまたは構造体の型。</span><span class="sxs-lookup"><span data-stu-id="f0538-120">The [/ Operator (Visual Basic)](../../../visual-basic/language-reference/operators/floating-point-division-operator.md) can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="f0538-121">オーバー ロード、`/`演算子の動作に影響、`/=`演算子。</span><span class="sxs-lookup"><span data-stu-id="f0538-121">Overloading the `/` operator affects the behavior of the `/=` operator.</span></span> <span data-ttu-id="f0538-122">コードで使用する場合`/=`クラスまたは構造体をオーバー ロードで`/`、再定義された動作を確認してください。</span><span class="sxs-lookup"><span data-stu-id="f0538-122">If your code uses `/=` on a class or structure that overloads `/`, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="f0538-123">詳細については、「 [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0538-123">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f0538-124">例</span><span class="sxs-lookup"><span data-stu-id="f0538-124">Example</span></span>  
 <span data-ttu-id="f0538-125">次の例では、`/=`演算子を 1 つの分割`Integer`秒と最初の変数に商の割り当てでは、変数。</span><span class="sxs-lookup"><span data-stu-id="f0538-125">The following example uses the `/=` operator to divide one `Integer` variable by a second and assign the quotient to the first variable.</span></span>  
  
 [!code-vb[VbVbalrOperators#17](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/floating-point-division-assignment-operator_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="f0538-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0538-126">See also</span></span>
- [<span data-ttu-id="f0538-127">/演算子 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f0538-127">/ Operator (Visual Basic)</span></span>](../../../visual-basic/language-reference/operators/floating-point-division-operator.md)
- [<span data-ttu-id="f0538-128">\\= 演算子</span><span class="sxs-lookup"><span data-stu-id="f0538-128">\\= Operator</span></span>](../../../visual-basic/language-reference/operators/integer-division-assignment-operator.md)
- [<span data-ttu-id="f0538-129">代入演算子</span><span class="sxs-lookup"><span data-stu-id="f0538-129">Assignment Operators</span></span>](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<span data-ttu-id="f0538-130">算術演算子</span><span class="sxs-lookup"><span data-stu-id="f0538-130">Arithmetic Operators</span></span>](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [<span data-ttu-id="f0538-131">Visual Basic における演算子の優先順位</span><span class="sxs-lookup"><span data-stu-id="f0538-131">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="f0538-132">機能別の演算子一覧</span><span class="sxs-lookup"><span data-stu-id="f0538-132">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="f0538-133">ステートメント</span><span class="sxs-lookup"><span data-stu-id="f0538-133">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
