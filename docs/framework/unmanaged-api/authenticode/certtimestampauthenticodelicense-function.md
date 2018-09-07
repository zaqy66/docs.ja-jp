---
title: CertTimestampAuthenticodeLicense 関数
ms.date: 03/30/2017
api_name:
- CertTimestampAuthenticodeLicense
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: d468325a-21c5-43ce-8567-84e342b22308
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fd77a8a81718837d55f3018564d0f4ba8fdc95ee
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44080327"
---
# <a name="certtimestampauthenticodelicense-function"></a><span data-ttu-id="a37c8-102">CertTimestampAuthenticodeLicense 関数</span><span class="sxs-lookup"><span data-stu-id="a37c8-102">CertTimestampAuthenticodeLicense Function</span></span>
<span data-ttu-id="a37c8-103">Authenticode XrML ライセンスにタイム スタンプを付けます。</span><span class="sxs-lookup"><span data-stu-id="a37c8-103">Time-stamps an Authenticode XrML license.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a37c8-104">構文</span><span class="sxs-lookup"><span data-stu-id="a37c8-104">Syntax</span></span>  
  
```  
HRESULT CertTimestampAuthenticodeLicense (  
    [in]  PCRYPT_DATA_BLOB   pSignedLicenseBlob,  
    [in]  LPCWSTR            pwszTimestampURI,  
    [out] PCRYPT_DATA_BLOB   pTimestampSignatureBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a37c8-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a37c8-105">Parameters</span></span>  
 `pSignedLicenseBlob`  
 <span data-ttu-id="a37c8-106">[in] タイム スタンプが付けられる、署名付きの Authenticode XrML ライセンス。</span><span class="sxs-lookup"><span data-stu-id="a37c8-106">[in] The signed Authenticode XrML license to be time-stamped.</span></span> <span data-ttu-id="a37c8-107">参照してください、 [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob)構造体。</span><span class="sxs-lookup"><span data-stu-id="a37c8-107">See the [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span></span>  
  
 `pwszTimestampURI`  
 <span data-ttu-id="a37c8-108">[in] タイム スタンプ サーバーの URI。</span><span class="sxs-lookup"><span data-stu-id="a37c8-108">[in] The time-stamp server's URI.</span></span>  
  
 `pTimestampSignatureBlob`  
 <span data-ttu-id="a37c8-109">[out] base64 でエンコードされたタイム スタンプの署名を取得するための、CRYPT_DATA_BLOB へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a37c8-109">[out] A pointer to CRYPT_DATA_BLOB to receive the base64-encoded time-stamp signature.</span></span> <span data-ttu-id="a37c8-110">解放する呼び出し元の責任`pTimestampSignatureBlob` -> `pbData`で`HepFree()`使用後にします。</span><span class="sxs-lookup"><span data-stu-id="a37c8-110">It is the caller's responsibility to free `pTimestampSignatureBlob`->`pbData` with `HepFree()` after use.</span></span> <span data-ttu-id="a37c8-111">参照してください、 [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob)構造体。</span><span class="sxs-lookup"><span data-stu-id="a37c8-111">See the [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a37c8-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="a37c8-112">Remarks</span></span>  
 <span data-ttu-id="a37c8-113">タイム スタンプの署名は、実際は PKCS #7 SignedData メッセージで、この内容は、ライセンスの署名の SignatureValue のバイナリ形式です。</span><span class="sxs-lookup"><span data-stu-id="a37c8-113">The time-stamp signature is actually a PKCS #7 SignedData message whose content is the binary form of the SignatureValue from the license's signature.</span></span> <span data-ttu-id="a37c8-114">これは基本的に、ライセンスの副署名として機能します。</span><span class="sxs-lookup"><span data-stu-id="a37c8-114">Basically, this acts as a counter-signature of the license.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a37c8-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="a37c8-115">Return Value</span></span>  
 <span data-ttu-id="a37c8-116">関数が成功した場合は `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="a37c8-116">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="a37c8-117">それ以外の場合はエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="a37c8-117">Otherwise, returns an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a37c8-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="a37c8-118">See Also</span></span>  
 [<span data-ttu-id="a37c8-119">Authenticode</span><span class="sxs-lookup"><span data-stu-id="a37c8-119">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
