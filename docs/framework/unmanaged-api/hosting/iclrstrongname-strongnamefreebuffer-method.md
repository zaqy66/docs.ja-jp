---
title: ICLRStrongName::StrongNameFreeBuffer メソッド
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameFreeBuffer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameFreeBuffer
helpviewer_keywords:
- StrongNameFreeBuffer method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameFreeBuffer method [.NET Framework hosting]
ms.assetid: 6148c508-bd1d-4a37-85c3-06ecb09cc857
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6ec34bde2b94fc6e03cb01647be9e92daa8955a7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743193"
---
# <a name="iclrstrongnamestrongnamefreebuffer-method"></a><span data-ttu-id="0f2bd-102">ICLRStrongName::StrongNameFreeBuffer メソッド</span><span class="sxs-lookup"><span data-stu-id="0f2bd-102">ICLRStrongName::StrongNameFreeBuffer Method</span></span>
<span data-ttu-id="0f2bd-103">など、以前の厳密な名前のメソッド呼び出しで割り当てられたメモリを解放[iclrstrongname::strongnamegetpublickey](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetpublickey-method.md)、 [iclrstrongname::strongnametokenfrompublickey](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfrompublickey-method.md)、または[Iclrstrongname::strongnamesignaturegeneration](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturegeneration-method.md)します。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-103">Frees memory that was allocated with a previous call to a strong name method such as [ICLRStrongName::StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetpublickey-method.md), [ICLRStrongName::StrongNameTokenFromPublicKey](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfrompublickey-method.md), or [ICLRStrongName::StrongNameSignatureGeneration](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturegeneration-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f2bd-104">構文</span><span class="sxs-lookup"><span data-stu-id="0f2bd-104">Syntax</span></span>  
  
```  
HRESULT StrongNameFreeBuffer (   
   [in] BYTE   *pbMemory  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0f2bd-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f2bd-105">Parameters</span></span>  
 `pbMemory`  
 <span data-ttu-id="0f2bd-106">[in]解放するメモリへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-106">[in] A pointer to the memory to free.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0f2bd-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="0f2bd-107">Return Value</span></span>  
 <span data-ttu-id="0f2bd-108">`S_OK` メソッドが正常に完了した場合それ以外の場合、エラーを示す HRESULT 値 (を参照してください[の共通 HRESULT 値](https://go.microsoft.com/fwlink/?LinkId=213878)一覧については)。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-108">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f2bd-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="0f2bd-109">Requirements</span></span>  
 <span data-ttu-id="0f2bd-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f2bd-111">**ヘッダー:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="0f2bd-111">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="0f2bd-112">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="0f2bd-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0f2bd-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0f2bd-113">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f2bd-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f2bd-114">See also</span></span>
- [<span data-ttu-id="0f2bd-115">ICLRStrongName インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0f2bd-115">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
