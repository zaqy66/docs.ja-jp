---
title: '方法: Blocks プロパティを介して FlowDocument を操作する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- 'documents [WPF], manipulating FlowDocuments through Blocks property [WPF], , '
- ', '
ms.assetid: cbb7291e-3f1b-433e-9e16-f4d93ced14e8
ms.openlocfilehash: e4367e8907bbe9e9ce9ff7252d30e34c04f8ebd8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54567946"
---
# <a name="how-to-manipulate-a-flowdocument-through-the-blocks-property"></a><span data-ttu-id="2ed03-102">方法: Blocks プロパティを介して FlowDocument を操作する</span><span class="sxs-lookup"><span data-stu-id="2ed03-102">How to: Manipulate a FlowDocument through the Blocks Property</span></span>
<span data-ttu-id="2ed03-103">これらの例で実行できる一般的な操作の一部を<xref:System.Windows.Documents.FlowDocument>を通じて、<xref:System.Windows.Documents.FlowDocument.Blocks%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="2ed03-103">These examples demonstrate some of the more common operations that can be performed on a <xref:System.Windows.Documents.FlowDocument> through the <xref:System.Windows.Documents.FlowDocument.Blocks%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2ed03-104">例</span><span class="sxs-lookup"><span data-stu-id="2ed03-104">Example</span></span>  
 <span data-ttu-id="2ed03-105">次の例では、作成、新しい<xref:System.Windows.Documents.FlowDocument>し、新しい追加<xref:System.Windows.Documents.Paragraph>要素を<xref:System.Windows.Documents.FlowDocument>します。</span><span class="sxs-lookup"><span data-stu-id="2ed03-105">The following example creates a new <xref:System.Windows.Documents.FlowDocument> and then appends a new <xref:System.Windows.Documents.Paragraph> element to the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_FlowDocumentBlocksAdd](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_flowdocumentblocksadd)]
 [!code-vb[FlowDocumentSnippets#_FlowDocumentBlocksAdd](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_flowdocumentblocksadd)]  
  
## <a name="example"></a><span data-ttu-id="2ed03-106">例</span><span class="sxs-lookup"><span data-stu-id="2ed03-106">Example</span></span>  
 <span data-ttu-id="2ed03-107">次の例では、作成、新しい<xref:System.Windows.Documents.Paragraph>要素の開始位置に挿入し、<xref:System.Windows.Documents.FlowDocument>します。</span><span class="sxs-lookup"><span data-stu-id="2ed03-107">The following example creates a new <xref:System.Windows.Documents.Paragraph> element and inserts it at the beginning of the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_FlowDocumentBlocksInsert](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_flowdocumentblocksinsert)]
 [!code-vb[FlowDocumentSnippets#_FlowDocumentBlocksInsert](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_flowdocumentblocksinsert)]  
  
## <a name="example"></a><span data-ttu-id="2ed03-108">例</span><span class="sxs-lookup"><span data-stu-id="2ed03-108">Example</span></span>  
 <span data-ttu-id="2ed03-109">次の例では、最上位レベルの数を取得します。<xref:System.Windows.Documents.Block>に含まれる要素、<xref:System.Windows.Documents.FlowDocument>します。</span><span class="sxs-lookup"><span data-stu-id="2ed03-109">The following example gets the number of top-level <xref:System.Windows.Documents.Block> elements contained in the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_FlowDocumentBlocksCount](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_flowdocumentblockscount)]
 [!code-vb[FlowDocumentSnippets#_FlowDocumentBlocksCount](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_flowdocumentblockscount)]  
  
## <a name="example"></a><span data-ttu-id="2ed03-110">例</span><span class="sxs-lookup"><span data-stu-id="2ed03-110">Example</span></span>  
 <span data-ttu-id="2ed03-111">次の例では、削除、最終<xref:System.Windows.Documents.Block>内の要素、<xref:System.Windows.Documents.FlowDocument>します。</span><span class="sxs-lookup"><span data-stu-id="2ed03-111">The following example deletes the last <xref:System.Windows.Documents.Block> element in the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_FlowDocumentBlocksRemoveLast](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_flowdocumentblocksremovelast)]
 [!code-vb[FlowDocumentSnippets#_FlowDocumentBlocksRemoveLast](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_flowdocumentblocksremovelast)]  
  
## <a name="example"></a><span data-ttu-id="2ed03-112">例</span><span class="sxs-lookup"><span data-stu-id="2ed03-112">Example</span></span>  
 <span data-ttu-id="2ed03-113">次の例では、すべての内容をクリア (<xref:System.Windows.Documents.Block>要素) から、<xref:System.Windows.Documents.FlowDocument>します。</span><span class="sxs-lookup"><span data-stu-id="2ed03-113">The following example clears all of the contents (<xref:System.Windows.Documents.Block> elements) from the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_FlowDocumentBlocksClear](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_flowdocumentblocksclear)]
 [!code-vb[FlowDocumentSnippets#_FlowDocumentBlocksClear](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_flowdocumentblocksclear)]  
  
## <a name="see-also"></a><span data-ttu-id="2ed03-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ed03-114">See also</span></span>
- [<span data-ttu-id="2ed03-115">RowGroups プロパティを介してテーブルの行グループを操作する</span><span class="sxs-lookup"><span data-stu-id="2ed03-115">Manipulate a Table's Row Groups through the RowGroups Property</span></span>](../../../../docs/framework/wpf/advanced/how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
- [<span data-ttu-id="2ed03-116">Columns プロパティによってテーブルの列を操作する</span><span class="sxs-lookup"><span data-stu-id="2ed03-116">Manipulate a Table's Columns through the Columns Property</span></span>](../../../../docs/framework/wpf/advanced/how-to-manipulate-table-columns-through-the-columns-property.md)
- [<span data-ttu-id="2ed03-117">RowGroups プロパティを介してテーブルの行グループを操作する</span><span class="sxs-lookup"><span data-stu-id="2ed03-117">Manipulate a Table's Row Groups through the RowGroups Property</span></span>](../../../../docs/framework/wpf/advanced/how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
