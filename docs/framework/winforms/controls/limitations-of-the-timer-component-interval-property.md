---
title: Windows フォームの Timer コンポーネントの制限事項&#39;秒間隔のプロパティ
ms.date: 03/30/2017
helpviewer_keywords:
- timers [Windows Forms], event intervals
- Interval property [Windows Forms], limitations
- timers [Windows Forms], Windows-based
- Timer component [Windows Forms], limitations of Interval property
ms.assetid: 7e5fb513-77e7-4046-a8e8-aab94e61ca0f
ms.openlocfilehash: 9710568c3c21878aa6aad626e3152168a2f0c2fe
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2018
ms.locfileid: "48836395"
---
# <a name="limitations-of-the-windows-forms-timer-component39s-interval-property"></a><span data-ttu-id="1bfdd-102">Windows フォームの Timer コンポーネントの制限事項&#39;秒間隔のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1bfdd-102">Limitations of the Windows Forms Timer Component&#39;s Interval Property</span></span>
<span data-ttu-id="1bfdd-103">Windows フォーム<xref:System.Windows.Forms.Timer>コンポーネントには、<xref:System.Windows.Forms.Timer.Interval%2A>と次の 1 つのタイマー イベントの間の経過時間をミリ秒数を指定するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1bfdd-103">The Windows Forms <xref:System.Windows.Forms.Timer> component has an <xref:System.Windows.Forms.Timer.Interval%2A> property that specifies the number of milliseconds that pass between one timer event and the next.</span></span> <span data-ttu-id="1bfdd-104">タイマーは引き続き受信コンポーネントが無効にしない限り、<xref:System.Windows.Forms.Timer.Tick>ほぼ一定の時間間隔でイベント。</span><span class="sxs-lookup"><span data-stu-id="1bfdd-104">Unless the component is disabled, a timer continues to receive the <xref:System.Windows.Forms.Timer.Tick> event at roughly equal intervals of time.</span></span>  
  
 <span data-ttu-id="1bfdd-105">このコンポーネントは、Windows フォームの環境用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="1bfdd-105">This component is designed for a Windows Forms environment.</span></span> <span data-ttu-id="1bfdd-106">サーバー環境に適したタイマーが必要な場合は、「[サーバー ベースのタイマーの概要](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1bfdd-106">If you need a timer that is suitable for a server environment, see [Introduction to Server-Based Timers](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc).</span></span>  
  
## <a name="the-interval-property"></a><span data-ttu-id="1bfdd-107">間隔のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1bfdd-107">The Interval Property</span></span>  
 <span data-ttu-id="1bfdd-108"><xref:System.Windows.Forms.Timer.Interval%2A>プロパティがプログラミングしているときに考慮すべきいくつかの制限、<xref:System.Windows.Forms.Timer>コンポーネント。</span><span class="sxs-lookup"><span data-stu-id="1bfdd-108">The <xref:System.Windows.Forms.Timer.Interval%2A> property has a few limitations to consider when you are programming a <xref:System.Windows.Forms.Timer> component:</span></span>  
  
-   <span data-ttu-id="1bfdd-109">アプリケーションまたは別のアプリケーションで、システムで重い負荷が早い場合、長いループや複雑な計算、またはドライブ、ネットワーク、またはポートへのアクセスなど-アプリケーションとしてのタイマー イベントを頻繁に利用できない、<xref:System.Windows.Forms.Timer.Interval%2A>プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="1bfdd-109">If your application or another application is making heavy demands on the system — such as long loops, intensive calculations, or drive, network, or port access — your application may not get timer events as often as the <xref:System.Windows.Forms.Timer.Interval%2A> property specifies.</span></span>  
  
-   <span data-ttu-id="1bfdd-110">間隔は、正確に時間の経過時間は保証されません。</span><span class="sxs-lookup"><span data-stu-id="1bfdd-110">The interval is not guaranteed to elapse exactly on time.</span></span> <span data-ttu-id="1bfdd-111">精度を保証するには、タイマーする必要があります、必要に応じて、システム クロックのチェックではなく保持の累積時間を内部的にしようとしています。</span><span class="sxs-lookup"><span data-stu-id="1bfdd-111">To ensure accuracy, the timer should check the system clock as needed, rather than try to keep track of accumulated time internally.</span></span>  
  
-   <span data-ttu-id="1bfdd-112">有効桁数、<xref:System.Windows.Forms.Timer.Interval%2A>プロパティの単位はミリ秒です。</span><span class="sxs-lookup"><span data-stu-id="1bfdd-112">The precision of the <xref:System.Windows.Forms.Timer.Interval%2A> property is in milliseconds.</span></span> <span data-ttu-id="1bfdd-113">一部のコンピューターでは、ミリ秒よりも高い解像度が高分解能カウンターを提供します。</span><span class="sxs-lookup"><span data-stu-id="1bfdd-113">Some computers provide a high-resolution counter that has a resolution higher than milliseconds.</span></span> <span data-ttu-id="1bfdd-114">このようなカウンターの可用性は、コンピューターのプロセッサ ハードウェアに依存します。</span><span class="sxs-lookup"><span data-stu-id="1bfdd-114">The availability of such a counter depends on the processor hardware of your computer.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1bfdd-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="1bfdd-115">See Also</span></span>  
 <xref:System.Windows.Forms.Timer>  
 [<span data-ttu-id="1bfdd-116">Timer コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1bfdd-116">Timer Component</span></span>](../../../../docs/framework/winforms/controls/timer-component-windows-forms.md)  
 [<span data-ttu-id="1bfdd-117">Timer コンポーネントの概要</span><span class="sxs-lookup"><span data-stu-id="1bfdd-117">Timer Component Overview</span></span>](../../../../docs/framework/winforms/controls/timer-component-overview-windows-forms.md)
