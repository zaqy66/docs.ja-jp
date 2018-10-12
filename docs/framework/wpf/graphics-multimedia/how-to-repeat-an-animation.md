---
title: '方法 : アニメーションを反復する'
ms.date: 03/30/2017
helpviewer_keywords:
- RepeatBehavior property of timelines [WPF]
- repeating animating [WPF]
- Timelines RepeatBehavior property [WPF]
- animation [WPF], repeating
ms.assetid: e6f3b068-eeeb-47fd-8d40-8848c31f1e1e
ms.openlocfilehash: 176fc9c31f85361a243cd9357d79608e0ff6a4cd
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43855297"
---
# <a name="how-to-repeat-an-animation"></a>方法 : アニメーションを反復する
この例は、使用する方法を示します、<xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A>のプロパティを<xref:System.Windows.Media.Animation.Timeline>アニメーションの繰り返し動作を制御するためにします。  
  
## <a name="example"></a>例  
 <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A>のプロパティを<xref:System.Windows.Media.Animation.Timeline>アニメーションは、単純継続時間を繰り返す回数を制御します。 使用して<xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A>、ことを指定できる、<xref:System.Windows.Media.Animation.Timeline>回数だけ繰り返されます (反復カウント) か、指定された期間。 いずれの場合も、アニメーションは、要求されたカウントまたは期間を入力するために必要な数の先頭まで実行します。  
  
 既定では、タイムラインは 1.0 では、1 回だけ再生して繰り返さない、つまりの繰り返し回数があります。 ただし、設定した場合、<xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A>のプロパティを<xref:System.Windows.Media.Animation.Timeline>に<xref:System.Windows.Media.Animation.RepeatBehavior.Forever%2A>タイムラインを無限に繰り返します。  
  
 次の例は、使用する方法を示します、<xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A>プロパティ アニメーションの繰り返し動作を制御するためです。 例では、アニメーション、<xref:System.Windows.FrameworkElement.Width%2A>繰り返し動作のさまざまな型を使用して各四角形を持つ 5 つの四角形のプロパティ。  
  
 [!code-xaml[timingbehaviors_snip#RepeatBehaviorWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/RepeatBehaviorExample.xaml#repeatbehaviorwholepage)]  
  
 サンプル全体については、次を参照してください。[アニメーションのタイミング動作のサンプル](https://go.microsoft.com/fwlink/?LinkID=159970)します。  
  
## <a name="see-also"></a>関連項目  
 [反復サイクル中にアニメーション値を累積する](../../../../docs/framework/wpf/graphics-multimedia/how-to-accumulate-animation-values-during-repeat-cycles.md)  
 [タイムラインを自動的に反転するかどうかを指定する](../../../../docs/framework/wpf/graphics-multimedia/how-to-specify-whether-a-timeline-automatically-reverses.md)  
 [方法トピック](../../../../docs/framework/wpf/graphics-multimedia/animation-and-timing-how-to-topics.md)  
 [アニメーションとタイミング](https://msdn.microsoft.com/library/7d83765b-d5ae-41b1-b423-80206e1124aa)  
 [アニメーションの概要](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [アニメーションのタイミング動作のサンプル](https://go.microsoft.com/fwlink/?LinkID=159970)
