---
title: GroupBox のスタイルとテンプレート
ms.date: 03/30/2017
helpviewer_keywords:
- ControlTemplate [WPF], GroupBox
- parts [WPF], GroupBox
- GroupBox [WPF], styles and templates
- states [WPF], GroupBox
- styles [WPF], GroupBox
- templates [WPF], GroupBox
ms.assetid: 33df7037-0a1b-476f-b9d0-41566a777699
ms.openlocfilehash: c67dd3fe7163bc09c74fb62fc448005334a24395
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54685127"
---
# <a name="groupbox-styles-and-templates"></a><span data-ttu-id="70281-102">GroupBox のスタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="70281-102">GroupBox Styles and Templates</span></span>
<a name="introduction"></a> <span data-ttu-id="70281-103">このトピックでは、スタイルとテンプレートについて説明します、<xref:System.Windows.Controls.GroupBox>コントロール。</span><span class="sxs-lookup"><span data-stu-id="70281-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.GroupBox> control.</span></span> <span data-ttu-id="70281-104">既定値を変更する<xref:System.Windows.Controls.ControlTemplate>固有の外観を制御します。</span><span class="sxs-lookup"><span data-stu-id="70281-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="70281-105">詳細については、「[ControlTemplate の作成による既存のコントロールの外観のカスタマイズ](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70281-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
<a name="groupbox_parts"></a>   
## <a name="groupbox-parts"></a><span data-ttu-id="70281-106">GroupBox のパーツ</span><span class="sxs-lookup"><span data-stu-id="70281-106">GroupBox Parts</span></span>  
 <span data-ttu-id="70281-107"><xref:System.Windows.Controls.GroupBox>コントロールには、名前付きパーツはありません。</span><span class="sxs-lookup"><span data-stu-id="70281-107">The <xref:System.Windows.Controls.GroupBox> control does not have any named parts.</span></span>  
  
<a name="groupbox_states"></a>   
## <a name="groupbox-states"></a><span data-ttu-id="70281-108">GroupBox の状態</span><span class="sxs-lookup"><span data-stu-id="70281-108">GroupBox States</span></span>  
 <span data-ttu-id="70281-109">次の表のビジュアルの状態、<xref:System.Windows.Controls.GroupBox>コントロール。</span><span class="sxs-lookup"><span data-stu-id="70281-109">The following table lists the visual states for the <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
|<span data-ttu-id="70281-110">VisualState 名</span><span class="sxs-lookup"><span data-stu-id="70281-110">VisualState Name</span></span>|<span data-ttu-id="70281-111">VisualStateGroup 名</span><span class="sxs-lookup"><span data-stu-id="70281-111">VisualStateGroup Name</span></span>|<span data-ttu-id="70281-112">説明</span><span class="sxs-lookup"><span data-stu-id="70281-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="70281-113">有効</span><span class="sxs-lookup"><span data-stu-id="70281-113">Valid</span></span>|<span data-ttu-id="70281-114">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="70281-114">ValidationStates</span></span>|<span data-ttu-id="70281-115">コントロールを使用して、<xref:System.Windows.Controls.Validation>クラスおよび<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`false`します。</span><span class="sxs-lookup"><span data-stu-id="70281-115">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="70281-116">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="70281-116">InvalidFocused</span></span>|<span data-ttu-id="70281-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="70281-117">ValidationStates</span></span>|<span data-ttu-id="70281-118"><xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`true`がコントロールにフォーカスします。</span><span class="sxs-lookup"><span data-stu-id="70281-118">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="70281-119">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="70281-119">InvalidUnfocused</span></span>|<span data-ttu-id="70281-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="70281-120">ValidationStates</span></span>|<span data-ttu-id="70281-121"><xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>添付プロパティは`true`がコントロールにフォーカスがないです。</span><span class="sxs-lookup"><span data-stu-id="70281-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
<a name="groupbox_controltemplate_example"></a>   
## <a name="groupbox-controltemplate-example"></a><span data-ttu-id="70281-122">GroupBox ControlTemplate の例</span><span class="sxs-lookup"><span data-stu-id="70281-122">GroupBox ControlTemplate Example</span></span>  
 <span data-ttu-id="70281-123">次の例は、定義する方法を示します、<xref:System.Windows.Controls.ControlTemplate>の<xref:System.Windows.Controls.GroupBox>コントロール。</span><span class="sxs-lookup"><span data-stu-id="70281-123">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#GroupBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/groupbox.xaml#groupbox)]  
  
 <span data-ttu-id="70281-124"><xref:System.Windows.Controls.ControlTemplate>次のリソースの 1 つ以上を使用します。</span><span class="sxs-lookup"><span data-stu-id="70281-124">The <xref:System.Windows.Controls.ControlTemplate> uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="70281-125">完全なサンプルについては、[Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70281-125">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70281-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="70281-126">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="70281-127">コントロールのスタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="70281-127">Control Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)
- [<span data-ttu-id="70281-128">コントロールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="70281-128">Control Customization</span></span>](../../../../docs/framework/wpf/controls/control-customization.md)
- [<span data-ttu-id="70281-129">スタイルとテンプレート</span><span class="sxs-lookup"><span data-stu-id="70281-129">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)
- [<span data-ttu-id="70281-130">ControlTemplate の作成による既存のコントロールの外観のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="70281-130">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
