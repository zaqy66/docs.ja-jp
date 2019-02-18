---
title: '方法: Windows フォーム DataGridView コントロールのボタン列のボタンを無効にします。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], disabling buttons
- buttons [Windows Forms], disabling in button columns
- DataGridView control [Windows Forms], disabling button cells
ms.assetid: 5c344d01-013a-4a6b-8f8d-62ec9321d81e
ms.openlocfilehash: b468e17213126162e13c1102a5bf261663899cb1
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56220128"
---
# <a name="how-to-disable-buttons-in-a-button-column-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="c1f1c-102">方法: Windows フォーム DataGridView コントロールのボタン列のボタンを無効にします。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-102">How to: Disable Buttons in a Button Column in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="c1f1c-103"><xref:System.Windows.Forms.DataGridView> コントロールには、ボタンのようなユーザー インターフェイス (UI) を持つセルを表示するための <xref:System.Windows.Forms.DataGridViewButtonCell> クラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-103">The <xref:System.Windows.Forms.DataGridView> control includes the <xref:System.Windows.Forms.DataGridViewButtonCell> class for displaying cells with a user interface (UI) like a button.</span></span> <span data-ttu-id="c1f1c-104">ただし、<xref:System.Windows.Forms.DataGridViewButtonCell> はセルによって表示されるボタンの外観を無効にする方法は提供しません。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-104">However, <xref:System.Windows.Forms.DataGridViewButtonCell> does not provide a way to disable the appearance of the button displayed by the cell.</span></span>  
  
 <span data-ttu-id="c1f1c-105">次のコード例は、<xref:System.Windows.Forms.DataGridViewButtonCell> クラスをカスタマイズして表示可能で無効になっているボタンを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-105">The following code example demonstrates how to customize the <xref:System.Windows.Forms.DataGridViewButtonCell> class to display buttons that can appear disabled.</span></span> <span data-ttu-id="c1f1c-106">この例は、<xref:System.Windows.Forms.DataGridViewButtonCell> から派生した新しいセルの種類 `DataGridViewDisableButtonCell` を定義します。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-106">The example defines a new cell type, `DataGridViewDisableButtonCell`, that derives from <xref:System.Windows.Forms.DataGridViewButtonCell>.</span></span> <span data-ttu-id="c1f1c-107">このセルの種類は、`false` に設定して無効になっているボタンをセルに描画する提供できる新しい `Enabled` プロパティを提供します。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-107">This cell type provides a new `Enabled` property that can be set to `false` to draw a disabled button in the cell.</span></span> <span data-ttu-id="c1f1c-108">例は、`DataGridViewDisableButtonCell` オブジェクトを表示する、新しい列の種類である `DataGridViewDisableButtonColumn` も定義します。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-108">The example also defines a new column type, `DataGridViewDisableButtonColumn`, that displays `DataGridViewDisableButtonCell` objects.</span></span> <span data-ttu-id="c1f1c-109">この新しいセルと列の種類を示すために、親の <xref:System.Windows.Forms.DataGridView> 内の各 <xref:System.Windows.Forms.DataGridViewCheckBoxCell> の現在値が、同じ行にある`DataGridViewDisableButtonCell` の `Enabled` プロパティが `true` と `false` のいずれであるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-109">To demonstrate this new cell and column type, the current value of each <xref:System.Windows.Forms.DataGridViewCheckBoxCell> in the parent <xref:System.Windows.Forms.DataGridView> determines whether the `Enabled` property of the `DataGridViewDisableButtonCell` in the same row is `true` or `false`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c1f1c-110"><xref:System.Windows.Forms.DataGridViewCell> や <xref:System.Windows.Forms.DataGridViewColumn> から派生したクラスに新しいプロパティを追加するときは、`Clone` メソッドをオーバーライドし、複製操作時に新しいプロパティをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-110">When you derive from <xref:System.Windows.Forms.DataGridViewCell> or <xref:System.Windows.Forms.DataGridViewColumn> and add new properties to the derived class, be sure to override the `Clone` method to copy the new properties during cloning operations.</span></span> <span data-ttu-id="c1f1c-111">また、基底クラスの `Clone` メソッドを呼び出して、基底クラスのプロパティを新しいセルまたは列にコピーする必要もあります。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-111">You should also call the base class's `Clone` method so that the properties of the base class are copied to the new cell or column.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c1f1c-112">例</span><span class="sxs-lookup"><span data-stu-id="c1f1c-112">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridView.DisabledButtons#0](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DisabledButtons/CS/form1.cs#0)]
 [!code-vb[System.Windows.Forms.DataGridView.DisabledButtons#0](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DisabledButtons/VB/form1.vb#0)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c1f1c-113">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="c1f1c-113">Compiling the Code</span></span>  
 <span data-ttu-id="c1f1c-114">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-114">This example requires:</span></span>  
  
-   <span data-ttu-id="c1f1c-115">System、System.Drawing、System.Windows.Forms、および System.Windows.Forms.VisualStyles の各アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-115">References to the System, System.Drawing, System.Windows.Forms and System.Windows.Forms.VisualStyles assemblies.</span></span>  
  
 <span data-ttu-id="c1f1c-116">コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-116">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="c1f1c-117">新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="c1f1c-117">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1f1c-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1f1c-118">See also</span></span>
- [<span data-ttu-id="c1f1c-119">Windows フォーム DataGridView コントロールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="c1f1c-119">Customizing the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/customizing-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="c1f1c-120">DataGridView コントロールのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="c1f1c-120">DataGridView Control Architecture</span></span>](../../../../docs/framework/winforms/controls/datagridview-control-architecture-windows-forms.md)
- [<span data-ttu-id="c1f1c-121">Windows フォーム DataGridView コントロールの列型</span><span class="sxs-lookup"><span data-stu-id="c1f1c-121">Column Types in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/column-types-in-the-windows-forms-datagridview-control.md)
