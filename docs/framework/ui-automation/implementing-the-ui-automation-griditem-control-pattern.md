---
title: UI オートメーション GridItem コントロール パターンの実装
ms.date: 03/30/2017
helpviewer_keywords:
- control patterns, GridItem
- UI Automation GridItem control pattern
- GridItem control pattern
ms.assetid: bffbae08-fe2a-42fd-ab84-f37187518916
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: adc018b2bf2b8922505083025135f1becf27f551
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54519217"
---
# <a name="implementing-the-ui-automation-griditem-control-pattern"></a><span data-ttu-id="60fd8-102">UI オートメーション GridItem コントロール パターンの実装</span><span class="sxs-lookup"><span data-stu-id="60fd8-102">Implementing the UI Automation GridItem Control Pattern</span></span>
> [!NOTE]
>  <span data-ttu-id="60fd8-103">このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="60fd8-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="60fd8-104">に関する最新情報については[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]を参照してください[Windows Automation API:UI オートメーション](https://go.microsoft.com/fwlink/?LinkID=156746)します。</span><span class="sxs-lookup"><span data-stu-id="60fd8-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="60fd8-105">ここでは、プロパティに関する情報など、 <xref:System.Windows.Automation.Provider.IGridItemProvider>を実装するガイドラインと規則について説明します。</span><span class="sxs-lookup"><span data-stu-id="60fd8-105">This topic introduces guidelines and conventions for implementing <xref:System.Windows.Automation.Provider.IGridItemProvider>, including information about properties.</span></span> <span data-ttu-id="60fd8-106">その他のリファレンスへのリンクは、概要の最後に記載します。</span><span class="sxs-lookup"><span data-stu-id="60fd8-106">Links to additional references are listed at the end of the overview.</span></span>  
  
 <span data-ttu-id="60fd8-107"><xref:System.Windows.Automation.Provider.IGridProvider> を実装するコンテナーの各子コントロールをサポートするために、<xref:System.Windows.Automation.GridItemPattern> コントロール パターンが使用されています。</span><span class="sxs-lookup"><span data-stu-id="60fd8-107">The <xref:System.Windows.Automation.GridItemPattern> control pattern is used to support individual child controls of containers that implement <xref:System.Windows.Automation.Provider.IGridProvider>.</span></span> <span data-ttu-id="60fd8-108">このコントロール パターンを実装するコントロールの例については、「 [Control Pattern Mapping for UI Automation Clients](../../../docs/framework/ui-automation/control-pattern-mapping-for-ui-automation-clients.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="60fd8-108">For examples of controls that implement this control pattern, see [Control Pattern Mapping for UI Automation Clients](../../../docs/framework/ui-automation/control-pattern-mapping-for-ui-automation-clients.md).</span></span>  
  
<a name="Implementation_Guidelines_and_Conventions"></a>   
## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="60fd8-109">実装のガイドラインと規則</span><span class="sxs-lookup"><span data-stu-id="60fd8-109">Implementation Guidelines and Conventions</span></span>  
 <span data-ttu-id="60fd8-110"><xref:System.Windows.Automation.Provider.IGridProvider> を実装する場合は、次のガイドラインと規則に留意してください。</span><span class="sxs-lookup"><span data-stu-id="60fd8-110">When implementing <xref:System.Windows.Automation.Provider.IGridProvider>, note the following guidelines and conventions:</span></span>  
  
-   <span data-ttu-id="60fd8-111">グリッドの座標は 0 から始まり、左上のセルの座標が (0, 0) です。</span><span class="sxs-lookup"><span data-stu-id="60fd8-111">Grid coordinates are zero-based with the upper left cell having coordinates (0, 0).</span></span>  
  
-   <span data-ttu-id="60fd8-112">結合されたセルが報告する <xref:System.Windows.Automation.Provider.IGridItemProvider.Row%2A> および <xref:System.Windows.Automation.Provider.IGridItemProvider.Column%2A> プロパティは、UI オートメーション プロバイダーによって定義された、基になるアンカー セルに基づきます。</span><span class="sxs-lookup"><span data-stu-id="60fd8-112">Merged cells will report their <xref:System.Windows.Automation.Provider.IGridItemProvider.Row%2A> and <xref:System.Windows.Automation.Provider.IGridItemProvider.Column%2A> properties based on their underlying anchor cell as defined by the UI Automation provider.</span></span> <span data-ttu-id="60fd8-113">通常、これは、最上位の左端の行または列です。</span><span class="sxs-lookup"><span data-stu-id="60fd8-113">Typically, it will be the topmost and leftmost row or column.</span></span>  
  
-   <span data-ttu-id="60fd8-114"><xref:System.Windows.Automation.Provider.IGridItemProvider> は、セルの結合や分割などのアクティブなグリッド操作を提供しません。</span><span class="sxs-lookup"><span data-stu-id="60fd8-114"><xref:System.Windows.Automation.Provider.IGridItemProvider> does not provide for active manipulation of the grid such as merging or splitting cells.</span></span>  
  
-   <span data-ttu-id="60fd8-115"><xref:System.Windows.Automation.Provider.IGridItemProvider> を実装するコントロールは、一般にキーボードを使用して横断できます (つまり、UI オートメーション クライアントが隣接するコントロールに移動できます)。</span><span class="sxs-lookup"><span data-stu-id="60fd8-115">Controls that implement <xref:System.Windows.Automation.Provider.IGridItemProvider> can typically be traversed (that is, a UI Automation client can move to adjacent controls) by using the keyboard.</span></span>  
  
<a name="Required_Members_for_IGridItemProvider"></a>   
## <a name="required-members-for-igriditemprovider"></a><span data-ttu-id="60fd8-116">IGridItemProvider の必須メンバー</span><span class="sxs-lookup"><span data-stu-id="60fd8-116">Required Members for IGridItemProvider</span></span>  
 <span data-ttu-id="60fd8-117"><xref:System.Windows.Automation.Provider.IGridItemProvider>の実装には、次のプロパティとメソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="60fd8-117">The following properties and methods are required for implementing <xref:System.Windows.Automation.Provider.IGridItemProvider>.</span></span>  
  
|<span data-ttu-id="60fd8-118">必須メンバー</span><span class="sxs-lookup"><span data-stu-id="60fd8-118">Required members</span></span>|<span data-ttu-id="60fd8-119">メンバーの型</span><span class="sxs-lookup"><span data-stu-id="60fd8-119">Member type</span></span>|<span data-ttu-id="60fd8-120">メモ</span><span class="sxs-lookup"><span data-stu-id="60fd8-120">Notes</span></span>|  
|----------------------|-----------------|-----------|  
|<xref:System.Windows.Automation.Provider.IGridItemProvider.Row%2A>|<span data-ttu-id="60fd8-121">プロパティ</span><span class="sxs-lookup"><span data-stu-id="60fd8-121">Property</span></span>|<span data-ttu-id="60fd8-122">なし</span><span class="sxs-lookup"><span data-stu-id="60fd8-122">None</span></span>|  
|<xref:System.Windows.Automation.Provider.IGridItemProvider.Column%2A>|<span data-ttu-id="60fd8-123">プロパティ</span><span class="sxs-lookup"><span data-stu-id="60fd8-123">Property</span></span>|<span data-ttu-id="60fd8-124">なし</span><span class="sxs-lookup"><span data-stu-id="60fd8-124">None</span></span>|  
|<xref:System.Windows.Automation.Provider.IGridItemProvider.RowSpan%2A>|<span data-ttu-id="60fd8-125">プロパティ</span><span class="sxs-lookup"><span data-stu-id="60fd8-125">Property</span></span>|<span data-ttu-id="60fd8-126">なし</span><span class="sxs-lookup"><span data-stu-id="60fd8-126">None</span></span>|  
|<xref:System.Windows.Automation.Provider.IGridItemProvider.ColumnSpan%2A>|<span data-ttu-id="60fd8-127">プロパティ</span><span class="sxs-lookup"><span data-stu-id="60fd8-127">Property</span></span>|<span data-ttu-id="60fd8-128">なし</span><span class="sxs-lookup"><span data-stu-id="60fd8-128">None</span></span>|  
|<xref:System.Windows.Automation.Provider.IGridItemProvider.ContainingGrid%2A>|<span data-ttu-id="60fd8-129">プロパティ</span><span class="sxs-lookup"><span data-stu-id="60fd8-129">Property</span></span>|<span data-ttu-id="60fd8-130">なし</span><span class="sxs-lookup"><span data-stu-id="60fd8-130">None</span></span>|  
  
 <span data-ttu-id="60fd8-131">このコントロール パターンに関連するメソッドまたはイベントはありません。</span><span class="sxs-lookup"><span data-stu-id="60fd8-131">This control pattern has no associated methods or events.</span></span>  
  
<a name="Exceptions"></a>   
## <a name="exceptions"></a><span data-ttu-id="60fd8-132">例外</span><span class="sxs-lookup"><span data-stu-id="60fd8-132">Exceptions</span></span>  
 <span data-ttu-id="60fd8-133">このコントロール パターンに関連付けられた例外はありません。</span><span class="sxs-lookup"><span data-stu-id="60fd8-133">This control pattern has no associated exceptions.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60fd8-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="60fd8-134">See also</span></span>
- [<span data-ttu-id="60fd8-135">UI Automation コントロール パターンの概要</span><span class="sxs-lookup"><span data-stu-id="60fd8-135">UI Automation Control Patterns Overview</span></span>](../../../docs/framework/ui-automation/ui-automation-control-patterns-overview.md)
- [<span data-ttu-id="60fd8-136">UI オートメーション プロバイダーでのコントロール パターンのサポート</span><span class="sxs-lookup"><span data-stu-id="60fd8-136">Support Control Patterns in a UI Automation Provider</span></span>](../../../docs/framework/ui-automation/support-control-patterns-in-a-ui-automation-provider.md)
- [<span data-ttu-id="60fd8-137">クライアントの UI オートメーション コントロール パターン</span><span class="sxs-lookup"><span data-stu-id="60fd8-137">UI Automation Control Patterns for Clients</span></span>](../../../docs/framework/ui-automation/ui-automation-control-patterns-for-clients.md)
- [<span data-ttu-id="60fd8-138">UI オートメーション Grid コントロール パターンの実装</span><span class="sxs-lookup"><span data-stu-id="60fd8-138">Implementing the UI Automation Grid Control Pattern</span></span>](../../../docs/framework/ui-automation/implementing-the-ui-automation-grid-control-pattern.md)
- [<span data-ttu-id="60fd8-139">UI Automation ツリーの概要</span><span class="sxs-lookup"><span data-stu-id="60fd8-139">UI Automation Tree Overview</span></span>](../../../docs/framework/ui-automation/ui-automation-tree-overview.md)
- [<span data-ttu-id="60fd8-140">UI オートメーションにおけるキャッシュの使用</span><span class="sxs-lookup"><span data-stu-id="60fd8-140">Use Caching in UI Automation</span></span>](../../../docs/framework/ui-automation/use-caching-in-ui-automation.md)
