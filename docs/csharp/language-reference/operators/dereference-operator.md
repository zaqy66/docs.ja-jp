---
title: -&gt; 演算子 (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- member access operator (->) [C#]
- -> operator [C#]
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
ms.openlocfilehash: fb95e508ce1339868723bcc3178851e8c1355c1f
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2018
ms.locfileid: "45609527"
---
# <a name="-gt-operator-c-reference"></a>-&gt; 演算子 (C# リファレンス)
`->` 演算子は、ポインターの逆参照とメンバー アクセスを組み合わせます。  
  
## <a name="remarks"></a>コメント  
 次のような形式の式があるとします。  
  
```csharp  
x->y  
```  
  
 ここで、`x` は `T*` 型のポインター、`y` は `T` のメンバーです。この式は次の式と同じです。  
  
```csharp  
(*x).y  
```  
  
 `->` 演算子は、[unsafe](../../../csharp/language-reference/keywords/unsafe.md) とマークされているコードでのみ使用できます。  
  
 `->` 演算子はオーバーロードできません。  
  
## <a name="example"></a>例  
 [!code-csharp[csRefOperators#15](../../../csharp/language-reference/operators/codesnippet/CSharp/dereference-operator_1.cs)]  
  
## <a name="see-also"></a>参照

- [C# リファレンス](../../../csharp/language-reference/index.md)  
- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [C# 演算子](../../../csharp/language-reference/operators/index.md)
