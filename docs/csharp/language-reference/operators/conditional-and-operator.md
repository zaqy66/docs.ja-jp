---
title: '&amp;&amp; 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '&&_CSharpKeyword'
helpviewer_keywords:
- '&& operator [C#]'
- logical AND operator [C#]
ms.assetid: 2e4f0a1c-92a3-40f8-8e3b-17b607f20c31
ms.openlocfilehash: 459b791fde3e4d3940dbd3d916f940e81f365da6
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43529236"
---
# <a name="ampamp-operator-c-reference"></a>&amp;&amp; 演算子 (C# リファレンス)
条件 AND 演算子 (`&&`) では `bool` オペランドの論理 AND が実行されますが、2 番目のオペランドは必要な場合にのみ評価されます。  
  
## <a name="remarks"></a>コメント  
 次の演算は、  
  
```csharp  
x && y  
```  
  
 次の演算に対応しています。  
  
```csharp  
x & y  
```  
  
 ただし `x` が `false` の場合は、AND 演算の結果は `y` の値に関係なく `false` となるため、`y` は評価されません。 これは、"ショートサーキット" 評価と呼ばれます。  
  
 条件 AND 演算子はオーバーロードできませんが、通常の論理演算子、[true](../../../csharp/language-reference/keywords/true.md) 演算子、[false](../../../csharp/language-reference/keywords/false.md) 演算子のオーバーロードは、条件論理演算子の制約付きのオーバーロードとも見なされます。  
  
## <a name="example"></a>例  
 次の例では、2 番目の `if` ステートメントの条件式で最初のオペランドのみが評価されます。これは、このオペランドが `false` を返すからです。  
  
 [!code-csharp[csRefOperators#48](../../../csharp/language-reference/operators/codesnippet/CSharp/conditional-and-operator_1.cs)]  
  
## <a name="c-language-specification"></a>C# 言語仕様  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>参照

- [C# リファレンス](../../../csharp/language-reference/index.md)  
- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [C# 演算子](../../../csharp/language-reference/operators/index.md)
