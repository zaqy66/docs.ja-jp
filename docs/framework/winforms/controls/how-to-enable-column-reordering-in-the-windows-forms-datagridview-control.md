---
title: '方法 : Windows フォーム DataGridView コントロールの列の並べ替えを有効にする'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], column order
- data grids [Windows Forms], reordering columns
- columns [Windows Forms], reordering
ms.assetid: cc20eae3-e4db-493f-95ce-a4215e29472a
ms.openlocfilehash: cfe61860e21a7c1b8317d22880440745d49e6751
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43489826"
---
# <a name="how-to-enable-column-reordering-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="12c05-102">方法 : Windows フォーム DataGridView コントロールの列の並べ替えを有効にする</span><span class="sxs-lookup"><span data-stu-id="12c05-102">How to: Enable Column Reordering in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="12c05-103"><xref:System.Windows.Forms.DataGridView> コントロールで列の並べ替えを有効にすると、ユーザーは列ヘッダーをマウスでドラッグすることにより列を新しい場所に移動できます。</span><span class="sxs-lookup"><span data-stu-id="12c05-103">When you enable column reordering in the <xref:System.Windows.Forms.DataGridView> control, users can move a column to a new position by dragging the column header with the mouse.</span></span> <span data-ttu-id="12c05-104"><xref:System.Windows.Forms.DataGridView> コントロールでは、<xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType> プロパティ値によってユーザーが列を別の場所に移動できるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="12c05-104">In the <xref:System.Windows.Forms.DataGridView> control, the <xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType> property value determines whether users can move columns to different positions.</span></span>  
  
 <span data-ttu-id="12c05-105">Visual Studio では、このタスクに対するサポートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="12c05-105">There is support for this task in Visual Studio.</span></span>  <span data-ttu-id="12c05-106">参照してください[方法: Windows フォーム DataGridView コントロールを使用して、デザイナーで列の並べ替えを有効にします。](https://msdn.microsoft.com/library/8xwtyc86\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="12c05-106">Also see [How to: Enable Column Reordering in the Windows Forms DataGridView Control Using the Designer](https://msdn.microsoft.com/library/8xwtyc86\(v=vs.110\))</span></span>  
  
### <a name="to-enable-column-reordering-programmatically"></a><span data-ttu-id="12c05-107">プログラムで列の並べ替えを有効にするには</span><span class="sxs-lookup"><span data-stu-id="12c05-107">To enable column reordering programmatically</span></span>  
  
-   <span data-ttu-id="12c05-108"><xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType> プロパティを `true` に設定します。</span><span class="sxs-lookup"><span data-stu-id="12c05-108">Set the <xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType> property to `true`.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#060](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#060)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#060](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#060)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="12c05-109">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="12c05-109">Compiling the Code</span></span>  
 <span data-ttu-id="12c05-110">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="12c05-110">This example requires:</span></span>  
  
-   <span data-ttu-id="12c05-111">`dataGridView1` という名前の <xref:System.Windows.Forms.DataGridView> コントロール。</span><span class="sxs-lookup"><span data-stu-id="12c05-111">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
-   <span data-ttu-id="12c05-112"><xref:System?displayProperty=nameWithType> アセンブリおよび <xref:System.Windows.Forms?displayProperty=nameWithType> アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="12c05-112">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12c05-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="12c05-113">See Also</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="12c05-114">Windows フォーム DataGridView コントロールでの列、行、およびセルの基本機能</span><span class="sxs-lookup"><span data-stu-id="12c05-114">Basic Column, Row, and Cell Features in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/basic-column-row-and-cell-features-wf-datagridview-control.md)  
 [<span data-ttu-id="12c05-115">方法: Windows フォーム DataGridView コントロールの列を固定する</span><span class="sxs-lookup"><span data-stu-id="12c05-115">How to: Freeze Columns in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-freeze-columns-in-the-windows-forms-datagridview-control.md)
