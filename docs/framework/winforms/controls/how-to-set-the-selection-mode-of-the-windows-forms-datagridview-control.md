---
title: '方法: Windows フォーム DataGridView コントロールの選択モードを設定します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- selection [Windows Forms], modes in DataGridView control
- DataGridView control [Windows Forms], selection mode
- data grids [Windows Forms], selection mode
ms.assetid: 2f241643-7f82-4583-8757-03494f63b465
ms.openlocfilehash: 65fb7360d45baea4fff20d06316d3955f0064207
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54539741"
---
# <a name="how-to-set-the-selection-mode-of-the-windows-forms-datagridview-control"></a><span data-ttu-id="ee1cf-102">方法: Windows フォーム DataGridView コントロールの選択モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee1cf-102">How to: Set the Selection Mode of the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="ee1cf-103">次のコード例は、構成する方法を示します、<xref:System.Windows.Forms.DataGridView>コントロールに自動的に、行内でクリックしてできるようには、全体の行を選択し、一度に 1 つだけその行を選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ee1cf-103">The following code example demonstrates how to configure a <xref:System.Windows.Forms.DataGridView> control so that clicking anywhere within a row automatically selects the entire row, and so that only one row at a time can be selected.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ee1cf-104">例</span><span class="sxs-lookup"><span data-stu-id="ee1cf-104">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#065](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#065)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#065](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#065)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ee1cf-105">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="ee1cf-105">Compiling the Code</span></span>  
 <span data-ttu-id="ee1cf-106">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ee1cf-106">This example requires:</span></span>  
  
-   <span data-ttu-id="ee1cf-107">`dataGridView1` という名前の <xref:System.Windows.Forms.DataGridView> コントロール。</span><span class="sxs-lookup"><span data-stu-id="ee1cf-107">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
-   <span data-ttu-id="ee1cf-108"><xref:System?displayProperty=nameWithType> アセンブリおよび <xref:System.Windows.Forms?displayProperty=nameWithType> アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="ee1cf-108">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee1cf-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee1cf-109">See also</span></span>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.MultiSelect%2A>
- <xref:System.Windows.Forms.DataGridView.SelectionMode%2A>
- <xref:System.Windows.Forms.DataGridViewSelectionMode>
- [<span data-ttu-id="ee1cf-110">Windows フォーム DataGridView コントロールでの選択およびクリップボードの使用</span><span class="sxs-lookup"><span data-stu-id="ee1cf-110">Selection and Clipboard Use with the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/selection-and-clipboard-use-with-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="ee1cf-111">Windows フォーム DataGridView コントロールの選択モード</span><span class="sxs-lookup"><span data-stu-id="ee1cf-111">Selection Modes in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/selection-modes-in-the-windows-forms-datagridview-control.md)
