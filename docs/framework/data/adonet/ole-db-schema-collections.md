---
title: OLE DB スキーマ コレクション
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: 1ab6426875b73b400a59b7e4cf155615d7472d05
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43514490"
---
# <a name="ole-db-schema-collections"></a><span data-ttu-id="d8ac8-102">OLE DB スキーマ コレクション</span><span class="sxs-lookup"><span data-stu-id="d8ac8-102">OLE DB Schema Collections</span></span>
<span data-ttu-id="d8ac8-103">ここでは、Microsoft SQL Server、Oracle、および Microsoft Jet 用の各 OLE DB プロバイダーでのスキーマ コレクションのサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d8ac8-103">This section discusses schema collection support for the OLE DB providers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-ole-db-provider"></a><span data-ttu-id="d8ac8-104">Microsoft SQL Server OLE DB Provider</span><span class="sxs-lookup"><span data-stu-id="d8ac8-104">Microsoft SQL Server OLE DB Provider</span></span>  
 <span data-ttu-id="d8ac8-105">Microsoft SQL Server OLE DB Driver は、共通のスキーマ コレクションに加えて次の特定のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d8ac8-105">The Microsoft SQL Server OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="d8ac8-106">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="d8ac8-106">Tables</span></span>  
  
-   <span data-ttu-id="d8ac8-107">列</span><span class="sxs-lookup"><span data-stu-id="d8ac8-107">Columns</span></span>  
  
-   <span data-ttu-id="d8ac8-108">手順</span><span class="sxs-lookup"><span data-stu-id="d8ac8-108">Procedures</span></span>  
  
-   <span data-ttu-id="d8ac8-109">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="d8ac8-109">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="d8ac8-110">Catalog</span><span class="sxs-lookup"><span data-stu-id="d8ac8-110">Catalog</span></span>  
  
-   <span data-ttu-id="d8ac8-111">Indexes</span><span class="sxs-lookup"><span data-stu-id="d8ac8-111">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="d8ac8-112">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="d8ac8-112">Tables</span></span>  
  
|<span data-ttu-id="d8ac8-113">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-113">ColumnName</span></span>|<span data-ttu-id="d8ac8-114">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-114">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-115">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-115">TABLE_CATALOG</span></span>|<span data-ttu-id="d8ac8-116">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-116">String</span></span>|  
|<span data-ttu-id="d8ac8-117">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-117">TABLE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-118">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-118">String</span></span>|  
|<span data-ttu-id="d8ac8-119">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-119">TABLE_NAME</span></span>|<span data-ttu-id="d8ac8-120">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-120">String</span></span>|  
|<span data-ttu-id="d8ac8-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-121">TABLE_TYPE</span></span>|<span data-ttu-id="d8ac8-122">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-122">String</span></span>|  
|<span data-ttu-id="d8ac8-123">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-123">TABLE_GUID</span></span>|<span data-ttu-id="d8ac8-124">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-124">Guid</span></span>|  
|<span data-ttu-id="d8ac8-125">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-125">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-126">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-126">String</span></span>|  
|<span data-ttu-id="d8ac8-127">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-127">TABLE_PROPID</span></span>|<span data-ttu-id="d8ac8-128">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-128">Int64</span></span>|  
|<span data-ttu-id="d8ac8-129">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-129">DATE_CREATED</span></span>|<span data-ttu-id="d8ac8-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-130">DateTime</span></span>|  
|<span data-ttu-id="d8ac8-131">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-131">DATE_MODIFIED</span></span>|<span data-ttu-id="d8ac8-132">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-132">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="d8ac8-133">列</span><span class="sxs-lookup"><span data-stu-id="d8ac8-133">Columns</span></span>  
  
|<span data-ttu-id="d8ac8-134">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-134">ColumnName</span></span>|<span data-ttu-id="d8ac8-135">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-135">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-136">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-136">TABLE_CATALOG</span></span>|<span data-ttu-id="d8ac8-137">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-137">String</span></span>|  
|<span data-ttu-id="d8ac8-138">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-138">TABLE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-139">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-139">String</span></span>|  
|<span data-ttu-id="d8ac8-140">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-140">TABLE_NAME</span></span>|<span data-ttu-id="d8ac8-141">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-141">String</span></span>|  
|<span data-ttu-id="d8ac8-142">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-142">COLUMN_NAME</span></span>|<span data-ttu-id="d8ac8-143">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-143">String</span></span>|  
|<span data-ttu-id="d8ac8-144">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-144">COLUMN_GUID</span></span>|<span data-ttu-id="d8ac8-145">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-145">Guid</span></span>|  
|<span data-ttu-id="d8ac8-146">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-146">COLUMN_PROPID</span></span>|<span data-ttu-id="d8ac8-147">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-147">Int64</span></span>|  
|<span data-ttu-id="d8ac8-148">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-148">ORDINAL_POSITION</span></span>|<span data-ttu-id="d8ac8-149">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-149">Int64</span></span>|  
|<span data-ttu-id="d8ac8-150">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="d8ac8-150">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="d8ac8-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-151">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-152">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d8ac8-152">COLUMN_DEFAULT</span></span>|<span data-ttu-id="d8ac8-153">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-153">String</span></span>|  
|<span data-ttu-id="d8ac8-154">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="d8ac8-154">COLUMN_FLAGS</span></span>|<span data-ttu-id="d8ac8-155">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-155">Int64</span></span>|  
|<span data-ttu-id="d8ac8-156">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-156">IS_NULLABLE</span></span>|<span data-ttu-id="d8ac8-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-157">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-158">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-158">DATA_TYPE</span></span>|<span data-ttu-id="d8ac8-159">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-159">Int32</span></span>|  
|<span data-ttu-id="d8ac8-160">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-160">TYPE_GUID</span></span>|<span data-ttu-id="d8ac8-161">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-161">Guid</span></span>|  
|<span data-ttu-id="d8ac8-162">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d8ac8-162">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="d8ac8-163">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-163">Int64</span></span>|  
|<span data-ttu-id="d8ac8-164">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d8ac8-164">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="d8ac8-165">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-165">Int64</span></span>|  
|<span data-ttu-id="d8ac8-166">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-166">NUMERIC_PRECISION</span></span>|<span data-ttu-id="d8ac8-167">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-167">Int32</span></span>|  
|<span data-ttu-id="d8ac8-168">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-168">NUMERIC_SCALE</span></span>|<span data-ttu-id="d8ac8-169">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-169">Int16</span></span>|  
|<span data-ttu-id="d8ac8-170">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-170">DATETIME_PRECISION</span></span>|<span data-ttu-id="d8ac8-171">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-171">Int64</span></span>|  
|<span data-ttu-id="d8ac8-172">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-172">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="d8ac8-173">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-173">String</span></span>|  
|<span data-ttu-id="d8ac8-174">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-174">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="d8ac8-175">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-175">String</span></span>|  
|<span data-ttu-id="d8ac8-176">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-176">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="d8ac8-177">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-177">String</span></span>|  
|<span data-ttu-id="d8ac8-178">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-178">COLLATION_CATALOG</span></span>|<span data-ttu-id="d8ac8-179">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-179">String</span></span>|  
|<span data-ttu-id="d8ac8-180">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-180">COLLATION_SCHEMA</span></span>|<span data-ttu-id="d8ac8-181">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-181">String</span></span>|  
|<span data-ttu-id="d8ac8-182">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-182">COLLATION_NAME</span></span>|<span data-ttu-id="d8ac8-183">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-183">String</span></span>|  
|<span data-ttu-id="d8ac8-184">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-184">DOMAIN_CATALOG</span></span>|<span data-ttu-id="d8ac8-185">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-185">String</span></span>|  
|<span data-ttu-id="d8ac8-186">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-186">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="d8ac8-187">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-187">String</span></span>|  
|<span data-ttu-id="d8ac8-188">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-188">DOMAIN_NAME</span></span>|<span data-ttu-id="d8ac8-189">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-189">String</span></span>|  
|<span data-ttu-id="d8ac8-190">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-190">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-191">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-191">String</span></span>|  
|<span data-ttu-id="d8ac8-192">COLUMN_LCID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-192">COLUMN_LCID</span></span>|<span data-ttu-id="d8ac8-193">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-193">Int32</span></span>|  
|<span data-ttu-id="d8ac8-194">COLUMN_COMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="d8ac8-194">COLUMN_COMPFLAGS</span></span>|<span data-ttu-id="d8ac8-195">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-195">Int32</span></span>|  
|<span data-ttu-id="d8ac8-196">COLUMN_SORTID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-196">COLUMN_SORTID</span></span>|<span data-ttu-id="d8ac8-197">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-197">Int32</span></span>|  
|<span data-ttu-id="d8ac8-198">COLUMN_TDSCOLLATION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-198">COLUMN_TDSCOLLATION</span></span>|<span data-ttu-id="d8ac8-199">Byte[]</span><span class="sxs-lookup"><span data-stu-id="d8ac8-199">Byte[]</span></span>|  
|<span data-ttu-id="d8ac8-200">IS_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-200">IS_COMPUTED</span></span>|<span data-ttu-id="d8ac8-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-201">Boolean</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="d8ac8-202">手順</span><span class="sxs-lookup"><span data-stu-id="d8ac8-202">Procedures</span></span>  
  
|<span data-ttu-id="d8ac8-203">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-203">ColumnName</span></span>|<span data-ttu-id="d8ac8-204">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-204">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-205">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-205">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="d8ac8-206">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-206">String</span></span>|  
|<span data-ttu-id="d8ac8-207">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-207">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-208">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-208">String</span></span>|  
|<span data-ttu-id="d8ac8-209">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-209">PROCEDURE_NAME</span></span>|<span data-ttu-id="d8ac8-210">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-210">String</span></span>|  
|<span data-ttu-id="d8ac8-211">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-211">PROCEDURE_TYPE</span></span>|<span data-ttu-id="d8ac8-212">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-212">Int16</span></span>|  
|<span data-ttu-id="d8ac8-213">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-213">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="d8ac8-214">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-214">String</span></span>|  
|<span data-ttu-id="d8ac8-215">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-215">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-216">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-216">String</span></span>|  
|<span data-ttu-id="d8ac8-217">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-217">DATE_CREATED</span></span>|<span data-ttu-id="d8ac8-218">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-218">DateTime</span></span>|  
|<span data-ttu-id="d8ac8-219">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-219">DATE_MODIFIED</span></span>|<span data-ttu-id="d8ac8-220">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-220">DateTime</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="d8ac8-221">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="d8ac8-221">ProcedureParameters</span></span>  
  
|<span data-ttu-id="d8ac8-222">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-222">ColumnName</span></span>|<span data-ttu-id="d8ac8-223">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-223">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-224">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-224">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="d8ac8-225">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-225">String</span></span>|  
|<span data-ttu-id="d8ac8-226">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-226">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-227">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-227">String</span></span>|  
|<span data-ttu-id="d8ac8-228">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-228">PROCEDURE_NAME</span></span>|<span data-ttu-id="d8ac8-229">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-229">String</span></span>|  
|<span data-ttu-id="d8ac8-230">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-230">PARAMETER_NAME</span></span>|<span data-ttu-id="d8ac8-231">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-231">String</span></span>|  
|<span data-ttu-id="d8ac8-232">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-232">ORDINAL_POSITION</span></span>|<span data-ttu-id="d8ac8-233">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-233">Int32</span></span>|  
|<span data-ttu-id="d8ac8-234">PARAMETER_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-234">PARAMETER_TYPE</span></span>|<span data-ttu-id="d8ac8-235">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-235">Int32</span></span>|  
|<span data-ttu-id="d8ac8-236">PARAMETER_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="d8ac8-236">PARAMETER_HASDEFAULT</span></span>|<span data-ttu-id="d8ac8-237">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-237">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-238">PARAMETER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d8ac8-238">PARAMETER_DEFAULT</span></span>|<span data-ttu-id="d8ac8-239">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-239">String</span></span>|  
|<span data-ttu-id="d8ac8-240">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-240">IS_NULLABLE</span></span>|<span data-ttu-id="d8ac8-241">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-241">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-242">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-242">DATA_TYPE</span></span>|<span data-ttu-id="d8ac8-243">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-243">Int32</span></span>|  
|<span data-ttu-id="d8ac8-244">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d8ac8-244">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="d8ac8-245">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-245">Int64</span></span>|  
|<span data-ttu-id="d8ac8-246">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d8ac8-246">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="d8ac8-247">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-247">Int64</span></span>|  
|<span data-ttu-id="d8ac8-248">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-248">NUMERIC_PRECISION</span></span>|<span data-ttu-id="d8ac8-249">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-249">Int32</span></span>|  
|<span data-ttu-id="d8ac8-250">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-250">NUMERIC_SCALE</span></span>|<span data-ttu-id="d8ac8-251">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-251">Int16</span></span>|  
|<span data-ttu-id="d8ac8-252">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-252">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-253">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-253">String</span></span>|  
|<span data-ttu-id="d8ac8-254">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-254">TYPE_NAME</span></span>|<span data-ttu-id="d8ac8-255">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-255">String</span></span>|  
|<span data-ttu-id="d8ac8-256">LOCAL_TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-256">LOCAL_TYPE_NAME</span></span>|<span data-ttu-id="d8ac8-257">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-257">String</span></span>|  
  
### <a name="catalog"></a><span data-ttu-id="d8ac8-258">Catalog</span><span class="sxs-lookup"><span data-stu-id="d8ac8-258">Catalog</span></span>  
  
|<span data-ttu-id="d8ac8-259">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-259">ColumnName</span></span>|<span data-ttu-id="d8ac8-260">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-260">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-261">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-261">CATALOG_NAME</span></span>|<span data-ttu-id="d8ac8-262">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-262">String</span></span>|  
|<span data-ttu-id="d8ac8-263">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-263">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-264">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-264">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="d8ac8-265">Indexes</span><span class="sxs-lookup"><span data-stu-id="d8ac8-265">Indexes</span></span>  
  
|<span data-ttu-id="d8ac8-266">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-266">ColumnName</span></span>|<span data-ttu-id="d8ac8-267">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-267">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-268">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-268">TABLE_CATALOG</span></span>|<span data-ttu-id="d8ac8-269">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-269">String</span></span>|  
|<span data-ttu-id="d8ac8-270">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-270">TABLE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-271">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-271">String</span></span>|  
|<span data-ttu-id="d8ac8-272">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-272">TABLE_NAME</span></span>|<span data-ttu-id="d8ac8-273">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-273">String</span></span>|  
|<span data-ttu-id="d8ac8-274">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-274">INDEX_CATALOG</span></span>|<span data-ttu-id="d8ac8-275">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-275">String</span></span>|  
|<span data-ttu-id="d8ac8-276">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-276">INDEX_SCHEMA</span></span>|<span data-ttu-id="d8ac8-277">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-277">String</span></span>|  
|<span data-ttu-id="d8ac8-278">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-278">INDEX_NAME</span></span>|<span data-ttu-id="d8ac8-279">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-279">String</span></span>|  
|<span data-ttu-id="d8ac8-280">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="d8ac8-280">PRIMARY_KEY</span></span>|<span data-ttu-id="d8ac8-281">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-281">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-282">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-282">UNIQUE</span></span>|<span data-ttu-id="d8ac8-283">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-283">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-284">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-284">CLUSTERED</span></span>|<span data-ttu-id="d8ac8-285">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-285">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-286">TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-286">TYPE</span></span>|<span data-ttu-id="d8ac8-287">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-287">Int32</span></span>|  
|<span data-ttu-id="d8ac8-288">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="d8ac8-288">FILL_FACTOR</span></span>|<span data-ttu-id="d8ac8-289">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-289">Int32</span></span>|  
|<span data-ttu-id="d8ac8-290">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-290">INITIAL_SIZE</span></span>|<span data-ttu-id="d8ac8-291">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-291">Int32</span></span>|  
|<span data-ttu-id="d8ac8-292">NULLS</span><span class="sxs-lookup"><span data-stu-id="d8ac8-292">NULLS</span></span>|<span data-ttu-id="d8ac8-293">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-293">Int32</span></span>|  
|<span data-ttu-id="d8ac8-294">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d8ac8-294">SORT_BOOKMARKS</span></span>|<span data-ttu-id="d8ac8-295">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-295">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-296">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-296">AUTO_UPDATE</span></span>|<span data-ttu-id="d8ac8-297">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-297">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-298">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-298">NULL_COLLATION</span></span>|<span data-ttu-id="d8ac8-299">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-299">Int32</span></span>|  
|<span data-ttu-id="d8ac8-300">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-300">ORDINAL_POSITION</span></span>|<span data-ttu-id="d8ac8-301">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-301">Int64</span></span>|  
|<span data-ttu-id="d8ac8-302">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-302">COLUMN_NAME</span></span>|<span data-ttu-id="d8ac8-303">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-303">String</span></span>|  
|<span data-ttu-id="d8ac8-304">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-304">COLUMN_GUID</span></span>|<span data-ttu-id="d8ac8-305">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-305">Guid</span></span>|  
|<span data-ttu-id="d8ac8-306">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-306">COLUMN_PROPID</span></span>|<span data-ttu-id="d8ac8-307">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-307">Int64</span></span>|  
|<span data-ttu-id="d8ac8-308">COLLATION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-308">COLLATION</span></span>|<span data-ttu-id="d8ac8-309">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-309">Int16</span></span>|  
|<span data-ttu-id="d8ac8-310">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="d8ac8-310">CARDINALITY</span></span>|<span data-ttu-id="d8ac8-311">Decimal (10 進数型)</span><span class="sxs-lookup"><span data-stu-id="d8ac8-311">Decimal</span></span>|  
|<span data-ttu-id="d8ac8-312">PAGES</span><span class="sxs-lookup"><span data-stu-id="d8ac8-312">PAGES</span></span>|<span data-ttu-id="d8ac8-313">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-313">Int32</span></span>|  
|<span data-ttu-id="d8ac8-314">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-314">FILTER_CONDITION</span></span>|<span data-ttu-id="d8ac8-315">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-315">String</span></span>|  
|<span data-ttu-id="d8ac8-316">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-316">INTEGRATED</span></span>|<span data-ttu-id="d8ac8-317">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-317">Boolean</span></span>|  
  
## <a name="microsoft-oracle-ole-db-provider"></a><span data-ttu-id="d8ac8-318">Microsoft Oracle OLE DB Provider</span><span class="sxs-lookup"><span data-stu-id="d8ac8-318">Microsoft Oracle OLE DB Provider</span></span>  
 <span data-ttu-id="d8ac8-319">Microsoft Oracle OLE DB Driver は、共通のスキーマ コレクションに加えて次のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d8ac8-319">The Microsoft Oracle OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="d8ac8-320">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="d8ac8-320">Tables</span></span>  
  
-   <span data-ttu-id="d8ac8-321">列</span><span class="sxs-lookup"><span data-stu-id="d8ac8-321">Columns</span></span>  
  
-   <span data-ttu-id="d8ac8-322">手順</span><span class="sxs-lookup"><span data-stu-id="d8ac8-322">Procedures</span></span>  
  
-   <span data-ttu-id="d8ac8-323">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="d8ac8-323">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="d8ac8-324">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="d8ac8-324">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="d8ac8-325">ビュー</span><span class="sxs-lookup"><span data-stu-id="d8ac8-325">Views</span></span>  
  
-   <span data-ttu-id="d8ac8-326">Indexes</span><span class="sxs-lookup"><span data-stu-id="d8ac8-326">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="d8ac8-327">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="d8ac8-327">Tables</span></span>  
  
|<span data-ttu-id="d8ac8-328">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-328">ColumnName</span></span>|<span data-ttu-id="d8ac8-329">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-329">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-330">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-330">TABLE_CATALOG</span></span>|<span data-ttu-id="d8ac8-331">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-331">String</span></span>|  
|<span data-ttu-id="d8ac8-332">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-332">TABLE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-333">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-333">String</span></span>|  
|<span data-ttu-id="d8ac8-334">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-334">TABLE_NAME</span></span>|<span data-ttu-id="d8ac8-335">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-335">String</span></span>|  
|<span data-ttu-id="d8ac8-336">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-336">TABLE_TYPE</span></span>|<span data-ttu-id="d8ac8-337">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-337">String</span></span>|  
|<span data-ttu-id="d8ac8-338">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-338">TABLE_GUID</span></span>|<span data-ttu-id="d8ac8-339">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-339">Guid</span></span>|  
|<span data-ttu-id="d8ac8-340">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-340">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-341">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-341">String</span></span>|  
|<span data-ttu-id="d8ac8-342">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-342">TABLE_PROPID</span></span>|<span data-ttu-id="d8ac8-343">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-343">Int64</span></span>|  
|<span data-ttu-id="d8ac8-344">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-344">DATE_CREATED</span></span>|<span data-ttu-id="d8ac8-345">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-345">DateTime</span></span>|  
|<span data-ttu-id="d8ac8-346">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-346">DATE_MODIFIED</span></span>|<span data-ttu-id="d8ac8-347">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-347">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="d8ac8-348">列</span><span class="sxs-lookup"><span data-stu-id="d8ac8-348">Columns</span></span>  
  
|<span data-ttu-id="d8ac8-349">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-349">ColumnName</span></span>|<span data-ttu-id="d8ac8-350">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-350">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-351">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-351">TABLE_CATALOG</span></span>|<span data-ttu-id="d8ac8-352">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-352">String</span></span>|  
|<span data-ttu-id="d8ac8-353">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-353">TABLE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-354">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-354">String</span></span>|  
|<span data-ttu-id="d8ac8-355">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-355">TABLE_NAME</span></span>|<span data-ttu-id="d8ac8-356">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-356">String</span></span>|  
|<span data-ttu-id="d8ac8-357">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-357">COLUMN_NAME</span></span>|<span data-ttu-id="d8ac8-358">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-358">String</span></span>|  
|<span data-ttu-id="d8ac8-359">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-359">COLUMN_GUID</span></span>|<span data-ttu-id="d8ac8-360">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-360">Guid</span></span>|  
|<span data-ttu-id="d8ac8-361">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-361">COLUMN_PROPID</span></span>|<span data-ttu-id="d8ac8-362">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-362">Int64</span></span>|  
|<span data-ttu-id="d8ac8-363">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-363">ORDINAL_POSITION</span></span>|<span data-ttu-id="d8ac8-364">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-364">Int64</span></span>|  
|<span data-ttu-id="d8ac8-365">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="d8ac8-365">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="d8ac8-366">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-366">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-367">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d8ac8-367">COLUMN_DEFAULT</span></span>|<span data-ttu-id="d8ac8-368">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-368">String</span></span>|  
|<span data-ttu-id="d8ac8-369">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="d8ac8-369">COLUMN_FLAGS</span></span>|<span data-ttu-id="d8ac8-370">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-370">Int64</span></span>|  
|<span data-ttu-id="d8ac8-371">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-371">IS_NULLABLE</span></span>|<span data-ttu-id="d8ac8-372">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-372">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-373">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-373">DATA_TYPE</span></span>|<span data-ttu-id="d8ac8-374">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-374">Int32</span></span>|  
|<span data-ttu-id="d8ac8-375">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-375">TYPE_GUID</span></span>|<span data-ttu-id="d8ac8-376">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-376">Guid</span></span>|  
|<span data-ttu-id="d8ac8-377">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d8ac8-377">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="d8ac8-378">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-378">Int64</span></span>|  
|<span data-ttu-id="d8ac8-379">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d8ac8-379">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="d8ac8-380">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-380">Int64</span></span>|  
|<span data-ttu-id="d8ac8-381">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-381">NUMERIC_PRECISION</span></span>|<span data-ttu-id="d8ac8-382">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-382">Int32</span></span>|  
|<span data-ttu-id="d8ac8-383">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-383">NUMERIC_SCALE</span></span>|<span data-ttu-id="d8ac8-384">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-384">Int16</span></span>|  
|<span data-ttu-id="d8ac8-385">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-385">DATETIME_PRECISION</span></span>|<span data-ttu-id="d8ac8-386">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-386">Int64</span></span>|  
|<span data-ttu-id="d8ac8-387">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-387">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="d8ac8-388">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-388">String</span></span>|  
|<span data-ttu-id="d8ac8-389">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-389">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="d8ac8-390">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-390">String</span></span>|  
|<span data-ttu-id="d8ac8-391">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-391">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="d8ac8-392">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-392">String</span></span>|  
|<span data-ttu-id="d8ac8-393">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-393">COLLATION_CATALOG</span></span>|<span data-ttu-id="d8ac8-394">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-394">String</span></span>|  
|<span data-ttu-id="d8ac8-395">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-395">COLLATION_SCHEMA</span></span>|<span data-ttu-id="d8ac8-396">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-396">String</span></span>|  
|<span data-ttu-id="d8ac8-397">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-397">COLLATION_NAME</span></span>|<span data-ttu-id="d8ac8-398">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-398">String</span></span>|  
|<span data-ttu-id="d8ac8-399">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-399">DOMAIN_CATALOG</span></span>|<span data-ttu-id="d8ac8-400">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-400">String</span></span>|  
|<span data-ttu-id="d8ac8-401">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-401">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="d8ac8-402">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-402">String</span></span>|  
|<span data-ttu-id="d8ac8-403">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-403">DOMAIN_NAME</span></span>|<span data-ttu-id="d8ac8-404">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-404">String</span></span>|  
|<span data-ttu-id="d8ac8-405">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-405">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-406">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-406">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="d8ac8-407">手順</span><span class="sxs-lookup"><span data-stu-id="d8ac8-407">Procedures</span></span>  
  
|<span data-ttu-id="d8ac8-408">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-408">ColumnName</span></span>|<span data-ttu-id="d8ac8-409">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-409">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-410">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-410">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="d8ac8-411">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-411">String</span></span>|  
|<span data-ttu-id="d8ac8-412">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-412">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-413">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-413">String</span></span>|  
|<span data-ttu-id="d8ac8-414">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-414">PROCEDURE_NAME</span></span>|<span data-ttu-id="d8ac8-415">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-415">String</span></span>|  
|<span data-ttu-id="d8ac8-416">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-416">PROCEDURE_TYPE</span></span>|<span data-ttu-id="d8ac8-417">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-417">Int16</span></span>|  
|<span data-ttu-id="d8ac8-418">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-418">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="d8ac8-419">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-419">String</span></span>|  
|<span data-ttu-id="d8ac8-420">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-420">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-421">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-421">String</span></span>|  
|<span data-ttu-id="d8ac8-422">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-422">DATE_CREATED</span></span>|<span data-ttu-id="d8ac8-423">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-423">DateTime</span></span>|  
|<span data-ttu-id="d8ac8-424">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-424">DATE_MODIFIED</span></span>|<span data-ttu-id="d8ac8-425">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-425">DateTime</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="d8ac8-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="d8ac8-426">ProcedureColumns</span></span>  
  
|<span data-ttu-id="d8ac8-427">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-427">ColumnName</span></span>|<span data-ttu-id="d8ac8-428">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-428">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-429">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-429">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="d8ac8-430">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-430">String</span></span>|  
|<span data-ttu-id="d8ac8-431">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-431">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-432">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-432">String</span></span>|  
|<span data-ttu-id="d8ac8-433">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-433">PROCEDURE_NAME</span></span>|<span data-ttu-id="d8ac8-434">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-434">String</span></span>|  
|<span data-ttu-id="d8ac8-435">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-435">COLUMN_NAME</span></span>|<span data-ttu-id="d8ac8-436">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-436">String</span></span>|  
|<span data-ttu-id="d8ac8-437">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-437">COLUMN_GUID</span></span>|<span data-ttu-id="d8ac8-438">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-438">Guid</span></span>|  
|<span data-ttu-id="d8ac8-439">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-439">COLUMN_PROPID</span></span>|<span data-ttu-id="d8ac8-440">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-440">Int64</span></span>|  
|<span data-ttu-id="d8ac8-441">ROWSET_NUMBER</span><span class="sxs-lookup"><span data-stu-id="d8ac8-441">ROWSET_NUMBER</span></span>|<span data-ttu-id="d8ac8-442">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-442">Int64</span></span>|  
|<span data-ttu-id="d8ac8-443">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-443">ORDINAL_POSITION</span></span>|<span data-ttu-id="d8ac8-444">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-444">Int64</span></span>|  
|<span data-ttu-id="d8ac8-445">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-445">IS_NULLABLE</span></span>|<span data-ttu-id="d8ac8-446">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-446">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-447">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-447">DATA_TYPE</span></span>|<span data-ttu-id="d8ac8-448">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-448">Int32</span></span>|  
|<span data-ttu-id="d8ac8-449">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-449">TYPE_GUID</span></span>|<span data-ttu-id="d8ac8-450">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-450">Guid</span></span>|  
|<span data-ttu-id="d8ac8-451">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d8ac8-451">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="d8ac8-452">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-452">Int64</span></span>|  
|<span data-ttu-id="d8ac8-453">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d8ac8-453">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="d8ac8-454">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-454">Int64</span></span>|  
|<span data-ttu-id="d8ac8-455">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-455">NUMERIC_PRECISION</span></span>|<span data-ttu-id="d8ac8-456">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-456">Int32</span></span>|  
|<span data-ttu-id="d8ac8-457">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-457">NUMERIC_SCALE</span></span>|<span data-ttu-id="d8ac8-458">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-458">Int16</span></span>|  
|<span data-ttu-id="d8ac8-459">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-459">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-460">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-460">String</span></span>|  
|<span data-ttu-id="d8ac8-461">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="d8ac8-461">OVERLOAD</span></span>|<span data-ttu-id="d8ac8-462">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-462">Int16</span></span>|  
  
### <a name="views"></a><span data-ttu-id="d8ac8-463">ビュー</span><span class="sxs-lookup"><span data-stu-id="d8ac8-463">Views</span></span>  
  
|<span data-ttu-id="d8ac8-464">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-464">ColumnName</span></span>|<span data-ttu-id="d8ac8-465">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-465">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-466">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-466">TABLE_CATALOG</span></span>|<span data-ttu-id="d8ac8-467">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-467">String</span></span>|  
|<span data-ttu-id="d8ac8-468">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-468">TABLE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-469">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-469">String</span></span>|  
|<span data-ttu-id="d8ac8-470">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-470">TABLE_NAME</span></span>|<span data-ttu-id="d8ac8-471">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-471">String</span></span>|  
|<span data-ttu-id="d8ac8-472">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-472">VIEW_DEFINITION</span></span>|<span data-ttu-id="d8ac8-473">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-473">String</span></span>|  
|<span data-ttu-id="d8ac8-474">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-474">CHECK_OPTION</span></span>|<span data-ttu-id="d8ac8-475">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-475">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-476">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-476">IS_UPDATABLE</span></span>|<span data-ttu-id="d8ac8-477">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-477">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-478">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-478">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-479">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-479">String</span></span>|  
|<span data-ttu-id="d8ac8-480">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-480">DATE_CREATED</span></span>|<span data-ttu-id="d8ac8-481">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-481">DateTime</span></span>|  
|<span data-ttu-id="d8ac8-482">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-482">DATE_MODIFIED</span></span>|<span data-ttu-id="d8ac8-483">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-483">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="d8ac8-484">Indexes</span><span class="sxs-lookup"><span data-stu-id="d8ac8-484">Indexes</span></span>  
  
|<span data-ttu-id="d8ac8-485">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-485">ColumnName</span></span>|<span data-ttu-id="d8ac8-486">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-486">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-487">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-487">TABLE_CATALOG</span></span>|<span data-ttu-id="d8ac8-488">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-488">String</span></span>|  
|<span data-ttu-id="d8ac8-489">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-489">TABLE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-490">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-490">String</span></span>|  
|<span data-ttu-id="d8ac8-491">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-491">TABLE_NAME</span></span>|<span data-ttu-id="d8ac8-492">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-492">String</span></span>|  
|<span data-ttu-id="d8ac8-493">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-493">INDEX_CATALOG</span></span>|<span data-ttu-id="d8ac8-494">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-494">String</span></span>|  
|<span data-ttu-id="d8ac8-495">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-495">INDEX_SCHEMA</span></span>|<span data-ttu-id="d8ac8-496">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-496">String</span></span>|  
|<span data-ttu-id="d8ac8-497">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-497">INDEX_NAME</span></span>|<span data-ttu-id="d8ac8-498">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-498">String</span></span>|  
|<span data-ttu-id="d8ac8-499">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="d8ac8-499">PRIMARY_KEY</span></span>|<span data-ttu-id="d8ac8-500">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-500">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-501">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-501">UNIQUE</span></span>|<span data-ttu-id="d8ac8-502">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-502">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-503">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-503">CLUSTERED</span></span>|<span data-ttu-id="d8ac8-504">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-504">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-505">TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-505">TYPE</span></span>|<span data-ttu-id="d8ac8-506">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-506">Int32</span></span>|  
|<span data-ttu-id="d8ac8-507">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="d8ac8-507">FILL_FACTOR</span></span>|<span data-ttu-id="d8ac8-508">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-508">Int32</span></span>|  
|<span data-ttu-id="d8ac8-509">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-509">INITIAL_SIZE</span></span>|<span data-ttu-id="d8ac8-510">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-510">Int32</span></span>|  
|<span data-ttu-id="d8ac8-511">NULLS</span><span class="sxs-lookup"><span data-stu-id="d8ac8-511">NULLS</span></span>|<span data-ttu-id="d8ac8-512">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-512">Int32</span></span>|  
|<span data-ttu-id="d8ac8-513">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d8ac8-513">SORT_BOOKMARKS</span></span>|<span data-ttu-id="d8ac8-514">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-514">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-515">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-515">AUTO_UPDATE</span></span>|<span data-ttu-id="d8ac8-516">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-516">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-517">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-517">NULL_COLLATION</span></span>|<span data-ttu-id="d8ac8-518">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-518">Int32</span></span>|  
|<span data-ttu-id="d8ac8-519">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-519">ORDINAL_POSITION</span></span>|<span data-ttu-id="d8ac8-520">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-520">Int64</span></span>|  
|<span data-ttu-id="d8ac8-521">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-521">COLUMN_NAME</span></span>|<span data-ttu-id="d8ac8-522">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-522">String</span></span>|  
|<span data-ttu-id="d8ac8-523">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-523">COLUMN_GUID</span></span>|<span data-ttu-id="d8ac8-524">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-524">Guid</span></span>|  
|<span data-ttu-id="d8ac8-525">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-525">COLUMN_PROPID</span></span>|<span data-ttu-id="d8ac8-526">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-526">Int64</span></span>|  
|<span data-ttu-id="d8ac8-527">COLLATION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-527">COLLATION</span></span>|<span data-ttu-id="d8ac8-528">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-528">Int16</span></span>|  
|<span data-ttu-id="d8ac8-529">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="d8ac8-529">CARDINALITY</span></span>|<span data-ttu-id="d8ac8-530">Decimal (10 進数型)</span><span class="sxs-lookup"><span data-stu-id="d8ac8-530">Decimal</span></span>|  
|<span data-ttu-id="d8ac8-531">PAGES</span><span class="sxs-lookup"><span data-stu-id="d8ac8-531">PAGES</span></span>|<span data-ttu-id="d8ac8-532">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-532">Int32</span></span>|  
|<span data-ttu-id="d8ac8-533">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-533">FILTER_CONDITION</span></span>|<span data-ttu-id="d8ac8-534">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-534">String</span></span>|  
|<span data-ttu-id="d8ac8-535">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-535">INTEGRATED</span></span>|<span data-ttu-id="d8ac8-536">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-536">Boolean</span></span>|  
  
## <a name="microsoft-jet-ole-db-provider"></a><span data-ttu-id="d8ac8-537">Microsoft Jet OLE DB Provider</span><span class="sxs-lookup"><span data-stu-id="d8ac8-537">Microsoft Jet OLE DB Provider</span></span>  
 <span data-ttu-id="d8ac8-538">Microsoft Jet OLE DB Driver は、共通のスキーマ コレクションに加えて次のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d8ac8-538">The Microsoft Jet OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="d8ac8-539">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="d8ac8-539">Tables</span></span>  
  
-   <span data-ttu-id="d8ac8-540">列</span><span class="sxs-lookup"><span data-stu-id="d8ac8-540">Columns</span></span>  
  
-   <span data-ttu-id="d8ac8-541">手順</span><span class="sxs-lookup"><span data-stu-id="d8ac8-541">Procedures</span></span>  
  
-   <span data-ttu-id="d8ac8-542">ビュー</span><span class="sxs-lookup"><span data-stu-id="d8ac8-542">Views</span></span>  
  
-   <span data-ttu-id="d8ac8-543">Indexes</span><span class="sxs-lookup"><span data-stu-id="d8ac8-543">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="d8ac8-544">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="d8ac8-544">Tables</span></span>  
  
|<span data-ttu-id="d8ac8-545">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-545">ColumnName</span></span>|<span data-ttu-id="d8ac8-546">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-546">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-547">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-547">TABLE_CATALOG</span></span>|<span data-ttu-id="d8ac8-548">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-548">String</span></span>|  
|<span data-ttu-id="d8ac8-549">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-549">TABLE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-550">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-550">String</span></span>|  
|<span data-ttu-id="d8ac8-551">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-551">TABLE_NAME</span></span>|<span data-ttu-id="d8ac8-552">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-552">String</span></span>|  
|<span data-ttu-id="d8ac8-553">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-553">TABLE_TYPE</span></span>|<span data-ttu-id="d8ac8-554">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-554">String</span></span>|  
|<span data-ttu-id="d8ac8-555">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-555">TABLE_GUID</span></span>|<span data-ttu-id="d8ac8-556">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-556">Guid</span></span>|  
|<span data-ttu-id="d8ac8-557">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-557">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-558">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-558">String</span></span>|  
|<span data-ttu-id="d8ac8-559">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-559">TABLE_PROPID</span></span>|<span data-ttu-id="d8ac8-560">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-560">Int64</span></span>|  
|<span data-ttu-id="d8ac8-561">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-561">DATE_CREATED</span></span>|<span data-ttu-id="d8ac8-562">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-562">DateTime</span></span>|  
|<span data-ttu-id="d8ac8-563">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-563">DATE_MODIFIED</span></span>|<span data-ttu-id="d8ac8-564">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-564">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="d8ac8-565">列</span><span class="sxs-lookup"><span data-stu-id="d8ac8-565">Columns</span></span>  
  
|<span data-ttu-id="d8ac8-566">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-566">ColumnName</span></span>|<span data-ttu-id="d8ac8-567">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-567">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-568">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-568">TABLE_CATALOG</span></span>|<span data-ttu-id="d8ac8-569">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-569">String</span></span>|  
|<span data-ttu-id="d8ac8-570">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-570">TABLE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-571">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-571">String</span></span>|  
|<span data-ttu-id="d8ac8-572">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-572">TABLE_NAME</span></span>|<span data-ttu-id="d8ac8-573">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-573">String</span></span>|  
|<span data-ttu-id="d8ac8-574">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-574">COLUMN_NAME</span></span>|<span data-ttu-id="d8ac8-575">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-575">String</span></span>|  
|<span data-ttu-id="d8ac8-576">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-576">COLUMN_GUID</span></span>|<span data-ttu-id="d8ac8-577">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-577">Guid</span></span>|  
|<span data-ttu-id="d8ac8-578">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-578">COLUMN_PROPID</span></span>|<span data-ttu-id="d8ac8-579">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-579">Int64</span></span>|  
|<span data-ttu-id="d8ac8-580">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-580">ORDINAL_POSITION</span></span>|<span data-ttu-id="d8ac8-581">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-581">Int64</span></span>|  
|<span data-ttu-id="d8ac8-582">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="d8ac8-582">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="d8ac8-583">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-583">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-584">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d8ac8-584">COLUMN_DEFAULT</span></span>|<span data-ttu-id="d8ac8-585">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-585">String</span></span>|  
|<span data-ttu-id="d8ac8-586">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="d8ac8-586">COLUMN_FLAGS</span></span>|<span data-ttu-id="d8ac8-587">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-587">Int64</span></span>|  
|<span data-ttu-id="d8ac8-588">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-588">IS_NULLABLE</span></span>|<span data-ttu-id="d8ac8-589">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-589">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-590">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-590">DATA_TYPE</span></span>|<span data-ttu-id="d8ac8-591">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-591">Int32</span></span>|  
|<span data-ttu-id="d8ac8-592">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-592">TYPE_GUID</span></span>|<span data-ttu-id="d8ac8-593">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-593">Guid</span></span>|  
|<span data-ttu-id="d8ac8-594">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d8ac8-594">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="d8ac8-595">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-595">Int64</span></span>|  
|<span data-ttu-id="d8ac8-596">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d8ac8-596">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="d8ac8-597">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-597">Int64</span></span>|  
|<span data-ttu-id="d8ac8-598">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-598">NUMERIC_PRECISION</span></span>|<span data-ttu-id="d8ac8-599">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-599">Int32</span></span>|  
|<span data-ttu-id="d8ac8-600">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-600">NUMERIC_SCALE</span></span>|<span data-ttu-id="d8ac8-601">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-601">Int16</span></span>|  
|<span data-ttu-id="d8ac8-602">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-602">DATETIME_PRECISION</span></span>|<span data-ttu-id="d8ac8-603">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-603">Int64</span></span>|  
|<span data-ttu-id="d8ac8-604">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-604">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="d8ac8-605">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-605">String</span></span>|  
|<span data-ttu-id="d8ac8-606">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-606">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="d8ac8-607">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-607">String</span></span>|  
|<span data-ttu-id="d8ac8-608">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-608">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="d8ac8-609">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-609">String</span></span>|  
|<span data-ttu-id="d8ac8-610">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-610">COLLATION_CATALOG</span></span>|<span data-ttu-id="d8ac8-611">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-611">String</span></span>|  
|<span data-ttu-id="d8ac8-612">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-612">COLLATION_SCHEMA</span></span>|<span data-ttu-id="d8ac8-613">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-613">String</span></span>|  
|<span data-ttu-id="d8ac8-614">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-614">COLLATION_NAME</span></span>|<span data-ttu-id="d8ac8-615">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-615">String</span></span>|  
|<span data-ttu-id="d8ac8-616">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-616">DOMAIN_CATALOG</span></span>|<span data-ttu-id="d8ac8-617">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-617">String</span></span>|  
|<span data-ttu-id="d8ac8-618">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-618">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="d8ac8-619">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-619">String</span></span>|  
|<span data-ttu-id="d8ac8-620">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-620">DOMAIN_NAME</span></span>|<span data-ttu-id="d8ac8-621">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-621">String</span></span>|  
|<span data-ttu-id="d8ac8-622">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-622">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-623">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-623">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="d8ac8-624">手順</span><span class="sxs-lookup"><span data-stu-id="d8ac8-624">Procedures</span></span>  
  
|<span data-ttu-id="d8ac8-625">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-625">ColumnName</span></span>|<span data-ttu-id="d8ac8-626">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-626">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-627">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-627">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="d8ac8-628">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-628">String</span></span>|  
|<span data-ttu-id="d8ac8-629">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-629">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-630">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-630">String</span></span>|  
|<span data-ttu-id="d8ac8-631">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-631">PROCEDURE_NAME</span></span>|<span data-ttu-id="d8ac8-632">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-632">String</span></span>|  
|<span data-ttu-id="d8ac8-633">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-633">PROCEDURE_TYPE</span></span>|<span data-ttu-id="d8ac8-634">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-634">Int16</span></span>|  
|<span data-ttu-id="d8ac8-635">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-635">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="d8ac8-636">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-636">String</span></span>|  
|<span data-ttu-id="d8ac8-637">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-637">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-638">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-638">String</span></span>|  
|<span data-ttu-id="d8ac8-639">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-639">DATE_CREATED</span></span>|<span data-ttu-id="d8ac8-640">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-640">DateTime</span></span>|  
|<span data-ttu-id="d8ac8-641">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-641">DATE_MODIFIED</span></span>|<span data-ttu-id="d8ac8-642">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-642">DateTime</span></span>|  
  
### <a name="views"></a><span data-ttu-id="d8ac8-643">ビュー</span><span class="sxs-lookup"><span data-stu-id="d8ac8-643">Views</span></span>  
  
|<span data-ttu-id="d8ac8-644">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-644">ColumnName</span></span>|<span data-ttu-id="d8ac8-645">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-645">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-646">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-646">TABLE_CATALOG</span></span>|<span data-ttu-id="d8ac8-647">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-647">String</span></span>|  
|<span data-ttu-id="d8ac8-648">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-648">TABLE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-649">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-649">String</span></span>|  
|<span data-ttu-id="d8ac8-650">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-650">TABLE_NAME</span></span>|<span data-ttu-id="d8ac8-651">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-651">String</span></span>|  
|<span data-ttu-id="d8ac8-652">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-652">VIEW_DEFINITION</span></span>|<span data-ttu-id="d8ac8-653">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-653">String</span></span>|  
|<span data-ttu-id="d8ac8-654">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-654">CHECK_OPTION</span></span>|<span data-ttu-id="d8ac8-655">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-655">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-656">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-656">IS_UPDATABLE</span></span>|<span data-ttu-id="d8ac8-657">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-657">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-658">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-658">DESCRIPTION</span></span>|<span data-ttu-id="d8ac8-659">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-659">String</span></span>|  
|<span data-ttu-id="d8ac8-660">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-660">DATE_CREATED</span></span>|<span data-ttu-id="d8ac8-661">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-661">DateTime</span></span>|  
|<span data-ttu-id="d8ac8-662">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-662">DATE_MODIFIED</span></span>|<span data-ttu-id="d8ac8-663">DateTime</span><span class="sxs-lookup"><span data-stu-id="d8ac8-663">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="d8ac8-664">Indexes</span><span class="sxs-lookup"><span data-stu-id="d8ac8-664">Indexes</span></span>  
  
|<span data-ttu-id="d8ac8-665">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d8ac8-665">ColumnName</span></span>|<span data-ttu-id="d8ac8-666">DataType</span><span class="sxs-lookup"><span data-stu-id="d8ac8-666">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d8ac8-667">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-667">TABLE_CATALOG</span></span>|<span data-ttu-id="d8ac8-668">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-668">String</span></span>|  
|<span data-ttu-id="d8ac8-669">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-669">TABLE_SCHEMA</span></span>|<span data-ttu-id="d8ac8-670">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-670">String</span></span>|  
|<span data-ttu-id="d8ac8-671">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-671">TABLE_NAME</span></span>|<span data-ttu-id="d8ac8-672">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-672">String</span></span>|  
|<span data-ttu-id="d8ac8-673">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d8ac8-673">INDEX_CATALOG</span></span>|<span data-ttu-id="d8ac8-674">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-674">String</span></span>|  
|<span data-ttu-id="d8ac8-675">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d8ac8-675">INDEX_SCHEMA</span></span>|<span data-ttu-id="d8ac8-676">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-676">String</span></span>|  
|<span data-ttu-id="d8ac8-677">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-677">INDEX_NAME</span></span>|<span data-ttu-id="d8ac8-678">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-678">String</span></span>|  
|<span data-ttu-id="d8ac8-679">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="d8ac8-679">PRIMARY_KEY</span></span>|<span data-ttu-id="d8ac8-680">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-680">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-681">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-681">UNIQUE</span></span>|<span data-ttu-id="d8ac8-682">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-682">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-683">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-683">CLUSTERED</span></span>|<span data-ttu-id="d8ac8-684">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-684">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-685">TYPE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-685">TYPE</span></span>|<span data-ttu-id="d8ac8-686">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-686">Int32</span></span>|  
|<span data-ttu-id="d8ac8-687">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="d8ac8-687">FILL_FACTOR</span></span>|<span data-ttu-id="d8ac8-688">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-688">Int32</span></span>|  
|<span data-ttu-id="d8ac8-689">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-689">INITIAL_SIZE</span></span>|<span data-ttu-id="d8ac8-690">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-690">Int32</span></span>|  
|<span data-ttu-id="d8ac8-691">NULLS</span><span class="sxs-lookup"><span data-stu-id="d8ac8-691">NULLS</span></span>|<span data-ttu-id="d8ac8-692">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-692">Int32</span></span>|  
|<span data-ttu-id="d8ac8-693">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d8ac8-693">SORT_BOOKMARKS</span></span>|<span data-ttu-id="d8ac8-694">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-694">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-695">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="d8ac8-695">AUTO_UPDATE</span></span>|<span data-ttu-id="d8ac8-696">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ac8-696">Boolean</span></span>|  
|<span data-ttu-id="d8ac8-697">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-697">NULL_COLLATION</span></span>|<span data-ttu-id="d8ac8-698">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-698">Int32</span></span>|  
|<span data-ttu-id="d8ac8-699">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-699">ORDINAL_POSITION</span></span>|<span data-ttu-id="d8ac8-700">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-700">Int64</span></span>|  
|<span data-ttu-id="d8ac8-701">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d8ac8-701">COLUMN_NAME</span></span>|<span data-ttu-id="d8ac8-702">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-702">String</span></span>|  
|<span data-ttu-id="d8ac8-703">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-703">COLUMN_GUID</span></span>|<span data-ttu-id="d8ac8-704">Guid</span><span class="sxs-lookup"><span data-stu-id="d8ac8-704">Guid</span></span>|  
|<span data-ttu-id="d8ac8-705">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="d8ac8-705">COLUMN_PROPID</span></span>|<span data-ttu-id="d8ac8-706">Int64</span><span class="sxs-lookup"><span data-stu-id="d8ac8-706">Int64</span></span>|  
|<span data-ttu-id="d8ac8-707">COLLATION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-707">COLLATION</span></span>|<span data-ttu-id="d8ac8-708">Int16</span><span class="sxs-lookup"><span data-stu-id="d8ac8-708">Int16</span></span>|  
|<span data-ttu-id="d8ac8-709">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="d8ac8-709">CARDINALITY</span></span>|<span data-ttu-id="d8ac8-710">Decimal (10 進数型)</span><span class="sxs-lookup"><span data-stu-id="d8ac8-710">Decimal</span></span>|  
|<span data-ttu-id="d8ac8-711">PAGES</span><span class="sxs-lookup"><span data-stu-id="d8ac8-711">PAGES</span></span>|<span data-ttu-id="d8ac8-712">Int32</span><span class="sxs-lookup"><span data-stu-id="d8ac8-712">Int32</span></span>|  
|<span data-ttu-id="d8ac8-713">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="d8ac8-713">FILTER_CONDITION</span></span>|<span data-ttu-id="d8ac8-714">String</span><span class="sxs-lookup"><span data-stu-id="d8ac8-714">String</span></span>|  
|<span data-ttu-id="d8ac8-715">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="d8ac8-715">INTEGRATED</span></span>|<span data-ttu-id="d8ac8-716">ブール型</span><span class="sxs-lookup"><span data-stu-id="d8ac8-716">Boolean</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d8ac8-717">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8ac8-717">See Also</span></span>  
 [<span data-ttu-id="d8ac8-718">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="d8ac8-718">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
