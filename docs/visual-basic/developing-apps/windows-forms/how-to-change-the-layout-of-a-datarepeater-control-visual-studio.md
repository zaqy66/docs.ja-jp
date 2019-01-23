---
title: '方法: DataRepeater コントロール (Visual Studio) のレイアウトを変更します。'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, changing layout style
- DataRepeater, changing orientation
ms.assetid: 33aa8fd5-ac63-4bd0-ba13-8c2ab17e7824
ms.openlocfilehash: 3389daa6383444b48faab4c5383b281e44349bce
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54625602"
---
# <a name="how-to-change-the-layout-of-a-datarepeater-control-visual-studio"></a><span data-ttu-id="1ae16-102">方法: DataRepeater コントロール (Visual Studio) のレイアウトを変更します。</span><span class="sxs-lookup"><span data-stu-id="1ae16-102">How to: Change the Layout of a DataRepeater Control (Visual Studio)</span></span>
<span data-ttu-id="1ae16-103"><xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> (垂直方向にスクロール バーの項目) 垂直または水平方向 (水平方向にスクロール バーの項目) のいずれかで表示できるコントロールの向き。</span><span class="sxs-lookup"><span data-stu-id="1ae16-103">The <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control can be displayed in either a vertical (items scroll vertically) or horizontal (items scroll horizontally) orientation.</span></span> <span data-ttu-id="1ae16-104">デザイン時または実行時に向きを変更するには変更することで、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="1ae16-104">You can change the orientation at design time or at run time by changing the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A> property.</span></span> <span data-ttu-id="1ae16-105">変更した場合、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>実行時にプロパティをすることもサイズを変更する、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>と子コントロールの位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="1ae16-105">If you change the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A> property at run time, you may also want to resize the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> and reposition the child controls.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1ae16-106">上のコントロールの位置を変更する場合、 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> 、実行時に呼び出す必要があります、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate%2A>と<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate%2A>メソッドは、コントロールを移動するコード ブロックの末尾、先頭にあります。</span><span class="sxs-lookup"><span data-stu-id="1ae16-106">If you reposition controls on the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> at run time, you will need to call the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate%2A> and <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate%2A> methods at the beginning and end of the code block that repositions the controls.</span></span>  
  
### <a name="to-change-the-layout-at-design-time"></a><span data-ttu-id="1ae16-107">デザイン時にレイアウトを変更するには</span><span class="sxs-lookup"><span data-stu-id="1ae16-107">To change the layout at design time</span></span>  
  
1.  <span data-ttu-id="1ae16-108">Windows フォーム デザイナーで、選択、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。</span><span class="sxs-lookup"><span data-stu-id="1ae16-108">In the Windows Forms Designer, select the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="1ae16-109">外側の境界線を選択する必要があります、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>上ではなく、コントロールの下の領域をクリックしてコントロール<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>リージョン。</span><span class="sxs-lookup"><span data-stu-id="1ae16-109">You must select the outer border of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control by clicking in the lower region of the control, not in the upper <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> region.</span></span>  
  
2.  <span data-ttu-id="1ae16-110">[プロパティ] ウィンドウで次のように設定します。、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>プロパティを<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Vertical>または<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Horizontal>します。</span><span class="sxs-lookup"><span data-stu-id="1ae16-110">In the Properties window, set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A> property to either <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Vertical> or <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Horizontal>.</span></span>  
  
### <a name="to-change-the-layout-at-run-time"></a><span data-ttu-id="1ae16-111">実行時にレイアウトを変更するには</span><span class="sxs-lookup"><span data-stu-id="1ae16-111">To change the layout at run time</span></span>  
  
1.  <span data-ttu-id="1ae16-112">次のコードをボタンまたはメニューに追加`Click`イベント ハンドラー。</span><span class="sxs-lookup"><span data-stu-id="1ae16-112">Add the following code to a button or menu `Click` event handler:</span></span>  
  
     [!code-csharp[VbPowerPacksDataRepeaterLayout#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterLayout#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_1.vb)]  
  
2.  <span data-ttu-id="1ae16-113">ほとんどの場合、サイズを変更する例」のセクションに示されているようなコードを追加しますが、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>および新しい向きに合わせてコントロールを再配置します。</span><span class="sxs-lookup"><span data-stu-id="1ae16-113">In most cases, you will want to add code similar to that shown in the Example section to resize the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> and rearrange controls to fit the new orientation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1ae16-114">例</span><span class="sxs-lookup"><span data-stu-id="1ae16-114">Example</span></span>  
 <span data-ttu-id="1ae16-115">次の例に応答する方法を示しています、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyleChanged>イベント ハンドラーでイベント。</span><span class="sxs-lookup"><span data-stu-id="1ae16-115">The following example shows how to respond to the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyleChanged> event in an event handler.</span></span> <span data-ttu-id="1ae16-116">この例が必要です、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>という名前のコントロール`DataRepeater1`フォームにその<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>2 つを含めることが<xref:System.Windows.Forms.TextBox>という名前のコントロール`TextBox1`と`TextBox2`します。</span><span class="sxs-lookup"><span data-stu-id="1ae16-116">This example requires that you have a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control named `DataRepeater1` on a form and that its <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> contain two <xref:System.Windows.Forms.TextBox> controls named `TextBox1` and `TextBox2`.</span></span>  
  
 [!code-csharp[VbPowerPacksDataRepeaterLayout#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_2.cs)]
 [!code-vb[VbPowerPacksDataRepeaterLayout#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="1ae16-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ae16-117">See also</span></span>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate%2A>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate%2A>
- [<span data-ttu-id="1ae16-118">DataRepeater コントロールの概要</span><span class="sxs-lookup"><span data-stu-id="1ae16-118">Introduction to the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="1ae16-119">DataRepeater コントロールのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="1ae16-119">Troubleshooting the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="1ae16-120">方法: DataRepeater コントロールの外観を変更します。</span><span class="sxs-lookup"><span data-stu-id="1ae16-120">How to: Change the Appearance of a DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
