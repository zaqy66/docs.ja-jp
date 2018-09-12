---
title: '方法 : デザイン時にフォームの端に合わせてコントロールを配置する'
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], docking using designer
- Dock property [Windows Forms], aligning controls (using designer)
ms.assetid: 51f08998-5e3b-4330-be58-a4edd0eb60f4
ms.openlocfilehash: 513029c1bd5cc4af52fcee97f7fab961729e613c
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44710516"
---
# <a name="how-to-align-a-control-to-the-edges-of-forms-at-design-time"></a>方法 : デザイン時にフォームの端に合わせてコントロールを配置する
コントロールを設定して、フォームの端に合わせて整列を行うことができます、<xref:System.Windows.Forms.Control.Dock%2A>します。 このプロパティは、フォーム内のコントロールの場所を指定します。 <xref:System.Windows.Forms.Control.Dock%2A> プロパティには次の値のいずれかを設定できます。  
  
|設定|コントロールへの影響|  
|-------------|----------------------------|  
|<xref:System.Windows.Forms.DockStyle.Bottom>|フォームの下部にドッキングします。|  
|<xref:System.Windows.Forms.DockStyle.Fill>|フォームの残りの全スペースを埋めます。|  
|<xref:System.Windows.Forms.DockStyle.Left>|フォームの左側にドッキングします。|  
|<xref:System.Windows.Forms.DockStyle.None>|によって指定された場所に表示されます、任意の場所と、ドッキングせずその<xref:System.Windows.Forms.Control.Location%2A>します。|  
|<xref:System.Windows.Forms.DockStyle.Right>|フォームの右側にドッキングします。|  
|<xref:System.Windows.Forms.DockStyle.Top>|フォームの上部にドッキングします。|  
  
 これらの値は、コードでも設定できます。 詳細については、次を参照してください。[方法: コントロールをフォームの端を揃える](../../../../docs/framework/winforms/controls/how-to-align-a-control-to-the-edges-of-forms.md)します。  
  
> [!NOTE]
>  実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。 設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。 詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。  
  
### <a name="to-set-the-dock-property-for-your-control-at-design-time"></a>デザイン時に、コントロールの Dock プロパティを設定するには  
  
1.  Windows フォーム デザイナーでコントロールを選択します。  
  
2.  **プロパティ**ウィンドウで、ドロップダウン リスト ボックスには、[次へ] をクリックして、<xref:System.Windows.Forms.Control.Dock%2A>プロパティ。  
  
     6 つを表すグラフィカル インターフェイス<xref:System.Windows.Forms.Control.Dock%2A>設定が表示されます。  
  
3.  適切な設定を選択します。  
  
4.  コントロールの設定で指定された方法でドッキングされます。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType>  
 [方法: フォームの端に合わせてコントロールを配置する](../../../../docs/framework/winforms/controls/how-to-align-a-control-to-the-edges-of-forms.md)  
 [チュートリアル: スナップ線を使用した Windows フォーム上のコントロールの配置](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)  
 [方法: Windows フォームにコントロールを固定する](../../../../docs/framework/winforms/controls/how-to-anchor-controls-on-windows-forms.md)  
 [方法: TableLayoutPanel コントロールで子コントロールを固定およびドッキングする](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)  
 [方法: FlowLayoutPanel コントロールで子コントロールを固定およびドッキングする](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)  
 [チュートリアル: TableLayoutPanel を使用した Windows フォーム上のコントロールの配置](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)  
 [チュートリアル: FlowLayoutPanel を使用した Windows フォーム上のコントロールの配置](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)  
 [デザイン時の Windows フォーム コントロールの開発](../../../../docs/framework/winforms/controls/developing-windows-forms-controls-at-design-time.md)
