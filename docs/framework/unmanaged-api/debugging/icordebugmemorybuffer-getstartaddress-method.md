---
title: ICorDebugMemoryBuffer::GetStartAddress メソッド
ms.date: 03/30/2017
ms.assetid: f804d9ab-8c88-44f0-b278-5fcca7f87726
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 29149ceb155cdfdf7b735d6939809e80f2ba4dc0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54695544"
---
# <a name="icordebugmemorybuffergetstartaddress-method"></a><span data-ttu-id="55309-102">ICorDebugMemoryBuffer::GetStartAddress メソッド</span><span class="sxs-lookup"><span data-stu-id="55309-102">ICorDebugMemoryBuffer::GetStartAddress Method</span></span>
<span data-ttu-id="55309-103">メモリ バッファーの開始アドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="55309-103">Gets the starting address of the memory buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55309-104">構文</span><span class="sxs-lookup"><span data-stu-id="55309-104">Syntax</span></span>  
  
```  
HRESULT GetStartAddress(  
   [out] LPCVOID *address  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="55309-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="55309-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="55309-106">[out] メモリ バッファーの開始アドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="55309-106">[out] A pointer to the starting address of the memory buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="55309-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="55309-107">Remarks</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="55309-108">このメソッドは .NET ネイティブでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="55309-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="55309-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="55309-109">Requirements</span></span>  
 <span data-ttu-id="55309-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="55309-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="55309-111">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="55309-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="55309-112">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="55309-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="55309-113">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="55309-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55309-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="55309-114">See also</span></span>
- [<span data-ttu-id="55309-115">ICorDebugMemoryBuffer インターフェイス</span><span class="sxs-lookup"><span data-stu-id="55309-115">ICorDebugMemoryBuffer Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)
- [<span data-ttu-id="55309-116">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="55309-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
