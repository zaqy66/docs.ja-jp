---
title: StackTrace_SimpleContext 構造体
ms.date: 03/30/2017
api_name:
- StackTrace_SimpleContext
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- SimpleContext
helpviewer_keywords:
- SimpleContext structure [.NET Framework debugging]
- StackTrace_SimpleContext structure [.NET Framework debugging]
ms.assetid: d4cef11f-a8ca-49bc-a1b8-6631f9e28f3e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 510ef77f217cdd6e3441e3d6684d431fc31307fd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54698922"
---
# <a name="stacktracesimplecontext-structure"></a><span data-ttu-id="e7fde-102">StackTrace_SimpleContext 構造体</span><span class="sxs-lookup"><span data-stu-id="e7fde-102">StackTrace_SimpleContext Structure</span></span>
<span data-ttu-id="e7fde-103">完全な `CONTEXT` 構造の代わりに使用できる単純なコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="e7fde-103">Provides a simple context that can be used in place of a full `CONTEXT` structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e7fde-104">構文</span><span class="sxs-lookup"><span data-stu-id="e7fde-104">Syntax</span></span>  
  
```  
struct StackTrace_SimpleContext  
{  
    ULONG64 StackOffset;       // ESP on x86  
    ULONG64 FrameOffset;       // EBP on x86  
    ULONG64 InstructionOffset; // EIP on x86  
};  
```  
  
## <a name="members"></a><span data-ttu-id="e7fde-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="e7fde-105">Members</span></span>  
  
|<span data-ttu-id="e7fde-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="e7fde-106">Member</span></span>|<span data-ttu-id="e7fde-107">説明</span><span class="sxs-lookup"><span data-stu-id="e7fde-107">Description</span></span>|  
|------------|-----------------|  
|`StackOffset`|<span data-ttu-id="e7fde-108">スタック ポインター、または x86 enter スタック ポインター (ESP) プラットフォーム。</span><span class="sxs-lookup"><span data-stu-id="e7fde-108">The stack pointer, or the enter stack pointer (ESP) on x86 platforms.</span></span>|  
|`FrameOffset`|<span data-ttu-id="e7fde-109">フレームのオフセット、または x86 EBP レジスタのプラットフォームです。</span><span class="sxs-lookup"><span data-stu-id="e7fde-109">The frame offset, or the EBP register on x86 platforms.</span></span>|  
|`InstructionOffset`|<span data-ttu-id="e7fde-110">命令ポインター、または x86 enter 命令ポインター (EIP) プラットフォーム。</span><span class="sxs-lookup"><span data-stu-id="e7fde-110">The instruction pointer, or the enter instruction pointer (EIP) on x86 platforms.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e7fde-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="e7fde-111">Remarks</span></span>  
 <span data-ttu-id="e7fde-112">使用できます必要に応じてスタック トレース関数は、通常、アドレス、フレームのオフセット、およびスタック アドレスのみを返す必要があります、ため、`SimpleContext`構造ではなく、大規模な`CONTEXT`構造体。</span><span class="sxs-lookup"><span data-stu-id="e7fde-112">Because stack trace functions typically need to return only the address, frame offset, and stack address, you can optionally use the `SimpleContext` structure instead of a large `CONTEXT` structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e7fde-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="e7fde-113">Requirements</span></span>  
 <span data-ttu-id="e7fde-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7fde-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7fde-115">**ヘッダー:** SOS_Stacktrace.h</span><span class="sxs-lookup"><span data-stu-id="e7fde-115">**Header:** SOS_Stacktrace.h</span></span>  
  
 <span data-ttu-id="e7fde-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7fde-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7fde-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7fde-117">See also</span></span>
- [<span data-ttu-id="e7fde-118">デバッグ構造体</span><span class="sxs-lookup"><span data-stu-id="e7fde-118">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="e7fde-119">デバッグ</span><span class="sxs-lookup"><span data-stu-id="e7fde-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
