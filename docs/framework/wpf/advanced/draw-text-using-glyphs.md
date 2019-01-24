---
title: グリフを使用したテキストの描画
ms.date: 03/30/2017
helpviewer_keywords:
- text [WPF], drawing with Glyphs objects
- Glyphs objects [WPF], drawing text
- typography [WPF], Glyphs objects
ms.assetid: 587ab17e-a419-4ad5-b6da-8933a8e83d97
ms.openlocfilehash: 7c7c4946d2c5cc2aa9001cf119b969dd375a1050
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54680245"
---
# <a name="draw-text-using-glyphs"></a>グリフを使用したテキストの描画
このトピックでは、低レベルを使用する方法を説明します<xref:System.Windows.Documents.Glyphs>内のテキストを表示するオブジェクト[!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]します。  
  
## <a name="example"></a>例  
 次の例のプロパティを定義する方法を示して、<xref:System.Windows.Documents.Glyphs>オブジェクト[!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]します。 <xref:System.Windows.Documents.Glyphs>オブジェクトの出力を表して、<xref:System.Windows.Media.GlyphRun>で[!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]します。 この例では、Arial、Courier New、Times New Roman フォントがローカル コンピューターの C:\WINDOWS\Fonts フォルダーにインストールされていると想定しています。  
  
 [!code-xaml[GlyphsOvwSample1#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GlyphsOvwSample1/CS/default.xaml#1)]  
  
 この例は、その他のプロパティを定義する方法を示します<xref:System.Windows.Documents.Glyphs>オブジェクト[!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]します。  
  
 [!code-xaml[GlyphsOvwSamp2#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GlyphsOvwSamp2/CS/default.xaml#1)]  
  
## <a name="see-also"></a>関連項目
- [WPF のタイポグラフィ](../../../../docs/framework/wpf/advanced/typography-in-wpf.md)
