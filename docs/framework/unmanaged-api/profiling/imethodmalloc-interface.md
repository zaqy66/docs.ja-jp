---
title: IMethodMalloc インターフェイス
ms.date: 03/30/2017
api_name:
- IMethodMalloc
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- IMethodMalloc
helpviewer_keywords:
- IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8c8ab5dc-557c-473a-82f2-6e403eca7dac
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6f5c21d329ed35f82e36c2d88ac911401799e820
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596021"
---
# <a name="imethodmalloc-interface"></a><span data-ttu-id="e4a67-102">IMethodMalloc インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e4a67-102">IMethodMalloc Interface</span></span>
<span data-ttu-id="e4a67-103">新しい Microsoft intermediate language (MSIL) 関数本体にメモリを割り当てるメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="e4a67-103">Provides a method to allocate memory for a new Microsoft intermediate language (MSIL) function body.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e4a67-104">`IMethodMalloc`インターフェイスは、単純なメモリ アロケーター。</span><span class="sxs-lookup"><span data-stu-id="e4a67-104">The `IMethodMalloc` interface is a simple memory allocator.</span></span> <span data-ttu-id="e4a67-105">これにより、メモリを割り当て、解放することができます。</span><span class="sxs-lookup"><span data-stu-id="e4a67-105">It allows you to allocate memory, but not to free it.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e4a67-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="e4a67-106">Methods</span></span>  
  
|<span data-ttu-id="e4a67-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="e4a67-107">Method</span></span>|<span data-ttu-id="e4a67-108">説明</span><span class="sxs-lookup"><span data-stu-id="e4a67-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e4a67-109">Alloc メソッド</span><span class="sxs-lookup"><span data-stu-id="e4a67-109">Alloc Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-alloc-method.md)|<span data-ttu-id="e4a67-110">新しい MSIL 関数本体の指定された量のメモリを割り当てようとします。</span><span class="sxs-lookup"><span data-stu-id="e4a67-110">Attempts to allocate a specified amount of memory for a new MSIL function body.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e4a67-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="e4a67-111">Remarks</span></span>  
 <span data-ttu-id="e4a67-112">各アロケーター モジュールに固有であり、関数本体は、モジュールのベースから正の値のオフセット位置になります。</span><span class="sxs-lookup"><span data-stu-id="e4a67-112">Each allocator is module-specific and ensures that the function body will be at a positive offset from the base of the module.</span></span> <span data-ttu-id="e4a67-113">モジュールのベースを超えるメモリはアロケーター関数本体にのみメモリを割り当てに使用するため貴重なことができます。</span><span class="sxs-lookup"><span data-stu-id="e4a67-113">Memory above the base of a module can be precious, so the allocator should be used to allocate memory only for a function body.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4a67-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="e4a67-114">Requirements</span></span>  
 <span data-ttu-id="e4a67-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4a67-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4a67-116">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e4a67-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e4a67-117">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e4a67-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e4a67-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4a67-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4a67-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4a67-119">See also</span></span>
- [<span data-ttu-id="e4a67-120">プロファイリングのインターフェイス</span><span class="sxs-lookup"><span data-stu-id="e4a67-120">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
