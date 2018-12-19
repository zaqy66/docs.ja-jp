---
title: / 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 12/13/2018
f1_keywords:
- /_CSharpKeyword
helpviewer_keywords:
- / operator [C#]
- division operator [C#]
ms.assetid: d155e496-678f-4efa-bebe-2bd08da2c5af
ms.openlocfilehash: 45bcd64b60e7d13f389064faefeda815ea1f32c9
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286534"
---
# <a name="-operator-c-reference"></a>/ 演算子 (C# リファレンス)

除算演算子 `/` は、1 つ目のオペランドを 2 つ目のオペランドで除算します。 数値型はすべて除算演算子に対応しています。

## <a name="integer-division"></a>整数の除算

整数型のオペランドに対する `/` 演算子の結果は、整数型で、2 つのオペランドの商を 0 方向に丸めたものと等しくなります。

[!code-csharp-interactive[integer division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#Integer)]

2 つのオペランドの商を浮動小数点数として取得するには、`float`、`double`、または `decimal` 型を使います。

[!code-csharp-interactive[integer as floating-point division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#IntegerAsFloatingPoint)]

## <a name="floating-point-division"></a>浮動小数点の除算

`float`、`double`、`decimal` 型に対する `/` 演算子の結果は、2 つのオペランドの商となります。

[!code-csharp-interactive[floating-point division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#FloatingPoint)]

オペランドの 1 つが `decimal` であった場合、もう 1 つのオペランドを `float` や `double` にすることはできません。`float` と `double` は暗黙的に `decimal` に変換できないためです。 `float` または `double` オペランドは明示的に `decimal` 型に変換する必要があります。 数値型間の暗黙的な変換について詳しくは、「[暗黙的な数値変換の一覧表](../keywords/implicit-numeric-conversions-table.md)」をご覧ください。

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型は `/` 演算子を[オーバーロード](../keywords/operator.md)できます。 `/` 演算子をオーバーロードすると、[除算代入演算子](division-assignment-operator.md) `/=` も暗黙的にオーバーロードされます。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、「[C# 言語仕様](../language-specification/index.md)」の「[除算演算子](~/_csharplang/spec/expressions.md#division-operator)」セクションを参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
- [% 演算子](remainder-operator.md)
