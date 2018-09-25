---
title: プロパティ条件に基づく UI オートメーション要素の検索
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- elements, finding by property conditions
- UI Automation, finding elements by property conditions
ms.assetid: 3acaee5a-6ce8-4c3e-81c8-67e59eb74477
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: 708393ced89e56536b92f73f603695f00fb5e76e
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47085854"
---
# <a name="find-a-ui-automation-element-based-on-a-property-condition"></a>プロパティ条件に基づく UI オートメーション要素の検索
> [!NOTE]
>  このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]に関する最新情報については[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)をご覧ください。  
  
 このトピックには内の要素を検索する方法を示すコード例が含まれています、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]ツリーでは、特定のプロパティまたはプロパティに基づいて。  
  
## <a name="example"></a>例  
 次の例では、一連のプロパティの条件がで指定された関心のある特定の要素 (または要素) を識別する、<xref:System.Windows.Automation.AutomationElement>ツリー。 一致するすべての要素の検索が実行し、<xref:System.Windows.Automation.AutomationElement.FindAll%2A>一連が組み込まれているメソッド<xref:System.Windows.Automation.AndCondition>一致する要素の数を制限するブール演算。  
  
> [!NOTE]
>  検索するときに、 <xref:System.Windows.Automation.AutomationElement.RootElement%2A>、直接の子のみを取得しようとする必要があります。 子孫を検索は、数百または数千ものスタック オーバーフローを引き起こす要素を反復処理する可能性があります。 下位レベルの特定の要素を取得しようとする場合、アプリケーション ウィンドウから、または下位レベルのコンテナーから検索を開始する必要があります。  
  
 [!code-csharp[InvokePatternApp#1100](../../../samples/snippets/csharp/VS_Snippets_Wpf/InvokePatternApp/CSharp/InvokePatternApp.cs#1100)]
 [!code-vb[InvokePatternApp#1100](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/InvokePatternApp/VisualBasic/Client.vb#1100)]  
  
## <a name="see-also"></a>関連項目  
 [InvokePattern および ExpandCollapsePattern メニュー項目のサンプル](https://msdn.microsoft.com/library/b7fa141c-e2d1-4da2-a27f-81a7d1172210)  
 [UI オートメーション要素の取得](../../../docs/framework/ui-automation/obtaining-ui-automation-elements.md)  
 [AutomationID プロパティの使用](../../../docs/framework/ui-automation/use-the-automationid-property.md)
