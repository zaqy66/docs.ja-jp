---
title: '*= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '*=_CSharpKeyword'
helpviewer_keywords:
- '*= operator [C#]'
- binary multiplication assignment operator (*=) [C#]
ms.assetid: 2e472155-59db-4dbf-bb94-bcccfa1a794d
ms.openlocfilehash: 2038f3b55d46f3503496275b3d25b17663b8c1db
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333435"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="b1cbe-102">\*= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="b1cbe-102">\*= Operator (C# Reference)</span></span>

<span data-ttu-id="b1cbe-103">二項乗算代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="b1cbe-103">The binary multiplication assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1cbe-104">コメント</span><span class="sxs-lookup"><span data-stu-id="b1cbe-104">Remarks</span></span>

<span data-ttu-id="b1cbe-105">次のような `*=` 代入演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="b1cbe-105">An expression using the `*=` assignment operator, such as</span></span>

```csharp
x *= y
```

<span data-ttu-id="b1cbe-106">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="b1cbe-106">is equivalent to</span></span>

```csharp
x = x * y
```

<span data-ttu-id="b1cbe-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="b1cbe-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="b1cbe-108">[\* 演算子](multiplication-operator.md)は、数値型の乗算のために事前定義されています。</span><span class="sxs-lookup"><span data-stu-id="b1cbe-108">The [\* operator](multiplication-operator.md) is predefined for numeric types to perform multiplication.</span></span>

<span data-ttu-id="b1cbe-109">`*=` 演算子は直接オーバーロードできませんが、ユーザー定義型は [\* 演算子](multiplication-operator.md)をオーバーロードできます (「[operator](../keywords/operator.md)」参照)。</span><span class="sxs-lookup"><span data-stu-id="b1cbe-109">The `*=` operator cannot be overloaded directly, but user-defined types can overload the [\* operator](multiplication-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="b1cbe-110">例</span><span class="sxs-lookup"><span data-stu-id="b1cbe-110">Example</span></span>

[!code-csharp[csRefOperators#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#13)]

## <a name="see-also"></a><span data-ttu-id="b1cbe-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1cbe-111">See also</span></span>

- [<span data-ttu-id="b1cbe-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="b1cbe-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="b1cbe-113">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="b1cbe-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="b1cbe-114">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="b1cbe-114">C# Operators</span></span>](index.md)
