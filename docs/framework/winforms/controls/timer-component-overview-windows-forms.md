---
title: Timer コンポーネントの概要 (Windows フォーム)
ms.date: 03/30/2017
f1_keywords:
- Timer
helpviewer_keywords:
- Timer component [Windows Forms], about Timer components
- timers [Windows Forms], about timers
ms.assetid: e672c05b-a8b6-4b26-9e4d-9223aa9e3873
ms.openlocfilehash: 6e453f6b7718c6c5be3109f51153a3f5e4b5b6f4
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44136460"
---
# <a name="timer-component-overview-windows-forms"></a><span data-ttu-id="dbfaa-102">Timer コンポーネントの概要 (Windows フォーム)</span><span class="sxs-lookup"><span data-stu-id="dbfaa-102">Timer Component Overview (Windows Forms)</span></span>
<span data-ttu-id="dbfaa-103">Windows フォーム <xref:System.Windows.Forms.Timer> は、一定の間隔でイベントを発生させるコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="dbfaa-103">The Windows Forms <xref:System.Windows.Forms.Timer> is a component that raises an event at regular intervals.</span></span> <span data-ttu-id="dbfaa-104">このコンポーネントは、Windows フォームの環境用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="dbfaa-104">This component is designed for a Windows Forms environment.</span></span> <span data-ttu-id="dbfaa-105">サーバー環境に適したタイマーが必要な場合は、「[サーバー ベースのタイマーの概要](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dbfaa-105">If you need a timer that is suitable for a server environment, see [Introduction to Server-Based Timers](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc).</span></span>  
  
## <a name="key-properties-methods-and-events"></a><span data-ttu-id="dbfaa-106">キー プロパティ、メソッド、およびイベント</span><span class="sxs-lookup"><span data-stu-id="dbfaa-106">Key Properties, Methods, and Events</span></span>  
 <span data-ttu-id="dbfaa-107">間隔の長さが定義されている、<xref:System.Windows.Forms.Timer.Interval%2A>プロパティ、値はミリ秒単位で。</span><span class="sxs-lookup"><span data-stu-id="dbfaa-107">The length of the intervals is defined by the <xref:System.Windows.Forms.Timer.Interval%2A> property, whose value is in milliseconds.</span></span> <span data-ttu-id="dbfaa-108">コンポーネントが有効にすると、<xref:System.Windows.Forms.Timer.Tick>イベントの発生間隔。</span><span class="sxs-lookup"><span data-stu-id="dbfaa-108">When the component is enabled, the <xref:System.Windows.Forms.Timer.Tick> event is raised every interval.</span></span> <span data-ttu-id="dbfaa-109">これは、実行するコードを追加することです。</span><span class="sxs-lookup"><span data-stu-id="dbfaa-109">This is where you would add code to be executed.</span></span> <span data-ttu-id="dbfaa-110">詳細については、次を参照してください。[方法: Windows フォームの Timer コンポーネントの設定間隔でプロシージャの実行](../../../../docs/framework/winforms/controls/run-procedures-at-set-intervals-with-wf-timer-component.md)します。</span><span class="sxs-lookup"><span data-stu-id="dbfaa-110">For more information, see [How to: Run Procedures at Set Intervals with the Windows Forms Timer Component](../../../../docs/framework/winforms/controls/run-procedures-at-set-intervals-with-wf-timer-component.md).</span></span> <span data-ttu-id="dbfaa-111">主要なメソッド、<xref:System.Windows.Forms.Timer>コンポーネントは<xref:System.Windows.Forms.Timer.Start%2A>と<xref:System.Windows.Forms.Timer.Stop%2A>タイマーをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="dbfaa-111">The key methods of the <xref:System.Windows.Forms.Timer> component are <xref:System.Windows.Forms.Timer.Start%2A> and <xref:System.Windows.Forms.Timer.Stop%2A>, which turn the timer on and off.</span></span> <span data-ttu-id="dbfaa-112">タイマーをオフにすると、ときにリセットされます。一時停止する方法はありません、<xref:System.Windows.Forms.Timer>コンポーネント。</span><span class="sxs-lookup"><span data-stu-id="dbfaa-112">When the timer is switched off, it resets; there is no way to pause a <xref:System.Windows.Forms.Timer> component.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dbfaa-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="dbfaa-113">See Also</span></span>  
 <xref:System.Windows.Forms.Timer>  
 [<span data-ttu-id="dbfaa-114">Timer コンポーネント</span><span class="sxs-lookup"><span data-stu-id="dbfaa-114">Timer Component</span></span>](../../../../docs/framework/winforms/controls/timer-component-windows-forms.md)  
 [<span data-ttu-id="dbfaa-115">Windows フォームの Timer コンポーネントの Interval プロパティの制限</span><span class="sxs-lookup"><span data-stu-id="dbfaa-115">Limitations of the Windows Forms Timer Component's Interval Property</span></span>](../../../../docs/framework/winforms/controls/limitations-of-the-timer-component-interval-property.md)
