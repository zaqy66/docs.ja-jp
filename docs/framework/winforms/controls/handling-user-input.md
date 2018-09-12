---
title: ユーザーの入力の処理
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], user input using code
- custom controls [Windows Forms], keyboard events using code
- custom controls [Windows Forms], mouse events using code
ms.assetid: d9b12787-86f6-4022-8e0f-e12d312c4af2
ms.openlocfilehash: 19bb494d6f478c8cb7adda770f441470c4b2d19f
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44705272"
---
# <a name="handling-user-input"></a><span data-ttu-id="39450-102">ユーザーの入力の処理</span><span class="sxs-lookup"><span data-stu-id="39450-102">Handling User Input</span></span>
<span data-ttu-id="39450-103">このトピックでは、によって提供されるメインのキーボードとマウスのイベントを説明します。<xref:System.Windows.Forms.Control?displayProperty=nameWithType>します。</span><span class="sxs-lookup"><span data-stu-id="39450-103">This topic describes the main keyboard and mouse events provided by <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span> <span data-ttu-id="39450-104">イベントを処理するときに、コントロール作成者はイベントにデリゲートを結び付けるのではなく、保護された `On`*EventName* メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="39450-104">When handling an event, control authors should override the protected `On`*EventName* method rather than attaching a delegate to the event.</span></span> <span data-ttu-id="39450-105">イベントのレビューについては、「[コンポーネントからのイベントの生成](https://msdn.microsoft.com/library/9aebf605-a87d-470b-b7c8-f9abfc8360a0)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39450-105">For a review of events, see [Raising Events from a Component](https://msdn.microsoft.com/library/9aebf605-a87d-470b-b7c8-f9abfc8360a0).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="39450-106">イベント、基底クラスのインスタンスに関連付けられているデータがないかどうかは<xref:System.EventArgs>への引数として渡される、 `On` *EventName*メソッド。</span><span class="sxs-lookup"><span data-stu-id="39450-106">If there is no data associated with an event, an instance of the base class <xref:System.EventArgs> is passed as an argument to the `On`*EventName* method.</span></span>  
  
## <a name="keyboard-events"></a><span data-ttu-id="39450-107">キーボード イベント</span><span class="sxs-lookup"><span data-stu-id="39450-107">Keyboard Events</span></span>  
 <span data-ttu-id="39450-108">コントロールで処理できる一般的なキーボード イベントは<xref:System.Windows.Forms.Control.KeyDown>、 <xref:System.Windows.Forms.Control.KeyPress>、および<xref:System.Windows.Forms.Control.KeyUp>します。</span><span class="sxs-lookup"><span data-stu-id="39450-108">The common keyboard events that your control can handle are <xref:System.Windows.Forms.Control.KeyDown>, <xref:System.Windows.Forms.Control.KeyPress>, and <xref:System.Windows.Forms.Control.KeyUp>.</span></span>  
  
|<span data-ttu-id="39450-109">イベント名</span><span class="sxs-lookup"><span data-stu-id="39450-109">Event Name</span></span>|<span data-ttu-id="39450-110">オーバーライドするメソッド</span><span class="sxs-lookup"><span data-stu-id="39450-110">Method to Override</span></span>|<span data-ttu-id="39450-111">イベントの説明</span><span class="sxs-lookup"><span data-stu-id="39450-111">Description of Event</span></span>|  
|----------------|------------------------|--------------------------|  
|`KeyDown`|`void OnKeyDown(KeyEventArgs)`|<span data-ttu-id="39450-112">キーが最初に押されたときにのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="39450-112">Raised only when a key is initially pressed.</span></span>|  
|`KeyPress`|`void OnKeyPress`<br /><br /> `(KeyPressEventArgs)`|<span data-ttu-id="39450-113">キーが押されるたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="39450-113">Raised every time a key is pressed.</span></span> <span data-ttu-id="39450-114">キーを押した場合、<xref:System.Windows.Forms.Control.KeyPress>オペレーティング システムで定義されたリピート間隔でイベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="39450-114">If a key is held down, a <xref:System.Windows.Forms.Control.KeyPress> event is raised at the repeat rate defined by the operating system.</span></span>|  
|`KeyUp`|`void OnKeyUp(KeyEventArgs)`|<span data-ttu-id="39450-115">キーが離されたときに発生します。</span><span class="sxs-lookup"><span data-stu-id="39450-115">Raised when a key is released.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="39450-116">キーボード入力の処理は、前の表のイベントをオーバーライドするよりもかなり複雑であり、このトピックでは触れていません。</span><span class="sxs-lookup"><span data-stu-id="39450-116">Handling keyboard input is considerably more complex than overriding the events in the preceding table and is beyond the scope of this topic.</span></span> <span data-ttu-id="39450-117">詳細については、「 [Windows フォームでのユーザー入力](../../../../docs/framework/winforms/user-input-in-windows-forms.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39450-117">For more information, see [User Input in Windows Forms](../../../../docs/framework/winforms/user-input-in-windows-forms.md).</span></span>  
  
## <a name="mouse-events"></a><span data-ttu-id="39450-118">マウス イベント</span><span class="sxs-lookup"><span data-stu-id="39450-118">Mouse Events</span></span>  
 <span data-ttu-id="39450-119">コントロールで処理できるマウス イベントは<xref:System.Windows.Forms.Control.MouseDown>、 <xref:System.Windows.Forms.Control.MouseEnter>、 <xref:System.Windows.Forms.Control.MouseHover>、 <xref:System.Windows.Forms.Control.MouseLeave>、 <xref:System.Windows.Forms.Control.MouseMove>、および<xref:System.Windows.Forms.Control.MouseUp>します。</span><span class="sxs-lookup"><span data-stu-id="39450-119">The mouse events that your control can handle are <xref:System.Windows.Forms.Control.MouseDown>, <xref:System.Windows.Forms.Control.MouseEnter>, <xref:System.Windows.Forms.Control.MouseHover>, <xref:System.Windows.Forms.Control.MouseLeave>, <xref:System.Windows.Forms.Control.MouseMove>, and <xref:System.Windows.Forms.Control.MouseUp>.</span></span>  
  
|<span data-ttu-id="39450-120">イベント名</span><span class="sxs-lookup"><span data-stu-id="39450-120">Event Name</span></span>|<span data-ttu-id="39450-121">オーバーライドするメソッド</span><span class="sxs-lookup"><span data-stu-id="39450-121">Method to Override</span></span>|<span data-ttu-id="39450-122">イベントの説明</span><span class="sxs-lookup"><span data-stu-id="39450-122">Description of Event</span></span>|  
|----------------|------------------------|--------------------------|  
|`MouseDown`|`void OnMouseDown(MouseEventArgs)`|<span data-ttu-id="39450-123">ポインターがコントロール上にある状態でマウス ボタンが押されると発生します。</span><span class="sxs-lookup"><span data-stu-id="39450-123">Raised when the mouse button is pressed while the pointer is over the control.</span></span>|  
|`MouseEnter`|`void OnMouseEnter(EventArgs)`|<span data-ttu-id="39450-124">ポインターがコントロールの領域に初めて入ったときに発生します。</span><span class="sxs-lookup"><span data-stu-id="39450-124">Raised when the pointer first enters the region of the control.</span></span>|  
|`MouseHover`|`void OnMouseHover(EventArgs)`|<span data-ttu-id="39450-125">ポインターがコントロールの上に置かれたときに発生します。</span><span class="sxs-lookup"><span data-stu-id="39450-125">Raised when the pointer hovers over the control.</span></span>|  
|`MouseLeave`|`void OnMouseLeave(EventArgs)`|<span data-ttu-id="39450-126">ポインターがコントロールの領域から離れると発生します。</span><span class="sxs-lookup"><span data-stu-id="39450-126">Raised when the pointer leaves the region of the control.</span></span>|  
|`MouseMove`|`void OnMouseMove(MouseEventArgs)`|<span data-ttu-id="39450-127">ポインターがコントロールの領域内で移動すると発生します。</span><span class="sxs-lookup"><span data-stu-id="39450-127">Raised when the pointer moves in the region of the control.</span></span>|  
|`MouseUp`|`void OnMouseUp(MouseEventArgs)`|<span data-ttu-id="39450-128">ポインターがコントロールの上にある状態でマウス ボタンが離されるか、ポインターがコントロールの領域から離れると発生します。</span><span class="sxs-lookup"><span data-stu-id="39450-128">Raised when the mouse button is released while the pointer is over the control or the pointer leaves the region of the control.</span></span>|  
  
 <span data-ttu-id="39450-129">次のコード フラグメントは、オーバーライドする例を示しています、<xref:System.Windows.Forms.Control.MouseDown>イベント。</span><span class="sxs-lookup"><span data-stu-id="39450-129">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseDown> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#7](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#7)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#7](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#7)]  
  
 <span data-ttu-id="39450-130">次のコード フラグメントは、オーバーライドする例を示しています、<xref:System.Windows.Forms.Control.MouseMove>イベント。</span><span class="sxs-lookup"><span data-stu-id="39450-130">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseMove> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#8](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#8)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#8](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#8)]  
  
 <span data-ttu-id="39450-131">次のコード フラグメントは、オーバーライドする例を示しています、<xref:System.Windows.Forms.Control.MouseUp>イベント。</span><span class="sxs-lookup"><span data-stu-id="39450-131">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseUp> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#9](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#9)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#9](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#9)]  
  
 <span data-ttu-id="39450-132">`FlashTrackBar` サンプルの完全なソース コードについては、「[方法 : 進行状況を示す Windows フォーム コントロールを作成する](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39450-132">For the complete source code for the `FlashTrackBar` sample, see [How to: Create a Windows Forms Control That Shows Progress](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39450-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="39450-133">See Also</span></span>  
 [<span data-ttu-id="39450-134">Windows フォーム コントロールのイベント</span><span class="sxs-lookup"><span data-stu-id="39450-134">Events in Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/events-in-windows-forms-controls.md)  
 [<span data-ttu-id="39450-135">イベントの定義</span><span class="sxs-lookup"><span data-stu-id="39450-135">Defining an Event</span></span>](../../../../docs/framework/winforms/controls/defining-an-event-in-windows-forms-controls.md)  
 [<span data-ttu-id="39450-136">イベント</span><span class="sxs-lookup"><span data-stu-id="39450-136">Events</span></span>](../../../../docs/standard/events/index.md)  
 [<span data-ttu-id="39450-137">Windows フォームでのユーザー入力</span><span class="sxs-lookup"><span data-stu-id="39450-137">User Input in Windows Forms</span></span>](../../../../docs/framework/winforms/user-input-in-windows-forms.md)
