---
title: '! 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '!_CSharpKeyword'
helpviewer_keywords:
- '! operator [C#]'
- logical negation operator (!) [C#]
- NOT operator [C#]
ms.assetid: f5ae133f-8f64-4560-b34f-cd9cd5eed4ad
ms.openlocfilehash: 6b6d1796032f536aac0be49d4f101c1380b4e98f
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333227"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="849da-103">!</span><span class="sxs-lookup"><span data-stu-id="849da-103">!</span></span> <span data-ttu-id="849da-104">operator (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="849da-104">operator (C# Reference)</span></span>

<span data-ttu-id="849da-105">論理否定演算子 (`!`) は、オペランドを否定する単項演算子です。</span><span class="sxs-lookup"><span data-stu-id="849da-105">The logical negation operator (`!`) is a unary operator that negates its operand.</span></span> <span data-ttu-id="849da-106">この演算子は `bool` として定義され、オペランドが `false` の場合にのみ、`true` を返します。</span><span class="sxs-lookup"><span data-stu-id="849da-106">It is defined for `bool` and returns `true` if and only if its operand is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="849da-107">コメント</span><span class="sxs-lookup"><span data-stu-id="849da-107">Remarks</span></span>

<span data-ttu-id="849da-108">ユーザー定義型は `!` 演算子をオーバーロードできます (「[演算子](../keywords/operator.md)」を参照)。</span><span class="sxs-lookup"><span data-stu-id="849da-108">User-defined types can overload the `!` operator (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="849da-109">例</span><span class="sxs-lookup"><span data-stu-id="849da-109">Example</span></span>

[!code-csharp[csRefOperators#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#7)]

## <a name="see-also"></a><span data-ttu-id="849da-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="849da-110">See also</span></span>

- [<span data-ttu-id="849da-111">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="849da-111">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="849da-112">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="849da-112">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="849da-113">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="849da-113">C# Operators</span></span>](index.md)