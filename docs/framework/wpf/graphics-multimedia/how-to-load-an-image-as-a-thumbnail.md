---
title: '方法: サムネイルとしてイメージを読み込む'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- loading images as thumbnails [WPF]
- images [WPF], loading as thumbnails
- thumbnails [WPF], loading images as
ms.assetid: 02e055a0-54df-499a-b8b6-ab6ff7535cff
ms.openlocfilehash: d92a489f19f8c7160bed5ec83535bdc33cfe561b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54735988"
---
# <a name="how-to-load-an-image-as-a-thumbnail"></a>方法: サムネイルとしてイメージを読み込む
次の例を読み込む方法を示して、<xref:System.Windows.Controls.Image>アプリケーション メモリを節約するサムネイルとして。  
  
## <a name="example"></a>例  
 次の例のセット、<xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A>のプロパティを<xref:System.Windows.Media.Imaging.BitmapImage>で[!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]イメージの読み込みに必要なメモリを削減します。  
  
 [!code-xaml[ImageElementExample_snip#ImageSimpleExampleInlineMarkup](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml#imagesimpleexampleinlinemarkup)]  
  
## <a name="example"></a>例  
 次の例のセット、<xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A>のプロパティを<xref:System.Windows.Media.Imaging.BitmapImage>コードに、イメージの読み込みに必要なメモリ量を減らします。  
  
 [!code-csharp[ImageElementExample_snip#ImageSimpleExampleInlineCode1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml.cs#imagesimpleexampleinlinecode1)]
 [!code-vb[ImageElementExample_snip#ImageSimpleExampleInlineCode1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample_snip/VB/ImageSimpleExample.xaml.vb#imagesimpleexampleinlinecode1)]  
  
## <a name="see-also"></a>関連項目
- [イメージングの概要](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)
