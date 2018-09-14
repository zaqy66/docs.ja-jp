---
title: インデックス付きプロパティ (F#)
description: F# でのインデックス付きプロパティ、される順序付けられたデータを配列に似たアクセスを提供するプロパティについて説明します。
ms.date: 05/16/2016
ms.openlocfilehash: e56e4e2ea3f35df4c8ec46012357242cb6ce69f3
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2018
ms.locfileid: "45583425"
---
# <a name="indexed-properties"></a>インデックス付きプロパティ

*インデックス付きプロパティ*データは順序付けを配列に似たアクセスを提供するプロパティ。 これらは 3 つの形式があります。

* `Item`
* `Ordinal`
* `Cardinal`

F# のメンバーは、配列に似たアクセスを提供するこれら 3 つの名前の 1 つ名前する必要があります。 `IndexerName` 次の 3 つのオプションのいずれかを表すために使用します。

## <a name="syntax"></a>構文

```fsharp
// Indexed property that has both get and set defined.
member self-identifier.IndexerName
    with get(index-variable) =
        get-function-body
    and set index-variablesvalue-variables =
        set-function-body

// Indexed property that has get only.
member self-identifier.IndexerName(index-variable) =
    get-function-body

// Alternative syntax for indexed property with get only
member self-identifier.IndexerName
    with get(index-variables) =
        get-function-body

// Indexed property that has set only.
member self-identifier.IndexerName
    with set index-variablesvalue-variables = 
        set-function-body
```

## <a name="remarks"></a>Remarks

前の構文のフォームは、両方があるインデックス付きプロパティを定義する方法を示して、`get`と`set`メソッドが、`get`メソッドのみかが、`set`メソッドのみ。 取得のみと set のみに対して表示される構文に示す構文を組み合わせてまたを get と set の両方を持つプロパティを生成します。 この後者の形式を使用すると、get に異なるアクセシビリティ修飾子と属性を配置し、メソッドを設定できます。

ときに、 *IndexerName*は`Item`コンパイラは、既定のインデックス付きプロパティとしてプロパティを扱います。 A*既定のインデックス付きプロパティ*オブジェクト インスタンスの配列に似た構文を使用してアクセスできるプロパティです。 たとえば場合、`obj`構文は、このプロパティを定義する型のオブジェクトである`obj.[index]`プロパティにアクセスするために使用します。

既定以外のインデックス付きプロパティにアクセスするための構文は、プロパティとかっこ内のインデックスの名前を提供します。 たとえば、次のプロパティが`Ordinal`、記述する`obj.Ordinal(index)`へのアクセスします。

使用する形式に関係なくのカリー化された形式を使用する必要があります常に、`set`インデックス付きプロパティのメソッド。 カリー化関数については、次を参照してください。[関数](../functions/index.md)します。

## <a name="example"></a>例

次のコード例では、定義と使用の既定と既定以外のインデックス付きプロパティ get し、set メソッドを示しています。

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3301.fs)]

## <a name="output"></a>出力

```
ONE two three four five six seven eight nine ten
ONE first two second three third four fourth five fifth six 6th
seven seventh eight eighth nine ninth ten tenth
```

## <a name="indexed-properties-with-multiple-index-variables"></a>複数のインデックス変数でインデックス付きプロパティ

インデックス付きプロパティには、1 つ以上のインデックス変数をことができます。 その場合は、変数は、プロパティを使用すると、コンマで区切られます。 このようなプロパティの set メソッドには、キーを含むタプル 1 つ目は、2 番目の値が設定されているは 2 つのカリー化された引数が必要です。

次のコードでは、複数のインデックス変数でインデックス付きプロパティの使用を示します。

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3302.fs)]

## <a name="see-also"></a>関連項目

- [メンバー](index.md)
