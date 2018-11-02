---
title: '例外: failwith 関数 (F#)'
description: "'Failwith' 関数は F# の例外を生成する方法について説明します。"
ms.date: 05/16/2016
ms.openlocfilehash: 69a2eb69e0157d3bde8cb8884cb0ae960634dddc
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "43863430"
---
# <a name="exceptions-the-failwith-function"></a>例外: failwith 関数

`failwith`関数は F# の例外を生成します。

## <a name="syntax"></a>構文

```fsharp
failwith error-message-string
```

## <a name="remarks"></a>Remarks

*エラー メッセージの文字列*リテラル文字列または型の値は、前の構文で`string`します。 `Message`例外のプロパティ。

によって生成される例外`failwith`は、`System.Exception`例外があり、名前を持つ参照`Failure`F# コードにします。 次のコードの使用を示します`failwith`例外をスローします。

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet6001.fs)]

## <a name="see-also"></a>関連項目

- [例外処理](index.md)
- [例外の種類](exception-types.md)
- [例外: `try...with` 式](the-try-with-expression.md)
- [例外: `try...finally` 式](the-try-finally-expression.md)
- [例外: `raise` 関数](the-raise-function.md)
