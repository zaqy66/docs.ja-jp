---
title: BETWEEN (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 4dcdd754-ae01-4e78-bf28-8a117fb2b73e
ms.openlocfilehash: cface8ab50e53f21293ad54ea6961c7e308080b3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54690693"
---
# <a name="between-entity-sql"></a>BETWEEN (Entity SQL)
式の結果が指定の範囲内の値になるかどうかを判断します。 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] BETWEEN 式が TRANSACT-SQL の BETWEEN 式と同じ機能です。  
  
## <a name="syntax"></a>構文  
  
```  
expression [ NOT ] BETWEEN begin_expression AND end_expression    
```  
  
## <a name="arguments"></a>引数  
 `expression`  
 `begin_expression` と `end_expression` で定義される範囲についてテストするための任意の有効な式。 `expression` は、`begin_expression` と `end_expression` の両方と同じ型にする必要があります。  
  
 `begin_expression`  
 任意の有効な式。 `begin_expression` は、`expression` と `end_expression` の両方と同じ型にする必要があります。 `begin_expression` は、`end_expression` 未満でなければなりません。それ以外の場合、戻り値は否定されます。  
  
 `end_expression`  
 任意の有効な式。 `end_expression` は、`expression` と `begin_expression` の両方と同じ型にする必要があります。  
  
 NOT  
 BETWEEN の結果を否定することを指定します。  
  
 AND  
 `expression` と `begin_expression` で表される範囲内で `end_expression` をテストする必要があることを示すプレースホルダーです。  
  
## <a name="return-value"></a>戻り値  
 `true` が、`expression` と `begin_expression` で指定される範囲内にある場合は `end_expression`。それ以外の場合は `false`。 `null` が `expression` であるか、`null` または `begin_expression` が `end_expression` である場合は、`null` が返されます。  
  
## <a name="remarks"></a>Remarks  
 両端を除いた範囲を指定するには、BETWEEN の代わりに、より大きい (>) とより小さい (<) を意味する演算子を使用します。  
  
## <a name="example"></a>例  
 次の Entity SQL クエリでは、BETWEEN 演算子を使用して、式の結果が指定の範囲内の値になるかどうかを調べます。 このクエリは、AdventureWorks Sales Model に基づいています。 このクエリをコンパイルして実行するには、次の手順を実行します。  
  
1.  」の手順に従って[方法。StructuralType 結果を返すクエリを実行](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)します。  
  
2.  次のクエリを引数として `ExecuteStructuralTypeQuery` メソッドに渡します。  
  
 [!code-csharp[DP EntityServices Concepts 2#BETWEEN](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#between)]  
  
## <a name="see-also"></a>関連項目
- [Entity SQL リファレンス](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
