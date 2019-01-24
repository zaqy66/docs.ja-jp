---
title: '方法: 読み取り専用テキスト ボックス (Windows フォーム) を作成します。'
ms.date: 03/30/2017
helpviewer_keywords:
- TextBox control [Windows Forms], read-only
- read-only text boxes
- text boxes [Windows Forms], read-only
ms.assetid: 60baa9ab-fa57-44ad-bb7c-61b05aa64296
ms.openlocfilehash: 89d331f6c7fad5880aff031eb808199292e493a6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54670343"
---
# <a name="how-to-create-a-read-only-text-box-windows-forms"></a>方法: 読み取り専用テキスト ボックス (Windows フォーム) を作成します。
編集可能な Windows フォームのテキスト ボックスは読み取り専用のコントロールに変換できます。 たとえば、テキスト ボックスが通常は編集ができない可能性があります現時点では、アプリケーションの状態が原因値を表示する可能性があります。  
  
### <a name="to-create-a-read-only-text-box"></a>読み取り専用テキスト ボックスを作成するには  
  
1.  設定、<xref:System.Windows.Forms.TextBox>コントロールの<xref:System.Windows.Forms.TextBoxBase.ReadOnly%2A>プロパティを`true`します。 プロパティを設定して`true`ユーザーがまだスクロールやテキスト ボックス内のテキストを強調表示、変更を許可しません。 A**コピー**コマンドは、テキスト ボックスでは、機能ですが**切り取り**と**貼り付け**のコマンドはできません。  
  
    > [!NOTE]
    >  <xref:System.Windows.Forms.TextBoxBase.ReadOnly%2A>プロパティでは、実行時にユーザーとの対話のみに影響します。 まだ変更テキスト ボックスの内容プログラムで実行時に変更することで、<xref:System.Windows.Forms.TextBox.Text%2A>テキスト ボックスのプロパティ。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.TextBox>
- [TextBox コントロールの概要](../../../../docs/framework/winforms/controls/textbox-control-overview-windows-forms.md)
- [方法: Windows フォーム TextBox コントロールでのカーソル位置を制御します。](../../../../docs/framework/winforms/controls/how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)
- [方法: Windows フォーム TextBox コントロールでパスワード テキスト ボックスを作成します。](../../../../docs/framework/winforms/controls/how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)
- [方法: 文字列に引用符を挿入します。](../../../../docs/framework/winforms/controls/how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [方法: Windows フォームの TextBox コントロールでテキストを選択します。](../../../../docs/framework/winforms/controls/how-to-select-text-in-the-windows-forms-textbox-control.md)
- [方法: Windows フォームの TextBox コントロールで複数の行を表示します。](../../../../docs/framework/winforms/controls/how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)
- [TextBox コントロール](../../../../docs/framework/winforms/controls/textbox-control-windows-forms.md)
