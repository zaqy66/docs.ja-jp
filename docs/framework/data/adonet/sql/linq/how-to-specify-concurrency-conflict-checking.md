---
title: '方法: 同時実行の競合のチェックを指定します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: c2547fcb-58eb-4377-9948-1b8d76a0f3d7
ms.openlocfilehash: 033a547b25e7280eb39be2698963391543437083
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54573726"
---
# <a name="how-to-specify-concurrency-conflict-checking"></a>方法: 同時実行の競合のチェックを指定します。
<xref:System.Data.Linq.DataContext.SubmitChanges%2A> を呼び出すときにコンカレンシーの競合をチェックするデータベース列を指定できます。 詳細については、「[方法 :同時実行の競合を検査するメンバーを指定](../../../../../../docs/framework/data/adonet/sql/linq/how-to-specify-which-members-are-tested-for-concurrency-conflicts.md)します。  
  
## <a name="example"></a>例  
 次のコード例では、更新の確認時に `HomePage` メンバーを検査しないことを指定しています。 詳細については、「 <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> 」を参照してください。  
  
 [!code-csharp[System.Data.Linq.Mapping.UpdateCheck#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.mapping.updatecheck/cs/northwind.cs#1)]
 [!code-vb[System.Data.Linq.Mapping.UpdateCheck#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.mapping.updatecheck/vb/northwind.vb#1)]  
  
## <a name="see-also"></a>関連項目
- [LINQ to SQL オブジェクト モデル](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [方法: コード エディターを使用してエンティティ クラスをカスタマイズします。](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
