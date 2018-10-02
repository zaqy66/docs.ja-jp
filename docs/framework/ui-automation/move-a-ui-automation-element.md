---
title: UI オートメーション要素の移動
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- moving elements
- elements, moving
- UI Automation, moving elements
ms.assetid: 4042cb44-e27e-4a03-ac36-9be1eed65b47
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: 144d2ce4b539a5eb4a744f176593b29f920cc528
ms.sourcegitcommit: daa8788af67ac2d1cecd24f9f3409babb2f978c9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47862603"
---
# <a name="move-a-ui-automation-element"></a><span data-ttu-id="3cad3-102">UI オートメーション要素の移動</span><span class="sxs-lookup"><span data-stu-id="3cad3-102">Move a UI Automation Element</span></span>
> [!NOTE]
>  <span data-ttu-id="3cad3-103">このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="3cad3-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="3cad3-104">[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]に関する最新情報については[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3cad3-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="3cad3-105">この例では、指定した画面位置に [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 要素を移動する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3cad3-105">This example demonstrates how to move a [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] element to a specified screen location.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3cad3-106">例</span><span class="sxs-lookup"><span data-stu-id="3cad3-106">Example</span></span>  
 <span data-ttu-id="3cad3-107">次の例では、 <xref:System.Windows.Automation.WindowPattern> および <xref:System.Windows.Automation.TransformPattern> コントロール パターンを使用して、 [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)] target application to discrete screen locations および track the <xref:System.Windows.Automation.AutomationElement.BoundingRectangleProperty> <xref:System.Windows.Automation.AutomationElement.AutomationPropertyChangedEvent>を追跡します。</span><span class="sxs-lookup"><span data-stu-id="3cad3-107">The following example uses the <xref:System.Windows.Automation.WindowPattern> and <xref:System.Windows.Automation.TransformPattern> control patterns to programmatically move a [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)] target application to discrete screen locations and track the <xref:System.Windows.Automation.AutomationElement.BoundingRectangleProperty> <xref:System.Windows.Automation.AutomationElement.AutomationPropertyChangedEvent>.</span></span>  
  
 [!code-csharp[WindowMove#1301](../../../samples/snippets/csharp/VS_Snippets_Wpf/WindowMove/CSharp/WindowMove.cs#1301)]
 [!code-vb[WindowMove#1301](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/WindowMove/VisualBasic/windowmove.vb#1301)]  
[!code-csharp[WindowMove#1300](../../../samples/snippets/csharp/VS_Snippets_Wpf/WindowMove/CSharp/WindowMove.cs#1300)]
[!code-vb[WindowMove#1300](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/WindowMove/VisualBasic/windowmove.vb#1300)]  
  
## <a name="see-also"></a><span data-ttu-id="3cad3-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="3cad3-108">See Also</span></span>  
 [<span data-ttu-id="3cad3-109">WindowPattern サンプル</span><span class="sxs-lookup"><span data-stu-id="3cad3-109">WindowPattern Sample</span></span>](https://msdn.microsoft.com/library/598b695c-8baf-406e-bbfb-2a1c7842a1de)
