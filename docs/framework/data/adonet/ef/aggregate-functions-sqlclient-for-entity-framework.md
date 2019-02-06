---
title: 集計関数 (Entity Framework 用 SqlClient)
ms.date: 03/30/2017
ms.assetid: 03303f01-b591-4efc-9875-f9c608edff0b
ms.openlocfilehash: f2f2b557cd9f126ddd513a0f42d3ac95114c3822
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2019
ms.locfileid: "55758701"
---
# <a name="aggregate-functions-sqlclient-for-entity-framework"></a><span data-ttu-id="0703d-102">集計関数 (Entity Framework 用 SqlClient)</span><span class="sxs-lookup"><span data-stu-id="0703d-102">Aggregate Functions (SqlClient for Entity Framework)</span></span>
<span data-ttu-id="0703d-103">.NET Framework Data Provider for SQL Server (SqlClient) には、集計関数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="0703d-103">The .NET Framework Data Provider for SQL Server (SqlClient) provides aggregate functions.</span></span> <span data-ttu-id="0703d-104">集計関数は、一連の入力値に対して計算を実行し、値を返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-104">Aggregate functions perform calculations on a set of input values and return a value.</span></span> <span data-ttu-id="0703d-105">これらの関数は、SqlClient の SqlServer 名前空間に存在します。</span><span class="sxs-lookup"><span data-stu-id="0703d-105">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="0703d-106">Entity Framework は、プロバイダーの名前空間プロパティを使用することにより、型や関数など、特定のコンストラクターに対してこのプロバイダーによってどのプレフィックスが使用されているかを特定できます。</span><span class="sxs-lookup"><span data-stu-id="0703d-106">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.</span></span>  
  
 <span data-ttu-id="0703d-107">SqlClient の集計関数を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0703d-107">The following are the SqlClient aggregate functions.</span></span>  

## <a name="avgexpression"></a><span data-ttu-id="0703d-108">AVG(expression)</span><span class="sxs-lookup"><span data-stu-id="0703d-108">AVG(expression)</span></span>

<span data-ttu-id="0703d-109">コレクション内の値の平均値を返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-109">Returns the average of the values in a collection.</span></span> <span data-ttu-id="0703d-110">NULL 値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="0703d-110">Null values are ignored.</span></span>

<span data-ttu-id="0703d-111">**引数**</span><span class="sxs-lookup"><span data-stu-id="0703d-111">**Arguments**</span></span>

<span data-ttu-id="0703d-112">`Int32`、 `Int64`、 `Double`、および`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="0703d-112">An `Int32`, `Int64`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="0703d-113">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0703d-113">**Return Value**</span></span>

<span data-ttu-id="0703d-114">`expression` の型。</span><span class="sxs-lookup"><span data-stu-id="0703d-114">The type of `expression`.</span></span>

<span data-ttu-id="0703d-115">**例**</span><span class="sxs-lookup"><span data-stu-id="0703d-115">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_AVG](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_avg)]
 [!code-sql[DP EntityServices Concepts#SQLSERVER_AVG](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_avg)]

## <a name="checksumaggcollection"></a><span data-ttu-id="0703d-116">CHECKSUM_AGG(collection)</span><span class="sxs-lookup"><span data-stu-id="0703d-116">CHECKSUM_AGG(collection)</span></span>
 
 <span data-ttu-id="0703d-117">コレクション内にある値のチェックサムを返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-117">Returns the checksum of the values in a collection.</span></span> <span data-ttu-id="0703d-118">NULL 値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="0703d-118">Null values are ignored.</span></span>
 
 <span data-ttu-id="0703d-119">**引数**</span><span class="sxs-lookup"><span data-stu-id="0703d-119">**Arguments**</span></span>
 
 <span data-ttu-id="0703d-120">コレクション (`Int32`)。</span><span class="sxs-lookup"><span data-stu-id="0703d-120">A Collection(`Int32`).</span></span>
 
 <span data-ttu-id="0703d-121">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0703d-121">**Return Value**</span></span>
 
 <span data-ttu-id="0703d-122">`Int32`。</span><span class="sxs-lookup"><span data-stu-id="0703d-122">An `Int32`.</span></span>
 
 <span data-ttu-id="0703d-123">**例**</span><span class="sxs-lookup"><span data-stu-id="0703d-123">**Example**</span></span>
 
 [!code-csharp[DP EntityServices Concepts#SQLSERVER_CHECKSUM](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_checksum)]
 [!code-sql[DP EntityServices Concepts#SQLSERVER_CHECKSUM](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_checksum)]
   
## <a name="countexpression"></a><span data-ttu-id="0703d-124">COUNT(expression)</span><span class="sxs-lookup"><span data-stu-id="0703d-124">COUNT(expression)</span></span>

<span data-ttu-id="0703d-125">コレクション内のアイテムの数を `Int32` 型の値として返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-125">Returns the number of items in a collection as an `Int32`.</span></span>

<span data-ttu-id="0703d-126">**引数**</span><span class="sxs-lookup"><span data-stu-id="0703d-126">**Arguments**</span></span>

<span data-ttu-id="0703d-127">コレクション\<T >、T は、次の種類のいずれか。</span><span class="sxs-lookup"><span data-stu-id="0703d-127">A Collection\<T>, where T is one of the following types:</span></span>

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`|<span data-ttu-id="0703d-128">`Guid` (SQL Server 2000 では返されません)</span><span class="sxs-lookup"><span data-stu-id="0703d-128">`Guid` (not returned in SQL Server 2000)</span></span>|

<span data-ttu-id="0703d-129">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0703d-129">**Return Value**</span></span>

<span data-ttu-id="0703d-130">`Int32`。</span><span class="sxs-lookup"><span data-stu-id="0703d-130">An `Int32`.</span></span>

<span data-ttu-id="0703d-131">**例**</span><span class="sxs-lookup"><span data-stu-id="0703d-131">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_COUNT](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_count)]
<span data-ttu-id="0703d-132">[! コード sql[DP EntityServices 概念 #SQLSERVER_COUNT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_count)</span><span class="sxs-lookup"><span data-stu-id="0703d-132">[!code-sql[DP EntityServices Concepts#SQLSERVER_COUNT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_count)</span></span>
 
## <a name="countbigexpression"></a><span data-ttu-id="0703d-133">COUNT_BIG(expression)</span><span class="sxs-lookup"><span data-stu-id="0703d-133">COUNT_BIG(expression)</span></span>
 
 <span data-ttu-id="0703d-134">コレクション内のアイテムの数を `bigint` 型の値として返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-134">Returns the number of items in a collection as a `bigint`.</span></span>
 
 <span data-ttu-id="0703d-135">**引数**</span><span class="sxs-lookup"><span data-stu-id="0703d-135">**Arguments**</span></span>
 
 <span data-ttu-id="0703d-136">T は、次の種類のいずれかの Collection(T):</span><span class="sxs-lookup"><span data-stu-id="0703d-136">A Collection(T), where T is one of the following types:</span></span>
 
 |   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`|<span data-ttu-id="0703d-137">`Guid` (SQL Server 2000 では返されません)</span><span class="sxs-lookup"><span data-stu-id="0703d-137">`Guid` (not returned in SQL Server 2000)</span></span>|

<span data-ttu-id="0703d-138">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0703d-138">**Return Value**</span></span>

<span data-ttu-id="0703d-139">`Int64`。</span><span class="sxs-lookup"><span data-stu-id="0703d-139">An `Int64`.</span></span>

<span data-ttu-id="0703d-140">**例**</span><span class="sxs-lookup"><span data-stu-id="0703d-140">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_COUNTBIG](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_countbig)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_COUNTBIG](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_countbig)]

## <a name="maxexpression"></a><span data-ttu-id="0703d-141">MAX(expression)</span><span class="sxs-lookup"><span data-stu-id="0703d-141">MAX(expression)</span></span>

<span data-ttu-id="0703d-142">コレクション内の最大値を返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-142">Returns the maximum value the collection.</span></span>

<span data-ttu-id="0703d-143">**引数**</span><span class="sxs-lookup"><span data-stu-id="0703d-143">**Arguments**</span></span>

<span data-ttu-id="0703d-144">T は、次の種類のいずれかの Collection(T):</span><span class="sxs-lookup"><span data-stu-id="0703d-144">A Collection(T), where T is one of the following types:</span></span> 

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`||

<span data-ttu-id="0703d-145">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0703d-145">**Return Value**</span></span>

<span data-ttu-id="0703d-146">`expression` の型。</span><span class="sxs-lookup"><span data-stu-id="0703d-146">The type of `expression`.</span></span>

<span data-ttu-id="0703d-147">**例**</span><span class="sxs-lookup"><span data-stu-id="0703d-147">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_MAX](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_max)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_MAX](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_max)]

## <a name="minexpression"></a><span data-ttu-id="0703d-148">MIN(expression)</span><span class="sxs-lookup"><span data-stu-id="0703d-148">MIN(expression)</span></span>

<span data-ttu-id="0703d-149">コレクション内の最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-149">Returns the minimum value in a collection.</span></span>

<span data-ttu-id="0703d-150">**引数**</span><span class="sxs-lookup"><span data-stu-id="0703d-150">**Arguments**</span></span>

<span data-ttu-id="0703d-151">T は、次の種類のいずれかの Collection(T):</span><span class="sxs-lookup"><span data-stu-id="0703d-151">A Collection(T), where T is one of the following types:</span></span> 

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`||

<span data-ttu-id="0703d-152">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0703d-152">**Return Value**</span></span>

<span data-ttu-id="0703d-153">`expression` の型。</span><span class="sxs-lookup"><span data-stu-id="0703d-153">The type of `expression`.</span></span>

<span data-ttu-id="0703d-154">**例**</span><span class="sxs-lookup"><span data-stu-id="0703d-154">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_MIN](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_min)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_MIN](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_min)]

## <a name="stdevexpression"></a><span data-ttu-id="0703d-155">STDEV(expression)</span><span class="sxs-lookup"><span data-stu-id="0703d-155">STDEV(expression)</span></span>

<span data-ttu-id="0703d-156">指定された式のすべての値の統計的標準偏差を返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-156">Returns the statistical standard deviation of all values in the specified expression.</span></span>

<span data-ttu-id="0703d-157">**引数**</span><span class="sxs-lookup"><span data-stu-id="0703d-157">**Arguments**</span></span>

<span data-ttu-id="0703d-158">コレクション (`Double`)。</span><span class="sxs-lookup"><span data-stu-id="0703d-158">A Collection(`Double`).</span></span>

<span data-ttu-id="0703d-159">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0703d-159">**Return Value**</span></span>

<span data-ttu-id="0703d-160">`Double`。</span><span class="sxs-lookup"><span data-stu-id="0703d-160">A `Double`.</span></span>

<span data-ttu-id="0703d-161">**例**</span><span class="sxs-lookup"><span data-stu-id="0703d-161">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_STDEV](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_stdev)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_STDEV](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_stdev)]

## <a name="stdevpexpression"></a><span data-ttu-id="0703d-162">STDEVP(expression)</span><span class="sxs-lookup"><span data-stu-id="0703d-162">STDEVP(expression)</span></span>

<span data-ttu-id="0703d-163">指定された式のすべての値を母集団として統計的標準偏差を返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-163">Returns the statistical standard deviation for the population for all values in the specified expression.</span></span>

<span data-ttu-id="0703d-164">**引数**</span><span class="sxs-lookup"><span data-stu-id="0703d-164">**Arguments**</span></span>

<span data-ttu-id="0703d-165">コレクション (`Double`)。</span><span class="sxs-lookup"><span data-stu-id="0703d-165">A Collection(`Double`).</span></span>

<span data-ttu-id="0703d-166">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0703d-166">**Return Value**</span></span>

<span data-ttu-id="0703d-167">`Double`。</span><span class="sxs-lookup"><span data-stu-id="0703d-167">A `Double`.</span></span>

<span data-ttu-id="0703d-168">**例**</span><span class="sxs-lookup"><span data-stu-id="0703d-168">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_STDEVP](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_stdevp)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_STDEVP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_stdevp)]

## <a name="sumexpression"></a><span data-ttu-id="0703d-169">SUM(expression)</span><span class="sxs-lookup"><span data-stu-id="0703d-169">SUM(expression)</span></span>

<span data-ttu-id="0703d-170">コレクション内のすべての値の合計を返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-170">Returns the sum of all the values in the collection.</span></span>

<span data-ttu-id="0703d-171">**引数**</span><span class="sxs-lookup"><span data-stu-id="0703d-171">**Arguments**</span></span>

<span data-ttu-id="0703d-172">T は、次の種類のいずれかの Collection(T): `Int32`、 `Int64`、 `Double`、`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="0703d-172">A Collection(T) where T is one of the following types: `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="0703d-173">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0703d-173">**Return Value**</span></span>

<span data-ttu-id="0703d-174">`expression` の型。</span><span class="sxs-lookup"><span data-stu-id="0703d-174">The type of `expression`.</span></span>

<span data-ttu-id="0703d-175">**例**</span><span class="sxs-lookup"><span data-stu-id="0703d-175">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_SUM](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_sum)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_SUM](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_sum)]

## <a name="varexpression"></a><span data-ttu-id="0703d-176">VAR(expression)</span><span class="sxs-lookup"><span data-stu-id="0703d-176">VAR(expression)</span></span>

<span data-ttu-id="0703d-177">指定された式のすべての値の統計的分散を返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-177">Returns the statistical variance of all values in the specified expression.</span></span>

<span data-ttu-id="0703d-178">**引数**</span><span class="sxs-lookup"><span data-stu-id="0703d-178">**Arguments**</span></span>

<span data-ttu-id="0703d-179">コレクション (`Double`)。</span><span class="sxs-lookup"><span data-stu-id="0703d-179">A Collection(`Double`).</span></span>

<span data-ttu-id="0703d-180">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0703d-180">**Return Value**</span></span>

<span data-ttu-id="0703d-181">`Double`。</span><span class="sxs-lookup"><span data-stu-id="0703d-181">A `Double`.</span></span>

<span data-ttu-id="0703d-182">**例**</span><span class="sxs-lookup"><span data-stu-id="0703d-182">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_VAR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_var)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_VAR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_var)]

## <a name="varpexpression"></a><span data-ttu-id="0703d-183">VARP(expression)</span><span class="sxs-lookup"><span data-stu-id="0703d-183">VARP(expression)</span></span>

<span data-ttu-id="0703d-184">指定した式のすべての値について、母集団に対する統計的変位を返します。</span><span class="sxs-lookup"><span data-stu-id="0703d-184">Returns the statistical variance for the population for all values in the specified expression.</span></span>

<span data-ttu-id="0703d-185">**引数**</span><span class="sxs-lookup"><span data-stu-id="0703d-185">**Arguments**</span></span>

<span data-ttu-id="0703d-186">コレクション (`Double`)。</span><span class="sxs-lookup"><span data-stu-id="0703d-186">A Collection(`Double`).</span></span>

<span data-ttu-id="0703d-187">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0703d-187">**Return Value**</span></span>

<span data-ttu-id="0703d-188">`Double`。</span><span class="sxs-lookup"><span data-stu-id="0703d-188">A `Double`.</span></span>

<span data-ttu-id="0703d-189">**例**</span><span class="sxs-lookup"><span data-stu-id="0703d-189">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_VARP](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_varp)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_VARP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_varp)] 
  
## <a name="see-also"></a><span data-ttu-id="0703d-190">関連項目</span><span class="sxs-lookup"><span data-stu-id="0703d-190">See also</span></span>

<span data-ttu-id="0703d-191">SqlClient でサポートされる集計関数の詳細については、SqlClient プロバイダー マニフェストで指定した SQL Server のバージョンのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0703d-191">For more information about the aggregate functions that SqlClient supports, see the documentation for the SQL Server version that you specified in the SqlClient provider manifest:</span></span>

- <span data-ttu-id="0703d-192">**SQL Server 2005:**[集計関数 (TRANSACT-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms173454(v=sql.90))</span><span class="sxs-lookup"><span data-stu-id="0703d-192">**SQL Server 2005:** [Aggregate Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms173454(v=sql.90))</span></span>
- <span data-ttu-id="0703d-193">**SQL Server 2008 以降:**[集計関数 (TRANSACT-SQL)](/sql/t-sql/functions/aggregate-functions-transact-sql)</span><span class="sxs-lookup"><span data-stu-id="0703d-193">**SQL Server 2008 and later:** [Aggregate Functions (Transact-SQL)](/sql/t-sql/functions/aggregate-functions-transact-sql)</span></span>

- [<span data-ttu-id="0703d-194">Entity SQL 言語</span><span class="sxs-lookup"><span data-stu-id="0703d-194">Entity SQL Language</span></span>](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md)
- [<span data-ttu-id="0703d-195">集計正規関数</span><span class="sxs-lookup"><span data-stu-id="0703d-195">Aggregate Canonical Functions</span></span>](../../../../../docs/framework/data/adonet/ef/language-reference/aggregate-canonical-functions.md)
