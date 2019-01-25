---
title: '&gt;&gt; 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>_CSharpKeyword'
helpviewer_keywords:
- '>> operator [C#]'
- right shift operator (>>) [C#]
ms.assetid: a07f8679-d318-4ef8-b38b-65903efb8056
ms.openlocfilehash: 80e38d8e75b9ad573b635d544d6381950f107583
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333688"
---
# <a name="gtgt-operator-c-reference"></a><span data-ttu-id="6dcb6-102">&gt;&gt; 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="6dcb6-102">&gt;&gt; operator (C# Reference)</span></span>

<span data-ttu-id="6dcb6-103">右シフト演算子 (`>>`) は、最初のオペランドを 2 番目のオペランドで指定されたビット数だけ右にシフトします。</span><span class="sxs-lookup"><span data-stu-id="6dcb6-103">The right-shift operator (`>>`) shifts its first operand right by the number of bits specified by its second operand.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dcb6-104">コメント</span><span class="sxs-lookup"><span data-stu-id="6dcb6-104">Remarks</span></span>

<span data-ttu-id="6dcb6-105">最初のオペランドが [int](../keywords/int.md) または [uint](../keywords/uint.md) (32 ビット値) である場合、シフト数は、2 番目のオペランド (2 番目のオペランドと 0x1f) の下位 5 ビットで指定されます。</span><span class="sxs-lookup"><span data-stu-id="6dcb6-105">If the first operand is an [int](../keywords/int.md) or [uint](../keywords/uint.md) (32-bit quantity), the shift count is given by the low-order five bits of the second operand (second operand & 0x1f).</span></span>

<span data-ttu-id="6dcb6-106">最初のオペランドが [long](../keywords/long.md) または [ulong](../keywords/ulong.md) (64 ビット値) である場合、シフト数は、2 番目のオペランド (2 番目のオペランドと 0x3f) の下位 6 ビットで指定されます。</span><span class="sxs-lookup"><span data-stu-id="6dcb6-106">If the first operand is a [long](../keywords/long.md) or [ulong](../keywords/ulong.md) (64-bit quantity), the shift count is given by the low-order six bits of the second operand (second operand & 0x3f).</span></span>

<span data-ttu-id="6dcb6-107">最初のオペランドが [int](../keywords/int.md) または [long](../keywords/long.md) である場合、右シフトは算術演算シフトになります (空の上位ビットが符号ビットに設定されます)。</span><span class="sxs-lookup"><span data-stu-id="6dcb6-107">If the first operand is an [int](../keywords/int.md) or [long](../keywords/long.md), the right-shift is an arithmetic shift (high-order empty bits are set to the sign bit).</span></span> <span data-ttu-id="6dcb6-108">最初のオペランドの型が [uint](../keywords/uint.md) または [ulong](../keywords/ulong.md) である場合、右シフトは論理シフトになります (上位ビットはゼロで埋められます)。</span><span class="sxs-lookup"><span data-stu-id="6dcb6-108">If the first operand is of type [uint](../keywords/uint.md) or [ulong](../keywords/ulong.md), the right-shift is a logical shift (high-order bits are zero-filled).</span></span>

<span data-ttu-id="6dcb6-109">ユーザー定義型は、`>>` 演算子をオーバーロードすることができます。最初のオペランドの型は、ユーザー定義型である必要があり、2 番目のオペランドの型は [int](../keywords/int.md) でなければなりません。詳細については、「[operator](../keywords/operator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6dcb6-109">User-defined types can overload the `>>` operator; the type of the first operand must be the user-defined type, and the type of the second operand must be [int](../keywords/int.md). For more information, see [operator](../keywords/operator.md).</span></span> <span data-ttu-id="6dcb6-110">二項演算子をオーバーロードすると、対応する代入演算子がある場合、これも暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="6dcb6-110">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>

## <a name="example"></a><span data-ttu-id="6dcb6-111">例</span><span class="sxs-lookup"><span data-stu-id="6dcb6-111">Example</span></span>

[!code-csharp[csRefOperators#26](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#26)]

## <a name="see-also"></a><span data-ttu-id="6dcb6-112">参照</span><span class="sxs-lookup"><span data-stu-id="6dcb6-112">See Also</span></span>

- [<span data-ttu-id="6dcb6-113">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="6dcb6-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="6dcb6-114">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="6dcb6-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="6dcb6-115">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="6dcb6-115">C# operators</span></span>](index.md)