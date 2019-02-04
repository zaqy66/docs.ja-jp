---
title: "	'#Else' の前には、対応する '#If' または '#ElseIf' が必要です。"
ms.date: 07/20/2015
f1_keywords:
- vbc30014
- bc30014
helpviewer_keywords:
- BC30014
ms.assetid: 5215585e-2efa-485a-9efe-9833a1cc83a0
ms.openlocfilehash: d6fa76b2aba45e3455cef6ceafc0f737ef56225d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271552"
---
# <a name="elseif-must-be-preceded-by-a-matching-if-or-elseif"></a>	'#Else' の前には、対応する '#If' または '#ElseIf' が必要です。
`#ElseIf` は条件付きコンパイル ディレクティブです。 `#ElseIf`句の前に、対応する`#If`または`#ElseIf`句が必要です。  
  
 **エラー ID:** BC30014  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  先行する`#If`または`#ElseIf`と、この`#ElseIf`とが、間に条件付きコンパイル ブロックを挿入することによって分離されていないこと、また
は`#End If`句を間違った場所に記述したために分離されていないことを確認します。  
  
2.  `#ElseIf`の前に`#Else`ディレクティブがある場合は、その`#Else`を削除するか、`#ElseIf`に変更します。  
  
3.  すべて問題ない場合は、条件付きコンパイル ブロックの先頭に `#If` ディレクティブを追加します。  
  
## <a name="see-also"></a>関連項目
- [#If...Then...#Else ディレクティブ](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
