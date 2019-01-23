---
title: 先頭&#39;します。&#39;または&#39;!&#39;内でのみ表示できます、&#39;で&#39;ステートメント
ms.date: 07/20/2015
f1_keywords:
- vbc30157
- bc30157
helpviewer_keywords:
- BC30157
ms.assetid: 70daaee1-14f9-45b7-9f30-53794310b95e
ms.openlocfilehash: e64318d4ececbd887f55a1a202cc2d58c90c8fc7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54625953"
---
# <a name="leading-3939-or-3939-can-only-appear-inside-a-39with39-statement"></a>先頭&#39;します。&#39;または&#39;!&#39;内でのみ表示できます、&#39;で&#39;ステートメント
ピリオド (.) または感嘆符 (!) でない内部、`With`左の式がブロックされます。 メンバー アクセス (`.`) およびディクショナリ メンバー アクセス (`!`) メンバーを含む要素を指定する式が必要です。 これは、アクセサーのまたはのターゲットとしての左側にすぐに表示する必要があります、`With`メンバー アクセスを含むブロックします。  
  
 **エラー ID:** BC30157  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  いることを確認、`With`ブロックが正しく書式設定します。  
  
2.  存在する場合ありません`With`ブロック、メンバーを含む定義の要素に評価されるアクセサーの左側に式を追加します。  
  
## <a name="see-also"></a>関連項目
- [コード内の特殊文字](../../../visual-basic/programming-guide/program-structure/special-characters-in-code.md)
- [With...End With ステートメント](../../../visual-basic/language-reference/statements/with-end-with-statement.md)
