---
title: '方法: LINQ to SQL コマンドの表示'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1decb05e-37ad-4ed6-ab2f-071eb4c4f628
ms.openlocfilehash: a70f1e0dd471e86afe2e744c157d4aed2a217deb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54630828"
---
# <a name="how-to-display-linq-to-sql-commands"></a><span data-ttu-id="fec33-102">方法: LINQ to SQL コマンドの表示</span><span class="sxs-lookup"><span data-stu-id="fec33-102">How to: Display LINQ to SQL Commands</span></span>
<span data-ttu-id="fec33-103">SQL コマンドとその他の情報を表示するには、<xref:System.Data.Linq.DataContext.GetCommand%2A> を使用します。</span><span class="sxs-lookup"><span data-stu-id="fec33-103">Use <xref:System.Data.Linq.DataContext.GetCommand%2A> to display SQL commands and other information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fec33-104">例</span><span class="sxs-lookup"><span data-stu-id="fec33-104">Example</span></span>  
 <span data-ttu-id="fec33-105">クエリからの出力、生成された SQL コマンド、コマンドの種類、および接続の種類をコンソール ウィンドウに表示する例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="fec33-105">In the following example, the console window displays the output from the query, followed by the SQL commands that are generated, the type of commands, and the type of connection.</span></span>  
  
 [!code-csharp[DLinqDebuggingSupport#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqDebuggingSupport/cs/Program.cs#3)]
 [!code-vb[DLinqDebuggingSupport#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqDebuggingSupport/vb/Module1.vb#3)]  
  
 <span data-ttu-id="fec33-106">次のような出力が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fec33-106">Output appears as follows:</span></span>  
  
```  
Customers from London:  
    Thomas Hardy  
    Victoria Ashworth  
    Elizabeth Brown  
    Ann Devon  
    Simon Crowther  
    Marie Bertrand  
    Hari Kumar  
    Dominique Perrier  
```  
  
```  
Command Text:  
SELECT [t0].[CustomerID], [t0].[CompanyName], [t0].[ContactName], [t0].[ContactT  
itle], [t0].[Address], [t0].[City], [t0].[Region], [t0].[PostalCode], [t0].[Coun  
try], [t0].[Phone], [t0].[Fax]  
FROM [dbo].[Customers] AS [t0]  
WHERE [t0].[City] = @p0  
  
Command Type: Text  
  
Connection: System.Data.SqlClient.SqlConnection  
```  
  
## <a name="see-also"></a><span data-ttu-id="fec33-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="fec33-107">See also</span></span>
- [<span data-ttu-id="fec33-108">デバッグのサポート</span><span class="sxs-lookup"><span data-stu-id="fec33-108">Debugging Support</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/debugging-support.md)
