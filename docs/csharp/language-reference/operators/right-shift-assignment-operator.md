---
title: '&gt;&gt;= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: 02a9559a5c4086eeed09094c15c3620366ffad8c
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333691"
---
# <a name="gtgt-operator-c-reference"></a><span data-ttu-id="42006-102">&gt;&gt;= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="42006-102">&gt;&gt;= operator (C# Reference)</span></span>

<span data-ttu-id="42006-103">右シフト代入演算子。</span><span class="sxs-lookup"><span data-stu-id="42006-103">The right-shift assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="42006-104">コメント</span><span class="sxs-lookup"><span data-stu-id="42006-104">Remarks</span></span>

<span data-ttu-id="42006-105">次のような形式の式があります。</span><span class="sxs-lookup"><span data-stu-id="42006-105">An expression of the form</span></span>

```csharp
x >>= y
```

<span data-ttu-id="42006-106">これが次のように評価されます。</span><span class="sxs-lookup"><span data-stu-id="42006-106">is evaluated as</span></span>

```csharp
x = x >> y
```

<span data-ttu-id="42006-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="42006-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="42006-108">[>> 演算子](right-shift-operator.md)は、`y` で指定された量だけ `x` を右にシフトします。</span><span class="sxs-lookup"><span data-stu-id="42006-108">The [>> operator](right-shift-operator.md) shifts `x` right by an amount specified by `y`.</span></span>

<span data-ttu-id="42006-109">>>= 演算子は直接オーバーロードできませんが、ユーザー定義型は [>> 演算子](right-shift-operator.md)をオーバーロードできます (「[operator](../keywords/operator.md)」参照)。</span><span class="sxs-lookup"><span data-stu-id="42006-109">The >>= operator cannot be overloaded directly, but user-defined types can overload the [>> operator](right-shift-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="42006-110">例</span><span class="sxs-lookup"><span data-stu-id="42006-110">Example</span></span>

[!code-csharp[csRefOperators#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#11)]

## <a name="see-also"></a><span data-ttu-id="42006-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="42006-111">See also</span></span>

- [<span data-ttu-id="42006-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="42006-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="42006-113">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="42006-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="42006-114">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="42006-114">C# operators</span></span>](index.md)