---
title: '方法 : パスに沿ってオブジェクトをアニメーション化する (ダブル アニメーション)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (double animation)
- double animation [WPF]
ms.assetid: 5a3c4a99-f303-42ad-a52a-e4794bb1798e
ms.openlocfilehash: 3dcdf6cfe8631ae0b7b1472e22d027cf9288a1db
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43386223"
---
# <a name="how-to-animate-an-object-along-a-path-double-animation"></a><span data-ttu-id="3ec1c-102">方法 : パスに沿ってオブジェクトをアニメーション化する (ダブル アニメーション)</span><span class="sxs-lookup"><span data-stu-id="3ec1c-102">How to: Animate an Object Along a Path (Double Animation)</span></span>
<span data-ttu-id="3ec1c-103">この例は、使用する方法を示します、<xref:System.Windows.Media.Animation.DoubleAnimationUsingPath>クラスによって定義されたパスに沿ってオブジェクトを移動する、<xref:System.Windows.Media.PathGeometry>します。</span><span class="sxs-lookup"><span data-stu-id="3ec1c-103">This example shows how to use the <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> class to move an object along a path defined by a <xref:System.Windows.Media.PathGeometry>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3ec1c-104">例</span><span class="sxs-lookup"><span data-stu-id="3ec1c-104">Example</span></span>  
 <span data-ttu-id="3ec1c-105">次の例を使用して 2 つ<xref:System.Windows.Media.Animation.DoubleAnimationUsingPath>四角形をジオメトリ パスに沿って移動するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="3ec1c-105">The following example uses two <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> objects to move a rectangle along a geometric path:</span></span>  
  
-   <span data-ttu-id="3ec1c-106">最初の<xref:System.Windows.Media.Animation.DoubleAnimationUsingPath>をアニメーション化、<xref:System.Windows.Media.TranslateTransform.X%2A>の<xref:System.Windows.Media.TranslateTransform>四角形に適用します。</span><span class="sxs-lookup"><span data-stu-id="3ec1c-106">The first <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> animates the <xref:System.Windows.Media.TranslateTransform.X%2A> of the <xref:System.Windows.Media.TranslateTransform> applied to the rectangle.</span></span> <span data-ttu-id="3ec1c-107">これにより、四角形がパスに沿って水平に移動します。</span><span class="sxs-lookup"><span data-stu-id="3ec1c-107">It makes the rectangle move horizontally along the path.</span></span>  
  
-   <span data-ttu-id="3ec1c-108">2 番目の<xref:System.Windows.Media.Animation.DoubleAnimationUsingPath>をアニメーション化、<xref:System.Windows.Media.TranslateTransform.Y%2A>の<xref:System.Windows.Media.TranslateTransform>四角形に適用します。</span><span class="sxs-lookup"><span data-stu-id="3ec1c-108">The second <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> animates the <xref:System.Windows.Media.TranslateTransform.Y%2A> of the <xref:System.Windows.Media.TranslateTransform> applied to the rectangle.</span></span> <span data-ttu-id="3ec1c-109">これにより、四角形がパスに沿って垂直に移動します。</span><span class="sxs-lookup"><span data-stu-id="3ec1c-109">It makes the rectangle move vertically along the path.</span></span>  
  
 [!code-xaml[PathAnimationGallery_snippet#DoubleAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/doubleanimationusingpathexample.xaml#doubleanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#DoubleAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/DoubleAnimationUsingPathExample.cs#doubleanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#DoubleAnimationUsingPathWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/DoubleAnimationUsingPathExample.vb#doubleanimationusingpathwholepage)]  
  
 <span data-ttu-id="3ec1c-110">サンプル全体については、次を参照してください。[パス アニメーションのサンプル](https://go.microsoft.com/fwlink/?LinkID=160028)します。</span><span class="sxs-lookup"><span data-stu-id="3ec1c-110">For the complete sample, see [Path Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160028).</span></span>  
  
 <span data-ttu-id="3ec1c-111">ジオメトリック パスを使用してオブジェクトを移動することもできますが、使用する、<xref:System.Windows.Media.Animation.MatrixAnimationUsingPath>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="3ec1c-111">Another way to move an object using a geometric path is to use a <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> object.</span></span> <span data-ttu-id="3ec1c-112">例については、次を参照してください。 [、オブジェクト パスに沿って (行列アニメーション) をアニメーション化する](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-an-object-along-a-path-matrix-animation.md)します。</span><span class="sxs-lookup"><span data-stu-id="3ec1c-112">For an example, see [Animate an Object Along a Path (Matrix Animation)](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-an-object-along-a-path-matrix-animation.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ec1c-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ec1c-113">See Also</span></span>  
 [<span data-ttu-id="3ec1c-114">アニメーションの概要</span><span class="sxs-lookup"><span data-stu-id="3ec1c-114">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [<span data-ttu-id="3ec1c-115">パス アニメーションに関する「方法」トピック</span><span class="sxs-lookup"><span data-stu-id="3ec1c-115">Path Animation How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/path-animation-how-to-topics.md)
