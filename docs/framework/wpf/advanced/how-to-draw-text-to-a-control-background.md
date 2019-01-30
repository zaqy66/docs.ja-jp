---
title: '方法: コントロールの背景にテキストを描画する'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], drawing text to backgrounds
- text [WPF], drawing to control backgrounds
- drawing [WPF], text to control backgrounds
- backgrounds [WPF], drawing text to
- typography [WPF], drawing text to control backgrounds
ms.assetid: 686d8fba-f61c-4974-a871-c635d67a7f69
ms.openlocfilehash: 9be4eb92021a62baaf6b43198587616d00cc265e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55259255"
---
# <a name="how-to-draw-text-to-a-controls-background"></a><span data-ttu-id="6463b-102">方法: コントロールの背景にテキストを描画する</span><span class="sxs-lookup"><span data-stu-id="6463b-102">How to: Draw Text to a Control's Background</span></span>
<span data-ttu-id="6463b-103">コントロールの背景に直接テキストを描画するにはテキスト文字列を変換することで、<xref:System.Windows.Media.FormattedText>オブジェクト、およびコントロールのオブジェクトを描画<xref:System.Windows.Media.DrawingContext>します。</span><span class="sxs-lookup"><span data-stu-id="6463b-103">You can draw text directly to the background of a control by converting a text string to a <xref:System.Windows.Media.FormattedText> object, and then drawing the object to the control's <xref:System.Windows.Media.DrawingContext>.</span></span> <span data-ttu-id="6463b-104">派生したオブジェクトの背景を描画のために、この手法を使用することもできます<xref:System.Windows.Controls.Panel>など<xref:System.Windows.Controls.Canvas>と<xref:System.Windows.Controls.StackPanel>します。</span><span class="sxs-lookup"><span data-stu-id="6463b-104">You can also use this technique for drawing to the background of objects derived from <xref:System.Windows.Controls.Panel>, such as <xref:System.Windows.Controls.Canvas> and <xref:System.Windows.Controls.StackPanel>.</span></span>  
  
 <span data-ttu-id="6463b-105">![背景にテキストを表示するコントロール](../../../../docs/framework/wpf/advanced/media/drawtext2background01.png "DrawText2Background01")</span><span class="sxs-lookup"><span data-stu-id="6463b-105">![Controls displaying text as background](../../../../docs/framework/wpf/advanced/media/drawtext2background01.png "DrawText2Background01")</span></span>  
<span data-ttu-id="6463b-106">カスタム テキスト背景のコントロールの例</span><span class="sxs-lookup"><span data-stu-id="6463b-106">Example of controls with custom text backgrounds</span></span>  
  
## <a name="example"></a><span data-ttu-id="6463b-107">例</span><span class="sxs-lookup"><span data-stu-id="6463b-107">Example</span></span>  
 <span data-ttu-id="6463b-108">コントロールの背景を描画するには、新しい作成<xref:System.Windows.Media.DrawingBrush>オブジェクトし、オブジェクトの変換後のテキストを描画<xref:System.Windows.Media.DrawingContext>します。</span><span class="sxs-lookup"><span data-stu-id="6463b-108">To draw to the background of a control, create a new <xref:System.Windows.Media.DrawingBrush> object and draw the converted text to the object's <xref:System.Windows.Media.DrawingContext>.</span></span> <span data-ttu-id="6463b-109">次に、割り当てる新しい<xref:System.Windows.Media.DrawingBrush>をコントロールの背景のプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6463b-109">Then, assign the new <xref:System.Windows.Media.DrawingBrush> to the control's background property.</span></span>  
  
 <span data-ttu-id="6463b-110">次のコード例を作成する方法を示しています、<xref:System.Windows.Media.FormattedText>オブジェクトし、の背景を描画、<xref:System.Windows.Controls.Label>と<xref:System.Windows.Controls.Button>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="6463b-110">The following code example shows how to create a <xref:System.Windows.Media.FormattedText> object and draw to the background of a <xref:System.Windows.Controls.Label> and <xref:System.Windows.Controls.Button> object.</span></span>  
  
 [!code-csharp[DrawTextToControlBackground#DrawTextToControlBackground1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawTextToControlBackground/CSHARP/Window1.xaml.cs#drawtexttocontrolbackground1)]  
  
## <a name="see-also"></a><span data-ttu-id="6463b-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="6463b-111">See also</span></span>
- <xref:System.Windows.Media.FormattedText>
- [<span data-ttu-id="6463b-112">書式設定されたテキストの描画</span><span class="sxs-lookup"><span data-stu-id="6463b-112">Drawing Formatted Text</span></span>](../../../../docs/framework/wpf/advanced/drawing-formatted-text.md)
