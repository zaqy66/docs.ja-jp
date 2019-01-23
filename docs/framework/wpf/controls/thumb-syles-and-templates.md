---
title: つまみのスタイルとテンプレート
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], Thumb
- styles [WPF], Thumb
- templates [WPF], Thumb
- Thumb [WPF], styles and templates
- ControlTemplate [WPF], Thumb
- parts [WPF], Thumb
ms.assetid: 86a49235-62d9-414e-923e-53126e3f930a
ms.openlocfilehash: e987932e00be09fdf5ac34bb2bfb24a890368a15
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596385"
---
# <a name="thumb-syles-and-templates"></a><span data-ttu-id="2493a-102">つまみのスタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="2493a-102">Thumb Syles and Templates</span></span>
<span data-ttu-id="2493a-103">このトピックでは、スタイルとテンプレートについて説明します、<xref:System.Windows.Controls.Primitives.Thumb>コントロール。</span><span class="sxs-lookup"><span data-stu-id="2493a-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Primitives.Thumb> control.</span></span> <span data-ttu-id="2493a-104">既定値を変更する<xref:System.Windows.Controls.ControlTemplate>固有の外観を制御します。</span><span class="sxs-lookup"><span data-stu-id="2493a-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="2493a-105">詳細については、「[ControlTemplate の作成による既存のコントロールの外観のカスタマイズ](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2493a-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="thumb-parts"></a><span data-ttu-id="2493a-106">Thumb パーツ</span><span class="sxs-lookup"><span data-stu-id="2493a-106">Thumb Parts</span></span>  
 <span data-ttu-id="2493a-107"><xref:System.Windows.Controls.Primitives.Thumb>コントロールには、名前付きパーツはありません。</span><span class="sxs-lookup"><span data-stu-id="2493a-107">The <xref:System.Windows.Controls.Primitives.Thumb> control does not have any named parts.</span></span>  
  
## <a name="thumb-states"></a><span data-ttu-id="2493a-108">つまみの状態</span><span class="sxs-lookup"><span data-stu-id="2493a-108">Thumb States</span></span>  
 <span data-ttu-id="2493a-109">次の表のビジュアルの状態、<xref:System.Windows.Controls.Primitives.Thumb>コントロール。</span><span class="sxs-lookup"><span data-stu-id="2493a-109">The following table lists the visual states for the <xref:System.Windows.Controls.Primitives.Thumb> control.</span></span>  
  
|<span data-ttu-id="2493a-110">VisualState 名</span><span class="sxs-lookup"><span data-stu-id="2493a-110">VisualState Name</span></span>|<span data-ttu-id="2493a-111">VisualStateGroup 名</span><span class="sxs-lookup"><span data-stu-id="2493a-111">VisualStateGroup Name</span></span>|<span data-ttu-id="2493a-112">説明</span><span class="sxs-lookup"><span data-stu-id="2493a-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="2493a-113">標準</span><span class="sxs-lookup"><span data-stu-id="2493a-113">Normal</span></span>|<span data-ttu-id="2493a-114">CommonStates</span><span class="sxs-lookup"><span data-stu-id="2493a-114">CommonStates</span></span>|<span data-ttu-id="2493a-115">既定の状態です。</span><span class="sxs-lookup"><span data-stu-id="2493a-115">The default state.</span></span>|  
|<span data-ttu-id="2493a-116">MouseOver</span><span class="sxs-lookup"><span data-stu-id="2493a-116">MouseOver</span></span>|<span data-ttu-id="2493a-117">CommonStates</span><span class="sxs-lookup"><span data-stu-id="2493a-117">CommonStates</span></span>|<span data-ttu-id="2493a-118">マウス ポインターがコントロール上に配置されています。</span><span class="sxs-lookup"><span data-stu-id="2493a-118">The mouse pointer is positioned over the control.</span></span>|  
|<span data-ttu-id="2493a-119">押されている</span><span class="sxs-lookup"><span data-stu-id="2493a-119">Pressed</span></span>|<span data-ttu-id="2493a-120">CommonStates</span><span class="sxs-lookup"><span data-stu-id="2493a-120">CommonStates</span></span>|<span data-ttu-id="2493a-121">コントロールが押されています。</span><span class="sxs-lookup"><span data-stu-id="2493a-121">The control is pressed.</span></span>|  
|<span data-ttu-id="2493a-122">無効</span><span class="sxs-lookup"><span data-stu-id="2493a-122">Disabled</span></span>|<span data-ttu-id="2493a-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="2493a-123">CommonStates</span></span>|<span data-ttu-id="2493a-124">コントロールが無効になっています。</span><span class="sxs-lookup"><span data-stu-id="2493a-124">The control is disabled.</span></span>|  
|<span data-ttu-id="2493a-125">フォーカスされている</span><span class="sxs-lookup"><span data-stu-id="2493a-125">Focused</span></span>|<span data-ttu-id="2493a-126">FocusStates</span><span class="sxs-lookup"><span data-stu-id="2493a-126">FocusStates</span></span>|<span data-ttu-id="2493a-127">コントロールにフォーカスがあります。</span><span class="sxs-lookup"><span data-stu-id="2493a-127">The control has focus.</span></span>|  
|<span data-ttu-id="2493a-128">フォーカスされていない</span><span class="sxs-lookup"><span data-stu-id="2493a-128">Unfocused</span></span>|<span data-ttu-id="2493a-129">FocusStates</span><span class="sxs-lookup"><span data-stu-id="2493a-129">FocusStates</span></span>|<span data-ttu-id="2493a-130">コントロールにフォーカスがありません。</span><span class="sxs-lookup"><span data-stu-id="2493a-130">The control does not have focus.</span></span>|  
|<span data-ttu-id="2493a-131">有効</span><span class="sxs-lookup"><span data-stu-id="2493a-131">Valid</span></span>|<span data-ttu-id="2493a-132">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="2493a-132">ValidationStates</span></span>|<span data-ttu-id="2493a-133">コントロールを使用して、<xref:System.Windows.Controls.Validation>クラスおよび<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`false`します。</span><span class="sxs-lookup"><span data-stu-id="2493a-133">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="2493a-134">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="2493a-134">InvalidFocused</span></span>|<span data-ttu-id="2493a-135">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="2493a-135">ValidationStates</span></span>|<span data-ttu-id="2493a-136"><xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`true`がコントロールにフォーカスします。</span><span class="sxs-lookup"><span data-stu-id="2493a-136">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="2493a-137">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="2493a-137">InvalidUnfocused</span></span>|<span data-ttu-id="2493a-138">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="2493a-138">ValidationStates</span></span>|<span data-ttu-id="2493a-139"><xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`true`がコントロールにフォーカスがないです。</span><span class="sxs-lookup"><span data-stu-id="2493a-139">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="thumb-controltemplate-example"></a><span data-ttu-id="2493a-140">Thumb ControlTemplate の例</span><span class="sxs-lookup"><span data-stu-id="2493a-140">Thumb ControlTemplate Example</span></span>  
 <span data-ttu-id="2493a-141">次の例は、定義する方法を示します、<xref:System.Windows.Controls.ControlTemplate>の<xref:System.Windows.Controls.Primitives.Thumb>コントロール。</span><span class="sxs-lookup"><span data-stu-id="2493a-141">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Primitives.Thumb> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Thumb](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/slider.xaml#thumb)]  
  
 <span data-ttu-id="2493a-142">前の例では、次のリソースの 1 つ以上を使用します。</span><span class="sxs-lookup"><span data-stu-id="2493a-142">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="2493a-143">完全なサンプルについては、[Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2493a-143">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2493a-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="2493a-144">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="2493a-145">コントロールのスタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="2493a-145">Control Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)
- [<span data-ttu-id="2493a-146">コントロールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="2493a-146">Control Customization</span></span>](../../../../docs/framework/wpf/controls/control-customization.md)
- [<span data-ttu-id="2493a-147">スタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="2493a-147">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)
- [<span data-ttu-id="2493a-148">ControlTemplate の作成による既存のコントロールの外観のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="2493a-148">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
