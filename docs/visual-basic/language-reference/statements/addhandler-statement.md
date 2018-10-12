---
title: AddHandler ステートメント (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.AddHandlerMethod
- addhandler
- vb.addhandler
helpviewer_keywords:
- AddHandler statement [Visual Basic]
ms.assetid: cfe69799-2a0f-42c0-a99e-09fed954da01
ms.openlocfilehash: f731ff150bd901e325726fca5aa682ff1770f979
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43502951"
---
# <a name="addhandler-statement"></a>AddHandler ステートメント
実行時にイベントをイベント ハンドラーに関連付けます。  
  
## <a name="syntax"></a>構文  
  
```  
AddHandler event, AddressOf eventhandler  
```  
  
## <a name="parts"></a>指定項目  
|||
|---|---|
|event|処理するイベントの名前。|  
|`eventhandler`|イベントを処理するプロシージャの名前。|
|||
  
## <a name="remarks"></a>Remarks  
 `AddHandler`と`RemoveHandler`ステートメントでは、開始およびプログラムの実行中にいつでもイベント処理を停止することができます。  
  
 署名、`eventhandler`プロシージャは、イベントのシグネチャに一致する必要があります`event`します。  
  
 `Handles` キーワードと `AddHandler` ステートメントはどちらも特定のプロシージャで特定のイベントを処理するように指定できますが、両者には違いがあります。 `AddHandler` ステートメントは、実行時にプロシージャをイベントに接続します。 `Handles` キーワードは、プロシージャの定義時に特定のイベントを処理するよう指定する場合に使用します。 詳細については、次を参照してください。[処理](../../../visual-basic/language-reference/statements/handles-clause.md)します。  
  
> [!NOTE]
>  カスタム イベントの場合、`AddHandler`ステートメントで呼び出されるイベントの`AddHandler`アクセサー。 カスタム イベントの詳細については、次を参照してください。 [Event ステートメント](../../../visual-basic/language-reference/statements/event-statement.md)します。  
  
## <a name="example"></a>例  
 [!code-vb[VbVbalrEvents#17](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/addhandler-statement_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [RemoveHandler ステートメント](../../../visual-basic/language-reference/statements/removehandler-statement.md)  
 [Handles](../../../visual-basic/language-reference/statements/handles-clause.md)  
 [Event ステートメント](../../../visual-basic/language-reference/statements/event-statement.md)  
 [イベント](../../../visual-basic/programming-guide/language-features/events/index.md)
