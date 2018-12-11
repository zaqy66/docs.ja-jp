---
title: 再帰関数:Rec キーワード (F#)
description: 再帰関数の定義に 'let' キーワードを使用して、F# の 'rec' キーワードが使用される方法について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 0db3ed7f85a1380654f2827b4773985b661589c7
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53127733"
---
# <a name="recursive-functions-the-rec-keyword"></a>再帰関数:Rec キーワード

`rec`と共にキーワードが使用される、`let`再帰関数を定義するキーワード。

## <a name="syntax"></a>構文

```fsharp
// Recursive function:
let rec function-nameparameter-list =
function-body

// Mutually recursive functions:
let rec function1-nameparameter-list =
function1-body
and function2-nameparameter-list =
function2-body
...
```

## <a name="remarks"></a>Remarks

再帰関数は、自身を呼び出す関数は、F# 言語で明示的に識別されます。 これにより、関数のスコープで定義されている識別子を使用可能なにします。

次のコードは、再帰関数を計算する、 *n*<sup>th</sup>フィボナッチ数。

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet4001.fs)]

> [!NOTE]
> 実際には、上記のようなコードは、事前に計算された値の再計算するため、メモリとプロセッサ時間の浪費になります。

メソッドは、暗黙的に型内で再帰追加する必要はありません、`rec`キーワード。 クラス内の let バインドは、暗黙的に再帰的ではできません。

## <a name="mutually-recursive-functions"></a>相互再帰関数

関数は、場合によって*相互再帰*呼び出しが、1 つの関数呼び出しを呼び出して、最初の呼び出しの数に別間に、円を描くことを意味します。 1 つで、このような関数をまとめて定義する必要があります`let`を使用したバインド、`and`それらをリンクするキーワード。

次の例は、2 つを相互には再帰関数。

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet4002.fs)]

## <a name="see-also"></a>関連項目

- [関数](index.md)
