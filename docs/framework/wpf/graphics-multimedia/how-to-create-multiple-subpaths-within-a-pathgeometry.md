---
title: '方法: PathGeometry 内に複数のサブパスを作成する'
ms.date: 03/30/2017
helpviewer_keywords:
- multiple subpaths [WPF]
- graphics [WPF], subpaths
- subpaths [WPF]
ms.assetid: 104a862c-dde2-4e62-ac87-80660dd1681c
ms.openlocfilehash: d7b3d24f8d947d342a2af5484a6620c8379ac664
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54638354"
---
# <a name="how-to-create-multiple-subpaths-within-a-pathgeometry"></a><span data-ttu-id="4110c-102">方法: PathGeometry 内に複数のサブパスを作成する</span><span class="sxs-lookup"><span data-stu-id="4110c-102">How to: Create Multiple Subpaths Within a PathGeometry</span></span>
<span data-ttu-id="4110c-103">この例で複数のサブパスを作成する方法を示しています、<xref:System.Windows.Media.PathGeometry>します。</span><span class="sxs-lookup"><span data-stu-id="4110c-103">This example shows how to create multiple subpaths in a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="4110c-104">作成する複数のサブパスを作成する、<xref:System.Windows.Media.PathFigure>各サブパスにします。</span><span class="sxs-lookup"><span data-stu-id="4110c-104">To create multiple subpaths, you create a <xref:System.Windows.Media.PathFigure> for each subpath.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4110c-105">例</span><span class="sxs-lookup"><span data-stu-id="4110c-105">Example</span></span>  
 <span data-ttu-id="4110c-106">次の例は、三角形が 1 つずつ、2 つのサブパスを作成します。</span><span class="sxs-lookup"><span data-stu-id="4110c-106">The following example creates two subpaths, each one a triangle.</span></span>  
  
 [!code-xaml[GeometrySample#38](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#38)]  
  
 <span data-ttu-id="4110c-107">次の例を使用して複数のサブパスを作成する方法を示しています、<xref:System.Windows.Shapes.Path>と[!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]属性構文。</span><span class="sxs-lookup"><span data-stu-id="4110c-107">The following example shows how to create multiple subpaths by using a <xref:System.Windows.Shapes.Path> and [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] attribute syntax.</span></span> <span data-ttu-id="4110c-108">各`M`例は、各三角形を描画しないこと、2 つのサブパスを作成できるように、新しいサブパスを作成します。</span><span class="sxs-lookup"><span data-stu-id="4110c-108">Each `M` creates a new subpath so that the example creates two subpaths that each draw a triangle.</span></span>  
  
 [!code-xaml[GeometrySample#58](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/geometryattributesyntaxexample.xaml#58)]  
  
 <span data-ttu-id="4110c-109">(この属性の構文が実際に作成するメモを<xref:System.Windows.Media.StreamGeometry>の軽量バージョンを<xref:System.Windows.Media.PathGeometry>します。</span><span class="sxs-lookup"><span data-stu-id="4110c-109">(Note that this attribute syntax actually creates a <xref:System.Windows.Media.StreamGeometry>, a lighter-weight version of a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="4110c-110">詳細については、「[パス マークアップ構文](../../../../docs/framework/wpf/graphics-multimedia/path-markup-syntax.md)」のページを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="4110c-110">For more information, see the [Path Markup Syntax](../../../../docs/framework/wpf/graphics-multimedia/path-markup-syntax.md) page.)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4110c-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="4110c-111">See also</span></span>
- [<span data-ttu-id="4110c-112">ジオメトリの概要</span><span class="sxs-lookup"><span data-stu-id="4110c-112">Geometry Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md)
