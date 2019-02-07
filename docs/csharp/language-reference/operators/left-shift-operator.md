---
title: << 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <<_CSharpKeyword
helpviewer_keywords:
- left shift operator (<<) [C#]
- << operator [C#]
ms.assetid: a654eb56-1ff7-4bf3-9064-b631be0cdccc
ms.openlocfilehash: 0271c97bc624a8946b90508e9ce39d217a128c05
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261751"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="0d999-102">\<\< 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="0d999-102">\<\< operator (C# Reference)</span></span>

<span data-ttu-id="0d999-103">左シフト演算子 (`<<`) は、最初のオペランドを 2 番目のオペランドで指定されたビット数だけ左にシフトします。</span><span class="sxs-lookup"><span data-stu-id="0d999-103">The left-shift operator (`<<`) shifts its first operand left by the number of bits specified by its second operand.</span></span> <span data-ttu-id="0d999-104">2 番目のオペランドの型は、[int](../keywords/int.md) または事前に定義された `int` への暗黙的な数値変換を持つ型にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d999-104">The type of the second operand must be an [int](../keywords/int.md) or a type that has a predefined implicit numeric conversion to `int`.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d999-105">コメント</span><span class="sxs-lookup"><span data-stu-id="0d999-105">Remarks</span></span>

<span data-ttu-id="0d999-106">最初のオペランドが [int](../keywords/int.md) または [uint](../keywords/uint.md) (32 ビット値) である場合、シフト数は、2 番目のオペランドの下位 5 ビットで指定されます。</span><span class="sxs-lookup"><span data-stu-id="0d999-106">If the first operand is an [int](../keywords/int.md) or [uint](../keywords/uint.md) (32-bit quantity), the shift count is given by the low-order five bits of the second operand.</span></span> <span data-ttu-id="0d999-107">つまり、実際のシフト数は、0 - 31 ビットです。</span><span class="sxs-lookup"><span data-stu-id="0d999-107">That is, the actual shift count is 0 to 31 bits.</span></span>

<span data-ttu-id="0d999-108">最初のオペランドが [long](../keywords/long.md) または [ulong](../keywords/ulong.md) (64 ビット値) である場合、シフト数は、2 番目のオペランドの下位 6 ビットで指定されます。</span><span class="sxs-lookup"><span data-stu-id="0d999-108">If the first operand is a [long](../keywords/long.md) or [ulong](../keywords/ulong.md) (64-bit quantity), the shift count is given by the low-order six bits of the second operand.</span></span> <span data-ttu-id="0d999-109">つまり、実際のシフト数は、0 - 63 ビットです。</span><span class="sxs-lookup"><span data-stu-id="0d999-109">That is, the actual shift count is 0 to 63 bits.</span></span>

<span data-ttu-id="0d999-110">シフトが破棄された後に最初のオペランドの型の範囲内に含まれないすべての上位ビットおよび下位の空のビットはゼロで埋められます。</span><span class="sxs-lookup"><span data-stu-id="0d999-110">Any high-order bits that are not within the range of the type of the first operand after the shift are discarded, and the low-order empty bits are zero-filled.</span></span> <span data-ttu-id="0d999-111">シフト演算ではオーバーフローは発生しません。</span><span class="sxs-lookup"><span data-stu-id="0d999-111">Shift operations never cause overflows.</span></span>

<span data-ttu-id="0d999-112">ユーザー定義型は、`<<` 演算子をオーバーロードすることができます (「[operator](../keywords/operator.md)」を参照)。最初のオペランドの型は、ユーザー定義型である必要があり、2 番目のオペランドの型は `int` でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="0d999-112">User-defined types can overload the `<<` operator (see [operator](../keywords/operator.md)); the type of the first operand must be the user-defined type, and the type of the second operand must be `int`.</span></span> <span data-ttu-id="0d999-113">二項演算子をオーバーロードすると、対応する代入演算子がある場合、これも暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="0d999-113">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>

## <a name="example"></a><span data-ttu-id="0d999-114">例</span><span class="sxs-lookup"><span data-stu-id="0d999-114">Example</span></span>

[!code-csharp[csRefOperators#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#14)]

## <a name="comments"></a><span data-ttu-id="0d999-115">コメント</span><span class="sxs-lookup"><span data-stu-id="0d999-115">Comments</span></span>

<span data-ttu-id="0d999-116">1 と 33 は同じ下位 5 ビットを持つため、`i<<1` と `i<<33` は、同じ結果になります。</span><span class="sxs-lookup"><span data-stu-id="0d999-116">Note that `i<<1` and `i<<33` give the same result, because 1 and 33 have the same low-order five bits.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d999-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d999-117">See also</span></span>

- [<span data-ttu-id="0d999-118">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="0d999-118">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="0d999-119">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="0d999-119">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="0d999-120">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="0d999-120">C# Operators</span></span>](index.md)
