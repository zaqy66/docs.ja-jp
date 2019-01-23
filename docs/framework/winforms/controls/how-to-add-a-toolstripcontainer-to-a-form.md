---
title: '方法: フォームに ToolStripContainer を追加します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms], built-in rafting
- ToolStrip control [Windows Forms], built-in rafting
- ToolStripContainer control [Windows Forms], adding to Windows Forms
ms.assetid: d0f55095-a833-453e-be5a-644906d75d54
ms.openlocfilehash: 9aace854a9583268ef7aac6ac1f57534cfdfe1e6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515522"
---
# <a name="how-to-add-a-toolstripcontainer-to-a-form"></a><span data-ttu-id="09f73-102">方法: フォームに ToolStripContainer を追加します。</span><span class="sxs-lookup"><span data-stu-id="09f73-102">How to: Add a ToolStripContainer to a Form</span></span>
<span data-ttu-id="09f73-103">プログラムで Windows フォームに <xref:System.Windows.Forms.ToolStripContainer> を追加し、そこにコントロールを配置できます。</span><span class="sxs-lookup"><span data-stu-id="09f73-103">You can programmatically add a <xref:System.Windows.Forms.ToolStripContainer> to a Windows Form and populate it with controls.</span></span>  
  
## <a name="example"></a><span data-ttu-id="09f73-104">例</span><span class="sxs-lookup"><span data-stu-id="09f73-104">Example</span></span>  
 <span data-ttu-id="09f73-105">次のコード例は、Windows フォームに <xref:System.Windows.Forms.ToolStripContainer> および <xref:System.Windows.Forms.ToolStrip> を追加する方法、<xref:System.Windows.Forms.ToolStrip> に項目を追加する方法、<xref:System.Windows.Forms.ToolStripContainer> の <xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanel%2A> に <xref:System.Windows.Forms.ToolStrip> を追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="09f73-105">The following code example demonstrates how to add a <xref:System.Windows.Forms.ToolStripContainer> and a <xref:System.Windows.Forms.ToolStrip> to a Windows Forms, how to add items to the <xref:System.Windows.Forms.ToolStrip>, and how to add the <xref:System.Windows.Forms.ToolStrip> to the <xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanel%2A> of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStripContainer2#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/system.windows.forms.toolstripcontainer2/cs/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStripContainer2#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/system.windows.forms.toolstripcontainer2/vb/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="09f73-106">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="09f73-106">Compiling the Code</span></span>  
 <span data-ttu-id="09f73-107">このコード例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="09f73-107">This code example requires:</span></span>  
  
-   <span data-ttu-id="09f73-108">System.Drawing、System.Text、および System.Windows.Forms の各アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="09f73-108">References to the System.Drawing, System.Text, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="09f73-109">コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="09f73-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="09f73-110">新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="09f73-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="09f73-111">「[方法: Visual Studio を使用して、完全な Windows フォームのコードの例をコンパイルして](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))または[ToolStripContainer タスク ダイアログ ボックス](https://msdn.microsoft.com/library/ms233647\(v=vs.110\))します。</span><span class="sxs-lookup"><span data-stu-id="09f73-111">See also [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)) or [ToolStripContainer Tasks Dialog Box](https://msdn.microsoft.com/library/ms233647\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09f73-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="09f73-112">See also</span></span>
- <xref:System.Windows.Forms.ToolStripContainer>
- [<span data-ttu-id="09f73-113">ToolStripContainer コントロール</span><span class="sxs-lookup"><span data-stu-id="09f73-113">ToolStripContainer Control</span></span>](../../../../docs/framework/winforms/controls/toolstripcontainer-control.md)
- [<span data-ttu-id="09f73-114">ToolStrip コントロール</span><span class="sxs-lookup"><span data-stu-id="09f73-114">ToolStrip Control</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
