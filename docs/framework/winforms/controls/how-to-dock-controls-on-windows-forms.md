---
title: '方法: Windows フォーム上のコントロールをドッキングします。'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], docking
- Explorer-style applications [Windows Forms], creating
- Windows Forms controls, filling client area
ms.assetid: bc11f2e4-e90a-4830-b0e2-f43b6e2b8bec
ms.openlocfilehash: f4a9d3bcf7f9db1634da2b2f06177c05061af28e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54733546"
---
# <a name="how-to-dock-controls-on-windows-forms"></a><span data-ttu-id="5ccf5-102">方法: Windows フォーム上のコントロールをドッキングします。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-102">How to: Dock Controls on Windows Forms</span></span>
<span data-ttu-id="5ccf5-103">コントロールをフォームの端にドッキングまたはコントロールのコンテナー (フォームまたはコンテナー コントロールのいずれか) を入力することがあることができます。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-103">You can dock controls to the edges of your form or have them fill the control's container (either a form or a container control).</span></span> <span data-ttu-id="5ccf5-104">たとえば、Windows エクスプ ローラーをドッキングその<xref:System.Windows.Forms.TreeView>、ウィンドウの左側にあるコントロールとその<xref:System.Windows.Forms.ListView>ウィンドウの右側にあるコントロール。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-104">For example, Windows Explorer docks its <xref:System.Windows.Forms.TreeView> control to the left side of the window and its <xref:System.Windows.Forms.ListView> control to the right side of the window.</span></span> <span data-ttu-id="5ccf5-105">使用して、<xref:System.Windows.Forms.Control.Dock%2A>ドッキングのモードを定義する表示されているすべての Windows フォーム コントロールのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-105">Use the <xref:System.Windows.Forms.Control.Dock%2A> property for all visible Windows Forms controls to define the docking mode.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5ccf5-106">逆の z オーダーでコントロールがドッキングされます。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-106">Controls are docked in reverse z-order.</span></span>  
  
 <span data-ttu-id="5ccf5-107"><xref:System.Windows.Forms.Control.Dock%2A>プロパティの対話、<xref:System.Windows.Forms.Control.AutoSize%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-107">The <xref:System.Windows.Forms.Control.Dock%2A> property interacts with the <xref:System.Windows.Forms.Control.AutoSize%2A> property.</span></span> <span data-ttu-id="5ccf5-108">詳細については、次を参照してください。 [AutoSize プロパティの概要](../../../../docs/framework/winforms/controls/autosize-property-overview.md)します。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-108">For more information, see [AutoSize Property Overview](../../../../docs/framework/winforms/controls/autosize-property-overview.md).</span></span>  
  
### <a name="to-dock-a-control"></a><span data-ttu-id="5ccf5-109">コントロールをドッキングするには</span><span class="sxs-lookup"><span data-stu-id="5ccf5-109">To dock a control</span></span>  
  
1.  <span data-ttu-id="5ccf5-110">ドッキングするコントロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-110">Select the control that you want to dock.</span></span>  
  
2.  <span data-ttu-id="5ccf5-111">[プロパティ] ウィンドウの右側にある矢印をクリックします。、<xref:System.Windows.Forms.Control.Dock%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-111">In the Properties window, click the arrow to the right of the <xref:System.Windows.Forms.Control.Dock%2A> property.</span></span>  
  
     <span data-ttu-id="5ccf5-112">一連の端とフォームの中央を表すボックスを示しています。 エディターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-112">An editor is displayed that shows a series of boxes representing the edges and the center of the form.</span></span>  
  
3.  <span data-ttu-id="5ccf5-113">コントロールをドッキングするフォームの端を表すボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-113">Click the button that represents the edge of the form where you want to dock the control.</span></span> <span data-ttu-id="5ccf5-114">コントロールのフォームまたはコンテナー コントロールの内容を入力するには、中央のボックスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-114">To fill the contents of the control's form or container control, click the center box.</span></span> <span data-ttu-id="5ccf5-115">クリックして **(なし)** ドッキングを無効にします。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-115">Click **(none)** to disable docking.</span></span>  
  
     <span data-ttu-id="5ccf5-116">コントロールのドッキングのエッジの境界に合わせてサイズを自動的にします。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-116">The control is automatically resized to fit the boundaries of the docked edge.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="5ccf5-117">継承されたコントロールである必要があります`Protected`ドッキングできるようにします。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-117">Inherited controls must be `Protected` to be able to be docked.</span></span> <span data-ttu-id="5ccf5-118">コントロールのアクセス レベルを変更するには、次のように設定します。 その**修飾子**プロパティ ウィンドウでプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5ccf5-118">To change the access level of a control, set its **Modifier** property in the Properties window.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ccf5-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ccf5-119">See also</span></span>
- [<span data-ttu-id="5ccf5-120">Windows フォーム コントロール</span><span class="sxs-lookup"><span data-stu-id="5ccf5-120">Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/index.md)
- [<span data-ttu-id="5ccf5-121">Windows フォームでのコントロールの配置</span><span class="sxs-lookup"><span data-stu-id="5ccf5-121">Arranging Controls on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/arranging-controls-on-windows-forms.md)
- [<span data-ttu-id="5ccf5-122">各 Windows フォーム コントロールのラベル設定とショートカットの作成</span><span class="sxs-lookup"><span data-stu-id="5ccf5-122">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](../../../../docs/framework/winforms/controls/labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [<span data-ttu-id="5ccf5-123">Windows フォームで使用するコントロール</span><span class="sxs-lookup"><span data-stu-id="5ccf5-123">Controls to Use on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)
- [<span data-ttu-id="5ccf5-124">Windows フォーム コントロールの機能別一覧</span><span class="sxs-lookup"><span data-stu-id="5ccf5-124">Windows Forms Controls by Function</span></span>](../../../../docs/framework/winforms/controls/windows-forms-controls-by-function.md)
- [<span data-ttu-id="5ccf5-125">方法: 固定およびドッキング FlowLayoutPanel コントロールで子コントロール</span><span class="sxs-lookup"><span data-stu-id="5ccf5-125">How to: Anchor and Dock Child Controls in a FlowLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [<span data-ttu-id="5ccf5-126">方法: 固定およびドッキング TableLayoutPanel コントロールで子コントロール</span><span class="sxs-lookup"><span data-stu-id="5ccf5-126">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="5ccf5-127">AutoSize プロパティの概要</span><span class="sxs-lookup"><span data-stu-id="5ccf5-127">AutoSize Property Overview</span></span>](../../../../docs/framework/winforms/controls/autosize-property-overview.md)
- [<span data-ttu-id="5ccf5-128">方法: Windows フォームにコントロールを固定</span><span class="sxs-lookup"><span data-stu-id="5ccf5-128">How to: Anchor Controls on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/how-to-anchor-controls-on-windows-forms.md)
