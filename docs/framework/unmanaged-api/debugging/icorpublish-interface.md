---
title: ICorPublish インターフェイス
ms.date: 03/30/2017
api_name:
- ICorPublish
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublish
helpviewer_keywords:
- ICorPublish interface [.NET Framework debugging]
ms.assetid: 87c4fcb2-7703-4a2e-afb6-42973381b960
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e1dea8cc54c68db333c409e3bd7b3e4211bd52ac
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54713968"
---
# <a name="icorpublish-interface"></a><span data-ttu-id="68d38-102">ICorPublish インターフェイス</span><span class="sxs-lookup"><span data-stu-id="68d38-102">ICorPublish Interface</span></span>
<span data-ttu-id="68d38-103">これらのプロセスでのプロセスに関する情報とアプリケーション ドメインに関する情報を公開するための一般的なインターフェイスとして機能します。</span><span class="sxs-lookup"><span data-stu-id="68d38-103">Serves as the general interface for publishing information about processes and information about the application domains in those processes.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="68d38-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="68d38-104">Methods</span></span>  
  
|<span data-ttu-id="68d38-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="68d38-105">Method</span></span>|<span data-ttu-id="68d38-106">説明</span><span class="sxs-lookup"><span data-stu-id="68d38-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="68d38-107">EnumProcesses メソッド</span><span class="sxs-lookup"><span data-stu-id="68d38-107">EnumProcesses Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublish-enumprocesses-method.md)|<span data-ttu-id="68d38-108">取得、 [ICorPublishProcessEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md)インスタンスをこのコンピューターで実行されている管理対象のプロセスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="68d38-108">Gets an [ICorPublishProcessEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md) instance that contains the managed processes running on this computer.</span></span>|  
|[<span data-ttu-id="68d38-109">GetProcess メソッド</span><span class="sxs-lookup"><span data-stu-id="68d38-109">GetProcess Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublish-getprocess-method.md)|<span data-ttu-id="68d38-110">取得、 [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)指定の識別子を持つプロセスを表すインスタンス。</span><span class="sxs-lookup"><span data-stu-id="68d38-110">Gets an [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance that represents the process with the specified identifier.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="68d38-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="68d38-111">Requirements</span></span>  
 <span data-ttu-id="68d38-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="68d38-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="68d38-113">**ヘッダー:** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="68d38-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="68d38-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="68d38-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="68d38-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="68d38-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68d38-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="68d38-116">See also</span></span>
- [<span data-ttu-id="68d38-117">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="68d38-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="68d38-118">CorpubPublish コクラス</span><span class="sxs-lookup"><span data-stu-id="68d38-118">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
