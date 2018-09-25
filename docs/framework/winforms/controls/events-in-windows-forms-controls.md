---
title: Windows フォーム コントロールのイベント
ms.date: 03/30/2017
helpviewer_keywords:
- events [Windows Forms], custom controls (using code)
- custom controls [Windows Forms], events overview (using code)
ms.assetid: 7e3d1379-87aa-437c-afce-c99454eff30e
ms.openlocfilehash: d18938565c302be085b7ac51f878d83ae5ab533d
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2018
ms.locfileid: "47027903"
---
# <a name="events-in-windows-forms-controls"></a><span data-ttu-id="f6c9c-102">Windows フォーム コントロールのイベント</span><span class="sxs-lookup"><span data-stu-id="f6c9c-102">Events in Windows Forms Controls</span></span>
<span data-ttu-id="f6c9c-103">Windows フォーム コントロールを継承から 60 を超えるイベント<xref:System.Windows.Forms.Control?displayProperty=nameWithType>します。</span><span class="sxs-lookup"><span data-stu-id="f6c9c-103">A Windows Forms control inherits more than sixty events from <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span> <span data-ttu-id="f6c9c-104">以下の<xref:System.Windows.Forms.Control.Paint>イベント、コントロールを描画する、ウィンドウの表示などに関連するイベント、<xref:System.Windows.Forms.Control.Resize>と<xref:System.Windows.Forms.Control.Layout>イベント、および低レベルのマウスとキーボード イベント。</span><span class="sxs-lookup"><span data-stu-id="f6c9c-104">These include the <xref:System.Windows.Forms.Control.Paint> event, which causes a control to be drawn, events related to displaying a window, such as the <xref:System.Windows.Forms.Control.Resize> and <xref:System.Windows.Forms.Control.Layout> events, and low-level mouse and keyboard events.</span></span> <span data-ttu-id="f6c9c-105">一部の下位イベントは合成<xref:System.Windows.Forms.Control>などのセマンティック イベントに<xref:System.Windows.Forms.Control.Click>と<xref:System.Windows.Forms.Control.DoubleClick>します。</span><span class="sxs-lookup"><span data-stu-id="f6c9c-105">Some low-level events are synthesized by <xref:System.Windows.Forms.Control> into semantic events such as <xref:System.Windows.Forms.Control.Click> and <xref:System.Windows.Forms.Control.DoubleClick>.</span></span> <span data-ttu-id="f6c9c-106">詳細については、継承されたイベントは、次を参照してください。<xref:System.Windows.Forms.Control>します。</span><span class="sxs-lookup"><span data-stu-id="f6c9c-106">For details about inherited events, see <xref:System.Windows.Forms.Control>.</span></span>  
  
 <span data-ttu-id="f6c9c-107">継承されたイベントの機能をカスタム コントロールでオーバーライドする必要がある場合、デリゲートを結び付けるのではなく、継承された `On`*EventName* メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="f6c9c-107">If your custom control needs to override inherited event functionality, override the inherited `On`*EventName* method instead of attaching a delegate.</span></span> <span data-ttu-id="f6c9c-108">.NET Framework でのイベント モデルに詳しくない場合は、「[コンポーネントからのイベントの生成](https://msdn.microsoft.com/library/9aebf605-a87d-470b-b7c8-f9abfc8360a0)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6c9c-108">If you are not familiar with the event model in the .NET Framework, see [Raising Events from a Component](https://msdn.microsoft.com/library/9aebf605-a87d-470b-b7c8-f9abfc8360a0).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6c9c-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6c9c-109">See Also</span></span>  
 [<span data-ttu-id="f6c9c-110">OnPaint メソッドのオーバーライド</span><span class="sxs-lookup"><span data-stu-id="f6c9c-110">Overriding the OnPaint Method</span></span>](../../../../docs/framework/winforms/controls/overriding-the-onpaint-method.md)  
 [<span data-ttu-id="f6c9c-111">ユーザーの入力の処理</span><span class="sxs-lookup"><span data-stu-id="f6c9c-111">Handling User Input</span></span>](../../../../docs/framework/winforms/controls/handling-user-input.md)  
 [<span data-ttu-id="f6c9c-112">イベントの定義</span><span class="sxs-lookup"><span data-stu-id="f6c9c-112">Defining an Event</span></span>](../../../../docs/framework/winforms/controls/defining-an-event-in-windows-forms-controls.md)  
 [<span data-ttu-id="f6c9c-113">イベント</span><span class="sxs-lookup"><span data-stu-id="f6c9c-113">Events</span></span>](../../../../docs/standard/events/index.md)
