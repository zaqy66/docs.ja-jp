---
title: '方法: ToolStrip アプリケーションの色をカスタマイズします。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms], customizing colors
- colors [Windows Forms], customizing in ToolStrip controls [Windows Forms]
- ToolStrip control [Windows Forms], custom colors
ms.assetid: e2752fe2-1afb-489e-ab96-b7805acd96bc
ms.openlocfilehash: 0a7679624d375fac610f6c74f124881d7235eab8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585433"
---
# <a name="how-to-customize-colors-in-toolstrip-applications"></a><span data-ttu-id="9465a-102">方法: ToolStrip アプリケーションの色をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="9465a-102">How to: Customize Colors in ToolStrip Applications</span></span>
<span data-ttu-id="9465a-103"><xref:System.Windows.Forms.ToolStripProfessionalRenderer> クラスを使用して、カスタマイズした色を使用すると、<xref:System.Windows.Forms.ToolStrip> の外観をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="9465a-103">You can customize the appearance of your <xref:System.Windows.Forms.ToolStrip> by using the <xref:System.Windows.Forms.ToolStripProfessionalRenderer> class to use customized colors.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9465a-104">例</span><span class="sxs-lookup"><span data-stu-id="9465a-104">Example</span></span>  
 <span data-ttu-id="9465a-105">次のコード例は、<xref:System.Windows.Forms.ToolStripProfessionalRenderer> を使用してカスタム カラーを実行時に定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9465a-105">The following code example demonstrates how to use a <xref:System.Windows.Forms.ToolStripProfessionalRenderer> to define custom colors at run time.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#20](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#20)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#20](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#20)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="9465a-106">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="9465a-106">Compiling the Code</span></span>  
 <span data-ttu-id="9465a-107">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9465a-107">This example requires:</span></span>  
  
-   <span data-ttu-id="9465a-108">System.Design、System.Drawing、および System.Windows.Forms の各アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="9465a-108">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="9465a-109">コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="9465a-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="9465a-110">新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="9465a-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="9465a-111">参照してください[方法。Visual Studio を使用して、完全な Windows フォームのコードの例をコンパイルして](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))します。</span><span class="sxs-lookup"><span data-stu-id="9465a-111">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9465a-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="9465a-112">See also</span></span>
- <xref:System.Windows.Forms.ToolStripManager>
- <xref:System.Windows.Forms.ProfessionalColorTable>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripProfessionalRenderer>
