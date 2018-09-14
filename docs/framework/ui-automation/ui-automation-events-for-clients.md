---
title: クライアントの UI オートメーション イベント
ms.date: 03/30/2017
helpviewer_keywords:
- UI Automation, events for clients
- events, UI Automation clients
ms.assetid: b909e388-3f24-4997-b6d4-bd9c35c2dc27
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: f295bbf44d6272879e8ea8e74c435d206b7af913
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2018
ms.locfileid: "45615223"
---
# <a name="ui-automation-events-for-clients"></a>クライアントの UI オートメーション イベント
> [!NOTE]
>  このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]に関する最新情報については[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)をご覧ください。  
  
 このトピックで説明する方法[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]イベントは、UI オートメーション クライアントで使用されます。  
  
 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 関心のあるイベントをサブスクライブするクライアントを使用できます。 この機能は、常にすべてをポーリングする必要がある、パフォーマンスを改善、[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]すべてについては、構造体、または状態が変更されたかどうか、システム内の要素。  
  
 また、定義されたスコープ内のイベントだけをリッスンできるため、効率性も向上します。 クライアントがすべてのフォーカス変更イベントのリッスンできるなど、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]ツリーで、または 1 つだけの要素とその子孫の要素。  
  
> [!NOTE]
>  使用できるすべてのイベントが発生すると想定しないで、[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]プロバイダー。 たとえば、すべてのプロパティの変更は、の標準プロキシ プロバイダーによって発生させるイベントを[!INCLUDE[TLA#tla_winforms](../../../includes/tlasharptla-winforms-md.md)]と[!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)]コントロール。  
  
 広い視野の[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]イベントを参照してください[UI Automation Events Overview](../../../docs/framework/ui-automation/ui-automation-events-overview.md)します。  
  
<a name="Subscribing_to_Events"></a>   
## <a name="subscribing-to-events"></a>イベントのサブスクライブ  
 クライアント アプリケーションは特定の種類のイベントをサブスクライブするために、次のいずれかのメソッドを使用してイベント ハンドラーを登録します。  
  
|メソッド|イベントの種類|イベント引数の種類|デリゲート型|  
|------------|----------------|--------------------------|-------------------|  
|<xref:System.Windows.Automation.Automation.AddAutomationFocusChangedEventHandler%2A>|フォーカスの変更|<xref:System.Windows.Automation.AutomationFocusChangedEventArgs>|<xref:System.Windows.Automation.AutomationFocusChangedEventHandler>|  
|<xref:System.Windows.Automation.Automation.AddAutomationPropertyChangedEventHandler%2A>|プロパティの変更|<xref:System.Windows.Automation.AutomationPropertyChangedEventArgs>|<xref:System.Windows.Automation.AutomationPropertyChangedEventHandler>|  
|<xref:System.Windows.Automation.Automation.AddStructureChangedEventHandler%2A>|構造の変更|<xref:System.Windows.Automation.StructureChangedEventArgs>|<xref:System.Windows.Automation.StructureChangedEventHandler>|  
|<xref:System.Windows.Automation.Automation.AddAutomationEventHandler%2A>|識別されるその他のすべてのイベント、 <xref:System.Windows.Automation.AutomationEvent>|<xref:System.Windows.Automation.AutomationEventArgs> または <xref:System.Windows.Automation.WindowClosedEventArgs>|<xref:System.Windows.Automation.AutomationEventHandler>|  
  
 メソッドを呼び出す前に、イベントを処理するデリゲート メソッドを作成する必要があります。 必要に応じて、単一のメソッドでさまざまな種類のイベントを処理し、そのメソッドを複数の呼び出しで表中のメソッドの 1 つに渡すことができます。 たとえば、1 つ<xref:System.Windows.Automation.AutomationEventHandler>異なるに応じたさまざまなイベントを処理するように設定できる、<xref:System.Windows.Automation.AutomationEventArgs.EventId%2A>します。  
  
> [!NOTE]
>  ウィンドウを閉じるイベントを処理する、イベント ハンドラーに渡される引数の型をキャスト<xref:System.Windows.Automation.WindowClosedEventArgs>します。 [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]ウィンドウの要素が無効になって、使用することはできません、`sender`情報を取得するパラメーターを使用して、<xref:System.Windows.Automation.WindowClosedEventArgs.GetRuntimeId%2A>代わりにします。  
  
> [!CAUTION]
>  アプリケーションが独自のイベントを受け取った場合[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]、アプリケーションの使用しない[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]スレッドのイベントにサブスクライブするまたは登録を解除します。 使用すると、予期しない動作を招く可能性があります。 詳細については、「 [UI Automation Threading Issues](../../../docs/framework/ui-automation/ui-automation-threading-issues.md)」を参照してください。  
  
 シャット ダウン時、または[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]アプリケーションに関心のあるイベントが不要になったが、UI オートメーション クライアントは、次のメソッドのいずれかを呼び出す必要があります。  
  
|メソッド|説明|  
|------------|-----------------|  
|<xref:System.Windows.Automation.Automation.RemoveAutomationEventHandler%2A>|使用して登録されたイベント ハンドラーの登録を解除します<xref:System.Windows.Automation.Automation.AddAutomationEventHandler%2A>します。|  
|<xref:System.Windows.Automation.Automation.RemoveAutomationFocusChangedEventHandler%2A>|使用して登録されたイベント ハンドラーの登録を解除します<xref:System.Windows.Automation.Automation.AddAutomationFocusChangedEventHandler%2A>します。|  
|<xref:System.Windows.Automation.Automation.RemoveAutomationPropertyChangedEventHandler%2A>|使用して登録されたイベント ハンドラーの登録を解除します<xref:System.Windows.Automation.Automation.AddAutomationPropertyChangedEventHandler%2A>します。|  
|<xref:System.Windows.Automation.Automation.RemoveAllEventHandlers%2A>|登録済みのすべてのイベント ハンドラーの登録を解除します。|  
  
 コード例は、「 [UI オートメーション イベントをサブスクライブ](../../../docs/framework/ui-automation/subscribe-to-ui-automation-events.md)します。  
  
## <a name="see-also"></a>関連項目  
 [UI オートメーション イベントのサブスクライブ](../../../docs/framework/ui-automation/subscribe-to-ui-automation-events.md)  
 [UI オートメーション イベントの概要](../../../docs/framework/ui-automation/ui-automation-events-overview.md)  
 [UI オートメーション プロパティの概要](../../../docs/framework/ui-automation/ui-automation-properties-overview.md)  
 [TrackFocus サンプル](https://msdn.microsoft.com/library/4a91c0af-6bb5-4d38-a743-cf136f268fc9)
