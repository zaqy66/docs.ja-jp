---
title: '方法: GridView を実装する ListView の項目をグループ化する'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], grouping items with GridViews
- grouping items in ListViews implementing GridViews [WPF]
- GridView controls [WPF], grouping items
ms.assetid: eebef25b-ddc6-424e-a66d-ea228d1bf33d
ms.openlocfilehash: 1570eab70dae690f508975162b7553de92be6f12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54664357"
---
# <a name="how-to-group-items-in-a-listview-that-implements-a-gridview"></a>方法: GridView を実装する ListView の項目をグループ化する
この例では、グループ内の項目の表示、<xref:System.Windows.Controls.GridView>の表示モード、<xref:System.Windows.Controls.ListView>コントロール。  
  
## <a name="example"></a>例  
 内の項目のグループを表示する、 <xref:System.Windows.Controls.ListView>、定義、<xref:System.Windows.Data.CollectionViewSource>します。 次の例は、<xref:System.Windows.Data.CollectionViewSource>の値に基づいてデータ項目をグループ化、`Catalog`データ フィールド。  
  
 [!code-xaml[GridViewWithGroups#GroupingCollectionViewSource](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#groupingcollectionviewsource)]  
  
 次の例のセット、<xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>の<xref:System.Windows.Controls.ListView>を<xref:System.Windows.Data.CollectionViewSource>前の例を定義します。 また、<xref:System.Windows.Controls.ItemsControl.GroupStyle%2A>を実装する、<xref:System.Windows.Controls.Expander>コントロール。  
  
 [!code-xaml[GridViewWithGroups#ListViewGroups](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#listviewgroups)]  
[!code-xaml[GridViewWithGroups#ListViewEnd](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#listviewend)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [方法トピック](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)
- [ListView の概要](../../../../docs/framework/wpf/controls/listview-overview.md)
- [GridView の概要](../../../../docs/framework/wpf/controls/gridview-overview.md)
