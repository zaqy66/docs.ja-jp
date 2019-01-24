---
title: '方法: 要素を変換する'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], translations
ms.assetid: 461c8273-15df-42f6-8672-89ba22887cc0
ms.openlocfilehash: 75b8f72647b1597396fde5d21f8378d3ce586a25
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672874"
---
# <a name="how-to-translate-an-element"></a>方法: 要素を変換する
この例では変換 (移動) に要素を使用して、<xref:System.Windows.Media.TranslateTransform>します。  
  
 <xref:System.Windows.Media.TranslateTransform>クラスは、絶対配置をサポートしていないパネル内の要素を移動するために特に便利です。 適用することなどによって、<xref:System.Windows.Media.TranslateTransform>を<xref:System.Windows.UIElement.RenderTransform%2A>要素のプロパティ内の要素を移動することができます、<xref:System.Windows.Controls.StackPanel>または<xref:System.Windows.Controls.DockPanel>。  
  
 使用して、<xref:System.Windows.Media.TranslateTransform.X%2A>のプロパティ、<xref:System.Windows.Media.TranslateTransform>要素を x 軸に沿って移動させるピクセル単位で、時間を指定します。 使用して、<xref:System.Windows.Media.TranslateTransform.Y%2A>プロパティ要素を y 軸に沿って移動させるピクセル単位で、時間を指定します。 最後に、適用、<xref:System.Windows.Media.TranslateTransform>を<xref:System.Windows.UIElement.RenderTransform%2A>要素のプロパティ。  
  
 次の例では、<xref:System.Windows.Media.TranslateTransform>下に移動する要素を 50 ピクセル右方向と 50 ピクセルにします。  
  
## <a name="example"></a>例  
 [!code-xaml[transformsSample#53](../../../../samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/TranslateTransformExample.xaml#53)]  
  
 完全なサンプルについては、「[2-D 変換のサンプル](https://go.microsoft.com/fwlink/?LinkID=158252)」をご覧ください。  
  
## <a name="see-also"></a>関連項目
- [変換の概要](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
