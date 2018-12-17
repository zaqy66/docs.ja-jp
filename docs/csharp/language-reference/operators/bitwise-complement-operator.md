---
title: ~ 演算子 (C# リファレンス)
ms.date: 11/05/2018
f1_keywords:
- ~_CSharpKeyword
helpviewer_keywords:
- tilde (~) one's complement operator [C#]
- ~ operator [C#]
- ~ [C#], bitwise complement operator
- bitwise complement operator [C#]
ms.assetid: 11bc078a-50e2-4d7e-9896-67ef669dc602
ms.openlocfilehash: 1bcb07c5639a098e3a8c566e92083ca0d48efb81
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153216"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="20d8a-102">~ 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="20d8a-102">~ Operator (C# Reference)</span></span>

<span data-ttu-id="20d8a-103">ビットごとの補数演算子 `~` は、各ビットを反転させてオペランドのビットごとの補数を生成する単項演算子です。</span><span class="sxs-lookup"><span data-stu-id="20d8a-103">The bitwise complement operator `~` is a unary operator that produces a bitwise complement of its operand by reversing each bit.</span></span> <span data-ttu-id="20d8a-104">すべての整数型で `~` 演算子がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="20d8a-104">All integer types support the `~` operator.</span></span>

> [!NOTE]
> <span data-ttu-id="20d8a-105">`~` シンボルはファイナライザーの宣言にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="20d8a-105">The `~` symbol is also used to declare finalizers.</span></span> <span data-ttu-id="20d8a-106">詳細については、「[Finalizers](../../programming-guide/classes-and-structs/destructors.md)」 (ファイナライザー) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20d8a-106">For more information, see [Finalizers](../../programming-guide/classes-and-structs/destructors.md).</span></span>

<span data-ttu-id="20d8a-107">`~` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="20d8a-107">The following example demonstrates the usage of the `~` operator:</span></span>

[!code-csharp-interactive[bitwise NOT](~/samples/snippets/csharp/language-reference/operators/BitwiseComplementExamples.cs#Example)]

> [!NOTE]
> <span data-ttu-id="20d8a-108">上記の例では、[C# 7.0 で導入され](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements)、[C# 7.2 で強化された](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals)バイナリ リテラルを使用しています。</span><span class="sxs-lookup"><span data-stu-id="20d8a-108">The preceding example uses the binary literals [introduced in C# 7.0](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements) and [enhanced  in C# 7.2](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="20d8a-109">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="20d8a-109">Operator overloadability</span></span>

<span data-ttu-id="20d8a-110">ユーザー定義型は `~` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="20d8a-110">User-defined types can [overload](../keywords/operator.md) the `~` operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="20d8a-111">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="20d8a-111">C# language specification</span></span>

<span data-ttu-id="20d8a-112">詳細については、「[C# 言語仕様](../language-specification/index.md)」の「[ビットごとの補数演算子](~/_csharplang/spec/expressions.md#bitwise-complement-operator)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="20d8a-112">For more information, see the [Bitwise complement operator](~/_csharplang/spec/expressions.md#bitwise-complement-operator) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="20d8a-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="20d8a-113">See also</span></span>

- [<span data-ttu-id="20d8a-114">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="20d8a-114">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="20d8a-115">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="20d8a-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="20d8a-116">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="20d8a-116">C# Operators</span></span>](index.md)
- [<span data-ttu-id="20d8a-117">ファイナライザー</span><span class="sxs-lookup"><span data-stu-id="20d8a-117">Finalizers</span></span>](../../programming-guide/classes-and-structs/destructors.md)
- [<span data-ttu-id="20d8a-118">& 演算子</span><span class="sxs-lookup"><span data-stu-id="20d8a-118">& operator</span></span>](and-operator.md)
- [<span data-ttu-id="20d8a-119">| 演算子</span><span class="sxs-lookup"><span data-stu-id="20d8a-119">| operator</span></span>](or-operator.md)
- [<span data-ttu-id="20d8a-120">^ 演算子</span><span class="sxs-lookup"><span data-stu-id="20d8a-120">^ operator</span></span>](xor-operator.md)
