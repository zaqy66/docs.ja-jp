---
title: IMetaDataImport::EnumEvents メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumEvents
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumEvents
helpviewer_keywords:
- IMetaDataImport::EnumEvents method [.NET Framework metadata]
- EnumEvents method [.NET Framework metadata]
ms.assetid: e1efedcb-3dd7-42ae-a399-21c24728aec5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f205615db29878bcfe936e88cab26c3d5a8e3562
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54514527"
---
# <a name="imetadataimportenumevents-method"></a><span data-ttu-id="68733-102">IMetaDataImport::EnumEvents メソッド</span><span class="sxs-lookup"><span data-stu-id="68733-102">IMetaDataImport::EnumEvents Method</span></span>
<span data-ttu-id="68733-103">指定した TypeDef トークンのイベント定義トークンを列挙します。</span><span class="sxs-lookup"><span data-stu-id="68733-103">Enumerates event definition tokens for the specified TypeDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="68733-104">構文</span><span class="sxs-lookup"><span data-stu-id="68733-104">Syntax</span></span>  
  
```  
HRESULT EnumEvents (   
   [in, out] HCORENUM    *phEnum,   
   [in]      mdTypeDef   td,   
   [out]     mdEvent     rEvents[],   
   [in]      ULONG       cMax,  
   [out]    ULONG        *pcEvents  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="68733-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68733-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="68733-106">[入力、出力]列挙子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="68733-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `td`  
 <span data-ttu-id="68733-107">[in]イベント定義を持つが列挙 TypeDef トークンです。</span><span class="sxs-lookup"><span data-stu-id="68733-107">[in] The TypeDef token whose event definitions are to be enumerated.</span></span>  
  
 `rEvents`  
 <span data-ttu-id="68733-108">[out]返されるイベントの配列。</span><span class="sxs-lookup"><span data-stu-id="68733-108">[out] The array of returned events.</span></span>  
  
 `cMax`  
 <span data-ttu-id="68733-109">[in] `rEvents` 配列の最大サイズ。</span><span class="sxs-lookup"><span data-stu-id="68733-109">[in] The maximum size of the `rEvents` array.</span></span>  
  
 `pcEvents`  
 <span data-ttu-id="68733-110">[out]実際に返されるイベントの数`rEvents`します。</span><span class="sxs-lookup"><span data-stu-id="68733-110">[out] The actual number of events returned in `rEvents`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="68733-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="68733-111">Return Value</span></span>  
  
|<span data-ttu-id="68733-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="68733-112">HRESULT</span></span>|<span data-ttu-id="68733-113">説明</span><span class="sxs-lookup"><span data-stu-id="68733-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="68733-114">`EnumEvents` 正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="68733-114">`EnumEvents` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="68733-115">列挙するためにイベントはありません。</span><span class="sxs-lookup"><span data-stu-id="68733-115">There are no events to enumerate.</span></span> <span data-ttu-id="68733-116">その場合は、`pcEvents`は 0 です。</span><span class="sxs-lookup"><span data-stu-id="68733-116">In that case, `pcEvents` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="68733-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="68733-117">Requirements</span></span>  
 <span data-ttu-id="68733-118">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="68733-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="68733-119">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="68733-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="68733-120">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="68733-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="68733-121">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="68733-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68733-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="68733-122">See also</span></span>
- [<span data-ttu-id="68733-123">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="68733-123">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="68733-124">IMetaDataImport2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="68733-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
