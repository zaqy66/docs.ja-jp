---
title: StrongNameKeyInstall 関数
ms.date: 03/30/2017
api_name:
- StrongNameKeyInstall
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameKeyInstall
helpviewer_keywords:
- StrongNameKeyInstall function [.NET Framework strong naming]
ms.assetid: e32fd546-7757-4681-be3d-658e93281e50
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ecd52fce8033876f0599fa0ba25fae0850c0e01f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54508487"
---
# <a name="strongnamekeyinstall-function"></a><span data-ttu-id="493e1-102">StrongNameKeyInstall 関数</span><span class="sxs-lookup"><span data-stu-id="493e1-102">StrongNameKeyInstall Function</span></span>
<span data-ttu-id="493e1-103">公開/秘密キーの組がコンテナーにインポートされます。</span><span class="sxs-lookup"><span data-stu-id="493e1-103">Imports a public/private key pair into a container.</span></span>  
  
 <span data-ttu-id="493e1-104">この関数は非推奨とされました。</span><span class="sxs-lookup"><span data-stu-id="493e1-104">This function has been deprecated.</span></span> <span data-ttu-id="493e1-105">使用して、 [iclrstrongname::strongnamekeyinstall](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md)メソッド代わりにします。</span><span class="sxs-lookup"><span data-stu-id="493e1-105">Use the [ICLRStrongName::StrongNameKeyInstall](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="493e1-106">構文</span><span class="sxs-lookup"><span data-stu-id="493e1-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameKeyInstall (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="493e1-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="493e1-107">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="493e1-108">[in]キー コンテナーの名前。</span><span class="sxs-lookup"><span data-stu-id="493e1-108">[in] The name of the key container.</span></span> <span data-ttu-id="493e1-109">`wszKeyContainer` 空でない文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="493e1-109">`wszKeyContainer` must be a non-empty string.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="493e1-110">[in]バイナリ キーのペアです。</span><span class="sxs-lookup"><span data-stu-id="493e1-110">[in] The binary key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="493e1-111">[in]サイズ (バイト単位) の`pbKeyBlob`します。</span><span class="sxs-lookup"><span data-stu-id="493e1-111">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="493e1-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="493e1-112">Return Value</span></span>  
 <span data-ttu-id="493e1-113">`true` 正常に終了します。それ以外の場合、`false`します。</span><span class="sxs-lookup"><span data-stu-id="493e1-113">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="493e1-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="493e1-114">Remarks</span></span>  
 <span data-ttu-id="493e1-115">使用して、 [StrongNameKeyDelete](../../../../docs/framework/unmanaged-api/strong-naming/strongnamekeydelete-function.md)キー コンテナーを削除する関数。</span><span class="sxs-lookup"><span data-stu-id="493e1-115">Use the [StrongNameKeyDelete](../../../../docs/framework/unmanaged-api/strong-naming/strongnamekeydelete-function.md) function to delete the key container.</span></span>  
  
 <span data-ttu-id="493e1-116">場合、`StrongNameKeyInstall`関数が正常に完了、呼び出すしていない、 [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md)最後に生成されたエラーを取得します。</span><span class="sxs-lookup"><span data-stu-id="493e1-116">If the `StrongNameKeyInstall` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="493e1-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="493e1-117">Requirements</span></span>  
 <span data-ttu-id="493e1-118">**プラットフォーム:** WindSee[システム要件](../../../../docs/framework/get-started/system-requirements.md)します。</span><span class="sxs-lookup"><span data-stu-id="493e1-118">**Platforms:** WindSee [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="493e1-119">**ヘッダー:** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="493e1-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="493e1-120">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="493e1-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="493e1-121">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="493e1-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="493e1-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="493e1-122">See also</span></span>
- [<span data-ttu-id="493e1-123">StrongNameKeyInstall メソッド</span><span class="sxs-lookup"><span data-stu-id="493e1-123">StrongNameKeyInstall Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md)
- [<span data-ttu-id="493e1-124">StrongNameKeyDelete メソッド</span><span class="sxs-lookup"><span data-stu-id="493e1-124">StrongNameKeyDelete Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeydelete-method.md)
- [<span data-ttu-id="493e1-125">ICLRStrongName インターフェイス</span><span class="sxs-lookup"><span data-stu-id="493e1-125">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
