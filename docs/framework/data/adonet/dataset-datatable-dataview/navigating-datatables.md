---
title: DataTable の移動
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 202026a1-ec79-435e-b507-12a77f5011b2
ms.openlocfilehash: f00e2171c1adf4ff99a669085131ebc8d38f7006
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47207722"
---
# <a name="navigating-datatables"></a><span data-ttu-id="5e1b6-102">DataTable の移動</span><span class="sxs-lookup"><span data-stu-id="5e1b6-102">Navigating DataTables</span></span>
<span data-ttu-id="5e1b6-103"><xref:System.Data.DataTableReader> は、1 つ以上の <xref:System.Data.DataTable> オブジェクトの内容を、読み取り専用、前方参照専用の 1 つ以上の結果セットとして取得します。</span><span class="sxs-lookup"><span data-stu-id="5e1b6-103">The <xref:System.Data.DataTableReader> obtains the contents of one or more <xref:System.Data.DataTable> objects in the form of one or more read-only, forward-only result sets.</span></span>  
  
 <span data-ttu-id="5e1b6-104"><xref:System.Data.DataTableReader> メソッドの呼び出しにより DataTableReader を作成した場合、<xref:System.Data.DataSet.CreateDataReader%2A> に複数の結果セットが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="5e1b6-104">A <xref:System.Data.DataTableReader> may contain multiple result sets if it is created by using the <xref:System.Data.DataSet.CreateDataReader%2A> method.</span></span> <span data-ttu-id="5e1b6-105">結果セットが複数ある場合、<xref:System.Data.DataTableReader.NextResult%2A> メソッドは、カーソルを次の結果セットに移動します。</span><span class="sxs-lookup"><span data-stu-id="5e1b6-105">When there is more than one result set, the <xref:System.Data.DataTableReader.NextResult%2A> method advances the cursor to the next result set.</span></span> <span data-ttu-id="5e1b6-106">これは前方参照専用です。</span><span class="sxs-lookup"><span data-stu-id="5e1b6-106">This is a forward-only process.</span></span> <span data-ttu-id="5e1b6-107">前の結果セットに戻ることはできません。</span><span class="sxs-lookup"><span data-stu-id="5e1b6-107">It is not possible to return to a previous result set.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5e1b6-108">例</span><span class="sxs-lookup"><span data-stu-id="5e1b6-108">Example</span></span>  
 <span data-ttu-id="5e1b6-109">次の例では、`TestConstructor`メソッドでは、2 つ作成されます<xref:System.Data.DataTable>インスタンス。</span><span class="sxs-lookup"><span data-stu-id="5e1b6-109">In the following example, the `TestConstructor` method creates two <xref:System.Data.DataTable> instances.</span></span> <span data-ttu-id="5e1b6-110">このコンス トラクターを示すために、<xref:System.Data.DataTableReader>クラス、サンプルを作成する新しい**DataTableReader** 、2 つを格納する配列に基づく**Datatable**、し、単純な操作を実行します。最初のいくつかの列から、コンソール ウィンドウに内容を印刷します。</span><span class="sxs-lookup"><span data-stu-id="5e1b6-110">In order to demonstrate this constructor for the <xref:System.Data.DataTableReader> class, the sample creates a new **DataTableReader** based on an array that contains the two **DataTables**, and performs a simple operation, printing the contents from the first few columns to the console window.</span></span>  
  
 [!code-csharp[DataWorks DataTableReader.NextResult#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks DataTableReader.NextResult/CS/source.cs#1)]
 [!code-vb[DataWorks DataTableReader.NextResult#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks DataTableReader.NextResult/VB/source.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="5e1b6-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e1b6-111">See Also</span></span>  
 [<span data-ttu-id="5e1b6-112">DataTableReaders</span><span class="sxs-lookup"><span data-stu-id="5e1b6-112">DataTableReaders</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatablereaders.md)  
 [<span data-ttu-id="5e1b6-113">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="5e1b6-113">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
