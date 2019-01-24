---
title: LoggingLevelEnum 列挙型
ms.date: 03/30/2017
api_name:
- LoggingLevelEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- LoggingLevelEnum
helpviewer_keywords:
- LoggingLevelEnum enumeration [.NET Framework debugging]
ms.assetid: 09daac08-005a-46b2-beab-408d0820c5e5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e72654dc62020e05f18c4d7d4d528617a0cd0c9f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54675250"
---
# <a name="logginglevelenum-enumeration"></a><span data-ttu-id="1fc32-102">LoggingLevelEnum 列挙型</span><span class="sxs-lookup"><span data-stu-id="1fc32-102">LoggingLevelEnum Enumeration</span></span>
<span data-ttu-id="1fc32-103">マネージド スレッドがイベントを記録する際にイベント ログに書き込まれる説明メッセージの重大度レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="1fc32-103">Indicates the severity level of a descriptive message that is written to the event log when a managed thread logs an event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1fc32-104">構文</span><span class="sxs-lookup"><span data-stu-id="1fc32-104">Syntax</span></span>  
  
```  
typedef enum LoggingLevelEnum {  
    LTraceLevel0 = 0,  
    LTraceLevel1,  
    LTraceLevel2,  
    LTraceLevel3,  
    LTraceLevel4,  
    LStatusLevel0 = 20,  
    LStatusLevel1,  
    LStatusLevel2,  
    LStatusLevel3,  
    LStatusLevel4,  
    LWarningLevel = 40,  
    LErrorLevel = 50,  
    LPanicLevel = 100  
} LoggingLevelEnum;  
```  
  
## <a name="members"></a><span data-ttu-id="1fc32-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="1fc32-105">Members</span></span>  
  
|<span data-ttu-id="1fc32-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="1fc32-106">Member</span></span>|<span data-ttu-id="1fc32-107">説明</span><span class="sxs-lookup"><span data-stu-id="1fc32-107">Description</span></span>|  
|------------|-----------------|  
|`LTraceLevel0`|<span data-ttu-id="1fc32-108">メッセージは、トレース レベル 0 です。</span><span class="sxs-lookup"><span data-stu-id="1fc32-108">The message is a trace level 0.</span></span>|  
|`LTraceLevel1`|<span data-ttu-id="1fc32-109">メッセージは、トレース レベル 1 です。</span><span class="sxs-lookup"><span data-stu-id="1fc32-109">The message is a trace level 1.</span></span>|  
|`LTraceLevel2`|<span data-ttu-id="1fc32-110">メッセージは、トレース レベル 2 です。</span><span class="sxs-lookup"><span data-stu-id="1fc32-110">The message is a trace level 2.</span></span>|  
|`LTraceLevel3`|<span data-ttu-id="1fc32-111">メッセージは、トレース レベル 3 です。</span><span class="sxs-lookup"><span data-stu-id="1fc32-111">The message is a trace level 3.</span></span>|  
|`LTraceLevel4`|<span data-ttu-id="1fc32-112">メッセージは、トレース レベル 4 です。</span><span class="sxs-lookup"><span data-stu-id="1fc32-112">The message is a trace level 4.</span></span>|  
|`LStatusLevel0`|<span data-ttu-id="1fc32-113">メッセージは、状態レベル 0 です。</span><span class="sxs-lookup"><span data-stu-id="1fc32-113">The message is a status level 0.</span></span>|  
|`LStatusLevel1`|<span data-ttu-id="1fc32-114">メッセージは、レベル 1 の状態です。</span><span class="sxs-lookup"><span data-stu-id="1fc32-114">The message is a status level 1.</span></span>|  
|`LStatusLevel2`|<span data-ttu-id="1fc32-115">メッセージは、状態のレベル 2 です。</span><span class="sxs-lookup"><span data-stu-id="1fc32-115">The message is a status level 2.</span></span>|  
|`LStatusLevel3`|<span data-ttu-id="1fc32-116">メッセージは、状態レベル 3 です。</span><span class="sxs-lookup"><span data-stu-id="1fc32-116">The message is a status level 3.</span></span>|  
|`LStatusLevel4`|<span data-ttu-id="1fc32-117">メッセージは、状態のレベル 4 です。</span><span class="sxs-lookup"><span data-stu-id="1fc32-117">The message is a status level 4.</span></span>|  
|`LWarningLevel`|<span data-ttu-id="1fc32-118">メッセージは、警告レベルです。</span><span class="sxs-lookup"><span data-stu-id="1fc32-118">The message is a warning level.</span></span>|  
|`LErrorLevel`|<span data-ttu-id="1fc32-119">メッセージは、エラー レベルです。</span><span class="sxs-lookup"><span data-stu-id="1fc32-119">The message is an error level.</span></span>|  
|`LPanicLevel`|<span data-ttu-id="1fc32-120">メッセージは、重大レベルです。</span><span class="sxs-lookup"><span data-stu-id="1fc32-120">The message is a panic level.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1fc32-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="1fc32-121">Remarks</span></span>  
 <span data-ttu-id="1fc32-122">共通言語ランタイム (CLR) の呼び出し、 [icordebugmanagedcallback::logmessage](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-logmessage-method.md)マネージ スレッドがイベントを記録するデバッガーに通知するメソッド。</span><span class="sxs-lookup"><span data-stu-id="1fc32-122">The common language runtime (CLR) calls the [ICorDebugManagedCallback::LogMessage](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-logmessage-method.md) method to notify the debugger that a managed thread has logged an event.</span></span> <span data-ttu-id="1fc32-123">CLR の値を渡す、`LoggingLevelEnum`マネージ スレッドは、イベント ログに書き込まれたメッセージの重大度レベルを示す列挙体。</span><span class="sxs-lookup"><span data-stu-id="1fc32-123">The CLR passes a value of the `LoggingLevelEnum` enumeration to indicate the severity level of the message that the managed thread wrote to the event log.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1fc32-124">必要条件</span><span class="sxs-lookup"><span data-stu-id="1fc32-124">Requirements</span></span>  
 <span data-ttu-id="1fc32-125">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fc32-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1fc32-126">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1fc32-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1fc32-127">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1fc32-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1fc32-128">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1fc32-128">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fc32-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="1fc32-129">See also</span></span>
- <xref:System.Diagnostics.EventLog>
- [<span data-ttu-id="1fc32-130">列挙型のデバッグ</span><span class="sxs-lookup"><span data-stu-id="1fc32-130">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
