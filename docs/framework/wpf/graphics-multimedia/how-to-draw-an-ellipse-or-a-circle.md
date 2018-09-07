---
title: '方法 : 楕円または円を描画する'
ms.date: 03/30/2017
helpviewer_keywords:
- ellipses [WPF], drawing
- circles [WPF], drawing
- drawing circles [WPF]
- drawing ellipses [WPF]
- graphics [WPF], drawing circles
- graphics [WPF], drawing ellipses
ms.assetid: 99763b8c-bfc8-44be-8231-8a70daf5481a
ms.openlocfilehash: ddeada8619d1b6c8970f1efb7cca1bc98773d0c5
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44079114"
---
# <a name="how-to-draw-an-ellipse-or-a-circle"></a><span data-ttu-id="eb470-102">方法 : 楕円または円を描画する</span><span class="sxs-lookup"><span data-stu-id="eb470-102">How to: Draw an Ellipse or a Circle</span></span>
<span data-ttu-id="eb470-103">この例を使用して楕円および真円を描画する方法を示しています、<xref:System.Windows.Shapes.Ellipse>要素。</span><span class="sxs-lookup"><span data-stu-id="eb470-103">This example shows how to draw ellipses and circles by using the <xref:System.Windows.Shapes.Ellipse> element.</span></span> <span data-ttu-id="eb470-104">楕円を描画するために作成、<xref:System.Windows.Shapes.Ellipse>要素を指定し、<xref:System.Windows.FrameworkElement.Width%2A>と<xref:System.Windows.FrameworkElement.Height%2A>します。</span><span class="sxs-lookup"><span data-stu-id="eb470-104">To draw an ellipse, create an <xref:System.Windows.Shapes.Ellipse> element and specify its <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A>.</span></span> <span data-ttu-id="eb470-105">使用してその<xref:System.Windows.Shapes.Shape.Fill%2A>プロパティを指定する、<xref:System.Windows.Media.Brush>楕円の内部を塗りつぶすために使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb470-105">Use its <xref:System.Windows.Shapes.Shape.Fill%2A> property to specify the <xref:System.Windows.Media.Brush> that is used to paint the interior of the ellipse.</span></span> <span data-ttu-id="eb470-106">使用してその<xref:System.Windows.Shapes.Shape.Stroke%2A>プロパティを指定する、<xref:System.Windows.Media.Brush>楕円のアウトラインを描画するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb470-106">Use its <xref:System.Windows.Shapes.Shape.Stroke%2A> property to specify the <xref:System.Windows.Media.Brush> that is used to paint the outline of the ellipse.</span></span> <span data-ttu-id="eb470-107"><xref:System.Windows.Shapes.Shape.StrokeThickness%2A>プロパティは、楕円のアウトラインの太さを指定します。</span><span class="sxs-lookup"><span data-stu-id="eb470-107">The <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> property specifies the thickness of the ellipse outline.</span></span>  
  
 <span data-ttu-id="eb470-108">円を描画するように、<xref:System.Windows.FrameworkElement.Width%2A>と<xref:System.Windows.FrameworkElement.Height%2A>の<xref:System.Windows.Shapes.Ellipse>互いに等しくない要素。</span><span class="sxs-lookup"><span data-stu-id="eb470-108">To draw a circle, make the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> of the <xref:System.Windows.Shapes.Ellipse> element equal to each other.</span></span>  
  
 <span data-ttu-id="eb470-109">次の例では、4 つを描画<xref:System.Windows.Shapes.Ellipse>内の要素を<xref:System.Windows.Controls.Canvas>します。</span><span class="sxs-lookup"><span data-stu-id="eb470-109">The following example draws four <xref:System.Windows.Shapes.Ellipse> elements within a <xref:System.Windows.Controls.Canvas>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="eb470-110">例</span><span class="sxs-lookup"><span data-stu-id="eb470-110">Example</span></span>  
 [!code-xaml[drawingwithshapeelements#EllipseExample1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/ellipseexample.xaml#ellipseexample1)]  
  
 <span data-ttu-id="eb470-111">この例を使用しますが、 <xref:System.Windows.Controls.Canvas> 、省略記号を格納することができます使用する楕円要素 (およびその他のすべての図形要素) のいずれか<xref:System.Windows.Controls.Panel>または<xref:System.Windows.Controls.Control>テキスト以外のコンテンツをサポートします。</span><span class="sxs-lookup"><span data-stu-id="eb470-111">Although this example uses a <xref:System.Windows.Controls.Canvas> to contain the ellipses, you can use ellipse elements (and all the other shape elements) with any <xref:System.Windows.Controls.Panel> or <xref:System.Windows.Controls.Control> that supports non-text content.</span></span>  
  
 <span data-ttu-id="eb470-112">この例より大きなサンプルの一部です。サンプル全体については、次を参照してください。 [Shape 要素のサンプル](https://go.microsoft.com/fwlink/?LinkID=160037)します。</span><span class="sxs-lookup"><span data-stu-id="eb470-112">This example is part of a larger sample; for the complete sample, see [Shape Elements Sample](https://go.microsoft.com/fwlink/?LinkID=160037).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb470-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb470-113">See Also</span></span>  
 <xref:System.Windows.Shapes.Ellipse>  
 <xref:System.Windows.Shapes.Shape>  
 [<span data-ttu-id="eb470-114">Shape 要素のサンプル</span><span class="sxs-lookup"><span data-stu-id="eb470-114">Shape Elements Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160037)
