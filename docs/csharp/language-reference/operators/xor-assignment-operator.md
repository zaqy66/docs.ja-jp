---
title: ^= 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^=_CSharpKeyword
helpviewer_keywords:
- ^= operator [C#]
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
ms.openlocfilehash: 12189d6469a9716d3b7ebcffef23423a75692d1a
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333552"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="bd7a9-102">^= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="bd7a9-102">^= operator (C# Reference)</span></span>

<span data-ttu-id="bd7a9-103">排他的 OR 代入演算子。</span><span class="sxs-lookup"><span data-stu-id="bd7a9-103">The exclusive-OR assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd7a9-104">コメント</span><span class="sxs-lookup"><span data-stu-id="bd7a9-104">Remarks</span></span>

<span data-ttu-id="bd7a9-105">次のような形式の式があります。</span><span class="sxs-lookup"><span data-stu-id="bd7a9-105">An expression of the form</span></span>

```csharp
x ^= y
```

<span data-ttu-id="bd7a9-106">これが次のように評価されます。</span><span class="sxs-lookup"><span data-stu-id="bd7a9-106">is evaluated as</span></span>

```csharp
x = x ^ y
```

<span data-ttu-id="bd7a9-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="bd7a9-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="bd7a9-108">[^ 演算子](xor-operator.md)は整数オペランドにビット演算排他的 OR 操作を実行し、[ブール](../keywords/bool.md) オペランドに論理的 OR 操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="bd7a9-108">The [^ operator](xor-operator.md) performs a bitwise exclusive-OR operation on integral operands and logical exclusive-OR on [bool](../keywords/bool.md) operands.</span></span>

<span data-ttu-id="bd7a9-109">^= 演算子は直接オーバーロードできませんが、ユーザー定義型は [^ 演算子](xor-operator.md)をオーバーロードできます (「[演算子](../keywords/operator.md)」参照)。</span><span class="sxs-lookup"><span data-stu-id="bd7a9-109">The ^= operator cannot be overloaded directly, but user-defined types can overload the [^ operator](xor-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="bd7a9-110">例</span><span class="sxs-lookup"><span data-stu-id="bd7a9-110">Example</span></span>

[!code-csharp[csRefOperators#23](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#23)]

## <a name="see-also"></a><span data-ttu-id="bd7a9-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd7a9-111">See also</span></span>

- [<span data-ttu-id="bd7a9-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="bd7a9-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="bd7a9-113">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="bd7a9-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="bd7a9-114">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="bd7a9-114">C# operators</span></span>](index.md)