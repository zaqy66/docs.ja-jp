---
title: サポートされている UI オートメーション コントロール パターンの取得
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- control patterns, getting
- UI Automation, getting control patterns
- getting, control patterns
ms.assetid: 006c54c9-50bf-48d9-a855-9d62eb95603a
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: b0bc694148dbd91cd9e942a3f051aea9362fc150
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43511477"
---
# <a name="get-supported-ui-automation-control-patterns"></a>サポートされている UI オートメーション コントロール パターンの取得
> [!NOTE]
>  このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。 に関する最新情報については[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]を参照してください[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)します。  
  
 このトピックからコントロール パターン オブジェクトを取得する方法を示しています。[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]要素。  
  
### <a name="obtain-all-control-patterns"></a>すべてのコントロール パターンの取得  
  
1.  取得、<xref:System.Windows.Automation.AutomationElement>に関心がコントロール パターンします。  
  
2.  呼び出す<xref:System.Windows.Automation.AutomationElement.GetSupportedPatterns%2A>要素からすべてのコントロール パターンを取得します。  
  
> [!CAUTION]
>  クライアントが使用しないことを強くお勧め<xref:System.Windows.Automation.AutomationElement.GetSupportedPatterns%2A>します。 このメソッドを呼び出すと、パフォーマンスを深刻な影響することができます<xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A>の各既存のコントロール パターンを内部的にします。 可能であれば、クライアントが呼び出す必要があります<xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A>の主なパターンです。  
  
### <a name="obtain-a-specific-control-pattern"></a>特定のコントロール パターンの取得  
  
1.  取得、<xref:System.Windows.Automation.AutomationElement>に関心がコントロール パターンします。  
  
2.  呼び出す<xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A>または<xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A>特定のパターンを照会します。 これらのメソッドと同様に、パターンが見つからない場合は<xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A>例外を発生させますと<xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A>返します`false`します。  
  
## <a name="example"></a>例  
 次の例では、取得、<xref:System.Windows.Automation.AutomationElement>リスト項目を取得し、<xref:System.Windows.Automation.SelectionItemPattern>その要素から。  
  
 [!code-csharp[UIAClient_snip#103](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#103)]
 [!code-vb[UIAClient_snip#103](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#103)]  
  
## <a name="see-also"></a>関連項目  
 [クライアントの UI オートメーション コントロール パターン](../../../docs/framework/ui-automation/ui-automation-control-patterns-for-clients.md)
