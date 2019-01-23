---
title: IMetaDataEmit::DefineSecurityAttributeSet メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineSecurityAttributeSet
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineSecurityAttributeSet
helpviewer_keywords:
- IMetaDataEmit::DefineSecurityAttributeSet method [.NET Framework metadata]
- DefineSecurityAttributeSet method [.NET Framework metadata]
ms.assetid: 27064ca2-4186-4433-90a7-3b297785e891
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 483f59ee3e81861ec1b05a0fee9c5db797aab68f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491151"
---
# <a name="imetadataemitdefinesecurityattributeset-method"></a><span data-ttu-id="e861c-102">IMetaDataEmit::DefineSecurityAttributeSet メソッド</span><span class="sxs-lookup"><span data-stu-id="e861c-102">IMetaDataEmit::DefineSecurityAttributeSet Method</span></span>
<span data-ttu-id="e861c-103">指定したトークンによって参照されるオブジェクトにアタッチするセキュリティ権限のセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="e861c-103">Creates a set of security permissions to attach to the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e861c-104">構文</span><span class="sxs-lookup"><span data-stu-id="e861c-104">Syntax</span></span>  
  
```  
HRESULT DefineSecurityAttributeSet (   
    [in]  mdToken       tkObj,   
    [in]  COR_SECATTR   rSecAttrs[],   
    [in]  ULONG         cSecAttrs,   
    [out] ULONG         *pulErrorAttr   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e861c-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e861c-105">Parameters</span></span>  
 `tkObj`  
 <span data-ttu-id="e861c-106">[in]セキュリティ情報が接続されているトークンです。</span><span class="sxs-lookup"><span data-stu-id="e861c-106">[in] The token to which the security information is attached.</span></span>  
  
 `rSecAttrs`  
 <span data-ttu-id="e861c-107">[in]配列の`COR_SECATTR`構造体。</span><span class="sxs-lookup"><span data-stu-id="e861c-107">[in] An array of `COR_SECATTR` structures.</span></span>  
  
 `cSecAttrs`  
 <span data-ttu-id="e861c-108">[in]要素数`rSecAttrs`します。</span><span class="sxs-lookup"><span data-stu-id="e861c-108">[in] The number of elements in `rSecAttrs`.</span></span>  
  
 `pulErrorAttr`  
 <span data-ttu-id="e861c-109">[out]メソッドが失敗した場合にインデックスを指定します。`rSecAttrs`の問題の原因となった要素。</span><span class="sxs-lookup"><span data-stu-id="e861c-109">[out] If the method fails, specifies the index in `rSecAttrs` of the element that caused the problem.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e861c-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="e861c-110">Requirements</span></span>  
 <span data-ttu-id="e861c-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e861c-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e861c-112">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e861c-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e861c-113">**ライブラリ:** MSCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="e861c-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e861c-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e861c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e861c-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="e861c-115">See also</span></span>
- [<span data-ttu-id="e861c-116">IMetaDataEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e861c-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="e861c-117">IMetaDataEmit2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e861c-117">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
