---
title: '&lt;= 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- <=_CSharpKeyword
helpviewer_keywords:
- less than or equal to operator (<=) [C#]
- <= operator [C#]
ms.assetid: bb0caec9-d253-4105-b8bc-5252233251e4
ms.openlocfilehash: afbb932c1be010790236bec73a36acf0f01b97f4
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/15/2018
ms.locfileid: "45595062"
---
# <a name="lt-operator-c-reference"></a><span data-ttu-id="78365-102">&lt;= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="78365-102">&lt;= Operator (C# Reference)</span></span>
<span data-ttu-id="78365-103">すべての数値型と列挙型で "以下" 関係演算子 (`<=`) が定義されます。これは、最初のオペランドが 2 番目のオペランドと等しいか、それより小さい場合に `true` を返し、それ以外の場合、`false` を返します。</span><span class="sxs-lookup"><span data-stu-id="78365-103">All numeric and enumeration types define a "less than or equal" relational operator (`<=`) that returns `true` if the first operand is less than or equal to the second, `false` otherwise.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="78365-104">コメント</span><span class="sxs-lookup"><span data-stu-id="78365-104">Remarks</span></span>  
 <span data-ttu-id="78365-105">ユーザー定義型は `<=` 演算子をオーバーロードできます。</span><span class="sxs-lookup"><span data-stu-id="78365-105">User-defined types can overload the `<=` operator.</span></span> <span data-ttu-id="78365-106">詳細については、「[operator](../../../csharp/language-reference/keywords/operator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78365-106">For more information, see [operator](../../../csharp/language-reference/keywords/operator.md).</span></span> <span data-ttu-id="78365-107">`<=` をオーバーロードする場合は、[>=](../../../csharp/language-reference/operators/greater-than-equal-operator.md) もオーバーロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="78365-107">If `<=` is overloaded, [>=](../../../csharp/language-reference/operators/greater-than-equal-operator.md) must also be overloaded.</span></span> <span data-ttu-id="78365-108">整数型に対する演算は、通常、列挙型で使用できます。</span><span class="sxs-lookup"><span data-stu-id="78365-108">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="78365-109">例</span><span class="sxs-lookup"><span data-stu-id="78365-109">Example</span></span>  
 [!code-csharp[csRefOperators#32](../../../csharp/language-reference/operators/codesnippet/CSharp/less-than-equal-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="78365-110">参照</span><span class="sxs-lookup"><span data-stu-id="78365-110">See Also</span></span>

- [<span data-ttu-id="78365-111">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="78365-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="78365-112">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="78365-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="78365-113">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="78365-113">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="78365-114">explicit</span><span class="sxs-lookup"><span data-stu-id="78365-114">explicit</span></span>](../../../csharp/language-reference/keywords/explicit.md)
