---
title: メソッド ベースのクエリ構文例:要素演算子
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8438b995-bd07-4223-b22d-13adadef33fb
ms.openlocfilehash: 89cbda4d049b30ee50accf94d5b7ec172bc25ae2
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2019
ms.locfileid: "55826500"
---
# <a name="method-based-query-syntax-examples-element-operators"></a><span data-ttu-id="8167f-102">メソッド ベースのクエリ構文例:要素演算子</span><span class="sxs-lookup"><span data-stu-id="8167f-102">Method-Based Query Syntax Examples: Element Operators</span></span>
<span data-ttu-id="8167f-103">このトピックの例では、使用する方法を示します、<xref:System.Linq.Enumerable.First%2A>メソッド クエリを[AdventureWorks Sales Model](https://archive.codeplex.com/?p=msftdbprodsamples)メソッド ベースのクエリ構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="8167f-103">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.First%2A> method to query the [AdventureWorks Sales Model](https://archive.codeplex.com/?p=msftdbprodsamples) using method-based query syntax.</span></span> <span data-ttu-id="8167f-104">これらの例で使用されている、AdventureWorks Sales Model は、AdventureWorks サンプル データベースの Contact、Address、Product、SalesOrderHeader、SalesOrderDetail の各テーブルから作成されています。</span><span class="sxs-lookup"><span data-stu-id="8167f-104">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="8167f-105">このトピックの例では、次を使用して`using` / `Imports`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="8167f-105">The example in this topic uses the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="first"></a><span data-ttu-id="8167f-106">First</span><span class="sxs-lookup"><span data-stu-id="8167f-106">First</span></span>  
  
### <a name="example"></a><span data-ttu-id="8167f-107">例</span><span class="sxs-lookup"><span data-stu-id="8167f-107">Example</span></span>  
 <span data-ttu-id="8167f-108">次の例では、 <xref:System.Linq.Enumerable.First%2A> 'caroline' で始まる最初の電子メール アドレスを検索するメソッド。</span><span class="sxs-lookup"><span data-stu-id="8167f-108">The following example uses the <xref:System.Linq.Enumerable.First%2A> method to find the first email address that starts with 'caroline'.</span></span>  
  
 [!code-csharp[DP L2E Examples#FirstCondition_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#firstcondition_mq)]
 [!code-vb[DP L2E Examples#FirstCondition_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#firstcondition_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="8167f-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="8167f-109">See also</span></span>
- [<span data-ttu-id="8167f-110">LINQ to Entities でのクエリ</span><span class="sxs-lookup"><span data-stu-id="8167f-110">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
