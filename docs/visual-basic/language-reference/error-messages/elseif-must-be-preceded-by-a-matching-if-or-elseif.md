---
title: "'#ElseIf' の前には、対応する '#If' または '#ElseIf' が必要です'"
ms.date: 07/20/2015
f1_keywords:
- vbc30014
- bc30014
helpviewer_keywords:
- BC30014
ms.assetid: 5215585e-2efa-485a-9efe-9833a1cc83a0
ms.openlocfilehash: 1e63595ee573e9356f6870a02b2131897c725baf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505784"
---
# <a name="39elseif39-must-be-preceded-by-a-matching-39if39-or-39elseif39"></a>'#ElseIf' の前には、対応する '#If' または '#ElseIf' が必要です'
`#ElseIf` は条件付きコンパイル ディレクティブです。 `#ElseIf`句の前に、対応する`#If`または`#ElseIf`句が必要です。  
  
 **エラー ID:** BC30014  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  いることを確認前に、`#If`または`#ElseIf`これからは分離されていないが`#ElseIf`によって、中間の条件付きコンパイル ブロックや、間違って配置された`#End If`します。  
  
2.  場合、`#ElseIf`が付いて、`#Else`ディレクティブを削除するか、`#Else`に変更を`#ElseIf`します。  
  
3.  他のすべての順序が正しい場合、 `#If` ディレクティブを条件付きコンパイル ブロックの先頭に追加します。  
  
## <a name="see-also"></a>関連項目
- [#If...Then...#Else ディレクティブ](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
