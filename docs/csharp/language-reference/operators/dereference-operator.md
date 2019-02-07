---
title: -> 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- member access operator (->) [C#]
- -> operator [C#]
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
ms.openlocfilehash: be74f02a85aa05cdab32768ed38222fc4d9289b1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255368"
---
# <a name="--operator-c-reference"></a>-> 演算子 (C# リファレンス)

ポインター メンバー アクセス演算子 `->` は、ポインターの間接アクセスとメンバー アクセスを結合したものです。

`x`が型 `T*` のポインターであり、`y` が `T` のアクセス可能なメンバーである場合、フォームの式

```csharp
x->y
```

上記の式は、次の式と同じです。

```csharp
(*x).y
```

`->` 演算子には [unsafe](../keywords/unsafe.md) コンテキストが必要です。

詳細については、「[方法 : ポインターを使用してメンバーにアクセスする](../../programming-guide/unsafe-code-pointers/how-to-access-a-member-with-a-pointer.md)」を参照してください。

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

`->` 演算子はオーバーロードできません。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、「[C# 言語仕様](../language-specification/index.md)」の「[ポインターのメンバー アクセス](~/_csharplang/spec/unsafe-code.md#pointer-member-access)」を参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
- [ポインター型](../../programming-guide/unsafe-code-pointers/pointer-types.md)
