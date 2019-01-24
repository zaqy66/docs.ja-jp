---
title: CertFreeAuthenticodeSignerInfo 関数
ms.date: 03/30/2017
api_name:
- CertFreeAuthenticodeSignerInfo
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 8029633c-b6e4-4665-a7c2-89607c3247ef
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4282be8e57c965e14398a9284002b1191c5169fa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54708039"
---
# <a name="certfreeauthenticodesignerinfo-function"></a><span data-ttu-id="2f654-102">CertFreeAuthenticodeSignerInfo 関数</span><span class="sxs-lookup"><span data-stu-id="2f654-102">CertFreeAuthenticodeSignerInfo Function</span></span>
<span data-ttu-id="2f654-103">割り当てられているリソース、 [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="2f654-103">Frees resources allocated for the [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md) structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f654-104">構文</span><span class="sxs-lookup"><span data-stu-id="2f654-104">Syntax</span></span>  
  
```  
HRESULT CertFreeAuthenticodeSignerInfo (  
    [in, out]  PAXL_AUTHENTICODE_SIGNER_INFO   pSignerInfo);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2f654-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2f654-105">Parameters</span></span>  
 `pSignerInfo`  
 <span data-ttu-id="2f654-106">[in, out] リリースされる署名者情報。</span><span class="sxs-lookup"><span data-stu-id="2f654-106">[in, out] Signer information to be released.</span></span> <span data-ttu-id="2f654-107">参照してください、 [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="2f654-107">See the [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md) structure.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2f654-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="2f654-108">Return Value</span></span>  
 <span data-ttu-id="2f654-109">関数が成功した場合は `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="2f654-109">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="2f654-110">それ以外の場合はエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="2f654-110">Otherwise, returns an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f654-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f654-111">See also</span></span>
- [<span data-ttu-id="2f654-112">Authenticode</span><span class="sxs-lookup"><span data-stu-id="2f654-112">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
