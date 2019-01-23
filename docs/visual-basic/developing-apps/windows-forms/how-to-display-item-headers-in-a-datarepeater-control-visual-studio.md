---
title: '方法: DataRepeater コントロール (Visual Studio) に項目ヘッダーの表示'
ms.date: 07/20/2015
helpviewer_keywords:
- DataRepeater, item headers
- DataRepeater, selection indicators
ms.assetid: 37321447-0ffa-43e1-bdc9-0480e392b90f
ms.openlocfilehash: eccac1b3b02da41a34d47072be267f6c51a7d490
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504562"
---
# <a name="how-to-display-item-headers-in-a-datarepeater-control-visual-studio"></a>方法: DataRepeater コントロール (Visual Studio) に項目ヘッダーの表示
内の項目ヘッダーを<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールは、視覚的なインジケーターを提供します。 ときに、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>が選択されています。 ときに、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>プロパティに設定されて<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Vertical>(既定)、各項目の左側に項目ヘッダーが表示されます。 ときに、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>プロパティに設定されて<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Horizontal>、各項目の上部にある項目のヘッダーが表示されます。  
  
 項目ヘッダーがで指定されている色で表示されますが最初にオンの場合、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor%2A>プロパティ、および、白い矢印のアイコンが表示されます。  
  
> [!NOTE]
>  設定した場合、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor%2A>に<xref:System.Drawing.Color.White%2A>項目が最初に選択されたときに、選択の記号は表示されません。  
  
 内のフィールドの場合に、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>フォーカスに項目ヘッダーの変更の色、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>背景の色を黒に矢印アイコンに変化します。 データが変更された場合は、項目のヘッダー用の鉛筆アイコンが表示されます。  
  
 既定の幅 (または高さときに、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>プロパティに設定されて<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Horizontal>) 項目のヘッダーには 15 ピクセルです。 設定して、幅を変更することができます、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize%2A>プロパティ。  
  
> [!NOTE]
>  場合、 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize%2A> 11 より小さい値に設定されて、項目ヘッダーのマークは表示されません。  
  
 項目ヘッダーを非表示を設定してできます、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderVisible%2A>プロパティを**False**します。 ときに<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderVisible%2A>に設定されている**False**、項目が選択されている唯一の目印の周囲に点線、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>します。  
  
> [!NOTE]
>  監視することによって、独自の選択インジケーターを提供することも、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem.IsCurrent%2A>のプロパティ、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>で、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem>のイベント、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。 詳細については、「 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem.IsCurrent%2A> 」を参照してください。  
  
### <a name="to-change-the-appearance-of-item-headers"></a>項目ヘッダーの外観を変更するには  
  
1.  Windows フォーム デザイナーでの下部の領域を選択して、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。  
  
    > [!NOTE]
    >  コントロールの下の領域を選択する必要があります。 項目テンプレートのセクションを選択した場合、異なるプロパティのセットは、[プロパティ] ウィンドウに表示されます。  
  
2.  [プロパティ] ウィンドウで使用して、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor%2A>項目ヘッダーの色を変更するプロパティ。  
  
    > [!NOTE]
    >  設定した場合、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor%2A>に<xref:System.Drawing.Color.White%2A>項目が最初に選択されたときに、選択の記号は表示されません。  
  
3.  使用して、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize%2A>項目ヘッダーの幅 (または高さ) を変更するプロパティ。  
  
    > [!NOTE]
    >  場合、 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize%2A> 11 より小さい値に設定されて、項目ヘッダーのマークは表示されません。  
  
### <a name="to-hide-item-headers"></a>項目ヘッダーを非表示にするには  
  
1.  Windows フォーム デザイナーでの下部の領域を選択して、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。  
  
    > [!NOTE]
    >  コントロールの下の領域を選択する必要があります。 項目テンプレートのセクションを選択した場合、異なるプロパティのセットは、[プロパティ] ウィンドウに表示されます。  
  
2.  [プロパティ] ウィンドウで次のように設定します。、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderVisible%2A>プロパティを**False**します。  
  
     内の項目のときに、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>が選択されている唯一の目印の周囲に点線になります、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>します。  
  
## <a name="see-also"></a>関連項目
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- [DataRepeater コントロールの概要](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールの外観を変更します。](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールのレイアウトを変更します。](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-layout-of-a-datarepeater-control-visual-studio.md)
- [DataRepeater コントロールのトラブルシューティング](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
