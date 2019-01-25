---
title: ICorDebugDataTarget2 インターフェイス
ms.date: 03/30/2017
ms.assetid: 13f11388-2f91-48d8-98d6-6a4a63cb5746
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0931cb5ed133d4de82473ae786f28f13fd396db5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743007"
---
# <a name="icordebugdatatarget2-interface"></a><span data-ttu-id="190c3-102">ICorDebugDataTarget2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="190c3-102">ICorDebugDataTarget2 Interface</span></span>
<span data-ttu-id="190c3-103">論理的に拡張し、 [ICorDebugDataTarget](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-interface.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="190c3-103">Logically extends the [ICorDebugDataTarget](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-interface.md)interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="190c3-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="190c3-104">Methods</span></span>  
  
|<span data-ttu-id="190c3-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="190c3-105">Method</span></span>|<span data-ttu-id="190c3-106">説明</span><span class="sxs-lookup"><span data-stu-id="190c3-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="190c3-107">CreateVirtualUnwinder メソッド</span><span class="sxs-lookup"><span data-stu-id="190c3-107">CreateVirtualUnwinder Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-createvirtualunwinder-method.md)|<span data-ttu-id="190c3-108">初期コンテキストからアンワインドを開始する新しいスタック アンワインダーを作成します (これは、必ずしもスレッドのリーフではありません)。</span><span class="sxs-lookup"><span data-stu-id="190c3-108">Creates a new stack unwinder that starts unwinding from an initial context (which isn't necessarily the leaf of a thread).</span></span>|  
|[<span data-ttu-id="190c3-109">EnumerateThreadIDs メソッド</span><span class="sxs-lookup"><span data-stu-id="190c3-109">EnumerateThreadIDs Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-enumeratethreadids-method.md)|<span data-ttu-id="190c3-110">アクティブなスレッド ID の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="190c3-110">Returns a list of active thread IDs.</span></span>|  
|[<span data-ttu-id="190c3-111">GetImageFromPointer メソッド</span><span class="sxs-lookup"><span data-stu-id="190c3-111">GetImageFromPointer Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-getimagefrompointer-method.md)|<span data-ttu-id="190c3-112">モジュールのアドレスから、そのモジュールのベース アドレスとサイズを返します。</span><span class="sxs-lookup"><span data-stu-id="190c3-112">Returns the module base address and size from an address in that module.</span></span>|  
|[<span data-ttu-id="190c3-113">GetImageLocation メソッド</span><span class="sxs-lookup"><span data-stu-id="190c3-113">GetImageLocation Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-getimagelocation-method.md)|<span data-ttu-id="190c3-114">モジュールのベース アドレスからモジュールのパスを返します。</span><span class="sxs-lookup"><span data-stu-id="190c3-114">Returns the path of a module from the module's base address.</span></span>|  
|[<span data-ttu-id="190c3-115">GetSymbolProviderForImage メソッド</span><span class="sxs-lookup"><span data-stu-id="190c3-115">GetSymbolProviderForImage Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-getsymbolproviderforimage-method.md)|<span data-ttu-id="190c3-116">モジュールのベース アドレスからそのモジュールのシンボル プロバイダーを返します。</span><span class="sxs-lookup"><span data-stu-id="190c3-116">Returns the symbol-provider for a module from the base address of that module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="190c3-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="190c3-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="190c3-118">このインターフェイスは .NET ネイティブでのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="190c3-118">This interface is available with .NET Native only.</span></span> <span data-ttu-id="190c3-119">.NET ネイティブの外部で ICorDebug シナリオについてこのインターフェイスを実装する場合は、共通言語ランタイムはこのインターフェイスを無視します。</span><span class="sxs-lookup"><span data-stu-id="190c3-119">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="190c3-120">必要条件</span><span class="sxs-lookup"><span data-stu-id="190c3-120">Requirements</span></span>  
 <span data-ttu-id="190c3-121">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="190c3-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="190c3-122">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="190c3-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="190c3-123">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="190c3-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="190c3-124">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="190c3-124">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="190c3-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="190c3-125">See also</span></span>
- [<span data-ttu-id="190c3-126">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="190c3-126">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="190c3-127">デバッグ</span><span class="sxs-lookup"><span data-stu-id="190c3-127">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
