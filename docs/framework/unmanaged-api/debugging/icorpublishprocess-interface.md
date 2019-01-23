---
title: ICorPublishProcess インターフェイス
ms.date: 03/30/2017
api_name:
- ICorPublishProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess
helpviewer_keywords:
- ICorPublishProcess interface [.NET Framework debugging]
ms.assetid: 6d1dc41b-8aa2-4889-bb00-1cbccc00c123
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 19bd34f95e17094a89e4929a5b6ae936afe39885
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54531916"
---
# <a name="icorpublishprocess-interface"></a><span data-ttu-id="21e66-102">ICorPublishProcess インターフェイス</span><span class="sxs-lookup"><span data-stu-id="21e66-102">ICorPublishProcess Interface</span></span>
<span data-ttu-id="21e66-103">表示するプロセスについての情報にアクセスするメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="21e66-103">Provides methods that access information to be displayed about a process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="21e66-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="21e66-104">Methods</span></span>  
  
|<span data-ttu-id="21e66-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="21e66-105">Method</span></span>|<span data-ttu-id="21e66-106">説明</span><span class="sxs-lookup"><span data-stu-id="21e66-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="21e66-107">EnumAppDomains メソッド</span><span class="sxs-lookup"><span data-stu-id="21e66-107">EnumAppDomains Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-enumappdomains-method.md)|<span data-ttu-id="21e66-108">取得、 [ICorPublishAppDomainEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md)これによって参照されるプロセス内のアプリケーション ドメインを含むインスタンス`ICorPublishProcess`します。</span><span class="sxs-lookup"><span data-stu-id="21e66-108">Gets an [ICorPublishAppDomainEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md) instance that contains the application domains in the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="21e66-109">GetDisplayName メソッド</span><span class="sxs-lookup"><span data-stu-id="21e66-109">GetDisplayName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-getdisplayname-method.md)|<span data-ttu-id="21e66-110">これによって参照されるプロセスの実行可能ファイルの完全なパスを取得`ICorPublishProcess`します。</span><span class="sxs-lookup"><span data-stu-id="21e66-110">Gets the full path of the executable for the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="21e66-111">GetProcessID メソッド</span><span class="sxs-lookup"><span data-stu-id="21e66-111">GetProcessID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-getprocessid-method.md)|<span data-ttu-id="21e66-112">これによって参照されるプロセスのオペレーティング システムの識別子を取得`ICorPublishProcess`します。</span><span class="sxs-lookup"><span data-stu-id="21e66-112">Gets the operating system identifier for the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="21e66-113">IsManaged メソッド</span><span class="sxs-lookup"><span data-stu-id="21e66-113">IsManaged Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-ismanaged-method.md)|<span data-ttu-id="21e66-114">これによって、プロセスが参照されるかどうかを示す値を取得します`ICorPublishProcess`マネージ コードを実行することがわかっています。</span><span class="sxs-lookup"><span data-stu-id="21e66-114">Gets a value that indicates whether the process referenced by this `ICorPublishProcess` is known to be running managed code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="21e66-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="21e66-115">Requirements</span></span>  
 <span data-ttu-id="21e66-116">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="21e66-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="21e66-117">**ヘッダー:** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="21e66-117">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="21e66-118">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="21e66-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="21e66-119">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="21e66-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21e66-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="21e66-120">See also</span></span>
- [<span data-ttu-id="21e66-121">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="21e66-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="21e66-122">CorpubPublish コクラス</span><span class="sxs-lookup"><span data-stu-id="21e66-122">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
