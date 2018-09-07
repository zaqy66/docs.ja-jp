---
title: '方法 : 開始後のストーリーボードをイベント トリガーを使用して制御する'
ms.date: 03/30/2017
helpviewer_keywords:
- triggers [WPF], controlling Storyboards
- event triggers [WPF], controlling Storyboards
- Storyboards [WPF], controlling after start
ms.assetid: 3b115594-6a93-4972-b24d-61aa16f1c15f
ms.openlocfilehash: f31b1233f00147fdccde5e0816fa4839ae33d549
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44098421"
---
# <a name="how-to-use-event-triggers-to-control-a-storyboard-after-it-starts"></a><span data-ttu-id="2f42f-102">方法 : 開始後のストーリーボードをイベント トリガーを使用して制御する</span><span class="sxs-lookup"><span data-stu-id="2f42f-102">How to: Use Event Triggers to Control a Storyboard After It Starts</span></span>
<span data-ttu-id="2f42f-103">この例では、制御、<xref:System.Windows.Media.Animation.Storyboard>開始後にします。</span><span class="sxs-lookup"><span data-stu-id="2f42f-103">This example shows how to control a <xref:System.Windows.Media.Animation.Storyboard> after it starts.</span></span> <span data-ttu-id="2f42f-104">開始する、<xref:System.Windows.Media.Animation.Storyboard>を使用して[!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]を使用して、<xref:System.Windows.Media.Animation.BeginStoryboard>オブジェクトとプロパティをアニメーション化して、ストーリー ボードを起動しにアニメーションを配布します。</span><span class="sxs-lookup"><span data-stu-id="2f42f-104">To start a <xref:System.Windows.Media.Animation.Storyboard> by using [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], use <xref:System.Windows.Media.Animation.BeginStoryboard>, which distributes the animations to the objects and properties they animate and then starts the storyboard.</span></span> <span data-ttu-id="2f42f-105">付ける場合<xref:System.Windows.Media.Animation.BeginStoryboard>名前を指定してその<xref:System.Windows.Media.Animation.BeginStoryboard.Name%2A>プロパティをできるようにする制御可能なストーリー ボード。</span><span class="sxs-lookup"><span data-stu-id="2f42f-105">If you give <xref:System.Windows.Media.Animation.BeginStoryboard> a name by specifying its <xref:System.Windows.Media.Animation.BeginStoryboard.Name%2A> property, you make it a controllable storyboard.</span></span> <span data-ttu-id="2f42f-106">ことができます対話的に制御、ストーリー ボードが開始されます。</span><span class="sxs-lookup"><span data-stu-id="2f42f-106">You can then interactively control the storyboard after it starts.</span></span>  
  
 <span data-ttu-id="2f42f-107">と共に次のストーリー ボード アクションを使用して、<xref:System.Windows.EventTrigger>ストーリー ボードを制御するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="2f42f-107">Use the following storyboard actions together with <xref:System.Windows.EventTrigger> objects to control a storyboard.</span></span>  
  
-   <span data-ttu-id="2f42f-108"><xref:System.Windows.Media.Animation.PauseStoryboard>: ストーリー ボードを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="2f42f-108"><xref:System.Windows.Media.Animation.PauseStoryboard>: Pauses the storyboard.</span></span>  
  
-   <span data-ttu-id="2f42f-109"><xref:System.Windows.Media.Animation.ResumeStoryboard>: 一時停止中のストーリー ボードを再開します。</span><span class="sxs-lookup"><span data-stu-id="2f42f-109"><xref:System.Windows.Media.Animation.ResumeStoryboard>: Resumes a paused storyboard.</span></span>  
  
-   <span data-ttu-id="2f42f-110"><xref:System.Windows.Media.Animation.SetStoryboardSpeedRatio>: ストーリー ボードの速度を変更します。</span><span class="sxs-lookup"><span data-stu-id="2f42f-110"><xref:System.Windows.Media.Animation.SetStoryboardSpeedRatio>: Changes the storyboard speed.</span></span>  
  
-   <span data-ttu-id="2f42f-111"><xref:System.Windows.Media.Animation.SkipStoryboardToFill>: ある場合、塗りつぶし期間の末尾にストーリー ボードを進めます。</span><span class="sxs-lookup"><span data-stu-id="2f42f-111"><xref:System.Windows.Media.Animation.SkipStoryboardToFill>: Advances a storyboard to the end of its fill period, if it has one.</span></span>  
  
-   <span data-ttu-id="2f42f-112"><xref:System.Windows.Media.Animation.StopStoryboard>: ストーリー ボードを停止します。</span><span class="sxs-lookup"><span data-stu-id="2f42f-112"><xref:System.Windows.Media.Animation.StopStoryboard>: Stops the storyboard.</span></span>  
  
-   <span data-ttu-id="2f42f-113"><xref:System.Windows.Media.Animation.RemoveStoryboard>: リソースの解放、ストーリー ボードを削除します。</span><span class="sxs-lookup"><span data-stu-id="2f42f-113"><xref:System.Windows.Media.Animation.RemoveStoryboard>: Removes the storyboard, freeing resources.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2f42f-114">例</span><span class="sxs-lookup"><span data-stu-id="2f42f-114">Example</span></span>  
 <span data-ttu-id="2f42f-115">次の例では、制御可能なストーリー ボード アクションを使用して、ストーリー ボードを対話的に制御します。</span><span class="sxs-lookup"><span data-stu-id="2f42f-115">The following example uses controllable storyboard actions to interactively control a storyboard.</span></span>  
  
 <span data-ttu-id="2f42f-116">**注:** コードを使用してストーリー ボードを制御するための例を表示するには、次を参照してください。 [、ストーリー ボードの後に開始の対話型メソッドを使用して制御](../../../../docs/framework/wpf/graphics-multimedia/how-to-control-a-storyboard-after-it-starts.md)します。</span><span class="sxs-lookup"><span data-stu-id="2f42f-116">**Note:** To see an example of controlling a storyboard by using code, see [Control a Storyboard After It Starts Using Its Interactive Methods](../../../../docs/framework/wpf/graphics-multimedia/how-to-control-a-storyboard-after-it-starts.md).</span></span>  
  
 [!code-xaml[timingbehaviors_snip#ControlStoryboardExampleUsingWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/ControlStoryboardExample.xaml#controlstoryboardexampleusingwholepage)]  
  
 <span data-ttu-id="2f42f-117">その他の例では、次を参照してください。、[アニメーション サンプル ギャラリー](https://go.microsoft.com/fwlink/?LinkID=159969)します。</span><span class="sxs-lookup"><span data-stu-id="2f42f-117">For additional examples, see the [Animation Example Gallery](https://go.microsoft.com/fwlink/?LinkID=159969).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f42f-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f42f-118">See Also</span></span>  
 <xref:System.Windows.Media.Animation.ResumeStoryboard>  
 <xref:System.Windows.Media.Animation.SetStoryboardSpeedRatio>  
 <xref:System.Windows.Media.Animation.SkipStoryboardToFill>  
 <xref:System.Windows.Media.Animation.PauseStoryboard>  
 <xref:System.Windows.Media.Animation.StopStoryboard>  
 <xref:System.Windows.Media.Animation.SeekStoryboard>  
 [<span data-ttu-id="2f42f-119">対話型メソッドを使用してストーリーボードを開始後に制御する</span><span class="sxs-lookup"><span data-stu-id="2f42f-119">Control a Storyboard After It Starts Using Its Interactive Methods</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-control-a-storyboard-after-it-starts.md)  
 [<span data-ttu-id="2f42f-120">アニメーションの概要</span><span class="sxs-lookup"><span data-stu-id="2f42f-120">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [<span data-ttu-id="2f42f-121">ストーリーボードの概要</span><span class="sxs-lookup"><span data-stu-id="2f42f-121">Storyboards Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/storyboards-overview.md)
