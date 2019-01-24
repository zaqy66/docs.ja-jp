---
title: '&#39;#Region&#39;と&#39;#End Region&#39;ステートメントがメソッド本体や複数行ラムダ内では有効ではありません。'
ms.date: 07/20/2015
f1_keywords:
- bc32025
- vbc32025
helpviewer_keywords:
- BC32025
ms.assetid: 43707bf1-1c6b-4d82-b081-e5a17dca51c1
ms.openlocfilehash: 55399cd123ce4d67cc833f2eabe3230acdafc0bf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54737216"
---
# <a name="39region39-and-39end-region39-statements-are-not-valid-within-method-bodiesmultiline-lambdas"></a>&#39;#Region&#39;と&#39;#End Region&#39;ステートメントがメソッド本体や複数行ラムダ内では有効ではありません。
`#Region`ブロックは、クラス、モジュール、または名前空間レベルで宣言する必要があります。 折りたたみ可能な領域は、1 つ以上のプロシージャを含めることができますが、開始またはプロシージャの内部で終了することはできません。  
  
 **エラー ID:** BC32025  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  前の手順が正しくで終了することを確認、`End Function`または`End Sub`ステートメント。  
  
2.  いることを確認、`#Region`と`#End Region`ディレクティブは、同じコード ブロックにします。  
  
## <a name="see-also"></a>関連項目
- [#Region ディレクティブ](../../../visual-basic/language-reference/directives/region-directive.md)
