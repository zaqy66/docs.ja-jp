---
title: ODBC スキーマ コレクション
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: 072a9cd365031cd5660d1824bc229d459abc5af8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525834"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="f10d0-102">ODBC スキーマ コレクション</span><span class="sxs-lookup"><span data-stu-id="f10d0-102">ODBC Schema Collections</span></span>
<span data-ttu-id="f10d0-103">ここでは、Microsoft SQL Server、Oracle、および Microsoft Jet 用の各 ODBC ドライバーでのスキーマ コレクションのサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f10d0-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="f10d0-104">Microsoft SQL Server ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="f10d0-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="f10d0-105">Microsoft SQL Server ODBC Driver には、共通のスキーマ コレクションに加えて次の特定のスキーマ コレクションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f10d0-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="f10d0-106">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="f10d0-106">Tables</span></span>  
  
-   <span data-ttu-id="f10d0-107">Indexes</span><span class="sxs-lookup"><span data-stu-id="f10d0-107">Indexes</span></span>  
  
-   <span data-ttu-id="f10d0-108">列</span><span class="sxs-lookup"><span data-stu-id="f10d0-108">Columns</span></span>  
  
-   <span data-ttu-id="f10d0-109">手順</span><span class="sxs-lookup"><span data-stu-id="f10d0-109">Procedures</span></span>  
  
-   <span data-ttu-id="f10d0-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="f10d0-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="f10d0-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="f10d0-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="f10d0-112">ビュー</span><span class="sxs-lookup"><span data-stu-id="f10d0-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="f10d0-113">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="f10d0-113">Tables and Views</span></span>  
  
|<span data-ttu-id="f10d0-114">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-114">ColumnName</span></span>|<span data-ttu-id="f10d0-115">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="f10d0-116">TABLE_CAT</span></span>|<span data-ttu-id="f10d0-117">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-117">String</span></span>|  
|<span data-ttu-id="f10d0-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="f10d0-118">TABLE_SCHEM</span></span>|<span data-ttu-id="f10d0-119">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-119">String</span></span>|  
|<span data-ttu-id="f10d0-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-120">TABLE_NAME</span></span>|<span data-ttu-id="f10d0-121">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-121">String</span></span>|  
|<span data-ttu-id="f10d0-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-122">TABLE_TYPE</span></span>|<span data-ttu-id="f10d0-123">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-123">String</span></span>|  
|<span data-ttu-id="f10d0-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-124">REMARKS</span></span>|<span data-ttu-id="f10d0-125">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="f10d0-126">Indexes</span><span class="sxs-lookup"><span data-stu-id="f10d0-126">Indexes</span></span>  
  
|<span data-ttu-id="f10d0-127">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-127">ColumnName</span></span>|<span data-ttu-id="f10d0-128">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="f10d0-129">TABLE_CAT</span></span>|<span data-ttu-id="f10d0-130">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-130">String</span></span>|  
|<span data-ttu-id="f10d0-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="f10d0-131">TABLE_SCHEM</span></span>|<span data-ttu-id="f10d0-132">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-132">String</span></span>|  
|<span data-ttu-id="f10d0-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-133">TABLE_NAME</span></span>|<span data-ttu-id="f10d0-134">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-134">String</span></span>|  
|<span data-ttu-id="f10d0-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="f10d0-135">NON_UNIQUE</span></span>|<span data-ttu-id="f10d0-136">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-136">Int16</span></span>|  
|<span data-ttu-id="f10d0-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="f10d0-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="f10d0-138">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-138">String</span></span>|  
|<span data-ttu-id="f10d0-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-139">INDEX_NAME</span></span>|<span data-ttu-id="f10d0-140">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-140">String</span></span>|  
|<span data-ttu-id="f10d0-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-141">TYPE</span></span>|<span data-ttu-id="f10d0-142">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-142">Int16</span></span>|  
|<span data-ttu-id="f10d0-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="f10d0-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="f10d0-144">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-144">Int16</span></span>|  
|<span data-ttu-id="f10d0-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-145">COLUMN_NAME</span></span>|<span data-ttu-id="f10d0-146">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-146">String</span></span>|  
|<span data-ttu-id="f10d0-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="f10d0-147">ASC_OR_DESC</span></span>|<span data-ttu-id="f10d0-148">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-148">String</span></span>|  
|<span data-ttu-id="f10d0-149">CARDINATLITY</span><span class="sxs-lookup"><span data-stu-id="f10d0-149">CARDINATLITY</span></span>|<span data-ttu-id="f10d0-150">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-150">Int32</span></span>|  
|<span data-ttu-id="f10d0-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="f10d0-151">PAGES</span></span>|<span data-ttu-id="f10d0-152">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-152">Int32</span></span>|  
|<span data-ttu-id="f10d0-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="f10d0-153">FILTER_CONDITION</span></span>|<span data-ttu-id="f10d0-154">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-154">String</span></span>|  
|<span data-ttu-id="f10d0-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f10d0-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="f10d0-156">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-156">String</span></span>|  
|<span data-ttu-id="f10d0-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="f10d0-158">Byte</span><span class="sxs-lookup"><span data-stu-id="f10d0-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="f10d0-159">列</span><span class="sxs-lookup"><span data-stu-id="f10d0-159">Columns</span></span>  
  
|<span data-ttu-id="f10d0-160">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-160">ColumnName</span></span>|<span data-ttu-id="f10d0-161">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="f10d0-162">TABLE_CAT</span></span>|<span data-ttu-id="f10d0-163">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-163">String</span></span>|  
|<span data-ttu-id="f10d0-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="f10d0-164">TABLE_SCHEM</span></span>|<span data-ttu-id="f10d0-165">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-165">String</span></span>|  
|<span data-ttu-id="f10d0-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-166">TABLE_NAME</span></span>|<span data-ttu-id="f10d0-167">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-167">String</span></span>|  
|<span data-ttu-id="f10d0-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-168">COLUMN_NAME</span></span>|<span data-ttu-id="f10d0-169">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-169">String</span></span>|  
|<span data-ttu-id="f10d0-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-170">DATA_TYPE</span></span>|<span data-ttu-id="f10d0-171">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-171">Int16</span></span>|  
|<span data-ttu-id="f10d0-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-172">TYPE_NAME</span></span>|<span data-ttu-id="f10d0-173">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-173">String</span></span>|  
|<span data-ttu-id="f10d0-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="f10d0-174">COLUMN_SIZE</span></span>|<span data-ttu-id="f10d0-175">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-175">Int32</span></span>|  
|<span data-ttu-id="f10d0-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="f10d0-177">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-177">Int32</span></span>|  
|<span data-ttu-id="f10d0-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="f10d0-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="f10d0-179">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-179">Int16</span></span>|  
|<span data-ttu-id="f10d0-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="f10d0-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="f10d0-181">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-181">Int16</span></span>|  
|<span data-ttu-id="f10d0-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-182">NULLABLE</span></span>|<span data-ttu-id="f10d0-183">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-183">Int16</span></span>|  
|<span data-ttu-id="f10d0-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-184">REMARKS</span></span>|<span data-ttu-id="f10d0-185">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-185">String</span></span>|  
|<span data-ttu-id="f10d0-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="f10d0-186">COLUMN_DEF</span></span>|<span data-ttu-id="f10d0-187">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-187">String</span></span>|  
|<span data-ttu-id="f10d0-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="f10d0-189">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-189">Int16</span></span>|  
|<span data-ttu-id="f10d0-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="f10d0-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="f10d0-191">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-191">Int16</span></span>|  
|<span data-ttu-id="f10d0-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="f10d0-193">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-193">Int32</span></span>|  
|<span data-ttu-id="f10d0-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="f10d0-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="f10d0-195">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-195">Int32</span></span>|  
|<span data-ttu-id="f10d0-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-196">IS_NULLABLE</span></span>|<span data-ttu-id="f10d0-197">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-197">String</span></span>|  
|<span data-ttu-id="f10d0-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f10d0-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="f10d0-199">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-199">String</span></span>|  
|<span data-ttu-id="f10d0-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f10d0-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="f10d0-201">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-201">String</span></span>|  
|<span data-ttu-id="f10d0-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="f10d0-203">Byte</span><span class="sxs-lookup"><span data-stu-id="f10d0-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="f10d0-204">手順</span><span class="sxs-lookup"><span data-stu-id="f10d0-204">Procedures</span></span>  
  
|<span data-ttu-id="f10d0-205">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-205">ColumnName</span></span>|<span data-ttu-id="f10d0-206">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="f10d0-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="f10d0-208">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-208">String</span></span>|  
|<span data-ttu-id="f10d0-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="f10d0-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="f10d0-210">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-210">String</span></span>|  
|<span data-ttu-id="f10d0-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="f10d0-212">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-212">String</span></span>|  
|<span data-ttu-id="f10d0-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="f10d0-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="f10d0-214">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-214">Int32</span></span>|  
|<span data-ttu-id="f10d0-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="f10d0-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="f10d0-216">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-216">Int32</span></span>|  
|<span data-ttu-id="f10d0-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="f10d0-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="f10d0-218">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-218">Int32</span></span>|  
|<span data-ttu-id="f10d0-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-219">REMARKS</span></span>|<span data-ttu-id="f10d0-220">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-220">String</span></span>|  
|<span data-ttu-id="f10d0-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="f10d0-222">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="f10d0-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="f10d0-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="f10d0-224">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-224">ColumnName</span></span>|<span data-ttu-id="f10d0-225">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="f10d0-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="f10d0-227">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-227">String</span></span>|  
|<span data-ttu-id="f10d0-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="f10d0-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="f10d0-229">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-229">String</span></span>|  
|<span data-ttu-id="f10d0-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="f10d0-231">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-231">String</span></span>|  
|<span data-ttu-id="f10d0-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-232">COLUMN_NAME</span></span>|<span data-ttu-id="f10d0-233">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-233">String</span></span>|  
|<span data-ttu-id="f10d0-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-234">COLUMN_TYPE</span></span>|<span data-ttu-id="f10d0-235">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-235">Int16</span></span>|  
|<span data-ttu-id="f10d0-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-236">DATA_TYPE</span></span>|<span data-ttu-id="f10d0-237">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-237">Int16</span></span>|  
|<span data-ttu-id="f10d0-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-238">TYPE_NAME</span></span>|<span data-ttu-id="f10d0-239">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-239">String</span></span>|  
|<span data-ttu-id="f10d0-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="f10d0-240">COLUMN_SIZE</span></span>|<span data-ttu-id="f10d0-241">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-241">Int32</span></span>|  
|<span data-ttu-id="f10d0-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="f10d0-243">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-243">Int32</span></span>|  
|<span data-ttu-id="f10d0-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="f10d0-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="f10d0-245">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-245">Int16</span></span>|  
|<span data-ttu-id="f10d0-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="f10d0-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="f10d0-247">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-247">Int16</span></span>|  
|<span data-ttu-id="f10d0-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-248">NULLABLE</span></span>|<span data-ttu-id="f10d0-249">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-249">Int16</span></span>|  
|<span data-ttu-id="f10d0-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-250">REMARKS</span></span>|<span data-ttu-id="f10d0-251">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-251">String</span></span>|  
|<span data-ttu-id="f10d0-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="f10d0-252">COLUMN_DEF</span></span>|<span data-ttu-id="f10d0-253">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-253">String</span></span>|  
|<span data-ttu-id="f10d0-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="f10d0-255">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-255">Int16</span></span>|  
|<span data-ttu-id="f10d0-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="f10d0-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="f10d0-257">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-257">Int16</span></span>|  
|<span data-ttu-id="f10d0-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="f10d0-259">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-259">Int32</span></span>|  
|<span data-ttu-id="f10d0-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="f10d0-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="f10d0-261">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-261">Int32</span></span>|  
|<span data-ttu-id="f10d0-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-262">IS_NULLABLE</span></span>|<span data-ttu-id="f10d0-263">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-263">String</span></span>|  
|<span data-ttu-id="f10d0-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f10d0-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="f10d0-265">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-265">String</span></span>|  
|<span data-ttu-id="f10d0-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f10d0-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="f10d0-267">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-267">String</span></span>|  
|<span data-ttu-id="f10d0-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="f10d0-269">Byte</span><span class="sxs-lookup"><span data-stu-id="f10d0-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="f10d0-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="f10d0-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="f10d0-271">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-271">ColumnName</span></span>|<span data-ttu-id="f10d0-272">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="f10d0-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="f10d0-274">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-274">String</span></span>|  
|<span data-ttu-id="f10d0-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="f10d0-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="f10d0-276">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-276">String</span></span>|  
|<span data-ttu-id="f10d0-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="f10d0-278">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-278">String</span></span>|  
|<span data-ttu-id="f10d0-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-279">COLUMN_NAME</span></span>|<span data-ttu-id="f10d0-280">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-280">String</span></span>|  
|<span data-ttu-id="f10d0-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-281">COLUMN_TYPE</span></span>|<span data-ttu-id="f10d0-282">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-282">Int16</span></span>|  
|<span data-ttu-id="f10d0-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-283">DATA_TYPE</span></span>|<span data-ttu-id="f10d0-284">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-284">Int16</span></span>|  
|<span data-ttu-id="f10d0-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-285">TYPE_NAME</span></span>|<span data-ttu-id="f10d0-286">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-286">String</span></span>|  
|<span data-ttu-id="f10d0-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="f10d0-287">COLUMN_SIZE</span></span>|<span data-ttu-id="f10d0-288">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-288">Int32</span></span>|  
|<span data-ttu-id="f10d0-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="f10d0-290">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-290">Int32</span></span>|  
|<span data-ttu-id="f10d0-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="f10d0-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="f10d0-292">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-292">Int16</span></span>|  
|<span data-ttu-id="f10d0-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="f10d0-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="f10d0-294">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-294">Int16</span></span>|  
|<span data-ttu-id="f10d0-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-295">NULLABLE</span></span>|<span data-ttu-id="f10d0-296">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-296">Int16</span></span>|  
|<span data-ttu-id="f10d0-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-297">REMARKS</span></span>|<span data-ttu-id="f10d0-298">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-298">String</span></span>|  
|<span data-ttu-id="f10d0-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="f10d0-299">COLUMN_DEF</span></span>|<span data-ttu-id="f10d0-300">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-300">String</span></span>|  
|<span data-ttu-id="f10d0-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="f10d0-302">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-302">Int16</span></span>|  
|<span data-ttu-id="f10d0-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="f10d0-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="f10d0-304">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-304">Int16</span></span>|  
|<span data-ttu-id="f10d0-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="f10d0-306">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-306">Int32</span></span>|  
|<span data-ttu-id="f10d0-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="f10d0-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="f10d0-308">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-308">Int32</span></span>|  
|<span data-ttu-id="f10d0-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-309">IS_NULLABLE</span></span>|<span data-ttu-id="f10d0-310">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-310">String</span></span>|  
|<span data-ttu-id="f10d0-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f10d0-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="f10d0-312">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-312">String</span></span>|  
|<span data-ttu-id="f10d0-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f10d0-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="f10d0-314">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-314">String</span></span>|  
|<span data-ttu-id="f10d0-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="f10d0-316">Byte</span><span class="sxs-lookup"><span data-stu-id="f10d0-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="f10d0-317">Microsoft Oracle ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="f10d0-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="f10d0-318">Microsoft SQL Server Oracle ODBC ドライバーは、共通のスキーマ コレクションに加えて次の特定のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f10d0-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="f10d0-319">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="f10d0-319">Tables</span></span>  
  
-   <span data-ttu-id="f10d0-320">列</span><span class="sxs-lookup"><span data-stu-id="f10d0-320">Columns</span></span>  
  
-   <span data-ttu-id="f10d0-321">手順</span><span class="sxs-lookup"><span data-stu-id="f10d0-321">Procedures</span></span>  
  
-   <span data-ttu-id="f10d0-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="f10d0-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="f10d0-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="f10d0-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="f10d0-324">ビュー</span><span class="sxs-lookup"><span data-stu-id="f10d0-324">Views</span></span>  
  
-   <span data-ttu-id="f10d0-325">Indexes</span><span class="sxs-lookup"><span data-stu-id="f10d0-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="f10d0-326">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="f10d0-326">Tables and Views</span></span>  
  
|<span data-ttu-id="f10d0-327">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-327">ColumnName</span></span>|<span data-ttu-id="f10d0-328">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="f10d0-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="f10d0-330">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-330">String</span></span>|  
|<span data-ttu-id="f10d0-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="f10d0-331">TABLE_OWNER</span></span>|<span data-ttu-id="f10d0-332">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-332">String</span></span>|  
|<span data-ttu-id="f10d0-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-333">TABLE_NAME</span></span>|<span data-ttu-id="f10d0-334">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-334">String</span></span>|  
|<span data-ttu-id="f10d0-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-335">TABLE_TYPE</span></span>|<span data-ttu-id="f10d0-336">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-336">String</span></span>|  
|<span data-ttu-id="f10d0-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-337">REMARKS</span></span>|<span data-ttu-id="f10d0-338">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="f10d0-339">列</span><span class="sxs-lookup"><span data-stu-id="f10d0-339">Columns</span></span>  
  
|<span data-ttu-id="f10d0-340">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-340">ColumnName</span></span>|<span data-ttu-id="f10d0-341">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="f10d0-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="f10d0-343">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-343">String</span></span>|  
|<span data-ttu-id="f10d0-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="f10d0-344">TABLE_OWNER</span></span>|<span data-ttu-id="f10d0-345">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-345">String</span></span>|  
|<span data-ttu-id="f10d0-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-346">TABLE_NAME</span></span>|<span data-ttu-id="f10d0-347">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-347">String</span></span>|  
|<span data-ttu-id="f10d0-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-348">COLUMN_NAME</span></span>|<span data-ttu-id="f10d0-349">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-349">String</span></span>|  
|<span data-ttu-id="f10d0-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-350">DATA_TYPE</span></span>|<span data-ttu-id="f10d0-351">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-351">Int16</span></span>|  
|<span data-ttu-id="f10d0-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-352">TYPE_NAME</span></span>|<span data-ttu-id="f10d0-353">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-353">String</span></span>|  
|<span data-ttu-id="f10d0-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="f10d0-354">PRECISION</span></span>|<span data-ttu-id="f10d0-355">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-355">Int32</span></span>|  
|<span data-ttu-id="f10d0-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-356">LENGTH</span></span>|<span data-ttu-id="f10d0-357">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-357">Int32</span></span>|  
|<span data-ttu-id="f10d0-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="f10d0-358">SCALE</span></span>|<span data-ttu-id="f10d0-359">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-359">Int16</span></span>|  
|<span data-ttu-id="f10d0-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="f10d0-360">RADIX</span></span>|<span data-ttu-id="f10d0-361">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-361">Int16</span></span>|  
|<span data-ttu-id="f10d0-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-362">NULLABLE</span></span>|<span data-ttu-id="f10d0-363">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-363">Int16</span></span>|  
|<span data-ttu-id="f10d0-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-364">REMARKS</span></span>|<span data-ttu-id="f10d0-365">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-365">String</span></span>|  
|<span data-ttu-id="f10d0-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="f10d0-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="f10d0-367">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="f10d0-368">手順</span><span class="sxs-lookup"><span data-stu-id="f10d0-368">Procedures</span></span>  
  
|<span data-ttu-id="f10d0-369">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-369">ColumnName</span></span>|<span data-ttu-id="f10d0-370">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="f10d0-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="f10d0-372">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-372">String</span></span>|  
|<span data-ttu-id="f10d0-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="f10d0-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="f10d0-374">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-374">String</span></span>|  
|<span data-ttu-id="f10d0-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="f10d0-376">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-376">String</span></span>|  
|<span data-ttu-id="f10d0-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="f10d0-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="f10d0-378">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-378">Int16</span></span>|  
|<span data-ttu-id="f10d0-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="f10d0-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="f10d0-380">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-380">Int16</span></span>|  
|<span data-ttu-id="f10d0-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="f10d0-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="f10d0-382">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-382">Int16</span></span>|  
|<span data-ttu-id="f10d0-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-383">REMARKS</span></span>|<span data-ttu-id="f10d0-384">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-384">String</span></span>|  
|<span data-ttu-id="f10d0-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="f10d0-386">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="f10d0-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="f10d0-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="f10d0-388">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-388">ColumnName</span></span>|<span data-ttu-id="f10d0-389">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="f10d0-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="f10d0-391">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-391">String</span></span>|  
|<span data-ttu-id="f10d0-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="f10d0-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="f10d0-393">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-393">String</span></span>|  
|<span data-ttu-id="f10d0-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="f10d0-395">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-395">String</span></span>|  
|<span data-ttu-id="f10d0-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-396">COLUMN_NAME</span></span>|<span data-ttu-id="f10d0-397">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-397">String</span></span>|  
|<span data-ttu-id="f10d0-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-398">COLUMN_TYPE</span></span>|<span data-ttu-id="f10d0-399">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-399">Int16</span></span>|  
|<span data-ttu-id="f10d0-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-400">DATA_TYPE</span></span>|<span data-ttu-id="f10d0-401">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-401">Int16</span></span>|  
|<span data-ttu-id="f10d0-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-402">TYPE_NAME</span></span>|<span data-ttu-id="f10d0-403">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-403">String</span></span>|  
|<span data-ttu-id="f10d0-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="f10d0-404">PRECISION</span></span>|<span data-ttu-id="f10d0-405">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-405">Int32</span></span>|  
|<span data-ttu-id="f10d0-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-406">LENGTH</span></span>|<span data-ttu-id="f10d0-407">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-407">Int32</span></span>|  
|<span data-ttu-id="f10d0-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="f10d0-408">SCALE</span></span>|<span data-ttu-id="f10d0-409">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-409">Int16</span></span>|  
|<span data-ttu-id="f10d0-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="f10d0-410">RADIX</span></span>|<span data-ttu-id="f10d0-411">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-411">Int16</span></span>|  
|<span data-ttu-id="f10d0-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-412">NULLABLE</span></span>|<span data-ttu-id="f10d0-413">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-413">Int16</span></span>|  
|<span data-ttu-id="f10d0-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-414">REMARKS</span></span>|<span data-ttu-id="f10d0-415">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-415">String</span></span>|  
|<span data-ttu-id="f10d0-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="f10d0-416">OVERLOAD</span></span>|<span data-ttu-id="f10d0-417">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-417">Int32</span></span>|  
|<span data-ttu-id="f10d0-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="f10d0-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="f10d0-419">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="f10d0-420">Microsoft Jet ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="f10d0-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="f10d0-421">Microsoft Jet ODBC Driver は、共通のスキーマ コレクションに加えて次のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f10d0-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="f10d0-422">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="f10d0-422">Tables</span></span>  
  
-   <span data-ttu-id="f10d0-423">Indexes</span><span class="sxs-lookup"><span data-stu-id="f10d0-423">Indexes</span></span>  
  
-   <span data-ttu-id="f10d0-424">列</span><span class="sxs-lookup"><span data-stu-id="f10d0-424">Columns</span></span>  
  
-   <span data-ttu-id="f10d0-425">手順</span><span class="sxs-lookup"><span data-stu-id="f10d0-425">Procedures</span></span>  
  
-   <span data-ttu-id="f10d0-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="f10d0-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="f10d0-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="f10d0-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="f10d0-428">ビュー</span><span class="sxs-lookup"><span data-stu-id="f10d0-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="f10d0-429">Tables と Views</span><span class="sxs-lookup"><span data-stu-id="f10d0-429">Tables and Views</span></span>  
  
|<span data-ttu-id="f10d0-430">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-430">ColumnName</span></span>|<span data-ttu-id="f10d0-431">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="f10d0-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="f10d0-433">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-433">String</span></span>|  
|<span data-ttu-id="f10d0-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="f10d0-434">TABLE_OWNER</span></span>|<span data-ttu-id="f10d0-435">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-435">String</span></span>|  
|<span data-ttu-id="f10d0-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-436">TABLE_NAME</span></span>|<span data-ttu-id="f10d0-437">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-437">String</span></span>|  
|<span data-ttu-id="f10d0-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-438">TABLE_TYPE</span></span>|<span data-ttu-id="f10d0-439">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-439">String</span></span>|  
|<span data-ttu-id="f10d0-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-440">REMARKS</span></span>|<span data-ttu-id="f10d0-441">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="f10d0-442">列</span><span class="sxs-lookup"><span data-stu-id="f10d0-442">Columns</span></span>  
  
|<span data-ttu-id="f10d0-443">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-443">ColumnName</span></span>|<span data-ttu-id="f10d0-444">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="f10d0-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="f10d0-446">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-446">String</span></span>|  
|<span data-ttu-id="f10d0-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="f10d0-447">TABLE_OWNER</span></span>|<span data-ttu-id="f10d0-448">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-448">String</span></span>|  
|<span data-ttu-id="f10d0-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-449">TABLE_NAME</span></span>|<span data-ttu-id="f10d0-450">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-450">String</span></span>|  
|<span data-ttu-id="f10d0-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-451">COLUMN_NAME</span></span>|<span data-ttu-id="f10d0-452">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-452">String</span></span>|  
|<span data-ttu-id="f10d0-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-453">DATA_TYPE</span></span>|<span data-ttu-id="f10d0-454">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-454">Int16</span></span>|  
|<span data-ttu-id="f10d0-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-455">TYPE_NAME</span></span>|<span data-ttu-id="f10d0-456">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-456">String</span></span>|  
|<span data-ttu-id="f10d0-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="f10d0-457">PRECISION</span></span>|<span data-ttu-id="f10d0-458">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-458">Int32</span></span>|  
|<span data-ttu-id="f10d0-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-459">LENGTH</span></span>|<span data-ttu-id="f10d0-460">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-460">Int32</span></span>|  
|<span data-ttu-id="f10d0-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="f10d0-461">SCALE</span></span>|<span data-ttu-id="f10d0-462">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-462">Int16</span></span>|  
|<span data-ttu-id="f10d0-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="f10d0-463">RADIX</span></span>|<span data-ttu-id="f10d0-464">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-464">Int16</span></span>|  
|<span data-ttu-id="f10d0-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-465">NULLABLE</span></span>|<span data-ttu-id="f10d0-466">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-466">Int16</span></span>|  
|<span data-ttu-id="f10d0-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-467">REMARKS</span></span>|<span data-ttu-id="f10d0-468">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-468">String</span></span>|  
|<span data-ttu-id="f10d0-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="f10d0-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="f10d0-470">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="f10d0-471">手順</span><span class="sxs-lookup"><span data-stu-id="f10d0-471">Procedures</span></span>  
  
|<span data-ttu-id="f10d0-472">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-472">ColumnName</span></span>|<span data-ttu-id="f10d0-473">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="f10d0-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="f10d0-475">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-475">String</span></span>|  
|<span data-ttu-id="f10d0-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="f10d0-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="f10d0-477">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-477">String</span></span>|  
|<span data-ttu-id="f10d0-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="f10d0-479">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-479">String</span></span>|  
|<span data-ttu-id="f10d0-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="f10d0-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="f10d0-481">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-481">Int16</span></span>|  
|<span data-ttu-id="f10d0-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="f10d0-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="f10d0-483">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-483">Int16</span></span>|  
|<span data-ttu-id="f10d0-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="f10d0-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="f10d0-485">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-485">Int16</span></span>|  
|<span data-ttu-id="f10d0-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-486">REMARKS</span></span>|<span data-ttu-id="f10d0-487">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-487">String</span></span>|  
|<span data-ttu-id="f10d0-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="f10d0-489">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="f10d0-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="f10d0-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="f10d0-491">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-491">ColumnName</span></span>|<span data-ttu-id="f10d0-492">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="f10d0-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="f10d0-494">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-494">String</span></span>|  
|<span data-ttu-id="f10d0-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="f10d0-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="f10d0-496">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-496">String</span></span>|  
|<span data-ttu-id="f10d0-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="f10d0-498">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-498">String</span></span>|  
|<span data-ttu-id="f10d0-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-499">COLUMN_NAME</span></span>|<span data-ttu-id="f10d0-500">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-500">String</span></span>|  
|<span data-ttu-id="f10d0-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-501">COLUMN_TYPE</span></span>|<span data-ttu-id="f10d0-502">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-502">Int16</span></span>|  
|<span data-ttu-id="f10d0-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-503">DATA_TYPE</span></span>|<span data-ttu-id="f10d0-504">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-504">Int16</span></span>|  
|<span data-ttu-id="f10d0-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-505">TYPE_NAME</span></span>|<span data-ttu-id="f10d0-506">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-506">String</span></span>|  
|<span data-ttu-id="f10d0-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="f10d0-507">PRECISION</span></span>|<span data-ttu-id="f10d0-508">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-508">Int32</span></span>|  
|<span data-ttu-id="f10d0-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-509">LENGTH</span></span>|<span data-ttu-id="f10d0-510">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-510">Int32</span></span>|  
|<span data-ttu-id="f10d0-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="f10d0-511">SCALE</span></span>|<span data-ttu-id="f10d0-512">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-512">Int16</span></span>|  
|<span data-ttu-id="f10d0-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="f10d0-513">RADIX</span></span>|<span data-ttu-id="f10d0-514">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-514">Int16</span></span>|  
|<span data-ttu-id="f10d0-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-515">NULLABLE</span></span>|<span data-ttu-id="f10d0-516">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-516">Int16</span></span>|  
|<span data-ttu-id="f10d0-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-517">REMARKS</span></span>|<span data-ttu-id="f10d0-518">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-518">String</span></span>|  
|<span data-ttu-id="f10d0-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="f10d0-519">OVERLOAD</span></span>|<span data-ttu-id="f10d0-520">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-520">Int32</span></span>|  
|<span data-ttu-id="f10d0-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="f10d0-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="f10d0-522">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="f10d0-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="f10d0-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="f10d0-524">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f10d0-524">ColumnName</span></span>|<span data-ttu-id="f10d0-525">DataType</span><span class="sxs-lookup"><span data-stu-id="f10d0-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="f10d0-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="f10d0-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="f10d0-527">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-527">String</span></span>|  
|<span data-ttu-id="f10d0-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="f10d0-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="f10d0-529">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-529">String</span></span>|  
|<span data-ttu-id="f10d0-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="f10d0-531">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-531">String</span></span>|  
|<span data-ttu-id="f10d0-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-532">COLUMN_NAME</span></span>|<span data-ttu-id="f10d0-533">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-533">String</span></span>|  
|<span data-ttu-id="f10d0-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-534">COLUMN_TYPE</span></span>|<span data-ttu-id="f10d0-535">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-535">Int16</span></span>|  
|<span data-ttu-id="f10d0-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-536">DATA_TYPE</span></span>|<span data-ttu-id="f10d0-537">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-537">Int16</span></span>|  
|<span data-ttu-id="f10d0-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="f10d0-538">TYPE_NAME</span></span>|<span data-ttu-id="f10d0-539">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-539">String</span></span>|  
|<span data-ttu-id="f10d0-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="f10d0-540">COLUMN_SIZE</span></span>|<span data-ttu-id="f10d0-541">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-541">Int32</span></span>|  
|<span data-ttu-id="f10d0-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="f10d0-543">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-543">Int32</span></span>|  
|<span data-ttu-id="f10d0-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="f10d0-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="f10d0-545">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-545">Int16</span></span>|  
|<span data-ttu-id="f10d0-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="f10d0-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="f10d0-547">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-547">Int16</span></span>|  
|<span data-ttu-id="f10d0-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-548">NULLABLE</span></span>|<span data-ttu-id="f10d0-549">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-549">Int16</span></span>|  
|<span data-ttu-id="f10d0-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="f10d0-550">REMARKS</span></span>|<span data-ttu-id="f10d0-551">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-551">String</span></span>|  
|<span data-ttu-id="f10d0-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="f10d0-552">COLUMN_DEF</span></span>|<span data-ttu-id="f10d0-553">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-553">String</span></span>|  
|<span data-ttu-id="f10d0-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f10d0-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="f10d0-555">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-555">Int16</span></span>|  
|<span data-ttu-id="f10d0-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="f10d0-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="f10d0-557">Int16</span><span class="sxs-lookup"><span data-stu-id="f10d0-557">Int16</span></span>|  
|<span data-ttu-id="f10d0-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="f10d0-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="f10d0-559">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-559">Int32</span></span>|  
|<span data-ttu-id="f10d0-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="f10d0-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="f10d0-561">Int32</span><span class="sxs-lookup"><span data-stu-id="f10d0-561">Int32</span></span>|  
|<span data-ttu-id="f10d0-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="f10d0-562">IS_NULLABLE</span></span>|<span data-ttu-id="f10d0-563">String</span><span class="sxs-lookup"><span data-stu-id="f10d0-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f10d0-564">関連項目</span><span class="sxs-lookup"><span data-stu-id="f10d0-564">See also</span></span>
- [<span data-ttu-id="f10d0-565">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="f10d0-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
