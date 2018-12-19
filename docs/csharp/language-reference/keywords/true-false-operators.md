---
title: true および false 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 12/10/2018
helpviewer_keywords:
- false operator [C#]
- true operator [C#]
ms.assetid: 81a888fd-011e-4589-b242-6c261fea505e
ms.openlocfilehash: 0a75566fdb6222157ecda12a50fd78e22f92fcb4
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245733"
---
# <a name="true-and-false-operators-c-reference"></a>true および false 演算子 (C# リファレンス)

`true` 演算子は、オペランドが確実に true であることを示す[ブール](bool.md)値 `true` を返します。 `false` 演算子は、オペランドが確実に false であることを示す `bool` 値 `true` を返します。 `true` および `false` 演算子が互いに補完することは保証されていません。 つまり、`true` と `false` 演算子の両方が同じオペランドに対して `bool` 値 `false` を返す場合があります。 ある型でこの 2 つの演算子の 1 つを定義する場合は、もう 1 つの演算子も定義する必要があります。

`true` と `false` 演算子が定義された型によって、[論理 OR 演算子](../operators/or-operator.md) `|` または[論理 AND 演算子](../operators/and-operator.md) `&` が特定の方法で[オーバーロード](operator.md)される場合、[条件付き論理 OR 演算子](../operators/conditional-or-operator.md) `||` または [条件付き論理 AND 演算子](../operators/conditional-and-operator.md) `&&` を、それぞれ、その型のオペランドに対して評価することができます。 詳細については、「[C# 言語仕様](../language-specification/index.md)」の[ユーザー定義型条件論理演算子](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators)に関するセクションを参照してください。

`true` 演算子が定義された型は、[if](if-else.md)、[do](do.md)、[while](while.md)、および [for](for.md) ステートメントと、[条件演算子 `?:`](../operators/conditional-operator.md) の制御条件式の結果の型にすることができます。 詳細については、「[C# 言語仕様](../language-specification/index.md)」の[ブール型の式](~/_csharplang/spec/expressions.md#boolean-expressions)に関するセクションを参照してください。

> [!TIP]
> 3 値ロジックをサポートする必要がある場合は、`bool?` 型を使用します。たとえば、3 値ロジック型をサポートするデータベースを操作する場合などです。 詳細については、「[Null 許容型の使用](../../programming-guide/nullable-types/using-nullable-types.md)」の記事の「[bool? 型](../../programming-guide/nullable-types/using-nullable-types.md#the-bool-type)」セクションを参照してください。

次の例では、`true` と `false` 演算子の両方を定義する型を示します。 さらに、論理 AND 演算子 `&` をオーバーロードして、演算子 `&&` もその型のオペランドで評価できるようにします。

[!code-csharp-interactive[true and false operators example](~/samples/snippets/csharp/keywords/TrueFalseOperatorsExample.cs)]

`&&` 演算子のショートサーキット動作に注意してください。 `GetFuelLaunchStatus` メソッドから `LaunchStatus.Red` が返されると、`&&` 演算子の 2 番目のオペランドは評価されません。 これは、`LaunchStatus.Red` が確実に false であるためです。 したがって、論理 AND の結果は 2 番目のオペランドの値に依存しません。 この例の出力は次のとおりです。

```console
Getting fuel launch status...
Wait!
```

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [C# のキーワード](index.md)
- [C# 演算子](../operators/index.md)
- [`true` リテラル](true-literal.md)
- [`false` リテラル](false-literal.md)