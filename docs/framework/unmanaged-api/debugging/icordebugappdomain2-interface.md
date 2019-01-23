---
title: ICorDebugAppDomain2 Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain2
helpviewer_keywords:
- ICorDebugAppDomain2 interface [.NET Framework debugging]
ms.assetid: 314d29f3-feb0-4a92-9530-b569c280cc31
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f4549b0fe6379979a7b9bd6344d65ff465f33f17
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506135"
---
# <a name="icordebugappdomain2-interface1"></a><span data-ttu-id="899b9-102">ICorDebugAppDomain2 Interface1</span><span class="sxs-lookup"><span data-stu-id="899b9-102">ICorDebugAppDomain2 Interface1</span></span>
<span data-ttu-id="899b9-103">配列、ポインター、関数ポインター、および参照型を使用するメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="899b9-103">Provides methods to work with arrays, pointers, function pointers, and reference types.</span></span> <span data-ttu-id="899b9-104">このインターフェイスは、ICorDebugAppDomain インターフェイスの拡張機能です。</span><span class="sxs-lookup"><span data-stu-id="899b9-104">This interface is an extension of the ICorDebugAppDomain interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="899b9-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="899b9-105">Methods</span></span>  
  
|<span data-ttu-id="899b9-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="899b9-106">Method</span></span>|<span data-ttu-id="899b9-107">説明</span><span class="sxs-lookup"><span data-stu-id="899b9-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="899b9-108">GetArrayOrPointerType メソッド</span><span class="sxs-lookup"><span data-stu-id="899b9-108">GetArrayOrPointerType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain2-getarrayorpointertype-method.md)|<span data-ttu-id="899b9-109">指定した型、ポインター、または指定した型への参照の配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="899b9-109">Gets an array of the specified type, or a pointer or reference to the specified type.</span></span>|  
|[<span data-ttu-id="899b9-110">GetFunctionPointerType</span><span class="sxs-lookup"><span data-stu-id="899b9-110">GetFunctionPointerType</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain2-getfunctionpointertype-method.md)|<span data-ttu-id="899b9-111">指定されたシグネチャを持つ関数へのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="899b9-111">Gets a pointer to a function that has a given signature.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="899b9-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="899b9-112">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="899b9-113">このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="899b9-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="899b9-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="899b9-114">Requirements</span></span>  
 <span data-ttu-id="899b9-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="899b9-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="899b9-116">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="899b9-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="899b9-117">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="899b9-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="899b9-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="899b9-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="899b9-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="899b9-119">See also</span></span>
- [<span data-ttu-id="899b9-120">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="899b9-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
