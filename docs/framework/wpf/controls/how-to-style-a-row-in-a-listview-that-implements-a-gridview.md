---
title: '方法: GridView を実装する ListView で行のスタイルを設定する'
ms.date: 03/30/2017
helpviewer_keywords:
- GridView controls [WPF], styling rows
- styling rows in ListViews implementing GridViews [WPF]
- ListView controls [WPF], styling rows with GridViews
ms.assetid: 2e406ba2-70a0-4e62-841f-0934859de76e
ms.openlocfilehash: 39801af88d3e64b92aa7e99ff794c3d7e7239df5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54680232"
---
# <a name="how-to-style-a-row-in-a-listview-that-implements-a-gridview"></a>方法: GridView を実装する ListView で行のスタイルを設定する
この例の行のスタイルを設定する方法を示しています、<xref:System.Windows.Controls.ListView>を実装するコントロールを<xref:System.Windows.Controls.GridView><xref:System.Windows.Controls.ListView.View%2A>モード。  
  
## <a name="example"></a>例  
 内の行のスタイルを設定することができます、<xref:System.Windows.Controls.ListView>コントロールを設定して、<xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A>上、<xref:System.Windows.Controls.ListView>コントロール。 として表されるアイテムのスタイルを設定する<xref:System.Windows.Controls.ListViewItem>オブジェクト。 <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A>参照、<xref:System.Windows.Controls.ControlTemplate>される行の内容を表示するオブジェクト。  
  
 次の例の抽出元である完全なサンプルは、[!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)]データベースに格納されている楽曲情報のコレクションを表示します。 データベースの各曲にはレーティングフィールドがあり、このフィールドの値が曲情報の行を表示する方法を指定します。  
  
 次の例は、定義する方法を示します<xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A>の<xref:System.Windows.Controls.ListViewItem>曲のコレクション内の曲を表すオブジェクト。 <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A>参照<xref:System.Windows.Controls.ControlTemplate>曲情報の行を表示する方法を指定するオブジェクト。  
  
 [!code-xaml[ListViewItemStyleSnippet#ItemContainerStyle](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#itemcontainerstyle)]  
  
 次の例は、<xref:System.Windows.Controls.ControlTemplate>テキスト文字列を追加する`"Strongly Recommended"`行にします。 このテンプレートが参照されている、<xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A>および楽曲のレーティングがある 5 (5) の値が表示されます。 <xref:System.Windows.Controls.ControlTemplate>が含まれています、<xref:System.Windows.Controls.GridViewRowPresenter>で定義されている列の行の内容がレイアウト オブジェクト、<xref:System.Windows.Controls.GridView>表示モード。  
  
 [!code-xaml[ListViewItemStyleSnippet#ControlTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#controltemplate)]  
  
 次の例では、定義<xref:System.Windows.Controls.GridView>します。  
  
 [!code-xaml[ListViewItemStyleSnippet#GridView](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#gridview)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [方法トピック](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)
- [ListView の概要](../../../../docs/framework/wpf/controls/listview-overview.md)
- [スタイルとテンプレート](../../../../docs/framework/wpf/controls/styling-and-templating.md)
