---
title: '方法: Windows フォーム ListView コントロールに列を追加します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView control [Windows Forms], adding column headers
- columns [Windows Forms], adding to ListView controls
- list views [Windows Forms], adding columns
ms.assetid: 79174274-12ee-4a5d-80db-6ec02976d010
ms.openlocfilehash: eed032ec0bacd50666c30979b33362dabf00d565
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700196"
---
# <a name="how-to-add-columns-to-the-windows-forms-listview-control"></a>方法: Windows フォーム ListView コントロールに列を追加します。
詳細ビューで、<xref:System.Windows.Forms.ListView>コントロールは、各リスト項目の複数の列を表示できます。 いくつかの種類の各リスト項目に関する情報をユーザーに表示するのに列を使用することができます。 たとえば、ファイルの一覧には、ファイル名、ファイルの種類、サイズ、およびファイルの最終更新日を表示できます。 作成した後、列の設定方法の詳細については、次を参照してください。[方法。Windows での列にサブ項目を表示フォーム ListView コントロール](../../../../docs/framework/winforms/controls/how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md)します。  
  
### <a name="to-add-columns-programmatically"></a>プログラムで列を追加するには  
  
1.  コントロールの設定<xref:System.Windows.Forms.ListView.View%2A>プロパティを<xref:System.Windows.Forms.View.Details>します。  
  
2.  使用して、<xref:System.Windows.Forms.ListView.ColumnHeaderCollection.Add%2A>メソッドのリスト ビューの<xref:System.Windows.Forms.ListView.Columns%2A>プロパティ。  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#31)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#31)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.ListView>
- [ListView コントロール](../../../../docs/framework/winforms/controls/listview-control-windows-forms.md)
- [ListView コントロールの概要](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)
