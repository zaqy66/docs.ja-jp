---
title: Windows フォーム内でのイベント ハンドラーの作成
ms.date: 03/30/2017
helpviewer_keywords:
- event handling [Windows Forms]
- Windows Forms controls, event handling
- Windows Forms, event handling
- events [Windows Forms], event handlers
- event handlers [Windows Forms]
ms.assetid: 6514e530-c6b8-489c-a8d2-eda7b7072701
ms.openlocfilehash: c77a004d52afc67a3811ff98e9a62c788c001803
ms.sourcegitcommit: 2b986afe4ce9e13bbeec929c9737757eb61de60e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56664784"
---
# <a name="creating-event-handlers-in-windows-forms"></a><span data-ttu-id="f830b-102">Windows フォーム内でのイベント ハンドラーの作成</span><span class="sxs-lookup"><span data-stu-id="f830b-102">Creating Event Handlers in Windows Forms</span></span>
<span data-ttu-id="f830b-103">イベント ハンドラーは、ユーザーがボタンをクリックする、またはメッセージ キューがメッセージを受信するなどのイベントが発生したときに実行するアクションを決定する、コード内の手順です。</span><span class="sxs-lookup"><span data-stu-id="f830b-103">An event handler is a procedure in your code that determines what actions are performed when an event occurs, such as when the user clicks a button or a message queue receives a message.</span></span> <span data-ttu-id="f830b-104">イベントが発生すると、そのイベントを受信した一つまたは複数のイベント ハンドラーが実行されます。</span><span class="sxs-lookup"><span data-stu-id="f830b-104">When an event is raised, the event handler or handlers that receive the event are executed.</span></span> <span data-ttu-id="f830b-105">イベントは複数のハンドラーに割り当てられ、特定のイベントを処理するメソッドは動的に変更できます。</span><span class="sxs-lookup"><span data-stu-id="f830b-105">Events can be assigned to multiple handlers, and the methods that handle particular events can be changed dynamically.</span></span> <span data-ttu-id="f830b-106">イベント ハンドラーを作成するには、Windows フォーム デザイナーを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="f830b-106">You can also use the Windows Forms Designer to create event handlers.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f830b-107">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="f830b-107">In This Section</span></span>  
 [<span data-ttu-id="f830b-108">イベントの概要</span><span class="sxs-lookup"><span data-stu-id="f830b-108">Events Overview</span></span>](../../../docs/framework/winforms/events-overview-windows-forms.md)  
 <span data-ttu-id="f830b-109">イベント モデルおよびデリゲートの役割を説明します。</span><span class="sxs-lookup"><span data-stu-id="f830b-109">Explains the event model and the role of delegates.</span></span>  
  
 [<span data-ttu-id="f830b-110">イベント ハンドラーの概要</span><span class="sxs-lookup"><span data-stu-id="f830b-110">Event Handlers Overview</span></span>](../../../docs/framework/winforms/event-handlers-overview-windows-forms.md)  
 <span data-ttu-id="f830b-111">イベントを処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f830b-111">Describes how to handle events.</span></span>  
  
 [<span data-ttu-id="f830b-112">方法: Windows フォームの実行時にイベント ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f830b-112">How to: Create Event Handlers at Run Time for Windows Forms</span></span>](../../../docs/framework/winforms/how-to-create-event-handlers-at-run-time-for-windows-forms.md)  
 <span data-ttu-id="f830b-113">システム イベントおよびユーザー イベントへの動的な応答の手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="f830b-113">Gives directions for responding to system or user events dynamically.</span></span>  
  
 [<span data-ttu-id="f830b-114">方法: Windows フォームで 1 つのイベント ハンドラーに複数のイベントを接続します。</span><span class="sxs-lookup"><span data-stu-id="f830b-114">How to: Connect Multiple Events to a Single Event Handler in Windows Forms</span></span>](../../../docs/framework/winforms/how-to-connect-multiple-events-to-a-single-event-handler-in-windows-forms.md)  
 <span data-ttu-id="f830b-115">イベントを通じて、複数のコントロールに同じ機能を割り当てる手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="f830b-115">Gives directions for assigning the same functionality to multiple controls through events.</span></span>  
  
 [<span data-ttu-id="f830b-116">Windows フォームのイベントの順序</span><span class="sxs-lookup"><span data-stu-id="f830b-116">Order of Events in Windows Forms</span></span>](../../../docs/framework/winforms/order-of-events-in-windows-forms.md)  
 <span data-ttu-id="f830b-117">Windows フォーム コントロールで発生するイベントの順序について説明します。</span><span class="sxs-lookup"><span data-stu-id="f830b-117">Describes the order in which events are raised in Windows Forms controls.</span></span>  
  
 <span data-ttu-id="f830b-118">[方法: デザイナーを使用してイベント ハンドラーを作成します。](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/zwwsdtbk(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="f830b-118">[How to: Create Event Handlers Using the Designer](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/zwwsdtbk(v=vs.100))</span></span>  
 <span data-ttu-id="f830b-119">Windows フォーム デザイナーを使用してイベント ハンドラーを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f830b-119">Describes how to use the Windows Forms Designer to create event handlers.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="f830b-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="f830b-120">Related Sections</span></span>  
 [<span data-ttu-id="f830b-121">イベント</span><span class="sxs-lookup"><span data-stu-id="f830b-121">Events</span></span>](../../../docs/standard/events/index.md)  
 <span data-ttu-id="f830b-122">[!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] を使用したイベントの処理および発生に関するトピックへのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="f830b-122">Provides links to topics on handling and raising events using the [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)].</span></span>  
  
 [<span data-ttu-id="f830b-123">Visual Basic での継承されたイベント ハンドラーのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f830b-123">Troubleshooting Inherited Event Handlers in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)  
 <span data-ttu-id="f830b-124">継承されたコンポーネントでイベント ハンドラーに生じる一般的な問題を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="f830b-124">Lists common issues that occur with event handlers in inherited components.</span></span>
