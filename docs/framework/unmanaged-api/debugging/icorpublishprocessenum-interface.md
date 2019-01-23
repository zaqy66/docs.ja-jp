---
title: ICorPublishProcessEnum インターフェイス
ms.date: 03/30/2017
api_name:
- ICorPublishProcessEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcessEnum
helpviewer_keywords:
- ICorPublishProcessEnum interface [.NET Framework debugging]
ms.assetid: aac8fcf9-ac09-437c-bd5c-2fda14ae1007
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b72f2581b9670dbc110f2ab33cb861128bd78dca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525847"
---
# <a name="icorpublishprocessenum-interface"></a><span data-ttu-id="e7cef-102">ICorPublishProcessEnum インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e7cef-102">ICorPublishProcessEnum Interface</span></span>
<span data-ttu-id="e7cef-103">サブクラスの[ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md)のコレクションを走査するメソッドを提供するインターフェイス[ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="e7cef-103">A subclass of the [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) interface that provides methods to traverse a collection of [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e7cef-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="e7cef-104">Methods</span></span>  
  
|<span data-ttu-id="e7cef-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="e7cef-105">Method</span></span>|<span data-ttu-id="e7cef-106">説明</span><span class="sxs-lookup"><span data-stu-id="e7cef-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e7cef-107">Next メソッド</span><span class="sxs-lookup"><span data-stu-id="e7cef-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-next-method.md)|<span data-ttu-id="e7cef-108">指定した数を取得`ICorPublishProcess`コレクションの現在の位置からのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="e7cef-108">Gets the specified number of `ICorPublishProcess` instances from the collection, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e7cef-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="e7cef-109">Remarks</span></span>  
 <span data-ttu-id="e7cef-110">`ICorPublishProcessEnum`インターフェイス、抽象インターフェイスのメソッドを実装[ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md)します。</span><span class="sxs-lookup"><span data-stu-id="e7cef-110">The `ICorPublishProcessEnum` interface implements the methods of the abstract interface, [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md).</span></span>  
  
 <span data-ttu-id="e7cef-111">`ICorPublishProcessEnum`によってインスタンスが作成された、 [icorpublish::enumprocesses](../../../../docs/framework/unmanaged-api/debugging/icorpublish-enumprocesses-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="e7cef-111">An `ICorPublishProcessEnum` instance is created by the [ICorPublish::EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icorpublish-enumprocesses-method.md) method.</span></span> <span data-ttu-id="e7cef-112">コレクションのトラバーサル`ICorPublishProcess`オブジェクトは、時に指定されたフィルター条件に基づいて、`ICorPublishProcessEnum`インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e7cef-112">The traversal of the collection of `ICorPublishProcess` objects is based on the filter criteria given at the time the `ICorPublishProcessEnum` instance was created.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e7cef-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="e7cef-113">Requirements</span></span>  
 <span data-ttu-id="e7cef-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7cef-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7cef-115">**ヘッダー:** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="e7cef-115">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="e7cef-116">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e7cef-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e7cef-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7cef-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7cef-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7cef-118">See also</span></span>
- [<span data-ttu-id="e7cef-119">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e7cef-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="e7cef-120">CorpubPublish コクラス</span><span class="sxs-lookup"><span data-stu-id="e7cef-120">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
