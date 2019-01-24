---
title: 最初のオペランドのバイナリで&#39;場合&#39;式は、null 許容である必要がありますまたは型の参照
ms.date: 07/20/2015
f1_keywords:
- bc33107
- vbc33107
helpviewer_keywords:
- BC33107
ms.assetid: 493c8899-3f6b-4471-8eb6-9284e8492768
ms.openlocfilehash: 85094ba6d6a44bf2e6cc4fba7946598c286a08a2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668274"
---
# <a name="first-operand-in-a-binary-39if39-expression-must-be-nullable-or-a-reference-type"></a><span data-ttu-id="bc73d-102">最初のオペランドのバイナリで&#39;場合&#39;式は、null 許容である必要がありますまたは型の参照</span><span class="sxs-lookup"><span data-stu-id="bc73d-102">First operand in a binary &#39;If&#39; expression must be nullable or a reference type</span></span>
<span data-ttu-id="bc73d-103">`If`式が 2 つまたは 3 つの引数を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="bc73d-103">An `If` expression can take either two or three arguments.</span></span> <span data-ttu-id="bc73d-104">2 つの引数を送信すると、最初の引数は、参照型または null 許容型でする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc73d-104">When you send only two arguments, the first argument must be a reference type or a nullable type.</span></span> <span data-ttu-id="bc73d-105">最初の引数の評価が何も以外の場合`Nothing`、その値が返されます。</span><span class="sxs-lookup"><span data-stu-id="bc73d-105">If the first argument evaluates to anything other than `Nothing`, its value is returned.</span></span> <span data-ttu-id="bc73d-106">最初の引数が評価された場合`Nothing`、2 番目の引数が評価され、返されます。</span><span class="sxs-lookup"><span data-stu-id="bc73d-106">If the first argument evaluates to `Nothing`, the second argument is evaluated and returned.</span></span>  
  
 <span data-ttu-id="bc73d-107">たとえば、次のコードには 2 つ`If`で 3 つの引数と 2 つの引数の式。</span><span class="sxs-lookup"><span data-stu-id="bc73d-107">For example, the following code contains two `If` expressions, one with three arguments and one with two arguments.</span></span> <span data-ttu-id="bc73d-108">式を計算し、同じ値を返します。</span><span class="sxs-lookup"><span data-stu-id="bc73d-108">The expressions calculate and return the same value.</span></span>  
  
```vb  
' firstChoice is a nullable value type.  
Dim firstChoice? As Integer = Nothing  
Dim secondChoice As Integer = 1128  
' If expression with three arguments.  
Console.WriteLine(If(firstChoice IsNot Nothing, firstChoice, secondChoice))  
' If expression with two arguments.  
Console.WriteLine(If(firstChoice, secondChoice))  
```  
  
 <span data-ttu-id="bc73d-109">次の式では、このエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="bc73d-109">The following expressions cause this error:</span></span>  
  
```vb  
Dim choice1 = 4  
Dim choice2 = 5  
Dim booleanVar = True  
  
' Not valid.  
'Console.WriteLine(If(choice1 < choice2, 1))  
' Not valid.  
'Console.WriteLine(If(booleanVar, "Test returns True."))  
```  
  
 <span data-ttu-id="bc73d-110">**エラー ID:** BC33107</span><span class="sxs-lookup"><span data-stu-id="bc73d-110">**Error ID:** BC33107</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="bc73d-111">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="bc73d-111">To correct this error</span></span>  
  
-   <span data-ttu-id="bc73d-112">最初の引数が null 許容型または参照型であるようにコードを変更することはできない場合、は、3 つの引数に変換することを検討してください`If`式、または、`If...Then...Else`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="bc73d-112">If you cannot change the code so that the first argument is a nullable type or reference type, consider converting to a three-argument `If` expression, or to an `If...Then...Else` statement.</span></span>  
  
```vb  
Console.WriteLine(If(choice1 < choice2, 1, 2))  
Console.WriteLine(If(booleanVar, "Test returns True.", "Test returns False."))  
```  
  
## <a name="see-also"></a><span data-ttu-id="bc73d-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc73d-113">See also</span></span>
- [<span data-ttu-id="bc73d-114">If 演算子</span><span class="sxs-lookup"><span data-stu-id="bc73d-114">If Operator</span></span>](../../../visual-basic/language-reference/operators/if-operator.md)
- [<span data-ttu-id="bc73d-115">If...Then...Else ステートメント</span><span class="sxs-lookup"><span data-stu-id="bc73d-115">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [<span data-ttu-id="bc73d-116">null 許容値型</span><span class="sxs-lookup"><span data-stu-id="bc73d-116">Nullable Value Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
