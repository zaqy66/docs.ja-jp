---
title: '方法: OvalShape コントロールおよび RectangleShape コントロール (Visual Studio) を使用して図形を描画します。'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- OvalShape control [Visual Basic]
- shapes, drawing
- RectangleShape control [Visual Basic]
ms.assetid: 0275b4c6-7a13-46c8-90f3-61db308c6b5d
ms.openlocfilehash: fe937236332591f6065e618c49ca5cf2c54b987c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701223"
---
# <a name="how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls-visual-studio"></a><span data-ttu-id="77da3-102">方法: OvalShape コントロールおよび RectangleShape コントロール (Visual Studio) を使用して図形を描画します。</span><span class="sxs-lookup"><span data-stu-id="77da3-102">How to: Draw Shapes with the OvalShape and RectangleShape Controls (Visual Studio)</span></span>
<span data-ttu-id="77da3-103">デザイン時にも実行時にも、<xref:Microsoft.VisualBasic.PowerPacks.OvalShape> コントロールを使用して、フォームまたはコンテナーに円または楕円を描画できます。</span><span class="sxs-lookup"><span data-stu-id="77da3-103">You can use the <xref:Microsoft.VisualBasic.PowerPacks.OvalShape> control to draw circles or ovals on a form or container, both at design time and at run time.</span></span> <span data-ttu-id="77da3-104"><xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> コントロールを使用して、フォームまたはコンテナーに正方形、長方形、または角の丸い四角形を描画できます。</span><span class="sxs-lookup"><span data-stu-id="77da3-104">You can use the <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> control to draw squares, rectangles, or rectangles with rounded corners on a form or container.</span></span> <span data-ttu-id="77da3-105">デザイン時にも実行時にも、このコントロールを使用して、図形を描画することもできます。</span><span class="sxs-lookup"><span data-stu-id="77da3-105">You can also use this control to draw shapes both at design time and at run time.</span></span>  
  
 <span data-ttu-id="77da3-106">境界線の幅、色、およびスタイルを変更することによって、図形の外観をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="77da3-106">You can customize the appearance of a shape by changing the width, color, and style of the border.</span></span> <span data-ttu-id="77da3-107">図形の背景は、既定では透明になっていますが、純色、パターン、グラデーション塗りつぶし (ある色から別の色への遷移)、またはイメージが表示されるようにカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="77da3-107">The background of a shape is transparent by default; you can customize the background to display a solid color, a pattern, a gradient fill (transitioning from one color to another), or an image.</span></span>  
  
### <a name="to-draw-a-simple-shape-at-design-time"></a><span data-ttu-id="77da3-108">デザイン時に単純な図形を描画するには</span><span class="sxs-lookup"><span data-stu-id="77da3-108">To draw a simple shape at design time</span></span>  
  
1.  <span data-ttu-id="77da3-109">ドラッグ、<xref:Microsoft.VisualBasic.PowerPacks.OvalShape>または<xref:Microsoft.VisualBasic.PowerPacks.RectangleShape>コントロールから、 **Visual Basic powerpacks**  タブ (をインストールするを参照してください[Visual Basic Power Packs コントロール](../../../visual-basic/developing-apps/windows-forms/power-packs-controls.md)) で、**ツールボックス**。フォームまたはコンテナー コントロール。</span><span class="sxs-lookup"><span data-stu-id="77da3-109">Drag the <xref:Microsoft.VisualBasic.PowerPacks.OvalShape> or <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> control from the **Visual Basic PowerPacks** tab (to install, see [Visual Basic Power Packs Controls](../../../visual-basic/developing-apps/windows-forms/power-packs-controls.md))in the **Toolbox** to a form or container control.</span></span>  
  
2.  <span data-ttu-id="77da3-110">サイズ変更ハンドルおよび移動ハンドルをドラッグして、図形のサイズと位置を設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-110">Drag the sizing and move handles to size and position the shape.</span></span>  
  
     <span data-ttu-id="77da3-111">サイズを変更し、変更することで、図形を配置することもできます、`Size`と`Position`プロパティで、**プロパティ**ウィンドウ。</span><span class="sxs-lookup"><span data-stu-id="77da3-111">You can also size and position the shape by changing the `Size` and `Position` properties in the **Properties** window.</span></span>  
  
     <span data-ttu-id="77da3-112">角の丸い四角形を作成するには、選択、`CornerRadius`プロパティ、**プロパティ**ウィンドウが 0 より大きい値に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-112">To create a rectangle with rounded corners, select the `CornerRadius` property in the **Properties** window and set it to a value that is greater than 0.</span></span>  
  
3.  <span data-ttu-id="77da3-113">**プロパティ**ウィンドウで、必要に応じて追加プロパティの設定、図形の外観を変更します。</span><span class="sxs-lookup"><span data-stu-id="77da3-113">In the **Properties** window, optionally set additional properties to change the appearance of the shape.</span></span>  
  
### <a name="to-draw-a-simple-shape-at-run-time"></a><span data-ttu-id="77da3-114">実行時に単純な図形を描画するには</span><span class="sxs-lookup"><span data-stu-id="77da3-114">To draw a simple shape at run time</span></span>  
  
1.  <span data-ttu-id="77da3-115">**[プロジェクト]** メニューの **[参照の追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77da3-115">On the **Project** menu, click **Add Reference**.</span></span>  
  
2.  <span data-ttu-id="77da3-116">**参照の追加**ダイアログ ボックスで、 **[microsoft.visualbasic.powerpacks.vs]**、順にクリックします**OK**します。</span><span class="sxs-lookup"><span data-stu-id="77da3-116">In the **Add Reference** dialog box, select **Microsoft.VisualBasic.PowerPacks.VS**, and then click **OK**.</span></span>  
  
3.  <span data-ttu-id="77da3-117">**コード エディター**、追加、`Imports`または`using`モジュールの上部にあるステートメント。</span><span class="sxs-lookup"><span data-stu-id="77da3-117">In the **Code Editor**, add an `Imports` or `using` statement at the top of the module:</span></span>  
  
```vb  
Imports Microsoft.VisualBasic.PowerPacks  
```  
  
```csharp  
using Microsoft.VisualBasic.PowerPacks;  
```  
  
4.  <span data-ttu-id="77da3-118">`Event` プロシージャに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="77da3-118">Add the following code in an `Event` procedure:</span></span>  
  
     [!code-csharp[VbPowerpacksShape#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls_1.cs)]
     [!code-vb[VbPowerpacksShape#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls_1.vb)]  
  
## <a name="customizing-shapes"></a><span data-ttu-id="77da3-119">図形のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="77da3-119">Customizing Shapes</span></span>  
 <span data-ttu-id="77da3-120">既定の設定を使用すると、<xref:Microsoft.VisualBasic.PowerPacks.OvalShape> と <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> の各コントロールが、1 ピクセル幅で透明な背景を持つ黒い実線の境界線と共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="77da3-120">When you use the default settings, the <xref:Microsoft.VisualBasic.PowerPacks.OvalShape> and <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> controls are displayed with a solid black border that is one pixel wide and a transparent background.</span></span> <span data-ttu-id="77da3-121">プロパティを設定することにより、境界線の幅、スタイル、および色を変更できます。</span><span class="sxs-lookup"><span data-stu-id="77da3-121">You can change the width, style, and color of the border by setting properties.</span></span> <span data-ttu-id="77da3-122">追加のプロパティを使用すると、図形の背景を純色、パターン、グラデーション塗りつぶし、またはイメージに変更できます。</span><span class="sxs-lookup"><span data-stu-id="77da3-122">Additional properties enable you to change the background of a shape to a solid color, a pattern, a gradient fill, or an image.</span></span>  
  
 <span data-ttu-id="77da3-123">図形の背景を変更する前に、一部のプロパティがどのように作用するかを知っておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="77da3-123">Before you change the background of a shape, you should know how several of the properties interact.</span></span>  
  
-   <span data-ttu-id="77da3-124"><xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackColor%2A> プロパティの設定は、<xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackStyle%2A> プロパティが <xref:Microsoft.VisualBasic.PowerPacks.BackStyle.Opaque> に設定されていない限り、何の効果もありません。</span><span class="sxs-lookup"><span data-stu-id="77da3-124">The <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackColor%2A> property setting has no effect unless the <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackStyle%2A> property is set to <xref:Microsoft.VisualBasic.PowerPacks.BackStyle.Opaque>.</span></span>  
  
-   <span data-ttu-id="77da3-125"><xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillStyle%2A> プロパティを <xref:Microsoft.VisualBasic.PowerPacks.FillStyle.Solid> に設定した場合、<xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillColor%2A>は <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackColor%2A> をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="77da3-125">If the <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillStyle%2A> property is set to <xref:Microsoft.VisualBasic.PowerPacks.FillStyle.Solid>, the <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillColor%2A> overrides the <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackColor%2A>.</span></span>  
  
-   <span data-ttu-id="77da3-126"><xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillStyle%2A> プロパティを <xref:Microsoft.VisualBasic.PowerPacks.FillStyle.Horizontal> や <xref:Microsoft.VisualBasic.PowerPacks.FillStyle.Vertical> などのパターン値に設定した場合、そのパターンが <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillColor%2A> で表示されます。</span><span class="sxs-lookup"><span data-stu-id="77da3-126">If the <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillStyle%2A> property is set to a pattern value such as <xref:Microsoft.VisualBasic.PowerPacks.FillStyle.Horizontal> or <xref:Microsoft.VisualBasic.PowerPacks.FillStyle.Vertical>, the pattern will be displayed in the <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillColor%2A>.</span></span> <span data-ttu-id="77da3-127"><xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackColor%2A> プロパティを <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackStyle%2A> に設定した場合、背景は <xref:Microsoft.VisualBasic.PowerPacks.BackStyle.Opaque> で表示されます。</span><span class="sxs-lookup"><span data-stu-id="77da3-127">The background will be displayed in the <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackColor%2A>, provided that the <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackStyle%2A> property is set to <xref:Microsoft.VisualBasic.PowerPacks.BackStyle.Opaque>.</span></span>  
  
-   <span data-ttu-id="77da3-128">グラデーション塗りつぶしを表示するには、<xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillStyle%2A> プロパティを <xref:Microsoft.VisualBasic.PowerPacks.FillStyle.Solid> に設定し、<xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillGradientStyle%2A> プロパティを <xref:Microsoft.VisualBasic.PowerPacks.FillGradientStyle.None> 以外の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77da3-128">In order to display a gradient fill, the <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillStyle%2A> property must be set to <xref:Microsoft.VisualBasic.PowerPacks.FillStyle.Solid> and the <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.FillGradientStyle%2A> property must be set to a value other than <xref:Microsoft.VisualBasic.PowerPacks.FillGradientStyle.None>.</span></span>  
  
-   <span data-ttu-id="77da3-129"><xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackgroundImage%2A> プロパティをイメージに設定すると、他のすべての背景設定がオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="77da3-129">Setting the <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape.BackgroundImage%2A> property to an image overrides all other background settings.</span></span>  
  
#### <a name="to-draw-a-circle-that-has-a-custom-border"></a><span data-ttu-id="77da3-130">飾り枠を持つ円を描画するには</span><span class="sxs-lookup"><span data-stu-id="77da3-130">To draw a circle that has a custom border</span></span>  
  
1.  <span data-ttu-id="77da3-131">ドラッグ、`OvalShape`コントロールから、 **Visual Basic powerpacks**  タブで、**ツールボックス**フォームまたはコンテナー コントロールにします。</span><span class="sxs-lookup"><span data-stu-id="77da3-131">Drag the `OvalShape` control from the **Visual Basic PowerPacks** tab in the **Toolbox** to a form or container control.</span></span>  
  
2.  <span data-ttu-id="77da3-132">**プロパティ**ウィンドウで、`Size`プロパティを設定`Height`と`Width`を等しい値です。</span><span class="sxs-lookup"><span data-stu-id="77da3-132">In the **Properties** window, in the `Size` property, set `Height` and `Width` to equal values.</span></span>  
  
3.  <span data-ttu-id="77da3-133">`BorderColor` プロパティを任意の色に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-133">Set the `BorderColor` property to the color that you want.</span></span>  
  
4.  <span data-ttu-id="77da3-134">`BorderStyle` プロパティを `Solid` 以外の任意の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-134">Set the `BorderStyle` property to any value other than `Solid`.</span></span>  
  
5.  <span data-ttu-id="77da3-135">`BorderWidth` をピクセル単位の任意のサイズに設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-135">Set the `BorderWidth` to the size that you want, in pixels.</span></span>  
  
#### <a name="to-draw-a-circle-that-has-a-solid-fill"></a><span data-ttu-id="77da3-136">純色の塗りつぶしを持つ円を描画するには</span><span class="sxs-lookup"><span data-stu-id="77da3-136">To draw a circle that has a solid fill</span></span>  
  
1.  <span data-ttu-id="77da3-137">ドラッグ、`OvalShape`コントロールから、 **Visual Basic powerpacks**  タブで、**ツールボックス**フォームまたはコンテナー コントロールにします。</span><span class="sxs-lookup"><span data-stu-id="77da3-137">Drag the `OvalShape` control from the **Visual Basic PowerPacks** tab in the **Toolbox** to a form or container control.</span></span>  
  
2.  <span data-ttu-id="77da3-138">**プロパティ**ウィンドウで、`Size`プロパティを設定`Height`と`Width`を等しい値です。</span><span class="sxs-lookup"><span data-stu-id="77da3-138">In the **Properties** window, in the `Size` property, set `Height` and `Width` to equal values.</span></span>  
  
3.  <span data-ttu-id="77da3-139">`BackColor` プロパティを任意の色に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-139">Set the `BackColor` property to the color that you want.</span></span>  
  
4.  <span data-ttu-id="77da3-140">`BackStyle` プロパティを `Opaque` に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-140">Set the `BackStyle` property to `Opaque`.</span></span>  
  
#### <a name="to-draw-a-circle-that-has-a-patterned-fill"></a><span data-ttu-id="77da3-141">塗りつぶしパターンを持つ円を描画するには</span><span class="sxs-lookup"><span data-stu-id="77da3-141">To draw a circle that has a patterned fill</span></span>  
  
1.  <span data-ttu-id="77da3-142">ドラッグ、`OvalShape`コントロールから、 **Visual Basic powerpacks**  タブで、**ツールボックス**フォームまたはコンテナー コントロールにします。</span><span class="sxs-lookup"><span data-stu-id="77da3-142">Drag the `OvalShape` control from the **Visual Basic PowerPacks** tab in the **Toolbox** to a form or container control.</span></span>  
  
2.  <span data-ttu-id="77da3-143">**プロパティ**ウィンドウで、`Size`プロパティを設定`Height`と`Width`を等しい値です。</span><span class="sxs-lookup"><span data-stu-id="77da3-143">In the **Properties** window, in the `Size` property, set `Height` and `Width` to equal values.</span></span>  
  
3.  <span data-ttu-id="77da3-144">`BackColor` プロパティを任意の背景色に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-144">Set the `BackColor` property to the color that you want for the background.</span></span>  
  
4.  <span data-ttu-id="77da3-145">`BackStyle` プロパティを `Opaque` に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-145">Set the `BackStyle` property to `Opaque`.</span></span>  
  
5.  <span data-ttu-id="77da3-146">`FillColor` プロパティを任意のパターン色に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-146">Set the `FillColor` property to the color that you want for the pattern.</span></span>  
  
6.  <span data-ttu-id="77da3-147">`FillStyle` プロパティを `Transparent` または `Solid` 以外の任意の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-147">Set the `FillStyle` property to any value other than `Transparent` or `Solid`.</span></span>  
  
#### <a name="to-draw-a-circle-that-has-a-gradient-fill"></a><span data-ttu-id="77da3-148">グラデーション塗りつぶしを持つ円を描画するには</span><span class="sxs-lookup"><span data-stu-id="77da3-148">To draw a circle that has a gradient fill</span></span>  
  
1.  <span data-ttu-id="77da3-149">ドラッグ、`OvalShape`コントロールから、 **Visual Basic powerpacks**  タブで、**ツールボックス**フォームまたはコンテナー コントロールにします。</span><span class="sxs-lookup"><span data-stu-id="77da3-149">Drag the `OvalShape` control from the **Visual Basic PowerPacks** tab in the **Toolbox** to a form or container control.</span></span>  
  
2.  <span data-ttu-id="77da3-150">**プロパティ**ウィンドウで、`Size`プロパティを設定`Height`と`Width`を等しい値です。</span><span class="sxs-lookup"><span data-stu-id="77da3-150">In the **Properties** window, in the `Size` property, set `Height` and `Width` to equal values.</span></span>  
  
3.  <span data-ttu-id="77da3-151">`FillColor` プロパティを任意の開始色に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-151">Set the `FillColor` property to the color that you want for the starting color.</span></span>  
  
4.  <span data-ttu-id="77da3-152">`FillGradientColor` プロパティを任意の終了色に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-152">Set the `FillGradientColor` property to the color that you want for the ending color.</span></span>  
  
5.  <span data-ttu-id="77da3-153">`FillGradientStyle` プロパティを `None` 以外の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="77da3-153">Set the `FillGradientStyle` property to a value other than `None`.</span></span>  
  
#### <a name="to-draw-a-circle-that-is-filled-with-an-image"></a><span data-ttu-id="77da3-154">イメージで塗りつぶされる円を描画するには</span><span class="sxs-lookup"><span data-stu-id="77da3-154">To draw a circle that is filled with an image</span></span>  
  
1.  <span data-ttu-id="77da3-155">ドラッグ、`OvalShape`コントロールから、 **Visual Basic powerpacks**  タブで、**ツールボックス**フォームまたはコンテナー コントロールにします。</span><span class="sxs-lookup"><span data-stu-id="77da3-155">Drag the `OvalShape` control from the **Visual Basic PowerPacks** tab in the **Toolbox** to a form or container control.</span></span>  
  
2.  <span data-ttu-id="77da3-156">**プロパティ**ウィンドウで、`Size`プロパティを設定`Height`と`Width`を等しい値です。</span><span class="sxs-lookup"><span data-stu-id="77da3-156">In the **Properties** window, in the `Size` property, set `Height` and `Width` to equal values.</span></span>  
  
3.  <span data-ttu-id="77da3-157">選択、`BackgroundImage`プロパティをクリックして、**省略記号**ボタン ([...])。</span><span class="sxs-lookup"><span data-stu-id="77da3-157">Select the `BackgroundImage` property and click the **ellipsis** button (...).</span></span>  
  
4.  <span data-ttu-id="77da3-158">**リソースの選択** ダイアログ ボックスで、表示するイメージを選択します。</span><span class="sxs-lookup"><span data-stu-id="77da3-158">In the **Select Resource** dialog box, select an image to display.</span></span> <span data-ttu-id="77da3-159">イメージ リソースが表示されない場合は、クリックして**インポート**イメージの場所を参照します。</span><span class="sxs-lookup"><span data-stu-id="77da3-159">If no image resources are listed, click **Import** to browse to the location of an image.</span></span>  
  
5.  <span data-ttu-id="77da3-160">クリックして**OK**イメージを挿入します。</span><span class="sxs-lookup"><span data-stu-id="77da3-160">Click **OK** to insert the image.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77da3-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="77da3-161">See also</span></span>
- <xref:Microsoft.VisualBasic.PowerPacks.OvalShape>
- <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape>
- [<span data-ttu-id="77da3-162">ライン コントロールとシェイプ コントロールの概要</span><span class="sxs-lookup"><span data-stu-id="77da3-162">Introduction to the Line and Shape Controls</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-line-and-shape-controls-visual-studio.md)
- [<span data-ttu-id="77da3-163">方法: LineShape コントロールを使用して線を描画します。</span><span class="sxs-lookup"><span data-stu-id="77da3-163">How to: Draw Lines with the LineShape Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-draw-lines-with-the-lineshape-control-visual-studio.md)
