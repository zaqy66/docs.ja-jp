---
title: ループ コントロール変数として宣言された配列を初期サイズで宣言することはできません
ms.date: 07/20/2015
f1_keywords:
- vbc32039
- bc32039
helpviewer_keywords:
- BC32039
ms.assetid: 1d8b6560-c9eb-4b71-a038-24c6f5a5ce46
ms.openlocfilehash: d8fe794adcc1c2d28437bac7e732f99a6b6c07c0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54518619"
---
# <a name="array-declared-as-for-loop-control-variable-cannot-be-declared-with-an-initial-size"></a>ループ コントロール変数として宣言された配列を初期サイズで宣言することはできません
A`For Each`ループとして配列を使用してその*要素*繰り返し変数は、その配列を初期化します。  
  
 次のステートメントでは、このエラーの生成方法を示しています。  
  
```  
Dim arrayList As New List(Of Integer())  
For Each listElement() As Integer In arrayList  
For Each listElement(1) As Integer In arrayList  
```  
  
 最初の`For Each`ステートメントの要素にアクセスする正しい方法は、`arrayList`します。 2 番目の`For Each`ステートメントには、このエラーが生成されます。  
  
 **エラー ID:** BC32039  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   宣言から初期化を削除、*要素*繰り返し変数。  
  
## <a name="see-also"></a>関連項目
- [For...Next ステートメント](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [配列](../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [コレクション](../../../standard/collections/index.md)
