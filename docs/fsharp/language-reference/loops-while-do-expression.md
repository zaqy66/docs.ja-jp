---
title: 'ループ: while...do 式 (F#)'
description: 参照してください、... 中は式を使用して、指定したテスト条件が true の場合は、反復実行 (ループ) を実行します。
ms.date: 05/16/2016
ms.openlocfilehash: 5cf4461669221f91cb50e238c25494f03a10bbc2
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44130226"
---
# <a name="loops-whiledo-expression"></a>ループ: while...do 式

`while...do`式を使用して、指定したテスト条件が true の場合は、反復実行 (ループ) を実行します。

## <a name="syntax"></a>構文

```fsharp
while test-expression do
    body-expression
```

## <a name="remarks"></a>Remarks

*テスト式*評価; である場合は、 `true`、*式の本体*を実行し、もう一度テスト式が評価されます。 *式の本体*型である必要があります`unit`します。 場合テスト式`false`イテレーションが終了します。

次の例では、使用、`while...do`式。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5301.fs)]

前のコードの出力は、1 から 20 までのランダムな数値のうち、最後は 10 ストリームです。

```
13 19 8 18 16 2 10
Found a 10!
```

>[!NOTE]
使用することができます`while...do`シーケンス式とその他のコンピュテーション式で、カスタマイズされたバージョンの場合、`while...do`式を使用します。 詳細については、次を参照してください。[シーケンス](sequences.md)、[非同期ワークフロー](asynchronous-workflows.md)、および[コンピュテーション式](computation-expressions.md)します。

## <a name="see-also"></a>関連項目

- [F# 言語リファレンス](index.md)
- [ループ: `for...in` 式](loops-for-in-expression.md)
- [ループ: `for...to` 式](loops-for-to-expression.md)
