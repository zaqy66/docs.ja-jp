---
title: 冗語構文 (F#)
description: F# プログラミング言語の詳細であり、軽量構文の違いについて説明します。
ms.date: 05/16/2016
ms.openlocfilehash: b4f2354738da4692cb444e5e7dd9531d80d26664
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44367944"
---
# <a name="verbose-syntax"></a>冗語構文

F# 言語で多くの構成要素に使用できる 2 つの形式の構文は:*冗語構文*と*軽量構文*します。 冗語構文は、一般的に使用されませんが、インデントを受けにくくなるという利点があります。 などの他のキーワード、軽量構文が短いとインデントを先頭と末尾、コンストラクトの使用ではなく`begin`、 `end`、`in`など。 既定の構文は、軽量構文です。 このトピックでは、軽量構文が有効でない場合、f# の構成要素の構文をについて説明します。 冗語構文はのでまま一部のコンストラクトの冗語構文を使用することができる場合でも、軽量構文を有効にすると、常に有効です。 使用して軽量構文を無効にすることができます、`#light "off"`ディレクティブ。

## <a name="table-of-constructs"></a>テーブルの構成体

次の表では、f# 言語コンストラクトの軽量と詳細な構文を示しますのコンテキストで 2 つの形式の違いがあります。 この表では、角度を角かっこ (&lt;&gt;) 構文のユーザーが指定した要素で囲みます。 これらのコンストラクト内で使用される構文の詳細情報の各言語構成要素は、ドキュメントを参照してください。

<table>
<tr>
<th>言語構成要素</th>
<th>軽量構文</th>
<th>冗語構文</th>
</tr>
<tr>
<td>
複合式
</td>
<td>

```xml
<expression1>
<expression2>
```
</td><td>

```
<expression1>; <expression2>
```

</td>
</tr>
<tr><td>


入れ子になった`let`バインド

</td><td>
```
let f x =
    let a = 1
    let b = 2
    x + a + b
```

</td><td>

```
let f x =
    let a = 1 in
    let b = 2 in
    x + a + b
```

</td>
</tr>
<tr><td>
コード ブロック
</td><td>

```
(
    <expression1>
    <expression2>
)
```

</td><td>

```
begin
    <expression1>;
    <expression2>;
end
```
</td>
</tr>
<tr><td>
`for...do`
</td><td>

```
for counter = start to finish do
    ...
```

</td><td>

```
for counter = start to finish do
    ...
done
```

</td>
</tr>
<tr><td>
`while...do`
</td><td>

```
while <condition> do
    ...
```

</td><td>

```
while <condition> do
    ...
done
```

</td>
</tr>
<tr><td>
`for...in`
</td><td>

```
for var in start .. finish do
    ...
```

</td><td>

```
for var in start .. finish do
    ...
done
```

</td>
</tr>
<tr><td>
`do`
</td><td>

```
do
    ...
```

</td><td>

```
do
    ...
in
```

</td>
</tr>
<tr><td>レコード
</td><td>

```
type <record-name> =
    {
        <field-declarations>
    }
    <value-or-member-definitions>
```

</td><td>

```
type <record-name> =
    {
        <field-declarations>
    }
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td>class
</td><td>
```
type <class-name>(<params>) = ... ```

</td><td>

```
type <class-name>(<params>) =
    class
        ...
    end
```
</td>
</tr>
<tr><td>構造体</td><td>

```
[<StructAttribute>]
type <structure-name> =
    ...
```
</td><td>

```
type <structure-name> =
    struct
        ...
    end
```

</td>
</tr>
<tr><td>判別共用体</td><td>

```
type <union-name> =
    | ...
    | ...
    ...
    <value-or-member definitions>
```
</td><td>

```
type <union-name> =
    | ...
    | ...
    ...
    with
        <value-or-member-definitions>
    end    
```

</td>
</tr>
<tr><td>interface</td><td>

```
type <interface-name> =
    ...
```
</td><td>

```
type <interface-name> =
    interface
        ...
    end
```

</td>
</tr>
<tr><td>オブジェクト式</td><td>

```
{ new <type-name>
    with
        <value-or-member-definitions>
        <interface-implementations>
}
```

</td><td>

```
{ new <type-name>
    with
        <value-or-member-definitions>
    end
    <interface-implementations>
}
```

</td>
</tr>
<tr><td>インターフェイスの実装</td><td>

```
interface <interface-name>
    with
        <value-or-member-definitions>
```

</td><td>

```
interface <interface-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td>型の拡張機能</td><td>

```
type <type-name>
    with
        <value-or-member-definitions>
```

</td><td>

```
type <type-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td>name</td><td>

```
module <module-name> =
    ...
```

</td><td>

```
module <module-name> =
    begin
        ...
    end
```

</td>
</tr>
</table>

## <a name="see-also"></a>関連項目

- [F# 言語リファレンス](index.md)
- [コンパイラ ディレクティブ](compiler-directives.md)
- [コードのフォーマットに関するガイドライン](code-formatting-guidelines.md)
