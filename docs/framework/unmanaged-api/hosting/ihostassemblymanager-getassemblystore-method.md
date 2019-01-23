---
title: IHostAssemblyManager::GetAssemblyStore メソッド
ms.date: 03/30/2017
api_name:
- IHostAssemblyManager.GetAssemblyStore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyManager::GetAssemblyStore
helpviewer_keywords:
- IHostAssemblyManager::GetAssemblyStore method [.NET Framework hosting]
- GetAssemblyStore method [.NET Framework hosting]
ms.assetid: d0f74593-9bb1-4a11-8096-e29734b20698
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 257c6856b54d77c4df0012880c9eac59884b52d9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571001"
---
# <a name="ihostassemblymanagergetassemblystore-method"></a><span data-ttu-id="b753d-102">IHostAssemblyManager::GetAssemblyStore メソッド</span><span class="sxs-lookup"><span data-stu-id="b753d-102">IHostAssemblyManager::GetAssemblyStore Method</span></span>
<span data-ttu-id="b753d-103">インターフェイス ポインターを取得、 [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)ホストによって読み込まれたアセンブリの一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="b753d-103">Gets an interface pointer to an [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) that represents the list of assemblies loaded by the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b753d-104">構文</span><span class="sxs-lookup"><span data-stu-id="b753d-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyStore (  
    [out] IHostAssemblyStore **ppAssemblyStore  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b753d-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b753d-105">Parameters</span></span>  
 `ppAssemblyStore`  
 <span data-ttu-id="b753d-106">[out]関数へのポインター、`IHostAssemblyStore`インスタンス、またはホストが実装していない場合は、null`IHostAssemblyStore`します。</span><span class="sxs-lookup"><span data-stu-id="b753d-106">[out] A function pointer to an `IHostAssemblyStore` instance, or null, if the host does not implement `IHostAssemblyStore`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b753d-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="b753d-107">Return Value</span></span>  
  
|<span data-ttu-id="b753d-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b753d-108">HRESULT</span></span>|<span data-ttu-id="b753d-109">説明</span><span class="sxs-lookup"><span data-stu-id="b753d-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b753d-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b753d-110">S_OK</span></span>|<span data-ttu-id="b753d-111">`GetAssemblyStore` 正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="b753d-111">`GetAssemblyStore` returned successfully.</span></span>|  
|<span data-ttu-id="b753d-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b753d-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b753d-113">共通言語ランタイム (CLR) は、プロセスに読み込まれていないか、CLR は状態をマネージ コードを実行または呼び出しを正常に処理ができません。</span><span class="sxs-lookup"><span data-stu-id="b753d-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b753d-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b753d-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b753d-115">呼び出しがタイムアウトになりました。</span><span class="sxs-lookup"><span data-stu-id="b753d-115">The call timed out.</span></span>|  
|<span data-ttu-id="b753d-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b753d-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b753d-117">呼び出し元がロックを所有していません。</span><span class="sxs-lookup"><span data-stu-id="b753d-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b753d-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b753d-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b753d-119">イベントがキャンセルされましたブロックされたスレッドまたはファイバーが待機しています。</span><span class="sxs-lookup"><span data-stu-id="b753d-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b753d-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b753d-120">E_FAIL</span></span>|<span data-ttu-id="b753d-121">不明な致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="b753d-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b753d-122">メソッドには、E_FAIL が返される、ときに、CLR は、プロセス内で使用可能ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="b753d-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b753d-123">メソッドをホストする後続の呼び出しには、HOST_E_CLRNOTAVAILABLE が返されます。</span><span class="sxs-lookup"><span data-stu-id="b753d-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="b753d-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="b753d-124">E_NOINTERFACE</span></span>|<span data-ttu-id="b753d-125">ホストがの実装を提供しない`IHostAssemblyStore`します。</span><span class="sxs-lookup"><span data-stu-id="b753d-125">The host does not provide an implementation of `IHostAssemblyStore`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b753d-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="b753d-126">Remarks</span></span>  
 <span data-ttu-id="b753d-127">`IHostAssemblyStore` ホストがアセンブリと CLR とは無関係にモジュールにバインドできるようにするメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="b753d-127">`IHostAssemblyStore` provides methods that allow a host to bind to assemblies and modules independently of the CLR.</span></span> <span data-ttu-id="b753d-128">ホストは、通常、ファイル システム以外の形式から読み込まれるアセンブリを許可するアセンブリのストアを提供します。</span><span class="sxs-lookup"><span data-stu-id="b753d-128">Hosts typically provide assembly stores to allow assemblies to be loaded from formats other than the file system.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b753d-129">ホストが実装していない場合`IHostAssemblyStore`、 `GetAssemblyStore` E_NOINTERFACE の HRESULT 値を返す必要があり、設定する必要があります`ppAssemblyStore`を null にします。</span><span class="sxs-lookup"><span data-stu-id="b753d-129">If the host does not implement `IHostAssemblyStore`, `GetAssemblyStore` should return an HRESULT value of E_NOINTERFACE, and should set `ppAssemblyStore` to null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b753d-130">必要条件</span><span class="sxs-lookup"><span data-stu-id="b753d-130">Requirements</span></span>  
 <span data-ttu-id="b753d-131">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b753d-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b753d-132">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b753d-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b753d-133">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="b753d-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b753d-134">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b753d-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b753d-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="b753d-135">See also</span></span>
- [<span data-ttu-id="b753d-136">IHostAssemblyManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b753d-136">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)
- [<span data-ttu-id="b753d-137">IHostAssemblyStore インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b753d-137">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
