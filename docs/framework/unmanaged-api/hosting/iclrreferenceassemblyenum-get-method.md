---
title: ICLRReferenceAssemblyEnum::Get メソッド
ms.date: 03/30/2017
api_name:
- ICLRReferenceAssemblyEnum.Get
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRReferenceAssemblyEnum::Get
helpviewer_keywords:
- ICLRReferenceAssemblyEnum::Get method [.NET Framework hosting]
- Get method, ICLRReferenceAssemblyEnum interface [.NET Framework hosting]
ms.assetid: f21c1612-9c5d-4abc-a337-577086d29c17
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ac7e551cad12766f3472289889907d6972663567
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54617370"
---
# <a name="iclrreferenceassemblyenumget-method"></a><span data-ttu-id="e5c35-102">ICLRReferenceAssemblyEnum::Get メソッド</span><span class="sxs-lookup"><span data-stu-id="e5c35-102">ICLRReferenceAssemblyEnum::Get Method</span></span>
<span data-ttu-id="e5c35-103">指定したインデックス位置にあるアセンブリの id を取得します。</span><span class="sxs-lookup"><span data-stu-id="e5c35-103">Gets the assembly identity at the supplied index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5c35-104">構文</span><span class="sxs-lookup"><span data-stu-id="e5c35-104">Syntax</span></span>  
  
```  
HRESULT Get (  
    [in] DWORD dwIndex,  
    [out, size_is(*pcchBufferSize)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBufferSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e5c35-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e5c35-105">Parameters</span></span>  
 `dwIndex`  
 <span data-ttu-id="e5c35-106">[in]アセンブリ id を返すの 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="e5c35-106">[in] The zero-based index of the assembly identity to return.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="e5c35-107">[out]アセンブリの id データを格納するバッファー。</span><span class="sxs-lookup"><span data-stu-id="e5c35-107">[out] A buffer containing the assembly identity data.</span></span>  
  
 `pcchBufferSize`  
 <span data-ttu-id="e5c35-108">[入力、出力]サイズ、`pwzBuffer`バッファー。</span><span class="sxs-lookup"><span data-stu-id="e5c35-108">[in, out] The size of the `pwzBuffer` buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e5c35-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="e5c35-109">Return Value</span></span>  
  
|<span data-ttu-id="e5c35-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e5c35-110">HRESULT</span></span>|<span data-ttu-id="e5c35-111">説明</span><span class="sxs-lookup"><span data-stu-id="e5c35-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e5c35-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5c35-112">S_OK</span></span>|<span data-ttu-id="e5c35-113">`Get` 正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="e5c35-113">`Get` returned successfully.</span></span>|  
|<span data-ttu-id="e5c35-114">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="e5c35-114">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="e5c35-115">`pwzBuffer` が小さすぎます。</span><span class="sxs-lookup"><span data-stu-id="e5c35-115">`pwzBuffer` is too small.</span></span>|  
|<span data-ttu-id="e5c35-116">ERROR_NO_MORE_ITEMS</span><span class="sxs-lookup"><span data-stu-id="e5c35-116">ERROR_NO_MORE_ITEMS</span></span>|<span data-ttu-id="e5c35-117">列挙には、これ以上項目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e5c35-117">The enumeration contains no more items.</span></span>|  
|<span data-ttu-id="e5c35-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e5c35-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e5c35-119">共通言語ランタイム (CLR) は、プロセスに読み込まれていないか、CLR は状態をマネージ コードを実行または呼び出しを正常に処理ができません。</span><span class="sxs-lookup"><span data-stu-id="e5c35-119">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="e5c35-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e5c35-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="e5c35-121">呼び出しがタイムアウトになりました。</span><span class="sxs-lookup"><span data-stu-id="e5c35-121">The call timed out.</span></span>|  
|<span data-ttu-id="e5c35-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="e5c35-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="e5c35-123">呼び出し元がロックを所有していません。</span><span class="sxs-lookup"><span data-stu-id="e5c35-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="e5c35-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="e5c35-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="e5c35-125">イベントがキャンセルされましたブロックされたスレッドまたはファイバーが待機しています。</span><span class="sxs-lookup"><span data-stu-id="e5c35-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="e5c35-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e5c35-126">E_FAIL</span></span>|<span data-ttu-id="e5c35-127">不明な致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="e5c35-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="e5c35-128">メソッドから E_FAIL が返された場合、CLR は、プロセス内で使用可能ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="e5c35-128">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="e5c35-129">メソッドをホストする後続の呼び出しには、HOST_E_CLRNOTAVAILABLE が返されます。</span><span class="sxs-lookup"><span data-stu-id="e5c35-129">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e5c35-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="e5c35-130">Remarks</span></span>  
 <span data-ttu-id="e5c35-131">`Get` 通常は 2 回呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e5c35-131">`Get` is typically called twice.</span></span> <span data-ttu-id="e5c35-132">最初の呼び出しには、null 値が指定されています`pwzBuffer`、設定と`pcchBufferSize`の適切なサイズに`pwzBuffer`します。</span><span class="sxs-lookup"><span data-stu-id="e5c35-132">The first call supplies a null value for `pwzBuffer`, and sets `pcchBufferSize` to the size appropriate for `pwzBuffer`.</span></span> <span data-ttu-id="e5c35-133">2 つ目の呼び出しが適切なサイズ指定されています`pwzBuffer`、完了すると標準アセンブリの id データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e5c35-133">The second call supplies an appropriately sized `pwzBuffer`, and contains the canonical assembly identity data upon completion.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5c35-134">必要条件</span><span class="sxs-lookup"><span data-stu-id="e5c35-134">Requirements</span></span>  
 <span data-ttu-id="e5c35-135">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5c35-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5c35-136">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e5c35-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e5c35-137">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="e5c35-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e5c35-138">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5c35-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5c35-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5c35-139">See also</span></span>
- [<span data-ttu-id="e5c35-140">ICLRAssemblyReferenceList インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e5c35-140">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="e5c35-141">ICLRReferenceAssemblyEnum インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e5c35-141">ICLRReferenceAssemblyEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrreferenceassemblyenum-interface.md)
