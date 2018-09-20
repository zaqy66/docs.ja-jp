---
title: UI オートメーション イベントのサブスクライブ
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UI Automation, subscribing to events
- subscribing to UI Automation events
- events, subscribing to
- listening for events
ms.assetid: b688effa-b3e8-4b05-944d-05ed89a245aa
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: c6845a85f9d3e07a4ecc9aad1ec11df8cdbc1f7a
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45745959"
---
# <a name="subscribe-to-ui-automation-events"></a><span data-ttu-id="58533-102">UI オートメーション イベントのサブスクライブ</span><span class="sxs-lookup"><span data-stu-id="58533-102">Subscribe to UI Automation Events</span></span>
> [!NOTE]
>  <span data-ttu-id="58533-103">このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="58533-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="58533-104">[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]に関する最新情報については[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="58533-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="58533-105">このトピックでは、UI オートメーション プロバイダーによって生成されるイベントをサブスクライブする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="58533-105">This topic shows how to subscribe to events raised by UI Automation providers.</span></span>  
  
## <a name="example"></a><span data-ttu-id="58533-106">例</span><span class="sxs-lookup"><span data-stu-id="58533-106">Example</span></span>  
 <span data-ttu-id="58533-107">次のコード例では、ボタンなどのコントロールが呼び出された場合に生成されるイベントに対してイベント ハンドラーを登録し、アプリケーション フォームが閉じられた時にそのイベント ハンドラーを削除します。</span><span class="sxs-lookup"><span data-stu-id="58533-107">The following example code registers an event handler for the event that is raised when a control such as a button is invoked, and removes it when the application form closes.</span></span> <span data-ttu-id="58533-108">イベントがで識別される、<xref:System.Windows.Automation.AutomationEvent>へのパラメーターとして渡される<xref:System.Windows.Automation.Automation.AddAutomationEventHandler%2A>します。</span><span class="sxs-lookup"><span data-stu-id="58533-108">The event is identified by an <xref:System.Windows.Automation.AutomationEvent> passed as a parameter to <xref:System.Windows.Automation.Automation.AddAutomationEventHandler%2A>.</span></span>  
  
 [!code-csharp[UIAClient_snip#101](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#101)]
 [!code-vb[UIAClient_snip#101](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#101)]  
  
## <a name="example"></a><span data-ttu-id="58533-109">例</span><span class="sxs-lookup"><span data-stu-id="58533-109">Example</span></span>  
 <span data-ttu-id="58533-110">次の例は、使用する方法を示します[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]にフォーカスが変更されたときに発生するイベントをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="58533-110">The following example shows how to use [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] to subscribe to an event that is raised when the focus changes.</span></span> <span data-ttu-id="58533-111">イベント ハンドラーの登録は、アプリケーションのシャットダウン時に呼び出されるメソッドで解除されるか、UI イベントの通知が必要なくなった時に解除されます。</span><span class="sxs-lookup"><span data-stu-id="58533-111">The event handler is unregistered in a method that could be called on application shutdown, or when notification of UI events is no longer required.</span></span>  
  
 [!code-csharp[UIAClient_snip#102](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#102)]
 [!code-vb[UIAClient_snip#102](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#102)]  
  
## <a name="see-also"></a><span data-ttu-id="58533-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="58533-112">See Also</span></span>  
 <xref:System.Windows.Automation.Automation.AddAutomationEventHandler%2A>  
 <xref:System.Windows.Automation.Automation.RemoveAllEventHandlers%2A>  
 <xref:System.Windows.Automation.Automation.RemoveAutomationEventHandler%2A>  
 [<span data-ttu-id="58533-113">UI オートメーション イベントの概要</span><span class="sxs-lookup"><span data-stu-id="58533-113">UI Automation Events Overview</span></span>](../../../docs/framework/ui-automation/ui-automation-events-overview.md)
