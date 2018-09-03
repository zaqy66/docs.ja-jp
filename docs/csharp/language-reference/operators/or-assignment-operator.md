---
title: '|= 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '|=_CSharpKeyword'
helpviewer_keywords:
- OR assignment operator (|=) [C#]
- '|= operator (OR assignment) [C#]'
ms.assetid: 8315b8cf-dd15-402f-92f0-c7db931696ca
ms.openlocfilehash: fe56005ce94656b5e8a075cddfb91dc0da096cf7
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43408424"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="e6cbc-102">|= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="e6cbc-102">|= Operator (C# Reference)</span></span>
<span data-ttu-id="e6cbc-103">OR 代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="e6cbc-103">The OR assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e6cbc-104">コメント</span><span class="sxs-lookup"><span data-stu-id="e6cbc-104">Remarks</span></span>  
 <span data-ttu-id="e6cbc-105">次のような `|=` 代入演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="e6cbc-105">An expression using the `|=` assignment operator, such as</span></span>  
  
```csharp  
x |= y  
```  
  
 <span data-ttu-id="e6cbc-106">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="e6cbc-106">is equivalent to</span></span>  
  
```csharp  
x = x | y  
```  
  
 <span data-ttu-id="e6cbc-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="e6cbc-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="e6cbc-108">[&#124; 演算子](../../../csharp/language-reference/operators/or-operator.md)では、整数のオペランドではビットごとの論理 OR 演算、ブール オペランドでは論理 OR 演算が実行されます。</span><span class="sxs-lookup"><span data-stu-id="e6cbc-108">The [&#124; operator](../../../csharp/language-reference/operators/or-operator.md) performs a bitwise logical OR operation on integral operands and logical OR on bool operands.</span></span>  
  
 <span data-ttu-id="e6cbc-109">`|=` 演算子は直接オーバーロードできませんが、ユーザー定義型は [&#124; 演算子](../../../csharp/language-reference/operators/or-operator.md)をオーバーロードできます (「[operator](../../../csharp/language-reference/keywords/operator.md)」参照)。</span><span class="sxs-lookup"><span data-stu-id="e6cbc-109">The `|=` operator cannot be overloaded directly, but user-defined types can overload the [&#124; operator](../../../csharp/language-reference/operators/or-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="e6cbc-110">例</span><span class="sxs-lookup"><span data-stu-id="e6cbc-110">Example</span></span>  
 [!code-csharp[csRefOperators#10](../../../csharp/language-reference/operators/codesnippet/CSharp/or-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="e6cbc-111">参照</span><span class="sxs-lookup"><span data-stu-id="e6cbc-111">See Also</span></span>

- [<span data-ttu-id="e6cbc-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="e6cbc-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="e6cbc-113">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="e6cbc-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="e6cbc-114">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="e6cbc-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
