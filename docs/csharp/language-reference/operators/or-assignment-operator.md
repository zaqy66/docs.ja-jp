---
title: '|= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '|=_CSharpKeyword'
helpviewer_keywords:
- OR assignment operator (|=) [C#]
- '|= operator (OR assignment) [C#]'
ms.assetid: 8315b8cf-dd15-402f-92f0-c7db931696ca
ms.openlocfilehash: f4f7806c8679af400a371decd0c367929b3fb81d
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333266"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="3aa0d-102">|= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="3aa0d-102">|= operator (C# Reference)</span></span>

<span data-ttu-id="3aa0d-103">OR 代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="3aa0d-103">The OR assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aa0d-104">コメント</span><span class="sxs-lookup"><span data-stu-id="3aa0d-104">Remarks</span></span>

<span data-ttu-id="3aa0d-105">次のような `|=` 代入演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="3aa0d-105">An expression using the `|=` assignment operator, such as</span></span>

```csharp
x |= y
```

<span data-ttu-id="3aa0d-106">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="3aa0d-106">is equivalent to</span></span>

```csharp
x = x | y
```

<span data-ttu-id="3aa0d-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="3aa0d-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="3aa0d-108">[&#124; 演算子](or-operator.md)では、整数のオペランドではビットごとの論理 OR 演算、ブール オペランドでは論理 OR 演算が実行されます。</span><span class="sxs-lookup"><span data-stu-id="3aa0d-108">The [&#124; operator](or-operator.md) performs a bitwise logical OR operation on integral operands and logical OR on bool operands.</span></span>

<span data-ttu-id="3aa0d-109">`|=` 演算子は直接オーバーロードできませんが、ユーザー定義型は [&#124; 演算子](or-operator.md)をオーバーロードできます (「[operator](../keywords/operator.md)」参照)。</span><span class="sxs-lookup"><span data-stu-id="3aa0d-109">The `|=` operator cannot be overloaded directly, but user-defined types can overload the [&#124; operator](or-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="3aa0d-110">例</span><span class="sxs-lookup"><span data-stu-id="3aa0d-110">Example</span></span>

[!code-csharp[csRefOperators#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#10)]

## <a name="see-also"></a><span data-ttu-id="3aa0d-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="3aa0d-111">See also</span></span>

- [<span data-ttu-id="3aa0d-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="3aa0d-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="3aa0d-113">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="3aa0d-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="3aa0d-114">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="3aa0d-114">C# operators</span></span>](index.md)