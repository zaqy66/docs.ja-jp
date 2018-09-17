---
title: ICLRStrongName::GetHashFromHandle メソッド
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromHandle
- ICLRStrongName.StrongNameCompareAssemblies
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromHandle
helpviewer_keywords:
- GetHashFromHandle method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::GetHashFromHandle method [.NET Framework hosting]
ms.assetid: 3bedbb7d-3cdd-4175-b370-10ae734062db
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 20c5f6bbb58b85f42ec00e356eccc5fb41ce813c
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45743606"
---
# <a name="iclrstrongnamegethashfromhandle-method"></a><span data-ttu-id="0b5f7-102">ICLRStrongName::GetHashFromHandle メソッド</span><span class="sxs-lookup"><span data-stu-id="0b5f7-102">ICLRStrongName::GetHashFromHandle Method</span></span>
<span data-ttu-id="0b5f7-103">指定したハッシュ アルゴリズムを使用して、指定したファイル ハンドルを含むファイルのコンテンツのハッシュを生成します。</span><span class="sxs-lookup"><span data-stu-id="0b5f7-103">Generates a hash over the contents of the file that has the specified file handle, using the specified hash algorithm.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b5f7-104">構文</span><span class="sxs-lookup"><span data-stu-id="0b5f7-104">Syntax</span></span>  
  
```  
HRESULT GetHashFromHandle (  
    [in]  HANDLE   hFile,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0b5f7-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0b5f7-105">Parameters</span></span>  
 `hFile`  
 <span data-ttu-id="0b5f7-106">[in]ハッシュされるファイルのハンドル。</span><span class="sxs-lookup"><span data-stu-id="0b5f7-106">[in] The handle of the file to be hashed.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="0b5f7-107">[入力、出力]ハッシュ アルゴリズムを指定する定数。</span><span class="sxs-lookup"><span data-stu-id="0b5f7-107">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="0b5f7-108">既定のアルゴリズムに 0 を使用します。</span><span class="sxs-lookup"><span data-stu-id="0b5f7-108">Use zero for the default algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="0b5f7-109">[out]返されたハッシュ バッファー。</span><span class="sxs-lookup"><span data-stu-id="0b5f7-109">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="0b5f7-110">[in]要求の最大サイズの`pbHash`します。</span><span class="sxs-lookup"><span data-stu-id="0b5f7-110">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="0b5f7-111">[out]サイズ (バイト単位)、返された`pbHash`します。</span><span class="sxs-lookup"><span data-stu-id="0b5f7-111">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0b5f7-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="0b5f7-112">Return Value</span></span>  
 <span data-ttu-id="0b5f7-113">`S_OK` メソッドが正常に完了した場合それ以外の場合、エラーを示す HRESULT 値 (を参照してください[の共通 HRESULT 値](https://go.microsoft.com/fwlink/?LinkId=213878)一覧については)。</span><span class="sxs-lookup"><span data-stu-id="0b5f7-113">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0b5f7-114">要件</span><span class="sxs-lookup"><span data-stu-id="0b5f7-114">Requirements</span></span>  
 <span data-ttu-id="0b5f7-115">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b5f7-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0b5f7-116">**ヘッダー:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="0b5f7-116">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="0b5f7-117">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="0b5f7-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0b5f7-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0b5f7-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b5f7-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b5f7-119">See Also</span></span>  
 [<span data-ttu-id="0b5f7-120">ICLRStrongName インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0b5f7-120">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
