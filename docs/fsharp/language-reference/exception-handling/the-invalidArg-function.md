---
title: '例外: invalidArg 関数 (F#)'
description: F# の 'invalidArg' 関数が引数の例外を生成する方法について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 8bf65fae9392a88205e3cdec8b7d7a3ff42f8416
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "44180320"
---
# <a name="exceptions-the-invalidarg-function"></a>例外: invalidArg 関数

`invalidArg`関数に引数例外が生成されます。

## <a name="syntax"></a>構文

```fsharp
invalidArg parameter-name error-message-string
```

## <a name="remarks"></a>Remarks

前の構文でパラメーター名は、文字列の引数が正しくないパラメーターの名前です。 *エラー メッセージの文字列*リテラル文字列または型の値は、`string`します。 `Message`例外オブジェクトのプロパティ。

によって生成された例外`invalidArg`は、`System.ArgumentException`例外。 次のコードの使用を示します`invalidArg`例外をスローします。

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet6101.fs)]

出力は、次は、後に (非表示) スタック トレース。

```
December
January
System.ArgumentException: Month parameter out of range.
```

## <a name="see-also"></a>関連項目

- [例外処理](index.md)
- [例外の種類](exception-types.md)
- [例外: `try...with` 式](the-try-with-expression.md)
- [例外: `try...finally` 式](the-try-finally-expression.md)
- [例外: `raise` 関数](the-raise-function.md)
- [例外: `failwith` 関数](the-failwith-function.md)
