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
# <a name="how-to-style-a-row-in-a-listview-that-implements-a-gridview"></a><span data-ttu-id="d45f3-102">方法: GridView を実装する ListView で行のスタイルを設定する</span><span class="sxs-lookup"><span data-stu-id="d45f3-102">How to: Style a Row in a ListView That Implements a GridView</span></span>
<span data-ttu-id="d45f3-103">この例の行のスタイルを設定する方法を示しています、<xref:System.Windows.Controls.ListView>を実装するコントロールを<xref:System.Windows.Controls.GridView><xref:System.Windows.Controls.ListView.View%2A>モード。</span><span class="sxs-lookup"><span data-stu-id="d45f3-103">This example shows how to style a row in a <xref:System.Windows.Controls.ListView> control that implements a <xref:System.Windows.Controls.GridView><xref:System.Windows.Controls.ListView.View%2A> mode.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d45f3-104">例</span><span class="sxs-lookup"><span data-stu-id="d45f3-104">Example</span></span>  
 <span data-ttu-id="d45f3-105">内の行のスタイルを設定することができます、<xref:System.Windows.Controls.ListView>コントロールを設定して、<xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A>上、<xref:System.Windows.Controls.ListView>コントロール。</span><span class="sxs-lookup"><span data-stu-id="d45f3-105">You can style a row in a <xref:System.Windows.Controls.ListView> control by setting an <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> on the <xref:System.Windows.Controls.ListView> control.</span></span> <span data-ttu-id="d45f3-106">として表されるアイテムのスタイルを設定する<xref:System.Windows.Controls.ListViewItem>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d45f3-106">Set the style for its items that are represented as <xref:System.Windows.Controls.ListViewItem> objects.</span></span> <span data-ttu-id="d45f3-107"><xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A>参照、<xref:System.Windows.Controls.ControlTemplate>される行の内容を表示するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d45f3-107">The <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> references the <xref:System.Windows.Controls.ControlTemplate> objects that are used to display the row content.</span></span>  
  
 <span data-ttu-id="d45f3-108">次の例の抽出元である完全なサンプルは、[!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)]データベースに格納されている楽曲情報のコレクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="d45f3-108">The complete sample, which the following examples are extracted from, displays a collection of song information that is stored in an [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] database.</span></span> <span data-ttu-id="d45f3-109">データベースの各曲にはレーティングフィールドがあり、このフィールドの値が曲情報の行を表示する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="d45f3-109">Each song in the database has a rating field and the value of this field specifies how to display a row of song information.</span></span>  
  
 <span data-ttu-id="d45f3-110">次の例は、定義する方法を示します<xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A>の<xref:System.Windows.Controls.ListViewItem>曲のコレクション内の曲を表すオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d45f3-110">The following example shows how to define <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> for the <xref:System.Windows.Controls.ListViewItem> objects that represent the songs in the song collection.</span></span> <span data-ttu-id="d45f3-111"><xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A>参照<xref:System.Windows.Controls.ControlTemplate>曲情報の行を表示する方法を指定するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d45f3-111">The <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> references <xref:System.Windows.Controls.ControlTemplate> objects that specify how to display a row of song information.</span></span>  
  
 [!code-xaml[ListViewItemStyleSnippet#ItemContainerStyle](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#itemcontainerstyle)]  
  
 <span data-ttu-id="d45f3-112">次の例は、<xref:System.Windows.Controls.ControlTemplate>テキスト文字列を追加する`"Strongly Recommended"`行にします。</span><span class="sxs-lookup"><span data-stu-id="d45f3-112">The following example shows a <xref:System.Windows.Controls.ControlTemplate> that adds the text string `"Strongly Recommended"` to the row.</span></span> <span data-ttu-id="d45f3-113">このテンプレートが参照されている、<xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A>および楽曲のレーティングがある 5 (5) の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d45f3-113">This template is referenced in the <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> and displays when the song's rating has a value of 5 (five).</span></span> <span data-ttu-id="d45f3-114"><xref:System.Windows.Controls.ControlTemplate>が含まれています、<xref:System.Windows.Controls.GridViewRowPresenter>で定義されている列の行の内容がレイアウト オブジェクト、<xref:System.Windows.Controls.GridView>表示モード。</span><span class="sxs-lookup"><span data-stu-id="d45f3-114">The <xref:System.Windows.Controls.ControlTemplate> includes a <xref:System.Windows.Controls.GridViewRowPresenter> object that lays out the contents of the row in columns as defined by the <xref:System.Windows.Controls.GridView> view mode.</span></span>  
  
 [!code-xaml[ListViewItemStyleSnippet#ControlTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#controltemplate)]  
  
 <span data-ttu-id="d45f3-115">次の例では、定義<xref:System.Windows.Controls.GridView>します。</span><span class="sxs-lookup"><span data-stu-id="d45f3-115">The following example defines <xref:System.Windows.Controls.GridView>.</span></span>  
  
 [!code-xaml[ListViewItemStyleSnippet#GridView](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#gridview)]  
  
## <a name="see-also"></a><span data-ttu-id="d45f3-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d45f3-116">See also</span></span>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="d45f3-117">方法トピック</span><span class="sxs-lookup"><span data-stu-id="d45f3-117">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)
- [<span data-ttu-id="d45f3-118">ListView の概要</span><span class="sxs-lookup"><span data-stu-id="d45f3-118">ListView Overview</span></span>](../../../../docs/framework/wpf/controls/listview-overview.md)
- [<span data-ttu-id="d45f3-119">スタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="d45f3-119">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)
