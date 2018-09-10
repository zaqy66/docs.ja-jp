---
title: '&amp;= 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '&=_CSharpKeyword'
helpviewer_keywords:
- AND assignment operator (&=) [C#]
- '&= operator [C#]'
ms.assetid: e8d58f3f-72dd-4b5a-b995-452fcce7e6bb
ms.openlocfilehash: f3a6fe20ca89a90b5a64118d73fb39e9a364d1e9
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43506402"
---
# <a name="amp-operator-c-reference"></a>&amp;= 演算子 (C# リファレンス)
AND 代入演算子です。  
  
## <a name="remarks"></a>コメント  
 次のような `&=` 代入演算子を使用する式があるとします  
  
```csharp  
x &= y  
```  
  
 上記の式は、次の式と同じです。  
  
```csharp  
x = x & y  
```  
  
 ただし、`x` が評価されるのは 1 回だけです。 [& 演算子](../../../csharp/language-reference/operators/and-operator.md)では、整数のオペランドではビットごとの論理 AND 演算、`bool` オペランドでは論理 AND 演算が実行されます。  
  
 `&=` 演算子は直接オーバーロードできませんが、[& 演算子](../../../csharp/language-reference/operators/and-operator.md)はユーザー定義型でオーバーロードできます (「[operator](../../../csharp/language-reference/keywords/operator.md)」を参照)。  
  
## <a name="example"></a>例  
 [!code-csharp[csRefOperators#34](../../../csharp/language-reference/operators/codesnippet/CSharp/and-assignment-operator_1.cs)]  
  
## <a name="see-also"></a>参照

- [C# リファレンス](../../../csharp/language-reference/index.md)  
- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [C# 演算子](../../../csharp/language-reference/operators/index.md)
