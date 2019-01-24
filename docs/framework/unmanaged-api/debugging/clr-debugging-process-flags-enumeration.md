---
title: CLR_DEBUGGING_PROCESS_FLAGS 列挙体
ms.date: 03/30/2017
api_name:
- CLR_DEBUGGING_PROCESS_FLAGS
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CLR_DEBUGGING_PROCESS_FLAG
helpviewer_keywords:
- CLR_DEBUGGING_PROCESS_FLAGS enumeration [.NET Framework debugging]
ms.assetid: 85b85fde-1f87-490b-ba8d-d604670959c3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 609bb050bb9c5addb5250f65a059a70d3ce32428
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662245"
---
# <a name="clrdebuggingprocessflags-enumeration"></a><span data-ttu-id="35f31-102">CLR_DEBUGGING_PROCESS_FLAGS 列挙体</span><span class="sxs-lookup"><span data-stu-id="35f31-102">CLR_DEBUGGING_PROCESS_FLAGS Enumeration</span></span>
<span data-ttu-id="35f31-103">使用される値を提供します、 [iclrdebugging::openvirtualprocess](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="35f31-103">Provides values that are used by the [ICLRDebugging::OpenVirtualProcess](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35f31-104">構文</span><span class="sxs-lookup"><span data-stu-id="35f31-104">Syntax</span></span>  
  
```  
typedef enum CLR_DEBUGGING_PROCESS_FLAGS  
{  
   CLR_DEBUGGING_MANAGED_EVENT_PENDING = 1,  
   CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH = 2  
}  CLR_DEBUGGING_PROCESS_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="35f31-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="35f31-105">Members</span></span>  
  
|<span data-ttu-id="35f31-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="35f31-106">Member</span></span>|<span data-ttu-id="35f31-107">説明</span><span class="sxs-lookup"><span data-stu-id="35f31-107">Description</span></span>|  
|------------|-----------------|  
|`CLR_DEBUGGING_MANAGED_EVENT_PENDING`|<span data-ttu-id="35f31-108">このランタイムには、送信する非 catch アップ マネージ デバッガー イベントがあります。</span><span class="sxs-lookup"><span data-stu-id="35f31-108">This runtime has a non-catch-up managed debugger event to send.</span></span> <span data-ttu-id="35f31-109">キャッチアップおよび非 catch アップ イベントを区別する、「解説」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35f31-109">See the Remarks section for the distinction between catch-up and non-catch-up events.</span></span>|  
|`CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH`|<span data-ttu-id="35f31-110">管理対象のイベントが保留中ですが、<xref:System.Diagnostics.Debugger.Launch%2A?displayProperty=nameWithType>要求。</span><span class="sxs-lookup"><span data-stu-id="35f31-110">The managed event that is pending is a <xref:System.Diagnostics.Debugger.Launch%2A?displayProperty=nameWithType> request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="35f31-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="35f31-111">Remarks</span></span>  
 <span data-ttu-id="35f31-112">キャッチアップ イベントには、プロセス、アプリケーション ドメイン、アセンブリ、モジュール、および現在の状態には、プロセスにアタッチした後、デバッガーになるスレッドの作成の通知が含まれます。</span><span class="sxs-lookup"><span data-stu-id="35f31-112">Catch-up events include process, application domain, assembly, module, and thread creation notifications that bring the debugger up to the current state after it has attached to a process.</span></span> <span data-ttu-id="35f31-113">示されている非 catch-アップ イベント、`CLR_DEBUGGING_MANAGED_EVENT_PENDING`フラグを設定し、すべて他のデバッガー イベント、例外などを追加し、マネージ デバッグ アシスタント (MDA) 通知します。</span><span class="sxs-lookup"><span data-stu-id="35f31-113">Non-catch-up events, which are indicated by the `CLR_DEBUGGING_MANAGED_EVENT_PENDING` flag, include all other debugger events, such as exceptions and managed debugging assistant (MDA) notifications.</span></span>  
  
 <span data-ttu-id="35f31-114">`CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH`フラグをランタイム終了例外とキャンセル可能なマネージ デバッガーをアタッチする要求を区別するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="35f31-114">The `CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH` flag enables the runtime to differentiate between a terminating exception and a request to attach a managed debugger that can be canceled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="35f31-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="35f31-115">Requirements</span></span>  
 <span data-ttu-id="35f31-116">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="35f31-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="35f31-117">**ヘッダー:** Metahost.idl、Metahost.h</span><span class="sxs-lookup"><span data-stu-id="35f31-117">**Header:** Metahost.idl, Metahost.h</span></span>  
  
 <span data-ttu-id="35f31-118">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="35f31-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="35f31-119">**.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="35f31-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="35f31-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="35f31-120">See also</span></span>
- [<span data-ttu-id="35f31-121">列挙型のデバッグ</span><span class="sxs-lookup"><span data-stu-id="35f31-121">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
- [<span data-ttu-id="35f31-122">デバッグ</span><span class="sxs-lookup"><span data-stu-id="35f31-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
