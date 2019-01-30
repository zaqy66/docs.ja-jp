---
title: "'#Region' および ' #End Region' ステートメントはメソッド本体や複数行ラムダ内では有効ではありません。"
ms.date: 07/20/2015
f1_keywords:
- bc32025
- vbc32025
helpviewer_keywords:
- BC32025
ms.assetid: 43707bf1-1c6b-4d82-b081-e5a17dca51c1
ms.openlocfilehash: 2a2f5692518c6784dfc6e3be6302f1e8dcf2aaa7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55265572"
---
# <a name="region-and-end-region-statements-are-not-valid-within-method-bodiesmultiline-lambdas"></a>'#Region' および '#End Region' ステートメントは、メソッド本体や複数行ラムダの内部では有効ではありません。
`#Region`ブロックは、クラス、モジュール、または名前空間レベルで宣言する必要があります。 折りたたみ可能な領域は、1 つ以上のプロシージャを含めることができますが、開始またはプロシージャの内部で終了することはできません。  
  
 **エラー ID:** BC32025  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  前の手順が正しくで終了することを確認、`End Function`または`End Sub`ステートメント。  
  
2.  いることを確認、`#Region`と`#End Region`ディレクティブは、同じコード ブロックにします。  
  
## <a name="see-also"></a>関連項目
- [#Region ディレクティブ](../../../visual-basic/language-reference/directives/region-directive.md)
