---
title: ICLRStrongName::StrongNameKeyInstall メソッド
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameKeyInstall
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameKeyInstall
helpviewer_keywords:
- ICLRStrongName::StrongNameKeyInstall method [.NET Framework hosting]
- StrongNameKeyInstall method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 5c15cf3b-164c-49d1-8e57-e42949d55acf
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d60e1e503cd48b9b9e2ed91a6bfea000aeeea2af
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43399216"
---
# <a name="iclrstrongnamestrongnamekeyinstall-method"></a><span data-ttu-id="f7c1b-102">ICLRStrongName::StrongNameKeyInstall メソッド</span><span class="sxs-lookup"><span data-stu-id="f7c1b-102">ICLRStrongName::StrongNameKeyInstall Method</span></span>
<span data-ttu-id="f7c1b-103">公開/秘密キー ペアをコンテナーにインポートします。</span><span class="sxs-lookup"><span data-stu-id="f7c1b-103">Imports a public/private key pair into a container.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f7c1b-104">構文</span><span class="sxs-lookup"><span data-stu-id="f7c1b-104">Syntax</span></span>  
  
```  
HRESULT StrongNameKeyInstall (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f7c1b-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7c1b-105">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="f7c1b-106">[in]キー コンテナーの名前。</span><span class="sxs-lookup"><span data-stu-id="f7c1b-106">[in] The name of the key container.</span></span> <span data-ttu-id="f7c1b-107">`wszKeyContainer` 空でない文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7c1b-107">`wszKeyContainer` must be a non-empty string.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="f7c1b-108">[in]バイナリ キーのペアです。</span><span class="sxs-lookup"><span data-stu-id="f7c1b-108">[in] The binary key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="f7c1b-109">[in]サイズ (バイト単位) の`pbKeyBlob`します。</span><span class="sxs-lookup"><span data-stu-id="f7c1b-109">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f7c1b-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7c1b-110">Return Value</span></span>  
 <span data-ttu-id="f7c1b-111">`S_OK` メソッドが正常に完了した場合それ以外の場合、エラーを示す HRESULT 値 (を参照してください[の共通 HRESULT 値](https://go.microsoft.com/fwlink/?LinkId=213878)一覧については)。</span><span class="sxs-lookup"><span data-stu-id="f7c1b-111">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f7c1b-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="f7c1b-112">Remarks</span></span>  
 <span data-ttu-id="f7c1b-113">使用して、 [iclrstrongname::strongnamekeydelete](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeydelete-method.md)キー コンテナーを削除するメソッド。</span><span class="sxs-lookup"><span data-stu-id="f7c1b-113">Use the [ICLRStrongName::StrongNameKeyDelete](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeydelete-method.md) method to delete the key container.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f7c1b-114">要件</span><span class="sxs-lookup"><span data-stu-id="f7c1b-114">Requirements</span></span>  
 <span data-ttu-id="f7c1b-115">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7c1b-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f7c1b-116">**ヘッダー:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="f7c1b-116">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="f7c1b-117">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="f7c1b-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f7c1b-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f7c1b-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f7c1b-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7c1b-119">See Also</span></span>  
 [<span data-ttu-id="f7c1b-120">StrongNameKeyDelete メソッド</span><span class="sxs-lookup"><span data-stu-id="f7c1b-120">StrongNameKeyDelete Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeydelete-method.md)  
 [<span data-ttu-id="f7c1b-121">ICLRStrongName インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f7c1b-121">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
