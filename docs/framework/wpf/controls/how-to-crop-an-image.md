---
title: '方法 : イメージをトリミングする'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [WPF], cropping
- cropping images [WPF]
ms.assetid: c6bba109-c6e7-4cf8-bfe6-9cf8d01bb4fc
ms.openlocfilehash: 189cb92d581ccc9209ebdb4de18487951d17818a
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43406305"
---
# <a name="how-to-crop-an-image"></a>方法 : イメージをトリミングする
この例を使用して、イメージをトリミングする方法を示しています。<xref:System.Windows.Media.Imaging.CroppedBitmap>します。  
  
 <xref:System.Windows.Media.Imaging.CroppedBitmap> 主に使用トリミング後のバージョンのイメージをエンコードする際にファイルを保存します。 表示目的でを参照してください。 イメージをトリミングするには、[クリップ領域を作成する](https://msdn.microsoft.com/library/56e4bed6-78d7-4292-b917-d72d0b3e4376)トピック。  
  
## <a name="example"></a>例  
 次[!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]以下のサンプル内で使用されるリソースを定義します。  
  
 [!code-xaml[imageelementexample#CroppedXAML1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml1)]  
  
 次の例を使用して、イメージを作成、<xref:System.Windows.Media.Imaging.CroppedBitmap>のソースとして。  
  
 [!code-xaml[imageelementexample#CroppedXAML2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml2)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp1)]
 [!code-vb[imageelementexample#CroppedCSharp1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp1)]  
  
 <xref:System.Windows.Media.Imaging.CroppedBitmap>別のソースとしても使用できます<xref:System.Windows.Media.Imaging.CroppedBitmap>、トリミングの組み合わせ。 なお、<xref:System.Windows.Media.Imaging.CroppedBitmap.SourceRect%2A>値は、トリミング ビットマップと初期イメージではなくソースを使用します。  
  
 [!code-xaml[imageelementexample#CroppedXAML3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml3)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp2)]
 [!code-vb[imageelementexample#CroppedCSharp2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp2)]  
  
## <a name="see-also"></a>関連項目  
 [クリップ領域を作成します。](https://msdn.microsoft.com/library/56e4bed6-78d7-4292-b917-d72d0b3e4376)
