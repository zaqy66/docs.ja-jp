---
title: '方法: パラメーターを受け取るストアド プロシージャを使用します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b935fd84-cb9c-4205-8c48-658d5db2ec93
ms.openlocfilehash: b81cb3b7428ba2ed4e958e18e9368f6f774e8ee3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604238"
---
# <a name="how-to-use-stored-procedures-that-take-parameters"></a>方法: パラメーターを受け取るストアド プロシージャを使用します。
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] は、出力パラメーターを参照パラメーターに対応付け、値型はパラメーターを null 許容型として宣言します。  
  
 入力パラメーターの行セットを返すクエリで使用する方法の例は、次を参照してください。[方法。行セットを返す](../../../../../../docs/framework/data/adonet/sql/linq/how-to-return-rowsets.md)します。  
  
## <a name="example"></a>例  
 次の例は、単一の入力パラメーター (顧客 ID) を受け取り、出力パラメーター (その顧客の売上合計) を返します。  
  
```  
CREATE PROCEDURE [dbo].[CustOrderTotal]   
@CustomerID nchar(5),  
@TotalSales money OUTPUT  
AS  
SELECT @TotalSales = SUM(OD.UNITPRICE*(1-OD.DISCOUNT) * OD.QUANTITY)  
FROM ORDERS O, "ORDER DETAILS" OD  
where O.CUSTOMERID = @CustomerID AND O.ORDERID = OD.ORDERID  
```  
  
 [!code-csharp[DLinqSprox#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSprox/cs/northwind-sprox.cs#2)]
 [!code-vb[DLinqSprox#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSprox/vb/northwind-sprox.vb#2)]  
  
## <a name="example"></a>例  
 このストアド プロシージャは次のように呼び出すことができます。  
  
 [!code-csharp[DLinqSprox#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSprox/cs/Program.cs#3)]
 [!code-vb[DLinqSprox#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSprox/vb/Module1.vb#3)]  
  
## <a name="see-also"></a>関連項目
- [ストアド プロシージャ](../../../../../../docs/framework/data/adonet/sql/linq/stored-procedures.md)
- [サンプル データベースのダウンロード](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)
- [Null 許容型の使用](~/docs/csharp/programming-guide/nullable-types/using-nullable-types.md)
- [null 許容値型](~/docs/visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
