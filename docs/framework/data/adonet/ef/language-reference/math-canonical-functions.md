---
title: 数値演算正規関数
ms.date: 03/30/2017
ms.assetid: 6f6cddc6-b561-4ebe-84b6-841ef5b4113b
ms.openlocfilehash: 0fc9f4942c3f76f139ab7e4400005f0bfe80204e
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47208439"
---
# <a name="math-canonical-functions"></a><span data-ttu-id="46001-102">数値演算正規関数</span><span class="sxs-lookup"><span data-stu-id="46001-102">Math Canonical Functions</span></span>

<span data-ttu-id="46001-103">Entity SQL では、次の数値演算正規関数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="46001-103">Entity SQL includes the following math canonical functions:</span></span>
  
## <a name="absvalue"></a><span data-ttu-id="46001-104">Abs(value)</span><span class="sxs-lookup"><span data-stu-id="46001-104">Abs(value)</span></span>

<span data-ttu-id="46001-105">`value` の絶対値を返します。</span><span class="sxs-lookup"><span data-stu-id="46001-105">Returns the absolute value of `value`.</span></span>

<span data-ttu-id="46001-106">**引数**</span><span class="sxs-lookup"><span data-stu-id="46001-106">**Arguments**</span></span>

<span data-ttu-id="46001-107">`Int16`、 `Int32`、 `Int64`、 `Byte`、 `Single`、 `Double`、および`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="46001-107">An `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="46001-108">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="46001-108">**Return Value**</span></span>

<span data-ttu-id="46001-109">`value` の型。</span><span class="sxs-lookup"><span data-stu-id="46001-109">The type of `value`.</span></span>

<span data-ttu-id="46001-110">**例**</span><span class="sxs-lookup"><span data-stu-id="46001-110">**Example**</span></span>

`Abs(-2)`

## <a name="ceilingvalue"></a><span data-ttu-id="46001-111">Ceiling(value)</span><span class="sxs-lookup"><span data-stu-id="46001-111">Ceiling(value)</span></span>

<span data-ttu-id="46001-112">`value` 以上で最小の整数値を返します。</span><span class="sxs-lookup"><span data-stu-id="46001-112">Returns the smallest integer that is not less than `value`.</span></span>

<span data-ttu-id="46001-113">**引数**</span><span class="sxs-lookup"><span data-stu-id="46001-113">**Arguments**</span></span>

<span data-ttu-id="46001-114">A `Single`、 `Double`、および`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="46001-114">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="46001-115">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="46001-115">**Return Value**</span></span>

<span data-ttu-id="46001-116">`value` の型。</span><span class="sxs-lookup"><span data-stu-id="46001-116">The type of `value`.</span></span>

<span data-ttu-id="46001-117">**例**</span><span class="sxs-lookup"><span data-stu-id="46001-117">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_ceiling)]
[!code-sql[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_ceiling)]

## <a name="floorvalue"></a><span data-ttu-id="46001-118">Floor(value)</span><span class="sxs-lookup"><span data-stu-id="46001-118">Floor(value)</span></span>

<span data-ttu-id="46001-119">`value` 以下で最大の整数値を返します。</span><span class="sxs-lookup"><span data-stu-id="46001-119">Returns the largest integer that is not greater than `value`.</span></span>

<span data-ttu-id="46001-120">**引数**</span><span class="sxs-lookup"><span data-stu-id="46001-120">**Arguments**</span></span>

<span data-ttu-id="46001-121">A `Single`、 `Double`、および`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="46001-121">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="46001-122">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="46001-122">**Return Value**</span></span>

<span data-ttu-id="46001-123">`value` の型。</span><span class="sxs-lookup"><span data-stu-id="46001-123">The type of `value`.</span></span>

<span data-ttu-id="46001-124">**例**</span><span class="sxs-lookup"><span data-stu-id="46001-124">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_floor)]
[!code-sql[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_floor)]

## <a name="powervalue-exponent"></a><span data-ttu-id="46001-125">Power(value, exponent)</span><span class="sxs-lookup"><span data-stu-id="46001-125">Power(value, exponent)</span></span>

<span data-ttu-id="46001-126">指定された `value` を指定された `exponent` でべき乗した結果を返します。</span><span class="sxs-lookup"><span data-stu-id="46001-126">Returns the result of the specified `value` to the specified `exponent`.</span></span>

<span data-ttu-id="46001-127">**引数**</span><span class="sxs-lookup"><span data-stu-id="46001-127">**Arguments**</span></span>

|  |  |
|--|--|
|`value` | <span data-ttu-id="46001-128">`Int32, Int64, Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="46001-128">An `Int32, Int64, Double`, or `Decimal`.</span></span> |
|`exponent` | <span data-ttu-id="46001-129">`Int64`、 `Double`、または`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="46001-129">An `Int64`, `Double`, or `Decimal`.</span></span> |

<span data-ttu-id="46001-130">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="46001-130">**Return Value**</span></span>

<span data-ttu-id="46001-131">`value` の型。</span><span class="sxs-lookup"><span data-stu-id="46001-131">The type of `value`.</span></span>

<span data-ttu-id="46001-132">**例**</span><span class="sxs-lookup"><span data-stu-id="46001-132">**Example**</span></span>

`Power(748.58,2)`

## <a name="roundvalue"></a><span data-ttu-id="46001-133">Round(value)</span><span class="sxs-lookup"><span data-stu-id="46001-133">Round(value)</span></span>

<span data-ttu-id="46001-134">最も近い整数に丸められた `value` の整数部分を返します。</span><span class="sxs-lookup"><span data-stu-id="46001-134">Returns the integer portion of `value`, rounded to the nearest integer.</span></span>

<span data-ttu-id="46001-135">**引数**</span><span class="sxs-lookup"><span data-stu-id="46001-135">**Arguments**</span></span>

<span data-ttu-id="46001-136">A `Single`、 `Double`、および`Decimal`します。</span><span class="sxs-lookup"><span data-stu-id="46001-136">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="46001-137">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="46001-137">**Return Value**</span></span>

<span data-ttu-id="46001-138">`value` の型。</span><span class="sxs-lookup"><span data-stu-id="46001-138">The type of `value`.</span></span>

<span data-ttu-id="46001-139">**例**</span><span class="sxs-lookup"><span data-stu-id="46001-139">**Example**</span></span>

`Round(748.58)`

## <a name="roundvalue-digits"></a><span data-ttu-id="46001-140">Round(value, digits)</span><span class="sxs-lookup"><span data-stu-id="46001-140">Round(value, digits)</span></span>

<span data-ttu-id="46001-141">`value` を指定された最も近い `digits` に丸めて返します。</span><span class="sxs-lookup"><span data-stu-id="46001-141">Returns the `value`, rounded to the nearest specified `digits`.</span></span>

<span data-ttu-id="46001-142">**引数**</span><span class="sxs-lookup"><span data-stu-id="46001-142">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="46001-143">`Double` または `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="46001-143">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="46001-144">`Int16` または `Int32`。</span><span class="sxs-lookup"><span data-stu-id="46001-144">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="46001-145">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="46001-145">**Return Value**</span></span>

<span data-ttu-id="46001-146">`value` の型。</span><span class="sxs-lookup"><span data-stu-id="46001-146">The type of `value`.</span></span>

<span data-ttu-id="46001-147">**例**</span><span class="sxs-lookup"><span data-stu-id="46001-147">**Example**</span></span>

`Round(748.58,1)`

## <a name="truncatevalue-digits"></a><span data-ttu-id="46001-148">Truncate(value, digits)</span><span class="sxs-lookup"><span data-stu-id="46001-148">Truncate(value, digits)</span></span>

<span data-ttu-id="46001-149">`value` を指定された最も近い `digits` に切り詰めて返します。</span><span class="sxs-lookup"><span data-stu-id="46001-149">Returns the `value`, truncated to the nearest specified `digits`.</span></span>

<span data-ttu-id="46001-150">**引数**</span><span class="sxs-lookup"><span data-stu-id="46001-150">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="46001-151">`Double` または `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="46001-151">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="46001-152">`Int16` または `Int32`。</span><span class="sxs-lookup"><span data-stu-id="46001-152">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="46001-153">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="46001-153">**Return Value**</span></span>

<span data-ttu-id="46001-154">`value` の型。</span><span class="sxs-lookup"><span data-stu-id="46001-154">The type of `value`.</span></span>

<span data-ttu-id="46001-155">**例**</span><span class="sxs-lookup"><span data-stu-id="46001-155">**Example**</span></span>

`Truncate(748.58,1)`  
  
 <span data-ttu-id="46001-156">`null` が入力された場合、これらの関数は `null` を返します。</span><span class="sxs-lookup"><span data-stu-id="46001-156">These functions will return `null` if given `null` input.</span></span>  
  
 <span data-ttu-id="46001-157">同等の機能は、Microsoft SQL クライアント マネージド プロバイダーでも利用できます。</span><span class="sxs-lookup"><span data-stu-id="46001-157">Equivalent functionality is available in the Microsoft SQL Client Managed Provider.</span></span> <span data-ttu-id="46001-158">詳細については、次を参照してください。 [Entity Framework の関数の SqlClient](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md)します。</span><span class="sxs-lookup"><span data-stu-id="46001-158">For more information, see [SqlClient for Entity Framework Functions](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46001-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="46001-159">See Also</span></span>  
 [<span data-ttu-id="46001-160">正規関数</span><span class="sxs-lookup"><span data-stu-id="46001-160">Canonical Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
