---
title: '方法: キー フレームを使用して文字列をアニメーション化する'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], strings with key frames
- strings [WPF], animating with key frames
- key frames [WPF], animating strings with
ms.assetid: c62bc9fd-c09a-4227-bce0-0a1ab82049dd
ms.openlocfilehash: 4cadc1e7e4b7ee70e3a71ddaf433327a7561125d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54670834"
---
# <a name="how-to-animate-a-string-by-using-key-frames"></a><span data-ttu-id="f8841-102">方法: キー フレームを使用して文字列をアニメーション化する</span><span class="sxs-lookup"><span data-stu-id="f8841-102">How to: Animate a String by Using Key Frames</span></span>
<span data-ttu-id="f8841-103">この例があり、この例では、文字列をアニメーション化する方法を示しています、<xref:System.Windows.Controls.ContentControl.Content%2A>のプロパティを<xref:System.Windows.Controls.Button>キー フレームを使用して、コントロール。</span><span class="sxs-lookup"><span data-stu-id="f8841-103">This example shows how to animate a string, which in this example is the <xref:System.Windows.Controls.ContentControl.Content%2A> property of a <xref:System.Windows.Controls.Button> control, by using key frames.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f8841-104">例</span><span class="sxs-lookup"><span data-stu-id="f8841-104">Example</span></span>  
 <span data-ttu-id="f8841-105">次の例では、<xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames>をアニメーション化するクラス、<xref:System.Windows.Controls.ContentControl.Content%2A>のプロパティを<xref:System.Windows.Controls.Button>します。</span><span class="sxs-lookup"><span data-stu-id="f8841-105">The following example uses the <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Controls.ContentControl.Content%2A> property of a <xref:System.Windows.Controls.Button>.</span></span>  
  
 <span data-ttu-id="f8841-106">この例ではすべてのキー フレームのインスタンスを使用して、<xref:System.Windows.Media.Animation.DiscreteStringKeyFrame>クラスをキー フレームで作成される文字列のアニメーションは不連続のキー フレームのみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8841-106">All the key frames in this example use an instance of the <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> class because a string animation that is created with key frames can only use discrete key frames.</span></span> <span data-ttu-id="f8841-107">などの不連続のキーフレーム<xref:System.Windows.Media.Animation.DiscreteStringKeyFrame>されている値の間に急なジャンプを作成、変更、アニメーションに迅速に実行およびはなく。</span><span class="sxs-lookup"><span data-stu-id="f8841-107">Discrete key frames like <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> create sudden jumps between values, that is, changes to the animation occur quickly and are not subtle.</span></span>  
  
 [!code-xaml[keyframes_snip#StringAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/StringAnimationUsingKeyFramesExample.xaml#stringanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="f8841-108">サンプル全体については、「[キーフレーム アニメーションのサンプル](https://go.microsoft.com/fwlink/?LinkID=160012)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8841-108">For the complete sample, see [KeyFrame Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160012).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8841-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8841-109">See also</span></span>
- <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames>
- <xref:System.Windows.Controls.ContentControl.Content%2A>
- <xref:System.Windows.Controls.Button>
- <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame>
- [<span data-ttu-id="f8841-110">キー フレーム アニメーションの概要</span><span class="sxs-lookup"><span data-stu-id="f8841-110">Key-Frame Animations Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)
- [<span data-ttu-id="f8841-111">キー フレームに関する「方法」トピック</span><span class="sxs-lookup"><span data-stu-id="f8841-111">Key-Frame How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)
