---
title: '方法 : Windows フォームにコントロールをロックする'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, locking
- controls [Windows Forms], locking
ms.assetid: 94efe0d2-c14e-4d14-b903-63ea9b07e290
ms.openlocfilehash: 8de22ae6667446620867f3c15aac3c4af65582bf
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/30/2018
ms.locfileid: "43253631"
---
# <a name="how-to-lock-controls-to-windows-forms"></a>方法 : Windows フォームにコントロールをロックする
Windows アプリケーションのユーザー インターフェイス (UI) を設計するときは、正しく配置を誤って移動や、その他のプロパティを設定するときにサイズを変更しないようにすると、コントロールをロックできます。  
  
 さらに、ロックして、フォーム、一度に多くのコントロールをフォームには、上のすべてのコントロールをロック解除することができますか、個々 のコントロールのロックを解除することができます。 すべてのコントロールを配置し、フォーム上の任意の場所が後、を誤って移動を防ぐためにすべてのロックします。  
  
> [!NOTE]
>  実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。 設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。 詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。  
  
### <a name="to-lock-a-control"></a>コントロールをロックするには  
  
1.  **プロパティ**ウィンドウで、をクリックして、**ロック**プロパティと選択`true`します。 (名前をダブルクリックするとは、プロパティの設定を切り替えます。)  
  
     または、コントロールを右クリックし、選択**ロック コントロール**します。  
  
    > [!NOTE]
    >  コントロールがロックされないように、デザイン サーフェイスの新しいサイズまたは場所にドラッグされています。 ただし、することができます、サイズや位置を変更ことで、コントロールの**プロパティ**ウィンドウまたはコード。  
  
### <a name="to-lock-all-the-controls-on-a-form"></a>フォーム上のすべてのコントロールをロックするには  
  
1.  **形式**] メニューの [選択**ロック コントロール**します。  
  
    > [!NOTE]
    >  このコマンドは、フォームがコントロールであるため、フォームのサイズもをロックします。  
  
### <a name="to-unlock-all-locked-controls-on-a-form"></a>フォーム上のコントロールがロックされているすべてのロックを解除するには  
  
1.  **形式**] メニューの [選択**ロック コントロール**します。  
  
     フォーム上のすべてのロックされているコントロールがロックを解除します。  
  
### <a name="to-unlock-locked-controls-individually"></a>ロックを解除するには、コントロールを個別にロック  
  
1.  **プロパティ**ウィンドウで、をクリックして、**ロック**プロパティと選択`false`します。 (名前をダブルクリックするとは、プロパティの設定を切り替えます。)  
  
## <a name="see-also"></a>関連項目  
 [Windows フォーム コントロール](../../../../docs/framework/winforms/controls/index.md)  
 [Windows フォームでのコントロールの配置](../../../../docs/framework/winforms/controls/arranging-controls-on-windows-forms.md)  
 [各 Windows フォーム コントロールのラベル設定とショートカットの作成](../../../../docs/framework/winforms/controls/labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)  
 [Windows フォームで使用するコントロール](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)  
 [Windows フォーム コントロールの機能別一覧](../../../../docs/framework/winforms/controls/windows-forms-controls-by-function.md)
