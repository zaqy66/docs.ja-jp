---
title: '方法: デザイナーを使用して Windows フォーム tabcontrol のタブ追加および削除'
ms.date: 03/30/2017
helpviewer_keywords:
- tabs [Windows Forms], removing from pages
- TabPage control
- TabPage control [Windows Forms], adding and removing tabs
- tabs [Windows Forms], adding to pages
- tab pages
ms.assetid: 480633db-413a-45d2-9c8f-0427cc13adbe
ms.openlocfilehash: befe0537d3046e7bbdd1860958487bd1d1fe7651
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2019
ms.locfileid: "56304935"
---
# <a name="how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol-using-the-designer"></a>方法: デザイナーを使用して Windows フォーム tabcontrol のタブ追加および削除
配置するとき、<xref:System.Windows.Forms.TabControl>コントロール フォームで、既定で 2 つのタブがあります。 追加したり、デザイナーを使用してタブを削除することができます。  
  
 次の手順が必要です、 **Windows アプリケーション**プロジェクトが含まれているフォームを<xref:System.Windows.Forms.TabControl>コントロール。 このようなプロジェクトの設定の詳細については、次を参照してください。[方法。Windows フォーム アプリケーション プロジェクトを作成](/visualstudio/ide/step-1-create-a-windows-forms-application-project)と[方法。Windows フォームにコントロールを追加](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)します。  
  
> [!NOTE]
>  実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。 設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。 詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。  
  
### <a name="to-add-or-remove-a-tab-using-the-designer"></a>追加またはデザイナーを使用してタブを削除するには  
  
-   コントロールのスマート タグでは、次のようにクリックします**タブの追加**または**タブの削除。**  
  
     - または -  
  
     **プロパティ**ウィンドウで、をクリックして、**省略記号**ボタン (![VisualStudioEllipsesButton スクリーン ショット](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) 横<xref:System.Windows.Forms.TabControl.TabPages%2A>プロパティを開き、 **TabPage コレクション エディター**します。 をクリックして、**追加**または**削除**ボタンをクリックします。  
  
## <a name="see-also"></a>関連項目
- [TabControl コントロール](../../../../docs/framework/winforms/controls/tabcontrol-control-windows-forms.md)
- [TabControl コントロールの概要](../../../../docs/framework/winforms/controls/tabcontrol-control-overview-windows-forms.md)
- [タブ ページにコントロールを追加します。](../../../../docs/framework/winforms/controls/how-to-add-a-control-to-a-tab-page.md)
- [タブ ページを無効にします。](../../../../docs/framework/winforms/controls/how-to-disable-tab-pages.md)
- [Windows フォーム TabControl の外観を変更します。](../../../../docs/framework/winforms/controls/how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
