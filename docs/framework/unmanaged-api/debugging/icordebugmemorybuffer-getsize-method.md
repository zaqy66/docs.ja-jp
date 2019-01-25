---
title: ICorDebugMemoryBuffer::GetSize メソッド
ms.date: 03/30/2017
ms.assetid: 9ffd5482-268e-4680-9fd1-bfb0b7d66450
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c5984addb41c33468068f7ad24a15533f75dc367
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54714725"
---
# <a name="icordebugmemorybuffergetsize-method"></a><span data-ttu-id="98806-102">ICorDebugMemoryBuffer::GetSize メソッド</span><span class="sxs-lookup"><span data-stu-id="98806-102">ICorDebugMemoryBuffer::GetSize Method</span></span>
<span data-ttu-id="98806-103">メモリ バッファーのサイズ (バイト単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="98806-103">Gets the size of the memory buffer in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="98806-104">構文</span><span class="sxs-lookup"><span data-stu-id="98806-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbBufferLength  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="98806-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="98806-105">Parameters</span></span>  
 `pcbBufferLength`  
 <span data-ttu-id="98806-106">[out] メモリ バッファーのサイズへのポインター。</span><span class="sxs-lookup"><span data-stu-id="98806-106">[out] A pointer to the size of the memory buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="98806-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="98806-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="98806-108">このメソッドは .NET ネイティブでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="98806-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="98806-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="98806-109">Requirements</span></span>  
 <span data-ttu-id="98806-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="98806-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="98806-111">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="98806-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="98806-112">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="98806-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="98806-113">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="98806-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="98806-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="98806-114">See also</span></span>
- [<span data-ttu-id="98806-115">ICorDebugMemoryBuffer インターフェイス</span><span class="sxs-lookup"><span data-stu-id="98806-115">ICorDebugMemoryBuffer Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)
- [<span data-ttu-id="98806-116">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="98806-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
