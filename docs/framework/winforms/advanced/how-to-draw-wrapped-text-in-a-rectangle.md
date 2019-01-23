---
title: '方法: 四角形内にテキストを折り返して描画'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, drawing text in a rectangle
- text [Windows Forms], drawing in a rectangle
- strings [Windows Forms], drawing in a rectangle
ms.assetid: e1fb432a-dc90-48b5-9b6b-acc14507133d
ms.openlocfilehash: 4afe3eb7c3525dac856751331117e0980063faad
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54602950"
---
# <a name="how-to-draw-wrapped-text-in-a-rectangle"></a><span data-ttu-id="5498a-102">方法: 四角形内にテキストを折り返して描画</span><span class="sxs-lookup"><span data-stu-id="5498a-102">How to: Draw Wrapped Text in a Rectangle</span></span>
<span data-ttu-id="5498a-103">使用して四角形でラップされたテキストを描画することができます、<xref:System.Drawing.Graphics.DrawString%2A>のメソッドをオーバー ロード、<xref:System.Drawing.Graphics>を受け取るクラス、<xref:System.Drawing.Rectangle>または<xref:System.Drawing.RectangleF>パラメーター。</span><span class="sxs-lookup"><span data-stu-id="5498a-103">You can draw wrapped text in a rectangle by using the <xref:System.Drawing.Graphics.DrawString%2A> overloaded method of the <xref:System.Drawing.Graphics> class that takes a <xref:System.Drawing.Rectangle> or <xref:System.Drawing.RectangleF> parameter.</span></span> <span data-ttu-id="5498a-104">使用することも、<xref:System.Drawing.Brush>と<xref:System.Drawing.Font>します。</span><span class="sxs-lookup"><span data-stu-id="5498a-104">You will also use a <xref:System.Drawing.Brush> and a <xref:System.Drawing.Font>.</span></span>  
  
 <span data-ttu-id="5498a-105">使用して、四角形でラップされたテキストを描画することも、<xref:System.Windows.Forms.TextRenderer.DrawText%2A>のメソッドをオーバー ロード、<xref:System.Windows.Forms.TextRenderer>を受け取る、<xref:System.Drawing.Rectangle>と<xref:System.Windows.Forms.TextFormatFlags>パラメーター。</span><span class="sxs-lookup"><span data-stu-id="5498a-105">You can also draw wrapped text in a rectangle by using the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> overloaded method of the <xref:System.Windows.Forms.TextRenderer> that takes a <xref:System.Drawing.Rectangle> and a <xref:System.Windows.Forms.TextFormatFlags> parameter.</span></span> <span data-ttu-id="5498a-106">使用することも、<xref:System.Drawing.Color>と<xref:System.Drawing.Font>します。</span><span class="sxs-lookup"><span data-stu-id="5498a-106">You will also use a <xref:System.Drawing.Color> and a <xref:System.Drawing.Font>.</span></span>  
  
 <span data-ttu-id="5498a-107">次の図は、使用すると、四角形の描画されるテキストの出力、<xref:System.Drawing.Graphics.DrawString%2A>メソッド。</span><span class="sxs-lookup"><span data-stu-id="5498a-107">The following illustration shows the output of text drawn in the rectangle when you use the <xref:System.Drawing.Graphics.DrawString%2A> method.</span></span>  
  
 <span data-ttu-id="5498a-108">![フォント テキスト](../../../../docs/framework/winforms/advanced/media/csfontstext2.png "csfontstext2")</span><span class="sxs-lookup"><span data-stu-id="5498a-108">![Fonts Text](../../../../docs/framework/winforms/advanced/media/csfontstext2.png "csfontstext2")</span></span>  
  
### <a name="to-draw-wrapped-text-in-a-rectangle-with-gdi"></a><span data-ttu-id="5498a-109">GDI + を使用して四角形内にテキストを折り返して描画するには</span><span class="sxs-lookup"><span data-stu-id="5498a-109">To draw wrapped text in a rectangle with GDI+</span></span>  
  
1.  <span data-ttu-id="5498a-110">使用して、 <xref:System.Drawing.Graphics.DrawString%2A> 、テキストを渡すメソッドをオーバー ロードされた<xref:System.Drawing.Rectangle>または<xref:System.Drawing.RectangleF>、<xref:System.Drawing.Font>と<xref:System.Drawing.Brush>します。</span><span class="sxs-lookup"><span data-stu-id="5498a-110">Use the <xref:System.Drawing.Graphics.DrawString%2A> overloaded method, passing the text you want, <xref:System.Drawing.Rectangle> or <xref:System.Drawing.RectangleF>, <xref:System.Drawing.Font> and <xref:System.Drawing.Brush>.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#50](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#50)]
     [!code-vb[System.Drawing.AlignDrawnText#50](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#50)]  
  
### <a name="to-draw-wrapped-text-in-a-rectangle-with-gdi"></a><span data-ttu-id="5498a-111">GDI を使用して四角形内にテキストを折り返して描画するには</span><span class="sxs-lookup"><span data-stu-id="5498a-111">To draw wrapped text in a rectangle with GDI</span></span>  
  
1.  <span data-ttu-id="5498a-112">使用して、<xref:System.Windows.Forms.TextFormatFlags>でテキストを指定する列挙値をラップする必要があります、 <xref:System.Windows.Forms.TextRenderer.DrawText%2A> 、テキストを渡すメソッドをオーバー ロードされた<xref:System.Drawing.Rectangle>、<xref:System.Drawing.Font>と<xref:System.Drawing.Color>します。</span><span class="sxs-lookup"><span data-stu-id="5498a-112">Use the <xref:System.Windows.Forms.TextFormatFlags> enumeration value to specify the text should be wrapped with the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> overloaded method, passing the text you want, <xref:System.Drawing.Rectangle>, <xref:System.Drawing.Font> and <xref:System.Drawing.Color>.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#60](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#60)]
     [!code-vb[System.Drawing.AlignDrawnText#60](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#60)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="5498a-113">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="5498a-113">Compiling the Code</span></span>  
 <span data-ttu-id="5498a-114">前の例が必要です。</span><span class="sxs-lookup"><span data-stu-id="5498a-114">The previous examples require:</span></span>  
  
-   <span data-ttu-id="5498a-115"><xref:System.Windows.Forms.PaintEventArgs> `e`でのパラメーターである<xref:System.Windows.Forms.PaintEventHandler>します。</span><span class="sxs-lookup"><span data-stu-id="5498a-115"><xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5498a-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="5498a-116">See also</span></span>
- [<span data-ttu-id="5498a-117">方法: GDI を使用してテキストを描画します。</span><span class="sxs-lookup"><span data-stu-id="5498a-117">How to: Draw Text with GDI</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-text-with-gdi.md)
- [<span data-ttu-id="5498a-118">フォントとテキストの使用</span><span class="sxs-lookup"><span data-stu-id="5498a-118">Using Fonts and Text</span></span>](../../../../docs/framework/winforms/advanced/using-fonts-and-text.md)
- [<span data-ttu-id="5498a-119">方法: フォント ファミリとフォントを作成します。</span><span class="sxs-lookup"><span data-stu-id="5498a-119">How to: Construct Font Families and Fonts</span></span>](../../../../docs/framework/winforms/advanced/how-to-construct-font-families-and-fonts.md)
- [<span data-ttu-id="5498a-120">方法: 指定した位置のテキストの描画</span><span class="sxs-lookup"><span data-stu-id="5498a-120">How to: Draw Text at a Specified Location</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-text-at-a-specified-location.md)
