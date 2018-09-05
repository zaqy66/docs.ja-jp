---
title: ODBC スキーマ コレクション
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: bdedbb11960f02b99dcca6388abf663635238f74
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43750010"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="0ce81-102">ODBC スキーマ コレクション</span><span class="sxs-lookup"><span data-stu-id="0ce81-102">ODBC Schema Collections</span></span>
<span data-ttu-id="0ce81-103">ここでは、Microsoft SQL Server、Oracle、および Microsoft Jet 用の各 ODBC ドライバーでのスキーマ コレクションのサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0ce81-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="0ce81-104">Microsoft SQL Server ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="0ce81-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="0ce81-105">Microsoft SQL Server ODBC Driver には、共通のスキーマ コレクションに加えて次の特定のスキーマ コレクションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0ce81-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="0ce81-106">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="0ce81-106">Tables</span></span>  
  
-   <span data-ttu-id="0ce81-107">Indexes</span><span class="sxs-lookup"><span data-stu-id="0ce81-107">Indexes</span></span>  
  
-   <span data-ttu-id="0ce81-108">列</span><span class="sxs-lookup"><span data-stu-id="0ce81-108">Columns</span></span>  
  
-   <span data-ttu-id="0ce81-109">手順</span><span class="sxs-lookup"><span data-stu-id="0ce81-109">Procedures</span></span>  
  
-   <span data-ttu-id="0ce81-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0ce81-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="0ce81-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0ce81-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="0ce81-112">ビュー</span><span class="sxs-lookup"><span data-stu-id="0ce81-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="0ce81-113">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="0ce81-113">Tables and Views</span></span>  
  
|<span data-ttu-id="0ce81-114">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-114">ColumnName</span></span>|<span data-ttu-id="0ce81-115">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="0ce81-116">TABLE_CAT</span></span>|<span data-ttu-id="0ce81-117">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-117">String</span></span>|  
|<span data-ttu-id="0ce81-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0ce81-118">TABLE_SCHEM</span></span>|<span data-ttu-id="0ce81-119">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-119">String</span></span>|  
|<span data-ttu-id="0ce81-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-120">TABLE_NAME</span></span>|<span data-ttu-id="0ce81-121">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-121">String</span></span>|  
|<span data-ttu-id="0ce81-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-122">TABLE_TYPE</span></span>|<span data-ttu-id="0ce81-123">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-123">String</span></span>|  
|<span data-ttu-id="0ce81-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-124">REMARKS</span></span>|<span data-ttu-id="0ce81-125">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="0ce81-126">Indexes</span><span class="sxs-lookup"><span data-stu-id="0ce81-126">Indexes</span></span>  
  
|<span data-ttu-id="0ce81-127">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-127">ColumnName</span></span>|<span data-ttu-id="0ce81-128">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="0ce81-129">TABLE_CAT</span></span>|<span data-ttu-id="0ce81-130">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-130">String</span></span>|  
|<span data-ttu-id="0ce81-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0ce81-131">TABLE_SCHEM</span></span>|<span data-ttu-id="0ce81-132">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-132">String</span></span>|  
|<span data-ttu-id="0ce81-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-133">TABLE_NAME</span></span>|<span data-ttu-id="0ce81-134">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-134">String</span></span>|  
|<span data-ttu-id="0ce81-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="0ce81-135">NON_UNIQUE</span></span>|<span data-ttu-id="0ce81-136">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-136">Int16</span></span>|  
|<span data-ttu-id="0ce81-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0ce81-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="0ce81-138">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-138">String</span></span>|  
|<span data-ttu-id="0ce81-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-139">INDEX_NAME</span></span>|<span data-ttu-id="0ce81-140">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-140">String</span></span>|  
|<span data-ttu-id="0ce81-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-141">TYPE</span></span>|<span data-ttu-id="0ce81-142">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-142">Int16</span></span>|  
|<span data-ttu-id="0ce81-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0ce81-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="0ce81-144">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-144">Int16</span></span>|  
|<span data-ttu-id="0ce81-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-145">COLUMN_NAME</span></span>|<span data-ttu-id="0ce81-146">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-146">String</span></span>|  
|<span data-ttu-id="0ce81-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="0ce81-147">ASC_OR_DESC</span></span>|<span data-ttu-id="0ce81-148">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-148">String</span></span>|  
|<span data-ttu-id="0ce81-149">CARDINATLITY</span><span class="sxs-lookup"><span data-stu-id="0ce81-149">CARDINATLITY</span></span>|<span data-ttu-id="0ce81-150">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-150">Int32</span></span>|  
|<span data-ttu-id="0ce81-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="0ce81-151">PAGES</span></span>|<span data-ttu-id="0ce81-152">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-152">Int32</span></span>|  
|<span data-ttu-id="0ce81-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="0ce81-153">FILTER_CONDITION</span></span>|<span data-ttu-id="0ce81-154">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-154">String</span></span>|  
|<span data-ttu-id="0ce81-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0ce81-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="0ce81-156">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-156">String</span></span>|  
|<span data-ttu-id="0ce81-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="0ce81-158">Byte</span><span class="sxs-lookup"><span data-stu-id="0ce81-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="0ce81-159">列</span><span class="sxs-lookup"><span data-stu-id="0ce81-159">Columns</span></span>  
  
|<span data-ttu-id="0ce81-160">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-160">ColumnName</span></span>|<span data-ttu-id="0ce81-161">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="0ce81-162">TABLE_CAT</span></span>|<span data-ttu-id="0ce81-163">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-163">String</span></span>|  
|<span data-ttu-id="0ce81-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0ce81-164">TABLE_SCHEM</span></span>|<span data-ttu-id="0ce81-165">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-165">String</span></span>|  
|<span data-ttu-id="0ce81-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-166">TABLE_NAME</span></span>|<span data-ttu-id="0ce81-167">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-167">String</span></span>|  
|<span data-ttu-id="0ce81-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-168">COLUMN_NAME</span></span>|<span data-ttu-id="0ce81-169">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-169">String</span></span>|  
|<span data-ttu-id="0ce81-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-170">DATA_TYPE</span></span>|<span data-ttu-id="0ce81-171">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-171">Int16</span></span>|  
|<span data-ttu-id="0ce81-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-172">TYPE_NAME</span></span>|<span data-ttu-id="0ce81-173">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-173">String</span></span>|  
|<span data-ttu-id="0ce81-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="0ce81-174">COLUMN_SIZE</span></span>|<span data-ttu-id="0ce81-175">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-175">Int32</span></span>|  
|<span data-ttu-id="0ce81-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="0ce81-177">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-177">Int32</span></span>|  
|<span data-ttu-id="0ce81-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="0ce81-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="0ce81-179">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-179">Int16</span></span>|  
|<span data-ttu-id="0ce81-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="0ce81-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="0ce81-181">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-181">Int16</span></span>|  
|<span data-ttu-id="0ce81-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-182">NULLABLE</span></span>|<span data-ttu-id="0ce81-183">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-183">Int16</span></span>|  
|<span data-ttu-id="0ce81-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-184">REMARKS</span></span>|<span data-ttu-id="0ce81-185">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-185">String</span></span>|  
|<span data-ttu-id="0ce81-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="0ce81-186">COLUMN_DEF</span></span>|<span data-ttu-id="0ce81-187">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-187">String</span></span>|  
|<span data-ttu-id="0ce81-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="0ce81-189">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-189">Int16</span></span>|  
|<span data-ttu-id="0ce81-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="0ce81-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="0ce81-191">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-191">Int16</span></span>|  
|<span data-ttu-id="0ce81-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="0ce81-193">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-193">Int32</span></span>|  
|<span data-ttu-id="0ce81-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0ce81-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="0ce81-195">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-195">Int32</span></span>|  
|<span data-ttu-id="0ce81-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-196">IS_NULLABLE</span></span>|<span data-ttu-id="0ce81-197">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-197">String</span></span>|  
|<span data-ttu-id="0ce81-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0ce81-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="0ce81-199">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-199">String</span></span>|  
|<span data-ttu-id="0ce81-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0ce81-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="0ce81-201">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-201">String</span></span>|  
|<span data-ttu-id="0ce81-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="0ce81-203">Byte</span><span class="sxs-lookup"><span data-stu-id="0ce81-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="0ce81-204">手順</span><span class="sxs-lookup"><span data-stu-id="0ce81-204">Procedures</span></span>  
  
|<span data-ttu-id="0ce81-205">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-205">ColumnName</span></span>|<span data-ttu-id="0ce81-206">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="0ce81-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="0ce81-208">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-208">String</span></span>|  
|<span data-ttu-id="0ce81-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0ce81-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="0ce81-210">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-210">String</span></span>|  
|<span data-ttu-id="0ce81-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="0ce81-212">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-212">String</span></span>|  
|<span data-ttu-id="0ce81-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0ce81-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="0ce81-214">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-214">Int32</span></span>|  
|<span data-ttu-id="0ce81-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0ce81-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="0ce81-216">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-216">Int32</span></span>|  
|<span data-ttu-id="0ce81-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="0ce81-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="0ce81-218">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-218">Int32</span></span>|  
|<span data-ttu-id="0ce81-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-219">REMARKS</span></span>|<span data-ttu-id="0ce81-220">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-220">String</span></span>|  
|<span data-ttu-id="0ce81-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="0ce81-222">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="0ce81-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0ce81-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="0ce81-224">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-224">ColumnName</span></span>|<span data-ttu-id="0ce81-225">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="0ce81-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="0ce81-227">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-227">String</span></span>|  
|<span data-ttu-id="0ce81-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0ce81-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="0ce81-229">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-229">String</span></span>|  
|<span data-ttu-id="0ce81-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="0ce81-231">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-231">String</span></span>|  
|<span data-ttu-id="0ce81-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-232">COLUMN_NAME</span></span>|<span data-ttu-id="0ce81-233">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-233">String</span></span>|  
|<span data-ttu-id="0ce81-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-234">COLUMN_TYPE</span></span>|<span data-ttu-id="0ce81-235">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-235">Int16</span></span>|  
|<span data-ttu-id="0ce81-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-236">DATA_TYPE</span></span>|<span data-ttu-id="0ce81-237">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-237">Int16</span></span>|  
|<span data-ttu-id="0ce81-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-238">TYPE_NAME</span></span>|<span data-ttu-id="0ce81-239">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-239">String</span></span>|  
|<span data-ttu-id="0ce81-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="0ce81-240">COLUMN_SIZE</span></span>|<span data-ttu-id="0ce81-241">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-241">Int32</span></span>|  
|<span data-ttu-id="0ce81-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="0ce81-243">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-243">Int32</span></span>|  
|<span data-ttu-id="0ce81-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="0ce81-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="0ce81-245">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-245">Int16</span></span>|  
|<span data-ttu-id="0ce81-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="0ce81-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="0ce81-247">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-247">Int16</span></span>|  
|<span data-ttu-id="0ce81-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-248">NULLABLE</span></span>|<span data-ttu-id="0ce81-249">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-249">Int16</span></span>|  
|<span data-ttu-id="0ce81-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-250">REMARKS</span></span>|<span data-ttu-id="0ce81-251">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-251">String</span></span>|  
|<span data-ttu-id="0ce81-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="0ce81-252">COLUMN_DEF</span></span>|<span data-ttu-id="0ce81-253">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-253">String</span></span>|  
|<span data-ttu-id="0ce81-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="0ce81-255">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-255">Int16</span></span>|  
|<span data-ttu-id="0ce81-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="0ce81-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="0ce81-257">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-257">Int16</span></span>|  
|<span data-ttu-id="0ce81-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="0ce81-259">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-259">Int32</span></span>|  
|<span data-ttu-id="0ce81-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0ce81-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="0ce81-261">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-261">Int32</span></span>|  
|<span data-ttu-id="0ce81-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-262">IS_NULLABLE</span></span>|<span data-ttu-id="0ce81-263">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-263">String</span></span>|  
|<span data-ttu-id="0ce81-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0ce81-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="0ce81-265">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-265">String</span></span>|  
|<span data-ttu-id="0ce81-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0ce81-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="0ce81-267">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-267">String</span></span>|  
|<span data-ttu-id="0ce81-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="0ce81-269">Byte</span><span class="sxs-lookup"><span data-stu-id="0ce81-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="0ce81-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0ce81-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="0ce81-271">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-271">ColumnName</span></span>|<span data-ttu-id="0ce81-272">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="0ce81-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="0ce81-274">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-274">String</span></span>|  
|<span data-ttu-id="0ce81-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0ce81-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="0ce81-276">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-276">String</span></span>|  
|<span data-ttu-id="0ce81-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="0ce81-278">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-278">String</span></span>|  
|<span data-ttu-id="0ce81-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-279">COLUMN_NAME</span></span>|<span data-ttu-id="0ce81-280">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-280">String</span></span>|  
|<span data-ttu-id="0ce81-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-281">COLUMN_TYPE</span></span>|<span data-ttu-id="0ce81-282">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-282">Int16</span></span>|  
|<span data-ttu-id="0ce81-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-283">DATA_TYPE</span></span>|<span data-ttu-id="0ce81-284">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-284">Int16</span></span>|  
|<span data-ttu-id="0ce81-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-285">TYPE_NAME</span></span>|<span data-ttu-id="0ce81-286">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-286">String</span></span>|  
|<span data-ttu-id="0ce81-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="0ce81-287">COLUMN_SIZE</span></span>|<span data-ttu-id="0ce81-288">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-288">Int32</span></span>|  
|<span data-ttu-id="0ce81-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="0ce81-290">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-290">Int32</span></span>|  
|<span data-ttu-id="0ce81-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="0ce81-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="0ce81-292">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-292">Int16</span></span>|  
|<span data-ttu-id="0ce81-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="0ce81-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="0ce81-294">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-294">Int16</span></span>|  
|<span data-ttu-id="0ce81-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-295">NULLABLE</span></span>|<span data-ttu-id="0ce81-296">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-296">Int16</span></span>|  
|<span data-ttu-id="0ce81-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-297">REMARKS</span></span>|<span data-ttu-id="0ce81-298">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-298">String</span></span>|  
|<span data-ttu-id="0ce81-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="0ce81-299">COLUMN_DEF</span></span>|<span data-ttu-id="0ce81-300">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-300">String</span></span>|  
|<span data-ttu-id="0ce81-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="0ce81-302">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-302">Int16</span></span>|  
|<span data-ttu-id="0ce81-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="0ce81-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="0ce81-304">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-304">Int16</span></span>|  
|<span data-ttu-id="0ce81-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="0ce81-306">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-306">Int32</span></span>|  
|<span data-ttu-id="0ce81-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0ce81-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="0ce81-308">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-308">Int32</span></span>|  
|<span data-ttu-id="0ce81-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-309">IS_NULLABLE</span></span>|<span data-ttu-id="0ce81-310">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-310">String</span></span>|  
|<span data-ttu-id="0ce81-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0ce81-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="0ce81-312">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-312">String</span></span>|  
|<span data-ttu-id="0ce81-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0ce81-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="0ce81-314">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-314">String</span></span>|  
|<span data-ttu-id="0ce81-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="0ce81-316">Byte</span><span class="sxs-lookup"><span data-stu-id="0ce81-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="0ce81-317">Microsoft Oracle ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="0ce81-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="0ce81-318">Microsoft SQL Server Oracle ODBC ドライバーは、共通のスキーマ コレクションに加えて次の特定のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0ce81-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="0ce81-319">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="0ce81-319">Tables</span></span>  
  
-   <span data-ttu-id="0ce81-320">列</span><span class="sxs-lookup"><span data-stu-id="0ce81-320">Columns</span></span>  
  
-   <span data-ttu-id="0ce81-321">手順</span><span class="sxs-lookup"><span data-stu-id="0ce81-321">Procedures</span></span>  
  
-   <span data-ttu-id="0ce81-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0ce81-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="0ce81-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0ce81-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="0ce81-324">ビュー</span><span class="sxs-lookup"><span data-stu-id="0ce81-324">Views</span></span>  
  
-   <span data-ttu-id="0ce81-325">Indexes</span><span class="sxs-lookup"><span data-stu-id="0ce81-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="0ce81-326">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="0ce81-326">Tables and Views</span></span>  
  
|<span data-ttu-id="0ce81-327">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-327">ColumnName</span></span>|<span data-ttu-id="0ce81-328">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0ce81-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="0ce81-330">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-330">String</span></span>|  
|<span data-ttu-id="0ce81-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0ce81-331">TABLE_OWNER</span></span>|<span data-ttu-id="0ce81-332">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-332">String</span></span>|  
|<span data-ttu-id="0ce81-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-333">TABLE_NAME</span></span>|<span data-ttu-id="0ce81-334">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-334">String</span></span>|  
|<span data-ttu-id="0ce81-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-335">TABLE_TYPE</span></span>|<span data-ttu-id="0ce81-336">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-336">String</span></span>|  
|<span data-ttu-id="0ce81-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-337">REMARKS</span></span>|<span data-ttu-id="0ce81-338">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="0ce81-339">列</span><span class="sxs-lookup"><span data-stu-id="0ce81-339">Columns</span></span>  
  
|<span data-ttu-id="0ce81-340">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-340">ColumnName</span></span>|<span data-ttu-id="0ce81-341">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0ce81-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="0ce81-343">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-343">String</span></span>|  
|<span data-ttu-id="0ce81-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0ce81-344">TABLE_OWNER</span></span>|<span data-ttu-id="0ce81-345">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-345">String</span></span>|  
|<span data-ttu-id="0ce81-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-346">TABLE_NAME</span></span>|<span data-ttu-id="0ce81-347">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-347">String</span></span>|  
|<span data-ttu-id="0ce81-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-348">COLUMN_NAME</span></span>|<span data-ttu-id="0ce81-349">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-349">String</span></span>|  
|<span data-ttu-id="0ce81-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-350">DATA_TYPE</span></span>|<span data-ttu-id="0ce81-351">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-351">Int16</span></span>|  
|<span data-ttu-id="0ce81-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-352">TYPE_NAME</span></span>|<span data-ttu-id="0ce81-353">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-353">String</span></span>|  
|<span data-ttu-id="0ce81-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="0ce81-354">PRECISION</span></span>|<span data-ttu-id="0ce81-355">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-355">Int32</span></span>|  
|<span data-ttu-id="0ce81-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-356">LENGTH</span></span>|<span data-ttu-id="0ce81-357">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-357">Int32</span></span>|  
|<span data-ttu-id="0ce81-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="0ce81-358">SCALE</span></span>|<span data-ttu-id="0ce81-359">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-359">Int16</span></span>|  
|<span data-ttu-id="0ce81-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="0ce81-360">RADIX</span></span>|<span data-ttu-id="0ce81-361">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-361">Int16</span></span>|  
|<span data-ttu-id="0ce81-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-362">NULLABLE</span></span>|<span data-ttu-id="0ce81-363">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-363">Int16</span></span>|  
|<span data-ttu-id="0ce81-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-364">REMARKS</span></span>|<span data-ttu-id="0ce81-365">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-365">String</span></span>|  
|<span data-ttu-id="0ce81-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0ce81-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="0ce81-367">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="0ce81-368">手順</span><span class="sxs-lookup"><span data-stu-id="0ce81-368">Procedures</span></span>  
  
|<span data-ttu-id="0ce81-369">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-369">ColumnName</span></span>|<span data-ttu-id="0ce81-370">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0ce81-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="0ce81-372">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-372">String</span></span>|  
|<span data-ttu-id="0ce81-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0ce81-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="0ce81-374">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-374">String</span></span>|  
|<span data-ttu-id="0ce81-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="0ce81-376">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-376">String</span></span>|  
|<span data-ttu-id="0ce81-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0ce81-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="0ce81-378">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-378">Int16</span></span>|  
|<span data-ttu-id="0ce81-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0ce81-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="0ce81-380">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-380">Int16</span></span>|  
|<span data-ttu-id="0ce81-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="0ce81-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="0ce81-382">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-382">Int16</span></span>|  
|<span data-ttu-id="0ce81-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-383">REMARKS</span></span>|<span data-ttu-id="0ce81-384">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-384">String</span></span>|  
|<span data-ttu-id="0ce81-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="0ce81-386">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="0ce81-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0ce81-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="0ce81-388">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-388">ColumnName</span></span>|<span data-ttu-id="0ce81-389">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0ce81-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="0ce81-391">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-391">String</span></span>|  
|<span data-ttu-id="0ce81-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0ce81-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="0ce81-393">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-393">String</span></span>|  
|<span data-ttu-id="0ce81-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="0ce81-395">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-395">String</span></span>|  
|<span data-ttu-id="0ce81-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-396">COLUMN_NAME</span></span>|<span data-ttu-id="0ce81-397">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-397">String</span></span>|  
|<span data-ttu-id="0ce81-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-398">COLUMN_TYPE</span></span>|<span data-ttu-id="0ce81-399">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-399">Int16</span></span>|  
|<span data-ttu-id="0ce81-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-400">DATA_TYPE</span></span>|<span data-ttu-id="0ce81-401">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-401">Int16</span></span>|  
|<span data-ttu-id="0ce81-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-402">TYPE_NAME</span></span>|<span data-ttu-id="0ce81-403">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-403">String</span></span>|  
|<span data-ttu-id="0ce81-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="0ce81-404">PRECISION</span></span>|<span data-ttu-id="0ce81-405">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-405">Int32</span></span>|  
|<span data-ttu-id="0ce81-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-406">LENGTH</span></span>|<span data-ttu-id="0ce81-407">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-407">Int32</span></span>|  
|<span data-ttu-id="0ce81-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="0ce81-408">SCALE</span></span>|<span data-ttu-id="0ce81-409">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-409">Int16</span></span>|  
|<span data-ttu-id="0ce81-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="0ce81-410">RADIX</span></span>|<span data-ttu-id="0ce81-411">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-411">Int16</span></span>|  
|<span data-ttu-id="0ce81-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-412">NULLABLE</span></span>|<span data-ttu-id="0ce81-413">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-413">Int16</span></span>|  
|<span data-ttu-id="0ce81-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-414">REMARKS</span></span>|<span data-ttu-id="0ce81-415">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-415">String</span></span>|  
|<span data-ttu-id="0ce81-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="0ce81-416">OVERLOAD</span></span>|<span data-ttu-id="0ce81-417">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-417">Int32</span></span>|  
|<span data-ttu-id="0ce81-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0ce81-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="0ce81-419">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="0ce81-420">Microsoft Jet ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="0ce81-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="0ce81-421">Microsoft Jet ODBC Driver は、共通のスキーマ コレクションに加えて次のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0ce81-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="0ce81-422">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="0ce81-422">Tables</span></span>  
  
-   <span data-ttu-id="0ce81-423">Indexes</span><span class="sxs-lookup"><span data-stu-id="0ce81-423">Indexes</span></span>  
  
-   <span data-ttu-id="0ce81-424">列</span><span class="sxs-lookup"><span data-stu-id="0ce81-424">Columns</span></span>  
  
-   <span data-ttu-id="0ce81-425">手順</span><span class="sxs-lookup"><span data-stu-id="0ce81-425">Procedures</span></span>  
  
-   <span data-ttu-id="0ce81-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0ce81-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="0ce81-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0ce81-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="0ce81-428">ビュー</span><span class="sxs-lookup"><span data-stu-id="0ce81-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="0ce81-429">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="0ce81-429">Tables and Views</span></span>  
  
|<span data-ttu-id="0ce81-430">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-430">ColumnName</span></span>|<span data-ttu-id="0ce81-431">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0ce81-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="0ce81-433">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-433">String</span></span>|  
|<span data-ttu-id="0ce81-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0ce81-434">TABLE_OWNER</span></span>|<span data-ttu-id="0ce81-435">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-435">String</span></span>|  
|<span data-ttu-id="0ce81-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-436">TABLE_NAME</span></span>|<span data-ttu-id="0ce81-437">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-437">String</span></span>|  
|<span data-ttu-id="0ce81-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-438">TABLE_TYPE</span></span>|<span data-ttu-id="0ce81-439">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-439">String</span></span>|  
|<span data-ttu-id="0ce81-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-440">REMARKS</span></span>|<span data-ttu-id="0ce81-441">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="0ce81-442">列</span><span class="sxs-lookup"><span data-stu-id="0ce81-442">Columns</span></span>  
  
|<span data-ttu-id="0ce81-443">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-443">ColumnName</span></span>|<span data-ttu-id="0ce81-444">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0ce81-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="0ce81-446">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-446">String</span></span>|  
|<span data-ttu-id="0ce81-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0ce81-447">TABLE_OWNER</span></span>|<span data-ttu-id="0ce81-448">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-448">String</span></span>|  
|<span data-ttu-id="0ce81-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-449">TABLE_NAME</span></span>|<span data-ttu-id="0ce81-450">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-450">String</span></span>|  
|<span data-ttu-id="0ce81-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-451">COLUMN_NAME</span></span>|<span data-ttu-id="0ce81-452">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-452">String</span></span>|  
|<span data-ttu-id="0ce81-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-453">DATA_TYPE</span></span>|<span data-ttu-id="0ce81-454">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-454">Int16</span></span>|  
|<span data-ttu-id="0ce81-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-455">TYPE_NAME</span></span>|<span data-ttu-id="0ce81-456">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-456">String</span></span>|  
|<span data-ttu-id="0ce81-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="0ce81-457">PRECISION</span></span>|<span data-ttu-id="0ce81-458">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-458">Int32</span></span>|  
|<span data-ttu-id="0ce81-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-459">LENGTH</span></span>|<span data-ttu-id="0ce81-460">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-460">Int32</span></span>|  
|<span data-ttu-id="0ce81-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="0ce81-461">SCALE</span></span>|<span data-ttu-id="0ce81-462">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-462">Int16</span></span>|  
|<span data-ttu-id="0ce81-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="0ce81-463">RADIX</span></span>|<span data-ttu-id="0ce81-464">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-464">Int16</span></span>|  
|<span data-ttu-id="0ce81-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-465">NULLABLE</span></span>|<span data-ttu-id="0ce81-466">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-466">Int16</span></span>|  
|<span data-ttu-id="0ce81-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-467">REMARKS</span></span>|<span data-ttu-id="0ce81-468">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-468">String</span></span>|  
|<span data-ttu-id="0ce81-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0ce81-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="0ce81-470">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="0ce81-471">手順</span><span class="sxs-lookup"><span data-stu-id="0ce81-471">Procedures</span></span>  
  
|<span data-ttu-id="0ce81-472">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-472">ColumnName</span></span>|<span data-ttu-id="0ce81-473">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0ce81-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="0ce81-475">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-475">String</span></span>|  
|<span data-ttu-id="0ce81-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0ce81-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="0ce81-477">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-477">String</span></span>|  
|<span data-ttu-id="0ce81-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="0ce81-479">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-479">String</span></span>|  
|<span data-ttu-id="0ce81-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0ce81-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="0ce81-481">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-481">Int16</span></span>|  
|<span data-ttu-id="0ce81-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0ce81-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="0ce81-483">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-483">Int16</span></span>|  
|<span data-ttu-id="0ce81-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="0ce81-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="0ce81-485">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-485">Int16</span></span>|  
|<span data-ttu-id="0ce81-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-486">REMARKS</span></span>|<span data-ttu-id="0ce81-487">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-487">String</span></span>|  
|<span data-ttu-id="0ce81-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="0ce81-489">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="0ce81-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0ce81-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="0ce81-491">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-491">ColumnName</span></span>|<span data-ttu-id="0ce81-492">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0ce81-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="0ce81-494">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-494">String</span></span>|  
|<span data-ttu-id="0ce81-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0ce81-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="0ce81-496">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-496">String</span></span>|  
|<span data-ttu-id="0ce81-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="0ce81-498">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-498">String</span></span>|  
|<span data-ttu-id="0ce81-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-499">COLUMN_NAME</span></span>|<span data-ttu-id="0ce81-500">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-500">String</span></span>|  
|<span data-ttu-id="0ce81-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-501">COLUMN_TYPE</span></span>|<span data-ttu-id="0ce81-502">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-502">Int16</span></span>|  
|<span data-ttu-id="0ce81-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-503">DATA_TYPE</span></span>|<span data-ttu-id="0ce81-504">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-504">Int16</span></span>|  
|<span data-ttu-id="0ce81-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-505">TYPE_NAME</span></span>|<span data-ttu-id="0ce81-506">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-506">String</span></span>|  
|<span data-ttu-id="0ce81-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="0ce81-507">PRECISION</span></span>|<span data-ttu-id="0ce81-508">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-508">Int32</span></span>|  
|<span data-ttu-id="0ce81-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-509">LENGTH</span></span>|<span data-ttu-id="0ce81-510">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-510">Int32</span></span>|  
|<span data-ttu-id="0ce81-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="0ce81-511">SCALE</span></span>|<span data-ttu-id="0ce81-512">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-512">Int16</span></span>|  
|<span data-ttu-id="0ce81-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="0ce81-513">RADIX</span></span>|<span data-ttu-id="0ce81-514">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-514">Int16</span></span>|  
|<span data-ttu-id="0ce81-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-515">NULLABLE</span></span>|<span data-ttu-id="0ce81-516">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-516">Int16</span></span>|  
|<span data-ttu-id="0ce81-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-517">REMARKS</span></span>|<span data-ttu-id="0ce81-518">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-518">String</span></span>|  
|<span data-ttu-id="0ce81-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="0ce81-519">OVERLOAD</span></span>|<span data-ttu-id="0ce81-520">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-520">Int32</span></span>|  
|<span data-ttu-id="0ce81-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0ce81-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="0ce81-522">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="0ce81-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0ce81-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="0ce81-524">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ce81-524">ColumnName</span></span>|<span data-ttu-id="0ce81-525">DataType</span><span class="sxs-lookup"><span data-stu-id="0ce81-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0ce81-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="0ce81-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="0ce81-527">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-527">String</span></span>|  
|<span data-ttu-id="0ce81-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0ce81-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="0ce81-529">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-529">String</span></span>|  
|<span data-ttu-id="0ce81-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="0ce81-531">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-531">String</span></span>|  
|<span data-ttu-id="0ce81-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-532">COLUMN_NAME</span></span>|<span data-ttu-id="0ce81-533">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-533">String</span></span>|  
|<span data-ttu-id="0ce81-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-534">COLUMN_TYPE</span></span>|<span data-ttu-id="0ce81-535">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-535">Int16</span></span>|  
|<span data-ttu-id="0ce81-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-536">DATA_TYPE</span></span>|<span data-ttu-id="0ce81-537">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-537">Int16</span></span>|  
|<span data-ttu-id="0ce81-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0ce81-538">TYPE_NAME</span></span>|<span data-ttu-id="0ce81-539">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-539">String</span></span>|  
|<span data-ttu-id="0ce81-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="0ce81-540">COLUMN_SIZE</span></span>|<span data-ttu-id="0ce81-541">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-541">Int32</span></span>|  
|<span data-ttu-id="0ce81-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="0ce81-543">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-543">Int32</span></span>|  
|<span data-ttu-id="0ce81-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="0ce81-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="0ce81-545">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-545">Int16</span></span>|  
|<span data-ttu-id="0ce81-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="0ce81-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="0ce81-547">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-547">Int16</span></span>|  
|<span data-ttu-id="0ce81-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-548">NULLABLE</span></span>|<span data-ttu-id="0ce81-549">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-549">Int16</span></span>|  
|<span data-ttu-id="0ce81-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0ce81-550">REMARKS</span></span>|<span data-ttu-id="0ce81-551">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-551">String</span></span>|  
|<span data-ttu-id="0ce81-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="0ce81-552">COLUMN_DEF</span></span>|<span data-ttu-id="0ce81-553">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-553">String</span></span>|  
|<span data-ttu-id="0ce81-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0ce81-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="0ce81-555">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-555">Int16</span></span>|  
|<span data-ttu-id="0ce81-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="0ce81-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="0ce81-557">Int16</span><span class="sxs-lookup"><span data-stu-id="0ce81-557">Int16</span></span>|  
|<span data-ttu-id="0ce81-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0ce81-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="0ce81-559">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-559">Int32</span></span>|  
|<span data-ttu-id="0ce81-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0ce81-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="0ce81-561">Int32</span><span class="sxs-lookup"><span data-stu-id="0ce81-561">Int32</span></span>|  
|<span data-ttu-id="0ce81-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0ce81-562">IS_NULLABLE</span></span>|<span data-ttu-id="0ce81-563">String</span><span class="sxs-lookup"><span data-stu-id="0ce81-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0ce81-564">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ce81-564">See Also</span></span>  
 [<span data-ttu-id="0ce81-565">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="0ce81-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
