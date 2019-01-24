---
title: ICorDebug::Initialize メソッド
ms.date: 03/30/2017
api_name:
- ICorDebug.Initialize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::Initialize
helpviewer_keywords:
- Initialize method, ICorDebug interface [.NET Framework debugging]
- ICorDebug::Initialize method [.NET Framework debugging]
ms.assetid: 6fae3b23-5c9f-47c0-85d8-6bb75e050786
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f7b4cf6c50d624f82a75f19b8e3f42c73910c4e5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54709300"
---
# <a name="icordebuginitialize-method"></a><span data-ttu-id="b704b-102">ICorDebug::Initialize メソッド</span><span class="sxs-lookup"><span data-stu-id="b704b-102">ICorDebug::Initialize Method</span></span>
<span data-ttu-id="b704b-103">`ICorDebug` オブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b704b-103">Initializes the `ICorDebug` object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b704b-104">構文</span><span class="sxs-lookup"><span data-stu-id="b704b-104">Syntax</span></span>  
  
```  
HRESULT Initialize ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="b704b-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="b704b-105">Remarks</span></span>  
 <span data-ttu-id="b704b-106">デバッガーを呼び出す必要があります`Initialize`デバッグを初期化するために時間がサービスの作成時。</span><span class="sxs-lookup"><span data-stu-id="b704b-106">The debugger must call `Initialize` at creation time to initialize the debugging services.</span></span> <span data-ttu-id="b704b-107">他のメソッドの前にこのメソッドを呼び出す必要があります`ICorDebug`が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b704b-107">This method must be called before any other method on `ICorDebug` is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b704b-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="b704b-108">Requirements</span></span>  
 <span data-ttu-id="b704b-109">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b704b-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b704b-110">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b704b-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b704b-111">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b704b-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b704b-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b704b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b704b-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="b704b-113">See also</span></span>
- [<span data-ttu-id="b704b-114">ICorDebug インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b704b-114">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
