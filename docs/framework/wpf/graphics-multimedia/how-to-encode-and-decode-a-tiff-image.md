---
title: '方法: TIFF イメージのエンコードおよびデコード'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TIFF encoding [WPF]
- encoding TIFF images [WPF]
- encoding image formats [WPF]
- decoding TIFF images [WPF]
- decoding image formats [WPF]
- TIFF decoding [WPF]
ms.assetid: 1dfe3209-fc73-40e6-ad1c-71c1c58b3364
ms.openlocfilehash: 0b1d5f19583e0a0014903ef6ace01bc164b70d0b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54696166"
---
# <a name="how-to-encode-and-decode-a-tiff-image"></a><span data-ttu-id="5c55e-102">方法: TIFF イメージのエンコードおよびデコード</span><span class="sxs-lookup"><span data-stu-id="5c55e-102">How to: Encode and Decode a TIFF Image</span></span>
<span data-ttu-id="5c55e-103">次の例では、デコードおよびエンコードする方法、[!INCLUDE[TLA#tla_tiff](../../../../includes/tlasharptla-tiff-md.md)]特定を使用するイメージ<xref:System.Windows.Media.Imaging.TiffBitmapDecoder>と<xref:System.Windows.Media.Imaging.TiffBitmapEncoder>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="5c55e-103">The following examples show how to decode and encode a [!INCLUDE[TLA#tla_tiff](../../../../includes/tlasharptla-tiff-md.md)] image using the specific <xref:System.Windows.Media.Imaging.TiffBitmapDecoder> and <xref:System.Windows.Media.Imaging.TiffBitmapEncoder> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5c55e-104">例</span><span class="sxs-lookup"><span data-stu-id="5c55e-104">Example</span></span>  
 <span data-ttu-id="5c55e-105">デコードする方法を示します、[!INCLUDE[TLA2#tla_tiff](../../../../includes/tla2sharptla-tiff-md.md)]イメージを使用して、<xref:System.Windows.Media.Imaging.TiffBitmapDecoder>から、<xref:System.Uri>します。</span><span class="sxs-lookup"><span data-stu-id="5c55e-105">This example demonstrates how to decode a [!INCLUDE[TLA2#tla_tiff](../../../../includes/tla2sharptla-tiff-md.md)] image using a <xref:System.Windows.Media.Imaging.TiffBitmapDecoder> from a <xref:System.Uri>.</span></span>  
  
 [!code-cpp[TiffBitmapDecoderEncoder#1](../../../../samples/snippets/cpp/VS_Snippets_Wpf/TiffBitmapDecoderEncoder/CPP/TiffEncoderDecoder.cpp#1)]
 [!code-csharp[TiffBitmapDecoderEncoder#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TiffBitmapDecoderEncoder/CSharp/TiffEncoderDecoder.cs#1)]
 [!code-vb[TiffBitmapDecoderEncoder#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TiffBitmapDecoderEncoder/VB/TiffEncoderDecoder.vb#1)]  
  
## <a name="example"></a><span data-ttu-id="5c55e-106">例</span><span class="sxs-lookup"><span data-stu-id="5c55e-106">Example</span></span>  
 <span data-ttu-id="5c55e-107">エンコードする方法を示します、<xref:System.Windows.Media.Imaging.BitmapSource>に、[!INCLUDE[TLA2#tla_tiff](../../../../includes/tla2sharptla-tiff-md.md)]イメージを使用して、<xref:System.Windows.Media.Imaging.TiffBitmapEncoder>します。</span><span class="sxs-lookup"><span data-stu-id="5c55e-107">This example demonstrates how to encode a <xref:System.Windows.Media.Imaging.BitmapSource> into a [!INCLUDE[TLA2#tla_tiff](../../../../includes/tla2sharptla-tiff-md.md)] image using a <xref:System.Windows.Media.Imaging.TiffBitmapEncoder>.</span></span>  
  
 [!code-cpp[TiffBitmapDecoderEncoder#4](../../../../samples/snippets/cpp/VS_Snippets_Wpf/TiffBitmapDecoderEncoder/CPP/TiffEncoderDecoder.cpp#4)]
 [!code-csharp[TiffBitmapDecoderEncoder#4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TiffBitmapDecoderEncoder/CSharp/TiffEncoderDecoder.cs#4)]
 [!code-vb[TiffBitmapDecoderEncoder#4](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TiffBitmapDecoderEncoder/VB/TiffEncoderDecoder.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="5c55e-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c55e-108">See also</span></span>
- [<span data-ttu-id="5c55e-109">イメージングの概要</span><span class="sxs-lookup"><span data-stu-id="5c55e-109">Imaging Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)
