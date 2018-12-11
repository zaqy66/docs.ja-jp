---
title: 数学関数
ms.date: 03/30/2017
ms.assetid: b040c7cb-156d-40f2-9152-61065b18148c
ms.openlocfilehash: 63f83532c399f77e268913da3198327345b9c2ee
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53143676"
---
# <a name="mathematical-functions"></a><span data-ttu-id="d8532-102">数学関数</span><span class="sxs-lookup"><span data-stu-id="d8532-102">Mathematical Functions</span></span>

<span data-ttu-id="d8532-103">.NET Framework Data Provider for SQL Server (SqlClient) には、引数として指定された入力値に対して計算を実行し、数値結果を返す数学関数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="d8532-103">The .NET Framework Data Provider for SQL Server (SqlClient) provides math functions that perform calculations on input values that are provided as arguments, and return a numeric value result.</span></span> <span data-ttu-id="d8532-104">これらの関数は、SqlClient の SqlServer 名前空間に存在します。</span><span class="sxs-lookup"><span data-stu-id="d8532-104">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="d8532-105">Entity Framework は、プロバイダーの名前空間プロパティを使用することにより、型や関数など、特定のコンストラクターに対してこのプロバイダーによってどのプレフィックスが使用されているかを特定できます。</span><span class="sxs-lookup"><span data-stu-id="d8532-105">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.</span></span> <span data-ttu-id="d8532-106">次の表では、SqlClient の数学関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="d8532-106">The following table describes the SqlClient math functions.</span></span>  
  
## <a name="absexpression"></a><span data-ttu-id="d8532-107">ABS(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-107">ABS(expression)</span></span>

<span data-ttu-id="d8532-108">絶対値を求める関数です。</span><span class="sxs-lookup"><span data-stu-id="d8532-108">Performs the absolute value function.</span></span>

<span data-ttu-id="d8532-109">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-109">**Arguments**</span></span>

<span data-ttu-id="d8532-110">`expression`:`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-110">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="d8532-111">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-111">**Return Value**</span></span>

<span data-ttu-id="d8532-112">指定された式の絶対値。</span><span class="sxs-lookup"><span data-stu-id="d8532-112">The absolute value of the specified expression.</span></span>

<span data-ttu-id="d8532-113">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-113">**Example**</span></span>

`SqlServer.ABS(-2)`

## <a name="acosexpression"></a><span data-ttu-id="d8532-114">ACOS(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-114">ACOS(expression)</span></span>

<span data-ttu-id="d8532-115">指定された式のアークコサイン (逆余弦) 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-115">Returns the arccosine value of the specified expression.</span></span>

<span data-ttu-id="d8532-116">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-116">**Arguments**</span></span>

<span data-ttu-id="d8532-117">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-117">`expression`: A `Double`.</span></span>

<span data-ttu-id="d8532-118">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-118">**Return Value**</span></span>

<span data-ttu-id="d8532-119">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-119">A `Double`.</span></span>

<span data-ttu-id="d8532-120">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-120">**Example**</span></span>

`SqlServer.ACOS(.9)`

## <a name="asinexpression"></a><span data-ttu-id="d8532-121">ASIN(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-121">ASIN(expression)</span></span>

<span data-ttu-id="d8532-122">指定された式のアークサイン (逆正弦) 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-122">Returns the arcsine value of the specified expression.</span></span>

<span data-ttu-id="d8532-123">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-123">**Arguments**</span></span>

<span data-ttu-id="d8532-124">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-124">`expression`: A `Double`.</span></span>

<span data-ttu-id="d8532-125">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-125">**Return Value**</span></span>

<span data-ttu-id="d8532-126">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-126">A `Double`.</span></span>

<span data-ttu-id="d8532-127">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-127">**Example**</span></span>

`SqlServer.ASIN(.9)`

## <a name="atanexpression"></a><span data-ttu-id="d8532-128">ATAN(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-128">ATAN(expression)</span></span>

<span data-ttu-id="d8532-129">指定された数値式のアークタンジェント (逆正接) 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-129">Returns the arctangent value of the specified numeric expression.</span></span>

<span data-ttu-id="d8532-130">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-130">**Arguments**</span></span>

<span data-ttu-id="d8532-131">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-131">`expression`: A `Double`.</span></span>

<span data-ttu-id="d8532-132">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-132">**Return Value**</span></span>

<span data-ttu-id="d8532-133">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-133">A `Double`.</span></span>

<span data-ttu-id="d8532-134">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-134">**Example**</span></span>

`SqlServer.ATAN(9)`

## <a name="atn2expression-expression"></a><span data-ttu-id="d8532-135">ATN2(expression, expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-135">ATN2(expression, expression)</span></span>

<span data-ttu-id="d8532-136">指定された 2 つの数値式の商がタンジェント (正接) となる角度をラジアンで返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-136">Returns the angle, in radians, whose tangent is between the two specified numeric expressions.</span></span>

<span data-ttu-id="d8532-137">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-137">**Arguments**</span></span>

<span data-ttu-id="d8532-138">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-138">`expression`: A `Double`.</span></span>

<span data-ttu-id="d8532-139">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-139">**Return Value**</span></span>

<span data-ttu-id="d8532-140">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-140">A `Double`.</span></span>

<span data-ttu-id="d8532-141">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-141">**Example**</span></span>

`SqlServer.ATN2(9, 8)`
 
## <a name="ceilingexpression"></a><span data-ttu-id="d8532-142">CEILING(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-142">CEILING(expression)</span></span>

<span data-ttu-id="d8532-143">指定された式をその式以上の最小整数に変換します。</span><span class="sxs-lookup"><span data-stu-id="d8532-143">Converts the specified expression to the smallest integer that is greater than or equal to it.</span></span>

<span data-ttu-id="d8532-144">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-144">**Arguments**</span></span>

<span data-ttu-id="d8532-145">`expression`:`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-145">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="d8532-146">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-146">**Return Value**</span></span>

<span data-ttu-id="d8532-147">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-147">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="d8532-148">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-148">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_ceiling)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_ceiling)]

## <a name="cosexpression"></a><span data-ttu-id="d8532-149">COS(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-149">COS(expression)</span></span>

<span data-ttu-id="d8532-150">ラジアンで指定された角度のコサイン (余弦) を計算します。</span><span class="sxs-lookup"><span data-stu-id="d8532-150">Calculates the trigonometric cosine of the specified angle in radians.</span></span> 

<span data-ttu-id="d8532-151">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-151">**Arguments**</span></span> 

<span data-ttu-id="d8532-152">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-152">`expression`: A `Double`.</span></span> 

<span data-ttu-id="d8532-153">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-153">**Return Value**</span></span> 

<span data-ttu-id="d8532-154">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-154">A `Double`.</span></span> 

<span data-ttu-id="d8532-155">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-155">**Example**</span></span> 

`SqlServer.COS(45)`

## <a name="cotexpression"></a><span data-ttu-id="d8532-156">COT(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-156">COT(expression)</span></span>

<span data-ttu-id="d8532-157">ラジアンで指定された角度のコタンジェント (余接) を計算します。</span><span class="sxs-lookup"><span data-stu-id="d8532-157">Calculates the trigonometric cotangent of the specified angle in radians.</span></span> 

<span data-ttu-id="d8532-158">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-158">**Arguments**</span></span> 

<span data-ttu-id="d8532-159">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-159">`expression`: A `Double`.</span></span> 

<span data-ttu-id="d8532-160">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-160">**Return Value**</span></span> 

<span data-ttu-id="d8532-161">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-161">A `Double`.</span></span> 

<span data-ttu-id="d8532-162">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-162">**Example**</span></span> 

`SqlServer.COT(60)`
  
## <a name="degreesradians"></a><span data-ttu-id="d8532-163">DEGREES(radians)</span><span class="sxs-lookup"><span data-stu-id="d8532-163">DEGREES(radians)</span></span>

<span data-ttu-id="d8532-164">対応する角度を度数で返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-164">Returns the corresponding angle in degrees.</span></span> 

<span data-ttu-id="d8532-165">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-165">**Arguments**</span></span> 

<span data-ttu-id="d8532-166">`expression`:`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-166">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="d8532-167">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-167">**Return Value**</span></span> 

<span data-ttu-id="d8532-168">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-168">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="d8532-169">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-169">**Example**</span></span> 

`SqlServer.DEGREES(3.1)`

## <a name="expexpression"></a><span data-ttu-id="d8532-170">EXP(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-170">EXP(expression)</span></span>

<span data-ttu-id="d8532-171">指定された数値式の指数値を計算します。</span><span class="sxs-lookup"><span data-stu-id="d8532-171">Calculates the exponential value of a specified numeric expression.</span></span> 

<span data-ttu-id="d8532-172">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-172">**Arguments**</span></span> 

<span data-ttu-id="d8532-173">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-173">`expression`: A `Double`.</span></span> 

<span data-ttu-id="d8532-174">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-174">**Return Value**</span></span> 

<span data-ttu-id="d8532-175">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-175">A `Double`.</span></span> 

<span data-ttu-id="d8532-176">**例** `SqlServer.EXP(1)`</span><span class="sxs-lookup"><span data-stu-id="d8532-176">**Example** `SqlServer.EXP(1)`</span></span>

## <a name="floorexpression"></a><span data-ttu-id="d8532-177">FLOOR(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-177">FLOOR(expression)</span></span>

<span data-ttu-id="d8532-178">指定された式をその式以下の最大整数に変換します。</span><span class="sxs-lookup"><span data-stu-id="d8532-178">Converts the specified expression to the largest integer less than or equal to it.</span></span> 

<span data-ttu-id="d8532-179">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-179">**Arguments**</span></span> 

<span data-ttu-id="d8532-180">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-180">`expression`: A `Double`.</span></span> 

<span data-ttu-id="d8532-181">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-181">**Return Value**</span></span> 

<span data-ttu-id="d8532-182">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-182">A `Double`.</span></span> 

<span data-ttu-id="d8532-183">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-183">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_floor)] 
[!code-sql[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_floor)]

## <a name="logexpression"></a><span data-ttu-id="d8532-184">LOG(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-184">LOG(expression)</span></span>

<span data-ttu-id="d8532-185">指定された `float` 型の式の自然対数を計算します。</span><span class="sxs-lookup"><span data-stu-id="d8532-185">Calculates the natural logarithm of the specified `float` expression.</span></span> 

<span data-ttu-id="d8532-186">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-186">**Arguments**</span></span> 

<span data-ttu-id="d8532-187">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-187">`expression`: A `Double`.</span></span> 

<span data-ttu-id="d8532-188">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-188">**Return Value**</span></span> 

<span data-ttu-id="d8532-189">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-189">A `Double`.</span></span> 

<span data-ttu-id="d8532-190">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-190">**Example**</span></span> 

`SqlServer.LOG(100)`

## <a name="log10expression"></a><span data-ttu-id="d8532-191">LOG10(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-191">LOG10(expression)</span></span>

<span data-ttu-id="d8532-192">指定された `Double` 型の式の 10 を底とした対数を返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-192">Returns the base-10 logarithm of the specified `Double` expression.</span></span> 

<span data-ttu-id="d8532-193">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-193">**Arguments**</span></span> 

<span data-ttu-id="d8532-194">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-194">`expression`: A `Double`.</span></span> 

<span data-ttu-id="d8532-195">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-195">**Return Value**</span></span> 

<span data-ttu-id="d8532-196">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-196">A `Double`.</span></span> 

<span data-ttu-id="d8532-197">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-197">**Example**</span></span> 

`SqlServer.LOG10(100)`

## <a name="pi"></a><span data-ttu-id="d8532-198">PI()」と指定</span><span class="sxs-lookup"><span data-stu-id="d8532-198">PI()</span></span>

<span data-ttu-id="d8532-199">π の定数値を `Double` として返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-199">Returns the constant value of pi as a `Double`.</span></span> 

<span data-ttu-id="d8532-200">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-200">**Return Value**</span></span> 

<span data-ttu-id="d8532-201">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-201">A `Double`.</span></span> 

<span data-ttu-id="d8532-202">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-202">**Example**</span></span> 

`SqlServer.PI()`

## <a name="powernumericexpression-powerexpression"></a><span data-ttu-id="d8532-203">電源 (numeric_expression、power_expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-203">POWER(numeric_expression, power_expression)</span></span>

<span data-ttu-id="d8532-204">指定された式の指定されたべき乗を計算します。</span><span class="sxs-lookup"><span data-stu-id="d8532-204">Calculates the value of a specified expression to a specified power.</span></span>

<span data-ttu-id="d8532-205">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-205">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="d8532-206">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-206">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>|
|`power_expression`| <span data-ttu-id="d8532-207">A`Double`のべき乗値を表す、`numeric_expression`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-207">A `Double` that represents the power to which to raise the `numeric_expression`.</span></span>| 

<span data-ttu-id="d8532-208">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-208">**Return Value**</span></span> 

<span data-ttu-id="d8532-209">指定された `numeric_expression` を指定された `power_expression` でべき乗した値。</span><span class="sxs-lookup"><span data-stu-id="d8532-209">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span> 

<span data-ttu-id="d8532-210">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-210">**Example**</span></span> 

`SqlServer.POWER(2,7)`

## <a name="radiansexpression"></a><span data-ttu-id="d8532-211">RADIANS(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-211">RADIANS(expression)</span></span>

<span data-ttu-id="d8532-212">角度をラジアンに変換します。</span><span class="sxs-lookup"><span data-stu-id="d8532-212">Converts degrees to radians.</span></span> 

<span data-ttu-id="d8532-213">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-213">**Arguments**</span></span> 

<span data-ttu-id="d8532-214">`expression`:`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-214">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="d8532-215">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-215">**Return Value**</span></span> 

<span data-ttu-id="d8532-216">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-216">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="d8532-217">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-217">**Example**</span></span> 

`SqlServer.RADIANS(360.0)`

## <a name="randseed"></a><span data-ttu-id="d8532-218">RAND([seed])</span><span class="sxs-lookup"><span data-stu-id="d8532-218">RAND([seed])</span></span>

<span data-ttu-id="d8532-219">0 から 1 までの範囲の乱数を返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-219">Returns a random value from 0 through 1.</span></span> 

<span data-ttu-id="d8532-220">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-220">**Arguments**</span></span> 

<span data-ttu-id="d8532-221">シード値として、`Int32`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-221">The seed value as an `Int32`.</span></span> <span data-ttu-id="d8532-222">シードを指定しない場合は、SQL Server データベース エンジンによってシード値がランダムに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d8532-222">If the seed is not specified, the SQL Server Database Engine assigns a seed value at random.</span></span> <span data-ttu-id="d8532-223">指定したシード値について、返される結果は常に同じです。</span><span class="sxs-lookup"><span data-stu-id="d8532-223">For a specified seed value, the result returned is always the same.</span></span>

<span data-ttu-id="d8532-224">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-224">**Return Value**</span></span> 

<span data-ttu-id="d8532-225">0 から 1 までの範囲の `Double` 型の乱数。</span><span class="sxs-lookup"><span data-stu-id="d8532-225">A random `Double` value from 0 through 1.</span></span> 

<span data-ttu-id="d8532-226">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-226">**Example**</span></span> 

`SqlServer.RAND()`
  
## <a name="roundnumericexpression-lengthfunction"></a><span data-ttu-id="d8532-227">ROUND(numeric_expression, length[,function])</span><span class="sxs-lookup"><span data-stu-id="d8532-227">ROUND(numeric_expression, length[,function])</span></span>

<span data-ttu-id="d8532-228">指定された長さまたは有効桁数に丸めた数値式を返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-228">Returns a numeric expression, rounded to the specified length or precision.</span></span> 

<span data-ttu-id="d8532-229">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-229">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="d8532-230">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-230">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 
|`length`| <span data-ttu-id="d8532-231">`Int32` を丸めた後の有効桁数を表す `numeric_expression`。</span><span class="sxs-lookup"><span data-stu-id="d8532-231">An `Int32` that represents the precision to which `numeric_expression` is to be rounded.</span></span> <span data-ttu-id="d8532-232">`length` に正の値を指定した場合、`numeric_expression` は `length` で指定した小数点以下桁数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="d8532-232">When `length` is a positive number, `numeric_expression` is rounded to the number of decimal positions specified by `length`.</span></span> <span data-ttu-id="d8532-233">`length` に負の値を指定した場合、`numeric_expression` は `length` で指定した小数点の左側の位置で丸められます。</span><span class="sxs-lookup"><span data-stu-id="d8532-233">When `length` is a negative number, `numeric_expression` is rounded on the left side of the decimal point, as specified by `length`.</span></span>|
|`function` | <span data-ttu-id="d8532-234">任意。</span><span class="sxs-lookup"><span data-stu-id="d8532-234">Optional.</span></span> <span data-ttu-id="d8532-235">`Int32`を実行する操作の種類を表します。</span><span class="sxs-lookup"><span data-stu-id="d8532-235">An `Int32` that represents the type of operation to perform.</span></span> <span data-ttu-id="d8532-236">関数を省略するか 0 (既定値) の値を持つとき`numeric_expression`は丸められます。</span><span class="sxs-lookup"><span data-stu-id="d8532-236">When function is omitted or has a value of 0 (default), `numeric_expression` is rounded.</span></span> <span data-ttu-id="d8532-237">以外の値は 0 を指定した、`numeric_expression`は切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="d8532-237">When a value other than 0 is specified, `numeric_expression` is truncated.</span></span> |

<span data-ttu-id="d8532-238">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-238">**Return Value**</span></span> 

<span data-ttu-id="d8532-239">指定された `numeric_expression` を指定された `power_expression` でべき乗した値。</span><span class="sxs-lookup"><span data-stu-id="d8532-239">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span>

<span data-ttu-id="d8532-240">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-240">**Example**</span></span> 

`SqlServer.ROUND(748.58, -3)`

## <a name="signexpression"></a><span data-ttu-id="d8532-241">SIGN(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-241">SIGN(expression)</span></span> 

<span data-ttu-id="d8532-242">指定した式の符号として、正 (+1)、負 (-1)、ゼロ (0) のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-242">Returns the positive (+1), zero (0), or negative (-1) sign of the specified expression.</span></span> 

<span data-ttu-id="d8532-243">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-243">**Arguments**</span></span> 

<span data-ttu-id="d8532-244">`expression`: `Int32`、`Int64`、`Double`、または `Decimal`</span><span class="sxs-lookup"><span data-stu-id="d8532-244">`expression`: `Int32`, `Int64`, `Double`, or `Decimal`</span></span> 

<span data-ttu-id="d8532-245">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-245">**Return Value**</span></span> 

<span data-ttu-id="d8532-246">`Int32`、 `Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="d8532-246">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="d8532-247">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-247">**Example**</span></span> 

`SqlServer.SIGN(-10)`

## <a name="sinexpression"></a><span data-ttu-id="d8532-248">SIN(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-248">SIN(expression)</span></span>

<span data-ttu-id="d8532-249">ラジアンで指定された角度のサイン (正弦) を計算し、`Double` 式を返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-249">Calculates the trigonometric sine of the specified angle in radians, and returns a `Double` expression.</span></span> 

<span data-ttu-id="d8532-250">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-250">**Arguments**</span></span> 

<span data-ttu-id="d8532-251">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-251">`expression`: A `Double`.</span></span> 

<span data-ttu-id="d8532-252">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-252">**Return Value**</span></span> 

<span data-ttu-id="d8532-253">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-253">A `Double`.</span></span> 

<span data-ttu-id="d8532-254">**例** `SqlServer.SIN(20)`</span><span class="sxs-lookup"><span data-stu-id="d8532-254">**Example** `SqlServer.SIN(20)`</span></span>

## <a name="sqrtexpression"></a><span data-ttu-id="d8532-255">SQRT(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-255">SQRT(expression)</span></span>

<span data-ttu-id="d8532-256">指定された式の平方根を返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-256">Returns the square root of the specified expression.</span></span> 

<span data-ttu-id="d8532-257">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-257">**Arguments**</span></span> 

<span data-ttu-id="d8532-258">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-258">`expression`: A `Double`.</span></span> 

<span data-ttu-id="d8532-259">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-259">**Return Value**</span></span> 

<span data-ttu-id="d8532-260">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-260">A `Double`.</span></span> 

<span data-ttu-id="d8532-261">**例** `SqlServer.SQRT(3600)`</span><span class="sxs-lookup"><span data-stu-id="d8532-261">**Example** `SqlServer.SQRT(3600)`</span></span>

## <a name="squareexpression"></a><span data-ttu-id="d8532-262">SQUARE(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-262">SQUARE(expression)</span></span>

<span data-ttu-id="d8532-263">指定された式の 2 乗値を返します。</span><span class="sxs-lookup"><span data-stu-id="d8532-263">Returns the square of the specified expression.</span></span> 

<span data-ttu-id="d8532-264">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-264">**Arguments**</span></span> 

<span data-ttu-id="d8532-265">`expression`:`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-265">`expression`: A `Double`.</span></span> 

<span data-ttu-id="d8532-266">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-266">**Return Value**</span></span> 

<span data-ttu-id="d8532-267">`Double`。</span><span class="sxs-lookup"><span data-stu-id="d8532-267">A `Double`.</span></span> 

<span data-ttu-id="d8532-268">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-268">**Example**</span></span> 

`SqlServer.SQUARE(25)`

## <a name="tanexpression"></a><span data-ttu-id="d8532-269">TAN(expression)</span><span class="sxs-lookup"><span data-stu-id="d8532-269">TAN(expression)</span></span>

<span data-ttu-id="d8532-270">指定された式のタンジェントを計算します。</span><span class="sxs-lookup"><span data-stu-id="d8532-270">Calculates the tangent of a specified expression.</span></span>

<span data-ttu-id="d8532-271">**引数**</span><span class="sxs-lookup"><span data-stu-id="d8532-271">**Arguments**</span></span> 

<span data-ttu-id="d8532-272">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="d8532-272">`expression`: `Double`</span></span> 

<span data-ttu-id="d8532-273">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d8532-273">**Return Value**</span></span> 

`Double` 

<span data-ttu-id="d8532-274">**例**</span><span class="sxs-lookup"><span data-stu-id="d8532-274">**Example**</span></span> 

`SqlServer.TAN(45.0)`
  
## <a name="see-also"></a><span data-ttu-id="d8532-275">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8532-275">See also</span></span>

<span data-ttu-id="d8532-276">SqlClient でサポートされる数学関数の詳細については、SqlClient プロバイダー マニフェストで指定した SQL Server のバージョンのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8532-276">For more information about the mathematical functions that SqlClient supports, see the documentation for the SQL Server version that you specified in the SqlClient provider manifest:</span></span>  
  
<span data-ttu-id="d8532-277">**SQL Server 2005:**[数学関数 (TRANSACT-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span><span class="sxs-lookup"><span data-stu-id="d8532-277">**SQL Server 2005:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span></span>  
<span data-ttu-id="d8532-278">**SQL Server 2008:**[数学関数 (TRANSACT-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span><span class="sxs-lookup"><span data-stu-id="d8532-278">**SQL Server 2008:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span></span>  
<span data-ttu-id="d8532-279">**SQL Server 2012 以降の場合:**[数学関数 (TRANSACT-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="d8532-279">**SQL Server 2012 and later:** [Mathematical Functions (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span></span>   

 [<span data-ttu-id="d8532-280">Entity Framework 用 SqlClient 関数</span><span class="sxs-lookup"><span data-stu-id="d8532-280">SqlClient for Entity Framework Functions</span></span>](sqlclient-for-ef-functions.md)
