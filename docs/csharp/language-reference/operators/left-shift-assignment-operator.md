---
title: '&lt;&lt;= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: f49c6360d6fee3f6d612aee51446545f25cd7d18
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53239174"
---
# <a name="ltlt-operator-c-reference"></a><span data-ttu-id="13db1-102">&lt;&lt;= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="13db1-102">&lt;&lt;= Operator (C# Reference)</span></span>
<span data-ttu-id="13db1-103">左シフト代入演算子。</span><span class="sxs-lookup"><span data-stu-id="13db1-103">The left-shift assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="13db1-104">コメント</span><span class="sxs-lookup"><span data-stu-id="13db1-104">Remarks</span></span>  
 <span data-ttu-id="13db1-105">次のような形式の式があります。</span><span class="sxs-lookup"><span data-stu-id="13db1-105">An expression of the form</span></span>  
  
```csharp  
x <<= y  
```  
  
 <span data-ttu-id="13db1-106">これが次のように評価されます。</span><span class="sxs-lookup"><span data-stu-id="13db1-106">is evaluated as</span></span>  
  
```csharp  
x = x << y  
```  
  
 <span data-ttu-id="13db1-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="13db1-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="13db1-108">[<< 演算子](../../../csharp/language-reference/operators/left-shift-operator.md) は、`y` で指定されたビット数だけ `x` を左にシフトします。</span><span class="sxs-lookup"><span data-stu-id="13db1-108">The [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) shifts `x` left by the number of bits specified by `y`.</span></span>  
  
 <span data-ttu-id="13db1-109">`<<=` 演算子は直接オーバーロードできませんが、ユーザー定義型は [<< 演算子](../../../csharp/language-reference/operators/left-shift-operator.md) をオーバーロードできます (「[operator](../../../csharp/language-reference/keywords/operator.md)」参照)。</span><span class="sxs-lookup"><span data-stu-id="13db1-109">The `<<=` operator cannot be overloaded directly, but user-defined types can overload the [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="13db1-110">例</span><span class="sxs-lookup"><span data-stu-id="13db1-110">Example</span></span>  
 [!code-csharp[csRefOperators#12](../../../csharp/language-reference/operators/codesnippet/CSharp/left-shift-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="13db1-111">参照</span><span class="sxs-lookup"><span data-stu-id="13db1-111">See Also</span></span>

- [<span data-ttu-id="13db1-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="13db1-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="13db1-113">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="13db1-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="13db1-114">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="13db1-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
