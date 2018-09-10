---
title: operator キーワード (C# リファレンス)
description: 組み込みの C# 演算子をオーバー ロードする方法を学習する
ms.date: 08/27/2018
f1_keywords:
- operator_CSharpKeyword
- operator
helpviewer_keywords:
- operator keyword [C#]
ms.assetid: 59218cce-e90e-42f6-a6bb-30300981b86a
ms.openlocfilehash: 1e11d7767b61becc39b1158fae9cb2abe997e4bd
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44207630"
---
# <a name="operator-c-reference"></a>operator (C# リファレンス)

`operator` キーワードを使用して、組み込みの演算子をオーバーロードしたり、クラスまたは構造体宣言内でユーザー定義の変換を行ったりすることができます。

カスタム クラスまたは構造体上で演算子をオーバー ロードするには、対応する型で演算子の宣言を作成します。 組み込みの C# 演算子をオーバーロードする演算子宣言は、次の規則を満たす必要があります。

- これには、`public` と `static` 修飾子の両方が含まれています。
- これには `operator X` が含まれています。ここで、`X` は、オーバーロードされる演算子の名前またはシンボルです。
- 単項演算子にはパラメーターが 1 つ、2 項演算子にはパラメーターが 2 つあります。 いずれの場合も、少なくとも 1 つのパラメーターが演算子を宣言するクラスまたは構造体と同じ型である必要があります。

変換演算子を定義する方法については、[明示的なキーワード](explicit.md)と[暗黙的なキーワード](implicit.md)に関する記事を参照してください。

オーバーロードできる C# 演算子の概要については、[オーバーロード可能な演算子](../../programming-guide/statements-expressions-operators/overloadable-operators.md)に関する記事を参照してください。

## <a name="example"></a>例

次の例では、小数部を表す `Fraction` 型が定義されています。 このクラスは、小数の加算および乗算を実行するために `+` 演算子および `*` 演算子をオーバーロードします。また、`Fraction` 型を `double` 型に変換する変換演算子も提供します。

[!code-csharp[csrefKeywordsConversion#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsConversion/CS/csrefKeywordsConversion.cs#6)]

## <a name="c-language-specification"></a>C# 言語仕様

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [C# のキーワード](index.md)
- [implicit](implicit.md)
- [explicit](explicit.md)
- [オーバーロード可能な演算子](../../programming-guide/statements-expressions-operators/overloadable-operators.md)
- [方法: 構造体間にユーザー定義の変換を実装する](../../programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)
