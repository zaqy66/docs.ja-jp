---
title: ICorDebugLoadedModule インターフェイス
ms.date: 03/30/2017
ms.assetid: 34be6369-2e75-4a95-a538-3b29ac97cf6d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f8f3a881a1beceb7d4aa35e2bd9a5e9e5419a391
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654868"
---
# <a name="icordebugloadedmodule-interface"></a><span data-ttu-id="e82f6-102">ICorDebugLoadedModule インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e82f6-102">ICorDebugLoadedModule Interface</span></span>
<span data-ttu-id="e82f6-103">読み込まれたモジュールに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e82f6-103">Provides information about a loaded module.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e82f6-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="e82f6-104">Methods</span></span>  
  
|<span data-ttu-id="e82f6-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="e82f6-105">Method</span></span>|<span data-ttu-id="e82f6-106">説明</span><span class="sxs-lookup"><span data-stu-id="e82f6-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e82f6-107">GetBaseAddress メソッド</span><span class="sxs-lookup"><span data-stu-id="e82f6-107">GetBaseAddress Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-getbaseaddress-method.md)|<span data-ttu-id="e82f6-108">読み込まれたモジュールのベース アドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="e82f6-108">Gets the base address of the loaded module.</span></span>|  
|[<span data-ttu-id="e82f6-109">GetName メソッド</span><span class="sxs-lookup"><span data-stu-id="e82f6-109">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-getname-method.md)|<span data-ttu-id="e82f6-110">読み込まれたモジュールの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="e82f6-110">Gets the name of the loaded module.</span></span>|  
|[<span data-ttu-id="e82f6-111">GetSize メソッド</span><span class="sxs-lookup"><span data-stu-id="e82f6-111">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-getsize-method.md)|<span data-ttu-id="e82f6-112">読み込まれたモジュールのサイズ (バイト単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="e82f6-112">Gets the size in bytes of the loaded module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e82f6-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="e82f6-113">Remarks</span></span>  
 <span data-ttu-id="e82f6-114">`ICorDebugLoadedModule` インターフェイスはデバッガーによって実装され、CLR デバッグ インターフェイスが、デバッガーから読み込まれたモジュールに関する情報を取得するために使用します。</span><span class="sxs-lookup"><span data-stu-id="e82f6-114">The `ICorDebugLoadedModule` interface is implemented by a debugger and is used by the CLR debugging interfaces to get information about the loaded module from the debugger.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e82f6-115">このインターフェイスは .NET ネイティブでのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="e82f6-115">This interface is available with .NET Native only.</span></span> <span data-ttu-id="e82f6-116">.NET ネイティブの外部で ICorDebug シナリオについてこのインターフェイスを実装する場合は、共通言語ランタイムはこのインターフェイスを無視します。</span><span class="sxs-lookup"><span data-stu-id="e82f6-116">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e82f6-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="e82f6-117">Requirements</span></span>  
 <span data-ttu-id="e82f6-118">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e82f6-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e82f6-119">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e82f6-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e82f6-120">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e82f6-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e82f6-121">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e82f6-121">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e82f6-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="e82f6-122">See also</span></span>
- [<span data-ttu-id="e82f6-123">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e82f6-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="e82f6-124">デバッグ</span><span class="sxs-lookup"><span data-stu-id="e82f6-124">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
