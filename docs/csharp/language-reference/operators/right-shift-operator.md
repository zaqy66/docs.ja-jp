---
title: '&gt;&gt; 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '>>_CSharpKeyword'
helpviewer_keywords:
- '>> operator [C#]'
- right shift operator (>>) [C#]
ms.assetid: a07f8679-d318-4ef8-b38b-65903efb8056
ms.openlocfilehash: 7a2992befcacfdc1d9bb968b611051e15702cca8
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/25/2018
ms.locfileid: "42924825"
---
# <a name="gtgt-operator-c-reference"></a><span data-ttu-id="215cc-102">&gt;&gt; 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="215cc-102">&gt;&gt; Operator (C# Reference)</span></span>
<span data-ttu-id="215cc-103">右シフト演算子 (`>>`) は、最初のオペランドを 2 番目のオペランドで指定されたビット数だけ右にシフトします。</span><span class="sxs-lookup"><span data-stu-id="215cc-103">The right-shift operator (`>>`) shifts its first operand right by the number of bits specified by its second operand.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="215cc-104">コメント</span><span class="sxs-lookup"><span data-stu-id="215cc-104">Remarks</span></span>  
 <span data-ttu-id="215cc-105">最初のオペランドが [int](../../../csharp/language-reference/keywords/int.md) または [uint](../../../csharp/language-reference/keywords/uint.md) (32 ビット値) である場合、シフト数は、2 番目のオペランド (2 番目のオペランドと 0x1f) の下位 5 ビットで指定されます。</span><span class="sxs-lookup"><span data-stu-id="215cc-105">If the first operand is an [int](../../../csharp/language-reference/keywords/int.md) or [uint](../../../csharp/language-reference/keywords/uint.md) (32-bit quantity), the shift count is given by the low-order five bits of the second operand (second operand & 0x1f).</span></span>  
  
 <span data-ttu-id="215cc-106">最初のオペランドが [long](../../../csharp/language-reference/keywords/long.md) または [ulong](../../../csharp/language-reference/keywords/ulong.md) (64 ビット値) である場合、シフト数は、2 番目のオペランド (2 番目のオペランドと 0x3f) の下位 6 ビットで指定されます。</span><span class="sxs-lookup"><span data-stu-id="215cc-106">If the first operand is a [long](../../../csharp/language-reference/keywords/long.md) or [ulong](../../../csharp/language-reference/keywords/ulong.md) (64-bit quantity), the shift count is given by the low-order six bits of the second operand (second operand & 0x3f).</span></span>  
  
 <span data-ttu-id="215cc-107">最初のオペランドが [int](../../../csharp/language-reference/keywords/int.md) または [long](../../../csharp/language-reference/keywords/long.md) である場合、右シフトは算術演算シフトになります (空の上位ビットが符号ビットに設定されます)。</span><span class="sxs-lookup"><span data-stu-id="215cc-107">If the first operand is an [int](../../../csharp/language-reference/keywords/int.md) or [long](../../../csharp/language-reference/keywords/long.md), the right-shift is an arithmetic shift (high-order empty bits are set to the sign bit).</span></span> <span data-ttu-id="215cc-108">最初のオペランドの型が [uint](../../../csharp/language-reference/keywords/uint.md) または [ulong](../../../csharp/language-reference/keywords/ulong.md) である場合、右シフトは論理シフトになります (上位ビットはゼロで埋められます)。</span><span class="sxs-lookup"><span data-stu-id="215cc-108">If the first operand is of type [uint](../../../csharp/language-reference/keywords/uint.md) or [ulong](../../../csharp/language-reference/keywords/ulong.md), the right-shift is a logical shift (high-order bits are zero-filled).</span></span>  
  
 <span data-ttu-id="215cc-109">ユーザー定義型は、`>>` 演算子をオーバーロードすることができます。最初のオペランドの型は、ユーザー定義型である必要があり、2 番目のオペランドの型は [int](../../../csharp/language-reference/keywords/int.md) でなければなりません。詳細については、「[operator](../../../csharp/language-reference/keywords/operator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="215cc-109">User-defined types can overload the `>>` operator; the type of the first operand must be the user-defined type, and the type of the second operand must be [int](../../../csharp/language-reference/keywords/int.md). For more information, see [operator](../../../csharp/language-reference/keywords/operator.md).</span></span> <span data-ttu-id="215cc-110">二項演算子をオーバーロードすると、対応する代入演算子がある場合、これも暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="215cc-110">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="215cc-111">例</span><span class="sxs-lookup"><span data-stu-id="215cc-111">Example</span></span>  
 [!code-csharp[csRefOperators#26](../../../csharp/language-reference/operators/codesnippet/CSharp/right-shift-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="215cc-112">参照</span><span class="sxs-lookup"><span data-stu-id="215cc-112">See Also</span></span>

- [<span data-ttu-id="215cc-113">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="215cc-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="215cc-114">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="215cc-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="215cc-115">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="215cc-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
