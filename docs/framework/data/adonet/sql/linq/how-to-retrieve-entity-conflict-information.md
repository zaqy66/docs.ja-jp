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
# <a name="how-to-retrieve-entity-conflict-information"></a>方法: エンティティの競合情報を取得します。
<xref:System.Data.Linq.ObjectChangeConflict> クラスのオブジェクトを使用して、<xref:System.Data.Linq.ChangeConflictException> 例外によって発生する競合に関する情報を提供できます。 詳細については、次を参照してください。[オプティミスティック同時実行制御。概要](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md)します。  
  
## <a name="example"></a>例  
 次の例では、累積した競合のリストを反復処理します。  
  
 [!code-csharp[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.objectchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.objectchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a>関連項目
- [方法: 変更の競合を管理します。](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
