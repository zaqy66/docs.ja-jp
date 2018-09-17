---
title: ++ 演算子 (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- ++_CSharpKeyword
helpviewer_keywords:
- increment operator (++) [C#]
- ++ operator [C#]
ms.assetid: e9dec353-070b-44fb-98ed-eb8fdf753feb
ms.openlocfilehash: a52f614ce1bbfb8e9d9be686b277c1e69f6f9d35
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45593102"
---
# <a name="-operator-c-reference"></a>++ 演算子 (C# リファレンス)
インクリメント演算子 (`++`) は、オペランドを 1 ずつインクリメントします。 インクリメント演算子はそのオペランド ( `++variable` および `variable++`) の前後に指定できます。  
  
## <a name="remarks"></a>コメント  
 1 番目の形式は前置インクリメント演算です この演算の結果は、インクリメント後のオペランドの値になります。  
  
 2 番目の形式は後置インクリメント演算です。 この演算の結果は、インクリメント前のオペランドの値になります。  
  
 数値型と列挙型には事前定義のインクリメント演算子があります。 ユーザー定義型は `++` 演算子をオーバーロードできます。 整数型に対する演算は、通常、列挙型で使用できます。  
  
## <a name="example"></a>例  
 [!code-csharp[csRefOperators#3](../../../csharp/language-reference/operators/codesnippet/CSharp/increment-operator_1.cs)]  
  
## <a name="see-also"></a>参照

- [C# リファレンス](../../../csharp/language-reference/index.md)  
- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [C# 演算子](../../../csharp/language-reference/operators/index.md)
