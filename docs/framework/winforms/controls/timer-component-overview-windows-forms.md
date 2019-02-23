---
title: Timer コンポーネントの概要 (Windows フォーム)
ms.date: 03/30/2017
f1_keywords:
- Timer
helpviewer_keywords:
- Timer component [Windows Forms], about Timer components
- timers [Windows Forms], about timers
ms.assetid: e672c05b-a8b6-4b26-9e4d-9223aa9e3873
ms.openlocfilehash: e92a8028fd532a7c3a44eba7a41799b7344a82df
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/23/2019
ms.locfileid: "56746550"
---
# <a name="timer-component-overview-windows-forms"></a><span data-ttu-id="75b82-102">Timer コンポーネントの概要 (Windows フォーム)</span><span class="sxs-lookup"><span data-stu-id="75b82-102">Timer Component Overview (Windows Forms)</span></span>
<span data-ttu-id="75b82-103">Windows フォーム <xref:System.Windows.Forms.Timer> は、一定の間隔でイベントを発生させるコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="75b82-103">The Windows Forms <xref:System.Windows.Forms.Timer> is a component that raises an event at regular intervals.</span></span> <span data-ttu-id="75b82-104">このコンポーネントは、Windows フォームの環境用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="75b82-104">This component is designed for a Windows Forms environment.</span></span> <span data-ttu-id="75b82-105">サーバー環境に適したタイマーが必要な場合は、「[サーバー ベースのタイマーの概要](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="75b82-105">If you need a timer that is suitable for a server environment, see [Introduction to Server-Based Timers](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).</span></span>  
  
## <a name="key-properties-methods-and-events"></a><span data-ttu-id="75b82-106">キー プロパティ、メソッド、およびイベント</span><span class="sxs-lookup"><span data-stu-id="75b82-106">Key Properties, Methods, and Events</span></span>  
 <span data-ttu-id="75b82-107">間隔の長さが定義されている、<xref:System.Windows.Forms.Timer.Interval%2A>プロパティ、値はミリ秒単位で。</span><span class="sxs-lookup"><span data-stu-id="75b82-107">The length of the intervals is defined by the <xref:System.Windows.Forms.Timer.Interval%2A> property, whose value is in milliseconds.</span></span> <span data-ttu-id="75b82-108">コンポーネントが有効にすると、<xref:System.Windows.Forms.Timer.Tick>イベントの発生間隔。</span><span class="sxs-lookup"><span data-stu-id="75b82-108">When the component is enabled, the <xref:System.Windows.Forms.Timer.Tick> event is raised every interval.</span></span> <span data-ttu-id="75b82-109">これは、実行するコードを追加することです。</span><span class="sxs-lookup"><span data-stu-id="75b82-109">This is where you would add code to be executed.</span></span> <span data-ttu-id="75b82-110">詳細については、「[方法 :Windows フォームの Timer コンポーネントを使用して一定間隔でプロシージャを実行](../../../../docs/framework/winforms/controls/run-procedures-at-set-intervals-with-wf-timer-component.md)します。</span><span class="sxs-lookup"><span data-stu-id="75b82-110">For more information, see [How to: Run Procedures at Set Intervals with the Windows Forms Timer Component](../../../../docs/framework/winforms/controls/run-procedures-at-set-intervals-with-wf-timer-component.md).</span></span> <span data-ttu-id="75b82-111">主要なメソッド、<xref:System.Windows.Forms.Timer>コンポーネントは<xref:System.Windows.Forms.Timer.Start%2A>と<xref:System.Windows.Forms.Timer.Stop%2A>タイマーをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="75b82-111">The key methods of the <xref:System.Windows.Forms.Timer> component are <xref:System.Windows.Forms.Timer.Start%2A> and <xref:System.Windows.Forms.Timer.Stop%2A>, which turn the timer on and off.</span></span> <span data-ttu-id="75b82-112">タイマーをオフにすると、ときにリセットされます。一時停止する方法はありません、<xref:System.Windows.Forms.Timer>コンポーネント。</span><span class="sxs-lookup"><span data-stu-id="75b82-112">When the timer is switched off, it resets; there is no way to pause a <xref:System.Windows.Forms.Timer> component.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75b82-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="75b82-113">See also</span></span>
- <xref:System.Windows.Forms.Timer>
- [<span data-ttu-id="75b82-114">Timer コンポーネント</span><span class="sxs-lookup"><span data-stu-id="75b82-114">Timer Component</span></span>](../../../../docs/framework/winforms/controls/timer-component-windows-forms.md)
- [<span data-ttu-id="75b82-115">Windows フォームの Timer コンポーネントの Interval プロパティの制限</span><span class="sxs-lookup"><span data-stu-id="75b82-115">Limitations of the Windows Forms Timer Component's Interval Property</span></span>](../../../../docs/framework/winforms/controls/limitations-of-the-timer-component-interval-property.md)
