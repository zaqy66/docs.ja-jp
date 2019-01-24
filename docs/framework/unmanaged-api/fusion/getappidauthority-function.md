---
title: GetAppIdAuthority 関数
ms.date: 03/30/2017
api_name:
- GetAppIdAuthority
api_location:
- fusion.dll
- clr.dll
api_type:
- COM
f1_keywords:
- GetAppIdAuthority
helpviewer_keywords:
- GetAppIdAuthority function [.NET Framework fusion]
ms.assetid: 9f968dad-0d09-47fb-bebc-94c39a0d16ad
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c45da047d384e56440ca5f883a4cfd755a7d0299
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54719714"
---
# <a name="getappidauthority-function"></a><span data-ttu-id="81f30-102">GetAppIdAuthority 関数</span><span class="sxs-lookup"><span data-stu-id="81f30-102">GetAppIdAuthority Function</span></span>
<span data-ttu-id="81f30-103">ポインターを取得、 [IAppIdAuthority](../../../../docs/framework/unmanaged-api/fusion/iappidauthority-interface.md)アプリケーション id と参照のキーを管理するインスタンス。</span><span class="sxs-lookup"><span data-stu-id="81f30-103">Gets a pointer to an [IAppIdAuthority](../../../../docs/framework/unmanaged-api/fusion/iappidauthority-interface.md) instance that manages keys for application identities and references.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81f30-104">構文</span><span class="sxs-lookup"><span data-stu-id="81f30-104">Syntax</span></span>  
  
```  
HRESULT GetAppIdAuthority (  
    [out] IAppIdAuthority **ppIAppIdAuthority  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="81f30-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81f30-105">Parameters</span></span>  
 `ppIAppIdAuthority`  
 <span data-ttu-id="81f30-106">[out]返された`IAppIdAuthority`ポインター。</span><span class="sxs-lookup"><span data-stu-id="81f30-106">[out] The returned `IAppIdAuthority` pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="81f30-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="81f30-107">Requirements</span></span>  
 <span data-ttu-id="81f30-108">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="81f30-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="81f30-109">**ヘッダー:** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="81f30-109">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="81f30-110">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="81f30-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81f30-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="81f30-111">See also</span></span>
- [<span data-ttu-id="81f30-112">IAppIdAuthority インターフェイス</span><span class="sxs-lookup"><span data-stu-id="81f30-112">IAppIdAuthority Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iappidauthority-interface.md)
- [<span data-ttu-id="81f30-113">Fusion グローバル静的関数</span><span class="sxs-lookup"><span data-stu-id="81f30-113">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
