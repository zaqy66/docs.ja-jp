---
title: 初期化子が必要です
ms.date: 07/20/2015
f1_keywords:
- vbc30996
- bc30996
helpviewer_keywords:
- BC30996
ms.assetid: 6e183fe0-8888-43ed-a062-01571079455f
ms.openlocfilehash: 1fa66a3c50b5c1eadd4c63b92c57ab60e1a11076
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54595995"
---
# <a name="initializer-expected"></a>初期化子が必要です
初期化リストの空の場合、次の例に示すように、オブジェクト初期化子を使用して、クラスのインスタンスを宣言しようとしました。  
  
 `' Not valid.`  
  
 `' Dim aStudent As New Student With {}`  
  
 次の例に示すように、少なくとも 1 つのフィールドまたはプロパティが、初期化子リストで初期化する必要があります。  
  
 `Dim aStudent As New Student With {.year = "Senior"}`  
  
 **エラー ID:** BC30996  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  少なくとも 1 つのフィールドまたはプロパティで、初期化子を初期化または、オブジェクト初期化子を使用しないでください。  
  
## <a name="see-also"></a>関連項目
- [オブジェクト初期化子:名前付きの匿名型](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md)
- [方法: オブジェクト初期化子を使用してオブジェクトを宣言します。](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-declare-an-object-by-using-an-object-initializer.md)
