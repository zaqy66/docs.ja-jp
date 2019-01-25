---
title: IMetaDataImport::CountEnum メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataImport.CountEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::CountEnum
helpviewer_keywords:
- CountEnum method [.NET Framework metadata]
- IMetaDataImport::CountEnum method [.NET Framework metadata]
ms.assetid: d1de53ad-9435-4b5f-9df7-07f21210e5b5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4b48ff81fad397adcd5b2d0caae961484bfea5e2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706392"
---
# <a name="imetadataimportcountenum-method"></a><span data-ttu-id="6db58-102">IMetaDataImport::CountEnum メソッド</span><span class="sxs-lookup"><span data-stu-id="6db58-102">IMetaDataImport::CountEnum Method</span></span>
<span data-ttu-id="6db58-103">指定された列挙子によって取得された列挙体の要素の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="6db58-103">Gets the number of elements in the enumeration that was retrieved by the specified enumerator.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6db58-104">構文</span><span class="sxs-lookup"><span data-stu-id="6db58-104">Syntax</span></span>  
  
```  
HRESULT CountEnum (  
   [in]  HCORENUM    hEnum,   
   [out] ULONG       *pulCount  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6db58-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6db58-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="6db58-106">[in]列挙子のハンドル。</span><span class="sxs-lookup"><span data-stu-id="6db58-106">[in] The handle for the enumerator.</span></span>  
  
 `pulCount`  
 <span data-ttu-id="6db58-107">[out]列挙された要素の数。</span><span class="sxs-lookup"><span data-stu-id="6db58-107">[out] The number of elements enumerated.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6db58-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="6db58-108">Remarks</span></span>  
 <span data-ttu-id="6db58-109">指定されたハンドル`hEnum`以前から取得されます`Enum`*名前*呼び出し (たとえば、 [imetadataimport::enumtypedefs](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumtypedefs-method.md))。</span><span class="sxs-lookup"><span data-stu-id="6db58-109">The handle specified by `hEnum` is obtained from a previous `Enum`*Name* call (for example, [IMetaDataImport::EnumTypeDefs](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumtypedefs-method.md)).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6db58-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="6db58-110">Requirements</span></span>  
 <span data-ttu-id="6db58-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6db58-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6db58-112">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="6db58-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6db58-113">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="6db58-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6db58-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6db58-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6db58-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="6db58-115">See also</span></span>
- [<span data-ttu-id="6db58-116">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6db58-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="6db58-117">IMetaDataImport2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6db58-117">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
