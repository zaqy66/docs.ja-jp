---
title: ScrollViewer のスタイルとテンプレート
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], ScrollViewer
- states [WPF], ScrollViewer
- styles [WPF], ScrollViewer
- templates [WPF], ScrollViewer
- ControlTemplate [WPF], ScrollViewer
- ScrollViewer [WPF], styles and templates
ms.assetid: dffdd822-ae69-4946-abaf-710860cd65b2
ms.openlocfilehash: 1f5c3d98d6fe2814addaad3e6c898f5341fac7f9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672202"
---
# <a name="scrollviewer-styles-and-templates"></a><span data-ttu-id="aa287-102">ScrollViewer のスタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="aa287-102">ScrollViewer Styles and Templates</span></span>
<span data-ttu-id="aa287-103">このトピックでは、スタイルとテンプレートについて説明します、<xref:System.Windows.Controls.ScrollViewer>コントロール。</span><span class="sxs-lookup"><span data-stu-id="aa287-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span> <span data-ttu-id="aa287-104">既定値を変更する<xref:System.Windows.Controls.ControlTemplate>固有の外観を制御します。</span><span class="sxs-lookup"><span data-stu-id="aa287-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="aa287-105">詳細については、「[ControlTemplate の作成による既存のコントロールの外観のカスタマイズ](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa287-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="scrollviewer-parts"></a><span data-ttu-id="aa287-106">ScrollViewer パーツ</span><span class="sxs-lookup"><span data-stu-id="aa287-106">ScrollViewer Parts</span></span>  
 <span data-ttu-id="aa287-107">次の表に、名前付きパーツ、<xref:System.Windows.Controls.ScrollViewer>コントロール。</span><span class="sxs-lookup"><span data-stu-id="aa287-107">The following table lists the named parts for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span>  
  
|<span data-ttu-id="aa287-108">パーツ</span><span class="sxs-lookup"><span data-stu-id="aa287-108">Part</span></span>|<span data-ttu-id="aa287-109">型</span><span class="sxs-lookup"><span data-stu-id="aa287-109">Type</span></span>|<span data-ttu-id="aa287-110">説明</span><span class="sxs-lookup"><span data-stu-id="aa287-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="aa287-111">PART_ScrollContentPresenter</span><span class="sxs-lookup"><span data-stu-id="aa287-111">PART_ScrollContentPresenter</span></span>|<xref:System.Windows.Controls.ScrollContentPresenter>|<span data-ttu-id="aa287-112">内のコンテンツのプレース ホルダー、<xref:System.Windows.Controls.ScrollViewer>します。</span><span class="sxs-lookup"><span data-stu-id="aa287-112">The placeholder for content in the <xref:System.Windows.Controls.ScrollViewer>.</span></span>|  
|<span data-ttu-id="aa287-113">PART_HorizontalScrollBar</span><span class="sxs-lookup"><span data-stu-id="aa287-113">PART_HorizontalScrollBar</span></span>|<xref:System.Windows.Controls.Primitives.ScrollBar>|<span data-ttu-id="aa287-114"><xref:System.Windows.Controls.Primitives.ScrollBar>コンテンツを水平方向にスクロールするために使用します。</span><span class="sxs-lookup"><span data-stu-id="aa287-114">The <xref:System.Windows.Controls.Primitives.ScrollBar> used to scroll the content horizontally.</span></span>|  
|<span data-ttu-id="aa287-115">PART_VerticalScrollBar</span><span class="sxs-lookup"><span data-stu-id="aa287-115">PART_VerticalScrollBar</span></span>|<xref:System.Windows.Controls.Primitives.ScrollBar>|<span data-ttu-id="aa287-116"><xref:System.Windows.Controls.Primitives.ScrollBar>コンテンツを垂直方向にスクロールするために使用します。</span><span class="sxs-lookup"><span data-stu-id="aa287-116">The <xref:System.Windows.Controls.Primitives.ScrollBar> used to scroll the content vertically.</span></span>|  
  
## <a name="scrollviewer-states"></a><span data-ttu-id="aa287-117">ScrollViewer の状態</span><span class="sxs-lookup"><span data-stu-id="aa287-117">ScrollViewer States</span></span>  
 <span data-ttu-id="aa287-118">次の表のビジュアルの状態、<xref:System.Windows.Controls.ScrollViewer>コントロール。</span><span class="sxs-lookup"><span data-stu-id="aa287-118">The following table lists the visual states for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span>  
  
|<span data-ttu-id="aa287-119">VisualState 名</span><span class="sxs-lookup"><span data-stu-id="aa287-119">VisualState Name</span></span>|<span data-ttu-id="aa287-120">VisualStateGroup 名</span><span class="sxs-lookup"><span data-stu-id="aa287-120">VisualStateGroup Name</span></span>|<span data-ttu-id="aa287-121">説明</span><span class="sxs-lookup"><span data-stu-id="aa287-121">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="aa287-122">有効</span><span class="sxs-lookup"><span data-stu-id="aa287-122">Valid</span></span>|<span data-ttu-id="aa287-123">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="aa287-123">ValidationStates</span></span>|<span data-ttu-id="aa287-124">コントロールを使用して、<xref:System.Windows.Controls.Validation>クラスおよび<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`false`します。</span><span class="sxs-lookup"><span data-stu-id="aa287-124">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="aa287-125">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="aa287-125">InvalidFocused</span></span>|<span data-ttu-id="aa287-126">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="aa287-126">ValidationStates</span></span>|<span data-ttu-id="aa287-127"><xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`true`がコントロールにフォーカスします。</span><span class="sxs-lookup"><span data-stu-id="aa287-127">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="aa287-128">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="aa287-128">InvalidUnfocused</span></span>|<span data-ttu-id="aa287-129">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="aa287-129">ValidationStates</span></span>|<span data-ttu-id="aa287-130"><xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`true`がコントロールにフォーカスがないです。</span><span class="sxs-lookup"><span data-stu-id="aa287-130">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="scrollviewer-controltemplate-example"></a><span data-ttu-id="aa287-131">ScrollViewer ControlTemplate の例</span><span class="sxs-lookup"><span data-stu-id="aa287-131">ScrollViewer ControlTemplate Example</span></span>  
 <span data-ttu-id="aa287-132">次の例は、定義する方法を示します、<xref:System.Windows.Controls.ControlTemplate>の<xref:System.Windows.Controls.ScrollViewer>コントロール。</span><span class="sxs-lookup"><span data-stu-id="aa287-132">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ScrollViewer](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/scrollviewer.xaml#scrollviewer)]  
  
 <span data-ttu-id="aa287-133">前の例では、次のリソースの 1 つ以上を使用します。</span><span class="sxs-lookup"><span data-stu-id="aa287-133">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="aa287-134">完全なサンプルについては、[Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa287-134">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa287-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa287-135">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="aa287-136">コントロールのスタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="aa287-136">Control Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)
- [<span data-ttu-id="aa287-137">コントロールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="aa287-137">Control Customization</span></span>](../../../../docs/framework/wpf/controls/control-customization.md)
- [<span data-ttu-id="aa287-138">スタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="aa287-138">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)
- [<span data-ttu-id="aa287-139">ControlTemplate の作成による既存のコントロールの外観のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="aa287-139">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
