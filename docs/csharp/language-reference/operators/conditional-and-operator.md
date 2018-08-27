---
title: '&amp;&amp; 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '&&_CSharpKeyword'
helpviewer_keywords:
- '&& operator [C#]'
- logical AND operator [C#]
ms.assetid: 2e4f0a1c-92a3-40f8-8e3b-17b607f20c31
ms.openlocfilehash: 459b791fde3e4d3940dbd3d916f940e81f365da6
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2018
ms.locfileid: "42999731"
---
# <a name="ampamp-operator-c-reference"></a><span data-ttu-id="b2479-102">&amp;&amp; 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="b2479-102">&amp;&amp; Operator (C# Reference)</span></span>
<span data-ttu-id="b2479-103">条件 AND 演算子 (`&&`) では `bool` オペランドの論理 AND が実行されますが、2 番目のオペランドは必要な場合にのみ評価されます。</span><span class="sxs-lookup"><span data-stu-id="b2479-103">The conditional-AND operator (`&&`) performs a logical-AND of its `bool` operands, but only evaluates its second operand if necessary.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b2479-104">コメント</span><span class="sxs-lookup"><span data-stu-id="b2479-104">Remarks</span></span>  
 <span data-ttu-id="b2479-105">次の演算は、</span><span class="sxs-lookup"><span data-stu-id="b2479-105">The operation</span></span>  
  
```csharp  
x && y  
```  
  
 <span data-ttu-id="b2479-106">次の演算に対応しています。</span><span class="sxs-lookup"><span data-stu-id="b2479-106">corresponds to the operation</span></span>  
  
```csharp  
x & y  
```  
  
 <span data-ttu-id="b2479-107">ただし `x` が `false` の場合は、AND 演算の結果は `y` の値に関係なく `false` となるため、`y` は評価されません。</span><span class="sxs-lookup"><span data-stu-id="b2479-107">except that if `x` is `false`, `y` is not evaluated, because the result of the AND operation is `false` no matter what the value of `y`  is.</span></span> <span data-ttu-id="b2479-108">これは、"ショートサーキット" 評価と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b2479-108">This is known as "short-circuit" evaluation.</span></span>  
  
 <span data-ttu-id="b2479-109">条件 AND 演算子はオーバーロードできませんが、通常の論理演算子、[true](../../../csharp/language-reference/keywords/true.md) 演算子、[false](../../../csharp/language-reference/keywords/false.md) 演算子のオーバーロードは、条件論理演算子の制約付きのオーバーロードとも見なされます。</span><span class="sxs-lookup"><span data-stu-id="b2479-109">The conditional-AND operator cannot be overloaded, but overloads of the regular logical operators and operators [true](../../../csharp/language-reference/keywords/true.md) and [false](../../../csharp/language-reference/keywords/false.md) are, with certain restrictions, also considered overloads of the conditional logical operators.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b2479-110">例</span><span class="sxs-lookup"><span data-stu-id="b2479-110">Example</span></span>  
 <span data-ttu-id="b2479-111">次の例では、2 番目の `if` ステートメントの条件式で最初のオペランドのみが評価されます。これは、このオペランドが `false` を返すからです。</span><span class="sxs-lookup"><span data-stu-id="b2479-111">In the following example, the conditional expression in the second `if` statement evaluates only the first operand because the operand returns `false`.</span></span>  
  
 [!code-csharp[csRefOperators#48](../../../csharp/language-reference/operators/codesnippet/CSharp/conditional-and-operator_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="b2479-112">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="b2479-112">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b2479-113">参照</span><span class="sxs-lookup"><span data-stu-id="b2479-113">See Also</span></span>

- [<span data-ttu-id="b2479-114">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="b2479-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="b2479-115">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="b2479-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="b2479-116">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="b2479-116">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
