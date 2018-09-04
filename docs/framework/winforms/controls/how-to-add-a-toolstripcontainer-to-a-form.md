---
title: '方法 : フォームに ToolStripContainer を追加する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms], built-in rafting
- ToolStrip control [Windows Forms], built-in rafting
- ToolStripContainer control [Windows Forms], adding to Windows Forms
ms.assetid: d0f55095-a833-453e-be5a-644906d75d54
ms.openlocfilehash: 0e3a766c8238d7388ee95ecda5c60836ed944e05
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43513186"
---
# <a name="how-to-add-a-toolstripcontainer-to-a-form"></a><span data-ttu-id="42b53-102">方法 : フォームに ToolStripContainer を追加する</span><span class="sxs-lookup"><span data-stu-id="42b53-102">How to: Add a ToolStripContainer to a Form</span></span>
<span data-ttu-id="42b53-103">プログラムで Windows フォームに <xref:System.Windows.Forms.ToolStripContainer> を追加し、そこにコントロールを配置できます。</span><span class="sxs-lookup"><span data-stu-id="42b53-103">You can programmatically add a <xref:System.Windows.Forms.ToolStripContainer> to a Windows Form and populate it with controls.</span></span>  
  
## <a name="example"></a><span data-ttu-id="42b53-104">例</span><span class="sxs-lookup"><span data-stu-id="42b53-104">Example</span></span>  
 <span data-ttu-id="42b53-105">次のコード例は、Windows フォームに <xref:System.Windows.Forms.ToolStripContainer> および <xref:System.Windows.Forms.ToolStrip> を追加する方法、<xref:System.Windows.Forms.ToolStrip> に項目を追加する方法、<xref:System.Windows.Forms.ToolStripContainer> の <xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanel%2A> に <xref:System.Windows.Forms.ToolStrip> を追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="42b53-105">The following code example demonstrates how to add a <xref:System.Windows.Forms.ToolStripContainer> and a <xref:System.Windows.Forms.ToolStrip> to a Windows Forms, how to add items to the <xref:System.Windows.Forms.ToolStrip>, and how to add the <xref:System.Windows.Forms.ToolStrip> to the <xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanel%2A> of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStripContainer2#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/system.windows.forms.toolstripcontainer2/cs/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStripContainer2#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/system.windows.forms.toolstripcontainer2/vb/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="42b53-106">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="42b53-106">Compiling the Code</span></span>  
 <span data-ttu-id="42b53-107">このコード例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="42b53-107">This code example requires:</span></span>  
  
-   <span data-ttu-id="42b53-108">System.Drawing、System.Text、および System.Windows.Forms の各アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="42b53-108">References to the System.Drawing, System.Text, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="42b53-109">コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="42b53-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="42b53-110">新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="42b53-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="42b53-111">また、「[方法: 完成した Windows フォーム コードの例を Visual Studio を使ってコンパイルして実行する](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))」または「[[ToolStripContainer タスク] ダイアログ ボックス](https://msdn.microsoft.com/library/ms233647\(v=vs.110\))」も参照してください。</span><span class="sxs-lookup"><span data-stu-id="42b53-111">See also [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)) or [ToolStripContainer Tasks Dialog Box](https://msdn.microsoft.com/library/ms233647\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="42b53-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="42b53-112">See Also</span></span>  
 <xref:System.Windows.Forms.ToolStripContainer>  
 [<span data-ttu-id="42b53-113">ToolStripContainer コントロール</span><span class="sxs-lookup"><span data-stu-id="42b53-113">ToolStripContainer Control</span></span>](../../../../docs/framework/winforms/controls/toolstripcontainer-control.md)  
 [<span data-ttu-id="42b53-114">ToolStrip コントロール</span><span class="sxs-lookup"><span data-stu-id="42b53-114">ToolStrip Control</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
