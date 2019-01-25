---
title: OLE DB スキーマ コレクション
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: f753f35aab0a0200da5de463a73abb9813253d11
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54658456"
---
# <a name="ole-db-schema-collections"></a><span data-ttu-id="0b980-102">OLE DB スキーマ コレクション</span><span class="sxs-lookup"><span data-stu-id="0b980-102">OLE DB Schema Collections</span></span>
<span data-ttu-id="0b980-103">ここでは、Microsoft SQL Server、Oracle、および Microsoft Jet 用の各 OLE DB プロバイダーでのスキーマ コレクションのサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0b980-103">This section discusses schema collection support for the OLE DB providers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-ole-db-provider"></a><span data-ttu-id="0b980-104">Microsoft SQL Server OLE DB Provider</span><span class="sxs-lookup"><span data-stu-id="0b980-104">Microsoft SQL Server OLE DB Provider</span></span>  
 <span data-ttu-id="0b980-105">Microsoft SQL Server OLE DB Driver は、共通のスキーマ コレクションに加えて次の特定のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0b980-105">The Microsoft SQL Server OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="0b980-106">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="0b980-106">Tables</span></span>  
  
-   <span data-ttu-id="0b980-107">列</span><span class="sxs-lookup"><span data-stu-id="0b980-107">Columns</span></span>  
  
-   <span data-ttu-id="0b980-108">手順</span><span class="sxs-lookup"><span data-stu-id="0b980-108">Procedures</span></span>  
  
-   <span data-ttu-id="0b980-109">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0b980-109">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="0b980-110">Catalog</span><span class="sxs-lookup"><span data-stu-id="0b980-110">Catalog</span></span>  
  
-   <span data-ttu-id="0b980-111">Indexes</span><span class="sxs-lookup"><span data-stu-id="0b980-111">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="0b980-112">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="0b980-112">Tables</span></span>  
  
|<span data-ttu-id="0b980-113">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-113">ColumnName</span></span>|<span data-ttu-id="0b980-114">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-114">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-115">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-115">TABLE_CATALOG</span></span>|<span data-ttu-id="0b980-116">String</span><span class="sxs-lookup"><span data-stu-id="0b980-116">String</span></span>|  
|<span data-ttu-id="0b980-117">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-117">TABLE_SCHEMA</span></span>|<span data-ttu-id="0b980-118">String</span><span class="sxs-lookup"><span data-stu-id="0b980-118">String</span></span>|  
|<span data-ttu-id="0b980-119">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-119">TABLE_NAME</span></span>|<span data-ttu-id="0b980-120">String</span><span class="sxs-lookup"><span data-stu-id="0b980-120">String</span></span>|  
|<span data-ttu-id="0b980-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-121">TABLE_TYPE</span></span>|<span data-ttu-id="0b980-122">String</span><span class="sxs-lookup"><span data-stu-id="0b980-122">String</span></span>|  
|<span data-ttu-id="0b980-123">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-123">TABLE_GUID</span></span>|<span data-ttu-id="0b980-124">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-124">Guid</span></span>|  
|<span data-ttu-id="0b980-125">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-125">DESCRIPTION</span></span>|<span data-ttu-id="0b980-126">String</span><span class="sxs-lookup"><span data-stu-id="0b980-126">String</span></span>|  
|<span data-ttu-id="0b980-127">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="0b980-127">TABLE_PROPID</span></span>|<span data-ttu-id="0b980-128">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-128">Int64</span></span>|  
|<span data-ttu-id="0b980-129">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="0b980-129">DATE_CREATED</span></span>|<span data-ttu-id="0b980-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-130">DateTime</span></span>|  
|<span data-ttu-id="0b980-131">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="0b980-131">DATE_MODIFIED</span></span>|<span data-ttu-id="0b980-132">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-132">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="0b980-133">列</span><span class="sxs-lookup"><span data-stu-id="0b980-133">Columns</span></span>  
  
|<span data-ttu-id="0b980-134">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-134">ColumnName</span></span>|<span data-ttu-id="0b980-135">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-135">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-136">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-136">TABLE_CATALOG</span></span>|<span data-ttu-id="0b980-137">String</span><span class="sxs-lookup"><span data-stu-id="0b980-137">String</span></span>|  
|<span data-ttu-id="0b980-138">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-138">TABLE_SCHEMA</span></span>|<span data-ttu-id="0b980-139">String</span><span class="sxs-lookup"><span data-stu-id="0b980-139">String</span></span>|  
|<span data-ttu-id="0b980-140">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-140">TABLE_NAME</span></span>|<span data-ttu-id="0b980-141">String</span><span class="sxs-lookup"><span data-stu-id="0b980-141">String</span></span>|  
|<span data-ttu-id="0b980-142">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-142">COLUMN_NAME</span></span>|<span data-ttu-id="0b980-143">String</span><span class="sxs-lookup"><span data-stu-id="0b980-143">String</span></span>|  
|<span data-ttu-id="0b980-144">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-144">COLUMN_GUID</span></span>|<span data-ttu-id="0b980-145">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-145">Guid</span></span>|  
|<span data-ttu-id="0b980-146">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="0b980-146">COLUMN_PROPID</span></span>|<span data-ttu-id="0b980-147">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-147">Int64</span></span>|  
|<span data-ttu-id="0b980-148">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0b980-148">ORDINAL_POSITION</span></span>|<span data-ttu-id="0b980-149">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-149">Int64</span></span>|  
|<span data-ttu-id="0b980-150">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="0b980-150">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="0b980-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-151">Boolean</span></span>|  
|<span data-ttu-id="0b980-152">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0b980-152">COLUMN_DEFAULT</span></span>|<span data-ttu-id="0b980-153">String</span><span class="sxs-lookup"><span data-stu-id="0b980-153">String</span></span>|  
|<span data-ttu-id="0b980-154">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="0b980-154">COLUMN_FLAGS</span></span>|<span data-ttu-id="0b980-155">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-155">Int64</span></span>|  
|<span data-ttu-id="0b980-156">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0b980-156">IS_NULLABLE</span></span>|<span data-ttu-id="0b980-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-157">Boolean</span></span>|  
|<span data-ttu-id="0b980-158">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-158">DATA_TYPE</span></span>|<span data-ttu-id="0b980-159">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-159">Int32</span></span>|  
|<span data-ttu-id="0b980-160">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-160">TYPE_GUID</span></span>|<span data-ttu-id="0b980-161">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-161">Guid</span></span>|  
|<span data-ttu-id="0b980-162">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0b980-162">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="0b980-163">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-163">Int64</span></span>|  
|<span data-ttu-id="0b980-164">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0b980-164">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="0b980-165">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-165">Int64</span></span>|  
|<span data-ttu-id="0b980-166">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="0b980-166">NUMERIC_PRECISION</span></span>|<span data-ttu-id="0b980-167">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-167">Int32</span></span>|  
|<span data-ttu-id="0b980-168">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="0b980-168">NUMERIC_SCALE</span></span>|<span data-ttu-id="0b980-169">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-169">Int16</span></span>|  
|<span data-ttu-id="0b980-170">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="0b980-170">DATETIME_PRECISION</span></span>|<span data-ttu-id="0b980-171">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-171">Int64</span></span>|  
|<span data-ttu-id="0b980-172">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-172">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="0b980-173">String</span><span class="sxs-lookup"><span data-stu-id="0b980-173">String</span></span>|  
|<span data-ttu-id="0b980-174">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-174">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="0b980-175">String</span><span class="sxs-lookup"><span data-stu-id="0b980-175">String</span></span>|  
|<span data-ttu-id="0b980-176">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-176">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="0b980-177">String</span><span class="sxs-lookup"><span data-stu-id="0b980-177">String</span></span>|  
|<span data-ttu-id="0b980-178">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-178">COLLATION_CATALOG</span></span>|<span data-ttu-id="0b980-179">String</span><span class="sxs-lookup"><span data-stu-id="0b980-179">String</span></span>|  
|<span data-ttu-id="0b980-180">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-180">COLLATION_SCHEMA</span></span>|<span data-ttu-id="0b980-181">String</span><span class="sxs-lookup"><span data-stu-id="0b980-181">String</span></span>|  
|<span data-ttu-id="0b980-182">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-182">COLLATION_NAME</span></span>|<span data-ttu-id="0b980-183">String</span><span class="sxs-lookup"><span data-stu-id="0b980-183">String</span></span>|  
|<span data-ttu-id="0b980-184">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-184">DOMAIN_CATALOG</span></span>|<span data-ttu-id="0b980-185">String</span><span class="sxs-lookup"><span data-stu-id="0b980-185">String</span></span>|  
|<span data-ttu-id="0b980-186">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-186">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="0b980-187">String</span><span class="sxs-lookup"><span data-stu-id="0b980-187">String</span></span>|  
|<span data-ttu-id="0b980-188">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-188">DOMAIN_NAME</span></span>|<span data-ttu-id="0b980-189">String</span><span class="sxs-lookup"><span data-stu-id="0b980-189">String</span></span>|  
|<span data-ttu-id="0b980-190">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-190">DESCRIPTION</span></span>|<span data-ttu-id="0b980-191">String</span><span class="sxs-lookup"><span data-stu-id="0b980-191">String</span></span>|  
|<span data-ttu-id="0b980-192">COLUMN_LCID</span><span class="sxs-lookup"><span data-stu-id="0b980-192">COLUMN_LCID</span></span>|<span data-ttu-id="0b980-193">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-193">Int32</span></span>|  
|<span data-ttu-id="0b980-194">COLUMN_COMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="0b980-194">COLUMN_COMPFLAGS</span></span>|<span data-ttu-id="0b980-195">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-195">Int32</span></span>|  
|<span data-ttu-id="0b980-196">COLUMN_SORTID</span><span class="sxs-lookup"><span data-stu-id="0b980-196">COLUMN_SORTID</span></span>|<span data-ttu-id="0b980-197">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-197">Int32</span></span>|  
|<span data-ttu-id="0b980-198">COLUMN_TDSCOLLATION</span><span class="sxs-lookup"><span data-stu-id="0b980-198">COLUMN_TDSCOLLATION</span></span>|<span data-ttu-id="0b980-199">Byte[]</span><span class="sxs-lookup"><span data-stu-id="0b980-199">Byte[]</span></span>|  
|<span data-ttu-id="0b980-200">IS_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="0b980-200">IS_COMPUTED</span></span>|<span data-ttu-id="0b980-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-201">Boolean</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="0b980-202">手順</span><span class="sxs-lookup"><span data-stu-id="0b980-202">Procedures</span></span>  
  
|<span data-ttu-id="0b980-203">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-203">ColumnName</span></span>|<span data-ttu-id="0b980-204">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-204">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-205">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-205">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="0b980-206">String</span><span class="sxs-lookup"><span data-stu-id="0b980-206">String</span></span>|  
|<span data-ttu-id="0b980-207">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-207">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="0b980-208">String</span><span class="sxs-lookup"><span data-stu-id="0b980-208">String</span></span>|  
|<span data-ttu-id="0b980-209">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-209">PROCEDURE_NAME</span></span>|<span data-ttu-id="0b980-210">String</span><span class="sxs-lookup"><span data-stu-id="0b980-210">String</span></span>|  
|<span data-ttu-id="0b980-211">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-211">PROCEDURE_TYPE</span></span>|<span data-ttu-id="0b980-212">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-212">Int16</span></span>|  
|<span data-ttu-id="0b980-213">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="0b980-213">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="0b980-214">String</span><span class="sxs-lookup"><span data-stu-id="0b980-214">String</span></span>|  
|<span data-ttu-id="0b980-215">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-215">DESCRIPTION</span></span>|<span data-ttu-id="0b980-216">String</span><span class="sxs-lookup"><span data-stu-id="0b980-216">String</span></span>|  
|<span data-ttu-id="0b980-217">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="0b980-217">DATE_CREATED</span></span>|<span data-ttu-id="0b980-218">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-218">DateTime</span></span>|  
|<span data-ttu-id="0b980-219">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="0b980-219">DATE_MODIFIED</span></span>|<span data-ttu-id="0b980-220">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-220">DateTime</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="0b980-221">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0b980-221">ProcedureParameters</span></span>  
  
|<span data-ttu-id="0b980-222">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-222">ColumnName</span></span>|<span data-ttu-id="0b980-223">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-223">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-224">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-224">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="0b980-225">String</span><span class="sxs-lookup"><span data-stu-id="0b980-225">String</span></span>|  
|<span data-ttu-id="0b980-226">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-226">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="0b980-227">String</span><span class="sxs-lookup"><span data-stu-id="0b980-227">String</span></span>|  
|<span data-ttu-id="0b980-228">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-228">PROCEDURE_NAME</span></span>|<span data-ttu-id="0b980-229">String</span><span class="sxs-lookup"><span data-stu-id="0b980-229">String</span></span>|  
|<span data-ttu-id="0b980-230">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-230">PARAMETER_NAME</span></span>|<span data-ttu-id="0b980-231">String</span><span class="sxs-lookup"><span data-stu-id="0b980-231">String</span></span>|  
|<span data-ttu-id="0b980-232">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0b980-232">ORDINAL_POSITION</span></span>|<span data-ttu-id="0b980-233">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-233">Int32</span></span>|  
|<span data-ttu-id="0b980-234">PARAMETER_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-234">PARAMETER_TYPE</span></span>|<span data-ttu-id="0b980-235">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-235">Int32</span></span>|  
|<span data-ttu-id="0b980-236">PARAMETER_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="0b980-236">PARAMETER_HASDEFAULT</span></span>|<span data-ttu-id="0b980-237">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-237">Boolean</span></span>|  
|<span data-ttu-id="0b980-238">PARAMETER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0b980-238">PARAMETER_DEFAULT</span></span>|<span data-ttu-id="0b980-239">String</span><span class="sxs-lookup"><span data-stu-id="0b980-239">String</span></span>|  
|<span data-ttu-id="0b980-240">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0b980-240">IS_NULLABLE</span></span>|<span data-ttu-id="0b980-241">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-241">Boolean</span></span>|  
|<span data-ttu-id="0b980-242">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-242">DATA_TYPE</span></span>|<span data-ttu-id="0b980-243">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-243">Int32</span></span>|  
|<span data-ttu-id="0b980-244">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0b980-244">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="0b980-245">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-245">Int64</span></span>|  
|<span data-ttu-id="0b980-246">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0b980-246">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="0b980-247">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-247">Int64</span></span>|  
|<span data-ttu-id="0b980-248">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="0b980-248">NUMERIC_PRECISION</span></span>|<span data-ttu-id="0b980-249">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-249">Int32</span></span>|  
|<span data-ttu-id="0b980-250">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="0b980-250">NUMERIC_SCALE</span></span>|<span data-ttu-id="0b980-251">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-251">Int16</span></span>|  
|<span data-ttu-id="0b980-252">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-252">DESCRIPTION</span></span>|<span data-ttu-id="0b980-253">String</span><span class="sxs-lookup"><span data-stu-id="0b980-253">String</span></span>|  
|<span data-ttu-id="0b980-254">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-254">TYPE_NAME</span></span>|<span data-ttu-id="0b980-255">String</span><span class="sxs-lookup"><span data-stu-id="0b980-255">String</span></span>|  
|<span data-ttu-id="0b980-256">LOCAL_TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-256">LOCAL_TYPE_NAME</span></span>|<span data-ttu-id="0b980-257">String</span><span class="sxs-lookup"><span data-stu-id="0b980-257">String</span></span>|  
  
### <a name="catalog"></a><span data-ttu-id="0b980-258">Catalog</span><span class="sxs-lookup"><span data-stu-id="0b980-258">Catalog</span></span>  
  
|<span data-ttu-id="0b980-259">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-259">ColumnName</span></span>|<span data-ttu-id="0b980-260">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-260">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-261">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-261">CATALOG_NAME</span></span>|<span data-ttu-id="0b980-262">String</span><span class="sxs-lookup"><span data-stu-id="0b980-262">String</span></span>|  
|<span data-ttu-id="0b980-263">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-263">DESCRIPTION</span></span>|<span data-ttu-id="0b980-264">String</span><span class="sxs-lookup"><span data-stu-id="0b980-264">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="0b980-265">Indexes</span><span class="sxs-lookup"><span data-stu-id="0b980-265">Indexes</span></span>  
  
|<span data-ttu-id="0b980-266">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-266">ColumnName</span></span>|<span data-ttu-id="0b980-267">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-267">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-268">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-268">TABLE_CATALOG</span></span>|<span data-ttu-id="0b980-269">String</span><span class="sxs-lookup"><span data-stu-id="0b980-269">String</span></span>|  
|<span data-ttu-id="0b980-270">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-270">TABLE_SCHEMA</span></span>|<span data-ttu-id="0b980-271">String</span><span class="sxs-lookup"><span data-stu-id="0b980-271">String</span></span>|  
|<span data-ttu-id="0b980-272">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-272">TABLE_NAME</span></span>|<span data-ttu-id="0b980-273">String</span><span class="sxs-lookup"><span data-stu-id="0b980-273">String</span></span>|  
|<span data-ttu-id="0b980-274">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-274">INDEX_CATALOG</span></span>|<span data-ttu-id="0b980-275">String</span><span class="sxs-lookup"><span data-stu-id="0b980-275">String</span></span>|  
|<span data-ttu-id="0b980-276">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-276">INDEX_SCHEMA</span></span>|<span data-ttu-id="0b980-277">String</span><span class="sxs-lookup"><span data-stu-id="0b980-277">String</span></span>|  
|<span data-ttu-id="0b980-278">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-278">INDEX_NAME</span></span>|<span data-ttu-id="0b980-279">String</span><span class="sxs-lookup"><span data-stu-id="0b980-279">String</span></span>|  
|<span data-ttu-id="0b980-280">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="0b980-280">PRIMARY_KEY</span></span>|<span data-ttu-id="0b980-281">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-281">Boolean</span></span>|  
|<span data-ttu-id="0b980-282">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="0b980-282">UNIQUE</span></span>|<span data-ttu-id="0b980-283">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-283">Boolean</span></span>|  
|<span data-ttu-id="0b980-284">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="0b980-284">CLUSTERED</span></span>|<span data-ttu-id="0b980-285">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-285">Boolean</span></span>|  
|<span data-ttu-id="0b980-286">TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-286">TYPE</span></span>|<span data-ttu-id="0b980-287">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-287">Int32</span></span>|  
|<span data-ttu-id="0b980-288">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="0b980-288">FILL_FACTOR</span></span>|<span data-ttu-id="0b980-289">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-289">Int32</span></span>|  
|<span data-ttu-id="0b980-290">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="0b980-290">INITIAL_SIZE</span></span>|<span data-ttu-id="0b980-291">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-291">Int32</span></span>|  
|<span data-ttu-id="0b980-292">NULLS</span><span class="sxs-lookup"><span data-stu-id="0b980-292">NULLS</span></span>|<span data-ttu-id="0b980-293">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-293">Int32</span></span>|  
|<span data-ttu-id="0b980-294">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="0b980-294">SORT_BOOKMARKS</span></span>|<span data-ttu-id="0b980-295">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-295">Boolean</span></span>|  
|<span data-ttu-id="0b980-296">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="0b980-296">AUTO_UPDATE</span></span>|<span data-ttu-id="0b980-297">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-297">Boolean</span></span>|  
|<span data-ttu-id="0b980-298">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="0b980-298">NULL_COLLATION</span></span>|<span data-ttu-id="0b980-299">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-299">Int32</span></span>|  
|<span data-ttu-id="0b980-300">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0b980-300">ORDINAL_POSITION</span></span>|<span data-ttu-id="0b980-301">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-301">Int64</span></span>|  
|<span data-ttu-id="0b980-302">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-302">COLUMN_NAME</span></span>|<span data-ttu-id="0b980-303">String</span><span class="sxs-lookup"><span data-stu-id="0b980-303">String</span></span>|  
|<span data-ttu-id="0b980-304">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-304">COLUMN_GUID</span></span>|<span data-ttu-id="0b980-305">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-305">Guid</span></span>|  
|<span data-ttu-id="0b980-306">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="0b980-306">COLUMN_PROPID</span></span>|<span data-ttu-id="0b980-307">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-307">Int64</span></span>|  
|<span data-ttu-id="0b980-308">COLLATION</span><span class="sxs-lookup"><span data-stu-id="0b980-308">COLLATION</span></span>|<span data-ttu-id="0b980-309">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-309">Int16</span></span>|  
|<span data-ttu-id="0b980-310">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="0b980-310">CARDINALITY</span></span>|<span data-ttu-id="0b980-311">Decimal (10 進数型)</span><span class="sxs-lookup"><span data-stu-id="0b980-311">Decimal</span></span>|  
|<span data-ttu-id="0b980-312">PAGES</span><span class="sxs-lookup"><span data-stu-id="0b980-312">PAGES</span></span>|<span data-ttu-id="0b980-313">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-313">Int32</span></span>|  
|<span data-ttu-id="0b980-314">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="0b980-314">FILTER_CONDITION</span></span>|<span data-ttu-id="0b980-315">String</span><span class="sxs-lookup"><span data-stu-id="0b980-315">String</span></span>|  
|<span data-ttu-id="0b980-316">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="0b980-316">INTEGRATED</span></span>|<span data-ttu-id="0b980-317">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-317">Boolean</span></span>|  
  
## <a name="microsoft-oracle-ole-db-provider"></a><span data-ttu-id="0b980-318">Microsoft Oracle OLE DB Provider</span><span class="sxs-lookup"><span data-stu-id="0b980-318">Microsoft Oracle OLE DB Provider</span></span>  
 <span data-ttu-id="0b980-319">Microsoft Oracle OLE DB Driver は、共通のスキーマ コレクションに加えて次のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0b980-319">The Microsoft Oracle OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="0b980-320">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="0b980-320">Tables</span></span>  
  
-   <span data-ttu-id="0b980-321">列</span><span class="sxs-lookup"><span data-stu-id="0b980-321">Columns</span></span>  
  
-   <span data-ttu-id="0b980-322">手順</span><span class="sxs-lookup"><span data-stu-id="0b980-322">Procedures</span></span>  
  
-   <span data-ttu-id="0b980-323">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0b980-323">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="0b980-324">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0b980-324">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="0b980-325">ビュー</span><span class="sxs-lookup"><span data-stu-id="0b980-325">Views</span></span>  
  
-   <span data-ttu-id="0b980-326">Indexes</span><span class="sxs-lookup"><span data-stu-id="0b980-326">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="0b980-327">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="0b980-327">Tables</span></span>  
  
|<span data-ttu-id="0b980-328">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-328">ColumnName</span></span>|<span data-ttu-id="0b980-329">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-329">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-330">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-330">TABLE_CATALOG</span></span>|<span data-ttu-id="0b980-331">String</span><span class="sxs-lookup"><span data-stu-id="0b980-331">String</span></span>|  
|<span data-ttu-id="0b980-332">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-332">TABLE_SCHEMA</span></span>|<span data-ttu-id="0b980-333">String</span><span class="sxs-lookup"><span data-stu-id="0b980-333">String</span></span>|  
|<span data-ttu-id="0b980-334">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-334">TABLE_NAME</span></span>|<span data-ttu-id="0b980-335">String</span><span class="sxs-lookup"><span data-stu-id="0b980-335">String</span></span>|  
|<span data-ttu-id="0b980-336">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-336">TABLE_TYPE</span></span>|<span data-ttu-id="0b980-337">String</span><span class="sxs-lookup"><span data-stu-id="0b980-337">String</span></span>|  
|<span data-ttu-id="0b980-338">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-338">TABLE_GUID</span></span>|<span data-ttu-id="0b980-339">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-339">Guid</span></span>|  
|<span data-ttu-id="0b980-340">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-340">DESCRIPTION</span></span>|<span data-ttu-id="0b980-341">String</span><span class="sxs-lookup"><span data-stu-id="0b980-341">String</span></span>|  
|<span data-ttu-id="0b980-342">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="0b980-342">TABLE_PROPID</span></span>|<span data-ttu-id="0b980-343">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-343">Int64</span></span>|  
|<span data-ttu-id="0b980-344">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="0b980-344">DATE_CREATED</span></span>|<span data-ttu-id="0b980-345">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-345">DateTime</span></span>|  
|<span data-ttu-id="0b980-346">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="0b980-346">DATE_MODIFIED</span></span>|<span data-ttu-id="0b980-347">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-347">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="0b980-348">列</span><span class="sxs-lookup"><span data-stu-id="0b980-348">Columns</span></span>  
  
|<span data-ttu-id="0b980-349">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-349">ColumnName</span></span>|<span data-ttu-id="0b980-350">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-350">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-351">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-351">TABLE_CATALOG</span></span>|<span data-ttu-id="0b980-352">String</span><span class="sxs-lookup"><span data-stu-id="0b980-352">String</span></span>|  
|<span data-ttu-id="0b980-353">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-353">TABLE_SCHEMA</span></span>|<span data-ttu-id="0b980-354">String</span><span class="sxs-lookup"><span data-stu-id="0b980-354">String</span></span>|  
|<span data-ttu-id="0b980-355">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-355">TABLE_NAME</span></span>|<span data-ttu-id="0b980-356">String</span><span class="sxs-lookup"><span data-stu-id="0b980-356">String</span></span>|  
|<span data-ttu-id="0b980-357">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-357">COLUMN_NAME</span></span>|<span data-ttu-id="0b980-358">String</span><span class="sxs-lookup"><span data-stu-id="0b980-358">String</span></span>|  
|<span data-ttu-id="0b980-359">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-359">COLUMN_GUID</span></span>|<span data-ttu-id="0b980-360">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-360">Guid</span></span>|  
|<span data-ttu-id="0b980-361">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="0b980-361">COLUMN_PROPID</span></span>|<span data-ttu-id="0b980-362">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-362">Int64</span></span>|  
|<span data-ttu-id="0b980-363">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0b980-363">ORDINAL_POSITION</span></span>|<span data-ttu-id="0b980-364">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-364">Int64</span></span>|  
|<span data-ttu-id="0b980-365">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="0b980-365">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="0b980-366">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-366">Boolean</span></span>|  
|<span data-ttu-id="0b980-367">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0b980-367">COLUMN_DEFAULT</span></span>|<span data-ttu-id="0b980-368">String</span><span class="sxs-lookup"><span data-stu-id="0b980-368">String</span></span>|  
|<span data-ttu-id="0b980-369">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="0b980-369">COLUMN_FLAGS</span></span>|<span data-ttu-id="0b980-370">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-370">Int64</span></span>|  
|<span data-ttu-id="0b980-371">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0b980-371">IS_NULLABLE</span></span>|<span data-ttu-id="0b980-372">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-372">Boolean</span></span>|  
|<span data-ttu-id="0b980-373">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-373">DATA_TYPE</span></span>|<span data-ttu-id="0b980-374">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-374">Int32</span></span>|  
|<span data-ttu-id="0b980-375">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-375">TYPE_GUID</span></span>|<span data-ttu-id="0b980-376">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-376">Guid</span></span>|  
|<span data-ttu-id="0b980-377">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0b980-377">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="0b980-378">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-378">Int64</span></span>|  
|<span data-ttu-id="0b980-379">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0b980-379">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="0b980-380">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-380">Int64</span></span>|  
|<span data-ttu-id="0b980-381">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="0b980-381">NUMERIC_PRECISION</span></span>|<span data-ttu-id="0b980-382">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-382">Int32</span></span>|  
|<span data-ttu-id="0b980-383">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="0b980-383">NUMERIC_SCALE</span></span>|<span data-ttu-id="0b980-384">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-384">Int16</span></span>|  
|<span data-ttu-id="0b980-385">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="0b980-385">DATETIME_PRECISION</span></span>|<span data-ttu-id="0b980-386">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-386">Int64</span></span>|  
|<span data-ttu-id="0b980-387">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-387">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="0b980-388">String</span><span class="sxs-lookup"><span data-stu-id="0b980-388">String</span></span>|  
|<span data-ttu-id="0b980-389">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-389">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="0b980-390">String</span><span class="sxs-lookup"><span data-stu-id="0b980-390">String</span></span>|  
|<span data-ttu-id="0b980-391">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-391">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="0b980-392">String</span><span class="sxs-lookup"><span data-stu-id="0b980-392">String</span></span>|  
|<span data-ttu-id="0b980-393">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-393">COLLATION_CATALOG</span></span>|<span data-ttu-id="0b980-394">String</span><span class="sxs-lookup"><span data-stu-id="0b980-394">String</span></span>|  
|<span data-ttu-id="0b980-395">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-395">COLLATION_SCHEMA</span></span>|<span data-ttu-id="0b980-396">String</span><span class="sxs-lookup"><span data-stu-id="0b980-396">String</span></span>|  
|<span data-ttu-id="0b980-397">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-397">COLLATION_NAME</span></span>|<span data-ttu-id="0b980-398">String</span><span class="sxs-lookup"><span data-stu-id="0b980-398">String</span></span>|  
|<span data-ttu-id="0b980-399">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-399">DOMAIN_CATALOG</span></span>|<span data-ttu-id="0b980-400">String</span><span class="sxs-lookup"><span data-stu-id="0b980-400">String</span></span>|  
|<span data-ttu-id="0b980-401">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-401">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="0b980-402">String</span><span class="sxs-lookup"><span data-stu-id="0b980-402">String</span></span>|  
|<span data-ttu-id="0b980-403">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-403">DOMAIN_NAME</span></span>|<span data-ttu-id="0b980-404">String</span><span class="sxs-lookup"><span data-stu-id="0b980-404">String</span></span>|  
|<span data-ttu-id="0b980-405">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-405">DESCRIPTION</span></span>|<span data-ttu-id="0b980-406">String</span><span class="sxs-lookup"><span data-stu-id="0b980-406">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="0b980-407">手順</span><span class="sxs-lookup"><span data-stu-id="0b980-407">Procedures</span></span>  
  
|<span data-ttu-id="0b980-408">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-408">ColumnName</span></span>|<span data-ttu-id="0b980-409">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-409">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-410">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-410">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="0b980-411">String</span><span class="sxs-lookup"><span data-stu-id="0b980-411">String</span></span>|  
|<span data-ttu-id="0b980-412">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-412">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="0b980-413">String</span><span class="sxs-lookup"><span data-stu-id="0b980-413">String</span></span>|  
|<span data-ttu-id="0b980-414">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-414">PROCEDURE_NAME</span></span>|<span data-ttu-id="0b980-415">String</span><span class="sxs-lookup"><span data-stu-id="0b980-415">String</span></span>|  
|<span data-ttu-id="0b980-416">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-416">PROCEDURE_TYPE</span></span>|<span data-ttu-id="0b980-417">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-417">Int16</span></span>|  
|<span data-ttu-id="0b980-418">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="0b980-418">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="0b980-419">String</span><span class="sxs-lookup"><span data-stu-id="0b980-419">String</span></span>|  
|<span data-ttu-id="0b980-420">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-420">DESCRIPTION</span></span>|<span data-ttu-id="0b980-421">String</span><span class="sxs-lookup"><span data-stu-id="0b980-421">String</span></span>|  
|<span data-ttu-id="0b980-422">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="0b980-422">DATE_CREATED</span></span>|<span data-ttu-id="0b980-423">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-423">DateTime</span></span>|  
|<span data-ttu-id="0b980-424">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="0b980-424">DATE_MODIFIED</span></span>|<span data-ttu-id="0b980-425">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-425">DateTime</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="0b980-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0b980-426">ProcedureColumns</span></span>  
  
|<span data-ttu-id="0b980-427">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-427">ColumnName</span></span>|<span data-ttu-id="0b980-428">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-428">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-429">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-429">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="0b980-430">String</span><span class="sxs-lookup"><span data-stu-id="0b980-430">String</span></span>|  
|<span data-ttu-id="0b980-431">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-431">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="0b980-432">String</span><span class="sxs-lookup"><span data-stu-id="0b980-432">String</span></span>|  
|<span data-ttu-id="0b980-433">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-433">PROCEDURE_NAME</span></span>|<span data-ttu-id="0b980-434">String</span><span class="sxs-lookup"><span data-stu-id="0b980-434">String</span></span>|  
|<span data-ttu-id="0b980-435">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-435">COLUMN_NAME</span></span>|<span data-ttu-id="0b980-436">String</span><span class="sxs-lookup"><span data-stu-id="0b980-436">String</span></span>|  
|<span data-ttu-id="0b980-437">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-437">COLUMN_GUID</span></span>|<span data-ttu-id="0b980-438">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-438">Guid</span></span>|  
|<span data-ttu-id="0b980-439">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="0b980-439">COLUMN_PROPID</span></span>|<span data-ttu-id="0b980-440">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-440">Int64</span></span>|  
|<span data-ttu-id="0b980-441">ROWSET_NUMBER</span><span class="sxs-lookup"><span data-stu-id="0b980-441">ROWSET_NUMBER</span></span>|<span data-ttu-id="0b980-442">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-442">Int64</span></span>|  
|<span data-ttu-id="0b980-443">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0b980-443">ORDINAL_POSITION</span></span>|<span data-ttu-id="0b980-444">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-444">Int64</span></span>|  
|<span data-ttu-id="0b980-445">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0b980-445">IS_NULLABLE</span></span>|<span data-ttu-id="0b980-446">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-446">Boolean</span></span>|  
|<span data-ttu-id="0b980-447">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-447">DATA_TYPE</span></span>|<span data-ttu-id="0b980-448">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-448">Int32</span></span>|  
|<span data-ttu-id="0b980-449">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-449">TYPE_GUID</span></span>|<span data-ttu-id="0b980-450">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-450">Guid</span></span>|  
|<span data-ttu-id="0b980-451">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0b980-451">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="0b980-452">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-452">Int64</span></span>|  
|<span data-ttu-id="0b980-453">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0b980-453">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="0b980-454">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-454">Int64</span></span>|  
|<span data-ttu-id="0b980-455">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="0b980-455">NUMERIC_PRECISION</span></span>|<span data-ttu-id="0b980-456">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-456">Int32</span></span>|  
|<span data-ttu-id="0b980-457">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="0b980-457">NUMERIC_SCALE</span></span>|<span data-ttu-id="0b980-458">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-458">Int16</span></span>|  
|<span data-ttu-id="0b980-459">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-459">DESCRIPTION</span></span>|<span data-ttu-id="0b980-460">String</span><span class="sxs-lookup"><span data-stu-id="0b980-460">String</span></span>|  
|<span data-ttu-id="0b980-461">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="0b980-461">OVERLOAD</span></span>|<span data-ttu-id="0b980-462">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-462">Int16</span></span>|  
  
### <a name="views"></a><span data-ttu-id="0b980-463">ビュー</span><span class="sxs-lookup"><span data-stu-id="0b980-463">Views</span></span>  
  
|<span data-ttu-id="0b980-464">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-464">ColumnName</span></span>|<span data-ttu-id="0b980-465">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-465">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-466">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-466">TABLE_CATALOG</span></span>|<span data-ttu-id="0b980-467">String</span><span class="sxs-lookup"><span data-stu-id="0b980-467">String</span></span>|  
|<span data-ttu-id="0b980-468">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-468">TABLE_SCHEMA</span></span>|<span data-ttu-id="0b980-469">String</span><span class="sxs-lookup"><span data-stu-id="0b980-469">String</span></span>|  
|<span data-ttu-id="0b980-470">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-470">TABLE_NAME</span></span>|<span data-ttu-id="0b980-471">String</span><span class="sxs-lookup"><span data-stu-id="0b980-471">String</span></span>|  
|<span data-ttu-id="0b980-472">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="0b980-472">VIEW_DEFINITION</span></span>|<span data-ttu-id="0b980-473">String</span><span class="sxs-lookup"><span data-stu-id="0b980-473">String</span></span>|  
|<span data-ttu-id="0b980-474">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-474">CHECK_OPTION</span></span>|<span data-ttu-id="0b980-475">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-475">Boolean</span></span>|  
|<span data-ttu-id="0b980-476">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="0b980-476">IS_UPDATABLE</span></span>|<span data-ttu-id="0b980-477">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-477">Boolean</span></span>|  
|<span data-ttu-id="0b980-478">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-478">DESCRIPTION</span></span>|<span data-ttu-id="0b980-479">String</span><span class="sxs-lookup"><span data-stu-id="0b980-479">String</span></span>|  
|<span data-ttu-id="0b980-480">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="0b980-480">DATE_CREATED</span></span>|<span data-ttu-id="0b980-481">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-481">DateTime</span></span>|  
|<span data-ttu-id="0b980-482">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="0b980-482">DATE_MODIFIED</span></span>|<span data-ttu-id="0b980-483">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-483">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="0b980-484">Indexes</span><span class="sxs-lookup"><span data-stu-id="0b980-484">Indexes</span></span>  
  
|<span data-ttu-id="0b980-485">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-485">ColumnName</span></span>|<span data-ttu-id="0b980-486">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-486">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-487">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-487">TABLE_CATALOG</span></span>|<span data-ttu-id="0b980-488">String</span><span class="sxs-lookup"><span data-stu-id="0b980-488">String</span></span>|  
|<span data-ttu-id="0b980-489">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-489">TABLE_SCHEMA</span></span>|<span data-ttu-id="0b980-490">String</span><span class="sxs-lookup"><span data-stu-id="0b980-490">String</span></span>|  
|<span data-ttu-id="0b980-491">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-491">TABLE_NAME</span></span>|<span data-ttu-id="0b980-492">String</span><span class="sxs-lookup"><span data-stu-id="0b980-492">String</span></span>|  
|<span data-ttu-id="0b980-493">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-493">INDEX_CATALOG</span></span>|<span data-ttu-id="0b980-494">String</span><span class="sxs-lookup"><span data-stu-id="0b980-494">String</span></span>|  
|<span data-ttu-id="0b980-495">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-495">INDEX_SCHEMA</span></span>|<span data-ttu-id="0b980-496">String</span><span class="sxs-lookup"><span data-stu-id="0b980-496">String</span></span>|  
|<span data-ttu-id="0b980-497">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-497">INDEX_NAME</span></span>|<span data-ttu-id="0b980-498">String</span><span class="sxs-lookup"><span data-stu-id="0b980-498">String</span></span>|  
|<span data-ttu-id="0b980-499">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="0b980-499">PRIMARY_KEY</span></span>|<span data-ttu-id="0b980-500">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-500">Boolean</span></span>|  
|<span data-ttu-id="0b980-501">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="0b980-501">UNIQUE</span></span>|<span data-ttu-id="0b980-502">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-502">Boolean</span></span>|  
|<span data-ttu-id="0b980-503">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="0b980-503">CLUSTERED</span></span>|<span data-ttu-id="0b980-504">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-504">Boolean</span></span>|  
|<span data-ttu-id="0b980-505">TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-505">TYPE</span></span>|<span data-ttu-id="0b980-506">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-506">Int32</span></span>|  
|<span data-ttu-id="0b980-507">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="0b980-507">FILL_FACTOR</span></span>|<span data-ttu-id="0b980-508">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-508">Int32</span></span>|  
|<span data-ttu-id="0b980-509">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="0b980-509">INITIAL_SIZE</span></span>|<span data-ttu-id="0b980-510">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-510">Int32</span></span>|  
|<span data-ttu-id="0b980-511">NULLS</span><span class="sxs-lookup"><span data-stu-id="0b980-511">NULLS</span></span>|<span data-ttu-id="0b980-512">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-512">Int32</span></span>|  
|<span data-ttu-id="0b980-513">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="0b980-513">SORT_BOOKMARKS</span></span>|<span data-ttu-id="0b980-514">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-514">Boolean</span></span>|  
|<span data-ttu-id="0b980-515">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="0b980-515">AUTO_UPDATE</span></span>|<span data-ttu-id="0b980-516">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-516">Boolean</span></span>|  
|<span data-ttu-id="0b980-517">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="0b980-517">NULL_COLLATION</span></span>|<span data-ttu-id="0b980-518">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-518">Int32</span></span>|  
|<span data-ttu-id="0b980-519">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0b980-519">ORDINAL_POSITION</span></span>|<span data-ttu-id="0b980-520">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-520">Int64</span></span>|  
|<span data-ttu-id="0b980-521">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-521">COLUMN_NAME</span></span>|<span data-ttu-id="0b980-522">String</span><span class="sxs-lookup"><span data-stu-id="0b980-522">String</span></span>|  
|<span data-ttu-id="0b980-523">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-523">COLUMN_GUID</span></span>|<span data-ttu-id="0b980-524">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-524">Guid</span></span>|  
|<span data-ttu-id="0b980-525">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="0b980-525">COLUMN_PROPID</span></span>|<span data-ttu-id="0b980-526">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-526">Int64</span></span>|  
|<span data-ttu-id="0b980-527">COLLATION</span><span class="sxs-lookup"><span data-stu-id="0b980-527">COLLATION</span></span>|<span data-ttu-id="0b980-528">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-528">Int16</span></span>|  
|<span data-ttu-id="0b980-529">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="0b980-529">CARDINALITY</span></span>|<span data-ttu-id="0b980-530">Decimal (10 進数型)</span><span class="sxs-lookup"><span data-stu-id="0b980-530">Decimal</span></span>|  
|<span data-ttu-id="0b980-531">PAGES</span><span class="sxs-lookup"><span data-stu-id="0b980-531">PAGES</span></span>|<span data-ttu-id="0b980-532">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-532">Int32</span></span>|  
|<span data-ttu-id="0b980-533">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="0b980-533">FILTER_CONDITION</span></span>|<span data-ttu-id="0b980-534">String</span><span class="sxs-lookup"><span data-stu-id="0b980-534">String</span></span>|  
|<span data-ttu-id="0b980-535">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="0b980-535">INTEGRATED</span></span>|<span data-ttu-id="0b980-536">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-536">Boolean</span></span>|  
  
## <a name="microsoft-jet-ole-db-provider"></a><span data-ttu-id="0b980-537">Microsoft Jet OLE DB Provider</span><span class="sxs-lookup"><span data-stu-id="0b980-537">Microsoft Jet OLE DB Provider</span></span>  
 <span data-ttu-id="0b980-538">Microsoft Jet OLE DB Driver は、共通のスキーマ コレクションに加えて次のスキーマ コレクションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0b980-538">The Microsoft Jet OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="0b980-539">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="0b980-539">Tables</span></span>  
  
-   <span data-ttu-id="0b980-540">列</span><span class="sxs-lookup"><span data-stu-id="0b980-540">Columns</span></span>  
  
-   <span data-ttu-id="0b980-541">手順</span><span class="sxs-lookup"><span data-stu-id="0b980-541">Procedures</span></span>  
  
-   <span data-ttu-id="0b980-542">ビュー</span><span class="sxs-lookup"><span data-stu-id="0b980-542">Views</span></span>  
  
-   <span data-ttu-id="0b980-543">Indexes</span><span class="sxs-lookup"><span data-stu-id="0b980-543">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="0b980-544">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="0b980-544">Tables</span></span>  
  
|<span data-ttu-id="0b980-545">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-545">ColumnName</span></span>|<span data-ttu-id="0b980-546">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-546">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-547">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-547">TABLE_CATALOG</span></span>|<span data-ttu-id="0b980-548">String</span><span class="sxs-lookup"><span data-stu-id="0b980-548">String</span></span>|  
|<span data-ttu-id="0b980-549">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-549">TABLE_SCHEMA</span></span>|<span data-ttu-id="0b980-550">String</span><span class="sxs-lookup"><span data-stu-id="0b980-550">String</span></span>|  
|<span data-ttu-id="0b980-551">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-551">TABLE_NAME</span></span>|<span data-ttu-id="0b980-552">String</span><span class="sxs-lookup"><span data-stu-id="0b980-552">String</span></span>|  
|<span data-ttu-id="0b980-553">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-553">TABLE_TYPE</span></span>|<span data-ttu-id="0b980-554">String</span><span class="sxs-lookup"><span data-stu-id="0b980-554">String</span></span>|  
|<span data-ttu-id="0b980-555">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-555">TABLE_GUID</span></span>|<span data-ttu-id="0b980-556">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-556">Guid</span></span>|  
|<span data-ttu-id="0b980-557">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-557">DESCRIPTION</span></span>|<span data-ttu-id="0b980-558">String</span><span class="sxs-lookup"><span data-stu-id="0b980-558">String</span></span>|  
|<span data-ttu-id="0b980-559">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="0b980-559">TABLE_PROPID</span></span>|<span data-ttu-id="0b980-560">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-560">Int64</span></span>|  
|<span data-ttu-id="0b980-561">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="0b980-561">DATE_CREATED</span></span>|<span data-ttu-id="0b980-562">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-562">DateTime</span></span>|  
|<span data-ttu-id="0b980-563">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="0b980-563">DATE_MODIFIED</span></span>|<span data-ttu-id="0b980-564">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-564">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="0b980-565">列</span><span class="sxs-lookup"><span data-stu-id="0b980-565">Columns</span></span>  
  
|<span data-ttu-id="0b980-566">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-566">ColumnName</span></span>|<span data-ttu-id="0b980-567">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-567">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-568">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-568">TABLE_CATALOG</span></span>|<span data-ttu-id="0b980-569">String</span><span class="sxs-lookup"><span data-stu-id="0b980-569">String</span></span>|  
|<span data-ttu-id="0b980-570">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-570">TABLE_SCHEMA</span></span>|<span data-ttu-id="0b980-571">String</span><span class="sxs-lookup"><span data-stu-id="0b980-571">String</span></span>|  
|<span data-ttu-id="0b980-572">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-572">TABLE_NAME</span></span>|<span data-ttu-id="0b980-573">String</span><span class="sxs-lookup"><span data-stu-id="0b980-573">String</span></span>|  
|<span data-ttu-id="0b980-574">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-574">COLUMN_NAME</span></span>|<span data-ttu-id="0b980-575">String</span><span class="sxs-lookup"><span data-stu-id="0b980-575">String</span></span>|  
|<span data-ttu-id="0b980-576">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-576">COLUMN_GUID</span></span>|<span data-ttu-id="0b980-577">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-577">Guid</span></span>|  
|<span data-ttu-id="0b980-578">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="0b980-578">COLUMN_PROPID</span></span>|<span data-ttu-id="0b980-579">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-579">Int64</span></span>|  
|<span data-ttu-id="0b980-580">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0b980-580">ORDINAL_POSITION</span></span>|<span data-ttu-id="0b980-581">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-581">Int64</span></span>|  
|<span data-ttu-id="0b980-582">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="0b980-582">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="0b980-583">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-583">Boolean</span></span>|  
|<span data-ttu-id="0b980-584">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0b980-584">COLUMN_DEFAULT</span></span>|<span data-ttu-id="0b980-585">String</span><span class="sxs-lookup"><span data-stu-id="0b980-585">String</span></span>|  
|<span data-ttu-id="0b980-586">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="0b980-586">COLUMN_FLAGS</span></span>|<span data-ttu-id="0b980-587">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-587">Int64</span></span>|  
|<span data-ttu-id="0b980-588">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0b980-588">IS_NULLABLE</span></span>|<span data-ttu-id="0b980-589">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-589">Boolean</span></span>|  
|<span data-ttu-id="0b980-590">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-590">DATA_TYPE</span></span>|<span data-ttu-id="0b980-591">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-591">Int32</span></span>|  
|<span data-ttu-id="0b980-592">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-592">TYPE_GUID</span></span>|<span data-ttu-id="0b980-593">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-593">Guid</span></span>|  
|<span data-ttu-id="0b980-594">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0b980-594">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="0b980-595">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-595">Int64</span></span>|  
|<span data-ttu-id="0b980-596">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0b980-596">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="0b980-597">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-597">Int64</span></span>|  
|<span data-ttu-id="0b980-598">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="0b980-598">NUMERIC_PRECISION</span></span>|<span data-ttu-id="0b980-599">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-599">Int32</span></span>|  
|<span data-ttu-id="0b980-600">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="0b980-600">NUMERIC_SCALE</span></span>|<span data-ttu-id="0b980-601">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-601">Int16</span></span>|  
|<span data-ttu-id="0b980-602">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="0b980-602">DATETIME_PRECISION</span></span>|<span data-ttu-id="0b980-603">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-603">Int64</span></span>|  
|<span data-ttu-id="0b980-604">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-604">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="0b980-605">String</span><span class="sxs-lookup"><span data-stu-id="0b980-605">String</span></span>|  
|<span data-ttu-id="0b980-606">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-606">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="0b980-607">String</span><span class="sxs-lookup"><span data-stu-id="0b980-607">String</span></span>|  
|<span data-ttu-id="0b980-608">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-608">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="0b980-609">String</span><span class="sxs-lookup"><span data-stu-id="0b980-609">String</span></span>|  
|<span data-ttu-id="0b980-610">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-610">COLLATION_CATALOG</span></span>|<span data-ttu-id="0b980-611">String</span><span class="sxs-lookup"><span data-stu-id="0b980-611">String</span></span>|  
|<span data-ttu-id="0b980-612">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-612">COLLATION_SCHEMA</span></span>|<span data-ttu-id="0b980-613">String</span><span class="sxs-lookup"><span data-stu-id="0b980-613">String</span></span>|  
|<span data-ttu-id="0b980-614">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-614">COLLATION_NAME</span></span>|<span data-ttu-id="0b980-615">String</span><span class="sxs-lookup"><span data-stu-id="0b980-615">String</span></span>|  
|<span data-ttu-id="0b980-616">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-616">DOMAIN_CATALOG</span></span>|<span data-ttu-id="0b980-617">String</span><span class="sxs-lookup"><span data-stu-id="0b980-617">String</span></span>|  
|<span data-ttu-id="0b980-618">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-618">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="0b980-619">String</span><span class="sxs-lookup"><span data-stu-id="0b980-619">String</span></span>|  
|<span data-ttu-id="0b980-620">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-620">DOMAIN_NAME</span></span>|<span data-ttu-id="0b980-621">String</span><span class="sxs-lookup"><span data-stu-id="0b980-621">String</span></span>|  
|<span data-ttu-id="0b980-622">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-622">DESCRIPTION</span></span>|<span data-ttu-id="0b980-623">String</span><span class="sxs-lookup"><span data-stu-id="0b980-623">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="0b980-624">手順</span><span class="sxs-lookup"><span data-stu-id="0b980-624">Procedures</span></span>  
  
|<span data-ttu-id="0b980-625">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-625">ColumnName</span></span>|<span data-ttu-id="0b980-626">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-626">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-627">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-627">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="0b980-628">String</span><span class="sxs-lookup"><span data-stu-id="0b980-628">String</span></span>|  
|<span data-ttu-id="0b980-629">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-629">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="0b980-630">String</span><span class="sxs-lookup"><span data-stu-id="0b980-630">String</span></span>|  
|<span data-ttu-id="0b980-631">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-631">PROCEDURE_NAME</span></span>|<span data-ttu-id="0b980-632">String</span><span class="sxs-lookup"><span data-stu-id="0b980-632">String</span></span>|  
|<span data-ttu-id="0b980-633">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-633">PROCEDURE_TYPE</span></span>|<span data-ttu-id="0b980-634">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-634">Int16</span></span>|  
|<span data-ttu-id="0b980-635">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="0b980-635">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="0b980-636">String</span><span class="sxs-lookup"><span data-stu-id="0b980-636">String</span></span>|  
|<span data-ttu-id="0b980-637">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-637">DESCRIPTION</span></span>|<span data-ttu-id="0b980-638">String</span><span class="sxs-lookup"><span data-stu-id="0b980-638">String</span></span>|  
|<span data-ttu-id="0b980-639">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="0b980-639">DATE_CREATED</span></span>|<span data-ttu-id="0b980-640">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-640">DateTime</span></span>|  
|<span data-ttu-id="0b980-641">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="0b980-641">DATE_MODIFIED</span></span>|<span data-ttu-id="0b980-642">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-642">DateTime</span></span>|  
  
### <a name="views"></a><span data-ttu-id="0b980-643">ビュー</span><span class="sxs-lookup"><span data-stu-id="0b980-643">Views</span></span>  
  
|<span data-ttu-id="0b980-644">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-644">ColumnName</span></span>|<span data-ttu-id="0b980-645">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-645">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-646">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-646">TABLE_CATALOG</span></span>|<span data-ttu-id="0b980-647">String</span><span class="sxs-lookup"><span data-stu-id="0b980-647">String</span></span>|  
|<span data-ttu-id="0b980-648">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-648">TABLE_SCHEMA</span></span>|<span data-ttu-id="0b980-649">String</span><span class="sxs-lookup"><span data-stu-id="0b980-649">String</span></span>|  
|<span data-ttu-id="0b980-650">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-650">TABLE_NAME</span></span>|<span data-ttu-id="0b980-651">String</span><span class="sxs-lookup"><span data-stu-id="0b980-651">String</span></span>|  
|<span data-ttu-id="0b980-652">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="0b980-652">VIEW_DEFINITION</span></span>|<span data-ttu-id="0b980-653">String</span><span class="sxs-lookup"><span data-stu-id="0b980-653">String</span></span>|  
|<span data-ttu-id="0b980-654">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-654">CHECK_OPTION</span></span>|<span data-ttu-id="0b980-655">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-655">Boolean</span></span>|  
|<span data-ttu-id="0b980-656">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="0b980-656">IS_UPDATABLE</span></span>|<span data-ttu-id="0b980-657">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-657">Boolean</span></span>|  
|<span data-ttu-id="0b980-658">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b980-658">DESCRIPTION</span></span>|<span data-ttu-id="0b980-659">String</span><span class="sxs-lookup"><span data-stu-id="0b980-659">String</span></span>|  
|<span data-ttu-id="0b980-660">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="0b980-660">DATE_CREATED</span></span>|<span data-ttu-id="0b980-661">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-661">DateTime</span></span>|  
|<span data-ttu-id="0b980-662">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="0b980-662">DATE_MODIFIED</span></span>|<span data-ttu-id="0b980-663">DateTime</span><span class="sxs-lookup"><span data-stu-id="0b980-663">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="0b980-664">Indexes</span><span class="sxs-lookup"><span data-stu-id="0b980-664">Indexes</span></span>  
  
|<span data-ttu-id="0b980-665">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b980-665">ColumnName</span></span>|<span data-ttu-id="0b980-666">DataType</span><span class="sxs-lookup"><span data-stu-id="0b980-666">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0b980-667">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-667">TABLE_CATALOG</span></span>|<span data-ttu-id="0b980-668">String</span><span class="sxs-lookup"><span data-stu-id="0b980-668">String</span></span>|  
|<span data-ttu-id="0b980-669">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-669">TABLE_SCHEMA</span></span>|<span data-ttu-id="0b980-670">String</span><span class="sxs-lookup"><span data-stu-id="0b980-670">String</span></span>|  
|<span data-ttu-id="0b980-671">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-671">TABLE_NAME</span></span>|<span data-ttu-id="0b980-672">String</span><span class="sxs-lookup"><span data-stu-id="0b980-672">String</span></span>|  
|<span data-ttu-id="0b980-673">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0b980-673">INDEX_CATALOG</span></span>|<span data-ttu-id="0b980-674">String</span><span class="sxs-lookup"><span data-stu-id="0b980-674">String</span></span>|  
|<span data-ttu-id="0b980-675">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b980-675">INDEX_SCHEMA</span></span>|<span data-ttu-id="0b980-676">String</span><span class="sxs-lookup"><span data-stu-id="0b980-676">String</span></span>|  
|<span data-ttu-id="0b980-677">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-677">INDEX_NAME</span></span>|<span data-ttu-id="0b980-678">String</span><span class="sxs-lookup"><span data-stu-id="0b980-678">String</span></span>|  
|<span data-ttu-id="0b980-679">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="0b980-679">PRIMARY_KEY</span></span>|<span data-ttu-id="0b980-680">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-680">Boolean</span></span>|  
|<span data-ttu-id="0b980-681">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="0b980-681">UNIQUE</span></span>|<span data-ttu-id="0b980-682">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-682">Boolean</span></span>|  
|<span data-ttu-id="0b980-683">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="0b980-683">CLUSTERED</span></span>|<span data-ttu-id="0b980-684">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-684">Boolean</span></span>|  
|<span data-ttu-id="0b980-685">TYPE</span><span class="sxs-lookup"><span data-stu-id="0b980-685">TYPE</span></span>|<span data-ttu-id="0b980-686">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-686">Int32</span></span>|  
|<span data-ttu-id="0b980-687">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="0b980-687">FILL_FACTOR</span></span>|<span data-ttu-id="0b980-688">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-688">Int32</span></span>|  
|<span data-ttu-id="0b980-689">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="0b980-689">INITIAL_SIZE</span></span>|<span data-ttu-id="0b980-690">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-690">Int32</span></span>|  
|<span data-ttu-id="0b980-691">NULLS</span><span class="sxs-lookup"><span data-stu-id="0b980-691">NULLS</span></span>|<span data-ttu-id="0b980-692">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-692">Int32</span></span>|  
|<span data-ttu-id="0b980-693">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="0b980-693">SORT_BOOKMARKS</span></span>|<span data-ttu-id="0b980-694">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-694">Boolean</span></span>|  
|<span data-ttu-id="0b980-695">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="0b980-695">AUTO_UPDATE</span></span>|<span data-ttu-id="0b980-696">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b980-696">Boolean</span></span>|  
|<span data-ttu-id="0b980-697">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="0b980-697">NULL_COLLATION</span></span>|<span data-ttu-id="0b980-698">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-698">Int32</span></span>|  
|<span data-ttu-id="0b980-699">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0b980-699">ORDINAL_POSITION</span></span>|<span data-ttu-id="0b980-700">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-700">Int64</span></span>|  
|<span data-ttu-id="0b980-701">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0b980-701">COLUMN_NAME</span></span>|<span data-ttu-id="0b980-702">String</span><span class="sxs-lookup"><span data-stu-id="0b980-702">String</span></span>|  
|<span data-ttu-id="0b980-703">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="0b980-703">COLUMN_GUID</span></span>|<span data-ttu-id="0b980-704">Guid</span><span class="sxs-lookup"><span data-stu-id="0b980-704">Guid</span></span>|  
|<span data-ttu-id="0b980-705">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="0b980-705">COLUMN_PROPID</span></span>|<span data-ttu-id="0b980-706">Int64</span><span class="sxs-lookup"><span data-stu-id="0b980-706">Int64</span></span>|  
|<span data-ttu-id="0b980-707">COLLATION</span><span class="sxs-lookup"><span data-stu-id="0b980-707">COLLATION</span></span>|<span data-ttu-id="0b980-708">Int16</span><span class="sxs-lookup"><span data-stu-id="0b980-708">Int16</span></span>|  
|<span data-ttu-id="0b980-709">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="0b980-709">CARDINALITY</span></span>|<span data-ttu-id="0b980-710">Decimal (10 進数型)</span><span class="sxs-lookup"><span data-stu-id="0b980-710">Decimal</span></span>|  
|<span data-ttu-id="0b980-711">PAGES</span><span class="sxs-lookup"><span data-stu-id="0b980-711">PAGES</span></span>|<span data-ttu-id="0b980-712">Int32</span><span class="sxs-lookup"><span data-stu-id="0b980-712">Int32</span></span>|  
|<span data-ttu-id="0b980-713">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="0b980-713">FILTER_CONDITION</span></span>|<span data-ttu-id="0b980-714">String</span><span class="sxs-lookup"><span data-stu-id="0b980-714">String</span></span>|  
|<span data-ttu-id="0b980-715">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="0b980-715">INTEGRATED</span></span>|<span data-ttu-id="0b980-716">ブール型</span><span class="sxs-lookup"><span data-stu-id="0b980-716">Boolean</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0b980-717">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b980-717">See also</span></span>
- [<span data-ttu-id="0b980-718">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="0b980-718">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
