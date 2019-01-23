---
title: _AxlRSAKeyValueToPublicKeyToken 関数
ms.date: 03/30/2017
api_name:
- _AxlRSAKeyValueToPublicKeyToken
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: d60f19fe-7bec-47ba-b60e-ba9ce66abf8c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2a340af9ba196dbcd8618afdd83bcf7e56124bf7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54529909"
---
# <a name="axlrsakeyvaluetopublickeytoken-function"></a><span data-ttu-id="f189e-102">\_AxlRSAKeyValueToPublicKeyToken 関数</span><span class="sxs-lookup"><span data-stu-id="f189e-102">\_AxlRSAKeyValueToPublicKeyToken function</span></span>

<span data-ttu-id="f189e-103">Modulus および Exponent を、厳密な名前の公開キー トークンに変換します。</span><span class="sxs-lookup"><span data-stu-id="f189e-103">Converts a Modulus and Exponent to a strong name public key token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f189e-104">構文</span><span class="sxs-lookup"><span data-stu-id="f189e-104">Syntax</span></span>  
  
```  
HRESULT _AxlRSAKeyValueToPublicKeyToken (  
    [in]  PCRYPT_DATA_BLOB pModulusBlob,  
    [in]  PCRYPT_DATA_BLOB pExponentBlob,  
    [out] LPWSTR           *ppwszPublicKeyToken  
);  
```  
  
### <a name="parameters"></a><span data-ttu-id="f189e-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f189e-105">Parameters</span></span>  
 `pModulusBlob`  
 <span data-ttu-id="f189e-106">[in]Base64 でエンコードされた Modulus blob (から、 \<Modulus > 要素)。</span><span class="sxs-lookup"><span data-stu-id="f189e-106">[in] The base64-encoded Modulus blob (from the \<Modulus> element).</span></span>  <span data-ttu-id="f189e-107">参照してください、 [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob)構造体。</span><span class="sxs-lookup"><span data-stu-id="f189e-107">See the [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span></span>  
  
 `pExponentBlob`  
 <span data-ttu-id="f189e-108">[in]Base64 でエンコードされた Exponent blob (から、\<指数 > 要素)。</span><span class="sxs-lookup"><span data-stu-id="f189e-108">[in] The base64-encoded Exponent blob (from the \<Exponent> element).</span></span> <span data-ttu-id="f189e-109">参照してください、 [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob)構造体。</span><span class="sxs-lookup"><span data-stu-id="f189e-109">See the [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span></span>  
  
 `ppwszPublicKeyToken`  
 <span data-ttu-id="f189e-110">[out] 16 進エンコードされた公開キー トークンを受け取るための WCHAR \* へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f189e-110">[out] A pointer to WCHAR \* to receive the hex-encoded public key token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f189e-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="f189e-111">Return Value</span></span>  
 <span data-ttu-id="f189e-112">関数が成功した場合は `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="f189e-112">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="f189e-113">それ以外の場合はエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="f189e-113">Otherwise, returns an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f189e-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="f189e-114">See also</span></span>
- [<span data-ttu-id="f189e-115">Authenticode</span><span class="sxs-lookup"><span data-stu-id="f189e-115">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
