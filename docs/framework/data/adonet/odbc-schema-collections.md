---
title: ODBC スキーマ コレクション
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: bdedbb11960f02b99dcca6388abf663635238f74
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43877532"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="5637d-102">ODBC スキーマ コレクション</span><span class="sxs-lookup"><span data-stu-id="5637d-102">ODBC Schema Collections</span></span>
<span data-ttu-id="5637d-103">ここでは、Microsoft SQL Server、Oracle、および Microsoft Jet 用の各 ODBC ドライバーでのスキーマ コレクションのサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5637d-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="5637d-104">Microsoft SQL Server ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="5637d-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="5637d-105">Microsoft SQL Server ODBC Driver には、共通のスキーマ コレクションに加えて次の特定のスキーマ コレクションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5637d-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="5637d-106">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="5637d-106">Tables</span></span>  
  
-   <span data-ttu-id="5637d-107">Indexes</span><span class="sxs-lookup"><span data-stu-id="5637d-107">Indexes</span></span>  
  
-   <span data-ttu-id="5637d-108">列</span><span class="sxs-lookup"><span data-stu-id="5637d-108">Columns</span></span>  
  
-   <span data-ttu-id="5637d-109">手順</span><span class="sxs-lookup"><span data-stu-id="5637d-109">Procedures</span></span>  
  
-   <span data-ttu-id="5637d-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5637d-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="5637d-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="5637d-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="5637d-112">ビュー</span><span class="sxs-lookup"><span data-stu-id="5637d-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="5637d-113">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="5637d-113">Tables and Views</span></span>  
  
|<span data-ttu-id="5637d-114">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-114">ColumnName</span></span>|<span data-ttu-id="5637d-115">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="5637d-116">TABLE_CAT</span></span>|<span data-ttu-id="5637d-117">String</span><span class="sxs-lookup"><span data-stu-id="5637d-117">String</span></span>|  
|<span data-ttu-id="5637d-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5637d-118">TABLE_SCHEM</span></span>|<span data-ttu-id="5637d-119">String</span><span class="sxs-lookup"><span data-stu-id="5637d-119">String</span></span>|  
|<span data-ttu-id="5637d-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-120">TABLE_NAME</span></span>|<span data-ttu-id="5637d-121">String</span><span class="sxs-lookup"><span data-stu-id="5637d-121">String</span></span>|  
|<span data-ttu-id="5637d-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-122">TABLE_TYPE</span></span>|<span data-ttu-id="5637d-123">String</span><span class="sxs-lookup"><span data-stu-id="5637d-123">String</span></span>|  
|<span data-ttu-id="5637d-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-124">REMARKS</span></span>|<span data-ttu-id="5637d-125">String</span><span class="sxs-lookup"><span data-stu-id="5637d-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="5637d-126">Indexes</span><span class="sxs-lookup"><span data-stu-id="5637d-126">Indexes</span></span>  
  
|<span data-ttu-id="5637d-127">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-127">ColumnName</span></span>|<span data-ttu-id="5637d-128">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="5637d-129">TABLE_CAT</span></span>|<span data-ttu-id="5637d-130">String</span><span class="sxs-lookup"><span data-stu-id="5637d-130">String</span></span>|  
|<span data-ttu-id="5637d-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5637d-131">TABLE_SCHEM</span></span>|<span data-ttu-id="5637d-132">String</span><span class="sxs-lookup"><span data-stu-id="5637d-132">String</span></span>|  
|<span data-ttu-id="5637d-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-133">TABLE_NAME</span></span>|<span data-ttu-id="5637d-134">String</span><span class="sxs-lookup"><span data-stu-id="5637d-134">String</span></span>|  
|<span data-ttu-id="5637d-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="5637d-135">NON_UNIQUE</span></span>|<span data-ttu-id="5637d-136">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-136">Int16</span></span>|  
|<span data-ttu-id="5637d-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5637d-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="5637d-138">String</span><span class="sxs-lookup"><span data-stu-id="5637d-138">String</span></span>|  
|<span data-ttu-id="5637d-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-139">INDEX_NAME</span></span>|<span data-ttu-id="5637d-140">String</span><span class="sxs-lookup"><span data-stu-id="5637d-140">String</span></span>|  
|<span data-ttu-id="5637d-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-141">TYPE</span></span>|<span data-ttu-id="5637d-142">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-142">Int16</span></span>|  
|<span data-ttu-id="5637d-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5637d-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="5637d-144">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-144">Int16</span></span>|  
|<span data-ttu-id="5637d-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-145">COLUMN_NAME</span></span>|<span data-ttu-id="5637d-146">String</span><span class="sxs-lookup"><span data-stu-id="5637d-146">String</span></span>|  
|<span data-ttu-id="5637d-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="5637d-147">ASC_OR_DESC</span></span>|<span data-ttu-id="5637d-148">String</span><span class="sxs-lookup"><span data-stu-id="5637d-148">String</span></span>|  
|<span data-ttu-id="5637d-149">CARDINATLITY</span><span class="sxs-lookup"><span data-stu-id="5637d-149">CARDINATLITY</span></span>|<span data-ttu-id="5637d-150">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-150">Int32</span></span>|  
|<span data-ttu-id="5637d-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="5637d-151">PAGES</span></span>|<span data-ttu-id="5637d-152">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-152">Int32</span></span>|  
|<span data-ttu-id="5637d-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="5637d-153">FILTER_CONDITION</span></span>|<span data-ttu-id="5637d-154">String</span><span class="sxs-lookup"><span data-stu-id="5637d-154">String</span></span>|  
|<span data-ttu-id="5637d-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5637d-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="5637d-156">String</span><span class="sxs-lookup"><span data-stu-id="5637d-156">String</span></span>|  
|<span data-ttu-id="5637d-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="5637d-158">Byte</span><span class="sxs-lookup"><span data-stu-id="5637d-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="5637d-159">列</span><span class="sxs-lookup"><span data-stu-id="5637d-159">Columns</span></span>  
  
|<span data-ttu-id="5637d-160">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-160">ColumnName</span></span>|<span data-ttu-id="5637d-161">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="5637d-162">TABLE_CAT</span></span>|<span data-ttu-id="5637d-163">String</span><span class="sxs-lookup"><span data-stu-id="5637d-163">String</span></span>|  
|<span data-ttu-id="5637d-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5637d-164">TABLE_SCHEM</span></span>|<span data-ttu-id="5637d-165">String</span><span class="sxs-lookup"><span data-stu-id="5637d-165">String</span></span>|  
|<span data-ttu-id="5637d-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-166">TABLE_NAME</span></span>|<span data-ttu-id="5637d-167">String</span><span class="sxs-lookup"><span data-stu-id="5637d-167">String</span></span>|  
|<span data-ttu-id="5637d-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-168">COLUMN_NAME</span></span>|<span data-ttu-id="5637d-169">String</span><span class="sxs-lookup"><span data-stu-id="5637d-169">String</span></span>|  
|<span data-ttu-id="5637d-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-170">DATA_TYPE</span></span>|<span data-ttu-id="5637d-171">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-171">Int16</span></span>|  
|<span data-ttu-id="5637d-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-172">TYPE_NAME</span></span>|<span data-ttu-id="5637d-173">String</span><span class="sxs-lookup"><span data-stu-id="5637d-173">String</span></span>|  
|<span data-ttu-id="5637d-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="5637d-174">COLUMN_SIZE</span></span>|<span data-ttu-id="5637d-175">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-175">Int32</span></span>|  
|<span data-ttu-id="5637d-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="5637d-177">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-177">Int32</span></span>|  
|<span data-ttu-id="5637d-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="5637d-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="5637d-179">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-179">Int16</span></span>|  
|<span data-ttu-id="5637d-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="5637d-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="5637d-181">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-181">Int16</span></span>|  
|<span data-ttu-id="5637d-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-182">NULLABLE</span></span>|<span data-ttu-id="5637d-183">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-183">Int16</span></span>|  
|<span data-ttu-id="5637d-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-184">REMARKS</span></span>|<span data-ttu-id="5637d-185">String</span><span class="sxs-lookup"><span data-stu-id="5637d-185">String</span></span>|  
|<span data-ttu-id="5637d-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="5637d-186">COLUMN_DEF</span></span>|<span data-ttu-id="5637d-187">String</span><span class="sxs-lookup"><span data-stu-id="5637d-187">String</span></span>|  
|<span data-ttu-id="5637d-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="5637d-189">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-189">Int16</span></span>|  
|<span data-ttu-id="5637d-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="5637d-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="5637d-191">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-191">Int16</span></span>|  
|<span data-ttu-id="5637d-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="5637d-193">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-193">Int32</span></span>|  
|<span data-ttu-id="5637d-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5637d-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="5637d-195">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-195">Int32</span></span>|  
|<span data-ttu-id="5637d-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-196">IS_NULLABLE</span></span>|<span data-ttu-id="5637d-197">String</span><span class="sxs-lookup"><span data-stu-id="5637d-197">String</span></span>|  
|<span data-ttu-id="5637d-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5637d-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="5637d-199">String</span><span class="sxs-lookup"><span data-stu-id="5637d-199">String</span></span>|  
|<span data-ttu-id="5637d-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5637d-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="5637d-201">String</span><span class="sxs-lookup"><span data-stu-id="5637d-201">String</span></span>|  
|<span data-ttu-id="5637d-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="5637d-203">Byte</span><span class="sxs-lookup"><span data-stu-id="5637d-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="5637d-204">手順</span><span class="sxs-lookup"><span data-stu-id="5637d-204">Procedures</span></span>  
  
|<span data-ttu-id="5637d-205">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-205">ColumnName</span></span>|<span data-ttu-id="5637d-206">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="5637d-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="5637d-208">String</span><span class="sxs-lookup"><span data-stu-id="5637d-208">String</span></span>|  
|<span data-ttu-id="5637d-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5637d-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="5637d-210">String</span><span class="sxs-lookup"><span data-stu-id="5637d-210">String</span></span>|  
|<span data-ttu-id="5637d-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="5637d-212">String</span><span class="sxs-lookup"><span data-stu-id="5637d-212">String</span></span>|  
|<span data-ttu-id="5637d-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5637d-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="5637d-214">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-214">Int32</span></span>|  
|<span data-ttu-id="5637d-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5637d-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="5637d-216">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-216">Int32</span></span>|  
|<span data-ttu-id="5637d-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="5637d-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="5637d-218">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-218">Int32</span></span>|  
|<span data-ttu-id="5637d-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-219">REMARKS</span></span>|<span data-ttu-id="5637d-220">String</span><span class="sxs-lookup"><span data-stu-id="5637d-220">String</span></span>|  
|<span data-ttu-id="5637d-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="5637d-222">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="5637d-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5637d-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="5637d-224">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-224">ColumnName</span></span>|<span data-ttu-id="5637d-225">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="5637d-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="5637d-227">String</span><span class="sxs-lookup"><span data-stu-id="5637d-227">String</span></span>|  
|<span data-ttu-id="5637d-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5637d-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="5637d-229">String</span><span class="sxs-lookup"><span data-stu-id="5637d-229">String</span></span>|  
|<span data-ttu-id="5637d-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="5637d-231">String</span><span class="sxs-lookup"><span data-stu-id="5637d-231">String</span></span>|  
|<span data-ttu-id="5637d-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-232">COLUMN_NAME</span></span>|<span data-ttu-id="5637d-233">String</span><span class="sxs-lookup"><span data-stu-id="5637d-233">String</span></span>|  
|<span data-ttu-id="5637d-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-234">COLUMN_TYPE</span></span>|<span data-ttu-id="5637d-235">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-235">Int16</span></span>|  
|<span data-ttu-id="5637d-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-236">DATA_TYPE</span></span>|<span data-ttu-id="5637d-237">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-237">Int16</span></span>|  
|<span data-ttu-id="5637d-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-238">TYPE_NAME</span></span>|<span data-ttu-id="5637d-239">String</span><span class="sxs-lookup"><span data-stu-id="5637d-239">String</span></span>|  
|<span data-ttu-id="5637d-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="5637d-240">COLUMN_SIZE</span></span>|<span data-ttu-id="5637d-241">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-241">Int32</span></span>|  
|<span data-ttu-id="5637d-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="5637d-243">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-243">Int32</span></span>|  
|<span data-ttu-id="5637d-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="5637d-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="5637d-245">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-245">Int16</span></span>|  
|<span data-ttu-id="5637d-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="5637d-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="5637d-247">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-247">Int16</span></span>|  
|<span data-ttu-id="5637d-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-248">NULLABLE</span></span>|<span data-ttu-id="5637d-249">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-249">Int16</span></span>|  
|<span data-ttu-id="5637d-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-250">REMARKS</span></span>|<span data-ttu-id="5637d-251">String</span><span class="sxs-lookup"><span data-stu-id="5637d-251">String</span></span>|  
|<span data-ttu-id="5637d-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="5637d-252">COLUMN_DEF</span></span>|<span data-ttu-id="5637d-253">String</span><span class="sxs-lookup"><span data-stu-id="5637d-253">String</span></span>|  
|<span data-ttu-id="5637d-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="5637d-255">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-255">Int16</span></span>|  
|<span data-ttu-id="5637d-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="5637d-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="5637d-257">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-257">Int16</span></span>|  
|<span data-ttu-id="5637d-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="5637d-259">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-259">Int32</span></span>|  
|<span data-ttu-id="5637d-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5637d-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="5637d-261">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-261">Int32</span></span>|  
|<span data-ttu-id="5637d-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-262">IS_NULLABLE</span></span>|<span data-ttu-id="5637d-263">String</span><span class="sxs-lookup"><span data-stu-id="5637d-263">String</span></span>|  
|<span data-ttu-id="5637d-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5637d-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="5637d-265">String</span><span class="sxs-lookup"><span data-stu-id="5637d-265">String</span></span>|  
|<span data-ttu-id="5637d-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5637d-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="5637d-267">String</span><span class="sxs-lookup"><span data-stu-id="5637d-267">String</span></span>|  
|<span data-ttu-id="5637d-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="5637d-269">Byte</span><span class="sxs-lookup"><span data-stu-id="5637d-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="5637d-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="5637d-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="5637d-271">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-271">ColumnName</span></span>|<span data-ttu-id="5637d-272">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="5637d-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="5637d-274">String</span><span class="sxs-lookup"><span data-stu-id="5637d-274">String</span></span>|  
|<span data-ttu-id="5637d-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5637d-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="5637d-276">String</span><span class="sxs-lookup"><span data-stu-id="5637d-276">String</span></span>|  
|<span data-ttu-id="5637d-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="5637d-278">String</span><span class="sxs-lookup"><span data-stu-id="5637d-278">String</span></span>|  
|<span data-ttu-id="5637d-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-279">COLUMN_NAME</span></span>|<span data-ttu-id="5637d-280">String</span><span class="sxs-lookup"><span data-stu-id="5637d-280">String</span></span>|  
|<span data-ttu-id="5637d-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-281">COLUMN_TYPE</span></span>|<span data-ttu-id="5637d-282">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-282">Int16</span></span>|  
|<span data-ttu-id="5637d-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-283">DATA_TYPE</span></span>|<span data-ttu-id="5637d-284">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-284">Int16</span></span>|  
|<span data-ttu-id="5637d-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-285">TYPE_NAME</span></span>|<span data-ttu-id="5637d-286">String</span><span class="sxs-lookup"><span data-stu-id="5637d-286">String</span></span>|  
|<span data-ttu-id="5637d-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="5637d-287">COLUMN_SIZE</span></span>|<span data-ttu-id="5637d-288">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-288">Int32</span></span>|  
|<span data-ttu-id="5637d-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="5637d-290">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-290">Int32</span></span>|  
|<span data-ttu-id="5637d-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="5637d-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="5637d-292">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-292">Int16</span></span>|  
|<span data-ttu-id="5637d-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="5637d-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="5637d-294">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-294">Int16</span></span>|  
|<span data-ttu-id="5637d-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-295">NULLABLE</span></span>|<span data-ttu-id="5637d-296">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-296">Int16</span></span>|  
|<span data-ttu-id="5637d-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-297">REMARKS</span></span>|<span data-ttu-id="5637d-298">String</span><span class="sxs-lookup"><span data-stu-id="5637d-298">String</span></span>|  
|<span data-ttu-id="5637d-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="5637d-299">COLUMN_DEF</span></span>|<span data-ttu-id="5637d-300">String</span><span class="sxs-lookup"><span data-stu-id="5637d-300">String</span></span>|  
|<span data-ttu-id="5637d-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="5637d-302">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-302">Int16</span></span>|  
|<span data-ttu-id="5637d-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="5637d-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="5637d-304">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-304">Int16</span></span>|  
|<span data-ttu-id="5637d-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="5637d-306">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-306">Int32</span></span>|  
|<span data-ttu-id="5637d-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5637d-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="5637d-308">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-308">Int32</span></span>|  
|<span data-ttu-id="5637d-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-309">IS_NULLABLE</span></span>|<span data-ttu-id="5637d-310">String</span><span class="sxs-lookup"><span data-stu-id="5637d-310">String</span></span>|  
|<span data-ttu-id="5637d-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5637d-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="5637d-312">String</span><span class="sxs-lookup"><span data-stu-id="5637d-312">String</span></span>|  
|<span data-ttu-id="5637d-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5637d-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="5637d-314">String</span><span class="sxs-lookup"><span data-stu-id="5637d-314">String</span></span>|  
|<span data-ttu-id="5637d-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="5637d-316">Byte</span><span class="sxs-lookup"><span data-stu-id="5637d-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="5637d-317">Microsoft Oracle ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="5637d-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="5637d-318">Microsoft SQL Server Oracle ODBC ドライバーは、共通のスキーマ コレクションに加えて次の特定のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5637d-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="5637d-319">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="5637d-319">Tables</span></span>  
  
-   <span data-ttu-id="5637d-320">列</span><span class="sxs-lookup"><span data-stu-id="5637d-320">Columns</span></span>  
  
-   <span data-ttu-id="5637d-321">手順</span><span class="sxs-lookup"><span data-stu-id="5637d-321">Procedures</span></span>  
  
-   <span data-ttu-id="5637d-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5637d-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="5637d-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="5637d-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="5637d-324">ビュー</span><span class="sxs-lookup"><span data-stu-id="5637d-324">Views</span></span>  
  
-   <span data-ttu-id="5637d-325">Indexes</span><span class="sxs-lookup"><span data-stu-id="5637d-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="5637d-326">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="5637d-326">Tables and Views</span></span>  
  
|<span data-ttu-id="5637d-327">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-327">ColumnName</span></span>|<span data-ttu-id="5637d-328">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5637d-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="5637d-330">String</span><span class="sxs-lookup"><span data-stu-id="5637d-330">String</span></span>|  
|<span data-ttu-id="5637d-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5637d-331">TABLE_OWNER</span></span>|<span data-ttu-id="5637d-332">String</span><span class="sxs-lookup"><span data-stu-id="5637d-332">String</span></span>|  
|<span data-ttu-id="5637d-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-333">TABLE_NAME</span></span>|<span data-ttu-id="5637d-334">String</span><span class="sxs-lookup"><span data-stu-id="5637d-334">String</span></span>|  
|<span data-ttu-id="5637d-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-335">TABLE_TYPE</span></span>|<span data-ttu-id="5637d-336">String</span><span class="sxs-lookup"><span data-stu-id="5637d-336">String</span></span>|  
|<span data-ttu-id="5637d-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-337">REMARKS</span></span>|<span data-ttu-id="5637d-338">String</span><span class="sxs-lookup"><span data-stu-id="5637d-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="5637d-339">列</span><span class="sxs-lookup"><span data-stu-id="5637d-339">Columns</span></span>  
  
|<span data-ttu-id="5637d-340">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-340">ColumnName</span></span>|<span data-ttu-id="5637d-341">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5637d-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="5637d-343">String</span><span class="sxs-lookup"><span data-stu-id="5637d-343">String</span></span>|  
|<span data-ttu-id="5637d-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5637d-344">TABLE_OWNER</span></span>|<span data-ttu-id="5637d-345">String</span><span class="sxs-lookup"><span data-stu-id="5637d-345">String</span></span>|  
|<span data-ttu-id="5637d-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-346">TABLE_NAME</span></span>|<span data-ttu-id="5637d-347">String</span><span class="sxs-lookup"><span data-stu-id="5637d-347">String</span></span>|  
|<span data-ttu-id="5637d-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-348">COLUMN_NAME</span></span>|<span data-ttu-id="5637d-349">String</span><span class="sxs-lookup"><span data-stu-id="5637d-349">String</span></span>|  
|<span data-ttu-id="5637d-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-350">DATA_TYPE</span></span>|<span data-ttu-id="5637d-351">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-351">Int16</span></span>|  
|<span data-ttu-id="5637d-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-352">TYPE_NAME</span></span>|<span data-ttu-id="5637d-353">String</span><span class="sxs-lookup"><span data-stu-id="5637d-353">String</span></span>|  
|<span data-ttu-id="5637d-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="5637d-354">PRECISION</span></span>|<span data-ttu-id="5637d-355">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-355">Int32</span></span>|  
|<span data-ttu-id="5637d-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-356">LENGTH</span></span>|<span data-ttu-id="5637d-357">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-357">Int32</span></span>|  
|<span data-ttu-id="5637d-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="5637d-358">SCALE</span></span>|<span data-ttu-id="5637d-359">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-359">Int16</span></span>|  
|<span data-ttu-id="5637d-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="5637d-360">RADIX</span></span>|<span data-ttu-id="5637d-361">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-361">Int16</span></span>|  
|<span data-ttu-id="5637d-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-362">NULLABLE</span></span>|<span data-ttu-id="5637d-363">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-363">Int16</span></span>|  
|<span data-ttu-id="5637d-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-364">REMARKS</span></span>|<span data-ttu-id="5637d-365">String</span><span class="sxs-lookup"><span data-stu-id="5637d-365">String</span></span>|  
|<span data-ttu-id="5637d-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5637d-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="5637d-367">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="5637d-368">手順</span><span class="sxs-lookup"><span data-stu-id="5637d-368">Procedures</span></span>  
  
|<span data-ttu-id="5637d-369">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-369">ColumnName</span></span>|<span data-ttu-id="5637d-370">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5637d-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="5637d-372">String</span><span class="sxs-lookup"><span data-stu-id="5637d-372">String</span></span>|  
|<span data-ttu-id="5637d-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5637d-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="5637d-374">String</span><span class="sxs-lookup"><span data-stu-id="5637d-374">String</span></span>|  
|<span data-ttu-id="5637d-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="5637d-376">String</span><span class="sxs-lookup"><span data-stu-id="5637d-376">String</span></span>|  
|<span data-ttu-id="5637d-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5637d-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="5637d-378">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-378">Int16</span></span>|  
|<span data-ttu-id="5637d-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5637d-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="5637d-380">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-380">Int16</span></span>|  
|<span data-ttu-id="5637d-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="5637d-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="5637d-382">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-382">Int16</span></span>|  
|<span data-ttu-id="5637d-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-383">REMARKS</span></span>|<span data-ttu-id="5637d-384">String</span><span class="sxs-lookup"><span data-stu-id="5637d-384">String</span></span>|  
|<span data-ttu-id="5637d-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="5637d-386">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="5637d-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5637d-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="5637d-388">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-388">ColumnName</span></span>|<span data-ttu-id="5637d-389">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5637d-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="5637d-391">String</span><span class="sxs-lookup"><span data-stu-id="5637d-391">String</span></span>|  
|<span data-ttu-id="5637d-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5637d-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="5637d-393">String</span><span class="sxs-lookup"><span data-stu-id="5637d-393">String</span></span>|  
|<span data-ttu-id="5637d-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="5637d-395">String</span><span class="sxs-lookup"><span data-stu-id="5637d-395">String</span></span>|  
|<span data-ttu-id="5637d-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-396">COLUMN_NAME</span></span>|<span data-ttu-id="5637d-397">String</span><span class="sxs-lookup"><span data-stu-id="5637d-397">String</span></span>|  
|<span data-ttu-id="5637d-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-398">COLUMN_TYPE</span></span>|<span data-ttu-id="5637d-399">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-399">Int16</span></span>|  
|<span data-ttu-id="5637d-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-400">DATA_TYPE</span></span>|<span data-ttu-id="5637d-401">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-401">Int16</span></span>|  
|<span data-ttu-id="5637d-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-402">TYPE_NAME</span></span>|<span data-ttu-id="5637d-403">String</span><span class="sxs-lookup"><span data-stu-id="5637d-403">String</span></span>|  
|<span data-ttu-id="5637d-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="5637d-404">PRECISION</span></span>|<span data-ttu-id="5637d-405">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-405">Int32</span></span>|  
|<span data-ttu-id="5637d-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-406">LENGTH</span></span>|<span data-ttu-id="5637d-407">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-407">Int32</span></span>|  
|<span data-ttu-id="5637d-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="5637d-408">SCALE</span></span>|<span data-ttu-id="5637d-409">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-409">Int16</span></span>|  
|<span data-ttu-id="5637d-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="5637d-410">RADIX</span></span>|<span data-ttu-id="5637d-411">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-411">Int16</span></span>|  
|<span data-ttu-id="5637d-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-412">NULLABLE</span></span>|<span data-ttu-id="5637d-413">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-413">Int16</span></span>|  
|<span data-ttu-id="5637d-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-414">REMARKS</span></span>|<span data-ttu-id="5637d-415">String</span><span class="sxs-lookup"><span data-stu-id="5637d-415">String</span></span>|  
|<span data-ttu-id="5637d-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="5637d-416">OVERLOAD</span></span>|<span data-ttu-id="5637d-417">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-417">Int32</span></span>|  
|<span data-ttu-id="5637d-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5637d-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="5637d-419">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="5637d-420">Microsoft Jet ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="5637d-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="5637d-421">Microsoft Jet ODBC Driver は、共通のスキーマ コレクションに加えて次のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5637d-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="5637d-422">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="5637d-422">Tables</span></span>  
  
-   <span data-ttu-id="5637d-423">Indexes</span><span class="sxs-lookup"><span data-stu-id="5637d-423">Indexes</span></span>  
  
-   <span data-ttu-id="5637d-424">列</span><span class="sxs-lookup"><span data-stu-id="5637d-424">Columns</span></span>  
  
-   <span data-ttu-id="5637d-425">手順</span><span class="sxs-lookup"><span data-stu-id="5637d-425">Procedures</span></span>  
  
-   <span data-ttu-id="5637d-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5637d-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="5637d-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="5637d-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="5637d-428">ビュー</span><span class="sxs-lookup"><span data-stu-id="5637d-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="5637d-429">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="5637d-429">Tables and Views</span></span>  
  
|<span data-ttu-id="5637d-430">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-430">ColumnName</span></span>|<span data-ttu-id="5637d-431">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5637d-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="5637d-433">String</span><span class="sxs-lookup"><span data-stu-id="5637d-433">String</span></span>|  
|<span data-ttu-id="5637d-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5637d-434">TABLE_OWNER</span></span>|<span data-ttu-id="5637d-435">String</span><span class="sxs-lookup"><span data-stu-id="5637d-435">String</span></span>|  
|<span data-ttu-id="5637d-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-436">TABLE_NAME</span></span>|<span data-ttu-id="5637d-437">String</span><span class="sxs-lookup"><span data-stu-id="5637d-437">String</span></span>|  
|<span data-ttu-id="5637d-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-438">TABLE_TYPE</span></span>|<span data-ttu-id="5637d-439">String</span><span class="sxs-lookup"><span data-stu-id="5637d-439">String</span></span>|  
|<span data-ttu-id="5637d-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-440">REMARKS</span></span>|<span data-ttu-id="5637d-441">String</span><span class="sxs-lookup"><span data-stu-id="5637d-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="5637d-442">列</span><span class="sxs-lookup"><span data-stu-id="5637d-442">Columns</span></span>  
  
|<span data-ttu-id="5637d-443">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-443">ColumnName</span></span>|<span data-ttu-id="5637d-444">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5637d-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="5637d-446">String</span><span class="sxs-lookup"><span data-stu-id="5637d-446">String</span></span>|  
|<span data-ttu-id="5637d-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5637d-447">TABLE_OWNER</span></span>|<span data-ttu-id="5637d-448">String</span><span class="sxs-lookup"><span data-stu-id="5637d-448">String</span></span>|  
|<span data-ttu-id="5637d-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-449">TABLE_NAME</span></span>|<span data-ttu-id="5637d-450">String</span><span class="sxs-lookup"><span data-stu-id="5637d-450">String</span></span>|  
|<span data-ttu-id="5637d-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-451">COLUMN_NAME</span></span>|<span data-ttu-id="5637d-452">String</span><span class="sxs-lookup"><span data-stu-id="5637d-452">String</span></span>|  
|<span data-ttu-id="5637d-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-453">DATA_TYPE</span></span>|<span data-ttu-id="5637d-454">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-454">Int16</span></span>|  
|<span data-ttu-id="5637d-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-455">TYPE_NAME</span></span>|<span data-ttu-id="5637d-456">String</span><span class="sxs-lookup"><span data-stu-id="5637d-456">String</span></span>|  
|<span data-ttu-id="5637d-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="5637d-457">PRECISION</span></span>|<span data-ttu-id="5637d-458">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-458">Int32</span></span>|  
|<span data-ttu-id="5637d-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-459">LENGTH</span></span>|<span data-ttu-id="5637d-460">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-460">Int32</span></span>|  
|<span data-ttu-id="5637d-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="5637d-461">SCALE</span></span>|<span data-ttu-id="5637d-462">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-462">Int16</span></span>|  
|<span data-ttu-id="5637d-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="5637d-463">RADIX</span></span>|<span data-ttu-id="5637d-464">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-464">Int16</span></span>|  
|<span data-ttu-id="5637d-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-465">NULLABLE</span></span>|<span data-ttu-id="5637d-466">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-466">Int16</span></span>|  
|<span data-ttu-id="5637d-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-467">REMARKS</span></span>|<span data-ttu-id="5637d-468">String</span><span class="sxs-lookup"><span data-stu-id="5637d-468">String</span></span>|  
|<span data-ttu-id="5637d-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5637d-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="5637d-470">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="5637d-471">手順</span><span class="sxs-lookup"><span data-stu-id="5637d-471">Procedures</span></span>  
  
|<span data-ttu-id="5637d-472">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-472">ColumnName</span></span>|<span data-ttu-id="5637d-473">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5637d-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="5637d-475">String</span><span class="sxs-lookup"><span data-stu-id="5637d-475">String</span></span>|  
|<span data-ttu-id="5637d-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5637d-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="5637d-477">String</span><span class="sxs-lookup"><span data-stu-id="5637d-477">String</span></span>|  
|<span data-ttu-id="5637d-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="5637d-479">String</span><span class="sxs-lookup"><span data-stu-id="5637d-479">String</span></span>|  
|<span data-ttu-id="5637d-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5637d-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="5637d-481">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-481">Int16</span></span>|  
|<span data-ttu-id="5637d-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="5637d-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="5637d-483">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-483">Int16</span></span>|  
|<span data-ttu-id="5637d-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="5637d-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="5637d-485">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-485">Int16</span></span>|  
|<span data-ttu-id="5637d-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-486">REMARKS</span></span>|<span data-ttu-id="5637d-487">String</span><span class="sxs-lookup"><span data-stu-id="5637d-487">String</span></span>|  
|<span data-ttu-id="5637d-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="5637d-489">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="5637d-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="5637d-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="5637d-491">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-491">ColumnName</span></span>|<span data-ttu-id="5637d-492">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="5637d-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="5637d-494">String</span><span class="sxs-lookup"><span data-stu-id="5637d-494">String</span></span>|  
|<span data-ttu-id="5637d-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="5637d-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="5637d-496">String</span><span class="sxs-lookup"><span data-stu-id="5637d-496">String</span></span>|  
|<span data-ttu-id="5637d-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="5637d-498">String</span><span class="sxs-lookup"><span data-stu-id="5637d-498">String</span></span>|  
|<span data-ttu-id="5637d-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-499">COLUMN_NAME</span></span>|<span data-ttu-id="5637d-500">String</span><span class="sxs-lookup"><span data-stu-id="5637d-500">String</span></span>|  
|<span data-ttu-id="5637d-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-501">COLUMN_TYPE</span></span>|<span data-ttu-id="5637d-502">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-502">Int16</span></span>|  
|<span data-ttu-id="5637d-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-503">DATA_TYPE</span></span>|<span data-ttu-id="5637d-504">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-504">Int16</span></span>|  
|<span data-ttu-id="5637d-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-505">TYPE_NAME</span></span>|<span data-ttu-id="5637d-506">String</span><span class="sxs-lookup"><span data-stu-id="5637d-506">String</span></span>|  
|<span data-ttu-id="5637d-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="5637d-507">PRECISION</span></span>|<span data-ttu-id="5637d-508">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-508">Int32</span></span>|  
|<span data-ttu-id="5637d-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-509">LENGTH</span></span>|<span data-ttu-id="5637d-510">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-510">Int32</span></span>|  
|<span data-ttu-id="5637d-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="5637d-511">SCALE</span></span>|<span data-ttu-id="5637d-512">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-512">Int16</span></span>|  
|<span data-ttu-id="5637d-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="5637d-513">RADIX</span></span>|<span data-ttu-id="5637d-514">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-514">Int16</span></span>|  
|<span data-ttu-id="5637d-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-515">NULLABLE</span></span>|<span data-ttu-id="5637d-516">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-516">Int16</span></span>|  
|<span data-ttu-id="5637d-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-517">REMARKS</span></span>|<span data-ttu-id="5637d-518">String</span><span class="sxs-lookup"><span data-stu-id="5637d-518">String</span></span>|  
|<span data-ttu-id="5637d-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="5637d-519">OVERLOAD</span></span>|<span data-ttu-id="5637d-520">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-520">Int32</span></span>|  
|<span data-ttu-id="5637d-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5637d-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="5637d-522">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="5637d-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="5637d-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="5637d-524">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5637d-524">ColumnName</span></span>|<span data-ttu-id="5637d-525">DataType</span><span class="sxs-lookup"><span data-stu-id="5637d-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="5637d-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="5637d-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="5637d-527">String</span><span class="sxs-lookup"><span data-stu-id="5637d-527">String</span></span>|  
|<span data-ttu-id="5637d-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="5637d-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="5637d-529">String</span><span class="sxs-lookup"><span data-stu-id="5637d-529">String</span></span>|  
|<span data-ttu-id="5637d-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="5637d-531">String</span><span class="sxs-lookup"><span data-stu-id="5637d-531">String</span></span>|  
|<span data-ttu-id="5637d-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-532">COLUMN_NAME</span></span>|<span data-ttu-id="5637d-533">String</span><span class="sxs-lookup"><span data-stu-id="5637d-533">String</span></span>|  
|<span data-ttu-id="5637d-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-534">COLUMN_TYPE</span></span>|<span data-ttu-id="5637d-535">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-535">Int16</span></span>|  
|<span data-ttu-id="5637d-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-536">DATA_TYPE</span></span>|<span data-ttu-id="5637d-537">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-537">Int16</span></span>|  
|<span data-ttu-id="5637d-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="5637d-538">TYPE_NAME</span></span>|<span data-ttu-id="5637d-539">String</span><span class="sxs-lookup"><span data-stu-id="5637d-539">String</span></span>|  
|<span data-ttu-id="5637d-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="5637d-540">COLUMN_SIZE</span></span>|<span data-ttu-id="5637d-541">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-541">Int32</span></span>|  
|<span data-ttu-id="5637d-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="5637d-543">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-543">Int32</span></span>|  
|<span data-ttu-id="5637d-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="5637d-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="5637d-545">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-545">Int16</span></span>|  
|<span data-ttu-id="5637d-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="5637d-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="5637d-547">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-547">Int16</span></span>|  
|<span data-ttu-id="5637d-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-548">NULLABLE</span></span>|<span data-ttu-id="5637d-549">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-549">Int16</span></span>|  
|<span data-ttu-id="5637d-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="5637d-550">REMARKS</span></span>|<span data-ttu-id="5637d-551">String</span><span class="sxs-lookup"><span data-stu-id="5637d-551">String</span></span>|  
|<span data-ttu-id="5637d-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="5637d-552">COLUMN_DEF</span></span>|<span data-ttu-id="5637d-553">String</span><span class="sxs-lookup"><span data-stu-id="5637d-553">String</span></span>|  
|<span data-ttu-id="5637d-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5637d-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="5637d-555">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-555">Int16</span></span>|  
|<span data-ttu-id="5637d-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="5637d-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="5637d-557">Int16</span><span class="sxs-lookup"><span data-stu-id="5637d-557">Int16</span></span>|  
|<span data-ttu-id="5637d-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="5637d-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="5637d-559">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-559">Int32</span></span>|  
|<span data-ttu-id="5637d-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="5637d-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="5637d-561">Int32</span><span class="sxs-lookup"><span data-stu-id="5637d-561">Int32</span></span>|  
|<span data-ttu-id="5637d-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="5637d-562">IS_NULLABLE</span></span>|<span data-ttu-id="5637d-563">String</span><span class="sxs-lookup"><span data-stu-id="5637d-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5637d-564">関連項目</span><span class="sxs-lookup"><span data-stu-id="5637d-564">See Also</span></span>  
 [<span data-ttu-id="5637d-565">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="5637d-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
