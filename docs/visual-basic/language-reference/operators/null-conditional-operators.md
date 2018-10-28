---
title: Null 条件演算子 (Visual Basic)
ms.date: 10/19/2018
helpviewer_keywords:
- null-conditional operators [Visual Basic]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.openlocfilehash: c29362a1e335e18b66821919e266b1ce57774692
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50195993"
---
# <a name="-and--null-conditional-operators-visual-basic"></a>?. そして。() null 条件演算子 (Visual Basic)

Null の左側のオペランドの値をテスト (`Nothing`) メンバー アクセスを実行する前に (`?.`) またはインデックス (`?()`); の操作を返します。`Nothing`に左側のオペランドが評価された場合`Nothing`します。 値の型を返すことが通常は、式の null 条件演算子を返すことに注意してください、<xref:System.Nullable%601>します。

これらの演算子を使用して、データ構造を下って場合は特に、null のチェックを処理するには、少ないコードを記述するのに役立ちます。 例えば:

```vb
Dim length As Integer? = customers?.Length  ' Nothing if customers is Nothing  
Dim first As Customer = customers?(0)  ' Nothing if customers is Nothing  
Dim count As Integer? = customers?(0)?.Orders?.Count()  ' Nothing if customers, the first customer, or Orders is Nothing  
```

比較については、null 条件演算子を使用せず、これらの式の最初の代替のコードは次のとおりです。

```vb
Dim length As Integer
If customers IsNot Nothing Then
   length = customers.Length
End If
```

Null 条件演算子はショートサーキットです。  条件付きメンバー アクセスおよびインデックス操作のチェーン内の 1 つの操作は、何も返された場合、チェーンの実行の残りの部分を停止します。  C(E) は次の例の場合は評価されません`A`、 `B`、または`C`Nothing に評価されます。

```vb
A?.B?.C?(E);
```

Null 条件メンバー アクセスの別の用途では、はるかに少ないコードでスレッド セーフな方法でデリゲートを呼び出します。  従来の方法には、次のようなコードが必要です。  

```vb  
Dim handler = AddressOf(Me.PropertyChanged)  
If handler IsNot Nothing  
    Call handler(…)  
```

新しい方法は格段に単純です。  

```vb
PropertyChanged?.Invoke(…)
```

コンパイラが `PropertyChanged` を評価するためのコードを一度しか生成せず、一時変数に結果が保持されるため、新しい方法はスレッド セーフです。 null 条件デリゲート呼び出し構文 `PropertyChanged?(e)` がないため、`Invoke` メソッドを明示的に呼び出す必要があります。  

## <a name="see-also"></a>関連項目

- [演算子 (Visual Basic)](index.md)
- [Visual Basic プログラミング ガイド](../../../visual-basic/programming-guide/index.md)
- [Visual Basic の言語リファレンス](../../../visual-basic/language-reference/index.md)  
