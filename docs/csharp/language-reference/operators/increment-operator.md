---
title: ++ 演算子 (C# リファレンス)
ms.date: 11/26/2018
f1_keywords:
- ++_CSharpKeyword
helpviewer_keywords:
- increment operator (++) [C#]
- ++ operator [C#]
ms.assetid: e9dec353-070b-44fb-98ed-eb8fdf753feb
ms.openlocfilehash: b29f4f1ab00c0f8026f118cb72b090e3b728bfc5
ms.sourcegitcommit: 6ae7cdd0437a32884556dd4826ca90e957b7a4e3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2018
ms.locfileid: "48030471"
---
# <a name="-operator-c-reference"></a>++ 演算子 (C# リファレンス)

単項インクリメント演算子 `++` は、オペランドを 1 ずつインクリメントします。 それは、後置インクリメント演算子である `x++` と、前置インクリメント演算子である`++x` という 2 つの形式でサポートされます。

## <a name="postfix-increment-operator"></a>後置インクリメント演算子

次の例に示すように、`x++` の結果は、演算子の`x` "*前の*" 値です。

[!code-csharp-interactive[postfix increment](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PostfixIncrement)]

## <a name="prefix-increment-operator"></a>前置インクリメント演算子

次の例に示すように、`++x` の結果は、演算子の`x` "*後ろの*" 値です。

[!code-csharp-interactive[prefix increment](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PrefixIncrement)]

## <a name="remarks"></a>コメント

インクリメント演算子は、すべての[整数型](../keywords/integral-types-table.md) ([文字](../keywords/char.md) 型を含みます)、[浮動小数点型](../keywords/floating-point-types-table.md)、および任意の[列挙](../keywords/enum.md)型に対して、事前に定義されています。

インクリメント演算子のオペランドは、変数、[プロパティ](../../programming-guide/classes-and-structs/properties.md)のアクセス、または [インデクサー](../../../csharp/programming-guide/indexers/index.md)のアクセスである必要があります。

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型は `++` 演算子を[オーバーロード](../keywords/operator.md)できます。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、「[C# 言語仕様](../language-specification/index.md)」の「[後置インクリメント演算子と後置デクリメント演算子](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators)と「[前置インクリメント演算子と前置デクリメント演算子](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators)」セクションを参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
- [-- 演算子](decrement-operator.md)
- [方法: ポインターのインクリメントとデクリメント](../../programming-guide/unsafe-code-pointers/how-to-increment-and-decrement-pointers.md)
