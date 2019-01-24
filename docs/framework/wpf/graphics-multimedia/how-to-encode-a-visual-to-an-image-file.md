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
# <a name="how-to-encode-a-visual-to-an-image-file"></a>方法: ビジュアルをイメージ ファイルにエンコードする
エンコードする方法を示します、<xref:System.Windows.Media.Visual>オブジェクトを使用してイメージ ファイルに、<xref:System.Windows.Media.Imaging.RenderTargetBitmap>と<xref:System.Windows.Media.Imaging.PngBitmapEncoder>します。  
  
## <a name="example"></a>例  
 <xref:System.Windows.Media.DrawingVisual>を使用して作成されて、<xref:System.Windows.Media.Imaging.BitmapImage>と<xref:System.Windows.Media.FormattedText>にレンダリングされる、<xref:System.Windows.Media.Imaging.RenderTargetBitmap>します。 レンダリングされたビットマップが作成に使用し、<xref:System.Windows.Media.Imaging.BitmapFrame>に追加されます、<xref:System.Windows.Media.Imaging.PngBitmapEncoder>新たに作成する[!INCLUDE[TLA#tla_png](../../../../includes/tlasharptla-png-md.md)]ファイル。  
  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#RTBEncodeInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample_Encode.cs#rtbencodeinline1)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#RTBEncodeInline1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample_Encode.vb#rtbencodeinline1)]  
  
 A<xref:System.Windows.Media.Imaging.PngBitmapEncoder>でこの例では、派生のいずれかが使用されていた<xref:System.Windows.Media.Imaging.BitmapEncoder>オブジェクトが、イメージ ファイルの作成に使用されている可能性があります。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Media.DrawingContext>
- [イメージングの概要](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)
- [Drawing オブジェクトの概要](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)
- [DrawingVisual オブジェクトの使用](../../../../docs/framework/wpf/graphics-multimedia/using-drawingvisual-objects.md)
