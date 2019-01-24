---
title: '方法: ビジュアルをイメージ ファイルにエンコードする'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image files [WPF], encoding from visuals
- encoding image formats [WPF]
- visuals [WPF], encoding to an image file
ms.assetid: 2036385b-ea47-4d54-8027-5797f52c8149
ms.openlocfilehash: e8988256d4b7181c5e1af12252ca26e0248d016f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54645224"
---
# <a name="how-to-encode-a-visual-to-an-image-file"></a><span data-ttu-id="dc028-102">方法: ビジュアルをイメージ ファイルにエンコードする</span><span class="sxs-lookup"><span data-stu-id="dc028-102">How to: Encode a Visual to an Image File</span></span>
<span data-ttu-id="dc028-103">エンコードする方法を示します、<xref:System.Windows.Media.Visual>オブジェクトを使用してイメージ ファイルに、<xref:System.Windows.Media.Imaging.RenderTargetBitmap>と<xref:System.Windows.Media.Imaging.PngBitmapEncoder>します。</span><span class="sxs-lookup"><span data-stu-id="dc028-103">This example demonstrates how to encode a <xref:System.Windows.Media.Visual> object into an image file using a <xref:System.Windows.Media.Imaging.RenderTargetBitmap> and a <xref:System.Windows.Media.Imaging.PngBitmapEncoder>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dc028-104">例</span><span class="sxs-lookup"><span data-stu-id="dc028-104">Example</span></span>  
 <span data-ttu-id="dc028-105"><xref:System.Windows.Media.DrawingVisual>を使用して作成されて、<xref:System.Windows.Media.Imaging.BitmapImage>と<xref:System.Windows.Media.FormattedText>にレンダリングされる、<xref:System.Windows.Media.Imaging.RenderTargetBitmap>します。</span><span class="sxs-lookup"><span data-stu-id="dc028-105">The <xref:System.Windows.Media.DrawingVisual> is created using a <xref:System.Windows.Media.Imaging.BitmapImage> and <xref:System.Windows.Media.FormattedText> which is rendered to a <xref:System.Windows.Media.Imaging.RenderTargetBitmap>.</span></span> <span data-ttu-id="dc028-106">レンダリングされたビットマップが作成に使用し、<xref:System.Windows.Media.Imaging.BitmapFrame>に追加されます、<xref:System.Windows.Media.Imaging.PngBitmapEncoder>新たに作成する[!INCLUDE[TLA#tla_png](../../../../includes/tlasharptla-png-md.md)]ファイル。</span><span class="sxs-lookup"><span data-stu-id="dc028-106">The rendered bitmap is then used to create a <xref:System.Windows.Media.Imaging.BitmapFrame> which is added to the <xref:System.Windows.Media.Imaging.PngBitmapEncoder> to create a new [!INCLUDE[TLA#tla_png](../../../../includes/tlasharptla-png-md.md)] file.</span></span>  
  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#RTBEncodeInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample_Encode.cs#rtbencodeinline1)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#RTBEncodeInline1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample_Encode.vb#rtbencodeinline1)]  
  
 <span data-ttu-id="dc028-107">A<xref:System.Windows.Media.Imaging.PngBitmapEncoder>でこの例では、派生のいずれかが使用されていた<xref:System.Windows.Media.Imaging.BitmapEncoder>オブジェクトが、イメージ ファイルの作成に使用されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dc028-107">A <xref:System.Windows.Media.Imaging.PngBitmapEncoder> was used in this example but any of the derived <xref:System.Windows.Media.Imaging.BitmapEncoder> objects could have been used to create the image file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc028-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc028-108">See also</span></span>
- <xref:System.Windows.Media.DrawingContext>
- [<span data-ttu-id="dc028-109">イメージングの概要</span><span class="sxs-lookup"><span data-stu-id="dc028-109">Imaging Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)
- [<span data-ttu-id="dc028-110">Drawing オブジェクトの概要</span><span class="sxs-lookup"><span data-stu-id="dc028-110">Drawing Objects Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)
- [<span data-ttu-id="dc028-111">DrawingVisual オブジェクトの使用</span><span class="sxs-lookup"><span data-stu-id="dc028-111">Using DrawingVisual Objects</span></span>](../../../../docs/framework/wpf/graphics-multimedia/using-drawingvisual-objects.md)
