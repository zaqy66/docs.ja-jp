---
title: ICorDebugVariableSymbol インターフェイス
ms.date: 03/30/2017
ms.assetid: 0e58b85e-69bd-41ff-bedb-8cdc8be6a7a2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9822a3403c6ff738f7a6556a35cb383426575cb9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54582592"
---
# <a name="icordebugvariablesymbol-interface"></a><span data-ttu-id="4644f-102">ICorDebugVariableSymbol インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4644f-102">ICorDebugVariableSymbol Interface</span></span>
<span data-ttu-id="4644f-103">変数のデバッグ シンボル情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="4644f-103">Retrieves the debug symbol information for a variable.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4644f-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="4644f-104">Methods</span></span>  
  
|<span data-ttu-id="4644f-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="4644f-105">Method</span></span>|<span data-ttu-id="4644f-106">説明</span><span class="sxs-lookup"><span data-stu-id="4644f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4644f-107">GetName メソッド</span><span class="sxs-lookup"><span data-stu-id="4644f-107">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-getname-method.md)|<span data-ttu-id="4644f-108">変数の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="4644f-108">Gets the name of a variable.</span></span>|  
|[<span data-ttu-id="4644f-109">GetSize メソッド</span><span class="sxs-lookup"><span data-stu-id="4644f-109">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-getsize-method.md)|<span data-ttu-id="4644f-110">変数のサイズ (バイト単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="4644f-110">Gets the size of a variable in bytes.</span></span>|  
|[<span data-ttu-id="4644f-111">GetSlotIndex メソッド</span><span class="sxs-lookup"><span data-stu-id="4644f-111">GetSlotIndex Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-getslotindex-method.md)|<span data-ttu-id="4644f-112">ローカル変数のマネージド スロット インデックスを取得します。</span><span class="sxs-lookup"><span data-stu-id="4644f-112">Gets the managed slot index of a local variable.</span></span>|  
|[<span data-ttu-id="4644f-113">GetValue メソッド</span><span class="sxs-lookup"><span data-stu-id="4644f-113">GetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-getvalue-method.md)|<span data-ttu-id="4644f-114">変数の値をバイト配列として取得します。</span><span class="sxs-lookup"><span data-stu-id="4644f-114">Gets the value of a variable as a byte array.</span></span>|  
|[<span data-ttu-id="4644f-115">SetValue メソッド</span><span class="sxs-lookup"><span data-stu-id="4644f-115">SetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-setvalue-method.md)|<span data-ttu-id="4644f-116">バイト配列の値を変数に代入します。</span><span class="sxs-lookup"><span data-stu-id="4644f-116">Assigns the value of a byte array to a variable.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4644f-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="4644f-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4644f-118">このインターフェイスは .NET ネイティブでのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="4644f-118">This interface is available with .NET Native only.</span></span> <span data-ttu-id="4644f-119">.NET ネイティブの外部で ICorDebug シナリオについてこのインターフェイスを実装する場合は、共通言語ランタイムはこのインターフェイスを無視します。</span><span class="sxs-lookup"><span data-stu-id="4644f-119">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4644f-120">必要条件</span><span class="sxs-lookup"><span data-stu-id="4644f-120">Requirements</span></span>  
 <span data-ttu-id="4644f-121">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4644f-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4644f-122">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4644f-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4644f-123">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4644f-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4644f-124">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4644f-124">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4644f-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="4644f-125">See also</span></span>
- [<span data-ttu-id="4644f-126">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4644f-126">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="4644f-127">デバッグ</span><span class="sxs-lookup"><span data-stu-id="4644f-127">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
