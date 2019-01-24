---
title: ICorDebugSymbolProvider::GetAssemblyImageBytes メソッド
ms.date: 03/30/2017
ms.assetid: 3db215aa-e180-4f70-8d23-6d5a0ffbc8e5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5365b05db58d807cc010b763ca338ce76c8d7632
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54578771"
---
# <a name="icordebugsymbolprovidergetassemblyimagebytes-method"></a><span data-ttu-id="0f362-102">ICorDebugSymbolProvider::GetAssemblyImageBytes メソッド</span><span class="sxs-lookup"><span data-stu-id="0f362-102">ICorDebugSymbolProvider::GetAssemblyImageBytes Method</span></span>
<span data-ttu-id="0f362-103">マージされたアセンブリ内の指定の相対仮想アドレス (RVA: relative virtual address) で、マージされたアセンブリのデータを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="0f362-103">Reads data from a merged assembly given a relative virtual address (RVA) in the merged assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f362-104">構文</span><span class="sxs-lookup"><span data-stu-id="0f362-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyImageBytes(  
   [in] CORDB_ADDRESS rva,   
   [in] ULONG32 length,   
   [out] ICorDebugMemoryBuffer** ppMemoryBuffer  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0f362-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f362-105">Parameters</span></span>  
 `rva`  
 <span data-ttu-id="0f362-106">[in] マージされたアセンブリ内の相対仮想アドレス (RVA)。</span><span class="sxs-lookup"><span data-stu-id="0f362-106">[in] A relative virtual address (RVA) in a merged assembly.</span></span>  
  
 `length`  
 <span data-ttu-id="0f362-107">マージされたアセンブリから読み取るバイト数。</span><span class="sxs-lookup"><span data-stu-id="0f362-107">The number of bytes to read from the merged assembly.</span></span>  
  
 `ppMemoryBuffer`  
 <span data-ttu-id="0f362-108">アドレスへのポインター、 [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)マージされたアセンブリ メタデータのメモリ バッファーに関する情報を含むオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0f362-108">A pointer to the address of an [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md) object that contains information about the memory buffer with merged assembly metadata.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0f362-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="0f362-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0f362-110">このメソッドは .NET ネイティブでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="0f362-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f362-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="0f362-111">Requirements</span></span>  
 <span data-ttu-id="0f362-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f362-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f362-113">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0f362-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0f362-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0f362-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0f362-115">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0f362-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f362-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f362-116">See also</span></span>
- [<span data-ttu-id="0f362-117">ICorDebugSymbolProvider インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0f362-117">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="0f362-118">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0f362-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
