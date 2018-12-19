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
# <a name="-operator-c-reference"></a>% 演算子 (C# リファレンス)

剰余演算子 `%` は、最初のオペランドを 2 番目のオペランドで除算した後の剰余を計算します。

ユーザー定義型は `%` 演算子を[オーバーロード](../keywords/operator.md)できます。 `%` がオーバーロードされると、[剰余代入演算子](remainder-assignment-operator.md) `%=` も暗黙的にオーバーロードされます。

数値型はすべて剰余演算子に対応しています。

## <a name="integer-remainder"></a>整数の剰余
  
整数オペランドの場合、`a % b` の結果は `a - (a / b) * b` で生成される値になります。 0 以外の剰余の符号は、次の例で示されるように、最初のオペランドの符号と同じになります。

[!code-csharp-interactive[integer remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#1)]

## <a name="floating-point-remainder"></a>浮動小数点の剰余

[浮動小数点型](../keywords/float.md)オペランドと[倍精度浮動小数点型](../keywords/double.md)オペランドの場合、有限の `x` と `y` の `x % y` の結果は、次のような値 `z` となります。

- `z` の符号は、0 以外の場合、`x` の符号と同じになります。
- `z` の絶対値は、`|x| - n * |y|` で生成される値となります。`n` は、`|x| / |y|` 以下で最も大きい整数であり、`|x|` と `|y|` はそれぞれ、`x` と `y` の絶対値です。

無限オペランドがある `%` 演算子の動作については、[C# 言語仕様](../language-specification/index.md)に関するページの「[剰余演算](~/_csharplang/spec/expressions.md#remainder-operator)」セクションを参照してください。

> [!NOTE]
> 剰余を計算するこの手法は、整数オペランドに使用される手法に類似していますが、IEEE 754 とは異なります。 IEEE 754 に準拠する剰余演算が必要な場合、<xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType> メソッドを使用してください。

次の例では、`float` オペランドと `double` オペランドの剰余演算子の動作を示しています。

[!code-csharp-interactive[float and double remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#2)]

浮動小数点型に関連している可能性がある丸めエラーに注意してください。

[10 進](../keywords/decimal.md)オペランドの場合、剰余演算子 `%` は <xref:System.Decimal?displayProperty=nameWithType> 型の[剰余演算子](<xref:System.Decimal.op_Modulus(System.Decimal,System.Decimal)>)に等しくなります。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
- <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType>
- <xref:System.Math.DivRem%2A?displayProperty=nameWithType>
