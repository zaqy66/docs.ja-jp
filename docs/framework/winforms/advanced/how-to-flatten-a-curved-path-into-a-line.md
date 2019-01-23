---
title: '方法: 行に曲線のパスをフラット化します。'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], flattening curves into lines
- curves [Windows Forms], flattening
- GraphicsPath object
- paths [Windows Forms], flattening
- drawing [Windows Forms], flattening curves
ms.assetid: e654b8de-25f4-4735-9208-42e4514a589c
ms.openlocfilehash: aa47a655417cdf82d79fb222dc6ff6f6d8c3a947
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54601819"
---
# <a name="how-to-flatten-a-curved-path-into-a-line"></a><span data-ttu-id="9c2c4-102">方法: 行に曲線のパスをフラット化します。</span><span class="sxs-lookup"><span data-stu-id="9c2c4-102">How to: Flatten a Curved Path into a Line</span></span>
<span data-ttu-id="9c2c4-103">A<xref:System.Drawing.Drawing2D.GraphicsPath>オブジェクトは、一連の行とベジエ スプラインを格納します。</span><span class="sxs-lookup"><span data-stu-id="9c2c4-103">A <xref:System.Drawing.Drawing2D.GraphicsPath> object stores a sequence of lines and Bézier splines.</span></span> <span data-ttu-id="9c2c4-104">パスに曲線 (省略記号、円弧、カーディナル スプライン) のいくつかの種類を追加できますが、パスに格納する前に、各曲線がベジエ スプラインに変換されます。</span><span class="sxs-lookup"><span data-stu-id="9c2c4-104">You can add several types of curves (ellipses, arcs, cardinal splines) to a path, but each curve is converted to a Bézier spline before it is stored in the path.</span></span> <span data-ttu-id="9c2c4-105">パスをフラット化は、パス内の各本のベジエ スプラインを一連の直線に変換するので構成されます。</span><span class="sxs-lookup"><span data-stu-id="9c2c4-105">Flattening a path consists of converting each Bézier spline in the path to a sequence of straight lines.</span></span> <span data-ttu-id="9c2c4-106">次の図は前に、とフラット化した後にパスを示します。</span><span class="sxs-lookup"><span data-stu-id="9c2c4-106">The following illustration shows a path before and after flattening.</span></span>  
  
 <span data-ttu-id="9c2c4-107">![直線と曲線](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art32a.gif "AboutGdip02_Art32A")</span><span class="sxs-lookup"><span data-stu-id="9c2c4-107">![Straight Lines and Curves](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art32a.gif "AboutGdip02_Art32A")</span></span>  
  
### <a name="to-flatten-a-path"></a><span data-ttu-id="9c2c4-108">パスをフラット化するには</span><span class="sxs-lookup"><span data-stu-id="9c2c4-108">To Flatten a Path</span></span>  
  
-   <span data-ttu-id="9c2c4-109">呼び出す、<xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A>のメソッドを<xref:System.Drawing.Drawing2D.GraphicsPath>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="9c2c4-109">call the <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> method of a <xref:System.Drawing.Drawing2D.GraphicsPath> object.</span></span> <span data-ttu-id="9c2c4-110"><xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A>メソッドは、フラット化されたパスと元のパスの最大距離を指定する平坦度引数を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="9c2c4-110">The <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> method receives a flatness argument that specifies the maximum distance between the flattened path and the original path.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c2c4-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c2c4-111">See also</span></span>
- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- [<span data-ttu-id="9c2c4-112">直線、曲線、および図形</span><span class="sxs-lookup"><span data-stu-id="9c2c4-112">Lines, Curves, and Shapes</span></span>](../../../../docs/framework/winforms/advanced/lines-curves-and-shapes.md)
- [<span data-ttu-id="9c2c4-113">パスの作成および描画</span><span class="sxs-lookup"><span data-stu-id="9c2c4-113">Constructing and Drawing Paths</span></span>](../../../../docs/framework/winforms/advanced/constructing-and-drawing-paths.md)
