---
title: -- 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- --_CSharpKeyword
helpviewer_keywords:
- -- operator [C#]
- decrement operator (--) [C#]
ms.assetid: 6b9cfe86-63c7-421f-9379-c9690fea8720
ms.openlocfilehash: 4fba014e8dabc13cd874e17f23515dc29d93f24b
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236928"
---
# <a name="---operator-c-reference"></a>-- 演算子 (C# リファレンス)

単項デクリメント演算子 `--` は、オペランドを 1 ずつデクリメントします。 それは、後置デクリメント演算子である `x--` と、前置デクリメント演算子である`--x` という 2 つの形式でサポートされます。

## <a name="postfix-decrement-operator"></a>後置デクリメント演算子

次の例に示すように、`x--` の結果は、演算子の "*前の*" `x` 値です。

[!code-csharp-interactive[postfix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PostfixDecrement)]

## <a name="prefix-decrement-operator"></a>前置デクリメント演算子

次の例に示すように、`--x` の結果は、演算子の "*後ろの*" `x` 値です。

[!code-csharp-interactive[prefix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PrefixDecrement)]

## <a name="remarks"></a>コメント

デクリメント演算子は、すべての[整数型](../keywords/integral-types-table.md) ([文字](../keywords/char.md) 型を含みます)、[浮動小数点型](../keywords/floating-point-types-table.md)、および任意の[列挙](../keywords/enum.md)型に対して、事前に定義されています。

デクリメント演算子のオペランドは、変数、[プロパティ](../../programming-guide/classes-and-structs/properties.md)のアクセス、または[インデクサー](../../../csharp/programming-guide/indexers/index.md)のアクセスである必要があります。

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型は `--` 演算子を[オーバーロード](../keywords/operator.md)できます。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、「[C# 言語仕様](../language-specification/index.md)」の「[後置インクリメント演算子と後置デクリメント演算子](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators)と「[前置インクリメント演算子と前置デクリメント演算子](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators)」セクションを参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
- [++ 演算子](increment-operator.md)
- [方法: ポインターのインクリメントとデクリメント](../../programming-guide/unsafe-code-pointers/how-to-increment-and-decrement-pointers.md)
