---
title: string - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- string
- string_CSharpKeyword
helpviewer_keywords:
- strings [C#], reference
- '@ string literal'
- string literals [C#]
- string keyword [C#]
ms.assetid: 3037e558-fb22-494d-bca1-a15ade11b11a
ms.openlocfilehash: f6c76f8effc5aef82803014b9a7257c2ad6865b8
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286482"
---
# <a name="string-c-reference"></a>string (C# リファレンス)

`string` 型は、0 個以上の Unicode 文字のシーケンスを表します。 `string` は .NET の <xref:System.String> の別名です。

`string` は参照型ですが、等値演算子 (`==` および `!=`) は、`string` オブジェクトの参照ではなく、値を比較するように定義されています。 これにより、文字列が等しいかを直感的にテストできます。 次に例を示します。

```csharp
string a = "hello";
string b = "h";
// Append to contents of 'b'
b += "ello";
Console.WriteLine(a == b);
Console.WriteLine((object)a == (object)b);
```

文字列の内容が等しいので、"True"、"False" の順に表示されますが、`a` および `b` は同じ文字列インスタンスを参照しません。

+ 演算子は、文字列を連結します。

```csharp
string a = "good " + "morning";
```

これは、"good morning" を含む文字列オブジェクトを作成します。

文字列は "*変更不可*" です。文字列オブジェクトの作成後、そのコンテンツを変更することはできません。構文では変更可能に見えても、変更不可です。 たとえば、このコードを作成すると、コンパイラによって新しい文字列オブジェクトを格納する新しいシーケンス オブジェクトが生成され、その新しいオブジェクトが b に割り当てられます。 そして、文字列 "h" がガベージ コレクションの対象になります。

```csharp
string b = "h";
b += "ello";
```

[] 演算子は、`string` の各文字への読み取り専用アクセスに使用できます。

```csharp
string str = "test";
char x = str[2];  // x = 's';
```

同様に、[] 演算子を使って `string` 内の各文字を反復処理することもできます。

```csharp
string str = "test";

for (int i = 0; i < str.Length; i++)
{
  Console.Write(str[i] + " ");
}
// Output: t e s t
``` 

リテラル文字列は `string` 型であり、二重引用符で囲む形式と、@-quoted 付きの二重引用符で囲む形式の 2 種類があります。 二重引用符で囲む場合は、リテラル文字列の前後に二重引用符 (") を付けます。

```csharp
"good morning"  // a string literal
```

リテラル文字列には、任意の文字リテラルを含めることができます。 これにはエスケープ シーケンスが含まれます。 次の例では、円記号にエスケープ シーケンス `\\`、文字 f に `\u0066`、改行に `\n` を使用しています。

```csharp
string a = "\\\u0066\n";
Console.WriteLine(a);
```

> [!NOTE]
> エスケープ コード `\udddd` (`dddd` は 4 桁の数字) は、Unicode 文字 U +`dddd` を表します。 8 桁の Unicode エスケープ コード `\Udddddddd` も認識できます。

verbatim 文字列リテラルの場合は、先頭に `@` を付け、さらに前後に二重引用符を付けます。 次に例を示します。

```csharp
@"good morning"  // a string literal
```

verbatim 文字列の場合の利点は、エスケープ シーケンスが "*処理されない*" ため、たとえば、完全修飾ファイル名が書きやすくなることです。

```csharp
@"c:\Docs\Source\a.txt"  // rather than "c:\\Docs\\Source\\a.txt"
```

@-quoted に続いて引用符で囲まれた文字列に二重引用符を含めるには、二重引用符を二重にします。

```csharp
@"""Ahoy!"" cried the captain." // "Ahoy!" cried the captain.
```

`@` 特殊文字のその他の使用については、[@ -- 逐語的識別子](../tokens/verbatim.md)に関するページを参照してください。

C# での文字列の詳細については、「[文字列](../../programming-guide/strings/index.md)」を参照してください。

## <a name="example"></a>例

[!code-csharp[csrefKeywordsTypes#17](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#17)]  

## <a name="c-language-specification"></a>C# 言語仕様

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [文字列を使用するためのベスト プラクティス](../../../standard/base-types/best-practices-strings.md)
- [C# のキーワード](index.md)
- [参照型](reference-types.md)
- [値型](value-types.md)
- [基本的な文字列操作](../../../standard/base-types/basic-string-operations.md)
- [新しい文字列の作成](../../../standard/base-types/creating-new.md)
- [数値結果テーブルの書式設定](formatting-numeric-results-table.md)
