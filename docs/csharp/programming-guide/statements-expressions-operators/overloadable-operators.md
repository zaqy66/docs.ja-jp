---
title: オーバーロード可能な演算子 - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 08/27/2018
helpviewer_keywords:
- C# language, operator overloading
- operator overloading [C#]
ms.assetid: 390d9d01-79fc-40ab-9ed3-0bf448da1b6a
ms.openlocfilehash: ce346920c301aabf652ea0e141d4a2f66a3e8b2d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54616252"
---
# <a name="overloadable-operators-c-programming-guide"></a>オーバーロード可能な演算子 (C# プログラミング ガイド)

C# では、[operator](../../language-reference/keywords/operator.md) キーワードを使用して静的なメンバー関数を定義することで、ユーザー定義型で演算子をオーバーロードできます。 ただし、次の表に示すように、すべての演算子をオーバーロードできるわけではなく、制限付きでオーバーロードできる演算子もあります。

| 演算子 | オーバーロード可/不可 |
| --------- | --------------- |
|[+](../../language-reference/operators/addition-operator.md)、[-](../../language-reference/operators/subtraction-operator.md)、[!](../../language-reference/operators/logical-negation-operator.md)、[~](../../language-reference/operators/bitwise-complement-operator.md)、[++](../../language-reference/operators/increment-operator.md)、[--](../../language-reference/operators/decrement-operator.md)、[true](../../language-reference/keywords/true.md)、[false](../../language-reference/keywords/false.md)|これらの単項演算子はオーバーロードできます。|
|[+](../../language-reference/operators/addition-operator.md)、[-](../../language-reference/operators/subtraction-operator.md)、[\*](../../language-reference/operators/multiplication-operator.md)、[/](../../language-reference/operators/division-operator.md)、[%](../../language-reference/operators/modulus-operator.md)、[&](../../language-reference/operators/and-operator.md)、[&#124;](../../language-reference/operators/or-operator.md)、[^](../../language-reference/operators/xor-operator.md)、[\<\<](../../language-reference/operators/left-shift-operator.md)、[>>](../../language-reference/operators/right-shift-operator.md)|これらの 2 項演算子はオーバーロードできます。|
|[==](../../language-reference/operators/equality-comparison-operator.md)、[!=](../../language-reference/operators/not-equal-operator.md)、[\<](../../language-reference/operators/less-than-operator.md)、[>](../../language-reference/operators/greater-than-operator.md)、[\<=](../../language-reference/operators/less-than-equal-operator.md)、[>=](../../language-reference/operators/greater-than-equal-operator.md)|比較演算子はオーバーロードできます (この表の後の注を参照してください)。|
|[&&](../../language-reference/operators/conditional-and-operator.md)、[&#124;&#124;](../../language-reference/operators/conditional-or-operator.md)|条件付き論理演算子はオーバーロードできません。ただし、オーバーロードできる `&` と <code>&#124;</code> を使用して評価できます。|
|[&#91;&#93;](../../language-reference/operators/index-operator.md)|配列のインデックス付け演算子はオーバーロードできませんが、[インデクサー](../indexers/index.md)を定義できます。|
|[(T)x](../../language-reference/operators/invocation-operator.md)|キャスト演算子はオーバーロードできませんが、新しい変換演算子を定義できます (「[explicit](../../language-reference/keywords/explicit.md)」および「[implicit](../../language-reference/keywords/implicit.md)」を参照してください)。|
|[+=](../../language-reference/operators/addition-assignment-operator.md), [-=](../../language-reference/operators/subtraction-assignment-operator.md), [\*=](../../language-reference/operators/multiplication-assignment-operator.md), [/=](../../language-reference/operators/division-assignment-operator.md), [%=](../../language-reference/operators/modulus-assignment-operator.md), [&=](../../language-reference/operators/and-assignment-operator.md), [&#124;=](../../language-reference/operators/or-assignment-operator.md), [^=](../../language-reference/operators/xor-assignment-operator.md), [\<\<=](../../language-reference/operators/left-shift-assignment-operator.md), [>>=](../../language-reference/operators/right-shift-assignment-operator.md)|代入演算子は明示的にオーバー ロードすることはできません。 ただし、二項演算子をオーバーロードするとき、対応する代入演算子がある場合は、それも暗黙的にオーバーロードされます。 たとえば、`+=` は、オーバーロード可能な `+` を使用して評価されます。|
|[=](../../language-reference/operators/assignment-operator.md)、[.](../../language-reference/operators/member-access-operator.md)、[?:](../../language-reference/operators/conditional-operator.md)、[??](../../language-reference/operators/null-coalescing-operator.md)、[->](../../language-reference/operators/dereference-operator.md)、[=>](../../language-reference/operators/lambda-operator.md)、[f(x)](../../language-reference/operators/invocation-operator.md)、[as](../../language-reference/keywords/as.md)、[checked](../../language-reference/keywords/checked.md)、[unchecked](../../language-reference/keywords/unchecked.md)、[default](../../programming-guide/statements-expressions-operators/default-value-expressions.md)、[delegate](../../programming-guide/statements-expressions-operators/anonymous-methods.md)、[is](../../language-reference/keywords/is.md)、[new](../../language-reference/keywords/new.md)、[sizeof](../../language-reference/keywords/sizeof.md)、[typeof](../../language-reference/keywords/typeof.md)|これらの演算子はオーバーロードできません。|

> [!NOTE]
> 比較演算子をオーバーロードする場合はペアでオーバーロードする必要があります。つまり、`==` をオーバーロードする場合は `!=` もオーバーロードする必要があります。 逆もまた真であり、`!=` をオーバーロードする場合は、`==` のオーバーロードも必要です。 比較演算子 `<` と `>`、および `<=` と `>=` の場合も同様です。

演算子をオーバー ロードする方法については、[演算子](../../language-reference/keywords/operator.md)キーワードに関する記事を参照してください。

## <a name="see-also"></a>関連項目

- [C# プログラミング ガイド](../index.md)
- [ステートメント、式、および演算子](index.md)
- [演算子](operators.md)
- [C# 演算子](../../language-reference/operators/index.md)
- [C# のオーバーロードされた演算子が常に静的である理由](https://blogs.msdn.microsoft.com/ericlippert/2007/05/14/why-are-overloaded-operators-always-static-in-c/)
