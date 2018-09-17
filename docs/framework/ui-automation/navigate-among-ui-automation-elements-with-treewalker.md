---
title: TreeWalker を使用した UI オートメーション要素間の移動
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- classes, TreeWalker
- TreeWalker class
- elements, navigating among
- UI Automation, navigating among elements
ms.assetid: afcd21dc-2ffa-48c9-9332-51269f44b7e9
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: 6a44cd16513bffa47e56064ea7e0e05692cb78a7
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45743496"
---
# <a name="navigate-among-ui-automation-elements-with-treewalker"></a>TreeWalker を使用した UI オートメーション要素間の移動
> [!NOTE]
>  このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]に関する最新情報については[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)をご覧ください。  
  
 このトピックでは、間を移動する方法を示すコード例を含む[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]要素を使用して、<xref:System.Windows.Automation.TreeWalker>クラス。  
  
## <a name="example"></a>例  
 次の例では<xref:System.Windows.Automation.TreeWalker.GetParent%2A>をウォーク、[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]ツリーのルート要素、またはデスクトップが見つかるまでです。 そのすぐ下の要素は、指定した要素の親ウィンドウです。  
  
 [!code-csharp[UIAFocusTracker_snip#102](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAFocusTracker_snip/CSharp/FocusTracker.cs#102)]
 [!code-vb[UIAFocusTracker_snip#102](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAFocusTracker_snip/VisualBasic/FocusTracker.vb#102)]  
  
## <a name="example"></a>例  
 次の例では<xref:System.Windows.Automation.TreeWalker.GetFirstChild%2A>と<xref:System.Windows.Automation.TreeWalker.GetNextSibling%2A>を作成する、<xref:System.Windows.Forms.TreeView>のサブツリー全体を示す[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]要素が有効になっていると、コントロール ビューになっています。  
  
 [!code-csharp[UIAClient_snip#174](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#174)]
 [!code-vb[UIAClient_snip#174](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#174)]  
  
## <a name="see-also"></a>関連項目  
 [UI オートメーション要素の取得](../../../docs/framework/ui-automation/obtaining-ui-automation-elements.md)
