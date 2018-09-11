---
title: アサーション (F#)
description: F# プログラミング言語で式をテストするためのデバッグ機能として 'アサート' 式を使用する方法について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 85b1e839bfd19bada48b7f1821d15ddd8fa77754
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44368087"
---
# <a name="assertions"></a>アサーション

`assert`式は、式のテストに使用できるデバッグ機能。 デバッグ モードでエラーが発生すると、アサーションによってシステム エラーのダイアログ ボックスが生成されます。

## <a name="syntax"></a>構文

```fsharp
assert condition
```

## <a name="remarks"></a>Remarks

`assert`式の型`bool -> unit`します。

前の構文で*条件*をテストするブール式を表します。 式が評価された場合`true`実行が影響を受けていないが続行されます。 評価されると、`false`システムのエラー ダイアログ ボックスが生成されます。 エラー ダイアログ ボックスには、文字列を含むキャプション**アサーションが失敗した**します。 ダイアログ ボックスには、アサーション エラーが発生したかを示すスタック トレースが含まれています。

デバッグ モードでコンパイルする場合にのみにアサーション チェックが有効にはつまり場合、定数`DEBUG`が定義されています。 既定で、プロジェクト システムで、`DEBUG`リリース構成ではなく、デバッグ構成で定義される定数。

F# の例外処理を使用してアサーション エラーをキャッチできません。

>[!NOTE]
`assert`関数に解決<xref:System.Diagnostics.Debug.Assert*?displayProperty=nameWithType>します。

## <a name="example"></a>例

次のコード例の使用を示しています、`assert`式。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5401.fs)]

## <a name="see-also"></a>関連項目

- [F# 言語リファレンス](index.md)
