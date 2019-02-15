---
title: '方法: 四角形をアニメーション化する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], rectangles
- rectangles [WPF], animating
ms.assetid: 572ffb95-790d-4ace-adbf-b2ea8a90e75b
ms.openlocfilehash: dbff015bdc5f9ce56d2c366e0d348429efb7f4b5
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2019
ms.locfileid: "56305156"
---
# <a name="how-to-animate-a-rectangle"></a><span data-ttu-id="1e009-102">方法: 四角形をアニメーション化する</span><span class="sxs-lookup"><span data-stu-id="1e009-102">How to: Animate a Rectangle</span></span>
<span data-ttu-id="1e009-103">この例では、四角形のサイズと位置の変化をアニメーション化する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1e009-103">This example shows how to animate changes to the size and position of a rectangle.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1e009-104">例</span><span class="sxs-lookup"><span data-stu-id="1e009-104">Example</span></span>  
 <span data-ttu-id="1e009-105">次の例のインスタンスを使用して、<xref:System.Windows.Media.Animation.RectAnimation>をアニメーション化するクラス、<xref:System.Windows.Media.RectangleGeometry.Rect%2A>のプロパティを<xref:System.Windows.Media.RectangleGeometry>、四角形の位置とサイズの変更をアニメーション化します。</span><span class="sxs-lookup"><span data-stu-id="1e009-105">The following example uses an instance of the <xref:System.Windows.Media.Animation.RectAnimation> class to animate the <xref:System.Windows.Media.RectangleGeometry.Rect%2A> property of a <xref:System.Windows.Media.RectangleGeometry>, which animates changes to the size and position of the rectangle.</span></span>  
  
 [!code-csharp[BasicAnimations_snip#RectAnimationWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/RectAnimationExample.cs#rectanimationwholepage)]
 [!code-vb[BasicAnimations_snip#RectAnimationWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/RectAnimationExample.vb#rectanimationwholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="1e009-106">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e009-106">See also</span></span>
- <xref:System.Windows.Media.Animation.RectAnimation>
- <xref:System.Windows.Media.RectangleGeometry.Rect%2A>
- <xref:System.Windows.Media.RectangleGeometry>
- [<span data-ttu-id="1e009-107">アニメーションの概要</span><span class="sxs-lookup"><span data-stu-id="1e009-107">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [<span data-ttu-id="1e009-108">グラフィックスとマルチメディア</span><span class="sxs-lookup"><span data-stu-id="1e009-108">Graphics and Multimedia</span></span>](../../../../docs/framework/wpf/graphics-multimedia/index.md)
- [<span data-ttu-id="1e009-109">グラフィックスの操作方法に関するトピック</span><span class="sxs-lookup"><span data-stu-id="1e009-109">Graphics How-to Topics</span></span>](graphics-how-to-topics.md)
- [<span data-ttu-id="1e009-110">アニメーションとタイミングに関するトピック</span><span class="sxs-lookup"><span data-stu-id="1e009-110">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
