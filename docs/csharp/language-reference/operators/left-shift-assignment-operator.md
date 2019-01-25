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
ms.openlocfilehash: 4513c4b78dea3e8102c72a43249b4a44ffa2421d
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333253"
---
# <a name="ltlt-operator-c-reference"></a><span data-ttu-id="3b5d7-102">&lt;&lt;= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="3b5d7-102">&lt;&lt;= operator (C# Reference)</span></span>

<span data-ttu-id="3b5d7-103">左シフト代入演算子。</span><span class="sxs-lookup"><span data-stu-id="3b5d7-103">The left-shift assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b5d7-104">コメント</span><span class="sxs-lookup"><span data-stu-id="3b5d7-104">Remarks</span></span>

<span data-ttu-id="3b5d7-105">次のような形式の式があります。</span><span class="sxs-lookup"><span data-stu-id="3b5d7-105">An expression of the form</span></span>

```csharp
x <<= y
```

<span data-ttu-id="3b5d7-106">これが次のように評価されます。</span><span class="sxs-lookup"><span data-stu-id="3b5d7-106">is evaluated as</span></span>

```csharp
x = x << y
```

<span data-ttu-id="3b5d7-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="3b5d7-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="3b5d7-108">[<< 演算子](left-shift-operator.md) は、`y` で指定されたビット数だけ `x` を左にシフトします。</span><span class="sxs-lookup"><span data-stu-id="3b5d7-108">The [<< operator](left-shift-operator.md) shifts `x` left by the number of bits specified by `y`.</span></span>

<span data-ttu-id="3b5d7-109">`<<=` 演算子は直接オーバーロードできませんが、ユーザー定義型は [<< 演算子](left-shift-operator.md) をオーバーロードできます (「[operator](../keywords/operator.md)」参照)。</span><span class="sxs-lookup"><span data-stu-id="3b5d7-109">The `<<=` operator cannot be overloaded directly, but user-defined types can overload the [<< operator](left-shift-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="3b5d7-110">例</span><span class="sxs-lookup"><span data-stu-id="3b5d7-110">Example</span></span>

[!code-csharp[csRefOperators#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#12)]

## <a name="see-also"></a><span data-ttu-id="3b5d7-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="3b5d7-111">See also</span></span>

- [<span data-ttu-id="3b5d7-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="3b5d7-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="3b5d7-113">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="3b5d7-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="3b5d7-114">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="3b5d7-114">C# Operators</span></span>](index.md)
