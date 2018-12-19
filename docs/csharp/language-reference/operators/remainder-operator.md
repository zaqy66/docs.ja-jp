---
title: '% 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 09/04/2018
f1_keywords:
- '%_CSharpKeyword'
helpviewer_keywords:
- remainder operator [C#]
- '% operator [C#]'
ms.assetid: 3b74f4f9-fd9c-45e7-84fa-c8d71a0dfad7
ms.openlocfilehash: a5c12b6683e35cc1ec2d40446dd0ed068c3d2552
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236480"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="d33b0-102">% 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="d33b0-102">% Operator (C# Reference)</span></span>

<span data-ttu-id="d33b0-103">剰余演算子 `%` は、最初のオペランドを 2 番目のオペランドで除算した後の剰余を計算します。</span><span class="sxs-lookup"><span data-stu-id="d33b0-103">The remainder operator `%` computes the remainder after dividing its first operand by its second operand.</span></span>

<span data-ttu-id="d33b0-104">ユーザー定義型は `%` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="d33b0-104">User-defined types can [overload](../keywords/operator.md) the `%` operator.</span></span> <span data-ttu-id="d33b0-105">`%` がオーバーロードされると、[剰余代入演算子](remainder-assignment-operator.md) `%=` も暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="d33b0-105">When the `%` is overloaded, the [remainder assignment operator](remainder-assignment-operator.md) `%=` is also implicitly overloaded.</span></span>

<span data-ttu-id="d33b0-106">数値型はすべて剰余演算子に対応しています。</span><span class="sxs-lookup"><span data-stu-id="d33b0-106">All numeric types support the remainder operator.</span></span>

## <a name="integer-remainder"></a><span data-ttu-id="d33b0-107">整数の剰余</span><span class="sxs-lookup"><span data-stu-id="d33b0-107">Integer remainder</span></span>
  
<span data-ttu-id="d33b0-108">整数オペランドの場合、`a % b` の結果は `a - (a / b) * b` で生成される値になります。</span><span class="sxs-lookup"><span data-stu-id="d33b0-108">For the integer operands, the result of `a % b` is the value produced by `a - (a / b) * b`.</span></span> <span data-ttu-id="d33b0-109">0 以外の剰余の符号は、次の例で示されるように、最初のオペランドの符号と同じになります。</span><span class="sxs-lookup"><span data-stu-id="d33b0-109">The sign of the non-zero remainder is the same as that of the first operand, as the following example shows:</span></span>

[!code-csharp-interactive[integer remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#1)]

## <a name="floating-point-remainder"></a><span data-ttu-id="d33b0-110">浮動小数点の剰余</span><span class="sxs-lookup"><span data-stu-id="d33b0-110">Floating-point remainder</span></span>

<span data-ttu-id="d33b0-111">[浮動小数点型](../keywords/float.md)オペランドと[倍精度浮動小数点型](../keywords/double.md)オペランドの場合、有限の `x` と `y` の `x % y` の結果は、次のような値 `z` となります。</span><span class="sxs-lookup"><span data-stu-id="d33b0-111">For the [float](../keywords/float.md) and [double](../keywords/double.md) operands, the result of `x % y` for the finite `x` and `y` is the value `z` such that</span></span>

- <span data-ttu-id="d33b0-112">`z` の符号は、0 以外の場合、`x` の符号と同じになります。</span><span class="sxs-lookup"><span data-stu-id="d33b0-112">the sign of `z`, if non-zero, is the same as the sign of `x`;</span></span>
- <span data-ttu-id="d33b0-113">`z` の絶対値は、`|x| - n * |y|` で生成される値となります。`n` は、`|x| / |y|` 以下で最も大きい整数であり、`|x|` と `|y|` はそれぞれ、`x` と `y` の絶対値です。</span><span class="sxs-lookup"><span data-stu-id="d33b0-113">the absolute value of `z` is the value produced by `|x| - n * |y|` where `n` is the largest possible integer that is less than or equal to `|x| / |y|` and `|x|` and `|y|` are the absolute values of `x` and `y`, respectively.</span></span>

<span data-ttu-id="d33b0-114">無限オペランドがある `%` 演算子の動作については、[C# 言語仕様](../language-specification/index.md)に関するページの「[剰余演算](~/_csharplang/spec/expressions.md#remainder-operator)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d33b0-114">For information about the behavior of the `%` operator with non-finite operands, see the [Remainder operator](~/_csharplang/spec/expressions.md#remainder-operator) section of the [C# language specification](../language-specification/index.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d33b0-115">剰余を計算するこの手法は、整数オペランドに使用される手法に類似していますが、IEEE 754 とは異なります。</span><span class="sxs-lookup"><span data-stu-id="d33b0-115">This method of computing the remainder is analogous to that used for integer operands, but differs from the IEEE 754.</span></span> <span data-ttu-id="d33b0-116">IEEE 754 に準拠する剰余演算が必要な場合、<xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType> メソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="d33b0-116">If you need the remainder operation that complies with the IEEE 754, use the <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType> method.</span></span>

<span data-ttu-id="d33b0-117">次の例では、`float` オペランドと `double` オペランドの剰余演算子の動作を示しています。</span><span class="sxs-lookup"><span data-stu-id="d33b0-117">The following example demonstrates the behavior of the remainder operator for `float` and `double` operands:</span></span>

[!code-csharp-interactive[float and double remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#2)]

<span data-ttu-id="d33b0-118">浮動小数点型に関連している可能性がある丸めエラーに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d33b0-118">Note the round-off errors that can be associated with the floating-point types.</span></span>

<span data-ttu-id="d33b0-119">[10 進](../keywords/decimal.md)オペランドの場合、剰余演算子 `%` は <xref:System.Decimal?displayProperty=nameWithType> 型の[剰余演算子](<xref:System.Decimal.op_Modulus(System.Decimal,System.Decimal)>)に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="d33b0-119">For the [decimal](../keywords/decimal.md) operands, the remainder operator `%` is equivalent to the [remainder operator](<xref:System.Decimal.op_Modulus(System.Decimal,System.Decimal)>) of the <xref:System.Decimal?displayProperty=nameWithType> type.</span></span>

## <a name="see-also"></a><span data-ttu-id="d33b0-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d33b0-120">See also</span></span>

- [<span data-ttu-id="d33b0-121">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="d33b0-121">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="d33b0-122">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="d33b0-122">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="d33b0-123">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="d33b0-123">C# Operators</span></span>](index.md)
- <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType>
- <xref:System.Math.DivRem%2A?displayProperty=nameWithType>
