---
title: '方法: Windows フォーム DataGridView コントロールでは読み取り専用に列を作成します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], read-only columns
- DataGridView control [Windows Forms], read-only columns
ms.assetid: 2bb73ebb-1a55-4362-9fda-e50574c087d5
ms.openlocfilehash: 6fbdf661983d39ad4793946f10deb3e224f2f711
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56583629"
---
# <a name="how-to-make-columns-read-only-in-the-windows-forms-datagridview-control"></a>方法: Windows フォーム DataGridView コントロールでは読み取り専用に列を作成します。
すべてのデータが編集できるわけではありません。 
  <xref:System.Windows.Forms.DataGridView> コントロールでは、列の <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A> プロパティの値はユーザーがその列のセルを編集できるかどうかを決定します。 完全に読み取り専用コントロールを作成する方法については、次を参照してください。[方法。行の追加を回避し、削除を Windows フォーム DataGridView コントロール](../../../../docs/framework/winforms/controls/prevent-row-addition-and-deletion-datagridview.md)します。  
  
 Visual Studio では、このタスクに対するサポートが用意されています。  参照してください[方法。列を読み取り専用の Windows フォーム DataGridView コントロールのデザイナーを使用して](make-columns-read-only-in-the-datagrid-using-the-designer.md)します。  
  
### <a name="to-make-a-column-read-only-programmatically"></a>プログラムで列を読み取り専用にするには  
  
-   <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A?displayProperty=nameWithType> プロパティを `true`に設定します。  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#064](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#064)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#064](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#064)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
-   `CompanyName` という名前の列を持つ `dataGridView1` という名前の <xref:System.Windows.Forms.DataGridView> コントロール。  
  
-   
  <xref:System?displayProperty=nameWithType> アセンブリおよび <xref:System.Windows.Forms?displayProperty=nameWithType> アセンブリへの参照。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.Columns%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A?displayProperty=nameWithType>
- [Windows フォーム DataGridView コントロールでの列、行、およびセルの基本機能](../../../../docs/framework/winforms/controls/basic-column-row-and-cell-features-wf-datagridview-control.md)
- [方法: Windows フォームの DataGridView コントロールで行の追加および削除を防ぐ](../../../../docs/framework/winforms/controls/prevent-row-addition-and-deletion-datagridview.md)
