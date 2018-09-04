---
title: '方法 : ビジュアルにテキストを描画する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- typography [WPF], drawing text to visuals
- visuals [WPF], drawing text to
- text [WPF], drawing to visuals
- drawing [WPF], text to visuals
ms.assetid: fee4003c-e8a6-46ec-babd-2c7f4231a101
ms.openlocfilehash: bc7a4f989137ec2b021d27a6e112ff1aebd99d07
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43523244"
---
# <a name="how-to-draw-text-to-a-visual"></a><span data-ttu-id="d1b49-102">方法 : ビジュアルにテキストを描画する</span><span class="sxs-lookup"><span data-stu-id="d1b49-102">How to: Draw Text to a Visual</span></span>
<span data-ttu-id="d1b49-103">次の例では、テキストを描画する方法を示しています、<xref:System.Windows.Media.DrawingVisual>を使用して、<xref:System.Windows.Media.DrawingContext>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d1b49-103">The following example shows how to draw text to a <xref:System.Windows.Media.DrawingVisual> using a <xref:System.Windows.Media.DrawingContext> object.</span></span> <span data-ttu-id="d1b49-104">描画コンテキストが呼び出しによって返される、<xref:System.Windows.Media.DrawingVisual.RenderOpen%2A>のメソッドを<xref:System.Windows.Media.DrawingVisual>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d1b49-104">A drawing context is returned by calling the <xref:System.Windows.Media.DrawingVisual.RenderOpen%2A> method of a <xref:System.Windows.Media.DrawingVisual> object.</span></span> <span data-ttu-id="d1b49-105">グラフィックスとテキストを描画コンテキストに描画できます。</span><span class="sxs-lookup"><span data-stu-id="d1b49-105">You can draw graphics and text into a drawing context.</span></span>  
  
 <span data-ttu-id="d1b49-106">描画コンテキストにテキストを描画するために使用して、<xref:System.Windows.Media.DrawingContext.DrawText%2A>のメソッドを<xref:System.Windows.Media.DrawingContext>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d1b49-106">To draw text into the drawing context, use the <xref:System.Windows.Media.DrawingContext.DrawText%2A> method of a <xref:System.Windows.Media.DrawingContext> object.</span></span> <span data-ttu-id="d1b49-107">コンテンツを描画コンテキストに描画が完了したら、呼び出し、<xref:System.Windows.Media.DrawingContext.Close%2A>メソッドを描画コンテキストを閉じるし、内容を保持します。</span><span class="sxs-lookup"><span data-stu-id="d1b49-107">When you are finished drawing content into the drawing context, call the <xref:System.Windows.Media.DrawingContext.Close%2A> method to close the drawing context and persist the content.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d1b49-108">例</span><span class="sxs-lookup"><span data-stu-id="d1b49-108">Example</span></span>  
 [!code-csharp[DrawingVisualSample#110](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingVisualSample/CSharp/Window1.xaml.cs#110)]
 [!code-vb[DrawingVisualSample#110](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DrawingVisualSample/visualbasic/window1.xaml.vb#110)]  
  
> [!NOTE]
>  <span data-ttu-id="d1b49-109">上記のコードの抽出元となった完全なコード サンプルについては、「[DrawingVisual を使用したヒット テストのサンプル](https://go.microsoft.com/fwlink/?LinkID=159994)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1b49-109">For the complete code sample from which the preceding code example was extracted, see [Hit Test Using DrawingVisuals Sample](https://go.microsoft.com/fwlink/?LinkID=159994).</span></span>
