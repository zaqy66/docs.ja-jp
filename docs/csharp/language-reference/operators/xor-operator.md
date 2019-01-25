---
title: ^ 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^_CSharpKeyword
helpviewer_keywords:
- ^ operator [C#]
- bitwise exclusive OR operator [C#]
ms.assetid: b09bc815-570f-4db6-a637-5b4ed99d014a
ms.openlocfilehash: 152be2d81d1bf340b839d74f169d63d7260f7ca5
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333708"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="3cb45-102">^ 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="3cb45-102">^ operator (C# Reference)</span></span>

<span data-ttu-id="3cb45-103">整数型と `bool` には、2 項 `^` 演算子が事前定義されています。</span><span class="sxs-lookup"><span data-stu-id="3cb45-103">Binary `^` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="3cb45-104">整数型の場合、`^` はそのオペランドのビット演算排他的 OR を計算します。</span><span class="sxs-lookup"><span data-stu-id="3cb45-104">For integral types, `^` computes the bitwise exclusive-OR of its operands.</span></span> <span data-ttu-id="3cb45-105">`bool` オペランドの場合、`^` はそのオペランドの論理排他的 OR を計算します。つまり、そのオペランドの厳密に 1 つが `true` の場合およびその場合に限って、結果が `true` になります。</span><span class="sxs-lookup"><span data-stu-id="3cb45-105">For `bool` operands, `^` computes the logical exclusive-or of its operands; that is, the result is `true` if and only if exactly one of its operands is `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb45-106">コメント</span><span class="sxs-lookup"><span data-stu-id="3cb45-106">Remarks</span></span>

<span data-ttu-id="3cb45-107">ユーザー定義型は `^` 演算子をオーバーロードできます (「[演算子](../keywords/operator.md)」を参照)。</span><span class="sxs-lookup"><span data-stu-id="3cb45-107">User-defined types can overload the `^` operator (see [operator](../keywords/operator.md)).</span></span> <span data-ttu-id="3cb45-108">整数型に対する演算は、通常、列挙型で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3cb45-108">Operations on integral types are generally allowed on enumeration.</span></span>

## <a name="example"></a><span data-ttu-id="3cb45-109">例</span><span class="sxs-lookup"><span data-stu-id="3cb45-109">Example</span></span>

[!code-csharp[csRefOperators#30](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#30)]

<span data-ttu-id="3cb45-110">前の例における `0xf8 ^ 0x3f` の計算では、16 進値の F8 と 3F に対応する次の 2 つのバイナリ値にビット演算排他的 OR が実行されます。</span><span class="sxs-lookup"><span data-stu-id="3cb45-110">The computation of `0xf8 ^ 0x3f` in the previous example performs a bitwise exclusive-OR of the following two binary values, which correspond to the hexadecimal values F8 and 3F:</span></span>

`1111 1000`

`0011 1111`

<span data-ttu-id="3cb45-111">排他的 OR の結果は `1100 0111` であり、16 進値の C7 です。</span><span class="sxs-lookup"><span data-stu-id="3cb45-111">The result of the exclusive-OR is `1100 0111`, which is C7 in hexadecimal.</span></span>

## <a name="see-also"></a><span data-ttu-id="3cb45-112">「</span><span class="sxs-lookup"><span data-stu-id="3cb45-112">See Also</span></span>

- [<span data-ttu-id="3cb45-113">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="3cb45-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="3cb45-114">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="3cb45-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="3cb45-115">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="3cb45-115">C# operators</span></span>](index.md)
