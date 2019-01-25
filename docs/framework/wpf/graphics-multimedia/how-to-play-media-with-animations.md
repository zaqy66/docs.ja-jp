---
title: '方法: アニメーションを使用してメディアを再生する'
ms.date: 03/30/2017
helpviewer_keywords:
- multimedia [WPF], playback with animations
- playback of media [WPF], with animations
- animation [WPF], media playback with
- media [WPF], playback with animations
ms.assetid: 8982b7b7-1c6c-4b24-8801-b328862975f5
ms.openlocfilehash: e6a011b1fa6f3551c3570370247fbae262b20e4c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54594253"
---
# <a name="how-to-play-media-with-animations"></a>方法: アニメーションを使用してメディアを再生する
この例を使用して、同時にメディアとアニメーションを再生する方法を示しています、<xref:System.Windows.Media.MediaTimeline>と<xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>、同じクラス<xref:System.Windows.Media.Animation.Storyboard>します。  
  
## <a name="example"></a>例  
 1 つまたは複数を使用する<xref:System.Windows.Media.MediaTimeline>内のオブジェクトを<xref:System.Windows.Media.Animation.Storyboard>と共に他<xref:System.Windows.Media.Animation.Timeline>アニメーションなどのオブジェクト。  
  
 次の例のセット、<xref:System.Windows.Media.Animation.ParallelTimeline.SlipBehavior%2A>のプロパティ、<xref:System.Windows.Media.Animation.Storyboard>の値に`Slip`メディア (この例ではビデオ) が進行するまで、アニメーションが進行しないことを指定します。 この機能は、読み込み時間のためにメディアの再生が遅れる場合などに必要です。  
  
 [!code-xaml[MediaGallery_snippet#MediaTimelinePlusAnimationExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snippet/CSharp/MediaTimelinePlusAnimationExample.xaml#mediatimelineplusanimationexamplewholepage)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Media.MediaTimeline>
- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>
- <xref:System.Windows.Media.Animation.Storyboard>
- <xref:System.Windows.Media.Animation.ParallelTimeline.SlipBehavior%2A>
- [方法トピック](../../../../docs/framework/wpf/graphics-multimedia/audio-and-video-how-to-topics.md)
- [ストーリーボードの概要](../../../../docs/framework/wpf/graphics-multimedia/storyboards-overview.md)
- [キー フレーム アニメーションの概要](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)
- [アニメーションの概要](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [グラフィックスとマルチメディア](../../../../docs/framework/wpf/graphics-multimedia/index.md)
