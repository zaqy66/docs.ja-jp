---
title: '方法: Windows フォームの RichTextBox コントロールにおける属性の変更を書式設定するかを判断します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], text boxes
- RichTextBox control [Windows Forms], determining font changes
- text boxes [Windows Forms], determining font changes
- SelChange event
ms.assetid: bdfed015-f77a-41e5-b38f-f8629b2fa166
ms.openlocfilehash: e746cd1d0f9f7d9850d0263ee6ed0a82472fcb5e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504151"
---
# <a name="how-to-determine-when-formatting-attributes-change-in-the-windows-forms-richtextbox-control"></a>方法: Windows フォームの RichTextBox コントロールにおける属性の変更を書式設定するかを判断します。
Windows フォームの一般的な用途<xref:System.Windows.Forms.RichTextBox>コントロールがフォントのオプションや段落スタイルなどの属性を持つテキストを書式設定します。 アプリケーションは、多くのワード プロセッシング アプリケーションと同様に、ツールバーを表示できるように書式設定文字列のすべての変更を追跡する必要があります。  
  
### <a name="to-respond-to-changes-in-formatting-attributes"></a>属性の書式設定の変更に応答するには  
  
1.  コードを記述、<xref:System.Windows.Forms.RichTextBox.SelectionChanged>属性の値に応じて適切なアクションを実行するイベント ハンドラー。 次の例の値に応じて、ツール バー ボタンの外観を変更する、<xref:System.Windows.Forms.RichTextBox.SelectionBullet%2A>プロパティ。 ツール バー ボタンは、コントロールのカーソルが移動したときにのみ更新されます。  
  
     次の例でフォームを前提としています、<xref:System.Windows.Forms.RichTextBox>コントロールと<xref:System.Windows.Forms.ToolBar>ツール バー ボタンを格納しているコントロール。 ツールバーとツールバー ボタンの詳細については、次を参照してください。[方法。ツール バー コントロールにボタンを追加](../../../../docs/framework/winforms/controls/how-to-add-buttons-to-a-toolbar-control.md)します。  
  
    ```vb  
    ' The following code assumes the existence of a toolbar control  
    ' with at least one toolbar button.  
    Private Sub RichTextBox1_SelectionChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles RichTextBox1.SelectionChanged  
       If RichTextBox1.SelectionBullet = True Then  
          ' Bullet button on toolbar should appear pressed  
          ToolBarButton1.Pushed = True  
       Else  
           ' Bullet button on toolbar should appear unpressed  
           ToolBarButton1.Pushed = False  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    // The following code assumes the existence of a toolbar control  
    // with at least one toolbar button.  
    private void richTextBox1_SelectionChanged(object sender,  
    System.EventArgs e)  
    {  
       if (richTextBox1.SelectionBullet == true)   
       {  
          // Bullet button on toolbar should appear pressed  
          toolBarButton1.Pushed = true;  
       }  
       else   
       {  
          // Bullet button on toolbar should appear unpressed  
          toolBarButton1.Pushed = false;  
       }  
    }  
    ```  
  
    ```cpp  
    // The following code assumes the existence of a toolbar control  
    // with at least one toolbar button.  
    private:  
       System::Void richTextBox1_SelectionChanged(  
          System::Object ^  sender, System::EventArgs ^  e)  
       {  
          if (richTextBox1->SelectionBullet == true)  
          {  
             // Bullet button on toolbar should appear pressed  
             toolBarButton1->Pushed = true;  
          }  
          else  
          {  
             // Bullet button on toolbar should appear unpressed  
             toolBarButton1->Pushed = false;  
          }  
       }  
    ```  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.RichTextBox.SelectionChanged>
- <xref:System.Windows.Forms.RichTextBox>
- [RichTextBox コントロール](../../../../docs/framework/winforms/controls/richtextbox-control-windows-forms.md)
- [Windows フォームで使用するコントロール](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)
