---
title: IMetaDataImport::CloseEnum メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataImport.CloseEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::CloseEnum
helpviewer_keywords:
- IMetaDataImport::CloseEnum method [.NET Framework metadata]
- CloseEnum method, IMetaDataImport interface [.NET Framework metadata]
ms.assetid: 727819d5-1dab-4ebb-ac25-950b4111dc72
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 724660cd5703ee9b893493df5d583d97b5bdfb3e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720523"
---
# <a name="imetadataimportcloseenum-method"></a><span data-ttu-id="49e87-102">IMetaDataImport::CloseEnum メソッド</span><span class="sxs-lookup"><span data-stu-id="49e87-102">IMetaDataImport::CloseEnum Method</span></span>
<span data-ttu-id="49e87-103">指定したハンドルによって識別される列挙子を閉じます。</span><span class="sxs-lookup"><span data-stu-id="49e87-103">Closes the enumerator that is identified by the specified handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49e87-104">構文</span><span class="sxs-lookup"><span data-stu-id="49e87-104">Syntax</span></span>  
  
```  
void CloseEnum (  
   [in] HCORENUM hEnum  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="49e87-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49e87-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="49e87-106">[in]閉じる、列挙子のハンドル。</span><span class="sxs-lookup"><span data-stu-id="49e87-106">[in] The handle for the enumerator to close.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="49e87-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="49e87-107">Remarks</span></span>  
 <span data-ttu-id="49e87-108">指定されたハンドル`hEnum`以前から取得されます`Enum`*名前*呼び出し (たとえば、 [imetadataimport::enumtypedefs](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumtypedefs-method.md))。</span><span class="sxs-lookup"><span data-stu-id="49e87-108">The handle specified by `hEnum` is obtained from a previous `Enum`*Name* call (for example, [IMetaDataImport::EnumTypeDefs](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumtypedefs-method.md)).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="49e87-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="49e87-109">Requirements</span></span>  
 <span data-ttu-id="49e87-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="49e87-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="49e87-111">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="49e87-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="49e87-112">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="49e87-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="49e87-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="49e87-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49e87-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="49e87-114">See also</span></span>
- [<span data-ttu-id="49e87-115">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="49e87-115">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="49e87-116">IMetaDataImport2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="49e87-116">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
