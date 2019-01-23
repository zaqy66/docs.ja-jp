---
title: IHostAssemblyManager インターフェイス
ms.date: 03/30/2017
api_name:
- IHostAssemblyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyManager
helpviewer_keywords:
- IHostAssemblyManager interface [.NET Framework hosting]
ms.assetid: dfec05bb-3cd7-4bd5-b396-a4f097c3a636
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0e60b578256fb516ee0bd4edcec0b5a1a5179b46
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54615336"
---
# <a name="ihostassemblymanager-interface"></a><span data-ttu-id="c82af-102">IHostAssemblyManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c82af-102">IHostAssemblyManager Interface</span></span>
<span data-ttu-id="c82af-103">ホストが共通言語ランタイム (CLR) またはホストに読み込む必要のあるアセンブリのセットを指定できるようにするメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="c82af-103">Provides methods that allow a host to specify sets of assemblies that should be loaded by the common language runtime (CLR) or by the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c82af-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="c82af-104">Methods</span></span>  
  
|<span data-ttu-id="c82af-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="c82af-105">Method</span></span>|<span data-ttu-id="c82af-106">説明</span><span class="sxs-lookup"><span data-stu-id="c82af-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c82af-107">GetAssemblyStore メソッド</span><span class="sxs-lookup"><span data-stu-id="c82af-107">GetAssemblyStore Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-getassemblystore-method.md)|<span data-ttu-id="c82af-108">インターフェイス ポインターを取得、 [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)ホストによって読み込まれたアセンブリの一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="c82af-108">Gets an interface pointer to an [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) that represents the list of assemblies loaded by the host.</span></span>|  
|[<span data-ttu-id="c82af-109">GetNonHostStoreAssemblies メソッド</span><span class="sxs-lookup"><span data-stu-id="c82af-109">GetNonHostStoreAssemblies Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-getnonhoststoreassemblies-method.md)|<span data-ttu-id="c82af-110">インターフェイス ポインターを取得、 [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)ホストが CLR をロードを必要とするアセンブリの一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="c82af-110">Gets an interface pointer to an [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) that represents the list of assemblies that the host expects the CLR to load.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c82af-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="c82af-111">Remarks</span></span>  
 <span data-ttu-id="c82af-112">ホストが実装する必要はありません`IHostAssemblyManager`または`IHostAssemblyStore`します。</span><span class="sxs-lookup"><span data-stu-id="c82af-112">The host is not required to implement `IHostAssemblyManager` or `IHostAssemblyStore`.</span></span> <span data-ttu-id="c82af-113">ホストが実装して場合`IHostAssemblyManager`、実装する必要も`IHostAssemblyStore`。</span><span class="sxs-lookup"><span data-stu-id="c82af-113">If the host does implement `IHostAssemblyManager`, it must also implement `IHostAssemblyStore`.</span></span>  
  
 <span data-ttu-id="c82af-114">ランタイムをクエリ、`IHostAssemblyManager`呼び出して[ihostcontrol::gethostmanager](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-gethostmanager-method.md)の初期化時に、 `IID` IID_IHostAssemblyManager の。</span><span class="sxs-lookup"><span data-stu-id="c82af-114">The runtime queries for an `IHostAssemblyManager` by calling [IHostControl::GetHostManager](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-gethostmanager-method.md) upon initialization with an `IID` of IID_IHostAssemblyManager.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c82af-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="c82af-115">Requirements</span></span>  
 <span data-ttu-id="c82af-116">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c82af-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c82af-117">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="c82af-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c82af-118">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="c82af-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c82af-119">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c82af-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c82af-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="c82af-120">See also</span></span>
- [<span data-ttu-id="c82af-121">ICLRAssemblyReferenceList インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c82af-121">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="c82af-122">IHostAssemblyStore インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c82af-122">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
- [<span data-ttu-id="c82af-123">IHostControl インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c82af-123">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)
- [<span data-ttu-id="c82af-124">ホスト インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c82af-124">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
