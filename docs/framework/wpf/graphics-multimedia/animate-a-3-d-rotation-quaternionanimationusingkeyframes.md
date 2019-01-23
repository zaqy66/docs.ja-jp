---
title: '方法: キー フレーム (QuaternionAnimationUsingKeyFrames) を使用して 3-D 回転をアニメーション化する'
ms.date: 03/30/2017
helpviewer_keywords:
- 3-D translations [WPF], animating [WPF], with key frames (QuaternionAnimationUsingKeyFrames)
- key frames [WPF], QuaternionAnimationUsingKeyFrames
- animation [WPF], 3-D translations [WPF], with key frames (QuaternionAnimationUsingKeyFrames)
ms.assetid: 09e5707b-7523-4a08-9aa7-bb13cbedccdf
ms.openlocfilehash: 6cb58c2ed97cad1539f3703c98b9af57b0af22fb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54637717"
---
# <a name="how-to-animate-a-3-d-rotation-using-key-frames-quaternionanimationusingkeyframes"></a><span data-ttu-id="8b27e-102">方法: キー フレーム (QuaternionAnimationUsingKeyFrames) を使用して 3-D 回転をアニメーション化する</span><span class="sxs-lookup"><span data-stu-id="8b27e-102">How to: Animate a 3-D Rotation Using Key Frames (QuaternionAnimationUsingKeyFrames)</span></span>
<span data-ttu-id="8b27e-103">次の例では、<xref:System.Windows.Media.Animation.QuaternionAnimationUsingKeyFrames>回転 3D オブジェクトを作成するために使用します。</span><span class="sxs-lookup"><span data-stu-id="8b27e-103">In the following example, <xref:System.Windows.Media.Animation.QuaternionAnimationUsingKeyFrames> is used to make a 3D object rotate.</span></span> <span data-ttu-id="8b27e-104">このアニメーションは、次のキー フレームを使用します。</span><span class="sxs-lookup"><span data-stu-id="8b27e-104">This animation uses the following key frames:</span></span>  
  
1.  <span data-ttu-id="8b27e-105"><xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> 作成する滑らかな線形補間値の間に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b27e-105"><xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> is used to create a smooth, linear interpolation between values.</span></span>  
  
2.  <span data-ttu-id="8b27e-106"><xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> (補間) の値の間で突然「ジャンプ」の作成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b27e-106"><xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> is used to create sudden "jumps" between values (no interpolation).</span></span>  
  
3.  <span data-ttu-id="8b27e-107"><xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> によって値の間に可変遷移を作成するために使用、<xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="8b27e-107"><xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> is used to create a variable transition between values depending on the <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="8b27e-108">次の例で、アニメーションのこの部分は低速と始まりますが、時間セグメントの末尾に向かって、急激に速くなります。</span><span class="sxs-lookup"><span data-stu-id="8b27e-108">In the example below, this part of the animation starts off slow but toward the end of the time segment, speeds up exponentially.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8b27e-109">例</span><span class="sxs-lookup"><span data-stu-id="8b27e-109">Example</span></span>  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationUsingKeyFramesExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationUsingKeyFramesExample.xaml#quaternionanimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="8b27e-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="8b27e-110">See also</span></span>
- [<span data-ttu-id="8b27e-111">ストーリーボードを使用して 3-D 回転をアニメーション化する</span><span class="sxs-lookup"><span data-stu-id="8b27e-111">Animate a 3-D Rotation Using Storyboards</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-3-d-rotation-using-storyboards.md)
- [<span data-ttu-id="8b27e-112">Rotation3DAnimation を使用して 3-D 回転をアニメーション化する</span><span class="sxs-lookup"><span data-stu-id="8b27e-112">Animate a 3-D Rotation Using Rotation3DAnimation</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
- [<span data-ttu-id="8b27e-113">四元数を使用して 3-D 回転をアニメーション化する</span><span class="sxs-lookup"><span data-stu-id="8b27e-113">Animate a 3-D Rotation Using Quaternions</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-3-d-rotation-using-quaternions.md)
- [<span data-ttu-id="8b27e-114">キー フレーム (Rotation3DAnimationUsingKeyFrames) を使用して 3-D 回転をアニメーション化する</span><span class="sxs-lookup"><span data-stu-id="8b27e-114">Animate a 3-D Rotation Using Key Frames (Rotation3DAnimationUsingKeyFrames)</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-3-d-rotation-using-key-frames.md)
- [<span data-ttu-id="8b27e-115">3-D グラフィックスの概要</span><span class="sxs-lookup"><span data-stu-id="8b27e-115">3-D Graphics Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)
- [<span data-ttu-id="8b27e-116">キー フレーム アニメーションの概要</span><span class="sxs-lookup"><span data-stu-id="8b27e-116">Key-Frame Animations Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)
