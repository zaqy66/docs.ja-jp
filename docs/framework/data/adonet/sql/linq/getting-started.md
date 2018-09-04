---
title: 作業の開始
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: db8a557a-fef8-4f4f-bb91-8cff7250ee25
ms.openlocfilehash: 17b014a5a56a2c60359f6fb0b60df29feb97f2a7
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43529412"
---
# <a name="getting-started"></a><span data-ttu-id="1893a-102">作業の開始</span><span class="sxs-lookup"><span data-stu-id="1893a-102">Getting Started</span></span>
<span data-ttu-id="1893a-103">使用して[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]、使用することができます、[!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)]メモリ内コレクションにアクセスするようデータベースを SQL にアクセスするテクノロジ。</span><span class="sxs-lookup"><span data-stu-id="1893a-103">By using [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], you can use the [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)] technology to access SQL databases just as you would access an in-memory collection.</span></span>  
  
 <span data-ttu-id="1893a-104">たとえば、次のコードでは、`nw` データベースを表す `Northwind` オブジェクトが作成され、`Customers` テーブルが対象とされ、`Customers` からの `London` を選択するように行がフィルター処理され、取得する `CompanyName` の文字列が選択されます。</span><span class="sxs-lookup"><span data-stu-id="1893a-104">For example, the `nw` object in the following code is created to represent the `Northwind` database, the `Customers` table is targeted, the rows are filtered for `Customers` from `London`, and a string for `CompanyName` is selected for retrieval.</span></span>  
  
 <span data-ttu-id="1893a-105">ループが実行されると、`CompanyName` の値のコレクションが取得されます。</span><span class="sxs-lookup"><span data-stu-id="1893a-105">When the loop is executed, the collection of `CompanyName` values is retrieved.</span></span>  
  
 [!code-csharp[DLinqGettingStarted#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqGettingStarted/cs/Program.cs#1)]
 [!code-vb[DLinqGettingStarted#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqGettingStarted/vb/Module1.vb#1)]  
  
## <a name="next-steps"></a><span data-ttu-id="1893a-106">次の手順</span><span class="sxs-lookup"><span data-stu-id="1893a-106">Next Steps</span></span>  
 <span data-ttu-id="1893a-107">挿入や更新など、その他のいくつか例を参照してください[何することができます実行と LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/what-you-can-do-with-linq-to-sql.md)します。</span><span class="sxs-lookup"><span data-stu-id="1893a-107">For some additional examples, including inserting and updating, see [What You Can Do With LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/what-you-can-do-with-linq-to-sql.md).</span></span>  
  
 <span data-ttu-id="1893a-108">次に、チュートリアルで [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] の使用を実際に体験できます。</span><span class="sxs-lookup"><span data-stu-id="1893a-108">Next, try some walkthroughs and tutorials to have a hands-on experience of using [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span> <span data-ttu-id="1893a-109">参照してください[チュートリアルによる学習](../../../../../../docs/framework/data/adonet/sql/linq/learning-by-walkthroughs.md)します。</span><span class="sxs-lookup"><span data-stu-id="1893a-109">See [Learning by Walkthroughs](../../../../../../docs/framework/data/adonet/sql/linq/learning-by-walkthroughs.md).</span></span>  
  
 <span data-ttu-id="1893a-110">最後に、自分で開始する方法を学習[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]を読み取ることによってプロジェクト[一般的な手順を使用して LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/typical-steps-for-using-linq-to-sql.md)します。</span><span class="sxs-lookup"><span data-stu-id="1893a-110">Finally, learn how to get started on your own [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] project by reading [Typical Steps for Using LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/typical-steps-for-using-linq-to-sql.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1893a-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="1893a-111">See Also</span></span>  
 [<span data-ttu-id="1893a-112">LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="1893a-112">LINQ to SQL</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/index.md)  
 [<span data-ttu-id="1893a-113">LINQ の概要</span><span class="sxs-lookup"><span data-stu-id="1893a-113">Introduction to LINQ</span></span>](https://msdn.microsoft.com/library/24dddf19-12a0-4707-a4bc-eba4fa7f219e)  
 [<span data-ttu-id="1893a-114">LINQ to SQL オブジェクト モデル</span><span class="sxs-lookup"><span data-stu-id="1893a-114">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
