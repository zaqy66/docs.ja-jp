---
title: ICorDebugClass2 Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugClass2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass2
helpviewer_keywords:
- ICorDebugClass2 interface [.NET Framework debugging]
ms.assetid: 5416de70-43f2-4cdf-a11f-d570759c9c0c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bb70016560f453caf7a7a3eed3e1aa6b5fc9f0ef
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54557367"
---
# <a name="icordebugclass2-interface1"></a><span data-ttu-id="61817-102">ICorDebugClass2 Interface1</span><span class="sxs-lookup"><span data-stu-id="61817-102">ICorDebugClass2 Interface1</span></span>
<span data-ttu-id="61817-103">ジェネリック、または <xref:System.Type> 型のメソッド パラメーターを持つクラスを表します。</span><span class="sxs-lookup"><span data-stu-id="61817-103">Represents a generic class or a class with a method parameter of type <xref:System.Type>.</span></span> <span data-ttu-id="61817-104">このインターフェイスは拡張[ICorDebugClass](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-interface.md)します。</span><span class="sxs-lookup"><span data-stu-id="61817-104">This interface extends [ICorDebugClass](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-interface.md).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="61817-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="61817-105">Methods</span></span>  
  
|<span data-ttu-id="61817-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="61817-106">Method</span></span>|<span data-ttu-id="61817-107">説明</span><span class="sxs-lookup"><span data-stu-id="61817-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="61817-108">GetParameterizedType メソッド</span><span class="sxs-lookup"><span data-stu-id="61817-108">GetParameterizedType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugclass2-getparameterizedtype-method.md)|<span data-ttu-id="61817-109">このクラスの型宣言を取得します。</span><span class="sxs-lookup"><span data-stu-id="61817-109">Gets the type declaration for this class.</span></span>|  
|[<span data-ttu-id="61817-110">SetJMCStatus メソッド</span><span class="sxs-lookup"><span data-stu-id="61817-110">SetJMCStatus Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugclass2-setjmcstatus-method.md)|<span data-ttu-id="61817-111">このクラスの各メソッドでは、メソッドは、ユーザー定義のコードかどうかを示す値を設定します。</span><span class="sxs-lookup"><span data-stu-id="61817-111">For each method of this class, sets a value that indicates whether the method is user-defined code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="61817-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="61817-112">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="61817-113">このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="61817-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="61817-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="61817-114">Requirements</span></span>  
 <span data-ttu-id="61817-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="61817-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="61817-116">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="61817-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="61817-117">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="61817-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="61817-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="61817-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61817-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="61817-119">See also</span></span>
- [<span data-ttu-id="61817-120">ICorDebugClass Interface1</span><span class="sxs-lookup"><span data-stu-id="61817-120">ICorDebugClass Interface1</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-interface.md)
- [<span data-ttu-id="61817-121">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="61817-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
