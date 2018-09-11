---
title: 型略称 (F#)
description: コードを読みやすくためにわかりやすい名前の型を提供する f# 型略称について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 259cd6c84e22fc7c98e08255d3e0ded5b87af352
ms.sourcegitcommit: 67de6cb5dd66a19f2180ba7e4d7aecc697f8a963
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/10/2018
ms.locfileid: "44336473"
---
# <a name="type-abbreviations"></a>型略称

A*型略称*エイリアスまたは代替名の種類。

## <a name="syntax"></a>構文

```fsharp
type [accessibility-modifier] type-abbreviation = type-name
```

## <a name="remarks"></a>Remarks

型の省略形を使用すると、コードを読みやすくために、型、わかりやすい名前を指定します。 書き込みに面倒なタイプの使いやすい名を作成するのにことも使用できます。さらに、型の省略形を使用すると、型を使用するすべてのコードを変更することがなく、基になる型を変更しやすきます。 単純な型の省略形を次に示します。

既定値の型の省略形のアクセシビリティ`public`します。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2301.fs)]

型の省略形は、次のコードのように、ジェネリック パラメーターを含めることができます。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2302.fs)]

上記のコードで`Transform`を任意の型の 1 つの引数を受け取る関数を表す型の省略形は、同じ型の 1 つの値を返します。

型の省略形は、.NET Framework の MSIL コードでは保持されません。 したがって、f# アセンブリ .NET Framework の別の言語からを使用する場合は、型の省略形の基になる種類の名前を使用する必要があります。

型の省略形は、測定単位にも使用できます。 詳細については、次を参照してください。[単位](units-of-measure.md)します。

## <a name="see-also"></a>関連項目

- [F# 言語リファレンス](index.md)
