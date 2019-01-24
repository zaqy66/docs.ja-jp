---
title: IInstallReferenceEnum::GetNextInstallReferenceItem メソッド
ms.date: 03/30/2017
api_name:
- IInstallReferenceEnum.GetNextInstallReferenceItem
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceEnum::GetNextInstallReferenceItem
helpviewer_keywords:
- IInstallReferenceEnum::GetNextInstallReferenceItem method [.NET Framework fusion]
- GetNextInstallReferenceItem method [.NET Framework fusion]
ms.assetid: ce969c9d-6538-4c34-8784-148ffd99fe7a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ba2abaccfc4a9ae2d1f07677a49a72c980acda24
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54607502"
---
# <a name="iinstallreferenceenumgetnextinstallreferenceitem-method"></a><span data-ttu-id="4862b-102">IInstallReferenceEnum::GetNextInstallReferenceItem メソッド</span><span class="sxs-lookup"><span data-stu-id="4862b-102">IInstallReferenceEnum::GetNextInstallReferenceItem Method</span></span>
<span data-ttu-id="4862b-103">次のポインターを取得[IInstallReferenceItem](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md)これに含まれるオブジェクト[IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md)オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="4862b-103">Gets a pointer to the next [IInstallReferenceItem](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md) object contained in this [IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4862b-104">構文</span><span class="sxs-lookup"><span data-stu-id="4862b-104">Syntax</span></span>  
  
```  
HRESULT GetNextInstallReferenceItem (  
    [out] IInstallReferenceItem **ppRefItem,  
    [in]  DWORD dwFlags,  
    [in]  LPVOID pvReserved  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4862b-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4862b-105">Parameters</span></span>  
 `ppRefItem`  
 <span data-ttu-id="4862b-106">[out]返された`IInstallReferenceItem`ポインター。</span><span class="sxs-lookup"><span data-stu-id="4862b-106">[out] The returned `IInstallReferenceItem` pointer.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="4862b-107">[入力] 将来の機能拡張に備えて予約されています。</span><span class="sxs-lookup"><span data-stu-id="4862b-107">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="4862b-108">`dwFlags` 0 (ゼロ) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4862b-108">`dwFlags` must be 0 (zero).</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="4862b-109">[入力] 将来の機能拡張に備えて予約されています。</span><span class="sxs-lookup"><span data-stu-id="4862b-109">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="4862b-110">`pvReserved` null 参照である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4862b-110">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4862b-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="4862b-111">Requirements</span></span>  
 <span data-ttu-id="4862b-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4862b-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4862b-113">**ヘッダー:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="4862b-113">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="4862b-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4862b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4862b-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="4862b-115">See also</span></span>
- [<span data-ttu-id="4862b-116">IInstallReferenceItem インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4862b-116">IInstallReferenceItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md)
- [<span data-ttu-id="4862b-117">IInstallReferenceEnum インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4862b-117">IInstallReferenceEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md)
