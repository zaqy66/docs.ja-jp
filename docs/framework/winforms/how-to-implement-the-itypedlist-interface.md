---
title: '方法: ITypedList インターフェイスを実装します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ITypedList interface
- BindingList(Of T) class
- data binding [Windows Forms], implementing
- IBindingList interface
ms.assetid: 834cc15c-50bc-4a8b-a610-313d6a217357
ms.openlocfilehash: 3d12c0b82d9475981d0c72f082665b11135d8bb0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54562169"
---
# <a name="how-to-implement-the-itypedlist-interface"></a><span data-ttu-id="9484e-102">方法: ITypedList インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="9484e-102">How to: Implement the ITypedList Interface</span></span>
<span data-ttu-id="9484e-103">実装、<xref:System.ComponentModel.ITypedList>バインド可能な一覧については、スキーマの検出を有効にするインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="9484e-103">Implement the <xref:System.ComponentModel.ITypedList> interface to enable discovery of the schema for a bindable list.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9484e-104">例</span><span class="sxs-lookup"><span data-stu-id="9484e-104">Example</span></span>  
 <span data-ttu-id="9484e-105">次のコード例は、実装する方法を示します、<xref:System.ComponentModel.ITypedList>インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="9484e-105">The following code example demonstrates how to implement the <xref:System.ComponentModel.ITypedList> interface.</span></span> <span data-ttu-id="9484e-106">という名前のジェネリック型`SortableBindingList`から派生した、<xref:System.ComponentModel.BindingList%601>クラスを実装、<xref:System.ComponentModel.ITypedList>インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="9484e-106">A generic type named `SortableBindingList` derives from the <xref:System.ComponentModel.BindingList%601> class and implements the <xref:System.ComponentModel.ITypedList> interface.</span></span> <span data-ttu-id="9484e-107">という名前の単純なクラス`Customer`のヘッダーにはバインドされているデータを提供する<xref:System.Windows.Forms.DataGridView>コントロール。</span><span class="sxs-lookup"><span data-stu-id="9484e-107">A simple class named `Customer` provides data, which is bound to the header of a <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 [!code-csharp[System.ComponentModel.ITypedList#1](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/SortableBindingList.cs#1)]
 [!code-vb[System.ComponentModel.ITypedList#1](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/SortableBindingList.vb#1)]  
  
 [!code-csharp[System.ComponentModel.ITypedList#10](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/Customer.cs#10)]
 [!code-vb[System.ComponentModel.ITypedList#10](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/Customer.vb#10)]  
  
 [!code-csharp[System.ComponentModel.ITypedList#100](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/Form1.cs#100)]
 [!code-vb[System.ComponentModel.ITypedList#100](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/Form1.vb#100)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="9484e-108">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="9484e-108">Compiling the Code</span></span>  
 <span data-ttu-id="9484e-109">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9484e-109">This example requires:</span></span>  
  
-   <span data-ttu-id="9484e-110">System.Drawing アセンブリおよび System.Windows.Forms アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="9484e-110">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9484e-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="9484e-111">See also</span></span>
- <xref:System.ComponentModel.ITypedList>
- <xref:System.ComponentModel.BindingList%601>
- <xref:System.ComponentModel.IBindingList>
- [<span data-ttu-id="9484e-112">データ連結と Windows フォーム</span><span class="sxs-lookup"><span data-stu-id="9484e-112">Data Binding and Windows Forms</span></span>](../../../docs/framework/winforms/data-binding-and-windows-forms.md)
