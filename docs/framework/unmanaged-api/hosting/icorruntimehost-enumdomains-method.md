---
title: ICorRuntimeHost::EnumDomains メソッド
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.EnumDomains
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::EnumDomains
helpviewer_keywords:
- ICorRuntimeHost::EnumDomains method [.NET Framework hosting]
- EnumDomains method [.NET Framework hosting]
ms.assetid: 96b74995-0cde-4876-b6df-7fc164e6a5d1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8e4db2330c6d46610bbb3da8b732b1c098659c97
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54729081"
---
# <a name="icorruntimehostenumdomains-method"></a><span data-ttu-id="89339-102">ICorRuntimeHost::EnumDomains メソッド</span><span class="sxs-lookup"><span data-stu-id="89339-102">ICorRuntimeHost::EnumDomains Method</span></span>
<span data-ttu-id="89339-103">現在のプロセスで、ドメインの列挙子を取得します。</span><span class="sxs-lookup"><span data-stu-id="89339-103">Gets an enumerator for the domains in the current process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="89339-104">構文</span><span class="sxs-lookup"><span data-stu-id="89339-104">Syntax</span></span>  
  
```  
HRESULT EnumDomains (  
    [out] HCORENUM *hEnum  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="89339-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89339-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="89339-106">[out]ドメインの列挙子。</span><span class="sxs-lookup"><span data-stu-id="89339-106">[out] An enumerator for the domains.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="89339-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="89339-107">Return Value</span></span>  
  
|<span data-ttu-id="89339-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="89339-108">HRESULT</span></span>|<span data-ttu-id="89339-109">説明</span><span class="sxs-lookup"><span data-stu-id="89339-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="89339-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="89339-110">S_OK</span></span>|<span data-ttu-id="89339-111">操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="89339-111">The operation was successful.</span></span>|  
|<span data-ttu-id="89339-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="89339-112">S_FALSE</span></span>|<span data-ttu-id="89339-113">操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="89339-113">The operation failed to complete.</span></span>|  
|<span data-ttu-id="89339-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="89339-114">E_FAIL</span></span>|<span data-ttu-id="89339-115">未知の致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="89339-115">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="89339-116">場合は、メソッドは、E_FAIL を返します、共通言語ランタイム (CLR) はプロセスで使用可能ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="89339-116">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="89339-117">Api をホストする後続の呼び出しには、HOST_E_CLRNOTAVAILABLE が返されます。</span><span class="sxs-lookup"><span data-stu-id="89339-117">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="89339-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="89339-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="89339-119">プロセスに CLR が読み込まれていないか、CLR は状態をマネージ コードを実行または呼び出しを正常に処理ができません。</span><span class="sxs-lookup"><span data-stu-id="89339-119">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="89339-120">必要条件</span><span class="sxs-lookup"><span data-stu-id="89339-120">Requirements</span></span>  
 <span data-ttu-id="89339-121">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="89339-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="89339-122">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="89339-122">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="89339-123">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="89339-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="89339-124">**.NET framework のバージョン:** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="89339-124">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="89339-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="89339-125">See also</span></span>
- [<span data-ttu-id="89339-126">ICorRuntimeHost インターフェイス</span><span class="sxs-lookup"><span data-stu-id="89339-126">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
