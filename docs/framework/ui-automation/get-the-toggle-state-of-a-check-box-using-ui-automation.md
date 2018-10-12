---
title: UI オートメーションを使用した、チェック ボックスのトグル状態の取得
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UI Automation, getting toggle states of check boxes
- check boxes, getting toggle states of
- getting, toggle states of check boxes
ms.assetid: 84fc31a3-175f-4e93-90a0-dd29d89b77ce
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: ebe51247a93384ab2d269220b08a1b3f3cb22e03
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47200621"
---
# <a name="get-the-toggle-state-of-a-check-box-using-ui-automation"></a>UI オートメーションを使用した、チェック ボックスのトグル状態の取得
> [!NOTE]
>  このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]に関する最新情報については[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)をご覧ください。  
  
 このトピックでは、使用する方法を示します[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]コントロールのトグル状態を取得します。  
  
## <a name="example"></a>例  
 この例では、<xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A>のメソッド、<xref:System.Windows.Automation.AutomationElement>を取得するクラス、<xref:System.Windows.Automation.TogglePattern>コントロールからオブジェクトを返す、<xref:System.Windows.Automation.ToggleState>プロパティ。  
  
 [!code-csharp[NavigatingWithTreeWalker#1200](../../../samples/snippets/csharp/VS_Snippets_Wpf/NavigatingWithTreeWalker/CSharp/ClientClass.cs#1200)]
 [!code-vb[NavigatingWithTreeWalker#1200](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/NavigatingWithTreeWalker/visualbasic/clientclass.vb#1200)]
