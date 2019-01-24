---
title: ガベージ コレクション ETW イベント
ms.date: 03/30/2017
helpviewer_keywords:
- GC events
- garbage collection events [.NET Framework]
- ETW, garbage collection events (CLR)
ms.assetid: f14b6fd7-0966-4d87-bc89-54ef3a44a94a
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 95762cbda4a1a251dd64fd33b2815d474f1fe2b9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54685218"
---
# <a name="garbage-collection-etw-events"></a><span data-ttu-id="84b38-102">ガベージ コレクション ETW イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-102">Garbage Collection ETW Events</span></span>
<a name="top"></a> <span data-ttu-id="84b38-103">これらのイベントは、ガベージ コレクションに関連する情報を収集します。</span><span class="sxs-lookup"><span data-stu-id="84b38-103">These events collect information pertaining to garbage collection.</span></span> <span data-ttu-id="84b38-104">ガベージ コレクションが実行された回数、ガベージ コレクションの間に解放されたメモリの量など、診断やデバッグに役立つ情報を入手できます。</span><span class="sxs-lookup"><span data-stu-id="84b38-104">They help in diagnostics and debugging, including determining how many times garbage collection was performed, how much memory was freed during garbage collection, and so on.</span></span>  
  
 <span data-ttu-id="84b38-105">このカテゴリは、次のイベントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="84b38-105">This category consists of the following events:</span></span>  
  
-   [<span data-ttu-id="84b38-106">GCStart_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-106">GCStart_V1 Event</span></span>](#gcstart_v1_event)  
  
-   [<span data-ttu-id="84b38-107">GCEnd_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-107">GCEnd_V1 Event</span></span>](#gcend_v1_event)  
  
-   [<span data-ttu-id="84b38-108">GCHeapStats_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-108">GCHeapStats_V1 Event</span></span>](#gcheapstats_v1_event)  
  
-   [<span data-ttu-id="84b38-109">GCCreateSegment_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-109">GCCreateSegment_V1 Event</span></span>](#gccreatesegment_v1_event)  
  
-   [<span data-ttu-id="84b38-110">GCFreeSegment_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-110">GCFreeSegment_V1 Event</span></span>](#gcfreesegment_v1_event)  
  
-   [<span data-ttu-id="84b38-111">GCRestartEEBegin_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-111">GCRestartEEBegin_V1 Event</span></span>](#gcrestarteebegin_v1_event)  
  
-   [<span data-ttu-id="84b38-112">GCRestartEEEnd_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-112">GCRestartEEEnd_V1 Event</span></span>](#gcrestarteeend_v1_event)  
  
-   [<span data-ttu-id="84b38-113">GCSuspendEE_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-113">GCSuspendEE_V1 Event</span></span>](#gcsuspendee_v1_event)  
  
-   [<span data-ttu-id="84b38-114">GCSuspendEEEnd_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-114">GCSuspendEEEnd_V1 Event</span></span>](#gcsuspendeeend_v1_event)  
  
-   [<span data-ttu-id="84b38-115">GCAllocationTick_V2 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-115">GCAllocationTick_V2 Event</span></span>](#gcallocationtick_v2_event)  
  
-   [<span data-ttu-id="84b38-116">GCFinalizersBegin_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-116">GCFinalizersBegin_V1 Event</span></span>](#gcfinalizersbegin_v1_event)  
  
-   [<span data-ttu-id="84b38-117">GCFinalizersEnd_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-117">GCFinalizersEnd_V1 Event</span></span>](#gcfinalizersend_v1_event)  
  
-   [<span data-ttu-id="84b38-118">GCCreateConcurrentThread_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-118">GCCreateConcurrentThread_V1 Event</span></span>](#gccreateconcurrentthread_v1_event)  
  
-   [<span data-ttu-id="84b38-119">GCTerminateConcurrentThread_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-119">GCTerminateConcurrentThread_V1 Event</span></span>](#gcterminateconcurrentthread_v1_event)  
  
<a name="gcstart_v1_event"></a>   
## <a name="gcstartv1-event"></a><span data-ttu-id="84b38-120">GCStart_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-120">GCStart_V1 Event</span></span>  
 <span data-ttu-id="84b38-121">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-121">The following table shows the keyword and level.</span></span> <span data-ttu-id="84b38-122">(詳細については、「 [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md)」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="84b38-122">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="84b38-123">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-123">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-124">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-124">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-125">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-125">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-126">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-126">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-127">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-127">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-128">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-128">Event</span></span>|<span data-ttu-id="84b38-129">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-129">Event ID</span></span>|<span data-ttu-id="84b38-130">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-130">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCStart_V1`|<span data-ttu-id="84b38-131">1</span><span class="sxs-lookup"><span data-stu-id="84b38-131">1</span></span>|<span data-ttu-id="84b38-132">ガベージ コレクションが開始されました。</span><span class="sxs-lookup"><span data-stu-id="84b38-132">A garbage collection has started.</span></span>|  
  
 <span data-ttu-id="84b38-133">次の表に、イベント データを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-133">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="84b38-134">フィールド名</span><span class="sxs-lookup"><span data-stu-id="84b38-134">Field name</span></span>|<span data-ttu-id="84b38-135">データ型</span><span class="sxs-lookup"><span data-stu-id="84b38-135">Data type</span></span>|<span data-ttu-id="84b38-136">説明</span><span class="sxs-lookup"><span data-stu-id="84b38-136">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="84b38-137">カウント</span><span class="sxs-lookup"><span data-stu-id="84b38-137">Count</span></span>|<span data-ttu-id="84b38-138">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-138">win:UInt32</span></span>|<span data-ttu-id="84b38-139">*n*回めのガベージ コレクション。</span><span class="sxs-lookup"><span data-stu-id="84b38-139">The *n*th garbage collection.</span></span>|  
|<span data-ttu-id="84b38-140">奥行</span><span class="sxs-lookup"><span data-stu-id="84b38-140">Depth</span></span>|<span data-ttu-id="84b38-141">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-141">win:UInt32</span></span>|<span data-ttu-id="84b38-142">収集されるジェネレーション。</span><span class="sxs-lookup"><span data-stu-id="84b38-142">The generation that is being collected.</span></span>|  
|<span data-ttu-id="84b38-143">理由</span><span class="sxs-lookup"><span data-stu-id="84b38-143">Reason</span></span>|<span data-ttu-id="84b38-144">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-144">win:UInt32</span></span>|<span data-ttu-id="84b38-145">ガベージ コレクションが発生した理由:</span><span class="sxs-lookup"><span data-stu-id="84b38-145">Why the garbage collection was triggered:</span></span><br /><br /> <span data-ttu-id="84b38-146">0x0 - 小さなオブジェクト ヒープの割り当て。</span><span class="sxs-lookup"><span data-stu-id="84b38-146">0x0 - Small object heap allocation.</span></span><br /><br /> <span data-ttu-id="84b38-147">0x1 - 強制実行。</span><span class="sxs-lookup"><span data-stu-id="84b38-147">0x1 - Induced.</span></span><br /><br /> <span data-ttu-id="84b38-148">0x2 - メモリ不足。</span><span class="sxs-lookup"><span data-stu-id="84b38-148">0x2 - Low memory.</span></span><br /><br /> <span data-ttu-id="84b38-149">0x3 - 空。</span><span class="sxs-lookup"><span data-stu-id="84b38-149">0x3 - Empty.</span></span><br /><br /> <span data-ttu-id="84b38-150">0x4 - 大きなオブジェクト ヒープの割り当て。</span><span class="sxs-lookup"><span data-stu-id="84b38-150">0x4 - Large object heap allocation.</span></span><br /><br /> <span data-ttu-id="84b38-151">0x5 - 領域不足 (小さなオブジェクト ヒープが対象)。</span><span class="sxs-lookup"><span data-stu-id="84b38-151">0x5 - Out of space (for small object heap).</span></span><br /><br /> <span data-ttu-id="84b38-152">0x6 - 領域不足 (大きなオブジェクト ヒープが対象)。</span><span class="sxs-lookup"><span data-stu-id="84b38-152">0x6 - Out of space (for large object heap).</span></span><br /><br /> <span data-ttu-id="84b38-153">0x7 - 強制実行されるが、ブロッキングとして強制されない。</span><span class="sxs-lookup"><span data-stu-id="84b38-153">0x7 - Induced but not forced as blocking.</span></span>|  
|<span data-ttu-id="84b38-154">型</span><span class="sxs-lookup"><span data-stu-id="84b38-154">Type</span></span>|<span data-ttu-id="84b38-155">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-155">win:UInt32</span></span>|<span data-ttu-id="84b38-156">0x0 - バックグラウンド ガベージ コレクションの外部で発生するブロッキング ガベージ コレクション。</span><span class="sxs-lookup"><span data-stu-id="84b38-156">0x0 - Blocking garbage collection occurred outside background garbage collection.</span></span><br /><br /> <span data-ttu-id="84b38-157">0x1 - バックグラウンド ガベージ コレクション。</span><span class="sxs-lookup"><span data-stu-id="84b38-157">0x1 - Background garbage collection.</span></span><br /><br /> <span data-ttu-id="84b38-158">0x2 - バックグラウンド ガベージ コレクションの実行中に発生するブロッキング ガベージ コレクション。</span><span class="sxs-lookup"><span data-stu-id="84b38-158">0x2 - Blocking garbage collection occurred during background garbage collection.</span></span>|  
|<span data-ttu-id="84b38-159">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="84b38-159">ClrInstanceID</span></span>|<span data-ttu-id="84b38-160">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="84b38-160">win:UInt16</span></span>|<span data-ttu-id="84b38-161">CLR または CoreCLR のインスタンスの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="84b38-161">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="84b38-162">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-162">Back to top</span></span>](#top)  
  
<a name="gcend_v1_event"></a>   
## <a name="gcendv1-event"></a><span data-ttu-id="84b38-163">GCEnd_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-163">GCEnd_V1 Event</span></span>  
 <span data-ttu-id="84b38-164">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-164">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-165">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-165">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-166">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-166">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-167">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-167">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-168">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-168">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-169">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-169">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-170">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-170">Event</span></span>|<span data-ttu-id="84b38-171">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-171">Event ID</span></span>|<span data-ttu-id="84b38-172">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-172">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCEnd_V1`|<span data-ttu-id="84b38-173">2</span><span class="sxs-lookup"><span data-stu-id="84b38-173">2</span></span>|<span data-ttu-id="84b38-174">ガベージ コレクションが終了しました。</span><span class="sxs-lookup"><span data-stu-id="84b38-174">The garbage collection has ended.</span></span>|  
  
 <span data-ttu-id="84b38-175">次の表に、イベント データを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-175">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="84b38-176">フィールド名</span><span class="sxs-lookup"><span data-stu-id="84b38-176">Field name</span></span>|<span data-ttu-id="84b38-177">データ型</span><span class="sxs-lookup"><span data-stu-id="84b38-177">Data type</span></span>|<span data-ttu-id="84b38-178">説明</span><span class="sxs-lookup"><span data-stu-id="84b38-178">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="84b38-179">カウント</span><span class="sxs-lookup"><span data-stu-id="84b38-179">Count</span></span>|<span data-ttu-id="84b38-180">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-180">win:UInt32</span></span>|<span data-ttu-id="84b38-181">*n*回めのガベージ コレクション。</span><span class="sxs-lookup"><span data-stu-id="84b38-181">The *n*th garbage collection.</span></span>|  
|<span data-ttu-id="84b38-182">奥行</span><span class="sxs-lookup"><span data-stu-id="84b38-182">Depth</span></span>|<span data-ttu-id="84b38-183">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-183">win:UInt32</span></span>|<span data-ttu-id="84b38-184">収集されたジェネレーション。</span><span class="sxs-lookup"><span data-stu-id="84b38-184">The generation that was collected.</span></span>|  
|<span data-ttu-id="84b38-185">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="84b38-185">ClrInstanceID</span></span>|<span data-ttu-id="84b38-186">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="84b38-186">win:UInt16</span></span>|<span data-ttu-id="84b38-187">CLR または CoreCLR のインスタンスの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="84b38-187">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="84b38-188">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-188">Back to top</span></span>](#top)  
  
<a name="gcheapstats_v1_event"></a>   
## <a name="gcheapstatsv1-event"></a><span data-ttu-id="84b38-189">GCHeapStats_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-189">GCHeapStats_V1 Event</span></span>  
 <span data-ttu-id="84b38-190">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-190">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-191">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-191">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-192">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-192">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-193">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-193">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-194">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-194">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-195">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-195">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-196">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-196">Event</span></span>|<span data-ttu-id="84b38-197">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-197">Event ID</span></span>|<span data-ttu-id="84b38-198">説明</span><span class="sxs-lookup"><span data-stu-id="84b38-198">Description</span></span>|  
|-----------|--------------|-----------------|  
|`GCHeapStats_V1`|<span data-ttu-id="84b38-199">4</span><span class="sxs-lookup"><span data-stu-id="84b38-199">4</span></span>|<span data-ttu-id="84b38-200">各ガベージ コレクション終了時のヒープの統計情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-200">Shows the heap statistics at the end of each garbage collection.</span></span>|  
  
 <span data-ttu-id="84b38-201">次の表に、イベント データを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-201">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="84b38-202">フィールド名</span><span class="sxs-lookup"><span data-stu-id="84b38-202">Field name</span></span>|<span data-ttu-id="84b38-203">データ型</span><span class="sxs-lookup"><span data-stu-id="84b38-203">Data type</span></span>|<span data-ttu-id="84b38-204">説明</span><span class="sxs-lookup"><span data-stu-id="84b38-204">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="84b38-205">GenerationSize0</span><span class="sxs-lookup"><span data-stu-id="84b38-205">GenerationSize0</span></span>|<span data-ttu-id="84b38-206">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-206">win:UInt64</span></span>|<span data-ttu-id="84b38-207">ジェネレーション 0 メモリのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="84b38-207">The size, in bytes, of generation 0 memory.</span></span>|  
|<span data-ttu-id="84b38-208">TotalPromotedSize0</span><span class="sxs-lookup"><span data-stu-id="84b38-208">TotalPromotedSize0</span></span>|<span data-ttu-id="84b38-209">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-209">win:UInt64</span></span>|<span data-ttu-id="84b38-210">ジェネレーション 0 からジェネレーション 1 に移されたバイト数。</span><span class="sxs-lookup"><span data-stu-id="84b38-210">The number of bytes that are promoted from generation 0 to generation 1.</span></span>|  
|<span data-ttu-id="84b38-211">GenerationSize1</span><span class="sxs-lookup"><span data-stu-id="84b38-211">GenerationSize1</span></span>|<span data-ttu-id="84b38-212">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-212">win:UInt64</span></span>|<span data-ttu-id="84b38-213">ジェネレーション 1 メモリのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="84b38-213">The size, in bytes, of generation 1 memory.</span></span>|  
|<span data-ttu-id="84b38-214">TotalPromotedSize1</span><span class="sxs-lookup"><span data-stu-id="84b38-214">TotalPromotedSize1</span></span>|<span data-ttu-id="84b38-215">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-215">win:UInt64</span></span>|<span data-ttu-id="84b38-216">ジェネレーション 1 からジェネレーション 2 に移されたバイト数。</span><span class="sxs-lookup"><span data-stu-id="84b38-216">The number of bytes that are promoted from generation 1 to generation 2.</span></span>|  
|<span data-ttu-id="84b38-217">GenerationSize2</span><span class="sxs-lookup"><span data-stu-id="84b38-217">GenerationSize2</span></span>|<span data-ttu-id="84b38-218">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-218">win:UInt64</span></span>|<span data-ttu-id="84b38-219">ジェネレーション 2 メモリのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="84b38-219">The size, in bytes, of generation 2 memory.</span></span>|  
|<span data-ttu-id="84b38-220">TotalPromotedSize2</span><span class="sxs-lookup"><span data-stu-id="84b38-220">TotalPromotedSize2</span></span>|<span data-ttu-id="84b38-221">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-221">win:UInt64</span></span>|<span data-ttu-id="84b38-222">最後のガベージ コレクションの後にジェネレーション 2 に残ったバイト数。</span><span class="sxs-lookup"><span data-stu-id="84b38-222">The number of bytes that survived in generation 2 after the last collection.</span></span>|  
|<span data-ttu-id="84b38-223">GenerationSize3</span><span class="sxs-lookup"><span data-stu-id="84b38-223">GenerationSize3</span></span>|<span data-ttu-id="84b38-224">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-224">win:UInt64</span></span>|<span data-ttu-id="84b38-225">大きなオブジェクト ヒープのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="84b38-225">The size, in bytes, of the large object heap.</span></span>|  
|<span data-ttu-id="84b38-226">TotalPromotedSize3</span><span class="sxs-lookup"><span data-stu-id="84b38-226">TotalPromotedSize3</span></span>|<span data-ttu-id="84b38-227">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-227">win:UInt64</span></span>|<span data-ttu-id="84b38-228">最後のガベージ コレクションの後に大きなオブジェクト ヒープに残ったバイト数。</span><span class="sxs-lookup"><span data-stu-id="84b38-228">The number of bytes that survived in the large object heap after the last collection.</span></span>|  
|<span data-ttu-id="84b38-229">FinalizationPromotedSize</span><span class="sxs-lookup"><span data-stu-id="84b38-229">FinalizationPromotedSize</span></span>|<span data-ttu-id="84b38-230">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-230">win:UInt64</span></span>|<span data-ttu-id="84b38-231">終了準備が完了しているオブジェクトの合計サイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="84b38-231">The total size, in bytes, of the objects that are ready for finalization.</span></span>|  
|<span data-ttu-id="84b38-232">FinalizationPromotedCount</span><span class="sxs-lookup"><span data-stu-id="84b38-232">FinalizationPromotedCount</span></span>|<span data-ttu-id="84b38-233">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-233">win:UInt64</span></span>|<span data-ttu-id="84b38-234">終了準備が完了しているオブジェクトの数。</span><span class="sxs-lookup"><span data-stu-id="84b38-234">The number of objects that are ready for finalization.</span></span>|  
|<span data-ttu-id="84b38-235">PinnedObjectCount</span><span class="sxs-lookup"><span data-stu-id="84b38-235">PinnedObjectCount</span></span>|<span data-ttu-id="84b38-236">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-236">win:UInt32</span></span>|<span data-ttu-id="84b38-237">ピン止めオブジェクト (移動できないオブジェクト) の数。</span><span class="sxs-lookup"><span data-stu-id="84b38-237">The number of pinned (unmovable) objects.</span></span>|  
|<span data-ttu-id="84b38-238">SinkBlockCount</span><span class="sxs-lookup"><span data-stu-id="84b38-238">SinkBlockCount</span></span>|<span data-ttu-id="84b38-239">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-239">win:UInt32</span></span>|<span data-ttu-id="84b38-240">使用中の同期ブロックの数。</span><span class="sxs-lookup"><span data-stu-id="84b38-240">The number of synchronization blocks in use.</span></span>|  
|<span data-ttu-id="84b38-241">GCHandleCount</span><span class="sxs-lookup"><span data-stu-id="84b38-241">GCHandleCount</span></span>|<span data-ttu-id="84b38-242">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-242">win:UInt32</span></span>|<span data-ttu-id="84b38-243">使用中のガベージ コレクション ハンドルの数。</span><span class="sxs-lookup"><span data-stu-id="84b38-243">The number of garbage collection handles in use.</span></span>|  
|<span data-ttu-id="84b38-244">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="84b38-244">ClrInstanceID</span></span>|<span data-ttu-id="84b38-245">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="84b38-245">win:UInt16</span></span>|<span data-ttu-id="84b38-246">CLR または CoreCLR のインスタンスの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="84b38-246">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="84b38-247">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-247">Back to top</span></span>](#top)  
  
<a name="gccreatesegment_v1_event"></a>   
## <a name="gccreatesegmentv1-event"></a><span data-ttu-id="84b38-248">GCCreateSegment_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-248">GCCreateSegment_V1 Event</span></span>  
 <span data-ttu-id="84b38-249">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-249">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-250">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-250">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-251">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-251">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-252">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-252">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-253">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-253">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-254">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-254">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-255">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-255">Event</span></span>|<span data-ttu-id="84b38-256">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-256">Event ID</span></span>|<span data-ttu-id="84b38-257">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-257">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCCreateSegment_V1`|<span data-ttu-id="84b38-258">5</span><span class="sxs-lookup"><span data-stu-id="84b38-258">5</span></span>|<span data-ttu-id="84b38-259">新しいガベージ コレクション セグメントが作成されました。</span><span class="sxs-lookup"><span data-stu-id="84b38-259">A new garbage collection segment has been created.</span></span> <span data-ttu-id="84b38-260">既に実行されているプロセスでトレースを有効にした場合は、このイベントが各既存セグメントについて発生します。</span><span class="sxs-lookup"><span data-stu-id="84b38-260">In addition, when tracing is enabled on a process that is already running, this event is raised for each existing segment.</span></span>|  
  
 <span data-ttu-id="84b38-261">次の表に、イベント データを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-261">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="84b38-262">フィールド名</span><span class="sxs-lookup"><span data-stu-id="84b38-262">Field name</span></span>|<span data-ttu-id="84b38-263">データ型</span><span class="sxs-lookup"><span data-stu-id="84b38-263">Data type</span></span>|<span data-ttu-id="84b38-264">説明</span><span class="sxs-lookup"><span data-stu-id="84b38-264">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="84b38-265">アドレス</span><span class="sxs-lookup"><span data-stu-id="84b38-265">Address</span></span>|<span data-ttu-id="84b38-266">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-266">win:UInt64</span></span>|<span data-ttu-id="84b38-267">セグメントのアドレス。</span><span class="sxs-lookup"><span data-stu-id="84b38-267">The address of the segment.</span></span>|  
|<span data-ttu-id="84b38-268">サイズ</span><span class="sxs-lookup"><span data-stu-id="84b38-268">Size</span></span>|<span data-ttu-id="84b38-269">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-269">win:UInt64</span></span>|<span data-ttu-id="84b38-270">セグメントのサイズ。</span><span class="sxs-lookup"><span data-stu-id="84b38-270">The size of the segment.</span></span>|  
|<span data-ttu-id="84b38-271">型</span><span class="sxs-lookup"><span data-stu-id="84b38-271">Type</span></span>|<span data-ttu-id="84b38-272">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-272">win:UInt32</span></span>|<span data-ttu-id="84b38-273">0x0 - 小さなオブジェクト ヒープ。</span><span class="sxs-lookup"><span data-stu-id="84b38-273">0x0 - Small object heap.</span></span><br /><br /> <span data-ttu-id="84b38-274">0x1 - 大きなオブジェクト ヒープ。</span><span class="sxs-lookup"><span data-stu-id="84b38-274">0x1 - Large object heap.</span></span><br /><br /> <span data-ttu-id="84b38-275">0x2 - 読み取り専用ヒープ。</span><span class="sxs-lookup"><span data-stu-id="84b38-275">0x2 - Read-only heap.</span></span>|  
|<span data-ttu-id="84b38-276">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="84b38-276">ClrInstanceID</span></span>|<span data-ttu-id="84b38-277">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="84b38-277">win:UInt16</span></span>|<span data-ttu-id="84b38-278">CLR または CoreCLR のインスタンスの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="84b38-278">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 <span data-ttu-id="84b38-279">ガベージ コレクターによって割り当てられるセグメントのサイズは実装に固有であり、定期的な更新プログラムによる場合を含め、いつでも変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="84b38-279">Note that the size of segments allocated by the garbage collector is implementation-specific and is subject to change at any time, including in periodic updates.</span></span> <span data-ttu-id="84b38-280">アプリでは、セグメント サイズを推測することや、特定のセグメント サイズに依存することを絶対に避けてください。また、セグメントの割り当てに使用可能なメモリの量を構成しようとしてもなりません。</span><span class="sxs-lookup"><span data-stu-id="84b38-280">Your app should never make assumptions about or depend on a particular segment size, nor should it attempt to configure the amount of memory available for segment allocations.</span></span>  
  
 [<span data-ttu-id="84b38-281">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-281">Back to top</span></span>](#top)  
  
<a name="gcfreesegment_v1_event"></a>   
## <a name="gcfreesegmentv1-event"></a><span data-ttu-id="84b38-282">GCFreeSegment_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-282">GCFreeSegment_V1 Event</span></span>  
 <span data-ttu-id="84b38-283">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-283">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-284">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-284">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-285">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-285">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-286">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-286">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-287">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-287">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-288">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-288">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-289">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-289">Event</span></span>|<span data-ttu-id="84b38-290">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-290">Event ID</span></span>|<span data-ttu-id="84b38-291">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-291">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCFreeSegment_V1`|<span data-ttu-id="84b38-292">6</span><span class="sxs-lookup"><span data-stu-id="84b38-292">6</span></span>|<span data-ttu-id="84b38-293">ガベージ コレクション セグメントが解放されました。</span><span class="sxs-lookup"><span data-stu-id="84b38-293">A garbage collection segment has been released.</span></span>|  
  
 <span data-ttu-id="84b38-294">次の表に、イベント データを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-294">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="84b38-295">フィールド名</span><span class="sxs-lookup"><span data-stu-id="84b38-295">Field name</span></span>|<span data-ttu-id="84b38-296">データ型</span><span class="sxs-lookup"><span data-stu-id="84b38-296">Data type</span></span>|<span data-ttu-id="84b38-297">説明</span><span class="sxs-lookup"><span data-stu-id="84b38-297">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="84b38-298">アドレス</span><span class="sxs-lookup"><span data-stu-id="84b38-298">Address</span></span>|<span data-ttu-id="84b38-299">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-299">win:UInt64</span></span>|<span data-ttu-id="84b38-300">セグメントのアドレス。</span><span class="sxs-lookup"><span data-stu-id="84b38-300">The address of the segment.</span></span>|  
|<span data-ttu-id="84b38-301">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="84b38-301">ClrInstanceID</span></span>|<span data-ttu-id="84b38-302">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="84b38-302">win:UInt16</span></span>|<span data-ttu-id="84b38-303">CLR または CoreCLR のインスタンスの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="84b38-303">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="84b38-304">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-304">Back to top</span></span>](#top)  
  
<a name="gcrestarteebegin_v1_event"></a>   
## <a name="gcrestarteebeginv1-event"></a><span data-ttu-id="84b38-305">GCRestartEEBegin_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-305">GCRestartEEBegin_V1 Event</span></span>  
 <span data-ttu-id="84b38-306">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-306">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-307">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-307">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-308">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-308">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-309">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-309">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-310">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-310">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-311">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-311">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-312">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-312">Event</span></span>|<span data-ttu-id="84b38-313">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-313">Event ID</span></span>|<span data-ttu-id="84b38-314">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-314">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCRestartEEBegin_V1`|<span data-ttu-id="84b38-315">7</span><span class="sxs-lookup"><span data-stu-id="84b38-315">7</span></span>|<span data-ttu-id="84b38-316">共通言語ランタイムの中断からの再開が開始されました。</span><span class="sxs-lookup"><span data-stu-id="84b38-316">Resumption from common language runtime suspension has begun.</span></span>|  
  
 <span data-ttu-id="84b38-317">イベント データはありません。</span><span class="sxs-lookup"><span data-stu-id="84b38-317">No event data.</span></span>  
  
 [<span data-ttu-id="84b38-318">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-318">Back to top</span></span>](#top)  
  
<a name="gcrestarteeend_v1_event"></a>   
## <a name="gcrestarteeendv1-event"></a><span data-ttu-id="84b38-319">GCRestartEEEnd_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-319">GCRestartEEEnd_V1 Event</span></span>  
 <span data-ttu-id="84b38-320">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-320">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-321">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-321">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-322">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-322">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-323">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-323">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-324">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-324">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-325">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-325">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-326">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-326">Event</span></span>|<span data-ttu-id="84b38-327">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-327">Event Id</span></span>|<span data-ttu-id="84b38-328">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-328">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCRestartEEEnd_V1`|<span data-ttu-id="84b38-329">3</span><span class="sxs-lookup"><span data-stu-id="84b38-329">3</span></span>|<span data-ttu-id="84b38-330">共通言語ランタイムの中断からの再開が終了しました。</span><span class="sxs-lookup"><span data-stu-id="84b38-330">Resumption from common language runtime suspension has ended.</span></span>|  
  
 <span data-ttu-id="84b38-331">イベント データはありません。</span><span class="sxs-lookup"><span data-stu-id="84b38-331">No event data.</span></span>  
  
 [<span data-ttu-id="84b38-332">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-332">Back to top</span></span>](#top)  
  
<a name="gcsuspendee_v1_event"></a>   
## <a name="gcsuspendeev1-event"></a><span data-ttu-id="84b38-333">GCSuspendEE_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-333">GCSuspendEE_V1 Event</span></span>  
 <span data-ttu-id="84b38-334">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-334">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-335">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-335">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-336">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-336">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-337">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-337">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-338">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-338">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-339">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-339">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-340">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-340">Event</span></span>|<span data-ttu-id="84b38-341">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-341">Event ID</span></span>|<span data-ttu-id="84b38-342">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-342">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCSuspendEE_V1`|<span data-ttu-id="84b38-343">9</span><span class="sxs-lookup"><span data-stu-id="84b38-343">9</span></span>|<span data-ttu-id="84b38-344">ガベージ コレクションのための実行エンジンの中断の開始。</span><span class="sxs-lookup"><span data-stu-id="84b38-344">Start of suspension of the execution engine for garbage collection.</span></span>|  
  
 <span data-ttu-id="84b38-345">次の表に、イベント データを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-345">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="84b38-346">フィールド名</span><span class="sxs-lookup"><span data-stu-id="84b38-346">Field name</span></span>|<span data-ttu-id="84b38-347">データ型</span><span class="sxs-lookup"><span data-stu-id="84b38-347">Data type</span></span>|<span data-ttu-id="84b38-348">説明</span><span class="sxs-lookup"><span data-stu-id="84b38-348">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="84b38-349">理由</span><span class="sxs-lookup"><span data-stu-id="84b38-349">Reason</span></span>|<span data-ttu-id="84b38-350">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="84b38-350">win:UInt16</span></span>|<span data-ttu-id="84b38-351">0x0 - その他。</span><span class="sxs-lookup"><span data-stu-id="84b38-351">0x0 - Other.</span></span><br /><br /> <span data-ttu-id="84b38-352">0x1 - ガベージ コレクション。</span><span class="sxs-lookup"><span data-stu-id="84b38-352">0x1 - Garbage collection.</span></span><br /><br /> <span data-ttu-id="84b38-353">0x2 - アプリケーション ドメインのシャットダウン。</span><span class="sxs-lookup"><span data-stu-id="84b38-353">0x2 - Application domain shutdown.</span></span><br /><br /> <span data-ttu-id="84b38-354">0x3 - コード ピッチ。</span><span class="sxs-lookup"><span data-stu-id="84b38-354">0x3 - Code pitching.</span></span><br /><br /> <span data-ttu-id="84b38-355">0x4 - シャットダウン。</span><span class="sxs-lookup"><span data-stu-id="84b38-355">0x4 - Shutdown.</span></span><br /><br /> <span data-ttu-id="84b38-356">0x5 - デバッガー。</span><span class="sxs-lookup"><span data-stu-id="84b38-356">0x5 - Debugger.</span></span><br /><br /> <span data-ttu-id="84b38-357">0x6 - ガベージ コレクションの準備。</span><span class="sxs-lookup"><span data-stu-id="84b38-357">0x6 - Preparation for garbage collection.</span></span>|  
|<span data-ttu-id="84b38-358">カウント</span><span class="sxs-lookup"><span data-stu-id="84b38-358">Count</span></span>|<span data-ttu-id="84b38-359">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-359">win:UInt32</span></span>|<span data-ttu-id="84b38-360">その時点の GC カウント。</span><span class="sxs-lookup"><span data-stu-id="84b38-360">The GC count at the time.</span></span> <span data-ttu-id="84b38-361">通常、この後に後続の GC 開始イベントが表示され、そのカウントは、ガベージ コレクション中に、GC インデックスが増えるため、このカウント + 1 になります。</span><span class="sxs-lookup"><span data-stu-id="84b38-361">Usually, you would see a subsequent GC Start event after this, and its Count would be this Count + 1 as we increase the GC index during a garbage collection.</span></span>|  
|<span data-ttu-id="84b38-362">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="84b38-362">ClrInstanceID</span></span>|<span data-ttu-id="84b38-363">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="84b38-363">win:UInt16</span></span>|<span data-ttu-id="84b38-364">CLR または CoreCLR のインスタンスの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="84b38-364">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="84b38-365">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-365">Back to top</span></span>](#top)  
  
<a name="gcsuspendeeend_v1_event"></a>   
## <a name="gcsuspendeeendv1-event"></a><span data-ttu-id="84b38-366">GCSuspendEEEnd_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-366">GCSuspendEEEnd_V1 Event</span></span>  
 <span data-ttu-id="84b38-367">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-367">The following table shows the keyword and level:</span></span>  
  
|<span data-ttu-id="84b38-368">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-368">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-369">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-369">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-370">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-370">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-371">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-371">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-372">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-372">The following table shows the event information:</span></span>  
  
|<span data-ttu-id="84b38-373">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-373">Event</span></span>|<span data-ttu-id="84b38-374">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-374">Event ID</span></span>|<span data-ttu-id="84b38-375">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-375">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCSuspendEEEnd_V1`|<span data-ttu-id="84b38-376">8</span><span class="sxs-lookup"><span data-stu-id="84b38-376">8</span></span>|<span data-ttu-id="84b38-377">ガベージ コレクションのための実行エンジンの中断の終了。</span><span class="sxs-lookup"><span data-stu-id="84b38-377">End of suspension of the execution engine for garbage collection.</span></span>|  
  
 <span data-ttu-id="84b38-378">イベント データはありません。</span><span class="sxs-lookup"><span data-stu-id="84b38-378">No event data.</span></span>  
  
 [<span data-ttu-id="84b38-379">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-379">Back to top</span></span>](#top)  
  
<a name="gcallocationtick_v2_event"></a>   
## <a name="gcallocationtickv2-event"></a><span data-ttu-id="84b38-380">GCAllocationTick_V2 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-380">GCAllocationTick_V2 Event</span></span>  
 <span data-ttu-id="84b38-381">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-381">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-382">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-382">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-383">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-383">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-384">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-384">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-385">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-385">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-386">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-386">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-387">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-387">Event</span></span>|<span data-ttu-id="84b38-388">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-388">Event ID</span></span>|<span data-ttu-id="84b38-389">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-389">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCAllocationTick_V2`|<span data-ttu-id="84b38-390">10</span><span class="sxs-lookup"><span data-stu-id="84b38-390">10</span></span>|<span data-ttu-id="84b38-391">約 100 KB が割り当てられるたび。</span><span class="sxs-lookup"><span data-stu-id="84b38-391">Each time approximately 100 KB is allocated.</span></span>|  
  
 <span data-ttu-id="84b38-392">次の表に、イベント データを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-392">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="84b38-393">フィールド名</span><span class="sxs-lookup"><span data-stu-id="84b38-393">Field name</span></span>|<span data-ttu-id="84b38-394">データ型</span><span class="sxs-lookup"><span data-stu-id="84b38-394">Data type</span></span>|<span data-ttu-id="84b38-395">説明</span><span class="sxs-lookup"><span data-stu-id="84b38-395">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="84b38-396">AllocationAmount</span><span class="sxs-lookup"><span data-stu-id="84b38-396">AllocationAmount</span></span>|<span data-ttu-id="84b38-397">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-397">win:UInt32</span></span>|<span data-ttu-id="84b38-398">割り当てサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="84b38-398">The allocation size, in bytes.</span></span> <span data-ttu-id="84b38-399">この値は、ULONG (4,294,967,295 バイト) の長さより短い割り当ての場合に正確です。</span><span class="sxs-lookup"><span data-stu-id="84b38-399">This value is accurate for allocations that are less than the length of a ULONG (4,294,967,295 bytes).</span></span> <span data-ttu-id="84b38-400">割り当てがこれを超える場合、このフィールドには切り捨てられた値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="84b38-400">If the allocation is greater, this field contains a truncated value.</span></span> <span data-ttu-id="84b38-401">非常に大きな割り当てには `AllocationAmount64` を使用します。</span><span class="sxs-lookup"><span data-stu-id="84b38-401">Use `AllocationAmount64` for very large allocations.</span></span>|  
|<span data-ttu-id="84b38-402">AllocationKind</span><span class="sxs-lookup"><span data-stu-id="84b38-402">AllocationKind</span></span>|<span data-ttu-id="84b38-403">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-403">win:UInt32</span></span>|<span data-ttu-id="84b38-404">0x0 - 小さなオブジェクトの割り当て (小さなオブジェクト ヒープへの割り当て)。</span><span class="sxs-lookup"><span data-stu-id="84b38-404">0x0 - Small object allocation (allocation is in small object heap).</span></span><br /><br /> <span data-ttu-id="84b38-405">0x1 - 大きなオブジェクトの割り当て (大きなオブジェクト ヒープへの割り当て)。</span><span class="sxs-lookup"><span data-stu-id="84b38-405">0x1 - Large object allocation (allocation is in large object heap).</span></span>|  
|<span data-ttu-id="84b38-406">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="84b38-406">ClrInstanceID</span></span>|<span data-ttu-id="84b38-407">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="84b38-407">win:UInt16</span></span>|<span data-ttu-id="84b38-408">CLR または CoreCLR のインスタンスの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="84b38-408">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
|<span data-ttu-id="84b38-409">AllocationAmount64</span><span class="sxs-lookup"><span data-stu-id="84b38-409">AllocationAmount64</span></span>|<span data-ttu-id="84b38-410">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="84b38-410">win:UInt64</span></span>|<span data-ttu-id="84b38-411">割り当てサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="84b38-411">The allocation size, in bytes.</span></span> <span data-ttu-id="84b38-412">この値は非常に大きな割り当ての場合に正確です。</span><span class="sxs-lookup"><span data-stu-id="84b38-412">This value is accurate for very large allocations.</span></span>|  
|<span data-ttu-id="84b38-413">TypeId</span><span class="sxs-lookup"><span data-stu-id="84b38-413">TypeId</span></span>|<span data-ttu-id="84b38-414">win:Pointer</span><span class="sxs-lookup"><span data-stu-id="84b38-414">win:Pointer</span></span>|<span data-ttu-id="84b38-415">MethodTable のアドレス。</span><span class="sxs-lookup"><span data-stu-id="84b38-415">The address of the MethodTable.</span></span> <span data-ttu-id="84b38-416">このイベント中に複数の型のオブジェクトが割り当てられた場合、これは最後に割り当てられたオブジェクト (100 KB のしきい値を超えたオブジェクト) に対応する MethodTable のアドレスです。</span><span class="sxs-lookup"><span data-stu-id="84b38-416">When there are several types of objects that were allocated during this event, this is the address of the MethodTable that corresponds to the last object allocated (the object that caused the 100 KB threshold to be exceeded).</span></span>|  
|<span data-ttu-id="84b38-417">TypeName</span><span class="sxs-lookup"><span data-stu-id="84b38-417">TypeName</span></span>|<span data-ttu-id="84b38-418">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="84b38-418">win:UnicodeString</span></span>|<span data-ttu-id="84b38-419">割り当てられた型の名前。</span><span class="sxs-lookup"><span data-stu-id="84b38-419">The name of the type that was allocated.</span></span> <span data-ttu-id="84b38-420">このイベント中に複数の型のオブジェクトが割り当てられた場合は、これは最後に割り当てられたオブジェクト (100 KB のしきい値を超えたオブジェクト) の型です。</span><span class="sxs-lookup"><span data-stu-id="84b38-420">When there are several types of objects that were allocated during this event, this is the type of the last object allocated (the object that caused the 100 KB threshold to be exceeded).</span></span>|  
|<span data-ttu-id="84b38-421">HeapIndex</span><span class="sxs-lookup"><span data-stu-id="84b38-421">HeapIndex</span></span>|<span data-ttu-id="84b38-422">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-422">win:UInt32</span></span>|<span data-ttu-id="84b38-423">オブジェクトが割り当てられたヒープ。</span><span class="sxs-lookup"><span data-stu-id="84b38-423">The heap where the object was allocated.</span></span> <span data-ttu-id="84b38-424">ワークステーションのガベージ コレクションと共に実行する場合、この値は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="84b38-424">This value is 0 (zero) when running with workstation garbage collection.</span></span>|  
  
 [<span data-ttu-id="84b38-425">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-425">Back to top</span></span>](#top)  
  
<a name="gcfinalizersbegin_v1_event"></a>   
## <a name="gcfinalizersbeginv1-event"></a><span data-ttu-id="84b38-426">GCFinalizersBegin_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-426">GCFinalizersBegin_V1 Event</span></span>  
 <span data-ttu-id="84b38-427">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-427">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-428">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-428">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-429">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-429">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-430">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-430">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-431">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-431">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-432">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-432">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-433">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-433">Event</span></span>|<span data-ttu-id="84b38-434">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-434">Event ID</span></span>|<span data-ttu-id="84b38-435">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-435">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCFinalizersBegin_V1`|<span data-ttu-id="84b38-436">14</span><span class="sxs-lookup"><span data-stu-id="84b38-436">14</span></span>|<span data-ttu-id="84b38-437">ファイナライザーの実行の開始。</span><span class="sxs-lookup"><span data-stu-id="84b38-437">The start of running finalizers.</span></span>|  
  
 <span data-ttu-id="84b38-438">イベント データはありません。</span><span class="sxs-lookup"><span data-stu-id="84b38-438">No event data.</span></span>  
  
 [<span data-ttu-id="84b38-439">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-439">Back to top</span></span>](#top)  
  
<a name="gcfinalizersend_v1_event"></a>   
## <a name="gcfinalizersendv1-event"></a><span data-ttu-id="84b38-440">GCFinalizersEnd_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-440">GCFinalizersEnd_V1 Event</span></span>  
 <span data-ttu-id="84b38-441">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-441">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-442">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-442">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-443">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-443">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-444">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-444">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-445">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-445">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-446">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-446">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-447">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-447">Event</span></span>|<span data-ttu-id="84b38-448">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-448">Event ID</span></span>|<span data-ttu-id="84b38-449">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-449">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCFinalizersEnd_V1`|<span data-ttu-id="84b38-450">13</span><span class="sxs-lookup"><span data-stu-id="84b38-450">13</span></span>|<span data-ttu-id="84b38-451">ファイナライザーの実行の終了。</span><span class="sxs-lookup"><span data-stu-id="84b38-451">The end of running finalizers.</span></span>|  
  
 <span data-ttu-id="84b38-452">次の表に、イベント データを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-452">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="84b38-453">フィールド名</span><span class="sxs-lookup"><span data-stu-id="84b38-453">Field name</span></span>|<span data-ttu-id="84b38-454">データ型</span><span class="sxs-lookup"><span data-stu-id="84b38-454">Data type</span></span>|<span data-ttu-id="84b38-455">説明</span><span class="sxs-lookup"><span data-stu-id="84b38-455">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="84b38-456">カウント</span><span class="sxs-lookup"><span data-stu-id="84b38-456">Count</span></span>|<span data-ttu-id="84b38-457">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="84b38-457">win:UInt32</span></span>|<span data-ttu-id="84b38-458">実行されたファイナライザーの数。</span><span class="sxs-lookup"><span data-stu-id="84b38-458">The number of finalizers that were run.</span></span>|  
|<span data-ttu-id="84b38-459">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="84b38-459">ClrInstanceID</span></span>|<span data-ttu-id="84b38-460">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="84b38-460">win:UInt16</span></span>|<span data-ttu-id="84b38-461">CLR または CoreCLR のインスタンスの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="84b38-461">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="84b38-462">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-462">Back to top</span></span>](#top)  
  
<a name="gccreateconcurrentthread_v1_event"></a>   
## <a name="gccreateconcurrentthreadv1-event"></a><span data-ttu-id="84b38-463">GCCreateConcurrentThread_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-463">GCCreateConcurrentThread_V1 Event</span></span>  
 <span data-ttu-id="84b38-464">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-464">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-465">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-465">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-466">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-466">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-467">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-467">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-468">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-468">Informational (4)</span></span>|  
|<span data-ttu-id="84b38-469">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="84b38-469">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="84b38-470">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-470">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-471">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-471">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-472">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-472">Event</span></span>|<span data-ttu-id="84b38-473">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-473">Event ID</span></span>|<span data-ttu-id="84b38-474">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-474">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCCreateConcurrentThread_V1`|<span data-ttu-id="84b38-475">11</span><span class="sxs-lookup"><span data-stu-id="84b38-475">11</span></span>|<span data-ttu-id="84b38-476">同時実行ガベージ コレクション スレッドが作成されました。</span><span class="sxs-lookup"><span data-stu-id="84b38-476">Concurrent garbage collection thread was created.</span></span>|  
  
 <span data-ttu-id="84b38-477">イベント データはありません。</span><span class="sxs-lookup"><span data-stu-id="84b38-477">No event data.</span></span>  
  
 [<span data-ttu-id="84b38-478">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="84b38-478">Back to top</span></span>](#top)  
  
<a name="gcterminateconcurrentthread_v1_event"></a>   
## <a name="gcterminateconcurrentthreadv1-event"></a><span data-ttu-id="84b38-479">GCTerminateConcurrentThread_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-479">GCTerminateConcurrentThread_V1 Event</span></span>  
 <span data-ttu-id="84b38-480">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-480">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="84b38-481">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="84b38-481">Keyword for raising the event</span></span>|<span data-ttu-id="84b38-482">レベル</span><span class="sxs-lookup"><span data-stu-id="84b38-482">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="84b38-483">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="84b38-483">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="84b38-484">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-484">Informational (4)</span></span>|  
|<span data-ttu-id="84b38-485">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="84b38-485">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="84b38-486">情報提供 (4)</span><span class="sxs-lookup"><span data-stu-id="84b38-486">Informational (4)</span></span>|  
  
 <span data-ttu-id="84b38-487">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84b38-487">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="84b38-488">イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-488">Event</span></span>|<span data-ttu-id="84b38-489">イベント ID</span><span class="sxs-lookup"><span data-stu-id="84b38-489">Event ID</span></span>|<span data-ttu-id="84b38-490">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="84b38-490">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCTerminateConcurrentThread_V1`|<span data-ttu-id="84b38-491">12</span><span class="sxs-lookup"><span data-stu-id="84b38-491">12</span></span>|<span data-ttu-id="84b38-492">同時実行ガベージ コレクションスレッドが終了しました。</span><span class="sxs-lookup"><span data-stu-id="84b38-492">Concurrent garbage collection thread was terminated.</span></span>|  
  
 <span data-ttu-id="84b38-493">イベント データはありません。</span><span class="sxs-lookup"><span data-stu-id="84b38-493">No event data.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84b38-494">関連項目</span><span class="sxs-lookup"><span data-stu-id="84b38-494">See also</span></span>
- [<span data-ttu-id="84b38-495">CLR ETW イベント</span><span class="sxs-lookup"><span data-stu-id="84b38-495">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
