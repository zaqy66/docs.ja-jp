---
title: '方法: 要素からすべての装飾を削除する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: fe5303a3-b76e-4643-aafb-51419032b47b
ms.openlocfilehash: 310b0249c215801b2634d51a1a1117bd7df83526
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54680192"
---
# <a name="how-to-remove-all-adorners-from-an-element"></a><span data-ttu-id="78568-102">方法: 要素からすべての装飾を削除する</span><span class="sxs-lookup"><span data-stu-id="78568-102">How to: Remove all Adorners from an Element</span></span>
<span data-ttu-id="78568-103">この例は、プログラムで指定したすべての装飾を削除する方法を示しています。<xref:System.Windows.UIElement>します。</span><span class="sxs-lookup"><span data-stu-id="78568-103">This example shows how to programmatically remove all adorners from a specified <xref:System.Windows.UIElement>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="78568-104">例</span><span class="sxs-lookup"><span data-stu-id="78568-104">Example</span></span>  
 <span data-ttu-id="78568-105">この詳細なコード例では、すべての装飾を削除によって返される装飾の配列で<xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>します。</span><span class="sxs-lookup"><span data-stu-id="78568-105">This verbose code example removes all of the adorners in the array of adorners returned by <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.</span></span>  <span data-ttu-id="78568-106">この例の発生時に、装飾を取得する、<xref:System.Windows.UIElement>という*myTextBox*します。</span><span class="sxs-lookup"><span data-stu-id="78568-106">This example happens to retrieve the adorners on a <xref:System.Windows.UIElement> named *myTextBox*.</span></span>  <span data-ttu-id="78568-107">呼び出しで、要素が指定されている場合<xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>、装飾を持たない`null`が返されます。</span><span class="sxs-lookup"><span data-stu-id="78568-107">If the element specified in the call to <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> has no adorners, `null` is returned.</span></span>  <span data-ttu-id="78568-108">このコードは明示的に null の配列をチェックし、アプリケーションに最適に比較的一般的な null 配列が必要な場合は、します。</span><span class="sxs-lookup"><span data-stu-id="78568-108">This code explicitly checks for a null array, and is best suited for applications where a null array is expected to be relatively common.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersLong](../../../../samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornerslong)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersLong](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornerslong)]  
  
## <a name="example"></a><span data-ttu-id="78568-109">例</span><span class="sxs-lookup"><span data-stu-id="78568-109">Example</span></span>  
 <span data-ttu-id="78568-110">この要約のコード例は、機能的には、前述の詳細な例です。</span><span class="sxs-lookup"><span data-stu-id="78568-110">This condensed code example is functionally equivalent to the verbose example shown above.</span></span> <span data-ttu-id="78568-111">このコードで明示的に確認、null 配列のできないできるようにする、<xref:System.NullReferenceException>例外が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="78568-111">This code does not explicitly check for a null array, so it is possible that a <xref:System.NullReferenceException> exception may be raised.</span></span>  <span data-ttu-id="78568-112">このコードは、null 配列のまれなことが必要です、アプリケーションに最適です。</span><span class="sxs-lookup"><span data-stu-id="78568-112">This code is best suited for applications where a null array is expected to be rare.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersShort](../../../../samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornersshort)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersShort](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornersshort)]  
  
## <a name="see-also"></a><span data-ttu-id="78568-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="78568-113">See also</span></span>
- [<span data-ttu-id="78568-114">装飾の概要</span><span class="sxs-lookup"><span data-stu-id="78568-114">Adorners Overview</span></span>](../../../../docs/framework/wpf/controls/adorners-overview.md)
