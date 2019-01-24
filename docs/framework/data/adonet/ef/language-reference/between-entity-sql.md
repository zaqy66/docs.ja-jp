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
# <a name="between-entity-sql"></a><span data-ttu-id="55dcb-102">BETWEEN (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="55dcb-102">BETWEEN (Entity SQL)</span></span>
<span data-ttu-id="55dcb-103">式の結果が指定の範囲内の値になるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="55dcb-103">Determines whether an expression results in a value in a specified range.</span></span> <span data-ttu-id="55dcb-104">[!INCLUDE[esql](../../../../../../includes/esql-md.md)] BETWEEN 式が TRANSACT-SQL の BETWEEN 式と同じ機能です。</span><span class="sxs-lookup"><span data-stu-id="55dcb-104">The [!INCLUDE[esql](../../../../../../includes/esql-md.md)] BETWEEN expression has the same functionality as the Transact-SQL BETWEEN expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55dcb-105">構文</span><span class="sxs-lookup"><span data-stu-id="55dcb-105">Syntax</span></span>  
  
```  
expression [ NOT ] BETWEEN begin_expression AND end_expression    
```  
  
## <a name="arguments"></a><span data-ttu-id="55dcb-106">引数</span><span class="sxs-lookup"><span data-stu-id="55dcb-106">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="55dcb-107">`begin_expression` と `end_expression` で定義される範囲についてテストするための任意の有効な式。</span><span class="sxs-lookup"><span data-stu-id="55dcb-107">Any valid expression to test for in the range defined by `begin_expression` and `end_expression`.</span></span> <span data-ttu-id="55dcb-108">`expression` は、`begin_expression` と `end_expression` の両方と同じ型にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="55dcb-108">`expression` must be the same type as both `begin_expression` and `end_expression`.</span></span>  
  
 `begin_expression`  
 <span data-ttu-id="55dcb-109">任意の有効な式。</span><span class="sxs-lookup"><span data-stu-id="55dcb-109">Any valid expression.</span></span> <span data-ttu-id="55dcb-110">`begin_expression` は、`expression` と `end_expression` の両方と同じ型にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="55dcb-110">`begin_expression` must be the same type as both `expression` and `end_expression`.</span></span> <span data-ttu-id="55dcb-111">`begin_expression` は、`end_expression` 未満でなければなりません。それ以外の場合、戻り値は否定されます。</span><span class="sxs-lookup"><span data-stu-id="55dcb-111">`begin_expression` should be less than `end_expression`, else the return value will be negated.</span></span>  
  
 `end_expression`  
 <span data-ttu-id="55dcb-112">任意の有効な式。</span><span class="sxs-lookup"><span data-stu-id="55dcb-112">Any valid expression.</span></span> <span data-ttu-id="55dcb-113">`end_expression` は、`expression` と `begin_expression` の両方と同じ型にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="55dcb-113">`end_expression` must be the same type as both `expression` and `begin_expression`.</span></span>  
  
 <span data-ttu-id="55dcb-114">NOT</span><span class="sxs-lookup"><span data-stu-id="55dcb-114">NOT</span></span>  
 <span data-ttu-id="55dcb-115">BETWEEN の結果を否定することを指定します。</span><span class="sxs-lookup"><span data-stu-id="55dcb-115">Specifies that the result of BETWEEN be negated.</span></span>  
  
 <span data-ttu-id="55dcb-116">AND</span><span class="sxs-lookup"><span data-stu-id="55dcb-116">AND</span></span>  
 <span data-ttu-id="55dcb-117">`expression` と `begin_expression` で表される範囲内で `end_expression` をテストする必要があることを示すプレースホルダーです。</span><span class="sxs-lookup"><span data-stu-id="55dcb-117">Acts as a placeholder that indicates `expression` should be within the range indicated by `begin_expression` and `end_expression`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="55dcb-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="55dcb-118">Return Value</span></span>  
 <span data-ttu-id="55dcb-119">`true` が、`expression` と `begin_expression` で指定される範囲内にある場合は `end_expression`。それ以外の場合は `false`。</span><span class="sxs-lookup"><span data-stu-id="55dcb-119">`true` if `expression` is between the range indicated by `begin_expression` and `end_expression`; otherwise, `false`.</span></span> <span data-ttu-id="55dcb-120">`null` が `expression` であるか、`null` または `begin_expression` が `end_expression` である場合は、`null` が返されます。</span><span class="sxs-lookup"><span data-stu-id="55dcb-120">`null` will be returned if `expression` is `null` or if `begin_expression` or `end_expression` is `null`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="55dcb-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="55dcb-121">Remarks</span></span>  
 <span data-ttu-id="55dcb-122">両端を除いた範囲を指定するには、BETWEEN の代わりに、より大きい (>) とより小さい (<) を意味する演算子を使用します。</span><span class="sxs-lookup"><span data-stu-id="55dcb-122">To specify an exclusive range, use the greater than (>) and less than (<) operators instead of BETWEEN.</span></span>  
  
## <a name="example"></a><span data-ttu-id="55dcb-123">例</span><span class="sxs-lookup"><span data-stu-id="55dcb-123">Example</span></span>  
 <span data-ttu-id="55dcb-124">次の Entity SQL クエリでは、BETWEEN 演算子を使用して、式の結果が指定の範囲内の値になるかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="55dcb-124">The following Entity SQL query uses BETWEEN operator to determine whether an expression results in a value in a specified range.</span></span> <span data-ttu-id="55dcb-125">このクエリは、AdventureWorks Sales Model に基づいています。</span><span class="sxs-lookup"><span data-stu-id="55dcb-125">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="55dcb-126">このクエリをコンパイルして実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="55dcb-126">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="55dcb-127">」の手順に従って[方法。StructuralType 結果を返すクエリを実行](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)します。</span><span class="sxs-lookup"><span data-stu-id="55dcb-127">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="55dcb-128">次のクエリを引数として `ExecuteStructuralTypeQuery` メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="55dcb-128">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#BETWEEN](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#between)]  
  
## <a name="see-also"></a><span data-ttu-id="55dcb-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="55dcb-129">See also</span></span>
- [<span data-ttu-id="55dcb-130">Entity SQL リファレンス</span><span class="sxs-lookup"><span data-stu-id="55dcb-130">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
