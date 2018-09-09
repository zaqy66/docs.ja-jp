---
title: 数学関数
ms.date: 03/30/2017
ms.assetid: b040c7cb-156d-40f2-9152-61065b18148c
ms.openlocfilehash: e6c58d781d7138f8295f2d0a2f0db110ad4b1dd6
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44225244"
---
# <a name="mathematical-functions"></a><span data-ttu-id="8c969-102">数学関数</span><span class="sxs-lookup"><span data-stu-id="8c969-102">Mathematical Functions</span></span>

<span data-ttu-id="8c969-103">.NET Framework Data Provider for SQL Server (SqlClient) には、引数として指定された入力値に対して計算を実行し、数値結果を返す数学関数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="8c969-103">The .NET Framework Data Provider for SQL Server (SqlClient) provides math functions that perform calculations on input values that are provided as arguments, and return a numeric value result.</span></span> <span data-ttu-id="8c969-104">これらの関数は、SqlClient の SqlServer 名前空間に存在します。</span><span class="sxs-lookup"><span data-stu-id="8c969-104">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="8c969-105">Entity Framework は、プロバイダーの名前空間プロパティを使用することにより、型や関数など、特定のコンストラクターに対してこのプロバイダーによってどのプレフィックスが使用されているかを特定できます。次の表に、SqlClient の数学関数を示します。</span><span class="sxs-lookup"><span data-stu-id="8c969-105">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.The following table describes the SqlClient math functions.</span></span>  
  
## <a name="absexpression"></a><span data-ttu-id="8c969-106">ABS(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-106">ABS(expression)</span></span>

<span data-ttu-id="8c969-107">絶対値を求める関数です。</span><span class="sxs-lookup"><span data-stu-id="8c969-107">Performs the absolute value function.</span></span>

<span data-ttu-id="8c969-108">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-108">**Arguments**</span></span>

<span data-ttu-id="8c969-109">`expression`: `Int32`、`Int64`、`Double`、または `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="8c969-109">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="8c969-110">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-110">**Return Value**</span></span>

<span data-ttu-id="8c969-111">指定された式の絶対値。</span><span class="sxs-lookup"><span data-stu-id="8c969-111">The absolute value of the specified expression.</span></span>

<span data-ttu-id="8c969-112">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-112">**Example**</span></span>

`SqlServer.ABS(-2)`

## <a name="acosexpression"></a><span data-ttu-id="8c969-113">ACOS(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-113">ACOS(expression)</span></span>

<span data-ttu-id="8c969-114">指定された式のアークコサイン (逆余弦) 値を返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-114">Returns the arccosine value of the specified expression.</span></span>

<span data-ttu-id="8c969-115">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-115">**Arguments**</span></span>

<span data-ttu-id="8c969-116">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-116">`expression`: A `Double`.</span></span>

<span data-ttu-id="8c969-117">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-117">**Return Value**</span></span>

<span data-ttu-id="8c969-118">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-118">A `Double`.</span></span>

<span data-ttu-id="8c969-119">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-119">**Example**</span></span>

`SqlServer.ACOS(.9)`

## <a name="asinexpression"></a><span data-ttu-id="8c969-120">ASIN(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-120">ASIN(expression)</span></span>

<span data-ttu-id="8c969-121">指定された式のアークサイン (逆正弦) 値を返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-121">Returns the arcsine value of the specified expression.</span></span>

<span data-ttu-id="8c969-122">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-122">**Arguments**</span></span>

<span data-ttu-id="8c969-123">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-123">`expression`: A `Double`.</span></span>

<span data-ttu-id="8c969-124">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-124">**Return Value**</span></span>

<span data-ttu-id="8c969-125">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-125">A `Double`.</span></span>

<span data-ttu-id="8c969-126">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-126">**Example**</span></span>

`SqlServer.ASIN(.9)`

## <a name="atanexpression"></a><span data-ttu-id="8c969-127">ATAN(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-127">ATAN(expression)</span></span>

<span data-ttu-id="8c969-128">指定された数値式のアークタンジェント (逆正接) 値を返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-128">Returns the arctangent value of the specified numeric expression.</span></span>

<span data-ttu-id="8c969-129">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-129">**Arguments**</span></span>

<span data-ttu-id="8c969-130">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-130">`expression`: A `Double`.</span></span>

<span data-ttu-id="8c969-131">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-131">**Return Value**</span></span>

<span data-ttu-id="8c969-132">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-132">A `Double`.</span></span>

<span data-ttu-id="8c969-133">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-133">**Example**</span></span>

`SqlServer.ATAN(9)`

## <a name="atn2expression-expression"></a><span data-ttu-id="8c969-134">ATN2(expression, expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-134">ATN2(expression, expression)</span></span>

<span data-ttu-id="8c969-135">指定された 2 つの数値式の商がタンジェント (正接) となる角度をラジアンで返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-135">Returns the angle, in radians, whose tangent is between the two specified numeric expressions.</span></span>

<span data-ttu-id="8c969-136">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-136">**Arguments**</span></span>

<span data-ttu-id="8c969-137">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-137">`expression`: A `Double`.</span></span>

<span data-ttu-id="8c969-138">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-138">**Return Value**</span></span>

<span data-ttu-id="8c969-139">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-139">A `Double`.</span></span>

<span data-ttu-id="8c969-140">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-140">**Example**</span></span>

`SqlServer.ATN2(9, 8)`
 
## <a name="ceilingexpression"></a><span data-ttu-id="8c969-141">CEILING(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-141">CEILING(expression)</span></span>

<span data-ttu-id="8c969-142">指定された式をその式以上の最小整数に変換します。</span><span class="sxs-lookup"><span data-stu-id="8c969-142">Converts the specified expression to the smallest integer that is greater than or equal to it.</span></span>

<span data-ttu-id="8c969-143">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-143">**Arguments**</span></span>

<span data-ttu-id="8c969-144">`expression`: `Int32`、`Int64`、`Double`、または `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="8c969-144">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="8c969-145">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-145">**Return Value**</span></span>

<span data-ttu-id="8c969-146">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="8c969-146">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="8c969-147">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-147">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_ceiling)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_ceiling)]

## <a name="cosexpression"></a><span data-ttu-id="8c969-148">COS(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-148">COS(expression)</span></span>

<span data-ttu-id="8c969-149">ラジアンで指定された角度のコサイン (余弦) を計算します。</span><span class="sxs-lookup"><span data-stu-id="8c969-149">Calculates the trigonometric cosine of the specified angle in radians.</span></span> 

<span data-ttu-id="8c969-150">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-150">**Arguments**</span></span> 

<span data-ttu-id="8c969-151">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-151">`expression`: A `Double`.</span></span> 

<span data-ttu-id="8c969-152">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-152">**Return Value**</span></span> 

<span data-ttu-id="8c969-153">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-153">A `Double`.</span></span> 

<span data-ttu-id="8c969-154">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-154">**Example**</span></span> 

`SqlServer.COS(45)`

## <a name="cotexpression"></a><span data-ttu-id="8c969-155">COT(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-155">COT(expression)</span></span>

<span data-ttu-id="8c969-156">ラジアンで指定された角度のコタンジェント (余接) を計算します。</span><span class="sxs-lookup"><span data-stu-id="8c969-156">Calculates the trigonometric cotangent of the specified angle in radians.</span></span> 

<span data-ttu-id="8c969-157">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-157">**Arguments**</span></span> 

<span data-ttu-id="8c969-158">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-158">`expression`: A `Double`.</span></span> 

<span data-ttu-id="8c969-159">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-159">**Return Value**</span></span> 

<span data-ttu-id="8c969-160">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-160">A `Double`.</span></span> 

<span data-ttu-id="8c969-161">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-161">**Example**</span></span> 

`SqlServer.COT(60)`
  
## <a name="degreesradians"></a><span data-ttu-id="8c969-162">DEGREES(radians)</span><span class="sxs-lookup"><span data-stu-id="8c969-162">DEGREES(radians)</span></span>

<span data-ttu-id="8c969-163">対応する角度を度数で返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-163">Returns the corresponding angle in degrees.</span></span> 

<span data-ttu-id="8c969-164">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-164">**Arguments**</span></span> 

<span data-ttu-id="8c969-165">`expression`: `Int32`、`Int64`、`Double`、または `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="8c969-165">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="8c969-166">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-166">**Return Value**</span></span> 

<span data-ttu-id="8c969-167">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="8c969-167">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="8c969-168">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-168">**Example**</span></span> 

`SqlServer.DEGREES(3.1)`

## <a name="expexpression"></a><span data-ttu-id="8c969-169">EXP(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-169">EXP(expression)</span></span>

<span data-ttu-id="8c969-170">指定された数値式の指数値を計算します。</span><span class="sxs-lookup"><span data-stu-id="8c969-170">Calculates the exponential value of a specified numeric expression.</span></span> 

<span data-ttu-id="8c969-171">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-171">**Arguments**</span></span> 

<span data-ttu-id="8c969-172">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-172">`expression`: A `Double`.</span></span> 

<span data-ttu-id="8c969-173">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-173">**Return Value**</span></span> 

<span data-ttu-id="8c969-174">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-174">A `Double`.</span></span> 

<span data-ttu-id="8c969-175">**例** `SqlServer.EXP(1)`</span><span class="sxs-lookup"><span data-stu-id="8c969-175">**Example** `SqlServer.EXP(1)`</span></span>

## <a name="floorexpression"></a><span data-ttu-id="8c969-176">FLOOR(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-176">FLOOR(expression)</span></span>

<span data-ttu-id="8c969-177">指定された式をその式以下の最大整数に変換します。</span><span class="sxs-lookup"><span data-stu-id="8c969-177">Converts the specified expression to the largest integer less than or equal to it.</span></span> 

<span data-ttu-id="8c969-178">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-178">**Arguments**</span></span> 

<span data-ttu-id="8c969-179">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-179">`expression`: A `Double`.</span></span> 

<span data-ttu-id="8c969-180">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-180">**Return Value**</span></span> 

<span data-ttu-id="8c969-181">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-181">A `Double`.</span></span> 

<span data-ttu-id="8c969-182">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-182">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_floor)] 
[!code-sql[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_floor)]

## <a name="logexpression"></a><span data-ttu-id="8c969-183">LOG(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-183">LOG(expression)</span></span>

<span data-ttu-id="8c969-184">指定された `float` 型の式の自然対数を計算します。</span><span class="sxs-lookup"><span data-stu-id="8c969-184">Calculates the natural logarithm of the specified `float` expression.</span></span> 

<span data-ttu-id="8c969-185">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-185">**Arguments**</span></span> 

<span data-ttu-id="8c969-186">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-186">`expression`: A `Double`.</span></span> 

<span data-ttu-id="8c969-187">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-187">**Return Value**</span></span> 

<span data-ttu-id="8c969-188">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-188">A `Double`.</span></span> 

<span data-ttu-id="8c969-189">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-189">**Example**</span></span> 

`SqlServer.LOG(100)`

## <a name="log10expression"></a><span data-ttu-id="8c969-190">LOG10(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-190">LOG10(expression)</span></span>

<span data-ttu-id="8c969-191">指定された `Double` 型の式の 10 を底とした対数を返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-191">Returns the base-10 logarithm of the specified `Double` expression.</span></span> 

<span data-ttu-id="8c969-192">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-192">**Arguments**</span></span> 

<span data-ttu-id="8c969-193">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-193">`expression`: A `Double`.</span></span> 

<span data-ttu-id="8c969-194">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-194">**Return Value**</span></span> 

<span data-ttu-id="8c969-195">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-195">A `Double`.</span></span> 

<span data-ttu-id="8c969-196">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-196">**Example**</span></span> 

`SqlServer.LOG10(100)`

## <a name="pi"></a><span data-ttu-id="8c969-197">PI()」と指定</span><span class="sxs-lookup"><span data-stu-id="8c969-197">PI()</span></span>

<span data-ttu-id="8c969-198">π の定数値を `Double` として返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-198">Returns the constant value of pi as a `Double`.</span></span> 

<span data-ttu-id="8c969-199">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-199">**Return Value**</span></span> 

<span data-ttu-id="8c969-200">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-200">A `Double`.</span></span> 

<span data-ttu-id="8c969-201">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-201">**Example**</span></span> 

`SqlServer.PI()`

## <a name="powernumericexpression-powerexpression"></a><span data-ttu-id="8c969-202">電源 (numeric_expression、power_expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-202">POWER(numeric_expression, power_expression)</span></span>

<span data-ttu-id="8c969-203">指定された式の指定されたべき乗を計算します。</span><span class="sxs-lookup"><span data-stu-id="8c969-203">Calculates the value of a specified expression to a specified power.</span></span>

<span data-ttu-id="8c969-204">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-204">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="8c969-205">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="8c969-205">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>|
|`power_expression`| <span data-ttu-id="8c969-206">A`Double`のべき乗値を表す、`numeric_expression`します。</span><span class="sxs-lookup"><span data-stu-id="8c969-206">A `Double` that represents the power to which to raise the `numeric_expression`.</span></span>| 

<span data-ttu-id="8c969-207">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-207">**Return Value**</span></span> 

<span data-ttu-id="8c969-208">指定された `numeric_expression` を指定された `power_expression` でべき乗した値。</span><span class="sxs-lookup"><span data-stu-id="8c969-208">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span> 

<span data-ttu-id="8c969-209">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-209">**Example**</span></span> 

`SqlServer.POWER(2,7)`

## <a name="radiansexpression"></a><span data-ttu-id="8c969-210">RADIANS(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-210">RADIANS(expression)</span></span>

<span data-ttu-id="8c969-211">角度をラジアンに変換します。</span><span class="sxs-lookup"><span data-stu-id="8c969-211">Converts degrees to radians.</span></span> 

<span data-ttu-id="8c969-212">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-212">**Arguments**</span></span> 

<span data-ttu-id="8c969-213">`expression`: `Int32`、`Int64`、`Double`、または `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="8c969-213">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="8c969-214">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-214">**Return Value**</span></span> 

<span data-ttu-id="8c969-215">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="8c969-215">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="8c969-216">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-216">**Example**</span></span> 

`SqlServer.RADIANS(360.0)`

## <a name="randseed"></a><span data-ttu-id="8c969-217">RAND([seed])</span><span class="sxs-lookup"><span data-stu-id="8c969-217">RAND([seed])</span></span>

<span data-ttu-id="8c969-218">0 から 1 までの範囲の乱数を返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-218">Returns a random value from 0 through 1.</span></span> 

<span data-ttu-id="8c969-219">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-219">**Arguments**</span></span> 

<span data-ttu-id="8c969-220">シード値として、`Int32`します。</span><span class="sxs-lookup"><span data-stu-id="8c969-220">The seed value as an `Int32`.</span></span> <span data-ttu-id="8c969-221">シードを指定しない場合は、SQL Server データベース エンジンによってシード値がランダムに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="8c969-221">If the seed is not specified, the SQL Server Database Engine assigns a seed value at random.</span></span> <span data-ttu-id="8c969-222">指定したシード値について、返される結果は常に同じです。</span><span class="sxs-lookup"><span data-stu-id="8c969-222">For a specified seed value, the result returned is always the same.</span></span>

<span data-ttu-id="8c969-223">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-223">**Return Value**</span></span> 

<span data-ttu-id="8c969-224">0 から 1 までの範囲の `Double` 型の乱数。</span><span class="sxs-lookup"><span data-stu-id="8c969-224">A random `Double` value from 0 through 1.</span></span> 

<span data-ttu-id="8c969-225">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-225">**Example**</span></span> 

`SqlServer.RAND()`
  
## <a name="roundnumericexpression-lengthfunction"></a><span data-ttu-id="8c969-226">ROUND(numeric_expression, length[,function])</span><span class="sxs-lookup"><span data-stu-id="8c969-226">ROUND(numeric_expression, length[,function])</span></span>

<span data-ttu-id="8c969-227">指定された長さまたは有効桁数に丸めた数値式を返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-227">Returns a numeric expression, rounded to the specified length or precision.</span></span> 

<span data-ttu-id="8c969-228">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-228">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="8c969-229">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="8c969-229">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 
|`length`| <span data-ttu-id="8c969-230">`Int32` を丸めた後の有効桁数を表す `numeric_expression`。</span><span class="sxs-lookup"><span data-stu-id="8c969-230">An `Int32` that represents the precision to which `numeric_expression` is to be rounded.</span></span> <span data-ttu-id="8c969-231">`length` に正の値を指定した場合、`numeric_expression` は `length` で指定した小数点以下桁数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="8c969-231">When `length` is a positive number, `numeric_expression` is rounded to the number of decimal positions specified by `length`.</span></span> <span data-ttu-id="8c969-232">`length` に負の値を指定した場合、`numeric_expression` は `length` で指定した小数点の左側の位置で丸められます。</span><span class="sxs-lookup"><span data-stu-id="8c969-232">When `length` is a negative number, `numeric_expression` is rounded on the left side of the decimal point, as specified by `length`.</span></span>|
|`function` | <span data-ttu-id="8c969-233">任意。</span><span class="sxs-lookup"><span data-stu-id="8c969-233">Optional.</span></span> <span data-ttu-id="8c969-234">`Int32`を実行する操作の種類を表します。</span><span class="sxs-lookup"><span data-stu-id="8c969-234">An `Int32` that represents the type of operation to perform.</span></span> <span data-ttu-id="8c969-235">関数を省略するか 0 (既定値) の値を持つとき`numeric_expression`は丸められます。</span><span class="sxs-lookup"><span data-stu-id="8c969-235">When function is omitted or has a value of 0 (default), `numeric_expression` is rounded.</span></span> <span data-ttu-id="8c969-236">以外の値は 0 を指定した、`numeric_expression`は切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="8c969-236">When a value other than 0 is specified, `numeric_expression` is truncated.</span></span> |

<span data-ttu-id="8c969-237">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-237">**Return Value**</span></span> 

<span data-ttu-id="8c969-238">指定された `numeric_expression` を指定された `power_expression` でべき乗した値。</span><span class="sxs-lookup"><span data-stu-id="8c969-238">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span>

<span data-ttu-id="8c969-239">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-239">**Example**</span></span> 

`SqlServer.ROUND(748.58, -3)`

## <a name="signexpression"></a><span data-ttu-id="8c969-240">SIGN(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-240">SIGN(expression)</span></span> 

<span data-ttu-id="8c969-241">指定した式の符号として、正 (+1)、負 (-1)、ゼロ (0) のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-241">Returns the positive (+1), zero (0), or negative (-1) sign of the specified expression.</span></span> 

<span data-ttu-id="8c969-242">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-242">**Arguments**</span></span> 

<span data-ttu-id="8c969-243">`expression`: `Int32`、`Int64`、`Double`、または `Decimal`</span><span class="sxs-lookup"><span data-stu-id="8c969-243">`expression`: `Int32`, `Int64`, `Double`, or `Decimal`</span></span> 

<span data-ttu-id="8c969-244">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-244">**Return Value**</span></span> 

<span data-ttu-id="8c969-245">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="8c969-245">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="8c969-246">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-246">**Example**</span></span> 

`SqlServer.SIGN(-10)`

## <a name="sinexpression"></a><span data-ttu-id="8c969-247">SIN(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-247">SIN(expression)</span></span>

<span data-ttu-id="8c969-248">ラジアンで指定された角度のサイン (正弦) を計算し、`Double` 式を返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-248">Calculates the trigonometric sine of the specified angle in radians, and returns a `Double` expression.</span></span> 

<span data-ttu-id="8c969-249">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-249">**Arguments**</span></span> 

<span data-ttu-id="8c969-250">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-250">`expression`: A `Double`.</span></span> 

<span data-ttu-id="8c969-251">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-251">**Return Value**</span></span> 

<span data-ttu-id="8c969-252">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-252">A `Double`.</span></span> 

<span data-ttu-id="8c969-253">**例** `SqlServer.SIN(20)`</span><span class="sxs-lookup"><span data-stu-id="8c969-253">**Example** `SqlServer.SIN(20)`</span></span>

## <a name="sqrtexpression"></a><span data-ttu-id="8c969-254">SQRT(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-254">SQRT(expression)</span></span>

<span data-ttu-id="8c969-255">指定された式の平方根を返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-255">Returns the square root of the specified expression.</span></span> 

<span data-ttu-id="8c969-256">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-256">**Arguments**</span></span> 

<span data-ttu-id="8c969-257">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-257">`expression`: A `Double`.</span></span> 

<span data-ttu-id="8c969-258">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-258">**Return Value**</span></span> 

<span data-ttu-id="8c969-259">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-259">A `Double`.</span></span> 

<span data-ttu-id="8c969-260">**例** `SqlServer.SQRT(3600)`</span><span class="sxs-lookup"><span data-stu-id="8c969-260">**Example** `SqlServer.SQRT(3600)`</span></span>

## <a name="squareexpression"></a><span data-ttu-id="8c969-261">SQUARE(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-261">SQUARE(expression)</span></span>

<span data-ttu-id="8c969-262">指定された式の 2 乗値を返します。</span><span class="sxs-lookup"><span data-stu-id="8c969-262">Returns the square of the specified expression.</span></span> 

<span data-ttu-id="8c969-263">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-263">**Arguments**</span></span> 

<span data-ttu-id="8c969-264">`expression`: `Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-264">`expression`: A `Double`.</span></span> 

<span data-ttu-id="8c969-265">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-265">**Return Value**</span></span> 

<span data-ttu-id="8c969-266">`Double`。</span><span class="sxs-lookup"><span data-stu-id="8c969-266">A `Double`.</span></span> 

<span data-ttu-id="8c969-267">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-267">**Example**</span></span> 

`SqlServer.SQUARE(25)`

## <a name="tanexpression"></a><span data-ttu-id="8c969-268">TAN(expression)</span><span class="sxs-lookup"><span data-stu-id="8c969-268">TAN(expression)</span></span>

<span data-ttu-id="8c969-269">指定された式のタンジェントを計算します。</span><span class="sxs-lookup"><span data-stu-id="8c969-269">Calculates the tangent of a specified expression.</span></span>

<span data-ttu-id="8c969-270">**引数**</span><span class="sxs-lookup"><span data-stu-id="8c969-270">**Arguments**</span></span> 

<span data-ttu-id="8c969-271">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="8c969-271">`expression`: `Double`</span></span> 

<span data-ttu-id="8c969-272">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="8c969-272">**Return Value**</span></span> 

`Double` 

<span data-ttu-id="8c969-273">**例**</span><span class="sxs-lookup"><span data-stu-id="8c969-273">**Example**</span></span> 

`SqlServer.TAN(45.0)`
  
## <a name="see-also"></a><span data-ttu-id="8c969-274">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c969-274">See also</span></span>

<span data-ttu-id="8c969-275">SqlClient でサポートされる数学関数の詳細については、SqlClient プロバイダー マニフェストで指定した SQL Server のバージョンのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c969-275">For more information about the mathematical functions that SqlClient supports, see the documentation for the SQL Server version that you specified in the SqlClient provider manifest:</span></span>  
  
<span data-ttu-id="8c969-276">**SQL Server 2005:** [数学関数 (TRANSACT-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span><span class="sxs-lookup"><span data-stu-id="8c969-276">**SQL Server 2005:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span></span>  
<span data-ttu-id="8c969-277">**SQL Server 2008:** [数学関数 (TRANSACT-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span><span class="sxs-lookup"><span data-stu-id="8c969-277">**SQL Server 2008:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span></span>  
<span data-ttu-id="8c969-278">**SQL Server 2012 以降:** [数学関数 (TRANSACT-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="8c969-278">**SQL Server 2012 and later:** [Mathematical Functions (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span></span>   

 [<span data-ttu-id="8c969-279">Entity Framework 用 SqlClient 関数</span><span class="sxs-lookup"><span data-stu-id="8c969-279">SqlClient for Entity Framework Functions</span></span>](sqlclient-for-ef-functions.md)
