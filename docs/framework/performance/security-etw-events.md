---
title: セキュリティ ETW イベント
ms.date: 03/30/2017
helpviewer_keywords:
- security events [.NET Framework]
- ETW, security events (CLR)
ms.assetid: 0ed69f73-5c01-4514-bd63-979c6e38d41d
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5cd5e660778b852cfee84359bb4d7253ca8f118d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54608077"
---
# <a name="security-etw-events"></a><span data-ttu-id="22ce6-102">セキュリティ ETW イベント</span><span class="sxs-lookup"><span data-stu-id="22ce6-102">Security ETW Events</span></span>
<a name="top"></a> <span data-ttu-id="22ce6-103">セキュリティ イベントは、厳密な名前の検証時と Authenticode の検証時に発生します。</span><span class="sxs-lookup"><span data-stu-id="22ce6-103">Security events are raised during strong name verification and Authenticode verification.</span></span>  
  
 <span data-ttu-id="22ce6-104">このカテゴリは、次のイベントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="22ce6-104">This category consists of the following events:</span></span>  
  
-   [<span data-ttu-id="22ce6-105">StrongNameVerificationStart_V1 イベントと StrongNameVerificationStop_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="22ce6-105">StrongNameVerificationStart_V1 and StrongNameVerificationStop_V1 Events</span></span>](#strongnameverificationstart_v1_and_strongnameverificationstop_v1_events)  
  
-   [<span data-ttu-id="22ce6-106">AuthenticodeVerificationStart_V1 イベントと AuthenticodeVerificationStop_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="22ce6-106">AuthenticodeVerificationStart_V1 and AuthenticodeVerificationStop_V1 Events</span></span>](#authenticodeverificationstart_v1_and_authenticodeverificationstop_v1_events)  
  
<a name="strongnameverificationstart_v1_and_strongnameverificationstop_v1_events"></a>   
## <a name="strongnameverificationstartv1-and-strongnameverificationstopv1-events"></a><span data-ttu-id="22ce6-107">StrongNameVerificationStart_V1 イベントと StrongNameVerificationStop_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="22ce6-107">StrongNameVerificationStart_V1 and StrongNameVerificationStop_V1 Events</span></span>  
 <span data-ttu-id="22ce6-108">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="22ce6-108">The following table shows the keyword and level.</span></span> <span data-ttu-id="22ce6-109">(詳細については、「 [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md)」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="22ce6-109">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="22ce6-110">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="22ce6-110">Keyword for raising the event</span></span>|<span data-ttu-id="22ce6-111">レベル</span><span class="sxs-lookup"><span data-stu-id="22ce6-111">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="22ce6-112">`SecurityKeyword` (0x400)</span><span class="sxs-lookup"><span data-stu-id="22ce6-112">`SecurityKeyword` (0x400)</span></span>|<span data-ttu-id="22ce6-113">情報通知 (4)</span><span class="sxs-lookup"><span data-stu-id="22ce6-113">Informational(4)</span></span>|  
  
 <span data-ttu-id="22ce6-114">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="22ce6-114">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="22ce6-115">イベント</span><span class="sxs-lookup"><span data-stu-id="22ce6-115">Event</span></span>|<span data-ttu-id="22ce6-116">イベント ID</span><span class="sxs-lookup"><span data-stu-id="22ce6-116">Event ID</span></span>|<span data-ttu-id="22ce6-117">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="22ce6-117">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`StrongNameVerificationStart_V1`|<span data-ttu-id="22ce6-118">181</span><span class="sxs-lookup"><span data-stu-id="22ce6-118">181</span></span>|<span data-ttu-id="22ce6-119">厳密な名前の検証の開始。</span><span class="sxs-lookup"><span data-stu-id="22ce6-119">Start of strong name verification.</span></span>|  
|`StrongNameVerificationStop_V1`|<span data-ttu-id="22ce6-120">182</span><span class="sxs-lookup"><span data-stu-id="22ce6-120">182</span></span>|<span data-ttu-id="22ce6-121">厳密な名前の検証の終了。</span><span class="sxs-lookup"><span data-stu-id="22ce6-121">End of strong name verification.</span></span>|  
  
 <span data-ttu-id="22ce6-122">次の表に、イベント データを示します。</span><span class="sxs-lookup"><span data-stu-id="22ce6-122">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="22ce6-123">フィールド名</span><span class="sxs-lookup"><span data-stu-id="22ce6-123">Field name</span></span>|<span data-ttu-id="22ce6-124">データ型</span><span class="sxs-lookup"><span data-stu-id="22ce6-124">Data type</span></span>|<span data-ttu-id="22ce6-125">説明</span><span class="sxs-lookup"><span data-stu-id="22ce6-125">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="22ce6-126">VerificationFlags</span><span class="sxs-lookup"><span data-stu-id="22ce6-126">VerificationFlags</span></span>|<span data-ttu-id="22ce6-127">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="22ce6-127">win:UInt32</span></span>|<span data-ttu-id="22ce6-128">検証フラグ。</span><span class="sxs-lookup"><span data-stu-id="22ce6-128">The verification flags.</span></span>|  
|<span data-ttu-id="22ce6-129">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="22ce6-129">ErrorCode</span></span>|<span data-ttu-id="22ce6-130">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="22ce6-130">win:UInt32</span></span>|<span data-ttu-id="22ce6-131">HResult エラー コード。</span><span class="sxs-lookup"><span data-stu-id="22ce6-131">The HResult error code.</span></span>|  
|<span data-ttu-id="22ce6-132">FullyQualifiedAssemblyName</span><span class="sxs-lookup"><span data-stu-id="22ce6-132">FullyQualifiedAssemblyName</span></span>|<span data-ttu-id="22ce6-133">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="22ce6-133">win:UnicodeString</span></span>|<span data-ttu-id="22ce6-134">完全修飾アセンブリ名。</span><span class="sxs-lookup"><span data-stu-id="22ce6-134">The fully qualified assembly name.</span></span>|  
|<span data-ttu-id="22ce6-135">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="22ce6-135">ClrInstanceID</span></span>|<span data-ttu-id="22ce6-136">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="22ce6-136">win:UInt16</span></span>|<span data-ttu-id="22ce6-137">CLR または CoreCLR のインスタンスの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="22ce6-137">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="22ce6-138">ページのトップへ</span><span class="sxs-lookup"><span data-stu-id="22ce6-138">Back to top</span></span>](#top)  
  
<a name="authenticodeverificationstart_v1_and_authenticodeverificationstop_v1_events"></a>   
## <a name="authenticodeverificationstartv1-and-authenticodeverificationstopv1-events"></a><span data-ttu-id="22ce6-139">AuthenticodeVerificationStart_V1 イベントと AuthenticodeVerificationStop_V1 イベント</span><span class="sxs-lookup"><span data-stu-id="22ce6-139">AuthenticodeVerificationStart_V1 and AuthenticodeVerificationStop_V1 Events</span></span>  
 <span data-ttu-id="22ce6-140">次の表に、キーワードとレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="22ce6-140">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="22ce6-141">イベントを発生させるキーワード</span><span class="sxs-lookup"><span data-stu-id="22ce6-141">Keyword for raising the event</span></span>|<span data-ttu-id="22ce6-142">レベル</span><span class="sxs-lookup"><span data-stu-id="22ce6-142">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="22ce6-143">`SecurityKeyword` (0x400)</span><span class="sxs-lookup"><span data-stu-id="22ce6-143">`SecurityKeyword` (0x400)</span></span>|<span data-ttu-id="22ce6-144">情報通知 (4)</span><span class="sxs-lookup"><span data-stu-id="22ce6-144">Informational(4)</span></span>|  
  
 <span data-ttu-id="22ce6-145">次の表に、イベント情報を示します。</span><span class="sxs-lookup"><span data-stu-id="22ce6-145">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="22ce6-146">イベント</span><span class="sxs-lookup"><span data-stu-id="22ce6-146">Event</span></span>|<span data-ttu-id="22ce6-147">イベント ID</span><span class="sxs-lookup"><span data-stu-id="22ce6-147">Event ID</span></span>|<span data-ttu-id="22ce6-148">いつ発生するか</span><span class="sxs-lookup"><span data-stu-id="22ce6-148">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AuthenticodeVerificationStart_V1`|<span data-ttu-id="22ce6-149">183</span><span class="sxs-lookup"><span data-stu-id="22ce6-149">183</span></span>|<span data-ttu-id="22ce6-150">Authenticode 検証の開始。</span><span class="sxs-lookup"><span data-stu-id="22ce6-150">Start of Authenticode verification.</span></span>|  
|`AuthenticodeVerificationStop_V1`|<span data-ttu-id="22ce6-151">184</span><span class="sxs-lookup"><span data-stu-id="22ce6-151">184</span></span>|<span data-ttu-id="22ce6-152">Authenticode 検証の終了。</span><span class="sxs-lookup"><span data-stu-id="22ce6-152">End of Authenticode verification.</span></span>|  
  
 <span data-ttu-id="22ce6-153">次の表に、イベント データを示します。</span><span class="sxs-lookup"><span data-stu-id="22ce6-153">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="22ce6-154">フィールド名</span><span class="sxs-lookup"><span data-stu-id="22ce6-154">Field name</span></span>|<span data-ttu-id="22ce6-155">データ型</span><span class="sxs-lookup"><span data-stu-id="22ce6-155">Data type</span></span>|<span data-ttu-id="22ce6-156">説明</span><span class="sxs-lookup"><span data-stu-id="22ce6-156">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="22ce6-157">VerificationFlags</span><span class="sxs-lookup"><span data-stu-id="22ce6-157">VerificationFlags</span></span>|<span data-ttu-id="22ce6-158">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="22ce6-158">win:UInt32</span></span>|<span data-ttu-id="22ce6-159">検証フラグ。</span><span class="sxs-lookup"><span data-stu-id="22ce6-159">The verification flags.</span></span>|  
|<span data-ttu-id="22ce6-160">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="22ce6-160">ErrorCode</span></span>|<span data-ttu-id="22ce6-161">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="22ce6-161">win:UInt32</span></span>|<span data-ttu-id="22ce6-162">HResult エラー コード。</span><span class="sxs-lookup"><span data-stu-id="22ce6-162">The HResult error code.</span></span>|  
|<span data-ttu-id="22ce6-163">ModulePath</span><span class="sxs-lookup"><span data-stu-id="22ce6-163">ModulePath</span></span>|<span data-ttu-id="22ce6-164">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="22ce6-164">win:UnicodeString</span></span>|<span data-ttu-id="22ce6-165">モジュール パス</span><span class="sxs-lookup"><span data-stu-id="22ce6-165">The module path.</span></span>|  
|<span data-ttu-id="22ce6-166">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="22ce6-166">ClrInstanceID</span></span>|<span data-ttu-id="22ce6-167">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="22ce6-167">win:UInt16</span></span>|<span data-ttu-id="22ce6-168">CLR または CoreCLR のインスタンスの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="22ce6-168">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="22ce6-169">関連項目</span><span class="sxs-lookup"><span data-stu-id="22ce6-169">See also</span></span>
- [<span data-ttu-id="22ce6-170">CLR ETW イベント</span><span class="sxs-lookup"><span data-stu-id="22ce6-170">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
