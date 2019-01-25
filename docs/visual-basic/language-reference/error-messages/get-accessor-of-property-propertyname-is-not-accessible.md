---
title: '&#39;取得&#39;プロパティのアクセサー &#39; &lt;propertyname&gt; &#39;にアクセスできません'
ms.date: 07/20/2015
f1_keywords:
- vbc31103
- bc31103
helpviewer_keywords:
- BC31103
ms.assetid: 3c346c32-7669-4b04-841d-7a9df9cb703e
ms.openlocfilehash: 10b7168ac40ca7c7d696cd63cd823454f404bb94
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54582215"
---
# <a name="39get39-accessor-of-property-39ltpropertynamegt39-is-not-accessible"></a>&#39;取得&#39;プロパティのアクセサー &#39; &lt;propertyname&gt; &#39;にアクセスできません
ステートメントが、プロパティへのアクセスがあるない場合は、プロパティの値を取得しようとしています。`Get`プロシージャ。  
  
 場合、 [Get ステートメント](../../../visual-basic/language-reference/statements/get-statement.md)レベルよりもより制限の厳しいアクセスでマークされたその[Property ステートメント](../../../visual-basic/language-reference/statements/property-statement.md)プロパティの値を読み取ろうとしてが失敗する、次の場合。  
  
-   `Get`ステートメントがマークされている[プライベート](../../../visual-basic/language-reference/modifiers/private.md)呼び出し元のコードとそれには、クラスまたは構造体のプロパティが定義されているとします。  
  
-   `Get`ステートメントがマークされている[Protected](../../../visual-basic/language-reference/modifiers/protected.md)呼び出し元のコードは、クラスまたはプロパティが定義されている構造体ではなく、派生クラスでも。  
  
-   `Get`ステートメントがマークされている[フレンド](../../../visual-basic/language-reference/modifiers/friend.md)プロパティが定義されている同じアセンブリに呼び出し元のコードがないとします。  
  
 **エラー ID:** BC31103  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   コントロールのプロパティを定義するソース コードを使っている場合を宣言することを検討してください、`Get`プロパティ自体と同じアクセス レベルを持つプロシージャ。  
  
-   場合は、プロパティを定義するソース コードがないか、または制限する必要があります、`Get`プロパティ自体へのアクセス性のあるコードの領域にプロパティ値を読み取るステートメントに移動しようとする複数のプロシージャ アクセス レベル、プロパティ。  
  
## <a name="see-also"></a>関連項目
- [Property プロシージャ](../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)
- [方法: 混合アクセス レベルを持つプロパティを宣言します。](../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-a-property-with-mixed-access-levels.md)
