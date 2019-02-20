---
title: ユーザーの入力の処理
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], user input using code
- custom controls [Windows Forms], keyboard events using code
- custom controls [Windows Forms], mouse events using code
ms.assetid: d9b12787-86f6-4022-8e0f-e12d312c4af2
ms.openlocfilehash: 8c6319929d4b419cc0a2e1cfd097bfae7d997120
ms.sourcegitcommit: acd8ed14fe94e9d4e3a7fb685fe83d05e941073c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/20/2019
ms.locfileid: "56443006"
---
# <a name="handling-user-input"></a>ユーザーの入力の処理
このトピックでは、によって提供されるメインのキーボードとマウスのイベントを説明します。<xref:System.Windows.Forms.Control?displayProperty=nameWithType>します。 イベントを処理するときに、コントロール作成者はイベントにデリゲートを結び付けるのではなく、保護された `On`*EventName* メソッドをオーバーライドする必要があります。 イベントのレビューについては、「[コンポーネントからのイベントの生成](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120))」を参照してください。  
  
> [!NOTE]
>  イベント、基底クラスのインスタンスに関連付けられているデータがないかどうかは<xref:System.EventArgs>への引数として渡される、 `On` *EventName*メソッド。  
  
## <a name="keyboard-events"></a>キーボード イベント  
 コントロールで処理できる一般的なキーボード イベントは<xref:System.Windows.Forms.Control.KeyDown>、 <xref:System.Windows.Forms.Control.KeyPress>、および<xref:System.Windows.Forms.Control.KeyUp>します。  
  
|イベント名|オーバーライドするメソッド|イベントの説明|  
|----------------|------------------------|--------------------------|  
|`KeyDown`|`void OnKeyDown(KeyEventArgs)`|キーが最初に押されたときにのみ発生します。|  
|`KeyPress`|`void OnKeyPress`<br /><br /> `(KeyPressEventArgs)`|キーが押されるたびに発生します。 キーを押した場合、<xref:System.Windows.Forms.Control.KeyPress>オペレーティング システムで定義されたリピート間隔でイベントが発生します。|  
|`KeyUp`|`void OnKeyUp(KeyEventArgs)`|キーが離されたときに発生します。|  
  
> [!NOTE]
>  キーボード入力の処理は、前の表のイベントをオーバーライドするよりもかなり複雑であり、このトピックでは触れていません。 詳細については、「 [Windows フォームでのユーザー入力](../../../../docs/framework/winforms/user-input-in-windows-forms.md)」を参照してください。  
  
## <a name="mouse-events"></a>マウス イベント  
 コントロールで処理できるマウス イベントは<xref:System.Windows.Forms.Control.MouseDown>、 <xref:System.Windows.Forms.Control.MouseEnter>、 <xref:System.Windows.Forms.Control.MouseHover>、 <xref:System.Windows.Forms.Control.MouseLeave>、 <xref:System.Windows.Forms.Control.MouseMove>、および<xref:System.Windows.Forms.Control.MouseUp>します。  
  
|イベント名|オーバーライドするメソッド|イベントの説明|  
|----------------|------------------------|--------------------------|  
|`MouseDown`|`void OnMouseDown(MouseEventArgs)`|ポインターがコントロール上にある状態でマウス ボタンが押されると発生します。|  
|`MouseEnter`|`void OnMouseEnter(EventArgs)`|ポインターがコントロールの領域に初めて入ったときに発生します。|  
|`MouseHover`|`void OnMouseHover(EventArgs)`|ポインターがコントロールの上に置かれたときに発生します。|  
|`MouseLeave`|`void OnMouseLeave(EventArgs)`|ポインターがコントロールの領域から離れると発生します。|  
|`MouseMove`|`void OnMouseMove(MouseEventArgs)`|ポインターがコントロールの領域内で移動すると発生します。|  
|`MouseUp`|`void OnMouseUp(MouseEventArgs)`|ポインターがコントロールの上にある状態でマウス ボタンが離されるか、ポインターがコントロールの領域から離れると発生します。|  
  
 次のコード フラグメントは、オーバーライドする例を示しています、<xref:System.Windows.Forms.Control.MouseDown>イベント。  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#7](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#7)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#7](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#7)]  
  
 次のコード フラグメントは、オーバーライドする例を示しています、<xref:System.Windows.Forms.Control.MouseMove>イベント。  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#8](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#8)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#8](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#8)]  
  
 次のコード フラグメントは、オーバーライドする例を示しています、<xref:System.Windows.Forms.Control.MouseUp>イベント。  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#9](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#9)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#9](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#9)]  
  
 完全なソース コード、`FlashTrackBar`サンプルを参照してください[方法。進行状況を示す Windows フォーム コントロールを作成する](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md)します。  
  
## <a name="see-also"></a>関連項目
- [Windows フォーム コントロールのイベント](../../../../docs/framework/winforms/controls/events-in-windows-forms-controls.md)
- [イベントの定義](../../../../docs/framework/winforms/controls/defining-an-event-in-windows-forms-controls.md)
- [イベント](../../../../docs/standard/events/index.md)
- [Windows フォームでのユーザー入力](../../../../docs/framework/winforms/user-input-in-windows-forms.md)
