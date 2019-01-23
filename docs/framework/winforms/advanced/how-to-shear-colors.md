---
title: '方法: 色の傾斜'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], transforming with color matrices
- colors [Windows Forms], shearing
ms.assetid: 0a424171-5b8b-45c4-afef-e9720a6c3e22
ms.openlocfilehash: bde3271398c6bc6a37c975476b76acb85511c1a4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54589833"
---
# <a name="how-to-shear-colors"></a><span data-ttu-id="c5988-102">方法: 色の傾斜</span><span class="sxs-lookup"><span data-stu-id="c5988-102">How to: Shear Colors</span></span>
<span data-ttu-id="c5988-103">傾斜増加またはカラー コンポーネントを別の色コンポーネントに比例した量ずつ減少します。</span><span class="sxs-lookup"><span data-stu-id="c5988-103">Shearing increases or decreases a color component by an amount proportional to another color component.</span></span> <span data-ttu-id="c5988-104">たとえば、赤のコンポーネントを増加して青のコンポーネントの値の半分して変換を検討してください。</span><span class="sxs-lookup"><span data-stu-id="c5988-104">For example, consider the transformation where the red component is increased by one half the value of the blue component.</span></span> <span data-ttu-id="c5988-105">このような変換では、(0.2, 0.5, 1) の色になります (0.7, 0.5, 1)。</span><span class="sxs-lookup"><span data-stu-id="c5988-105">Under such a transformation, the color (0.2, 0.5, 1) would become (0.7, 0.5, 1).</span></span> <span data-ttu-id="c5988-106">新しいの赤のコンポーネントが 0.2 + (1/2)(1) 0.7 を = です。</span><span class="sxs-lookup"><span data-stu-id="c5988-106">The new red component is 0.2 + (1/2)(1) = 0.7.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c5988-107">例</span><span class="sxs-lookup"><span data-stu-id="c5988-107">Example</span></span>  
 <span data-ttu-id="c5988-108">次の例では、構築、 <xref:System.Drawing.Image> ColorBars4.bmp ファイルからのオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="c5988-108">The following example constructs an <xref:System.Drawing.Image> object from the file ColorBars4.bmp.</span></span> <span data-ttu-id="c5988-109">コードは、イメージ内の各ピクセルに前の段落で説明されている傾斜変換を適用します。</span><span class="sxs-lookup"><span data-stu-id="c5988-109">Then the code applies the shearing transformation described in the preceding paragraph to each pixel in the image.</span></span>  
  
 <span data-ttu-id="c5988-110">次の図は、右側の左側に、元のイメージと傾斜のイメージを示します。</span><span class="sxs-lookup"><span data-stu-id="c5988-110">The following illustration shows the original image on the left and the sheared image on the right.</span></span>  
  
 <span data-ttu-id="c5988-111">![色を傾斜](../../../../docs/framework/winforms/advanced/media/colortrans6.png "colortrans6")</span><span class="sxs-lookup"><span data-stu-id="c5988-111">![Shear Colors](../../../../docs/framework/winforms/advanced/media/colortrans6.png "colortrans6")</span></span>  
  
 <span data-ttu-id="c5988-112">次の表は、傾斜変換の前後に 4 つのバーの色のベクターを示します。</span><span class="sxs-lookup"><span data-stu-id="c5988-112">The following table lists the color vectors for the four bars before and after the shearing transformation.</span></span>  
  
|<span data-ttu-id="c5988-113">元</span><span class="sxs-lookup"><span data-stu-id="c5988-113">Original</span></span>|<span data-ttu-id="c5988-114">傾斜</span><span class="sxs-lookup"><span data-stu-id="c5988-114">Sheared</span></span>|  
|--------------|-------------|  
|<span data-ttu-id="c5988-115">(0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="c5988-115">(0, 0, 1, 1)</span></span>|<span data-ttu-id="c5988-116">(0.5, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="c5988-116">(0.5, 0, 1, 1)</span></span>|  
|<span data-ttu-id="c5988-117">(0.5, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="c5988-117">(0.5, 1, 0.5, 1)</span></span>|<span data-ttu-id="c5988-118">(0.75, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="c5988-118">(0.75, 1, 0.5, 1)</span></span>|  
|<span data-ttu-id="c5988-119">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="c5988-119">(1, 1, 0, 1)</span></span>|<span data-ttu-id="c5988-120">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="c5988-120">(1, 1, 0, 1)</span></span>|  
|<span data-ttu-id="c5988-121">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="c5988-121">(0.4, 0.4, 0.4, 1)</span></span>|<span data-ttu-id="c5988-122">(0.6, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="c5988-122">(0.6, 0.4, 0.4, 1)</span></span>|  
  
 [!code-csharp[System.Drawing.Misc3#9](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Misc3/CS/Form1.cs#9)]
 [!code-vb[System.Drawing.Misc3#9](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Misc3/VB/Form1.vb#9)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c5988-123">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="c5988-123">Compiling the Code</span></span>  
 <span data-ttu-id="c5988-124">前の例は、Windows フォームで使用するために設計されていて、<xref:System.Windows.Forms.PaintEventArgs> イベント ハンドラーのパラメーターである `e`<xref:System.Windows.Forms.Control.Paint> を必要とします。</span><span class="sxs-lookup"><span data-stu-id="c5988-124">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="c5988-125">置換`ColorBars.bmp`イメージ名とパス、システムでは無効です。</span><span class="sxs-lookup"><span data-stu-id="c5988-125">Replace `ColorBars.bmp` with an image name and path valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5988-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="c5988-126">See also</span></span>
- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [<span data-ttu-id="c5988-127">Windows フォームにおけるグラフィックスと描画</span><span class="sxs-lookup"><span data-stu-id="c5988-127">Graphics and Drawing in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="c5988-128">イメージの色の変更</span><span class="sxs-lookup"><span data-stu-id="c5988-128">Recoloring Images</span></span>](../../../../docs/framework/winforms/advanced/recoloring-images.md)
