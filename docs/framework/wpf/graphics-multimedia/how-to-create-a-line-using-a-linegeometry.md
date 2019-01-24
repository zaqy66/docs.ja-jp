---
title: '方法: LineGeometry を使用して線を作成する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], lines
ms.assetid: 41231b22-1f74-4c26-a8e7-a55b29f8f6bd
ms.openlocfilehash: fbf44f627ede0fe3bdf7e629728a1e3b858fd30e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54690567"
---
# <a name="how-to-create-a-line-using-a-linegeometry"></a>方法: LineGeometry を使用して線を作成する
この例は、使用する方法を示します、<xref:System.Windows.Media.LineGeometry>行を記述するクラス。 A<xref:System.Windows.Media.LineGeometry>の始点と終点で定義されます。  
  
## <a name="example"></a>例  
 次の例を作成してレンダリングする方法を示しています、<xref:System.Windows.Media.LineGeometry>します。  A<xref:System.Windows.Shapes.Path>要素は、行を表示するために使用します。  行に領域があるないので、<xref:System.Windows.Shapes.Path>オブジェクトの<xref:System.Windows.Shapes.Shape.Fill%2A>が指定されていません; 代わりに、<xref:System.Windows.Shapes.Shape.Stroke%2A>と<xref:System.Windows.Shapes.Shape.StrokeThickness%2A>プロパティを使用します。  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMLineGeometryExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmlinegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmlinegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmlinegeometryexample)]  
  
 ![LineGeometry](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-line.gif "graphicsmm_line")  
(10,20) から (100,130) まで描画された LineGeometry  
  
 その他の単純なジオメトリ クラス<xref:System.Windows.Media.LineGeometry>と<xref:System.Windows.Media.EllipseGeometry>します。 複雑なものと同様にこれらのジオメトリを作成することもを使用して、<xref:System.Windows.Media.PathGeometry>または<xref:System.Windows.Media.StreamGeometry>します。 詳細については、次を参照してください。、[ジオメトリの概要](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md)します。  
  
## <a name="see-also"></a>関連項目
- [ジオメトリの概要](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md)
- [複合図形を作成する](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-composite-shape.md)
- [PathGeometry を使用して図形を作成する](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-shape-by-using-a-pathgeometry.md)
