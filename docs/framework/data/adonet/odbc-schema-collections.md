---
title: ODBC スキーマ コレクション
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: bdedbb11960f02b99dcca6388abf663635238f74
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43479981"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="e4530-102">ODBC スキーマ コレクション</span><span class="sxs-lookup"><span data-stu-id="e4530-102">ODBC Schema Collections</span></span>
<span data-ttu-id="e4530-103">ここでは、Microsoft SQL Server、Oracle、および Microsoft Jet 用の各 ODBC ドライバーでのスキーマ コレクションのサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e4530-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="e4530-104">Microsoft SQL Server ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="e4530-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="e4530-105">Microsoft SQL Server ODBC Driver には、共通のスキーマ コレクションに加えて次の特定のスキーマ コレクションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e4530-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="e4530-106">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="e4530-106">Tables</span></span>  
  
-   <span data-ttu-id="e4530-107">Indexes</span><span class="sxs-lookup"><span data-stu-id="e4530-107">Indexes</span></span>  
  
-   <span data-ttu-id="e4530-108">列</span><span class="sxs-lookup"><span data-stu-id="e4530-108">Columns</span></span>  
  
-   <span data-ttu-id="e4530-109">手順</span><span class="sxs-lookup"><span data-stu-id="e4530-109">Procedures</span></span>  
  
-   <span data-ttu-id="e4530-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="e4530-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="e4530-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="e4530-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="e4530-112">ビュー</span><span class="sxs-lookup"><span data-stu-id="e4530-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="e4530-113">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="e4530-113">Tables and Views</span></span>  
  
|<span data-ttu-id="e4530-114">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-114">ColumnName</span></span>|<span data-ttu-id="e4530-115">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="e4530-116">TABLE_CAT</span></span>|<span data-ttu-id="e4530-117">String</span><span class="sxs-lookup"><span data-stu-id="e4530-117">String</span></span>|  
|<span data-ttu-id="e4530-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="e4530-118">TABLE_SCHEM</span></span>|<span data-ttu-id="e4530-119">String</span><span class="sxs-lookup"><span data-stu-id="e4530-119">String</span></span>|  
|<span data-ttu-id="e4530-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-120">TABLE_NAME</span></span>|<span data-ttu-id="e4530-121">String</span><span class="sxs-lookup"><span data-stu-id="e4530-121">String</span></span>|  
|<span data-ttu-id="e4530-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-122">TABLE_TYPE</span></span>|<span data-ttu-id="e4530-123">String</span><span class="sxs-lookup"><span data-stu-id="e4530-123">String</span></span>|  
|<span data-ttu-id="e4530-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-124">REMARKS</span></span>|<span data-ttu-id="e4530-125">String</span><span class="sxs-lookup"><span data-stu-id="e4530-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="e4530-126">Indexes</span><span class="sxs-lookup"><span data-stu-id="e4530-126">Indexes</span></span>  
  
|<span data-ttu-id="e4530-127">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-127">ColumnName</span></span>|<span data-ttu-id="e4530-128">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="e4530-129">TABLE_CAT</span></span>|<span data-ttu-id="e4530-130">String</span><span class="sxs-lookup"><span data-stu-id="e4530-130">String</span></span>|  
|<span data-ttu-id="e4530-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="e4530-131">TABLE_SCHEM</span></span>|<span data-ttu-id="e4530-132">String</span><span class="sxs-lookup"><span data-stu-id="e4530-132">String</span></span>|  
|<span data-ttu-id="e4530-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-133">TABLE_NAME</span></span>|<span data-ttu-id="e4530-134">String</span><span class="sxs-lookup"><span data-stu-id="e4530-134">String</span></span>|  
|<span data-ttu-id="e4530-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="e4530-135">NON_UNIQUE</span></span>|<span data-ttu-id="e4530-136">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-136">Int16</span></span>|  
|<span data-ttu-id="e4530-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="e4530-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="e4530-138">String</span><span class="sxs-lookup"><span data-stu-id="e4530-138">String</span></span>|  
|<span data-ttu-id="e4530-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-139">INDEX_NAME</span></span>|<span data-ttu-id="e4530-140">String</span><span class="sxs-lookup"><span data-stu-id="e4530-140">String</span></span>|  
|<span data-ttu-id="e4530-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-141">TYPE</span></span>|<span data-ttu-id="e4530-142">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-142">Int16</span></span>|  
|<span data-ttu-id="e4530-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="e4530-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="e4530-144">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-144">Int16</span></span>|  
|<span data-ttu-id="e4530-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-145">COLUMN_NAME</span></span>|<span data-ttu-id="e4530-146">String</span><span class="sxs-lookup"><span data-stu-id="e4530-146">String</span></span>|  
|<span data-ttu-id="e4530-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="e4530-147">ASC_OR_DESC</span></span>|<span data-ttu-id="e4530-148">String</span><span class="sxs-lookup"><span data-stu-id="e4530-148">String</span></span>|  
|<span data-ttu-id="e4530-149">CARDINATLITY</span><span class="sxs-lookup"><span data-stu-id="e4530-149">CARDINATLITY</span></span>|<span data-ttu-id="e4530-150">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-150">Int32</span></span>|  
|<span data-ttu-id="e4530-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="e4530-151">PAGES</span></span>|<span data-ttu-id="e4530-152">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-152">Int32</span></span>|  
|<span data-ttu-id="e4530-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="e4530-153">FILTER_CONDITION</span></span>|<span data-ttu-id="e4530-154">String</span><span class="sxs-lookup"><span data-stu-id="e4530-154">String</span></span>|  
|<span data-ttu-id="e4530-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="e4530-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="e4530-156">String</span><span class="sxs-lookup"><span data-stu-id="e4530-156">String</span></span>|  
|<span data-ttu-id="e4530-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="e4530-158">Byte</span><span class="sxs-lookup"><span data-stu-id="e4530-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="e4530-159">列</span><span class="sxs-lookup"><span data-stu-id="e4530-159">Columns</span></span>  
  
|<span data-ttu-id="e4530-160">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-160">ColumnName</span></span>|<span data-ttu-id="e4530-161">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="e4530-162">TABLE_CAT</span></span>|<span data-ttu-id="e4530-163">String</span><span class="sxs-lookup"><span data-stu-id="e4530-163">String</span></span>|  
|<span data-ttu-id="e4530-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="e4530-164">TABLE_SCHEM</span></span>|<span data-ttu-id="e4530-165">String</span><span class="sxs-lookup"><span data-stu-id="e4530-165">String</span></span>|  
|<span data-ttu-id="e4530-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-166">TABLE_NAME</span></span>|<span data-ttu-id="e4530-167">String</span><span class="sxs-lookup"><span data-stu-id="e4530-167">String</span></span>|  
|<span data-ttu-id="e4530-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-168">COLUMN_NAME</span></span>|<span data-ttu-id="e4530-169">String</span><span class="sxs-lookup"><span data-stu-id="e4530-169">String</span></span>|  
|<span data-ttu-id="e4530-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-170">DATA_TYPE</span></span>|<span data-ttu-id="e4530-171">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-171">Int16</span></span>|  
|<span data-ttu-id="e4530-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-172">TYPE_NAME</span></span>|<span data-ttu-id="e4530-173">String</span><span class="sxs-lookup"><span data-stu-id="e4530-173">String</span></span>|  
|<span data-ttu-id="e4530-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="e4530-174">COLUMN_SIZE</span></span>|<span data-ttu-id="e4530-175">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-175">Int32</span></span>|  
|<span data-ttu-id="e4530-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="e4530-177">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-177">Int32</span></span>|  
|<span data-ttu-id="e4530-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="e4530-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="e4530-179">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-179">Int16</span></span>|  
|<span data-ttu-id="e4530-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="e4530-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="e4530-181">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-181">Int16</span></span>|  
|<span data-ttu-id="e4530-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-182">NULLABLE</span></span>|<span data-ttu-id="e4530-183">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-183">Int16</span></span>|  
|<span data-ttu-id="e4530-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-184">REMARKS</span></span>|<span data-ttu-id="e4530-185">String</span><span class="sxs-lookup"><span data-stu-id="e4530-185">String</span></span>|  
|<span data-ttu-id="e4530-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="e4530-186">COLUMN_DEF</span></span>|<span data-ttu-id="e4530-187">String</span><span class="sxs-lookup"><span data-stu-id="e4530-187">String</span></span>|  
|<span data-ttu-id="e4530-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="e4530-189">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-189">Int16</span></span>|  
|<span data-ttu-id="e4530-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="e4530-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="e4530-191">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-191">Int16</span></span>|  
|<span data-ttu-id="e4530-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="e4530-193">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-193">Int32</span></span>|  
|<span data-ttu-id="e4530-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="e4530-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="e4530-195">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-195">Int32</span></span>|  
|<span data-ttu-id="e4530-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-196">IS_NULLABLE</span></span>|<span data-ttu-id="e4530-197">String</span><span class="sxs-lookup"><span data-stu-id="e4530-197">String</span></span>|  
|<span data-ttu-id="e4530-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="e4530-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="e4530-199">String</span><span class="sxs-lookup"><span data-stu-id="e4530-199">String</span></span>|  
|<span data-ttu-id="e4530-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="e4530-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="e4530-201">String</span><span class="sxs-lookup"><span data-stu-id="e4530-201">String</span></span>|  
|<span data-ttu-id="e4530-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="e4530-203">Byte</span><span class="sxs-lookup"><span data-stu-id="e4530-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="e4530-204">手順</span><span class="sxs-lookup"><span data-stu-id="e4530-204">Procedures</span></span>  
  
|<span data-ttu-id="e4530-205">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-205">ColumnName</span></span>|<span data-ttu-id="e4530-206">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="e4530-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="e4530-208">String</span><span class="sxs-lookup"><span data-stu-id="e4530-208">String</span></span>|  
|<span data-ttu-id="e4530-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="e4530-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="e4530-210">String</span><span class="sxs-lookup"><span data-stu-id="e4530-210">String</span></span>|  
|<span data-ttu-id="e4530-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="e4530-212">String</span><span class="sxs-lookup"><span data-stu-id="e4530-212">String</span></span>|  
|<span data-ttu-id="e4530-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="e4530-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="e4530-214">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-214">Int32</span></span>|  
|<span data-ttu-id="e4530-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="e4530-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="e4530-216">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-216">Int32</span></span>|  
|<span data-ttu-id="e4530-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="e4530-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="e4530-218">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-218">Int32</span></span>|  
|<span data-ttu-id="e4530-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-219">REMARKS</span></span>|<span data-ttu-id="e4530-220">String</span><span class="sxs-lookup"><span data-stu-id="e4530-220">String</span></span>|  
|<span data-ttu-id="e4530-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="e4530-222">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="e4530-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="e4530-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="e4530-224">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-224">ColumnName</span></span>|<span data-ttu-id="e4530-225">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="e4530-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="e4530-227">String</span><span class="sxs-lookup"><span data-stu-id="e4530-227">String</span></span>|  
|<span data-ttu-id="e4530-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="e4530-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="e4530-229">String</span><span class="sxs-lookup"><span data-stu-id="e4530-229">String</span></span>|  
|<span data-ttu-id="e4530-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="e4530-231">String</span><span class="sxs-lookup"><span data-stu-id="e4530-231">String</span></span>|  
|<span data-ttu-id="e4530-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-232">COLUMN_NAME</span></span>|<span data-ttu-id="e4530-233">String</span><span class="sxs-lookup"><span data-stu-id="e4530-233">String</span></span>|  
|<span data-ttu-id="e4530-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-234">COLUMN_TYPE</span></span>|<span data-ttu-id="e4530-235">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-235">Int16</span></span>|  
|<span data-ttu-id="e4530-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-236">DATA_TYPE</span></span>|<span data-ttu-id="e4530-237">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-237">Int16</span></span>|  
|<span data-ttu-id="e4530-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-238">TYPE_NAME</span></span>|<span data-ttu-id="e4530-239">String</span><span class="sxs-lookup"><span data-stu-id="e4530-239">String</span></span>|  
|<span data-ttu-id="e4530-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="e4530-240">COLUMN_SIZE</span></span>|<span data-ttu-id="e4530-241">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-241">Int32</span></span>|  
|<span data-ttu-id="e4530-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="e4530-243">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-243">Int32</span></span>|  
|<span data-ttu-id="e4530-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="e4530-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="e4530-245">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-245">Int16</span></span>|  
|<span data-ttu-id="e4530-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="e4530-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="e4530-247">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-247">Int16</span></span>|  
|<span data-ttu-id="e4530-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-248">NULLABLE</span></span>|<span data-ttu-id="e4530-249">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-249">Int16</span></span>|  
|<span data-ttu-id="e4530-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-250">REMARKS</span></span>|<span data-ttu-id="e4530-251">String</span><span class="sxs-lookup"><span data-stu-id="e4530-251">String</span></span>|  
|<span data-ttu-id="e4530-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="e4530-252">COLUMN_DEF</span></span>|<span data-ttu-id="e4530-253">String</span><span class="sxs-lookup"><span data-stu-id="e4530-253">String</span></span>|  
|<span data-ttu-id="e4530-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="e4530-255">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-255">Int16</span></span>|  
|<span data-ttu-id="e4530-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="e4530-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="e4530-257">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-257">Int16</span></span>|  
|<span data-ttu-id="e4530-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="e4530-259">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-259">Int32</span></span>|  
|<span data-ttu-id="e4530-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="e4530-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="e4530-261">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-261">Int32</span></span>|  
|<span data-ttu-id="e4530-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-262">IS_NULLABLE</span></span>|<span data-ttu-id="e4530-263">String</span><span class="sxs-lookup"><span data-stu-id="e4530-263">String</span></span>|  
|<span data-ttu-id="e4530-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="e4530-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="e4530-265">String</span><span class="sxs-lookup"><span data-stu-id="e4530-265">String</span></span>|  
|<span data-ttu-id="e4530-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="e4530-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="e4530-267">String</span><span class="sxs-lookup"><span data-stu-id="e4530-267">String</span></span>|  
|<span data-ttu-id="e4530-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="e4530-269">Byte</span><span class="sxs-lookup"><span data-stu-id="e4530-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="e4530-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="e4530-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="e4530-271">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-271">ColumnName</span></span>|<span data-ttu-id="e4530-272">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="e4530-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="e4530-274">String</span><span class="sxs-lookup"><span data-stu-id="e4530-274">String</span></span>|  
|<span data-ttu-id="e4530-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="e4530-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="e4530-276">String</span><span class="sxs-lookup"><span data-stu-id="e4530-276">String</span></span>|  
|<span data-ttu-id="e4530-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="e4530-278">String</span><span class="sxs-lookup"><span data-stu-id="e4530-278">String</span></span>|  
|<span data-ttu-id="e4530-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-279">COLUMN_NAME</span></span>|<span data-ttu-id="e4530-280">String</span><span class="sxs-lookup"><span data-stu-id="e4530-280">String</span></span>|  
|<span data-ttu-id="e4530-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-281">COLUMN_TYPE</span></span>|<span data-ttu-id="e4530-282">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-282">Int16</span></span>|  
|<span data-ttu-id="e4530-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-283">DATA_TYPE</span></span>|<span data-ttu-id="e4530-284">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-284">Int16</span></span>|  
|<span data-ttu-id="e4530-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-285">TYPE_NAME</span></span>|<span data-ttu-id="e4530-286">String</span><span class="sxs-lookup"><span data-stu-id="e4530-286">String</span></span>|  
|<span data-ttu-id="e4530-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="e4530-287">COLUMN_SIZE</span></span>|<span data-ttu-id="e4530-288">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-288">Int32</span></span>|  
|<span data-ttu-id="e4530-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="e4530-290">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-290">Int32</span></span>|  
|<span data-ttu-id="e4530-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="e4530-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="e4530-292">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-292">Int16</span></span>|  
|<span data-ttu-id="e4530-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="e4530-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="e4530-294">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-294">Int16</span></span>|  
|<span data-ttu-id="e4530-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-295">NULLABLE</span></span>|<span data-ttu-id="e4530-296">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-296">Int16</span></span>|  
|<span data-ttu-id="e4530-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-297">REMARKS</span></span>|<span data-ttu-id="e4530-298">String</span><span class="sxs-lookup"><span data-stu-id="e4530-298">String</span></span>|  
|<span data-ttu-id="e4530-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="e4530-299">COLUMN_DEF</span></span>|<span data-ttu-id="e4530-300">String</span><span class="sxs-lookup"><span data-stu-id="e4530-300">String</span></span>|  
|<span data-ttu-id="e4530-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="e4530-302">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-302">Int16</span></span>|  
|<span data-ttu-id="e4530-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="e4530-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="e4530-304">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-304">Int16</span></span>|  
|<span data-ttu-id="e4530-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="e4530-306">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-306">Int32</span></span>|  
|<span data-ttu-id="e4530-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="e4530-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="e4530-308">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-308">Int32</span></span>|  
|<span data-ttu-id="e4530-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-309">IS_NULLABLE</span></span>|<span data-ttu-id="e4530-310">String</span><span class="sxs-lookup"><span data-stu-id="e4530-310">String</span></span>|  
|<span data-ttu-id="e4530-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="e4530-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="e4530-312">String</span><span class="sxs-lookup"><span data-stu-id="e4530-312">String</span></span>|  
|<span data-ttu-id="e4530-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="e4530-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="e4530-314">String</span><span class="sxs-lookup"><span data-stu-id="e4530-314">String</span></span>|  
|<span data-ttu-id="e4530-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="e4530-316">Byte</span><span class="sxs-lookup"><span data-stu-id="e4530-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="e4530-317">Microsoft Oracle ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="e4530-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="e4530-318">Microsoft SQL Server Oracle ODBC ドライバーは、共通のスキーマ コレクションに加えて次の特定のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e4530-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="e4530-319">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="e4530-319">Tables</span></span>  
  
-   <span data-ttu-id="e4530-320">列</span><span class="sxs-lookup"><span data-stu-id="e4530-320">Columns</span></span>  
  
-   <span data-ttu-id="e4530-321">手順</span><span class="sxs-lookup"><span data-stu-id="e4530-321">Procedures</span></span>  
  
-   <span data-ttu-id="e4530-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="e4530-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="e4530-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="e4530-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="e4530-324">ビュー</span><span class="sxs-lookup"><span data-stu-id="e4530-324">Views</span></span>  
  
-   <span data-ttu-id="e4530-325">Indexes</span><span class="sxs-lookup"><span data-stu-id="e4530-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="e4530-326">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="e4530-326">Tables and Views</span></span>  
  
|<span data-ttu-id="e4530-327">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-327">ColumnName</span></span>|<span data-ttu-id="e4530-328">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="e4530-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="e4530-330">String</span><span class="sxs-lookup"><span data-stu-id="e4530-330">String</span></span>|  
|<span data-ttu-id="e4530-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="e4530-331">TABLE_OWNER</span></span>|<span data-ttu-id="e4530-332">String</span><span class="sxs-lookup"><span data-stu-id="e4530-332">String</span></span>|  
|<span data-ttu-id="e4530-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-333">TABLE_NAME</span></span>|<span data-ttu-id="e4530-334">String</span><span class="sxs-lookup"><span data-stu-id="e4530-334">String</span></span>|  
|<span data-ttu-id="e4530-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-335">TABLE_TYPE</span></span>|<span data-ttu-id="e4530-336">String</span><span class="sxs-lookup"><span data-stu-id="e4530-336">String</span></span>|  
|<span data-ttu-id="e4530-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-337">REMARKS</span></span>|<span data-ttu-id="e4530-338">String</span><span class="sxs-lookup"><span data-stu-id="e4530-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="e4530-339">列</span><span class="sxs-lookup"><span data-stu-id="e4530-339">Columns</span></span>  
  
|<span data-ttu-id="e4530-340">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-340">ColumnName</span></span>|<span data-ttu-id="e4530-341">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="e4530-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="e4530-343">String</span><span class="sxs-lookup"><span data-stu-id="e4530-343">String</span></span>|  
|<span data-ttu-id="e4530-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="e4530-344">TABLE_OWNER</span></span>|<span data-ttu-id="e4530-345">String</span><span class="sxs-lookup"><span data-stu-id="e4530-345">String</span></span>|  
|<span data-ttu-id="e4530-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-346">TABLE_NAME</span></span>|<span data-ttu-id="e4530-347">String</span><span class="sxs-lookup"><span data-stu-id="e4530-347">String</span></span>|  
|<span data-ttu-id="e4530-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-348">COLUMN_NAME</span></span>|<span data-ttu-id="e4530-349">String</span><span class="sxs-lookup"><span data-stu-id="e4530-349">String</span></span>|  
|<span data-ttu-id="e4530-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-350">DATA_TYPE</span></span>|<span data-ttu-id="e4530-351">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-351">Int16</span></span>|  
|<span data-ttu-id="e4530-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-352">TYPE_NAME</span></span>|<span data-ttu-id="e4530-353">String</span><span class="sxs-lookup"><span data-stu-id="e4530-353">String</span></span>|  
|<span data-ttu-id="e4530-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="e4530-354">PRECISION</span></span>|<span data-ttu-id="e4530-355">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-355">Int32</span></span>|  
|<span data-ttu-id="e4530-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-356">LENGTH</span></span>|<span data-ttu-id="e4530-357">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-357">Int32</span></span>|  
|<span data-ttu-id="e4530-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="e4530-358">SCALE</span></span>|<span data-ttu-id="e4530-359">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-359">Int16</span></span>|  
|<span data-ttu-id="e4530-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="e4530-360">RADIX</span></span>|<span data-ttu-id="e4530-361">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-361">Int16</span></span>|  
|<span data-ttu-id="e4530-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-362">NULLABLE</span></span>|<span data-ttu-id="e4530-363">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-363">Int16</span></span>|  
|<span data-ttu-id="e4530-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-364">REMARKS</span></span>|<span data-ttu-id="e4530-365">String</span><span class="sxs-lookup"><span data-stu-id="e4530-365">String</span></span>|  
|<span data-ttu-id="e4530-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="e4530-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="e4530-367">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="e4530-368">手順</span><span class="sxs-lookup"><span data-stu-id="e4530-368">Procedures</span></span>  
  
|<span data-ttu-id="e4530-369">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-369">ColumnName</span></span>|<span data-ttu-id="e4530-370">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="e4530-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="e4530-372">String</span><span class="sxs-lookup"><span data-stu-id="e4530-372">String</span></span>|  
|<span data-ttu-id="e4530-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="e4530-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="e4530-374">String</span><span class="sxs-lookup"><span data-stu-id="e4530-374">String</span></span>|  
|<span data-ttu-id="e4530-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="e4530-376">String</span><span class="sxs-lookup"><span data-stu-id="e4530-376">String</span></span>|  
|<span data-ttu-id="e4530-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="e4530-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="e4530-378">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-378">Int16</span></span>|  
|<span data-ttu-id="e4530-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="e4530-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="e4530-380">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-380">Int16</span></span>|  
|<span data-ttu-id="e4530-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="e4530-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="e4530-382">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-382">Int16</span></span>|  
|<span data-ttu-id="e4530-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-383">REMARKS</span></span>|<span data-ttu-id="e4530-384">String</span><span class="sxs-lookup"><span data-stu-id="e4530-384">String</span></span>|  
|<span data-ttu-id="e4530-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="e4530-386">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="e4530-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="e4530-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="e4530-388">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-388">ColumnName</span></span>|<span data-ttu-id="e4530-389">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="e4530-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="e4530-391">String</span><span class="sxs-lookup"><span data-stu-id="e4530-391">String</span></span>|  
|<span data-ttu-id="e4530-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="e4530-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="e4530-393">String</span><span class="sxs-lookup"><span data-stu-id="e4530-393">String</span></span>|  
|<span data-ttu-id="e4530-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="e4530-395">String</span><span class="sxs-lookup"><span data-stu-id="e4530-395">String</span></span>|  
|<span data-ttu-id="e4530-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-396">COLUMN_NAME</span></span>|<span data-ttu-id="e4530-397">String</span><span class="sxs-lookup"><span data-stu-id="e4530-397">String</span></span>|  
|<span data-ttu-id="e4530-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-398">COLUMN_TYPE</span></span>|<span data-ttu-id="e4530-399">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-399">Int16</span></span>|  
|<span data-ttu-id="e4530-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-400">DATA_TYPE</span></span>|<span data-ttu-id="e4530-401">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-401">Int16</span></span>|  
|<span data-ttu-id="e4530-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-402">TYPE_NAME</span></span>|<span data-ttu-id="e4530-403">String</span><span class="sxs-lookup"><span data-stu-id="e4530-403">String</span></span>|  
|<span data-ttu-id="e4530-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="e4530-404">PRECISION</span></span>|<span data-ttu-id="e4530-405">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-405">Int32</span></span>|  
|<span data-ttu-id="e4530-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-406">LENGTH</span></span>|<span data-ttu-id="e4530-407">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-407">Int32</span></span>|  
|<span data-ttu-id="e4530-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="e4530-408">SCALE</span></span>|<span data-ttu-id="e4530-409">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-409">Int16</span></span>|  
|<span data-ttu-id="e4530-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="e4530-410">RADIX</span></span>|<span data-ttu-id="e4530-411">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-411">Int16</span></span>|  
|<span data-ttu-id="e4530-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-412">NULLABLE</span></span>|<span data-ttu-id="e4530-413">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-413">Int16</span></span>|  
|<span data-ttu-id="e4530-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-414">REMARKS</span></span>|<span data-ttu-id="e4530-415">String</span><span class="sxs-lookup"><span data-stu-id="e4530-415">String</span></span>|  
|<span data-ttu-id="e4530-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="e4530-416">OVERLOAD</span></span>|<span data-ttu-id="e4530-417">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-417">Int32</span></span>|  
|<span data-ttu-id="e4530-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="e4530-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="e4530-419">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="e4530-420">Microsoft Jet ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="e4530-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="e4530-421">Microsoft Jet ODBC Driver は、共通のスキーマ コレクションに加えて次のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e4530-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="e4530-422">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="e4530-422">Tables</span></span>  
  
-   <span data-ttu-id="e4530-423">Indexes</span><span class="sxs-lookup"><span data-stu-id="e4530-423">Indexes</span></span>  
  
-   <span data-ttu-id="e4530-424">列</span><span class="sxs-lookup"><span data-stu-id="e4530-424">Columns</span></span>  
  
-   <span data-ttu-id="e4530-425">手順</span><span class="sxs-lookup"><span data-stu-id="e4530-425">Procedures</span></span>  
  
-   <span data-ttu-id="e4530-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="e4530-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="e4530-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="e4530-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="e4530-428">ビュー</span><span class="sxs-lookup"><span data-stu-id="e4530-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="e4530-429">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="e4530-429">Tables and Views</span></span>  
  
|<span data-ttu-id="e4530-430">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-430">ColumnName</span></span>|<span data-ttu-id="e4530-431">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="e4530-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="e4530-433">String</span><span class="sxs-lookup"><span data-stu-id="e4530-433">String</span></span>|  
|<span data-ttu-id="e4530-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="e4530-434">TABLE_OWNER</span></span>|<span data-ttu-id="e4530-435">String</span><span class="sxs-lookup"><span data-stu-id="e4530-435">String</span></span>|  
|<span data-ttu-id="e4530-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-436">TABLE_NAME</span></span>|<span data-ttu-id="e4530-437">String</span><span class="sxs-lookup"><span data-stu-id="e4530-437">String</span></span>|  
|<span data-ttu-id="e4530-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-438">TABLE_TYPE</span></span>|<span data-ttu-id="e4530-439">String</span><span class="sxs-lookup"><span data-stu-id="e4530-439">String</span></span>|  
|<span data-ttu-id="e4530-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-440">REMARKS</span></span>|<span data-ttu-id="e4530-441">String</span><span class="sxs-lookup"><span data-stu-id="e4530-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="e4530-442">列</span><span class="sxs-lookup"><span data-stu-id="e4530-442">Columns</span></span>  
  
|<span data-ttu-id="e4530-443">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-443">ColumnName</span></span>|<span data-ttu-id="e4530-444">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="e4530-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="e4530-446">String</span><span class="sxs-lookup"><span data-stu-id="e4530-446">String</span></span>|  
|<span data-ttu-id="e4530-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="e4530-447">TABLE_OWNER</span></span>|<span data-ttu-id="e4530-448">String</span><span class="sxs-lookup"><span data-stu-id="e4530-448">String</span></span>|  
|<span data-ttu-id="e4530-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-449">TABLE_NAME</span></span>|<span data-ttu-id="e4530-450">String</span><span class="sxs-lookup"><span data-stu-id="e4530-450">String</span></span>|  
|<span data-ttu-id="e4530-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-451">COLUMN_NAME</span></span>|<span data-ttu-id="e4530-452">String</span><span class="sxs-lookup"><span data-stu-id="e4530-452">String</span></span>|  
|<span data-ttu-id="e4530-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-453">DATA_TYPE</span></span>|<span data-ttu-id="e4530-454">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-454">Int16</span></span>|  
|<span data-ttu-id="e4530-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-455">TYPE_NAME</span></span>|<span data-ttu-id="e4530-456">String</span><span class="sxs-lookup"><span data-stu-id="e4530-456">String</span></span>|  
|<span data-ttu-id="e4530-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="e4530-457">PRECISION</span></span>|<span data-ttu-id="e4530-458">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-458">Int32</span></span>|  
|<span data-ttu-id="e4530-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-459">LENGTH</span></span>|<span data-ttu-id="e4530-460">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-460">Int32</span></span>|  
|<span data-ttu-id="e4530-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="e4530-461">SCALE</span></span>|<span data-ttu-id="e4530-462">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-462">Int16</span></span>|  
|<span data-ttu-id="e4530-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="e4530-463">RADIX</span></span>|<span data-ttu-id="e4530-464">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-464">Int16</span></span>|  
|<span data-ttu-id="e4530-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-465">NULLABLE</span></span>|<span data-ttu-id="e4530-466">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-466">Int16</span></span>|  
|<span data-ttu-id="e4530-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-467">REMARKS</span></span>|<span data-ttu-id="e4530-468">String</span><span class="sxs-lookup"><span data-stu-id="e4530-468">String</span></span>|  
|<span data-ttu-id="e4530-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="e4530-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="e4530-470">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="e4530-471">手順</span><span class="sxs-lookup"><span data-stu-id="e4530-471">Procedures</span></span>  
  
|<span data-ttu-id="e4530-472">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-472">ColumnName</span></span>|<span data-ttu-id="e4530-473">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="e4530-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="e4530-475">String</span><span class="sxs-lookup"><span data-stu-id="e4530-475">String</span></span>|  
|<span data-ttu-id="e4530-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="e4530-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="e4530-477">String</span><span class="sxs-lookup"><span data-stu-id="e4530-477">String</span></span>|  
|<span data-ttu-id="e4530-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="e4530-479">String</span><span class="sxs-lookup"><span data-stu-id="e4530-479">String</span></span>|  
|<span data-ttu-id="e4530-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="e4530-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="e4530-481">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-481">Int16</span></span>|  
|<span data-ttu-id="e4530-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="e4530-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="e4530-483">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-483">Int16</span></span>|  
|<span data-ttu-id="e4530-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="e4530-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="e4530-485">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-485">Int16</span></span>|  
|<span data-ttu-id="e4530-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-486">REMARKS</span></span>|<span data-ttu-id="e4530-487">String</span><span class="sxs-lookup"><span data-stu-id="e4530-487">String</span></span>|  
|<span data-ttu-id="e4530-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="e4530-489">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="e4530-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="e4530-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="e4530-491">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-491">ColumnName</span></span>|<span data-ttu-id="e4530-492">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="e4530-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="e4530-494">String</span><span class="sxs-lookup"><span data-stu-id="e4530-494">String</span></span>|  
|<span data-ttu-id="e4530-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="e4530-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="e4530-496">String</span><span class="sxs-lookup"><span data-stu-id="e4530-496">String</span></span>|  
|<span data-ttu-id="e4530-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="e4530-498">String</span><span class="sxs-lookup"><span data-stu-id="e4530-498">String</span></span>|  
|<span data-ttu-id="e4530-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-499">COLUMN_NAME</span></span>|<span data-ttu-id="e4530-500">String</span><span class="sxs-lookup"><span data-stu-id="e4530-500">String</span></span>|  
|<span data-ttu-id="e4530-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-501">COLUMN_TYPE</span></span>|<span data-ttu-id="e4530-502">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-502">Int16</span></span>|  
|<span data-ttu-id="e4530-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-503">DATA_TYPE</span></span>|<span data-ttu-id="e4530-504">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-504">Int16</span></span>|  
|<span data-ttu-id="e4530-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-505">TYPE_NAME</span></span>|<span data-ttu-id="e4530-506">String</span><span class="sxs-lookup"><span data-stu-id="e4530-506">String</span></span>|  
|<span data-ttu-id="e4530-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="e4530-507">PRECISION</span></span>|<span data-ttu-id="e4530-508">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-508">Int32</span></span>|  
|<span data-ttu-id="e4530-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-509">LENGTH</span></span>|<span data-ttu-id="e4530-510">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-510">Int32</span></span>|  
|<span data-ttu-id="e4530-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="e4530-511">SCALE</span></span>|<span data-ttu-id="e4530-512">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-512">Int16</span></span>|  
|<span data-ttu-id="e4530-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="e4530-513">RADIX</span></span>|<span data-ttu-id="e4530-514">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-514">Int16</span></span>|  
|<span data-ttu-id="e4530-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-515">NULLABLE</span></span>|<span data-ttu-id="e4530-516">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-516">Int16</span></span>|  
|<span data-ttu-id="e4530-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-517">REMARKS</span></span>|<span data-ttu-id="e4530-518">String</span><span class="sxs-lookup"><span data-stu-id="e4530-518">String</span></span>|  
|<span data-ttu-id="e4530-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="e4530-519">OVERLOAD</span></span>|<span data-ttu-id="e4530-520">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-520">Int32</span></span>|  
|<span data-ttu-id="e4530-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="e4530-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="e4530-522">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="e4530-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="e4530-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="e4530-524">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4530-524">ColumnName</span></span>|<span data-ttu-id="e4530-525">DataType</span><span class="sxs-lookup"><span data-stu-id="e4530-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="e4530-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="e4530-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="e4530-527">String</span><span class="sxs-lookup"><span data-stu-id="e4530-527">String</span></span>|  
|<span data-ttu-id="e4530-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="e4530-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="e4530-529">String</span><span class="sxs-lookup"><span data-stu-id="e4530-529">String</span></span>|  
|<span data-ttu-id="e4530-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="e4530-531">String</span><span class="sxs-lookup"><span data-stu-id="e4530-531">String</span></span>|  
|<span data-ttu-id="e4530-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-532">COLUMN_NAME</span></span>|<span data-ttu-id="e4530-533">String</span><span class="sxs-lookup"><span data-stu-id="e4530-533">String</span></span>|  
|<span data-ttu-id="e4530-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-534">COLUMN_TYPE</span></span>|<span data-ttu-id="e4530-535">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-535">Int16</span></span>|  
|<span data-ttu-id="e4530-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-536">DATA_TYPE</span></span>|<span data-ttu-id="e4530-537">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-537">Int16</span></span>|  
|<span data-ttu-id="e4530-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="e4530-538">TYPE_NAME</span></span>|<span data-ttu-id="e4530-539">String</span><span class="sxs-lookup"><span data-stu-id="e4530-539">String</span></span>|  
|<span data-ttu-id="e4530-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="e4530-540">COLUMN_SIZE</span></span>|<span data-ttu-id="e4530-541">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-541">Int32</span></span>|  
|<span data-ttu-id="e4530-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="e4530-543">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-543">Int32</span></span>|  
|<span data-ttu-id="e4530-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="e4530-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="e4530-545">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-545">Int16</span></span>|  
|<span data-ttu-id="e4530-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="e4530-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="e4530-547">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-547">Int16</span></span>|  
|<span data-ttu-id="e4530-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-548">NULLABLE</span></span>|<span data-ttu-id="e4530-549">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-549">Int16</span></span>|  
|<span data-ttu-id="e4530-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="e4530-550">REMARKS</span></span>|<span data-ttu-id="e4530-551">String</span><span class="sxs-lookup"><span data-stu-id="e4530-551">String</span></span>|  
|<span data-ttu-id="e4530-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="e4530-552">COLUMN_DEF</span></span>|<span data-ttu-id="e4530-553">String</span><span class="sxs-lookup"><span data-stu-id="e4530-553">String</span></span>|  
|<span data-ttu-id="e4530-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4530-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="e4530-555">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-555">Int16</span></span>|  
|<span data-ttu-id="e4530-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="e4530-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="e4530-557">Int16</span><span class="sxs-lookup"><span data-stu-id="e4530-557">Int16</span></span>|  
|<span data-ttu-id="e4530-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="e4530-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="e4530-559">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-559">Int32</span></span>|  
|<span data-ttu-id="e4530-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="e4530-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="e4530-561">Int32</span><span class="sxs-lookup"><span data-stu-id="e4530-561">Int32</span></span>|  
|<span data-ttu-id="e4530-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="e4530-562">IS_NULLABLE</span></span>|<span data-ttu-id="e4530-563">String</span><span class="sxs-lookup"><span data-stu-id="e4530-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e4530-564">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4530-564">See Also</span></span>  
 [<span data-ttu-id="e4530-565">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="e4530-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
