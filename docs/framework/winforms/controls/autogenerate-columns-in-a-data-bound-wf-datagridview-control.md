---
title: '方法: データ バインド Windows フォームの DataGridView コントロールで列を自動生成'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], autogenerating columns
- columns [Windows Forms], autogenerating
- DataGridView control [Windows Forms], data-bound columns
ms.assetid: 699f6f9e-6aa5-4811-902b-6a2c57dec7d6
ms.openlocfilehash: 1968968461edb475be4cd30261a66b53cd7f0e94
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554012"
---
# <a name="how-to-autogenerate-columns-in-a-data-bound-windows-forms-datagridview-control"></a><span data-ttu-id="e645e-102">方法: データ バインド Windows フォームの DataGridView コントロールで列を自動生成</span><span class="sxs-lookup"><span data-stu-id="e645e-102">How to: Autogenerate Columns in a Data-Bound Windows Forms DataGridView Control</span></span>
<span data-ttu-id="e645e-103">次のコード例は、バインドされたデータ ソースから列を表示する方法を示します、<xref:System.Windows.Forms.DataGridView>コントロール。</span><span class="sxs-lookup"><span data-stu-id="e645e-103">The following code example demonstrates how to display columns from a bound data source in a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="e645e-104">ときに、<xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A>プロパティの値が`true`(既定)、<xref:System.Windows.Forms.DataGridViewColumn>データ ソース テーブル内の各列が作成されます。</span><span class="sxs-lookup"><span data-stu-id="e645e-104">When the <xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A> property value is `true` (the default), a <xref:System.Windows.Forms.DataGridViewColumn> is created for each column in the data source table.</span></span>  
  
 <span data-ttu-id="e645e-105">場合、<xref:System.Windows.Forms.DataGridView>コントロールは既に列を設定すると、<xref:System.Windows.Forms.DataGridViewComboBoxColumn.DataSource%2A>プロパティの既存のバインドされた列がデータ ソース内の列と比較され、一致があるたびに保持されます。</span><span class="sxs-lookup"><span data-stu-id="e645e-105">If the <xref:System.Windows.Forms.DataGridView> control already has columns when you set the <xref:System.Windows.Forms.DataGridViewComboBoxColumn.DataSource%2A> property, the existing bound columns are compared to the columns in the data source and preserved whenever there is a match.</span></span> <span data-ttu-id="e645e-106">バインドされていない列は常に保持されます。</span><span class="sxs-lookup"><span data-stu-id="e645e-106">Unbound columns are always preserved.</span></span> <span data-ttu-id="e645e-107">対象のデータ ソース内の一致がないバインドされた列が削除されます。</span><span class="sxs-lookup"><span data-stu-id="e645e-107">Bound columns for which there is no match in the data source are removed.</span></span> <span data-ttu-id="e645e-108">コントロール内の一致がないデータ ソース内の列が新規生成<xref:System.Windows.Forms.DataGridViewColumn>、オブジェクトの末尾に追加される、<xref:System.Windows.Forms.DataGridView.Columns%2A>コレクション。</span><span class="sxs-lookup"><span data-stu-id="e645e-108">Columns in the data source for which there is no match in the control generate new <xref:System.Windows.Forms.DataGridViewColumn> objects, which are added to the end of the <xref:System.Windows.Forms.DataGridView.Columns%2A> collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e645e-109">例</span><span class="sxs-lookup"><span data-stu-id="e645e-109">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#020](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#020)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#020](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#020)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e645e-110">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="e645e-110">Compiling the Code</span></span>  
 <span data-ttu-id="e645e-111">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e645e-111">This example requires:</span></span>  
  
-   <span data-ttu-id="e645e-112">`customersDataGridView` という名前の <xref:System.Windows.Forms.DataGridView> コントロール。</span><span class="sxs-lookup"><span data-stu-id="e645e-112">A <xref:System.Windows.Forms.DataGridView> control named `customersDataGridView`.</span></span>  
  
-   <span data-ttu-id="e645e-113">A<xref:System.Data.DataSet>という名前のオブジェクト`customersDataSet`という名前のテーブルを持つ`Customers`します。</span><span class="sxs-lookup"><span data-stu-id="e645e-113">A <xref:System.Data.DataSet> object named `customersDataSet` that has a table named `Customers`.</span></span>  
  
-   <span data-ttu-id="e645e-114"><xref:System?displayProperty=nameWithType>、<xref:System.Windows.Forms?displayProperty=nameWithType>、<xref:System.Data?displayProperty=nameWithType>、および <xref:System.Xml?displayProperty=nameWithType> の各アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="e645e-114">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, <xref:System.Data?displayProperty=nameWithType>, and <xref:System.Xml?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e645e-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="e645e-115">See also</span></span>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A?displayProperty=nameWithType>
- [<span data-ttu-id="e645e-116">Windows フォーム DataGridView コントロールでのデータの表示</span><span class="sxs-lookup"><span data-stu-id="e645e-116">Displaying Data in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/displaying-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="e645e-117">方法: Windows フォーム DataGridView コントロールから自動生成された列を削除します。</span><span class="sxs-lookup"><span data-stu-id="e645e-117">How to: Remove Autogenerated Columns from a Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/remove-autogenerated-columns-from-a-wf-datagridview-control.md)
