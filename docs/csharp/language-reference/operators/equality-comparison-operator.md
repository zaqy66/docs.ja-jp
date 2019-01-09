---
title: == 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 12/14/2018
f1_keywords:
- ==_CSharpKeyword
helpviewer_keywords:
- == operator [C#]
- equality operator [C#]
ms.assetid: 34c6b597-caa2-4855-a7cd-38ecdd11bd07
ms.openlocfilehash: 6d86348eefc87e847267f262141ff49e5d51faae
ms.sourcegitcommit: 3d0c29b878f00caec288dfecb3a5c959de5aa629
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2018
ms.locfileid: "53655960"
---
# <a name="-operator-c-reference"></a>== 演算子 (C# リファレンス)

等値演算子 `==` は、そのオペランドが等しい場合には `true` を返し、それ以外の場合は `false` を返します。

## <a name="value-types-equality"></a>値の型の等価性

[組み込みの値の型](../keywords/value-types-table.md)のオペランドは、その値が等しい場合は等しくなります。

[!code-csharp-interactive[value types equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#ValueTypesEquality)]

> [!NOTE]
> 関係演算子 `==`、`>`、`<`、`>=`、および `<=` で、いずれかのオペランドが数字 (<xref:System.Double.NaN?displayProperty=nameWithType> または <xref:System.Single.NaN?displayProperty=nameWithType>) ではない場合、演算の結果は `false` になります。 つまり、`NaN` の値はそれ以外のどの `double` (または `float`) の値を上回ることも、下回ることも、等しいこともありません。 詳細およびサンプルについては、<xref:System.Double.NaN?displayProperty=nameWithType> または <xref:System.Single.NaN?displayProperty=nameWithType> の参照記事をご覧ください。

同じ[列挙](../keywords/enum.md)型の 2 つのオペランドは、基になる整数型の対応する値が等しい場合は等しくなります。

既定では、`==` 演算子はユーザー定義の[構造体](../keywords/struct.md)型には定義されていません。 ユーザー定義型は `==` 演算子を[オーバーロード](#operator-overloadability)できます。

C# 7.3 より、`==` および [`!=`](not-equal-operator.md) 演算子は C# の[タプル](../../tuples.md)によってサポートされています。 詳細については、「[C# のタプル型](../../tuples.md)」の記事の「[等値とタプル](../../tuples.md#equality-and-tuples)」のセクションを参照してください。

## <a name="string-equality"></a>文字列の等価性

2 つの [string](../keywords/string.md) オペランドは、その両方が `null` であるか、両方の文字列インスタンスの長さが同じで、それぞれの文字列の位置に同じ文字が含まれている場合に等しくなります。

[!code-csharp-interactive[string equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#StringEquality)]

序数の比較では大文字と小文字が区別されます。 文字列を比較する方法の詳細については、「[C# で文字列を比較する方法](../../how-to/compare-strings.md)」を参照してください。

## <a name="reference-types-equality"></a>参照型の等価性

`string` 参照型オペランド以外の 2 つは、同じオブジェクトを参照しているときに等しくなります。

[!code-csharp-interactive[reference type equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#ReferenceTypesEquality)]

次の例は、`==` 演算子がユーザー定義の参照型でサポートされていることを示しています。 ただし、ユーザー定義の参照型は `==` 演算子をオーバーロードできます。 参照型が `==` 演算子をオーバーロードする場合、その型の 2 つの参照が同じオブジェクトを参照しているかどうかを調べるには <xref:System.Object.ReferenceEquals%2A?displayProperty=nameWithType> メソッドを使用します。

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型は `==` 演算子を[オーバーロード](../keywords/operator.md)できます。 型が等値演算子 `==` をオーバーロードしている場合、[非等値演算子](not-equal-operator.md) `!=` もオーバーロードする必要があります。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[関係演算子と型検査演算子](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators)」のセクションを参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
- [等価比較](../../programming-guide/statements-expressions-operators/equality-comparisons.md)
