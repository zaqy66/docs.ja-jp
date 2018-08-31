---
title: Function 式 (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Function expression [Visual Basic]
- functions [Visual Basic], function expressions
- lambda expressions [Visual Basic], function expression
ms.assetid: e8a47a45-4b8a-4f45-a623-7653625dffbc
ms.openlocfilehash: cfdd17f6f4ee6c4ddb3fa73ab3ec9c5ce46a162f
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/30/2018
ms.locfileid: "43255605"
---
# <a name="function-expression-visual-basic"></a><span data-ttu-id="597fb-102">Function 式 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="597fb-102">Function Expression (Visual Basic)</span></span>
<span data-ttu-id="597fb-103">パラメーターと、関数ラムダ式を定義するコードを宣言します。</span><span class="sxs-lookup"><span data-stu-id="597fb-103">Declares the parameters and code that define a function lambda expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="597fb-104">構文</span><span class="sxs-lookup"><span data-stu-id="597fb-104">Syntax</span></span>  
  
```  
Function ( [ parameterlist ] ) expression  
- or -  
Function ( [ parameterlist ] )  
  [ statements ]  
End Function  
```  
  
## <a name="parts"></a><span data-ttu-id="597fb-105">指定項目</span><span class="sxs-lookup"><span data-stu-id="597fb-105">Parts</span></span>  
  
|<span data-ttu-id="597fb-106">用語</span><span class="sxs-lookup"><span data-stu-id="597fb-106">Term</span></span>|<span data-ttu-id="597fb-107">定義</span><span class="sxs-lookup"><span data-stu-id="597fb-107">Definition</span></span>|  
|---|---|  
|`parameterlist`|<span data-ttu-id="597fb-108">任意。</span><span class="sxs-lookup"><span data-stu-id="597fb-108">Optional.</span></span> <span data-ttu-id="597fb-109">このプロシージャのパラメーターを表すローカル変数名の一覧。</span><span class="sxs-lookup"><span data-stu-id="597fb-109">A list of local variable names that represent the parameters of this procedure.</span></span> <span data-ttu-id="597fb-110">かっこは、リストが空の場合にも存在である必要があります。</span><span class="sxs-lookup"><span data-stu-id="597fb-110">The parentheses must be present even when the list is empty.</span></span> <span data-ttu-id="597fb-111">参照してください[パラメーター リスト](../../../visual-basic/language-reference/statements/parameter-list.md)します。</span><span class="sxs-lookup"><span data-stu-id="597fb-111">See [Parameter List](../../../visual-basic/language-reference/statements/parameter-list.md).</span></span>|  
|`expression`|<span data-ttu-id="597fb-112">必須。</span><span class="sxs-lookup"><span data-stu-id="597fb-112">Required.</span></span> <span data-ttu-id="597fb-113">1 つの式。</span><span class="sxs-lookup"><span data-stu-id="597fb-113">A single expression.</span></span> <span data-ttu-id="597fb-114">式の型は、関数の戻り値の型です。</span><span class="sxs-lookup"><span data-stu-id="597fb-114">The type of the expression is the return type of the function.</span></span>|  
|`statements`|<span data-ttu-id="597fb-115">必須。</span><span class="sxs-lookup"><span data-stu-id="597fb-115">Required.</span></span> <span data-ttu-id="597fb-116">使用して値を返すステートメントの一覧、`Return`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="597fb-116">A list of statements that returns a value by using the `Return` statement.</span></span> <span data-ttu-id="597fb-117">(を参照してください[Return ステートメント](../../../visual-basic/language-reference/statements/return-statement.md))。返される値の型は、関数の戻り値の型です。</span><span class="sxs-lookup"><span data-stu-id="597fb-117">(See [Return Statement](../../../visual-basic/language-reference/statements/return-statement.md).) The type of the value returned is the return type of the function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="597fb-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="597fb-118">Remarks</span></span>  
 <span data-ttu-id="597fb-119">A*ラムダ式*を計算し、値を返します名のない関数です。</span><span class="sxs-lookup"><span data-stu-id="597fb-119">A *lambda expression* is a function without a name that calculates and returns a value.</span></span> <span data-ttu-id="597fb-120">ラムダ式を使用することができますを引数としてを除く、デリゲート型を使用する任意の場所`RemoveHandler`します。</span><span class="sxs-lookup"><span data-stu-id="597fb-120">You can use a lambda expression anywhere you can use a delegate type, except as an argument to `RemoveHandler`.</span></span> <span data-ttu-id="597fb-121">デリゲート、およびデリゲートとラムダ式の使用に関する詳細については、次を参照してください。 [Delegate ステートメント](../../../visual-basic/language-reference/statements/delegate-statement.md)と[厳密でないデリゲート変換](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)します。</span><span class="sxs-lookup"><span data-stu-id="597fb-121">For more information about delegates, and the use of lambda expressions with delegates, see [Delegate Statement](../../../visual-basic/language-reference/statements/delegate-statement.md) and [Relaxed Delegate Conversion](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md).</span></span>  
  
## <a name="lambda-expression-syntax"></a><span data-ttu-id="597fb-122">ラムダ式の構文</span><span class="sxs-lookup"><span data-stu-id="597fb-122">Lambda Expression Syntax</span></span>  
 <span data-ttu-id="597fb-123">ラムダ式の構文では、標準的な関数に似ています。</span><span class="sxs-lookup"><span data-stu-id="597fb-123">The syntax of a lambda expression resembles that of a standard function.</span></span> <span data-ttu-id="597fb-124">相違点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="597fb-124">The differences are as follows:</span></span>  
  
-   <span data-ttu-id="597fb-125">ラムダ式の名前ではありません。</span><span class="sxs-lookup"><span data-stu-id="597fb-125">A lambda expression does not have a name.</span></span>  
  
-   <span data-ttu-id="597fb-126">ラムダ式などで、修飾子を含めることはできません`Overloads`または`Overrides`します。</span><span class="sxs-lookup"><span data-stu-id="597fb-126">Lambda expressions cannot have modifiers, such as `Overloads` or `Overrides`.</span></span>  
  
-   <span data-ttu-id="597fb-127">ラムダ式は使用しないでください、`As`関数の戻り値の型を指定する句。</span><span class="sxs-lookup"><span data-stu-id="597fb-127">Lambda expressions do not use an `As` clause to designate the return type of the function.</span></span> <span data-ttu-id="597fb-128">代わりに、型は、1 行のラムダ式の本体が評価される値または複数行のラムダ式の戻り値から推論されます。</span><span class="sxs-lookup"><span data-stu-id="597fb-128">Instead, the type is inferred from the value that the body of a single-line lambda expression evaluates to, or the return value of a multiline lambda expression.</span></span> <span data-ttu-id="597fb-129">たとえば、1 行のラムダ式の本体が`Where cust.City = "London"`、戻り値の型は`Boolean`します。</span><span class="sxs-lookup"><span data-stu-id="597fb-129">For example, if the body of a single-line lambda expression is `Where cust.City = "London"`, its return type is `Boolean`.</span></span>  
  
-   <span data-ttu-id="597fb-130">単一行のラムダ式の本体は、ステートメントではなく、式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="597fb-130">The body of a single-line lambda expression must be an expression, not a statement.</span></span> <span data-ttu-id="597fb-131">本文は、関数、プロシージャの呼び出しが sub プロシージャへの呼び出しではないので構成できます。</span><span class="sxs-lookup"><span data-stu-id="597fb-131">The body can consist of a call to a function procedure, but not a call to a sub procedure.</span></span>  
  
-   <span data-ttu-id="597fb-132">すべてのパラメーターまたはすべてのデータ型を推論する必要があります指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="597fb-132">Either all parameters must have specified data types or all must be inferred.</span></span>  
  
-   <span data-ttu-id="597fb-133">(省略可能) と Paramarray パラメーターは使用できません。</span><span class="sxs-lookup"><span data-stu-id="597fb-133">Optional and Paramarray parameters are not permitted.</span></span>  
  
-   <span data-ttu-id="597fb-134">ジェネリック パラメーターを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="597fb-134">Generic parameters are not permitted.</span></span>  
  
## <a name="example"></a><span data-ttu-id="597fb-135">例</span><span class="sxs-lookup"><span data-stu-id="597fb-135">Example</span></span>  
 <span data-ttu-id="597fb-136">次の例では、単純なラムダ式を作成する 2 つの方法を示します。</span><span class="sxs-lookup"><span data-stu-id="597fb-136">The following examples show two ways to create simple lambda expressions.</span></span> <span data-ttu-id="597fb-137">最初の使用、`Dim`関数の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="597fb-137">The first uses a `Dim` to provide a name for the function.</span></span> <span data-ttu-id="597fb-138">関数を呼び出すには、パラメーターの値で送信します。</span><span class="sxs-lookup"><span data-stu-id="597fb-138">To call the function, you send in a value for the parameter.</span></span>  
  
 [!code-vb[VbVbalrLambdas#1](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/function-expression_1.vb)]  
  
 [!code-vb[VbVbalrLambdas#2](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/function-expression_2.vb)]  
  
## <a name="example"></a><span data-ttu-id="597fb-139">例</span><span class="sxs-lookup"><span data-stu-id="597fb-139">Example</span></span>  
 <span data-ttu-id="597fb-140">またはを宣言し、同時に、関数を実行します。</span><span class="sxs-lookup"><span data-stu-id="597fb-140">Alternatively, you can declare and run the function at the same time.</span></span>  
  
 [!code-vb[VbVbalrLambdas#3](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/function-expression_3.vb)]  
  
## <a name="example"></a><span data-ttu-id="597fb-141">例</span><span class="sxs-lookup"><span data-stu-id="597fb-141">Example</span></span>  
 <span data-ttu-id="597fb-142">引数をインクリメントし、値を返すラムダ式の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="597fb-142">Following is an example of a lambda expression that increments its argument and returns the value.</span></span> <span data-ttu-id="597fb-143">この例では、単一行および複数行のラムダ式の両方の構文、関数を示します。</span><span class="sxs-lookup"><span data-stu-id="597fb-143">The example shows both the single-line and multiline lambda expression syntax for a function.</span></span> <span data-ttu-id="597fb-144">例については、次を参照してください。[ラムダ式](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)します。</span><span class="sxs-lookup"><span data-stu-id="597fb-144">For more examples, see [Lambda Expressions](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md).</span></span>  
  
 [!code-vb[VbVbalrLambdas#14](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/function-expression_4.vb)]  
  
## <a name="example"></a><span data-ttu-id="597fb-145">例</span><span class="sxs-lookup"><span data-stu-id="597fb-145">Example</span></span>  
 <span data-ttu-id="597fb-146">ラムダ式では、多くのクエリ演算子の基本となる[!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)]、メソッド ベースのクエリで明示的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="597fb-146">Lambda expressions underlie many of the query operators in [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)], and can be used explicitly in method-based queries.</span></span> <span data-ttu-id="597fb-147">次の例は、一般的な[!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)]メソッドの形式に、クエリの変換後にクエリします。</span><span class="sxs-lookup"><span data-stu-id="597fb-147">The following example shows a typical [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] query, followed by the translation of the query into method format.</span></span>  
  
```vb  
Dim londonCusts = From cust In db.Customers  
                       Where cust.City = "London"  
                       Select cust  
  
' This query is compiled to the following code:  
Dim londonCusts = db.Customers.  
                  Where(Function(cust) cust.City = "London").  
                  Select(Function(cust) cust)  
```  
  
 <span data-ttu-id="597fb-148">クエリ メソッドの詳細については、次を参照してください。[クエリ](../../../visual-basic/language-reference/queries/index.md)します。</span><span class="sxs-lookup"><span data-stu-id="597fb-148">For more information about query methods, see [Queries](../../../visual-basic/language-reference/queries/index.md).</span></span> <span data-ttu-id="597fb-149">標準クエリ演算子の詳細については、次を参照してください。[標準クエリ演算子の概要](../../programming-guide/concepts/linq/standard-query-operators-overview.md)します。</span><span class="sxs-lookup"><span data-stu-id="597fb-149">For more information about standard query operators, see [Standard Query Operators Overview](../../programming-guide/concepts/linq/standard-query-operators-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="597fb-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="597fb-150">See Also</span></span>  
 [<span data-ttu-id="597fb-151">Function ステートメント</span><span class="sxs-lookup"><span data-stu-id="597fb-151">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
 [<span data-ttu-id="597fb-152">ラムダ式</span><span class="sxs-lookup"><span data-stu-id="597fb-152">Lambda Expressions</span></span>](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)  
 [<span data-ttu-id="597fb-153">演算子および式</span><span class="sxs-lookup"><span data-stu-id="597fb-153">Operators and Expressions</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)  
 [<span data-ttu-id="597fb-154">ステートメント</span><span class="sxs-lookup"><span data-stu-id="597fb-154">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)  
 [<span data-ttu-id="597fb-155">値の比較</span><span class="sxs-lookup"><span data-stu-id="597fb-155">Value Comparisons</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/value-comparisons.md)  
 [<span data-ttu-id="597fb-156">ブール式</span><span class="sxs-lookup"><span data-stu-id="597fb-156">Boolean Expressions</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/boolean-expressions.md)  
 [<span data-ttu-id="597fb-157">If 演算子</span><span class="sxs-lookup"><span data-stu-id="597fb-157">If Operator</span></span>](../../../visual-basic/language-reference/operators/if-operator.md)  
 [<span data-ttu-id="597fb-158">厳密でないデリゲート変換</span><span class="sxs-lookup"><span data-stu-id="597fb-158">Relaxed Delegate Conversion</span></span>](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
