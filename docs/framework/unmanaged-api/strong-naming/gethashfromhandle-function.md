---
title: GetHashFromHandle 関数
ms.date: 03/30/2017
api_name:
- GetHashFromHandle
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromHandle
helpviewer_keywords:
- GetHashFromHandle function [.NET Framework strong naming]
ms.assetid: 9e00337f-b307-4602-9bc3-965a8dbf02cd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: defa18bde8e5ce0f1cc7ff040aaa4fa0e95fd7e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54619219"
---
# <a name="gethashfromhandle-function"></a><span data-ttu-id="6989c-102">GetHashFromHandle 関数</span><span class="sxs-lookup"><span data-stu-id="6989c-102">GetHashFromHandle Function</span></span>
<span data-ttu-id="6989c-103">指定したハッシュ アルゴリズムを使用して、指定したファイル ハンドルを含むファイルの内容に対してハッシュが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6989c-103">Generates a hash over the contents of the file with the specified file handle, using the specified hash algorithm.</span></span>  
  
 <span data-ttu-id="6989c-104">この関数は非推奨とされました。</span><span class="sxs-lookup"><span data-stu-id="6989c-104">This function has been deprecated.</span></span> <span data-ttu-id="6989c-105">使用して、 [iclrstrongname::gethashfromhandle](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromhandle-method.md)メソッド代わりにします。</span><span class="sxs-lookup"><span data-stu-id="6989c-105">Use the [ICLRStrongName::GetHashFromHandle](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromhandle-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6989c-106">構文</span><span class="sxs-lookup"><span data-stu-id="6989c-106">Syntax</span></span>  
  
```  
HRESULT GetHashFromHandle (  
    [in]  HANDLE   hFile,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6989c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6989c-107">Parameters</span></span>  
 `hFile`  
 <span data-ttu-id="6989c-108">[in]ハッシュされるファイルのハンドル。</span><span class="sxs-lookup"><span data-stu-id="6989c-108">[in] The handle of the file to be hashed.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="6989c-109">[入力、出力]ハッシュ アルゴリズムを指定する定数。</span><span class="sxs-lookup"><span data-stu-id="6989c-109">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="6989c-110">既定のアルゴリズムに 0 を使用します。</span><span class="sxs-lookup"><span data-stu-id="6989c-110">Use zero for the default algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="6989c-111">[out]返されたハッシュ バッファー。</span><span class="sxs-lookup"><span data-stu-id="6989c-111">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="6989c-112">[in]要求の最大サイズの`pbHash`します。</span><span class="sxs-lookup"><span data-stu-id="6989c-112">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="6989c-113">[out]サイズ (バイト単位)、返された`pbHash`します。</span><span class="sxs-lookup"><span data-stu-id="6989c-113">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6989c-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="6989c-114">Requirements</span></span>  
 <span data-ttu-id="6989c-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6989c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6989c-116">**ヘッダー:** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="6989c-116">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="6989c-117">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="6989c-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6989c-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6989c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6989c-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="6989c-119">See also</span></span>
- [<span data-ttu-id="6989c-120">GetHashFromHandle メソッド</span><span class="sxs-lookup"><span data-stu-id="6989c-120">GetHashFromHandle Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromhandle-method.md)
- [<span data-ttu-id="6989c-121">ICLRStrongName インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6989c-121">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
