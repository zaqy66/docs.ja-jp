---
title: SET (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 28b4deac-c7e4-4f09-b428-4d352ef2dc94
ms.openlocfilehash: b6adce314e5d4fb1e4077b0efef758d07444e496
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54744441"
---
# <a name="set-entity-sql"></a><span data-ttu-id="7cfe1-102">SET (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="7cfe1-102">SET (Entity SQL)</span></span>
<span data-ttu-id="7cfe1-103">SET 式は、重複する要素をすべて除外した新しいコレクションを生成することによって、オブジェクトのコレクションを 1 つの集合に変換します。</span><span class="sxs-lookup"><span data-stu-id="7cfe1-103">The SET expression is used to convert a collection of objects into a set by yielding a new collection with all duplicate elements removed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7cfe1-104">構文</span><span class="sxs-lookup"><span data-stu-id="7cfe1-104">Syntax</span></span>  
  
```  
SET ( expression )  
```  
  
## <a name="arguments"></a><span data-ttu-id="7cfe1-105">引数</span><span class="sxs-lookup"><span data-stu-id="7cfe1-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="7cfe1-106">コレクションを返す任意の有効なクエリ式。</span><span class="sxs-lookup"><span data-stu-id="7cfe1-106">Any valid query expression that returns a collection.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7cfe1-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="7cfe1-107">Remarks</span></span>  
 <span data-ttu-id="7cfe1-108">集合式 `SET(c)` は、論理上、次の select ステートメントと等価です。</span><span class="sxs-lookup"><span data-stu-id="7cfe1-108">The set expression `SET(c)` is logically equivalent to the following select statement:</span></span>  
  
```  
SELECT VALUE DISTINCT c FROM c  
```  
  
 <span data-ttu-id="7cfe1-109">`SET` は、 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] の集合演算子の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="7cfe1-109">`SET` is one of the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span> <span data-ttu-id="7cfe1-110">[!INCLUDE[esql](../../../../../../includes/esql-md.md)] のすべての集合演算子は左から右に評価されます。</span><span class="sxs-lookup"><span data-stu-id="7cfe1-110">All [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators are evaluated from left to right.</span></span> <span data-ttu-id="7cfe1-111">参照してください[EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md)の優先順位は、[!INCLUDE[esql](../../../../../../includes/esql-md.md)]演算子を設定します。</span><span class="sxs-lookup"><span data-stu-id="7cfe1-111">See [EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md) for precedence information for the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7cfe1-112">例</span><span class="sxs-lookup"><span data-stu-id="7cfe1-112">Example</span></span>  
 <span data-ttu-id="7cfe1-113">次の Entity SQL クエリでは、SET 式を使用して、オブジェクトのコレクションを 1 つの集合に変換します。</span><span class="sxs-lookup"><span data-stu-id="7cfe1-113">The following Entity SQL query uses the SET expression to convert a collection of objects into a set.</span></span> <span data-ttu-id="7cfe1-114">このクエリは、AdventureWorks Sales Model に基づいています。</span><span class="sxs-lookup"><span data-stu-id="7cfe1-114">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="7cfe1-115">このクエリをコンパイルして実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7cfe1-115">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="7cfe1-116">」の手順に従って[方法。PrimitiveType 結果を返すクエリを実行](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md)します。</span><span class="sxs-lookup"><span data-stu-id="7cfe1-116">Follow the procedure in [How to: Execute a Query that Returns PrimitiveType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md).</span></span>  
  
2.  <span data-ttu-id="7cfe1-117">次のクエリを引数として `ExecutePrimitiveTypeQuery` メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="7cfe1-117">Pass the following query as an argument to the `ExecutePrimitiveTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#SET](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#set)]  
  
## <a name="see-also"></a><span data-ttu-id="7cfe1-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="7cfe1-118">See also</span></span>
- [<span data-ttu-id="7cfe1-119">Entity SQL リファレンス</span><span class="sxs-lookup"><span data-stu-id="7cfe1-119">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
