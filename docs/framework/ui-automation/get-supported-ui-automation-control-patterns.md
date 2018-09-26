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
ms.openlocfilehash: d948ff2f71ff7d4335cacc0fa3815dd75af4ad45
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47231382"
---
# <a name="get-supported-ui-automation-control-patterns"></a><span data-ttu-id="999fe-102">サポートされている UI オートメーション コントロール パターンの取得</span><span class="sxs-lookup"><span data-stu-id="999fe-102">Get Supported UI Automation Control Patterns</span></span>
> [!NOTE]
>  <span data-ttu-id="999fe-103">このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="999fe-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="999fe-104">[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]に関する最新情報については[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="999fe-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="999fe-105">このトピックからコントロール パターン オブジェクトを取得する方法を示しています。[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]要素。</span><span class="sxs-lookup"><span data-stu-id="999fe-105">This topic shows how to retrieve control pattern objects from [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] elements.</span></span>  
  
### <a name="obtain-all-control-patterns"></a><span data-ttu-id="999fe-106">すべてのコントロール パターンの取得</span><span class="sxs-lookup"><span data-stu-id="999fe-106">Obtain All Control Patterns</span></span>  
  
1.  <span data-ttu-id="999fe-107">取得、<xref:System.Windows.Automation.AutomationElement>に関心がコントロール パターンします。</span><span class="sxs-lookup"><span data-stu-id="999fe-107">Get the <xref:System.Windows.Automation.AutomationElement> whose control patterns you are interested in.</span></span>  
  
2.  <span data-ttu-id="999fe-108">呼び出す<xref:System.Windows.Automation.AutomationElement.GetSupportedPatterns%2A>要素からすべてのコントロール パターンを取得します。</span><span class="sxs-lookup"><span data-stu-id="999fe-108">Call <xref:System.Windows.Automation.AutomationElement.GetSupportedPatterns%2A> to get all control patterns from the element.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="999fe-109">クライアントが使用しないことを強くお勧め<xref:System.Windows.Automation.AutomationElement.GetSupportedPatterns%2A>します。</span><span class="sxs-lookup"><span data-stu-id="999fe-109">It is strongly recommended that a client not use <xref:System.Windows.Automation.AutomationElement.GetSupportedPatterns%2A>.</span></span> <span data-ttu-id="999fe-110">このメソッドを呼び出すと、パフォーマンスを深刻な影響することができます<xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A>の各既存のコントロール パターンを内部的にします。</span><span class="sxs-lookup"><span data-stu-id="999fe-110">Performance can be severely affected as this method calls <xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A> internally for each existing control pattern.</span></span> <span data-ttu-id="999fe-111">可能であれば、クライアントが呼び出す必要があります<xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A>の主なパターンです。</span><span class="sxs-lookup"><span data-stu-id="999fe-111">If possible, a client should call <xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A> for the key patterns of interest.</span></span>  
  
### <a name="obtain-a-specific-control-pattern"></a><span data-ttu-id="999fe-112">特定のコントロール パターンの取得</span><span class="sxs-lookup"><span data-stu-id="999fe-112">Obtain a Specific Control Pattern</span></span>  
  
1.  <span data-ttu-id="999fe-113">取得、<xref:System.Windows.Automation.AutomationElement>に関心がコントロール パターンします。</span><span class="sxs-lookup"><span data-stu-id="999fe-113">Get the <xref:System.Windows.Automation.AutomationElement> whose control patterns you are interested in.</span></span>  
  
2.  <span data-ttu-id="999fe-114">呼び出す<xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A>または<xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A>特定のパターンを照会します。</span><span class="sxs-lookup"><span data-stu-id="999fe-114">Call <xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A> or <xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A> to query for a specific pattern.</span></span> <span data-ttu-id="999fe-115">これらのメソッドと同様に、パターンが見つからない場合は<xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A>例外を発生させますと<xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A>返します`false`します。</span><span class="sxs-lookup"><span data-stu-id="999fe-115">These methods are similar, but if the pattern is not found, <xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A> raises an exception, and <xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A> returns `false`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="999fe-116">例</span><span class="sxs-lookup"><span data-stu-id="999fe-116">Example</span></span>  
 <span data-ttu-id="999fe-117">次の例では、取得、<xref:System.Windows.Automation.AutomationElement>リスト項目を取得し、<xref:System.Windows.Automation.SelectionItemPattern>その要素から。</span><span class="sxs-lookup"><span data-stu-id="999fe-117">The following example retrieves an <xref:System.Windows.Automation.AutomationElement> for a list item and obtains a <xref:System.Windows.Automation.SelectionItemPattern> from that element.</span></span>  
  
 [!code-csharp[UIAClient_snip#103](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#103)]
 [!code-vb[UIAClient_snip#103](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#103)]  
  
## <a name="see-also"></a><span data-ttu-id="999fe-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="999fe-118">See Also</span></span>  
 [<span data-ttu-id="999fe-119">クライアントの UI オートメーション コントロール パターン</span><span class="sxs-lookup"><span data-stu-id="999fe-119">UI Automation Control Patterns for Clients</span></span>](../../../docs/framework/ui-automation/ui-automation-control-patterns-for-clients.md)
