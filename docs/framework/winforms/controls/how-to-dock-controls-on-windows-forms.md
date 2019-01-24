---
title: '方法: Windows フォーム上のコントロールをドッキングします。'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], docking
- Explorer-style applications [Windows Forms], creating
- Windows Forms controls, filling client area
ms.assetid: bc11f2e4-e90a-4830-b0e2-f43b6e2b8bec
ms.openlocfilehash: f4a9d3bcf7f9db1634da2b2f06177c05061af28e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54733546"
---
# <a name="how-to-dock-controls-on-windows-forms"></a>方法: Windows フォーム上のコントロールをドッキングします。
コントロールをフォームの端にドッキングまたはコントロールのコンテナー (フォームまたはコンテナー コントロールのいずれか) を入力することがあることができます。 たとえば、Windows エクスプ ローラーをドッキングその<xref:System.Windows.Forms.TreeView>、ウィンドウの左側にあるコントロールとその<xref:System.Windows.Forms.ListView>ウィンドウの右側にあるコントロール。 使用して、<xref:System.Windows.Forms.Control.Dock%2A>ドッキングのモードを定義する表示されているすべての Windows フォーム コントロールのプロパティ。  
  
> [!NOTE]
>  逆の z オーダーでコントロールがドッキングされます。  
  
 <xref:System.Windows.Forms.Control.Dock%2A>プロパティの対話、<xref:System.Windows.Forms.Control.AutoSize%2A>プロパティ。 詳細については、次を参照してください。 [AutoSize プロパティの概要](../../../../docs/framework/winforms/controls/autosize-property-overview.md)します。  
  
### <a name="to-dock-a-control"></a>コントロールをドッキングするには  
  
1.  ドッキングするコントロールを選択します。  
  
2.  [プロパティ] ウィンドウの右側にある矢印をクリックします。、<xref:System.Windows.Forms.Control.Dock%2A>プロパティ。  
  
     一連の端とフォームの中央を表すボックスを示しています。 エディターが表示されます。  
  
3.  コントロールをドッキングするフォームの端を表すボタンをクリックします。 コントロールのフォームまたはコンテナー コントロールの内容を入力するには、中央のボックスをクリックします。 クリックして **(なし)** ドッキングを無効にします。  
  
     コントロールのドッキングのエッジの境界に合わせてサイズを自動的にします。  
  
    > [!NOTE]
    >  継承されたコントロールである必要があります`Protected`ドッキングできるようにします。 コントロールのアクセス レベルを変更するには、次のように設定します。 その**修飾子**プロパティ ウィンドウでプロパティ。  
  
## <a name="see-also"></a>関連項目
- [Windows フォーム コントロール](../../../../docs/framework/winforms/controls/index.md)
- [Windows フォームでのコントロールの配置](../../../../docs/framework/winforms/controls/arranging-controls-on-windows-forms.md)
- [各 Windows フォーム コントロールのラベル設定とショートカットの作成](../../../../docs/framework/winforms/controls/labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [Windows フォームで使用するコントロール](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)
- [Windows フォーム コントロールの機能別一覧](../../../../docs/framework/winforms/controls/windows-forms-controls-by-function.md)
- [方法: 固定およびドッキング FlowLayoutPanel コントロールで子コントロール](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [方法: 固定およびドッキング TableLayoutPanel コントロールで子コントロール](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [AutoSize プロパティの概要](../../../../docs/framework/winforms/controls/autosize-property-overview.md)
- [方法: Windows フォームにコントロールを固定](../../../../docs/framework/winforms/controls/how-to-anchor-controls-on-windows-forms.md)
