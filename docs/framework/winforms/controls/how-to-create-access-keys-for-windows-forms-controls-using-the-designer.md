---
title: '方法: デザイナーを使用して Windows フォーム コントロールのアクセス キーを作成します。'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], access keys
- Button control [Windows Forms], access keys
- dialog box controls [Windows Forms], mnemonics
- access keys [Windows Forms], creating for controls
- mnemonics [Windows Forms], adding to dialog box controls
- ampersand character in shortcut key
- Windows Forms controls, access keys
- examples [Windows Forms], controls
- Text property [Windows Forms], specifying access keys for controls
- keyboard shortcuts [Windows Forms], creating for controls
- access keys [Windows Forms], Windows Forms
- ALT key
ms.assetid: 4c374c4c-4ca9-4a68-ac96-9dc3ab0f518a
ms.openlocfilehash: e9524449b457fc276678ecaadd1d137e7280156a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54527472"
---
# <a name="how-to-create-access-keys-for-windows-forms-controls-using-the-designer"></a>方法: デザイナーを使用して Windows フォーム コントロールのアクセス キーを作成します。
*アクセス キー*がメニューやメニュー項目では、ボタンなどのコントロールのラベルのテキストに下線付きの文字。 組み合わせて定義済みのアクセス キーを持つ、ALT キーを押してボタンを「クリックして」にユーザーができるようにします。 たとえば、フォームを印刷する手順を実行するボタンとその`Text`プロパティを設定すると、実行時のボタン テキストに下線付きで表示するには、"P"を"P"により、文字の文字の前に「印刷、」アンパサンドを追加する (&)。 ユーザーには、ALT キーを押しながら P キーを押して、ボタンに関連付けられているコマンドを実行できます。 フォーカスを受け取ることはできませんが、コントロールのアクセス キーを持つことはできません。  
  
> [!NOTE]
>  実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。 設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。 詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。  
  
### <a name="to-create-an-access-key-for-a-control"></a>コントロールのアクセス キーを作成するには  
  
1.  **プロパティ**ウィンドウで、設定、`Text`プロパティへのアクセス キーとなる文字の前にアンパサンドを含む文字列 (&)。 たとえば、アクセス キーとして、文字"P"を設定する次のように入力します。 **& 印刷**グリッドにします。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.Button>
- [方法: Windows フォームのボタン クリックに応答するには](../../../../docs/framework/winforms/controls/how-to-respond-to-windows-forms-button-clicks.md)
- [方法: によって表示されるテキストを設定、Windows フォーム コントロール](../../../../docs/framework/winforms/controls/how-to-set-the-text-displayed-by-a-windows-forms-control.md)
- [各 Windows フォーム コントロールのラベル設定とショートカットの作成](../../../../docs/framework/winforms/controls/labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
