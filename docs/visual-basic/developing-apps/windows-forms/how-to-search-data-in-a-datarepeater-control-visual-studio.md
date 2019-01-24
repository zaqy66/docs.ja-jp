---
title: '方法: DataRepeater コントロール (Visual Studio) でデータの検索'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, implementing search
- DataRepeater, searching data
ms.assetid: a8ab5d17-b94f-43c4-8dd7-d0450226d73f
ms.openlocfilehash: 514e72afc9570071f57e385574456ff7d716bad7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654387"
---
# <a name="how-to-search-data-in-a-datarepeater-control-visual-studio"></a>方法: DataRepeater コントロール (Visual Studio) でデータの検索
使用する場合は、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>ユーザーの特定のレコードを検索する場合、多くのレコードを格納しているコントロール。 基になるクエリを実行して、検索を実装するコントロール自体にデータを検索するのではなく<xref:System.Windows.Forms.BindingSource>します。 使用できますし、項目が見つかった場合、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CurrentItemIndex%2A>プロパティを項目を選択し、表示されるまでスクロールします。  
  
### <a name="to-implement-search"></a>検索を実装する  
  
1.  <xref:System.Windows.Forms.TextBox> コントロールが含まれるフォーム上に、 **ツールボックス** から <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> コントロールをドラッグします。  
  
2.  [プロパティ] ウィンドウで、 **Name** プロパティを **SearchTextBox**に変更します。  
  
3.  <xref:System.Windows.Forms.Button> コントロールが含まれるフォーム上に、 **ツールボックス** から <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> コントロールをドラッグします。  
  
4.  [プロパティ] ウィンドウで、 **Name** プロパティを **SearchButton**に変更します。 **Text** プロパティを **Search**に変更します。  
  
5.  <xref:System.Windows.Forms.Button> コントロールをダブルクリックしてコード エディターを開き、 `SearchButton_Click` イベント ハンドラーに次のコードを追加します。  
  
     [!code-vb[VbPowerPacksDataRepeaterSearch#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-search-data-in-a-datarepeater-control-visual-studio_1.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterSearch#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-search-data-in-a-datarepeater-control-visual-studio_1.cs)]  
  
     置換*ProductsBindingSource*の名前を持つ、<xref:System.Windows.Forms.BindingSource>の<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>と置換*ProductID*に検索するフィールドの名前に置き換えます。  
  
## <a name="see-also"></a>関連項目
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- [DataRepeater コントロールの概要](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [DataRepeater コントロールのトラブルシューティング](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールの外観を変更します。](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
