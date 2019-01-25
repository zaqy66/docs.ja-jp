---
title: OVERLAPS (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 41743e89-79cb-4d7b-8a27-355b45024b61
ms.openlocfilehash: 8ab2b00767aed19cff5448d811d7cdcd1871d9a7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54679332"
---
# <a name="overlaps-entity-sql"></a><span data-ttu-id="e1f31-102">OVERLAPS (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="e1f31-102">OVERLAPS (Entity SQL)</span></span>
<span data-ttu-id="e1f31-103">2 つのコレクションに共通の要素が存在するかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="e1f31-103">Determines whether two collections have common elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e1f31-104">構文</span><span class="sxs-lookup"><span data-stu-id="e1f31-104">Syntax</span></span>  
  
```  
expression OVERLAPS expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="e1f31-105">引数</span><span class="sxs-lookup"><span data-stu-id="e1f31-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="e1f31-106">コレクションを返す任意の有効なクエリ式。もう一方のクエリ式から返されたコレクションと比較されます。</span><span class="sxs-lookup"><span data-stu-id="e1f31-106">Any valid query expression that returns a collection to compare with the collection returned from another query expression.</span></span> <span data-ttu-id="e1f31-107">すべての式は、 `expression`と同じ型であるか、共通の基本型または派生型である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1f31-107">All expressions must be of the same type or of a common base or derived type as `expression`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e1f31-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="e1f31-108">Return Value</span></span>  
 <span data-ttu-id="e1f31-109">2 つのコレクションに共通の要素がある場合は`true` 、それ以外の場合は `false`。</span><span class="sxs-lookup"><span data-stu-id="e1f31-109">`true` if the two collections have common elements; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e1f31-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="e1f31-110">Remarks</span></span>  
 <span data-ttu-id="e1f31-111">機能的には、次と同等で重複が用意されています。</span><span class="sxs-lookup"><span data-stu-id="e1f31-111">OVERLAPS provides functionally equivalent to the following:</span></span>  
  
 `EXISTS ( expression INTERSECT expression )`  
  
 <span data-ttu-id="e1f31-112">OVERLAPS は、 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] の集合演算子の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="e1f31-112">OVERLAPS is one of the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span> <span data-ttu-id="e1f31-113">[!INCLUDE[esql](../../../../../../includes/esql-md.md)] のすべての集合演算子は左から右に評価されます。</span><span class="sxs-lookup"><span data-stu-id="e1f31-113">All [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators are evaluated from left to right.</span></span> <span data-ttu-id="e1f31-114">優先順位は、[!INCLUDE[esql](../../../../../../includes/esql-md.md)]集合演算子を参照してください[EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md)します。</span><span class="sxs-lookup"><span data-stu-id="e1f31-114">For precedence information for the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators, see [EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="e1f31-115">例</span><span class="sxs-lookup"><span data-stu-id="e1f31-115">Example</span></span>  
 <span data-ttu-id="e1f31-116">次の Entity SQL クエリでは、OVERLAPS 演算子を使用して、2 つのコレクションに共通の値が存在するかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="e1f31-116">The following Entity SQL query uses the OVERLAPS operator to determines whether two collections have a common value.</span></span> <span data-ttu-id="e1f31-117">このクエリは、AdventureWorks Sales Model に基づいています。</span><span class="sxs-lookup"><span data-stu-id="e1f31-117">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="e1f31-118">これをコンパイルして実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e1f31-118">To compile and run this, follow these steps:</span></span>  
  
1.  <span data-ttu-id="e1f31-119">」の手順に従って[方法。StructuralType 結果を返すクエリを実行](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)します。</span><span class="sxs-lookup"><span data-stu-id="e1f31-119">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="e1f31-120">次のクエリを引数として `ExecuteStructuralTypeQuery` メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="e1f31-120">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#OVERLAPS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#overlaps)]  
  
## <a name="see-also"></a><span data-ttu-id="e1f31-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1f31-121">See also</span></span>
- [<span data-ttu-id="e1f31-122">Entity SQL リファレンス</span><span class="sxs-lookup"><span data-stu-id="e1f31-122">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
