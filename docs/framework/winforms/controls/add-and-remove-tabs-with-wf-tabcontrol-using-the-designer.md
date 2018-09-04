---
title: '方法 : デザイナーで Windows フォーム TabControl を使ってタブを追加および削除する'
ms.date: 03/30/2017
helpviewer_keywords:
- tabs [Windows Forms], removing from pages
- TabPage control
- TabPage control [Windows Forms], adding and removing tabs
- tabs [Windows Forms], adding to pages
- tab pages
ms.assetid: 480633db-413a-45d2-9c8f-0427cc13adbe
ms.openlocfilehash: 51f84a1272749b92f8ef4a74771c84e01511a678
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43521327"
---
# <a name="how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol-using-the-designer"></a>方法 : デザイナーで Windows フォーム TabControl を使ってタブを追加および削除する
配置するとき、<xref:System.Windows.Forms.TabControl>コントロール フォームで、既定で 2 つのタブがあります。 追加したり、デザイナーを使用してタブを削除することができます。  
  
 次の手順が必要です、 **Windows アプリケーション**プロジェクトが含まれているフォームを<xref:System.Windows.Forms.TabControl>コントロール。 このようなプロジェクトの設定の詳細については、次を参照してください。[方法: Windows アプリケーション プロジェクトを作成](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa)と[方法: Windows フォームにコントロールを追加](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)します。  
  
> [!NOTE]
>  実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。 設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。 詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。  
  
### <a name="to-add-or-remove-a-tab-using-the-designer"></a>追加またはデザイナーを使用してタブを削除するには  
  
-   コントロールのスマート タグでは、次のようにクリックします**タブの追加**または**タブの削除。**  
  
     - または -  
  
     **プロパティ**ウィンドウで、をクリックして、**省略記号**ボタン (![VisualStudioEllipsesButton スクリーン ショット](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) 横<xref:System.Windows.Forms.TabControl.TabPages%2A>プロパティを開き、 **TabPage コレクション エディター**します。 をクリックして、**追加**または**削除**ボタンをクリックします。  
  
## <a name="see-also"></a>関連項目  
 [TabControl コントロール](../../../../docs/framework/winforms/controls/tabcontrol-control-windows-forms.md)  
 [TabControl コントロールの概要](../../../../docs/framework/winforms/controls/tabcontrol-control-overview-windows-forms.md)  
 [方法: タブ ページにコントロールを追加する](../../../../docs/framework/winforms/controls/how-to-add-a-control-to-a-tab-page.md)  
 [方法: タブ ページを無効化する](../../../../docs/framework/winforms/controls/how-to-disable-tab-pages.md)  
 [方法: Windows フォーム TabControl の表示形式を変更する](../../../../docs/framework/winforms/controls/how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
