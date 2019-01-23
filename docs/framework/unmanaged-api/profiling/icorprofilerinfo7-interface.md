---
title: ICorProfilerInfo7 インターフェイス
ms.date: 03/30/2017
ms.assetid: cf37c462-73c5-412a-a7f8-bb26ca746313
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c33e620b861f1065f95ba9f1f732911723c16f88
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54526276"
---
# <a name="icorprofilerinfo7-interface"></a><span data-ttu-id="3158c-102">ICorProfilerInfo7 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3158c-102">ICorProfilerInfo7 Interface</span></span>
<span data-ttu-id="3158c-103">[[!INCLUDE[net_v461](../../../../includes/net-v461-md.md)] 以降のバージョンでサポート]</span><span class="sxs-lookup"><span data-stu-id="3158c-103">[Supported in the [!INCLUDE[net_v461](../../../../includes/net-v461-md.md)] and later versions]</span></span>  
  
 <span data-ttu-id="3158c-104">サブクラス[ICorProfilerInfo6](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo6-interface.md)新しくを適用するメソッドをモジュールにメタデータを定義して、メモリ内のシンボルのストリームへのアクセスを提供するを提供します。</span><span class="sxs-lookup"><span data-stu-id="3158c-104">A subclass of [ICorProfilerInfo6](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo6-interface.md) that provides a method to apply newly defined metadata to a module and that provides access to an in-memory symbol stream.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3158c-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="3158c-105">Methods</span></span>  
  
|<span data-ttu-id="3158c-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3158c-106">Method</span></span>|<span data-ttu-id="3158c-107">説明</span><span class="sxs-lookup"><span data-stu-id="3158c-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3158c-108">ApplyMetaData メソッド</span><span class="sxs-lookup"><span data-stu-id="3158c-108">ApplyMetaData Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-applymetadata-method.md)|<span data-ttu-id="3158c-109">新しく定義されたメタデータを適用、`IMetadataEmit::Define*`メソッドが指定されたモジュールにします。</span><span class="sxs-lookup"><span data-stu-id="3158c-109">Applies the metadata newly defined by the `IMetadataEmit::Define*` methods to a specified module.</span></span>|  
|[<span data-ttu-id="3158c-110">GetInMemorySymbolsLength メソッド</span><span class="sxs-lookup"><span data-stu-id="3158c-110">GetInMemorySymbolsLength Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-getinmemorysymbolslength-method.md)|<span data-ttu-id="3158c-111">メモリ内のシンボルのストリームの長さを返します。</span><span class="sxs-lookup"><span data-stu-id="3158c-111">Returns the length of an in-memory symbol stream.</span></span>|  
|[<span data-ttu-id="3158c-112">ReadInMemorySymbols</span><span class="sxs-lookup"><span data-stu-id="3158c-112">ReadInMemorySymbols</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-readinmemorysymbols.md)|<span data-ttu-id="3158c-113">メモリ内のシンボルのストリームからバイトを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="3158c-113">Reads bytes from an in-memory symbol stream.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3158c-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="3158c-114">Requirements</span></span>  
 <span data-ttu-id="3158c-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3158c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3158c-116">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3158c-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3158c-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3158c-117">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3158c-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="3158c-118">See also</span></span>
- [<span data-ttu-id="3158c-119">プロファイリングのインターフェイス</span><span class="sxs-lookup"><span data-stu-id="3158c-119">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
