---
title: '&amp;= 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '&=_CSharpKeyword'
helpviewer_keywords:
- AND assignment operator (&=) [C#]
- '&= operator [C#]'
ms.assetid: e8d58f3f-72dd-4b5a-b995-452fcce7e6bb
ms.openlocfilehash: f3a6fe20ca89a90b5a64118d73fb39e9a364d1e9
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42933953"
---
# <a name="amp-operator-c-reference"></a><span data-ttu-id="2ac75-102">&amp;= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="2ac75-102">&amp;= Operator (C# Reference)</span></span>
<span data-ttu-id="2ac75-103">AND 代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="2ac75-103">The AND assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2ac75-104">コメント</span><span class="sxs-lookup"><span data-stu-id="2ac75-104">Remarks</span></span>  
 <span data-ttu-id="2ac75-105">次のような `&=` 代入演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="2ac75-105">An expression using the `&=` assignment operator, such as</span></span>  
  
```csharp  
x &= y  
```  
  
 <span data-ttu-id="2ac75-106">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="2ac75-106">is equivalent to</span></span>  
  
```csharp  
x = x & y  
```  
  
 <span data-ttu-id="2ac75-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="2ac75-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="2ac75-108">[& 演算子](../../../csharp/language-reference/operators/and-operator.md)では、整数のオペランドではビットごとの論理 AND 演算、`bool` オペランドでは論理 AND 演算が実行されます。</span><span class="sxs-lookup"><span data-stu-id="2ac75-108">The [& operator](../../../csharp/language-reference/operators/and-operator.md) performs a bitwise logical AND operation on integral operands and logical AND on `bool` operands.</span></span>  
  
 <span data-ttu-id="2ac75-109">`&=` 演算子は直接オーバーロードできませんが、[& 演算子](../../../csharp/language-reference/operators/and-operator.md)はユーザー定義型でオーバーロードできます (「[operator](../../../csharp/language-reference/keywords/operator.md)」を参照)。</span><span class="sxs-lookup"><span data-stu-id="2ac75-109">The `&=` operator cannot be overloaded directly, but user-defined types can overload the binary [& operator](../../../csharp/language-reference/operators/and-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2ac75-110">例</span><span class="sxs-lookup"><span data-stu-id="2ac75-110">Example</span></span>  
 [!code-csharp[csRefOperators#34](../../../csharp/language-reference/operators/codesnippet/CSharp/and-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="2ac75-111">参照</span><span class="sxs-lookup"><span data-stu-id="2ac75-111">See Also</span></span>

- [<span data-ttu-id="2ac75-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="2ac75-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="2ac75-113">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="2ac75-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="2ac75-114">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="2ac75-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
