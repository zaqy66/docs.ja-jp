---
title: '方法: LineShape コントロール (Visual Studio) を使用して線を描画します。'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- LineShape control [Visual Basic]
- lines, drawing
ms.assetid: 83e71b4e-aa76-4f9b-b547-8704309fd1e5
ms.openlocfilehash: 46360c01dfaf2c6fe199725a9ecfba2248c72d6d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596229"
---
# <a name="how-to-draw-lines-with-the-lineshape-control-visual-studio"></a><span data-ttu-id="66767-102">方法: LineShape コントロール (Visual Studio) を使用して線を描画します。</span><span class="sxs-lookup"><span data-stu-id="66767-102">How to: Draw Lines with the LineShape Control (Visual Studio)</span></span>
<span data-ttu-id="66767-103">使用することができます、<xref:Microsoft.VisualBasic.PowerPacks.LineShape>デザイン時と実行時の両方に、フォームまたはコンテナー、水平、垂直、または対角線方向の線を描画するコントロール。</span><span class="sxs-lookup"><span data-stu-id="66767-103">You can use the <xref:Microsoft.VisualBasic.PowerPacks.LineShape> control to draw horizontal, vertical, or diagonal lines on a form or container, both at design time and at run time.</span></span>  
  
 <span data-ttu-id="66767-104">**注**コンピューター可能性がありますさまざまな名前や場所が一部の Visual Studio のユーザー インターフェイス要素、次の手順でします。</span><span class="sxs-lookup"><span data-stu-id="66767-104">**Note** Your computer might show different names or locations for some of the Visual Studio user interface elements in the following instructions.</span></span> <span data-ttu-id="66767-105">これらの要素は、使用している Visual Studio のエディションや独自の設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="66767-105">The Visual Studio edition that you have and the settings that you use determine these elements.</span></span> <span data-ttu-id="66767-106">詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66767-106">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-draw-a-line-at-design-time"></a><span data-ttu-id="66767-107">デザイン時に線を描画するには</span><span class="sxs-lookup"><span data-stu-id="66767-107">To draw a line at design time</span></span>  
  
1.  <span data-ttu-id="66767-108">ドラッグ、<xref:Microsoft.VisualBasic.PowerPacks.LineShape>コントロールから、 **Visual Basic powerpacks**  タブで、**ツールボックス**をフォームまたはコンテナー コントロールにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="66767-108">Drag the <xref:Microsoft.VisualBasic.PowerPacks.LineShape> control from the **Visual Basic PowerPacks** tab in the **Toolbox** drag to a form or container control.</span></span>  
  
2.  <span data-ttu-id="66767-109">サイズをドラッグし、サイズし、位置の行へのハンドルを移動します。</span><span class="sxs-lookup"><span data-stu-id="66767-109">Drag the sizing and move handles to size and position the line.</span></span>  
  
     <span data-ttu-id="66767-110">サイズを変更し、変更することで、行を配置することもできます、 `X1`、 `X2`、 `Y1`、および`Y2`プロパティで、**プロパティ**ウィンドウ。</span><span class="sxs-lookup"><span data-stu-id="66767-110">You can also size and position the line by changing the `X1`, `X2`, `Y1`, and `Y2` properties in the **Properties** window.</span></span>  
  
3.  <span data-ttu-id="66767-111">**プロパティ**ウィンドウで、必要に応じて設定追加のプロパティなど`BorderStyle`または`BorderColor`行の外観を変更します。</span><span class="sxs-lookup"><span data-stu-id="66767-111">In the **Properties** window, optionally set additional properties such as `BorderStyle` or `BorderColor` to change the appearance of the line.</span></span>  
  
### <a name="to-draw-a-line-at-run-time"></a><span data-ttu-id="66767-112">実行時に線を描画するには</span><span class="sxs-lookup"><span data-stu-id="66767-112">To draw a line at run time</span></span>  
  
1.  <span data-ttu-id="66767-113">**[プロジェクト]** メニューの **[参照の追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66767-113">On the **Project** menu, click **Add Reference**.</span></span>  
  
2.  <span data-ttu-id="66767-114">**参照の追加**ダイアログ ボックスで、 **[microsoft.visualbasic.powerpacks.vs]**、順にクリックします**OK**します。</span><span class="sxs-lookup"><span data-stu-id="66767-114">In the **Add Reference** dialog box, select **Microsoft.VisualBasic.PowerPacks.VS**, and then click **OK**.</span></span>  
  
3.  <span data-ttu-id="66767-115">**コード エディター**、追加、`Imports`または`using`モジュールの上部にあるステートメント。</span><span class="sxs-lookup"><span data-stu-id="66767-115">In the **Code Editor**, add an `Imports` or `using` statement at the top of the module:</span></span>  
  
```vb  
Imports Microsoft.VisualBasic.PowerPacks  
```  
  
```csharp  
using Microsoft.VisualBasic.PowerPacks;  
```  
  
4.  <span data-ttu-id="66767-116">`Event` プロシージャに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="66767-116">Add the following code in an `Event` procedure:</span></span>  
  
     [!code-csharp[VbPowerPacksLine#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-draw-lines-with-the-lineshape-control-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksLine#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-draw-lines-with-the-lineshape-control-visual-studio_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="66767-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="66767-117">See also</span></span>
- <xref:Microsoft.VisualBasic.PowerPacks.LineShape>
- [<span data-ttu-id="66767-118">ライン コントロールとシェイプ コントロールの概要</span><span class="sxs-lookup"><span data-stu-id="66767-118">Introduction to the Line and Shape Controls</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-line-and-shape-controls-visual-studio.md)
- [<span data-ttu-id="66767-119">方法: 図形、OvalShape コントロールおよび RectangleShape コントロールを描く</span><span class="sxs-lookup"><span data-stu-id="66767-119">How to: Draw Shapes with the OvalShape and RectangleShape Controls</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)
