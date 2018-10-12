---
title: '| 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '|_CSharpKeyword'
helpviewer_keywords:
- bitwise OR operator [C#]
- '| operator [C#]'
- binary operator (|) [C#]
ms.assetid: 82d6bb78-54c8-40bf-b679-531180ddaf70
ms.openlocfilehash: 999df9db0819a5f33e21a29b892de0a8854dd5d8
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2018
ms.locfileid: "46706149"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="75b79-102">| 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="75b79-102">| Operator (C# Reference)</span></span>
<span data-ttu-id="75b79-103">整数型と `bool` には、2 項 `|` 演算子が事前定義されています。</span><span class="sxs-lookup"><span data-stu-id="75b79-103">Binary `|` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="75b79-104">整数型の場合、`|` はそのオペランドのビットごとの OR を計算します。</span><span class="sxs-lookup"><span data-stu-id="75b79-104">For integral types, `|` computes the bitwise OR of its operands.</span></span> <span data-ttu-id="75b79-105">`bool` オペランドの場合、`|` は、そのオペランドの論理 OR を計算します。つまり、結果は、両方のオペランドが `false` の場合にのみ `false` になります。</span><span class="sxs-lookup"><span data-stu-id="75b79-105">For `bool` operands, `|` computes the logical OR of its operands; that is, the result is `false` if and only if both its operands are `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="75b79-106">コメント</span><span class="sxs-lookup"><span data-stu-id="75b79-106">Remarks</span></span>  
 <span data-ttu-id="75b79-107">バイナリ `|` 演算子では、[条件 OR 演算子](conditional-or-operator.md) `||` とは対照的に、最初の演算子の値に関係なく、両方の演算子が評価されます。</span><span class="sxs-lookup"><span data-stu-id="75b79-107">The binary `|` operator evaluates both operands regardless of the first one's value, in contrast to the [conditional-OR operator](conditional-or-operator.md) `||`.</span></span>
 
 <span data-ttu-id="75b79-108">ユーザー定義型は `|` 演算子をオーバーロードできます (「[演算子](../../../csharp/language-reference/keywords/operator.md)」を参照)。</span><span class="sxs-lookup"><span data-stu-id="75b79-108">User-defined types can overload the `|` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="75b79-109">例</span><span class="sxs-lookup"><span data-stu-id="75b79-109">Example</span></span>  
 [!code-csharp[csRefOperators#31](../../../csharp/language-reference/operators/codesnippet/CSharp/or-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="75b79-110">参照</span><span class="sxs-lookup"><span data-stu-id="75b79-110">See Also</span></span>

- [<span data-ttu-id="75b79-111">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="75b79-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="75b79-112">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="75b79-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="75b79-113">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="75b79-113">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
