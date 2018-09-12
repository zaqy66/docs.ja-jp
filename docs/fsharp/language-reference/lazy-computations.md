---
title: 遅延計算 (F#)
description: F# 遅延計算が、アプリとライブラリのパフォーマンスを向上する方法について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 8afe815f26978de96291a52973d54a9dbcc5eaf2
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44508427"
---
# <a name="lazy-computations"></a>遅延計算

*遅延計算*は計算には、すぐに評価されませんが、結果が必要なときに代わりに評価されます。 これは、コードのパフォーマンスを向上させるために役立ちます。

## <a name="syntax"></a>構文

```fsharp
let identifier = lazy ( expression )
```

## <a name="remarks"></a>Remarks

前の構文で*式*結果が、必要な場合にのみ評価されるコードと*識別子*は結果を格納する値です。 型の値は、 [ `Lazy<'T>`](https://msdn.microsoft.com/library/b29d0af5-6efb-4a55-a278-2662a4ecc489)場所、実際の種類のために使用`'T`式の結果から決定されます。

遅延計算を使用すると、結果が必要な場合のみ、計算の実行を制限することでパフォーマンスを向上させることができます。

メソッドを呼び出すを強制的に実行する計算、`Force`します。 `Force` 1 回だけ実行する実行をします。 後続の呼び出し`Force`同じが、任意のコードを実行せずに返します。

遅延計算の使用と、使用して、次のコードを示しています`Force`します。 このコードの種類で`result`は`Lazy<int>`、および`Force`メソッドを返します。、`int`します。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet73011.fs)]

遅延評価は、ではなく、`Lazy`入力、シーケンスにも使用します。 詳細については、次を参照してください。[シーケンス](sequences.md)します。

## <a name="see-also"></a>関連項目

- [F# 言語リファレンス](index.md)
- [LazyExtensions モジュール](https://msdn.microsoft.com/library/86671f40-84a0-402a-867d-ae596218d948)
