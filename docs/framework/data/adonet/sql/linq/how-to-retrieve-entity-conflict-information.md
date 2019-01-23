---
title: '方法: エンティティの競合情報を取得します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 9a02b608-e7bb-4041-a452-a7fed26fd008
ms.openlocfilehash: 1c2f9a5f822d8783f997c9c5c09ef508c2d8dca7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629034"
---
# <a name="how-to-retrieve-entity-conflict-information"></a><span data-ttu-id="f0176-102">方法: エンティティの競合情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="f0176-102">How to: Retrieve Entity Conflict Information</span></span>
<span data-ttu-id="f0176-103"><xref:System.Data.Linq.ObjectChangeConflict> クラスのオブジェクトを使用して、<xref:System.Data.Linq.ChangeConflictException> 例外によって発生する競合に関する情報を提供できます。</span><span class="sxs-lookup"><span data-stu-id="f0176-103">You can use objects of the <xref:System.Data.Linq.ObjectChangeConflict> class to provide information about conflicts revealed by <xref:System.Data.Linq.ChangeConflictException> exceptions.</span></span> <span data-ttu-id="f0176-104">詳細については、次を参照してください。[オプティミスティック同時実行制御。概要](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md)します。</span><span class="sxs-lookup"><span data-stu-id="f0176-104">For more information, see [Optimistic Concurrency: Overview](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f0176-105">例</span><span class="sxs-lookup"><span data-stu-id="f0176-105">Example</span></span>  
 <span data-ttu-id="f0176-106">次の例では、累積した競合のリストを反復処理します。</span><span class="sxs-lookup"><span data-stu-id="f0176-106">The following example iterates through a list of accumulated conflicts.</span></span>  
  
 [!code-csharp[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.objectchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.objectchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="f0176-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0176-107">See also</span></span>
- [<span data-ttu-id="f0176-108">方法: 変更の競合を管理します。</span><span class="sxs-lookup"><span data-stu-id="f0176-108">How to: Manage Change Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
