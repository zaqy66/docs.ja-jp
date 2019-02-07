---
title: '>>= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: 8cc341c14ee1b90fde2abb369c187e57b4ce5c00
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278981"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="2188f-102">>>= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="2188f-102">>>= operator (C# Reference)</span></span>

<span data-ttu-id="2188f-103">右シフト代入演算子。</span><span class="sxs-lookup"><span data-stu-id="2188f-103">The right-shift assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="2188f-104">コメント</span><span class="sxs-lookup"><span data-stu-id="2188f-104">Remarks</span></span>

<span data-ttu-id="2188f-105">次のような形式の式があります。</span><span class="sxs-lookup"><span data-stu-id="2188f-105">An expression of the form</span></span>

```csharp
x >>= y
```

<span data-ttu-id="2188f-106">これが次のように評価されます。</span><span class="sxs-lookup"><span data-stu-id="2188f-106">is evaluated as</span></span>

```csharp
x = x >> y
```

<span data-ttu-id="2188f-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="2188f-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="2188f-108">[>> 演算子](right-shift-operator.md)は、`y` で指定された量だけ `x` を右にシフトします。</span><span class="sxs-lookup"><span data-stu-id="2188f-108">The [>> operator](right-shift-operator.md) shifts `x` right by an amount specified by `y`.</span></span>

<span data-ttu-id="2188f-109">>>= 演算子は直接オーバーロードできませんが、ユーザー定義型は [>> 演算子](right-shift-operator.md)をオーバーロードできます (「[operator](../keywords/operator.md)」参照)。</span><span class="sxs-lookup"><span data-stu-id="2188f-109">The >>= operator cannot be overloaded directly, but user-defined types can overload the [>> operator](right-shift-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="2188f-110">例</span><span class="sxs-lookup"><span data-stu-id="2188f-110">Example</span></span>

[!code-csharp[csRefOperators#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#11)]

## <a name="see-also"></a><span data-ttu-id="2188f-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="2188f-111">See also</span></span>

- [<span data-ttu-id="2188f-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="2188f-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="2188f-113">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="2188f-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="2188f-114">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="2188f-114">C# operators</span></span>](index.md)