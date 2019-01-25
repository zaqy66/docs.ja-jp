---
title: '方法: TextWrapping プロパティをプログラムにより変更する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- documents [WPF], changing TextWrapping property programmatically
- TextWrapping property [WPF], changing programmatically
ms.assetid: 30d25554-4c82-4df9-a8d6-35683a4a13bb
ms.openlocfilehash: 6cf0993d0433e03a3c19bb59bf3621672e164b43
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54640226"
---
# <a name="how-to-change-the-textwrapping-property-programmatically"></a>方法: TextWrapping プロパティをプログラムにより変更する
## <a name="example"></a>例  
 次のコード例の値を変更する方法を示しています、<xref:System.Windows.Controls.TextBlock.TextWrapping%2A>プロパティ プログラムを使用します。  
  
 次の 3 つ<xref:System.Windows.Controls.Button>要素は、内に配置されます、<xref:System.Windows.Controls.StackPanel>要素[!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]します。 各<xref:System.Windows.Controls.Primitives.ButtonBase.Click>イベントを<xref:System.Windows.Controls.Button>コードでイベント ハンドラーに対応します。 イベント ハンドラーと同じ名前を使用して、<xref:System.Windows.Controls.TextBlock.TextWrapping%2A>値に適用されます`txt2`ボタンがクリックされたとき。 内のテキストも、 `txt1` (、<xref:System.Windows.Controls.TextBlock>に表示されていない、 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]) プロパティに変更を反映するように更新されます。  
  
 [!code-xaml[TextWrapProperty#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextWrapProperty/VisualBasic/Pane1.xaml#1)]  
  
 [!code-csharp[TextWrapProperty#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextWrapProperty/CSharp/Window1.xaml.cs#2)]
 [!code-vb[TextWrapProperty#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextWrapProperty/VisualBasic/Pane1.xaml.vb#2)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Controls.TextBlock.TextWrapping%2A>
- <xref:System.Windows.TextWrapping>
