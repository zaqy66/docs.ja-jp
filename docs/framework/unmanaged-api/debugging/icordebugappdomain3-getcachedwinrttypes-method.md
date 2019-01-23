---
title: ICorDebugAppDomain3::GetCachedWinRTTypes メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain3.GetCachedWinRTTypes
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypes
helpviewer_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypes method [.NET Framework debugging]
- GetCachedWinRTTypes method, ICorDebugAppDomain3 interface [.NET Framework debugging]
ms.assetid: 9afd0e04-a403-41e2-9528-a6dcbcdcbd4d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: afbe368d58c96c8ddc97ccc3bb077ce768b229b0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54566113"
---
# <a name="icordebugappdomain3getcachedwinrttypes-method"></a><span data-ttu-id="68f02-102">ICorDebugAppDomain3::GetCachedWinRTTypes メソッド</span><span class="sxs-lookup"><span data-stu-id="68f02-102">ICorDebugAppDomain3::GetCachedWinRTTypes Method</span></span>
<span data-ttu-id="68f02-103">キャッシュされたすべての列挙子を取得します。[!INCLUDE[wrt](../../../../includes/wrt-md.md)]型。</span><span class="sxs-lookup"><span data-stu-id="68f02-103">Gets an enumerator for all cached [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="68f02-104">構文</span><span class="sxs-lookup"><span data-stu-id="68f02-104">Syntax</span></span>  
  
```  
HRESULT GetCachedWinRTTypes (   
    [out] ICorDebugGuidToTypeEnum **ppGuidToTypeEnum)  
;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="68f02-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68f02-105">Parameters</span></span>  
 `ppGuidToTypeEnum`  
 <span data-ttu-id="68f02-106">[out]ポインター、 [ICorDebugGuidToTypeEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-interface.md)インターフェイス オブジェクトのマネージ表現を列挙できる[!INCLUDE[wrt](../../../../includes/wrt-md.md)]アプリケーション ドメインで現在読み込まれている型。</span><span class="sxs-lookup"><span data-stu-id="68f02-106">[out] A pointer to an [ICorDebugGuidToTypeEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-interface.md) interface object that can enumerate the managed representations of [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types currently loaded in the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="68f02-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="68f02-107">Requirements</span></span>  
 <span data-ttu-id="68f02-108">**プラットフォーム:** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]</span><span class="sxs-lookup"><span data-stu-id="68f02-108">**Platforms:** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]</span></span>  
  
 <span data-ttu-id="68f02-109">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="68f02-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="68f02-110">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="68f02-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="68f02-111">**.NET Framework のバージョン:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="68f02-111">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68f02-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="68f02-112">See also</span></span>
- [<span data-ttu-id="68f02-113">ICorDebugAppDomain3 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="68f02-113">ICorDebugAppDomain3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-interface.md)
