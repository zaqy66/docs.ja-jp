---
title: '方法: DataRepeater コントロール (Visual Studio) のレイアウトを変更します。'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, changing layout style
- DataRepeater, changing orientation
ms.assetid: 33aa8fd5-ac63-4bd0-ba13-8c2ab17e7824
ms.openlocfilehash: 3389daa6383444b48faab4c5383b281e44349bce
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54625602"
---
# <a name="how-to-change-the-layout-of-a-datarepeater-control-visual-studio"></a>方法: DataRepeater コントロール (Visual Studio) のレイアウトを変更します。
<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> (垂直方向にスクロール バーの項目) 垂直または水平方向 (水平方向にスクロール バーの項目) のいずれかで表示できるコントロールの向き。 デザイン時または実行時に向きを変更するには変更することで、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>プロパティ。 変更した場合、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>実行時にプロパティをすることもサイズを変更する、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>と子コントロールの位置を指定します。  
  
> [!NOTE]
>  上のコントロールの位置を変更する場合、 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> 、実行時に呼び出す必要があります、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate%2A>と<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate%2A>メソッドは、コントロールを移動するコード ブロックの末尾、先頭にあります。  
  
### <a name="to-change-the-layout-at-design-time"></a>デザイン時にレイアウトを変更するには  
  
1.  Windows フォーム デザイナーで、選択、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。  
  
    > [!NOTE]
    >  外側の境界線を選択する必要があります、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>上ではなく、コントロールの下の領域をクリックしてコントロール<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>リージョン。  
  
2.  [プロパティ] ウィンドウで次のように設定します。、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>プロパティを<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Vertical>または<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Horizontal>します。  
  
### <a name="to-change-the-layout-at-run-time"></a>実行時にレイアウトを変更するには  
  
1.  次のコードをボタンまたはメニューに追加`Click`イベント ハンドラー。  
  
     [!code-csharp[VbPowerPacksDataRepeaterLayout#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterLayout#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_1.vb)]  
  
2.  ほとんどの場合、サイズを変更する例」のセクションに示されているようなコードを追加しますが、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>および新しい向きに合わせてコントロールを再配置します。  
  
## <a name="example"></a>例  
 次の例に応答する方法を示しています、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyleChanged>イベント ハンドラーでイベント。 この例が必要です、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>という名前のコントロール`DataRepeater1`フォームにその<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>2 つを含めることが<xref:System.Windows.Forms.TextBox>という名前のコントロール`TextBox1`と`TextBox2`します。  
  
 [!code-csharp[VbPowerPacksDataRepeaterLayout#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_2.cs)]
 [!code-vb[VbPowerPacksDataRepeaterLayout#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_2.vb)]  
  
## <a name="see-also"></a>関連項目
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate%2A>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate%2A>
- [DataRepeater コントロールの概要](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [DataRepeater コントロールのトラブルシューティング](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールの外観を変更します。](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
