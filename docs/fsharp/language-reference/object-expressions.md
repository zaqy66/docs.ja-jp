---
title: オブジェクト式 (F#)
description: 名前付きの型コードを追加し、新たに作成するために必要なオーバーヘッドを回避するときに、F# オブジェクト式を使用する方法をについて説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 1a971044d680d3bf5a6fff38affdaf001d5403b4
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "43865463"
---
# <a name="object-expressions"></a>オブジェクト式

*オブジェクト式*は動的に作成された、匿名のオブジェクトの種類の新しいインスタンスを作成する式が、既存の基本型、インターフェイス、またはインターフェイスのセットに基づいてです。

## <a name="syntax"></a>構文

```fsharp
// When typename is a class:
{ new typename [type-params]arguments with
    member-definitions
    [ additional-interface-definitions ]
}
// When typename is not a class:
{ new typename [generic-type-args] with
    member-definitions
    [ additional-interface-definitions ]
}
```

## <a name="remarks"></a>Remarks

前の構文で、 *typename*既存のクラス型またはインターフェイス型を表します。 *型 params*省略可能なジェネリック型パラメーターについて説明します。 *引数*コンス トラクターのパラメーターを必要とするクラス型にのみ使用されます。 *メンバー定義*は基底クラスのメソッドのオーバーライドまたは基底クラスまたはインターフェイスのいずれかの抽象メソッドの実装。

次の例は、さまざまな種類のオブジェクト式を示しています。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4301.fs)]

## <a name="using-object-expressions"></a>オブジェクトの式の使用

余分なコードと名前付きの型を新しく作成する必要なオーバーヘッドを回避する場合に、オブジェクトの式を使用します。 プログラムで作成された型の数を最小限に抑えるには、オブジェクト表現を使用する場合のコード行の数を削減し、型の不要な急増を回避できます。 特定の状況に対処するためだけに多くの種類を作成する代わりには、既存の種類をカスタマイズできます。 または、特定の状況に適切なインターフェイスの実装を提供するオブジェクト式を使用することができます。

## <a name="see-also"></a>関連項目

- [F# 言語リファレンス](index.md)
