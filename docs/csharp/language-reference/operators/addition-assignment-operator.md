---
title: += 演算子 (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: bd0997ec5b7d79a41e01f9c2b17533293e412c1e
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42933788"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="7546a-102">+= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="7546a-102">+= Operator (C# Reference)</span></span>
<span data-ttu-id="7546a-103">加算代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="7546a-103">The addition assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7546a-104">コメント</span><span class="sxs-lookup"><span data-stu-id="7546a-104">Remarks</span></span>  
 <span data-ttu-id="7546a-105">次のような `+=` 代入演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="7546a-105">An expression using the `+=` assignment operator, such as</span></span>  
  
```csharp  
x += y  
```  
  
 <span data-ttu-id="7546a-106">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="7546a-106">is equivalent to</span></span>  
  
```csharp  
x = x + y  
```  
  
 <span data-ttu-id="7546a-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="7546a-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="7546a-108">[+ 演算子](../../../csharp/language-reference/operators/addition-operator.md)の意味は、`x` および `y` の型によって異なります (たとえば、数値オペランドの場合は加算、文字列オペランドの場合は連結になります)。</span><span class="sxs-lookup"><span data-stu-id="7546a-108">The meaning of the [+ operator](../../../csharp/language-reference/operators/addition-operator.md) depends on the types of `x` and `y` (addition for numeric operands, concatenation for string operands, and so forth).</span></span>  
  
 <span data-ttu-id="7546a-109">`+=` 演算子は直接オーバーロードできませんが、ユーザー定義型は [+ 演算子](../../../csharp/language-reference/operators/addition-operator.md)をオーバーロードできます (「[演算子](../../../csharp/language-reference/keywords/operator.md)」参照)。</span><span class="sxs-lookup"><span data-stu-id="7546a-109">The `+=` operator cannot be overloaded directly, but user-defined types can overload the [+ operator](../../../csharp/language-reference/operators/addition-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
 <span data-ttu-id="7546a-110">`+=` 演算子は、イベントに対する応答として呼び出されるメソッドを指定するときにも使用されます。こうしたメソッドは、イベント ハンドラーと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="7546a-110">The `+=` operator is also used to specify a method that will be called in response to an event; such methods are called event handlers.</span></span> <span data-ttu-id="7546a-111">このコンテキストでの `+=` 演算子の使用は、"*イベントのサブスクライブ*" と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="7546a-111">The use of the `+=` operator in this context is referred to as *subscribing to an event*.</span></span> <span data-ttu-id="7546a-112">詳細については、「[方法: イベント サブスクリプションとサブスクリプションの解除](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)」と「[デリゲート](../../../csharp/programming-guide/delegates/index.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7546a-112">For more information, see [How to: Subscribe to and Unsubscribe from Events](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md) and [Delegates](../../../csharp/programming-guide/delegates/index.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="7546a-113">例</span><span class="sxs-lookup"><span data-stu-id="7546a-113">Example</span></span>  
 [!code-csharp[csRefOperators#35](../../../csharp/language-reference/operators/codesnippet/CSharp/addition-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="7546a-114">参照</span><span class="sxs-lookup"><span data-stu-id="7546a-114">See Also</span></span>

- [<span data-ttu-id="7546a-115">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="7546a-115">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="7546a-116">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="7546a-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="7546a-117">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="7546a-117">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
