---
title: Null 許容型の使用 (C# プログラミング ガイド)
description: Learn how to work with C# nullable types (C# Null 許容型の操作方法について)
ms.date: 08/02/2018
helpviewer_keywords:
- nullable types [C#], about nullable types
ms.assetid: 0bacbe72-ce15-4b14-83e1-9c14e6380c28
ms.openlocfilehash: 600a18cc4dc9d3eda5577336f209c5814a7edb88
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42933130"
---
# <a name="using-nullable-types-c-programming-guide"></a>Null 許容型の使用 (C# プログラミング ガイド)

Null 許容型は、基になる値型 `T` のすべての値と、追加の [null](../../language-reference/keywords/null.md) 値を表す型です。 詳細については、「[Null 許容型](index.md)」のトピックを参照してください。

Null 許容型は、`Nullable<T>` または `T?` のいずれかの形式で参照できます。 この 2 つの形式は同義であり、どちらでも使用できます。  
  
## <a name="declaration-and-assignment"></a>宣言と代入

値型は、対応する Null 許容型に暗黙的に変換できるので、基になる値型の場合と同様に Null 許容型に値を代入します。 `null` 値を代入することもできます。  例:
  
[!code-csharp[declare and assign](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#1)]

## <a name="examination-of-a-nullable-type-value"></a>Null 許容型の値の検査

Null 許容型のインスタンスが null かどうかを調べて、基になる型の値を取得するには、次の読み取り専用プロパティを使用します。  
  
- <xref:System.Nullable%601.HasValue%2A?displayProperty=nameWithType> は、Null 許容型のインスタンスに、基になる型の値が含まれるかどうかを示します。
  
- <xref:System.Nullable%601.HasValue%2A> が `true` の場合、<xref:System.Nullable%601.Value%2A?displayProperty=nameWithType> は基になる型の値を取得します。 <xref:System.Nullable%601.HasValue%2A> が `false` の場合、<xref:System.Nullable%601.Value%2A> プロパティは <xref:System.InvalidOperationException> をスローします。
  
次の例のコードでは、`HasValue` プロパティを使用して、値を表示する前に変数に値が格納されているかどうかをテストします。
  
[!code-csharp-interactive[use HasValue](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#2)]
  
次の例に示すように、`HasValue` プロパティを使用する代わりに、Null 許容型の変数を `null` と比較することもできます。  
  
[!code-csharp-interactive[use comparison with null](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#3)]

C# 7.0 以降では、[パターン マッチング](../../pattern-matching.md)を使用して Null 許容型の値を調べて取得することができます。

[!code-csharp-interactive[use pattern matching](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#4)]

## <a name="conversion-from-a-nullable-type-to-an-underlying-type"></a>Null 許容型から基になる型への変換

Null 許容型の値を Null 非許容型に代入する必要がある場合は、[Null 合体演算子 `??`](../../language-reference/operators/null-coalescing-operator.md) を使用して、Null 許容型の値が null の場合に代入される値を指定します (<xref:System.Nullable%601.GetValueOrDefault(%600)?displayProperty=nameWithType> メソッドを使用してこの操作を行うこともできます)。
  
[!code-csharp-interactive[?? operator](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#5)]

Null 許容型の値が null の場合に使用される値を、基になる値型の既定値にする場合は、<xref:System.Nullable%601.GetValueOrDefault?displayProperty=nameWithType> メソッドを使用します。
  
Null 許容型を Null 非許容型に明示的にキャストすることができます。 例:  
  
[!code-csharp[explicit cast](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#6)]

実行時に Null 許容型の値が null の場合は、明示的なキャストによって <xref:System.InvalidOperationException> がスローされます。

Null 非許容値型は、対応する Null 許容型に暗黙的に変換されます。
  
## <a name="operators"></a>演算子

値型向けに存在している定義済みの単項演算子、2 項演算子およびすべてのユーザー定義演算子は、Null 許容型でも使用できます。 これらの演算子では、1 つまたは両方のオペランドが null の場合は null 値が生成され、null 以外の場合は、含まれている値に基づいて結果が算出されます。 例:  
  
[!code-csharp[operators](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#7)]
  
関係演算子 (`<`、`>`、`<=`、`>=`) では、1 つまたは両方のオペランドが null の場合、結果は `false` になります。 ある比較 (たとえば、`<=`) から返される結果が `false` であっても、逆の比較 (`>`) から返される結果が `true` であるとは限りません。 次の例は、10 が

- null より大きくも等しくもなく、
- null 未満でもないことを示しています。
  
[!code-csharp-interactive[relational and equality operators](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#8)]
  
上記の例は、どちらも null である 2 つの null 許容型を等価比較すると、結果が `true` と評価されることを示しています。

## <a name="boxing-and-unboxing"></a>ボックス化とボックス化解除

Null 許容値型は、次の規則に従って[ボックス化](../types/boxing-and-unboxing.md)されます。

- <xref:System.Nullable%601.HasValue%2A> が `false` を返した場合は、null 参照が生成されます。  
- <xref:System.Nullable%601.HasValue%2A> が `true` を返した場合は、<xref:System.Nullable%601> のインスタンスではなく、基になる値型 `T` の値がボックス化されます。

次の例に示すように、ボックス化された値型を、対応する Null 許容型にボックス化解除できます。

[!code-csharp-interactive[boxing and unboxing](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#9)]

## <a name="the-bool-type"></a>bool? 型

Null 許容 `bool?` 型は、[true](../../language-reference/keywords/true-literal.md)、[false](../../language-reference/keywords/false-literal.md)、[null](../../language-reference/keywords/null.md) の 3 つの異なる値を格納できます。 `bool?` 型は、SQL で使用されるブール変数型に似ています。 `&` 演算子と `|` 演算子によって生成される結果が SQL の 3 値のブール型と一致するようにするには、次の定義済みの演算子を指定します。

- `bool? operator &(bool? x, bool? y)`  
- `bool? operator |(bool? x, bool? y)`  
  
次の表に、これらの演算子のセマンティクスが定義されています。  
  
|x|Y|x&y|x&#124;y|  
|-------|-------|---------|--------------|  
|true|true|true|true|  
|TRUE|False|false|true|  
|true|null|null|true|  
|False|true|False|true|  
|False|False|False|False|  
|False|null|False|null|  
|null|true|null|true|  
|null|False|False|null|  
|null|null|null|null|  

これら 2 つの演算子は、「[演算子](#operators)」セクションで説明されている規則に従わないことに注意してください。オペランドの 1 つが null の場合も、演算子の評価の結果は null 以外である可能性があります。
  
## <a name="see-also"></a>関連項目

 [Null 許容型](index.md)  
 [C# プログラミング ガイド](../../programming-guide/index.md)  
 [What Exactly Does 'Lifted' mean? ('Lifted' の正確な意味)](https://blogs.msdn.microsoft.com/ericlippert/2007/06/27/what-exactly-does-lifted-mean/)  
