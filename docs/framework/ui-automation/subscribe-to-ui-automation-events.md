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
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43870277"
---
# <a name="subscribe-to-ui-automation-events"></a>UI オートメーション イベントのサブスクライブ
> [!NOTE]
>  このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。 に関する最新情報については[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]を参照してください[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)します。  
  
 このトピックでは、UI オートメーション プロバイダーによって生成されるイベントをサブスクライブする方法について説明します。  
  
## <a name="example"></a>例  
 次のコード例では、ボタンなどのコントロールが呼び出された場合に生成されるイベントに対してイベント ハンドラーを登録し、アプリケーション フォームが閉じられた時にそのイベント ハンドラーを削除します。 イベントがで識別される、<xref:System.Windows.Automation.AutomationEvent>へのパラメーターとして渡される<xref:System.Windows.Automation.Automation.AddAutomationEventHandler%2A>します。  
  
 [!code-csharp[UIAClient_snip#101](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#101)]
 [!code-vb[UIAClient_snip#101](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#101)]  
  
## <a name="example"></a>例  
 次の例は、使用する方法を示します[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]にフォーカスが変更されたときに発生するイベントをサブスクライブします。 イベント ハンドラーの登録は、アプリケーションのシャットダウン時に呼び出されるメソッドで解除されるか、UI イベントの通知が必要なくなった時に解除されます。  
  
 [!code-csharp[UIAClient_snip#102](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#102)]
 [!code-vb[UIAClient_snip#102](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#102)]  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.Automation.Automation.AddAutomationEventHandler%2A>  
 <xref:System.Windows.Automation.Automation.RemoveAllEventHandlers%2A>  
 <xref:System.Windows.Automation.Automation.RemoveAutomationEventHandler%2A>  
 [UI オートメーション イベントの概要](../../../docs/framework/ui-automation/ui-automation-events-overview.md)
