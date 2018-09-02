---
title: '方法 : カスタムの ToolStripRenderer を実装する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStrip control [Windows Forms]
ms.assetid: c66fd3f7-2377-4553-8f1b-006527f08f32
ms.openlocfilehash: 91c04ba41a02c7c620c2f6c621505a19e0302c19
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43398116"
---
# <a name="how-to-implement-a-custom-toolstriprenderer"></a><span data-ttu-id="8b345-102">方法 : カスタムの ToolStripRenderer を実装する</span><span class="sxs-lookup"><span data-stu-id="8b345-102">How to: Implement a Custom ToolStripRenderer</span></span>
<span data-ttu-id="8b345-103"><xref:System.Windows.Forms.ToolStripRenderer> から派生するクラスを実装することで、<xref:System.Windows.Forms.ToolStrip> コントロールの外観をカスタマイズできます</span><span class="sxs-lookup"><span data-stu-id="8b345-103">You can customize the appearance of a <xref:System.Windows.Forms.ToolStrip> control by implementing a class that derives from <xref:System.Windows.Forms.ToolStripRenderer>.</span></span> <span data-ttu-id="8b345-104">これによって、<xref:System.Windows.Forms.ToolStripProfessionalRenderer> クラスや <xref:System.Windows.Forms.ToolStripSystemRenderer> クラスで提供される外観とは異なる外観を柔軟に作成できます。</span><span class="sxs-lookup"><span data-stu-id="8b345-104">This gives you the flexibility to create an appearance that differs from the appearance provided the <xref:System.Windows.Forms.ToolStripProfessionalRenderer> and <xref:System.Windows.Forms.ToolStripSystemRenderer> classes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8b345-105">例</span><span class="sxs-lookup"><span data-stu-id="8b345-105">Example</span></span>  
 <span data-ttu-id="8b345-106">次のコード例は、カスタムの <xref:System.Windows.Forms.ToolStripRenderer> クラスを実装する方法を示しています</span><span class="sxs-lookup"><span data-stu-id="8b345-106">The following code example demonstrates how to implement a custom <xref:System.Windows.Forms.ToolStripRenderer> class.</span></span> <span data-ttu-id="8b345-107">この例では、`GridStrip` コントロールでタイルをスライドさせるパズルを実装します。これは、ユーザーがテーブル レイアウト内のタイルを移動して 1 つの画像を作成するパズルです。</span><span class="sxs-lookup"><span data-stu-id="8b345-107">In this example, the `GridStrip` control implements a sliding-tile puzzle, which allows the user to move tiles in a table layout to form an image.</span></span> <span data-ttu-id="8b345-108">カスタムの <xref:System.Windows.Forms.ToolStrip> コントロールで、グリッド レイアウトの <xref:System.Windows.Forms.ToolStripButton> コントロールを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="8b345-108">A custom <xref:System.Windows.Forms.ToolStrip> control arranges its <xref:System.Windows.Forms.ToolStripButton> controls in a grid layout.</span></span> <span data-ttu-id="8b345-109">レイアウトには空のセルが 1 つ含まれており、ユーザーは、ドラッグ アンド ドロップ操作を使用することにより、隣接するタイルを空のセルにスライドできます。</span><span class="sxs-lookup"><span data-stu-id="8b345-109">The layout contains one empty cell, into which the user can slide an adjacent tile by using a drag-and-drop operation.</span></span> <span data-ttu-id="8b345-110">ユーザーが移動できるタイルは強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="8b345-110">Tiles that the user can move are highlighted.</span></span>  
  
 <span data-ttu-id="8b345-111">`GridStripRenderer` クラスでは `GridStrip` コントロールの外観を 3 つの点でカスタマイズしています。</span><span class="sxs-lookup"><span data-stu-id="8b345-111">The `GridStripRenderer` class customizes three aspects of the `GridStrip` control's appearance:</span></span>  
  
-   <span data-ttu-id="8b345-112">`GridStrip` の境界線</span><span class="sxs-lookup"><span data-stu-id="8b345-112">`GridStrip` border</span></span>  
  
-   <span data-ttu-id="8b345-113"><xref:System.Windows.Forms.ToolStripButton> の境界線</span><span class="sxs-lookup"><span data-stu-id="8b345-113"><xref:System.Windows.Forms.ToolStripButton> border</span></span>  
  
-   <span data-ttu-id="8b345-114"><xref:System.Windows.Forms.ToolStripButton> のイメージ</span><span class="sxs-lookup"><span data-stu-id="8b345-114"><xref:System.Windows.Forms.ToolStripButton> image</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.GridStrip#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.GridStrip/CS/GridStrip.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.GridStrip#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.GridStrip/VB/GridStrip.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="8b345-115">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="8b345-115">Compiling the Code</span></span>  
 <span data-ttu-id="8b345-116">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8b345-116">This example requires:</span></span>  
  
-   <span data-ttu-id="8b345-117">System.Drawing アセンブリおよび System.Windows.Forms アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="8b345-117">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="8b345-118">コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="8b345-118">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="8b345-119">新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="8b345-119">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="8b345-120">「[方法: 完成した Windows フォーム コードの例を Visual Studio を使ってコンパイルして実行する](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))」も参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b345-120">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b345-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="8b345-121">See Also</span></span>  
 <xref:System.Windows.Forms.MenuStrip>  
 <xref:System.Windows.Forms.ToolStrip>  
 <xref:System.Windows.Forms.ToolStripRenderer>  
 <xref:System.Windows.Forms.ToolStripProfessionalRenderer>  
 <xref:System.Windows.Forms.ToolStripSystemRenderer>  
 <xref:System.Windows.Forms.StatusStrip>  
 [<span data-ttu-id="8b345-122">ToolStrip コントロール</span><span class="sxs-lookup"><span data-stu-id="8b345-122">ToolStrip Control</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
