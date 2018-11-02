---
title: do 束縛 (F#)
description: F# の 'do' のバインドを使用する方法、関数または値を定義することがなくコードを実行について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 78dbf8da0fe40b5af566ad98693df1109eede7e4
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "45973145"
---
# <a name="do-bindings"></a>do 束縛

A`do`関数または値を定義することがなくコードを実行するバインディングを使用します。 またはバインドできるクラスを使用してを参照してください[`do`クラス内のバインディング](../members/do-bindings-in-classes.md)します。

## <a name="syntax"></a>構文

```fsharp
[ attributes ]
[ do ]expression
```

## <a name="remarks"></a>Remarks

使用して、`do`関数または値の定義とは別にコードを実行するときにバインディングします。 内の式を`do`バインディングを返す必要があります`unit`します。 最上位のコード`do`モジュールの初期化時にバインディングを実行します。 キーワード`do`は省略可能です。

属性は、最上位レベルに適用できる`do`バインドします。 たとえば、プログラムでは、COM 相互運用機能を使用する場合があります適用する、`STAThread`属性をプログラムします。 属性を使用してこれを行う、`do`バインド、次のコードに示すようにします。

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet201.fs)]

## <a name="see-also"></a>関連項目

- [F# 言語リファレンス](../index.md)
- [関数](index.md)
