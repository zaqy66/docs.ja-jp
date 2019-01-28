---
title: '方法: 構造体間にユーザー定義の変換を実装する - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- user-defined conversions [C#]
ms.assetid: 97839aef-8fbc-40d5-9769-6b569bc2710b
ms.openlocfilehash: 4b38271c1aaf582c8c58b7198765b679cdfe4881
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499565"
---
# <a name="how-to-implement-user-defined-conversions-between-structs-c-programming-guide"></a>方法: 構造体間にユーザー定義の変換を実装する (C# プログラミング ガイド)
この例では `RomanNumeral` および `BinaryNumeral` という 2 つの構造体を定義し、それらの間の変換を示します。  
  
## <a name="example"></a>例  
 [!code-csharp[csProgGuideStatements#13](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-implement-user-defined-conversions-between-structs_1.cs)]  
  
## <a name="robust-programming"></a>信頼性の高いプログラミング  
  
-   前述の例では、次のようなステートメントがあります。  
  
     [!code-csharp[csProgGuideStatements#14](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-implement-user-defined-conversions-between-structs_2.cs)]  
  
     このステートメントでは `RomanNumeral` から `BinaryNumeral` への変換を実行します。 `RomanNumeral` から `BinaryNumeral` への直接変換はないため、`RomanNumeral` から `int` へ変換するためのキャストと、`int` から `BinaryNumeral` へ変換するためのキャストが使用されています。  
  
-   次のようなステートメントもあります。  
  
     [!code-csharp[csProgGuideStatements#15](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-implement-user-defined-conversions-between-structs_3.cs)]  
  
     このステートメントでは `BinaryNumeral` から `RomanNumeral` への変換を実行します。 `RomanNumeral` は `BinaryNumeral` からの暗黙の型変換を定義しているため、キャストは不要です。  
  
## <a name="see-also"></a>関連項目

- [C# リファレンス](../../../csharp/language-reference/index.md)
- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)
- [変換演算子](../../../csharp/programming-guide/statements-expressions-operators/conversion-operators.md)
