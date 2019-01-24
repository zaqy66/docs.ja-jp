---
title: StatusBar のスタイルとテンプレート
ms.date: 03/30/2017
helpviewer_keywords:
- ControlTemplate [WPF], StatusBar
- styles [WPF], StatusBar
- templates [WPF], StatusBar
- states [WPF], StatusBar
- parts [WPF], StatusBar
- StatusBar [WPF], styles and templates
ms.assetid: 9f5e1c25-81eb-4756-a0ac-d9e1fbe33ee2
ms.openlocfilehash: ee3bd060268d5ab6f713a74f871d7de0dd77782b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54660464"
---
# <a name="statusbar-styles-and-templates"></a><span data-ttu-id="0dc53-102">StatusBar のスタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="0dc53-102">StatusBar Styles and Templates</span></span>
<span data-ttu-id="0dc53-103">このトピックでは、スタイルとテンプレートについて説明します、<xref:System.Windows.Controls.Primitives.StatusBar>コントロール。</span><span class="sxs-lookup"><span data-stu-id="0dc53-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Primitives.StatusBar> control.</span></span> <span data-ttu-id="0dc53-104">既定値を変更する<xref:System.Windows.Controls.ControlTemplate>固有の外観を制御します。</span><span class="sxs-lookup"><span data-stu-id="0dc53-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="0dc53-105">詳細については、「[ControlTemplate の作成による既存のコントロールの外観のカスタマイズ](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0dc53-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="statusbar-parts"></a><span data-ttu-id="0dc53-106">ステータス バーの部品</span><span class="sxs-lookup"><span data-stu-id="0dc53-106">StatusBar Parts</span></span>  
 <span data-ttu-id="0dc53-107"><xref:System.Windows.Controls.Primitives.StatusBar>コントロールには、名前付きパーツはありません。</span><span class="sxs-lookup"><span data-stu-id="0dc53-107">The <xref:System.Windows.Controls.Primitives.StatusBar> control does not have any named parts.</span></span>  
  
## <a name="statusbar-states"></a><span data-ttu-id="0dc53-108">ステータス バーの状態</span><span class="sxs-lookup"><span data-stu-id="0dc53-108">StatusBar States</span></span>  
 <span data-ttu-id="0dc53-109">次の表のビジュアルの状態、<xref:System.Windows.Controls.Primitives.StatusBar>コントロール。</span><span class="sxs-lookup"><span data-stu-id="0dc53-109">The following table lists the visual states for the <xref:System.Windows.Controls.Primitives.StatusBar> control.</span></span>  
  
|<span data-ttu-id="0dc53-110">VisualState 名</span><span class="sxs-lookup"><span data-stu-id="0dc53-110">VisualState Name</span></span>|<span data-ttu-id="0dc53-111">VisualStateGroup 名</span><span class="sxs-lookup"><span data-stu-id="0dc53-111">VisualStateGroup Name</span></span>|<span data-ttu-id="0dc53-112">説明</span><span class="sxs-lookup"><span data-stu-id="0dc53-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="0dc53-113">有効</span><span class="sxs-lookup"><span data-stu-id="0dc53-113">Valid</span></span>|<span data-ttu-id="0dc53-114">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0dc53-114">ValidationStates</span></span>|<span data-ttu-id="0dc53-115">コントロールを使用して、<xref:System.Windows.Controls.Validation>クラスおよび<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`false`します。</span><span class="sxs-lookup"><span data-stu-id="0dc53-115">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="0dc53-116">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="0dc53-116">InvalidFocused</span></span>|<span data-ttu-id="0dc53-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0dc53-117">ValidationStates</span></span>|<span data-ttu-id="0dc53-118"><xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`true`がコントロールにフォーカスします。</span><span class="sxs-lookup"><span data-stu-id="0dc53-118">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="0dc53-119">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="0dc53-119">InvalidUnfocused</span></span>|<span data-ttu-id="0dc53-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0dc53-120">ValidationStates</span></span>|<span data-ttu-id="0dc53-121"><xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`true`がコントロールにフォーカスがないです。</span><span class="sxs-lookup"><span data-stu-id="0dc53-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="statusbaritem-parts"></a><span data-ttu-id="0dc53-122">StatusBarItem パーツ</span><span class="sxs-lookup"><span data-stu-id="0dc53-122">StatusBarItem Parts</span></span>  
 <span data-ttu-id="0dc53-123"><xref:System.Windows.Controls.Primitives.StatusBarItem>コントロールには、名前付きパーツはありません。</span><span class="sxs-lookup"><span data-stu-id="0dc53-123">The <xref:System.Windows.Controls.Primitives.StatusBarItem> control does not have any named parts.</span></span>  
  
## <a name="statusbar-states"></a><span data-ttu-id="0dc53-124">ステータス バーの状態</span><span class="sxs-lookup"><span data-stu-id="0dc53-124">StatusBar States</span></span>  
 <span data-ttu-id="0dc53-125">次の表のビジュアルの状態、<xref:System.Windows.Controls.Primitives.StatusBarItem>コントロール。</span><span class="sxs-lookup"><span data-stu-id="0dc53-125">The following table lists the visual states for the <xref:System.Windows.Controls.Primitives.StatusBarItem> control.</span></span>  
  
|<span data-ttu-id="0dc53-126">VisualState 名</span><span class="sxs-lookup"><span data-stu-id="0dc53-126">VisualState Name</span></span>|<span data-ttu-id="0dc53-127">VisualStateGroup 名</span><span class="sxs-lookup"><span data-stu-id="0dc53-127">VisualStateGroup Name</span></span>|<span data-ttu-id="0dc53-128">説明</span><span class="sxs-lookup"><span data-stu-id="0dc53-128">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="0dc53-129">有効</span><span class="sxs-lookup"><span data-stu-id="0dc53-129">Valid</span></span>|<span data-ttu-id="0dc53-130">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0dc53-130">ValidationStates</span></span>|<span data-ttu-id="0dc53-131">コントロールを使用して、<xref:System.Windows.Controls.Validation>クラスおよび<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`false`します。</span><span class="sxs-lookup"><span data-stu-id="0dc53-131">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="0dc53-132">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="0dc53-132">InvalidFocused</span></span>|<span data-ttu-id="0dc53-133">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0dc53-133">ValidationStates</span></span>|<span data-ttu-id="0dc53-134"><xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`true`がコントロールにフォーカスします。</span><span class="sxs-lookup"><span data-stu-id="0dc53-134">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="0dc53-135">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="0dc53-135">InvalidUnfocused</span></span>|<span data-ttu-id="0dc53-136">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0dc53-136">ValidationStates</span></span>|<span data-ttu-id="0dc53-137"><xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`true`がコントロールにフォーカスがないです。</span><span class="sxs-lookup"><span data-stu-id="0dc53-137">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="statusbar-controltemplate-example"></a><span data-ttu-id="0dc53-138">StatusBar ControlTemplate の例</span><span class="sxs-lookup"><span data-stu-id="0dc53-138">StatusBar ControlTemplate Example</span></span>  
 <span data-ttu-id="0dc53-139">次の例は、定義する方法を示します、<xref:System.Windows.Controls.ControlTemplate>の<xref:System.Windows.Controls.Primitives.StatusBar>コントロール。</span><span class="sxs-lookup"><span data-stu-id="0dc53-139">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Primitives.StatusBar> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#StatusBar](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/statusbar.xaml#statusbar)]  
  
 <span data-ttu-id="0dc53-140"><xref:System.Windows.Controls.ControlTemplate>次のリソースの 1 つ以上を使用します。</span><span class="sxs-lookup"><span data-stu-id="0dc53-140">The <xref:System.Windows.Controls.ControlTemplate> uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="0dc53-141">完全なサンプルについては、[Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0dc53-141">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0dc53-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="0dc53-142">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="0dc53-143">コントロールのスタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="0dc53-143">Control Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)
- [<span data-ttu-id="0dc53-144">コントロールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="0dc53-144">Control Customization</span></span>](../../../../docs/framework/wpf/controls/control-customization.md)
- [<span data-ttu-id="0dc53-145">スタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="0dc53-145">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)
- [<span data-ttu-id="0dc53-146">ControlTemplate の作成による既存のコントロールの外観のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="0dc53-146">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
