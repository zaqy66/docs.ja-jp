---
title: '方法: TreeView のパフォーマンスを改善する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TreeView control [WPF], improving the performance
ms.assetid: b792c740-cf2b-4da8-8ba8-3d2e5a821874
ms.openlocfilehash: 3c7bd151e1c8a5f318660cc45702b5b9c98534a8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54500695"
---
# <a name="how-to-improve-the-performance-of-a-treeview"></a><span data-ttu-id="a1a71-102">方法: TreeView のパフォーマンスを改善する</span><span class="sxs-lookup"><span data-stu-id="a1a71-102">How to: Improve the Performance of a TreeView</span></span>
<span data-ttu-id="a1a71-103">場合、<xref:System.Windows.Controls.TreeView>多くの項目を含むの読み込みにかかる時間は、ユーザー インターフェイスで大きな遅延を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a1a71-103">If a <xref:System.Windows.Controls.TreeView> contains many items, the amount of time it takes to load may cause a significant delay in the user interface.</span></span> <span data-ttu-id="a1a71-104">設定して、読み込み時間を向上させることができます、`VirtualizingStackPanel.IsVirtualizing`添付プロパティを`true`します。</span><span class="sxs-lookup"><span data-stu-id="a1a71-104">You can improve the load time by setting the `VirtualizingStackPanel.IsVirtualizing` attached property to `true`.</span></span>  <span data-ttu-id="a1a71-105">UI は、ユーザーがスクロールときに応答に時間がかかる場合があります、<xref:System.Windows.Controls.TreeView>をマウス ホイールを使用するかスクロール バーのつまみをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="a1a71-105">The UI might also be slow to react when a user scrolls the <xref:System.Windows.Controls.TreeView> by using the mouse wheel or dragging the thumb of a scrollbar.</span></span> <span data-ttu-id="a1a71-106">パフォーマンスを向上させることができます、<xref:System.Windows.Controls.TreeView>を設定してユーザーがスクロールすると、`VirtualizingStackPanel.VirtualizationMode`添付プロパティを<xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType>します。</span><span class="sxs-lookup"><span data-stu-id="a1a71-106">You can improve the performance of the <xref:System.Windows.Controls.TreeView> when the user scrolls by setting the `VirtualizingStackPanel.VirtualizationMode` attached property to <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a1a71-107">例</span><span class="sxs-lookup"><span data-stu-id="a1a71-107">Example</span></span>  
  
## <a name="description"></a><span data-ttu-id="a1a71-108">説明</span><span class="sxs-lookup"><span data-stu-id="a1a71-108">Description</span></span>  
<span data-ttu-id="a1a71-109">次の例では、作成、<xref:System.Windows.Controls.TreeView>設定、`VirtualizingStackPanel.IsVirtualizing`添付プロパティを true に、`VirtualizingStackPanel.VirtualizationMode`添付プロパティを<xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType>そのパフォーマンスを最適化します。</span><span class="sxs-lookup"><span data-stu-id="a1a71-109">The following example creates a <xref:System.Windows.Controls.TreeView> that sets the `VirtualizingStackPanel.IsVirtualizing` attached property to true and the `VirtualizingStackPanel.VirtualizationMode` attached property to <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> to optimize its performance.</span></span>  
  
## <a name="code"></a><span data-ttu-id="a1a71-110">コード</span><span class="sxs-lookup"><span data-stu-id="a1a71-110">Code</span></span>  
 [!code-xaml[RecycleItemContainerShippets#VirtualizingTreeView](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml#virtualizingtreeview)]  
  
 <span data-ttu-id="a1a71-111">次の例では、前の例を使用してデータを示します。</span><span class="sxs-lookup"><span data-stu-id="a1a71-111">The following example shows the data that the previous example uses.</span></span>  
  
 [!code-csharp[RecycleItemContainerShippets#TreeViewData](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml.cs#treeviewdata)]
 [!code-vb[RecycleItemContainerShippets#TreeViewData](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/RecycleItemContainerShippets/visualbasic/window1.xaml.vb#treeviewdata)]  
  
## <a name="see-also"></a><span data-ttu-id="a1a71-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1a71-112">See also</span></span>
- [<span data-ttu-id="a1a71-113">コントロール</span><span class="sxs-lookup"><span data-stu-id="a1a71-113">Controls</span></span>](../../../../docs/framework/wpf/advanced/optimizing-performance-controls.md)
