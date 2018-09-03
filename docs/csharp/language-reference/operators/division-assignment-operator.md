---
title: /= 演算子 (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- /=_CSharpKeyword
helpviewer_keywords:
- division assignment operator (/=) [C#]
- /= (division assignment operator) [C#]
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
ms.openlocfilehash: 8fff048cc441181aa3f0e3c0c638d501aaf9de3f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43477946"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="64daf-102">/= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="64daf-102">/= Operator (C# Reference)</span></span>
<span data-ttu-id="64daf-103">除算代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="64daf-103">The division assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="64daf-104">コメント</span><span class="sxs-lookup"><span data-stu-id="64daf-104">Remarks</span></span>  
 <span data-ttu-id="64daf-105">次のような `/=` 代入演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="64daf-105">An expression using the `/=` assignment operator, such as</span></span>  
  
```csharp  
x /= y  
```  
  
 <span data-ttu-id="64daf-106">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="64daf-106">is equivalent to</span></span>  
  
```csharp  
x = x / y  
```  
  
 <span data-ttu-id="64daf-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="64daf-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="64daf-108">[/ 演算子](../../../csharp/language-reference/operators/division-operator.md)は、数値型の除算のために事前定義されています。</span><span class="sxs-lookup"><span data-stu-id="64daf-108">The [/ operator](../../../csharp/language-reference/operators/division-operator.md) is predefined for numeric types to perform division.</span></span>  
  
 <span data-ttu-id="64daf-109">`/=` 演算子は直接オーバーロードできませんが、ユーザー定義型では [/ 演算子](../../../csharp/language-reference/operators/division-operator.md)をオーバーロードできます。(「[演算子](../../../csharp/language-reference/keywords/operator.md)」参照)。</span><span class="sxs-lookup"><span data-stu-id="64daf-109">The `/=` operator cannot be overloaded directly, but user-defined types can overload the [/ operator](../../../csharp/language-reference/operators/division-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="64daf-110">すべての複合代入演算子において、二項演算子をオーバーロードすると、同等の複合代入が暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="64daf-110">On all compound assignment operators, overloading the binary operator implicitly overloads the equivalent compound assignment.</span></span>  
  
## <a name="example"></a><span data-ttu-id="64daf-111">例</span><span class="sxs-lookup"><span data-stu-id="64daf-111">Example</span></span>  
 [!code-csharp[csRefOperators#5](codesnippet/CSharp/division-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="64daf-112">参照</span><span class="sxs-lookup"><span data-stu-id="64daf-112">See Also</span></span>

- [<span data-ttu-id="64daf-113">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="64daf-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="64daf-114">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="64daf-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="64daf-115">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="64daf-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
