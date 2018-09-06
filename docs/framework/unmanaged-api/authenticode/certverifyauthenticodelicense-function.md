---
title: CertVerifyAuthenticodeLicense 関数
ms.date: 03/30/2017
api_name:
- CertVerifyAuthenticodeLicense
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 00118de7-33c6-41c4-8e1f-5d5e35e0da83
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1c10d5f363d454a64f9052315514e896f90f7081
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43867960"
---
# <a name="certverifyauthenticodelicense-function"></a><span data-ttu-id="acf64-102">CertVerifyAuthenticodeLicense 関数</span><span class="sxs-lookup"><span data-stu-id="acf64-102">CertVerifyAuthenticodeLicense Function</span></span>
<span data-ttu-id="acf64-103">Authenticode XrML ライセンスの有効性を検証します。</span><span class="sxs-lookup"><span data-stu-id="acf64-103">Verifies the validity of an Authenticode XrML license.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="acf64-104">構文</span><span class="sxs-lookup"><span data-stu-id="acf64-104">Syntax</span></span>  
  
```  
HRESULT CertVerifyAuthenticodeLicense (  
    [in]   PCRYPT_DATA_BLOB                   pLicenseBlob,  
    [in]   OPTIONAL DWORD                     dwFlags,  
    [out]  PAXL_AUTHENTICODE_SIGNER_INFO      pSignerInfo,  
    [out]  PAXL_AUTHENTICODE_TIMESTAMPER_INFO pTimestamperInfo  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="acf64-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="acf64-105">Parameters</span></span>  
 `pLicenseBlob`  
 <span data-ttu-id="acf64-106">[in] 検証する Authenticode XrML ライセンス。</span><span class="sxs-lookup"><span data-stu-id="acf64-106">[in] The Authenticode XrML license to be verified.</span></span>  
  
 <span data-ttu-id="acf64-107">参照してください、 [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob)構造体。</span><span class="sxs-lookup"><span data-stu-id="acf64-107">See the [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="acf64-108">[in] オプション。</span><span class="sxs-lookup"><span data-stu-id="acf64-108">[in] Optional.</span></span> <span data-ttu-id="acf64-109">以下の値の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="acf64-109">A combination of following values:</span></span>  
  
-   <span data-ttu-id="acf64-110">AXL_REVOCATION_NO_CHECK</span><span class="sxs-lookup"><span data-stu-id="acf64-110">AXL_REVOCATION_NO_CHECK</span></span>  
  
-   <span data-ttu-id="acf64-111">AXL_REVOCATION_CHECK_END_CERT_ONLY</span><span class="sxs-lookup"><span data-stu-id="acf64-111">AXL_REVOCATION_CHECK_END_CERT_ONLY</span></span>  
  
-   <span data-ttu-id="acf64-112">AXL_REVOCATION_CHECK_ENTIRE_CHAIN</span><span class="sxs-lookup"><span data-stu-id="acf64-112">AXL_REVOCATION_CHECK_ENTIRE_CHAIN</span></span>  
  
-   <span data-ttu-id="acf64-113">AXL_URL_CACHE_ONLY_RETRIEVAL</span><span class="sxs-lookup"><span data-stu-id="acf64-113">AXL_URL_CACHE_ONLY_RETRIEVAL</span></span>  
  
-   <span data-ttu-id="acf64-114">AXL_LIFETIME_SIGNING</span><span class="sxs-lookup"><span data-stu-id="acf64-114">AXL_LIFETIME_SIGNING</span></span>  
  
-   <span data-ttu-id="acf64-115">AXL_TRUST_MICROSOFT_ROOT_ONLY</span><span class="sxs-lookup"><span data-stu-id="acf64-115">AXL_TRUST_MICROSOFT_ROOT_ONLY</span></span>  
  
 `pSignerInfo`  
 <span data-ttu-id="acf64-116">[out] 署名者の情報を受け取るため。</span><span class="sxs-lookup"><span data-stu-id="acf64-116">[out] To receive the signer's information.</span></span> <span data-ttu-id="acf64-117">ライセンスに署名がない場合、`dwError` は TRUST_E_NOSIGNATURE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="acf64-117">If the license wasn't signed, `dwError` is set to TRUST_E_NOSIGNATURE.</span></span> <span data-ttu-id="acf64-118">使用してリソースを解放する呼び出し元の責任、 [CertFreeAuthenticodeSignerInfo](../../../../docs/framework/unmanaged-api/authenticode/certfreeauthenticodesignerinfo-function.md)使用後に機能します。</span><span class="sxs-lookup"><span data-stu-id="acf64-118">It is the caller's responsibility to free resources by using the [CertFreeAuthenticodeSignerInfo](../../../../docs/framework/unmanaged-api/authenticode/certfreeauthenticodesignerinfo-function.md) function after use.</span></span>  
  
 <span data-ttu-id="acf64-119">参照してください[AXL_AUTHENTICODE_SIGNER_INFO 構造体](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md)します。</span><span class="sxs-lookup"><span data-stu-id="acf64-119">See [AXL_AUTHENTICODE_SIGNER_INFO Structure](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md).</span></span>  
  
 `pTimestamperInfo`  
 <span data-ttu-id="acf64-120">[out] 可能な場合は、タイム スタンプの情報を受け取るため。</span><span class="sxs-lookup"><span data-stu-id="acf64-120">[out] To receive time stamper's information, if available.</span></span> <span data-ttu-id="acf64-121">ライセンスにタイム スタンプがない場合、`dwError` は TRUST_E_NOSIGNATURE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="acf64-121">If the license was not time-stamped, `dwError` is set to TRUST_E_NOSIGNATURE.</span></span> <span data-ttu-id="acf64-122">使用してリソースを解放する呼び出し元の責任、 [CertFreeAuthenticodeTimestamperInfo](../../../../docs/framework/unmanaged-api/authenticode/certfreeauthenticodetimestamperinfo-function.md)使用後に機能します。</span><span class="sxs-lookup"><span data-stu-id="acf64-122">It is the caller's responsibility to free resources by using the [CertFreeAuthenticodeTimestamperInfo](../../../../docs/framework/unmanaged-api/authenticode/certfreeauthenticodetimestamperinfo-function.md) function after use.</span></span>  
  
 <span data-ttu-id="acf64-123">参照してください[AXL_AUTHENTICODE_TIMESTAMPER_INFO 構造体](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-timestamper-info-structure.md)します。</span><span class="sxs-lookup"><span data-stu-id="acf64-123">See [AXL_AUTHENTICODE_TIMESTAMPER_INFO Structure](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-timestamper-info-structure.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="acf64-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="acf64-124">Return Value</span></span>  
 <span data-ttu-id="acf64-125">正常に終了した場合は `S_OK` を返します。</span><span class="sxs-lookup"><span data-stu-id="acf64-125">Returns `S_OK` if successful.</span></span> <span data-ttu-id="acf64-126">それ以外の場合はエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="acf64-126">Otherwise, returns an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="acf64-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="acf64-127">See Also</span></span>  
 [<span data-ttu-id="acf64-128">Authenticode</span><span class="sxs-lookup"><span data-stu-id="acf64-128">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)  
 [<span data-ttu-id="acf64-129">GetHashFromHandle メソッド</span><span class="sxs-lookup"><span data-stu-id="acf64-129">GetHashFromHandle Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromhandle-method.md)  
 [<span data-ttu-id="acf64-130">ICLRStrongName インターフェイス</span><span class="sxs-lookup"><span data-stu-id="acf64-130">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
