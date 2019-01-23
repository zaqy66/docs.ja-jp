---
title: '方法: Windows フォーム DataGridView コントロールでイメージの列の使用します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- image columns
- image columns [Windows Forms], Windows Forms
- DataGridView control [Windows Forms], image columns
ms.assetid: 8a37aa75-3c6e-4893-91d0-7a5f34bfe287
ms.openlocfilehash: 649362055273c12c13b04fc06d4fdeb6d8d4b491
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54579486"
---
# <a name="how-to-work-with-image-columns-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="ebd41-102">方法: Windows フォーム DataGridView コントロールでイメージの列の使用します。</span><span class="sxs-lookup"><span data-stu-id="ebd41-102">How to: Work with Image Columns in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="ebd41-103">次のコード例は、対話型のユーザー インターフェイス (UI) で <xref:System.Windows.Forms.DataGridView> イメージ列を使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ebd41-103">The following code example shows how to use the <xref:System.Windows.Forms.DataGridView> image columns in an interactive user interface (UI).</span></span> <span data-ttu-id="ebd41-104">例では、<xref:System.Windows.Forms.DataGridViewImageColumn> を使用したイメージのサイズとレイアウトの可能性も示しています。</span><span class="sxs-lookup"><span data-stu-id="ebd41-104">The example also demonstrates image sizing and layout possibilities with the <xref:System.Windows.Forms.DataGridViewImageColumn>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ebd41-105">例</span><span class="sxs-lookup"><span data-stu-id="ebd41-105">Example</span></span>  
 [!code-cpp[System.Windows.Forms.DataGridView.ImageColumn_TicTacToe#0](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.ImageColumn_TicTacToe/CPP/tictactoe.cpp#0)]
 [!code-csharp[System.Windows.Forms.DataGridView.ImageColumn_TicTacToe#0](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.ImageColumn_TicTacToe/CS/tictactoe.cs#0)]
 [!code-vb[System.Windows.Forms.DataGridView.ImageColumn_TicTacToe#0](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.ImageColumn_TicTacToe/VB/tictactoe.vb#0)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ebd41-106">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="ebd41-106">Compiling the Code</span></span>  
 <span data-ttu-id="ebd41-107">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ebd41-107">This example requires:</span></span>  
  
-   <span data-ttu-id="ebd41-108">System アセンブリおよび System.Windows.Forms アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="ebd41-108">References to the System and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="ebd41-109">コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="ebd41-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="ebd41-110">新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="ebd41-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="ebd41-111">参照してください[方法。Visual Studio を使用して、完全な Windows フォームのコードの例をコンパイルして](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))します。</span><span class="sxs-lookup"><span data-stu-id="ebd41-111">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebd41-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebd41-112">See also</span></span>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewImageColumn>
- [<span data-ttu-id="ebd41-113">Windows フォーム DataGridView コントロールのセル、行、および列を使用したプログラミング</span><span class="sxs-lookup"><span data-stu-id="ebd41-113">Programming with Cells, Rows, and Columns in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/programming-with-cells-rows-and-columns-in-the-datagrid.md)
- [<span data-ttu-id="ebd41-114">方法: Windows フォーム DataGridView コントロールのセルにイメージを表示</span><span class="sxs-lookup"><span data-stu-id="ebd41-114">How to: Display Images in Cells of the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-display-images-in-cells-of-the-windows-forms-datagridview-control.md)
