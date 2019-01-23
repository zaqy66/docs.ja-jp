---
title: ICorDebugProcess3::SetEnableCustomNotification メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugProcess3.SetEnableCustomNotification Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess3::SetEnableCustomNotification
helpviewer_keywords:
- ICorDebugProcess3::SetEnableCustomNotification method [.NET Framework debugging]
- SetEnableCustomNotification method [.NET Framework debugging]
ms.assetid: afd88ee9-2589-4461-a75a-9b6fe55a2525
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7501a8a0f8368049c87b3c90e1e707e12773a853
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54531643"
---
# <a name="icordebugprocess3setenablecustomnotification-method"></a><span data-ttu-id="d1bb8-102">ICorDebugProcess3::SetEnableCustomNotification メソッド</span><span class="sxs-lookup"><span data-stu-id="d1bb8-102">ICorDebugProcess3::SetEnableCustomNotification Method</span></span>
<span data-ttu-id="d1bb8-103">有効にし、指定した型のカスタムのデバッガー通知を無効にします。</span><span class="sxs-lookup"><span data-stu-id="d1bb8-103">Enables and disables custom debugger notifications of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1bb8-104">構文</span><span class="sxs-lookup"><span data-stu-id="d1bb8-104">Syntax</span></span>  
  
```  
HRESULT SetEnableCustomNotification(ICorDebugClass * pClass,  
                                    BOOL fEnable);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d1bb8-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d1bb8-105">Parameters</span></span>  
 `pClass`  
 <span data-ttu-id="d1bb8-106">[in]カスタムのデバッガー通知を指定する型。</span><span class="sxs-lookup"><span data-stu-id="d1bb8-106">[in] The type that specifies custom debugger notifications.</span></span>  
  
 `fEnable`  
 <span data-ttu-id="d1bb8-107">[in]`true`カスタムのデバッガー通知を有効にするには`false`通知を無効にします。</span><span class="sxs-lookup"><span data-stu-id="d1bb8-107">[in] `true` to enable custom debugger notifications; `false` to disable notifications.</span></span> <span data-ttu-id="d1bb8-108">既定値は `false` です。</span><span class="sxs-lookup"><span data-stu-id="d1bb8-108">The default value is `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d1bb8-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="d1bb8-109">Remarks</span></span>  
 <span data-ttu-id="d1bb8-110">ときに`fEnable`に設定されている`true`への呼び出し、 <xref:System.Diagnostics.Debugger.NotifyOfCrossThreadDependency%2A?displayProperty=nameWithType> trigger メソッド、 [icordebugmanagedcallback 3::customnotification](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md)コールバック。</span><span class="sxs-lookup"><span data-stu-id="d1bb8-110">When `fEnable` is set to `true`, calls to the <xref:System.Diagnostics.Debugger.NotifyOfCrossThreadDependency%2A?displayProperty=nameWithType> method trigger an [ICorDebugManagedCallback3::CustomNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md) callback.</span></span> <span data-ttu-id="d1bb8-111">既定では通知が無効になっていますそのため、デバッガーは、通知の種類が認識し、処理する必要があるを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1bb8-111">Notifications are disabled by default; therefore, the debugger must specify any notification types it knows about and wants to handle.</span></span> <span data-ttu-id="d1bb8-112">[ICorDebugClass](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)クラスのスコープは、アプリケーション ドメインによって、デバッガーを呼び出す必要があります`SetEnableCustomNotification`のプロセス全体で、通知を受信する場合にプロセス内の各アプリケーション ドメイン。</span><span class="sxs-lookup"><span data-stu-id="d1bb8-112">Because the [ICorDebugClass](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) class is scoped by application domain, the debugger must call `SetEnableCustomNotification` for every application domain in the process if it wants to receive the notification across the entire process.</span></span>  
  
 <span data-ttu-id="d1bb8-113">以降では、 [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)]、のみサポートされている通知がスレッド間の依存関係の通知。</span><span class="sxs-lookup"><span data-stu-id="d1bb8-113">Starting with the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)], the only supported notification is a cross-thread dependency notification.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d1bb8-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="d1bb8-114">Requirements</span></span>  
 <span data-ttu-id="d1bb8-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1bb8-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d1bb8-116">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d1bb8-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d1bb8-117">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d1bb8-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d1bb8-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d1bb8-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1bb8-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1bb8-119">See also</span></span>
- [<span data-ttu-id="d1bb8-120">ICorDebugProcess3 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d1bb8-120">ICorDebugProcess3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess3-interface.md)
- [<span data-ttu-id="d1bb8-121">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d1bb8-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="d1bb8-122">デバッグ</span><span class="sxs-lookup"><span data-stu-id="d1bb8-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
