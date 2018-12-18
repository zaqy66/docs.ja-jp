---
title: ~ 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 11/05/2018
f1_keywords:
- ~_CSharpKeyword
helpviewer_keywords:
- tilde (~) one's complement operator [C#]
- ~ operator [C#]
- ~ [C#], bitwise complement operator
- bitwise complement operator [C#]
ms.assetid: 11bc078a-50e2-4d7e-9896-67ef669dc602
ms.openlocfilehash: 57e5baee423c0b5d9292d0ad4cbf909646eb3a38
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235726"
---
# <a name="-operator-c-reference"></a>~ 演算子 (C# リファレンス)

ビットごとの補数演算子 `~` は、各ビットを反転させてオペランドのビットごとの補数を生成する単項演算子です。 すべての整数型で `~` 演算子がサポートされます。

> [!NOTE]
> `~` シンボルはファイナライザーの宣言にも使用されます。 詳細については、「[Finalizers](../../programming-guide/classes-and-structs/destructors.md)」 (ファイナライザー) を参照してください。

`~` 演算子の使用例を次に示します。

[!code-csharp-interactive[bitwise NOT](~/samples/snippets/csharp/language-reference/operators/BitwiseComplementExamples.cs#Example)]

> [!NOTE]
> 上記の例では、[C# 7.0 で導入され](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements)、[C# 7.2 で強化された](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals)バイナリ リテラルを使用しています。

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型は `~` 演算子を[オーバーロード](../keywords/operator.md)できます。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、「[C# 言語仕様](../language-specification/index.md)」の「[ビットごとの補数演算子](~/_csharplang/spec/expressions.md#bitwise-complement-operator)」セクションを参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
- [ファイナライザー](../../programming-guide/classes-and-structs/destructors.md)
- [& 演算子](and-operator.md)
- [| 演算子](or-operator.md)
- [^ 演算子](xor-operator.md)
