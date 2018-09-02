---
title: ICLRStrongName::StrongNameGetBlobFromImage メソッド
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameGetBlobFromImage
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameGetBlobFromImage
helpviewer_keywords:
- StrongNameGetBlobFromImage method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameGetBlobFromImage method [.NET Framework hosting]
ms.assetid: 0f5a2ec8-e776-4fd8-bda6-937b6834575a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cd6cb0116e1080a68c91df365cc7dd1485b21791
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43421542"
---
# <a name="iclrstrongnamestrongnamegetblobfromimage-method"></a><span data-ttu-id="ea65a-102">ICLRStrongName::StrongNameGetBlobFromImage メソッド</span><span class="sxs-lookup"><span data-stu-id="ea65a-102">ICLRStrongName::StrongNameGetBlobFromImage Method</span></span>
<span data-ttu-id="ea65a-103">指定されたメモリ アドレスにあるアセンブリの画像のバイナリ表現を取得します。</span><span class="sxs-lookup"><span data-stu-id="ea65a-103">Gets a binary representation of the assembly image at the specified memory address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea65a-104">構文</span><span class="sxs-lookup"><span data-stu-id="ea65a-104">Syntax</span></span>  
  
```  
HRESULT StrongNameGetBlobFromImage (  
    [in]  BYTE        *pbBase,  
    [in]  DWORD       dwLength,  
    [in]  BYTE        *pbBlob,  
    [in, out] DWORD   *pcbBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ea65a-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ea65a-105">Parameters</span></span>  
 `pbBase`  
 <span data-ttu-id="ea65a-106">[in]マップされているアセンブリ マニフェストのメモリ アドレス。</span><span class="sxs-lookup"><span data-stu-id="ea65a-106">[in] The memory address of the mapped assembly manifest.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="ea65a-107">[in]サイズをバイト単位でイメージの`pbBase`します。</span><span class="sxs-lookup"><span data-stu-id="ea65a-107">[in] The size, in bytes, of the image at `pbBase`.</span></span>  
  
 `pbBlob`  
 <span data-ttu-id="ea65a-108">[in]画像のバイナリ表現を格納するバッファー。</span><span class="sxs-lookup"><span data-stu-id="ea65a-108">[in] A buffer to contain the binary representation of the image.</span></span>  
  
 `pcbBlob`  
 <span data-ttu-id="ea65a-109">[入力、出力]最大サイズ (バイト単位) を要求された`pbBlob`します。</span><span class="sxs-lookup"><span data-stu-id="ea65a-109">[in, out] The requested maximum size, in bytes, of `pbBlob`.</span></span> <span data-ttu-id="ea65a-110">関数が戻るとき、実際のサイズをバイト単位の`pbBlob`します。</span><span class="sxs-lookup"><span data-stu-id="ea65a-110">Upon return, the actual size, in bytes, of `pbBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ea65a-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="ea65a-111">Return Value</span></span>  
 <span data-ttu-id="ea65a-112">`S_OK` メソッドが正常に完了した場合それ以外の場合、エラーを示す HRESULT 値 (を参照してください[の共通 HRESULT 値](https://go.microsoft.com/fwlink/?LinkId=213878)一覧については)。</span><span class="sxs-lookup"><span data-stu-id="ea65a-112">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ea65a-113">要件</span><span class="sxs-lookup"><span data-stu-id="ea65a-113">Requirements</span></span>  
 <span data-ttu-id="ea65a-114">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea65a-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ea65a-115">**ヘッダー:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="ea65a-115">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="ea65a-116">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="ea65a-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ea65a-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ea65a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea65a-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="ea65a-118">See Also</span></span>  
 [<span data-ttu-id="ea65a-119">StrongNameGetBlob メソッド</span><span class="sxs-lookup"><span data-stu-id="ea65a-119">StrongNameGetBlob Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblob-method.md)  
 [<span data-ttu-id="ea65a-120">ICLRStrongName インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ea65a-120">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
