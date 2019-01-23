---
title: '方法: BetweenShowDelay プロパティを使用する'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolTip control [WPF], BetweenShowDelay time property
- BetweenShowDelay time property [WPF]
ms.assetid: 984ea76d-f2a2-4326-a02e-f97ec3d036d6
ms.openlocfilehash: ee9c532f8b2eeddb2c798df53e1864e8f543638b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564059"
---
# <a name="how-to-use-the-betweenshowdelay-property"></a>方法: BetweenShowDelay プロパティを使用する
使用する方法を示します、<xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A>時間プロパティのツールヒントがすぐに表示されるように、ほとんどまたはまったくない遅延が、移動したときに、ユーザー、マウスのポインター 1 つのヒントからを別。  
  
## <a name="example"></a>例  
 次の例では、<xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A>プロパティが 1 秒 (1000 ミリ秒) に設定し、 <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> 2 秒 (2000 ミリ秒) の両方に設定されている<xref:System.Windows.Shapes.Ellipse>コントロール。 省略記号のいずれかのツールヒントを表示し、マウス ポインターを移動もう 1 つの楕円に一時停止、2 秒以内にしていて、すぐに 2 番目の楕円のツールヒントを表示します。  
  
 次のシナリオのいずれかで、<xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A>が適用されることが表示されるまで 1 秒間待機する 2 番目の楕円のツールヒントを停止します。  
  
-   移動にかかる時間 2 番目のボタンは 2 秒以上が。  
  
-   ツールヒントが最初の楕円の時間間隔の先頭に表示されていない場合。  
  
 [!code-xaml[ToolTipService#ToolTip](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#tooltip)]  
[!code-xaml[ToolTipService#NoToolTip](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#notooltip)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Controls.ToolTip>
- <xref:System.Windows.Controls.ToolTipService>
- [方法トピック](../../../../docs/framework/wpf/controls/tooltip-how-to-topics.md)
- [ToolTip の概要](../../../../docs/framework/wpf/controls/tooltip-overview.md)
