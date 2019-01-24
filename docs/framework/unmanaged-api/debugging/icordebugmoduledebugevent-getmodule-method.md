---
title: ICorDebugModuleDebugEvent::GetModule メソッド
ms.date: 03/30/2017
ms.assetid: b1141c35-4253-4e34-b3e4-ed406a9dea4f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1ad20bdee5fee83b62d5da7f52c607835055616f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672332"
---
# <a name="icordebugmoduledebugeventgetmodule-method"></a><span data-ttu-id="533d2-102">ICorDebugModuleDebugEvent::GetModule メソッド</span><span class="sxs-lookup"><span data-stu-id="533d2-102">ICorDebugModuleDebugEvent::GetModule Method</span></span>
<span data-ttu-id="533d2-103">ロードまたはアンロードされたばかりのマージ モジュールを取得します。</span><span class="sxs-lookup"><span data-stu-id="533d2-103">Gets the merged module that was just loaded or unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="533d2-104">構文</span><span class="sxs-lookup"><span data-stu-id="533d2-104">Syntax</span></span>  
  
```  
HRESULT GetModule(  
   [out]ICorDebugModule **ppModule  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="533d2-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="533d2-105">Parameters</span></span>  
 `ppModule`  
 <span data-ttu-id="533d2-106">[out]ICorDebugModule だけロードまたはアンロードされたマージ モジュールを表すオブジェクトのアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="533d2-106">[out] A pointer to the address of an ICorDebugModule object that represents the merged module that was just loaded or unloaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="533d2-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="533d2-107">Remarks</span></span>  
 <span data-ttu-id="533d2-108">呼び出すことができます、 [GetEventKind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md)モジュールの読み込みまたはアンロードされたかどうかを判断するメソッド。</span><span class="sxs-lookup"><span data-stu-id="533d2-108">You can call the [GetEventKind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md) method to determine whether the module was loaded or unloaded.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="533d2-109">このメソッドは .NET ネイティブでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="533d2-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="533d2-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="533d2-110">Requirements</span></span>  
 <span data-ttu-id="533d2-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="533d2-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="533d2-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="533d2-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="533d2-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="533d2-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="533d2-114">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="533d2-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="533d2-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="533d2-115">See also</span></span>
- [<span data-ttu-id="533d2-116">ICorDebugModuleDebugEvent インターフェイス</span><span class="sxs-lookup"><span data-stu-id="533d2-116">ICorDebugModuleDebugEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmoduledebugevent-interface.md)
- [<span data-ttu-id="533d2-117">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="533d2-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
