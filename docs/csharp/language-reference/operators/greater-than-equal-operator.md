---
title: '&gt;= 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '>=_CSharpKeyword'
helpviewer_keywords:
- greater than or equal to operator (>=) [C#]
- '>= operator [C#]'
ms.assetid: 0db4dcaf-56a3-4884-a7ad-35f64978a58d
ms.openlocfilehash: 8749d1dc0670a5a76bda5ee0d69a4a142671c1e6
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43511094"
---
# <a name="gt-operator-c-reference"></a><span data-ttu-id="39454-102">&gt;= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="39454-102">&gt;= Operator (C# Reference)</span></span>
<span data-ttu-id="39454-103">すべての数値型と列挙型で "以上" 関係演算子 `>=` が定義されます。これは、最初のオペランドが 2 番目のオペランドと等しいか、それより大きい場合に `true` を返し、それ以外の場合、`false` を返します。</span><span class="sxs-lookup"><span data-stu-id="39454-103">All numeric and enumeration types define a "greater than or equal" relational operator, `>=` that returns `true` if the first operand is greater than or equal to the second, `false` otherwise.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="39454-104">コメント</span><span class="sxs-lookup"><span data-stu-id="39454-104">Remarks</span></span>  
 <span data-ttu-id="39454-105">ユーザー定義型は `>=` 演算子をオーバーロードできます。</span><span class="sxs-lookup"><span data-stu-id="39454-105">User-defined types can overload the `>=` operator.</span></span> <span data-ttu-id="39454-106">詳細については、「[operator](../../../csharp/language-reference/keywords/operator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39454-106">For more information, see [operator](../../../csharp/language-reference/keywords/operator.md).</span></span> <span data-ttu-id="39454-107">`>=` をオーバーロードする場合は、[<=](../../../csharp/language-reference/operators/less-than-equal-operator.md) もオーバーロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="39454-107">If `>=` is overloaded, [<=](../../../csharp/language-reference/operators/less-than-equal-operator.md) must also be overloaded.</span></span> <span data-ttu-id="39454-108">整数型に対する演算は、通常、列挙型で使用できます。</span><span class="sxs-lookup"><span data-stu-id="39454-108">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="39454-109">例</span><span class="sxs-lookup"><span data-stu-id="39454-109">Example</span></span>  
 [!code-csharp[csRefOperators#39](../../../csharp/language-reference/operators/codesnippet/CSharp/greater-than-equal-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="39454-110">参照</span><span class="sxs-lookup"><span data-stu-id="39454-110">See Also</span></span>

- [<span data-ttu-id="39454-111">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="39454-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="39454-112">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="39454-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="39454-113">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="39454-113">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
