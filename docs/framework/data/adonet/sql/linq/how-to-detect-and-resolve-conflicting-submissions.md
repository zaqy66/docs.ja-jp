---
title: '方法: 検出および送信の競合を解決します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 91e27206-01fb-4c7a-8afc-1383a6ac5067
ms.openlocfilehash: ab1b56d409a3b185be15ebc8dc119a57038d55bd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54510508"
---
# <a name="how-to-detect-and-resolve-conflicting-submissions"></a>方法: 検出および送信の競合を解決します。
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] には、複数のユーザーがデータベースを変更するために生じる競合を、検出および解決するための多くのリソースが用意されています。 詳細については、「[方法 :変更の競合を管理](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)します。  
  
## <a name="example"></a>例  
 次の例は、 `try` / `catch`キャッチ ブロックを<xref:System.Data.Linq.ChangeConflictException>例外。 各競合のエンティティおよびメンバー情報が、コンソール ウィンドウに表示されます。  
  
> [!NOTE]
>  情報の取得をサポートするには、`using System.Reflection` ディレクティブ (Visual Basic の場合は `Imports System.Reflection`) を含める必要があります。 詳細については、「 <xref:System.Reflection> 」を参照してください。  
  
 [!code-csharp[DLinqSubmittingChanges#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#2)]
 [!code-vb[DLinqSubmittingChanges#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#2)]  
  
## <a name="see-also"></a>関連項目
- [データの変更と変更の送信](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
- [方法: 変更の競合を管理します。](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
