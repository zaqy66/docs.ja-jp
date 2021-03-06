---
title: Windows フォーム DataGridView コントロールのカスタマイズ
ms.date: 03/30/2017
helpviewer_keywords:
- data grids [Windows Forms], customization
- DataGridView control [Windows Forms], customization
ms.assetid: 01ea5d4c-a736-4596-b0e9-a67a1b86e15f
ms.openlocfilehash: 901b221f74fa76221ed3f19e9eb4c5f17c6534fa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54559555"
---
# <a name="customizing-the-windows-forms-datagridview-control"></a>Windows フォーム DataGridView コントロールのカスタマイズ
`DataGridView`コントロールのセル、行、列の基本的な動作 (ルック アンド フィール) と外観を調整するために使用できるいくつかのプロパティを提供します。 機能を上回る特別なニーズがあるかどうか、<xref:System.Windows.Forms.DataGridViewCellStyle>クラス、ただしも所有者コントロールの描画を実装したり、カスタムのセル、列、および行を作成してその機能を拡張します。  
  
 描画するセルと行自分で、さまざまな処理できる`DataGridView`描画イベント。 既存から派生した独自の型を作成するには、既存の機能を変更したり、新しい機能を提供、 `DataGridViewCell`、 `DataGridViewColumn`、および`DataGridViewRow`型。 独自のセルが編集モードのときのコントロールを表示する派生型を作成、新しい編集機能を指定することもできます。  
  
## <a name="in-this-section"></a>このセクションの内容  
 [方法: Windows フォームの DataGridView コントロール内のセルの外観をカスタマイズします。](../../../../docs/framework/winforms/controls/customize-the-appearance-of-cells-in-the-datagrid.md)  
 処理する方法について説明します、<xref:System.Windows.Forms.DataGridView.CellPainting>セルを手動で描画するためにイベント。  
  
 [方法: Windows フォームの DataGridView コントロール内の行の外観をカスタマイズします。](../../../../docs/framework/winforms/controls/customize-the-appearance-of-rows-in-the-datagrid.md)  
 処理する方法について説明します、<xref:System.Windows.Forms.DataGridView.RowPrePaint>と<xref:System.Windows.Forms.DataGridView.RowPostPaint>にまたがる複数の列のカスタムのグラデーションの背景を持つ行を描画してコンテンツをするためにイベント。  
  
 [方法: それぞれの動作と外観を拡張することによって、セルと、Windows フォーム DataGridView コントロール内の列をカスタマイズします。](../../../../docs/framework/winforms/controls/customize-cells-and-columns-in-the-datagrid-by-extending-behavior.md)  
 派生したカスタムの型を作成する方法について説明します`DataGridViewCell`と`DataGridViewColumn`にマウス ポインターを合わせると、セルを強調表示するためにします。  
  
 [方法: Windows フォーム DataGridView コントロールのボタン列のボタンを無効にします。](../../../../docs/framework/winforms/controls/disable-buttons-in-a-button-column-in-the-datagrid.md)  
 派生したカスタムの型を作成する方法について説明します<xref:System.Windows.Forms.DataGridViewButtonCell>と<xref:System.Windows.Forms.DataGridViewButtonColumn>ボタン列に無効になっているボタンを表示するためにします。  
  
 [方法: Windows フォーム DataGridView Cells でコントロールをホスト](../../../../docs/framework/winforms/controls/how-to-host-controls-in-windows-forms-datagridview-cells.md)  
 実装する方法について説明します、`IDataGridViewEditingControl`インターフェイスし、から派生したカスタムの型を作成`DataGridViewCell`と`DataGridViewColumn`表示するために、<xref:System.Windows.Forms.DateTimePicker>セルが編集モードのときを制御します。  
  
## <a name="reference"></a>参照  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.DataGridView> コントロールのリファレンス ドキュメントを提供します。  
  
 <xref:System.Windows.Forms.DataGridViewCell>  
 リファレンス ドキュメントを提供、<xref:System.Windows.Forms.DataGridViewCell>クラス。  
  
 <xref:System.Windows.Forms.DataGridViewRow>  
 リファレンス ドキュメントを提供、<xref:System.Windows.Forms.DataGridViewRow>クラス。  
  
 <xref:System.Windows.Forms.DataGridViewColumn>  
 リファレンス ドキュメントを提供、<xref:System.Windows.Forms.DataGridViewColumn>クラス。  
  
 <xref:System.Windows.Forms.IDataGridViewEditingControl>  
 リファレンス ドキュメントを提供、<xref:System.Windows.Forms.IDataGridViewEditingControl>インターフェイス。  
  
## <a name="related-sections"></a>関連項目  
 [Windows フォームの DataGridView コントロールの基本的な書式設定およびスタイル設定](../../../../docs/framework/winforms/controls/basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)  
 コントロールの基本の外観およびセル データの書式設定を変更する方法を説明するトピックを示します。  
  
## <a name="see-also"></a>関連項目
- [DataGridView コントロール](../../../../docs/framework/winforms/controls/datagridview-control-windows-forms.md)
- [Windows フォーム DataGridView コントロールの列型](../../../../docs/framework/winforms/controls/column-types-in-the-windows-forms-datagridview-control.md)
