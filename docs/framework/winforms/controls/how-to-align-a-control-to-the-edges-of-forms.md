---
title: '方法: コントロールをフォームの端を揃える'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Dock property [Windows Forms], aligning controls (using code)
- forms [Windows Forms], aligning controls
- controls [Windows Forms], aligning on forms
- custom controls [Windows Forms], docking using code
ms.assetid: 5994cb59-242b-4e75-bd0e-62879c34d702
ms.openlocfilehash: ba5e9fc92f2805206f6c3796689898f3ff845896
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610410"
---
# <a name="how-to-align-a-control-to-the-edges-of-forms"></a><span data-ttu-id="87438-102">方法: コントロールをフォームの端を揃える</span><span class="sxs-lookup"><span data-stu-id="87438-102">How to: Align a Control to the Edges of Forms</span></span>
<span data-ttu-id="87438-103"><xref:System.Windows.Forms.Control.Dock%2A> プロパティを設定することにより、フォームの端に合わせてコントロールを配置することができます。</span><span class="sxs-lookup"><span data-stu-id="87438-103">You can make your control align to the edge of your forms by setting the <xref:System.Windows.Forms.Control.Dock%2A> property.</span></span> <span data-ttu-id="87438-104">このプロパティは、フォーム内のコントロールの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="87438-104">This property designates where your control resides in the form.</span></span> <span data-ttu-id="87438-105"><xref:System.Windows.Forms.Control.Dock%2A> プロパティには次の値のいずれかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="87438-105">The <xref:System.Windows.Forms.Control.Dock%2A> property can be set to the following values:</span></span>  
  
|<span data-ttu-id="87438-106">設定</span><span class="sxs-lookup"><span data-stu-id="87438-106">Setting</span></span>|<span data-ttu-id="87438-107">コントロールへの影響</span><span class="sxs-lookup"><span data-stu-id="87438-107">Effect on your control</span></span>|  
|-------------|----------------------------|  
|<xref:System.Windows.Forms.DockStyle.Bottom>|<span data-ttu-id="87438-108">フォームの下部にドッキングします。</span><span class="sxs-lookup"><span data-stu-id="87438-108">Docks to the bottom of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Fill>|<span data-ttu-id="87438-109">フォームの残りの全スペースを埋めます。</span><span class="sxs-lookup"><span data-stu-id="87438-109">Fills all remaining space in the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Left>|<span data-ttu-id="87438-110">フォームの左側にドッキングします。</span><span class="sxs-lookup"><span data-stu-id="87438-110">Docks to the left side of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.None>|<span data-ttu-id="87438-111">どこにもドッキングせず、その <xref:System.Windows.Forms.Control.Location%2A> プロパティで指定された位置に表示されます。</span><span class="sxs-lookup"><span data-stu-id="87438-111">Does not dock anywhere, and it appears at the location specified by its <xref:System.Windows.Forms.Control.Location%2A> property.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Right>|<span data-ttu-id="87438-112">フォームの右側にドッキングします。</span><span class="sxs-lookup"><span data-stu-id="87438-112">Docks to the right side of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Top>|<span data-ttu-id="87438-113">フォームの上部にドッキングします。</span><span class="sxs-lookup"><span data-stu-id="87438-113">Docks to the top of the form.</span></span>|  
  
 <span data-ttu-id="87438-114">Visual Studio では、この機能のデザイン時サポートがあります。</span><span class="sxs-lookup"><span data-stu-id="87438-114">There is design-time support for this feature in Visual Studio.</span></span>  
  
### <a name="to-set-the-dock-property-for-your-control-at-run-time"></a><span data-ttu-id="87438-115">実行時にコントロールの Dock プロパティを設定するには</span><span class="sxs-lookup"><span data-stu-id="87438-115">To set the Dock property for your control at run time</span></span>  
  
1.  <span data-ttu-id="87438-116">コードで <xref:System.Windows.Forms.Control.Dock%2A> プロパティを適切な値に設定します。</span><span class="sxs-lookup"><span data-stu-id="87438-116">Set the <xref:System.Windows.Forms.Control.Dock%2A> property to the appropriate value in code.</span></span>  
  
    ```vb  
    ' To set the Dock property internally.  
    Me.Dock = DockStyle.Top  
    ' To set the Dock property from another object.  
    UserControl1.Dock = DockStyle.Top  
    ```  
  
    ```csharp  
    // To set the Dock property internally.  
    this.Dock = DockStyle.Top;  
    // To set the Dock property from another object.  
    UserControl1.Dock = DockStyle.Top;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="87438-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="87438-117">See also</span></span>
- <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType>
- [<span data-ttu-id="87438-118">.NET Framework を使用したカスタム Windows フォーム コントロールの開発</span><span class="sxs-lookup"><span data-stu-id="87438-118">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](../../../../docs/framework/winforms/controls/developing-custom-windows-forms-controls.md)
- [<span data-ttu-id="87438-119">方法: 固定およびドッキング FlowLayoutPanel コントロールで子コントロール</span><span class="sxs-lookup"><span data-stu-id="87438-119">How to: Anchor and Dock Child Controls in a FlowLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [<span data-ttu-id="87438-120">方法: 固定およびドッキング TableLayoutPanel コントロールで子コントロール</span><span class="sxs-lookup"><span data-stu-id="87438-120">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="87438-121">AutoSize プロパティの概要</span><span class="sxs-lookup"><span data-stu-id="87438-121">AutoSize Property Overview</span></span>](../../../../docs/framework/winforms/controls/autosize-property-overview.md)
