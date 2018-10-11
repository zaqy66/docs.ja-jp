---
title: IMetaDataEmit::ApplyEditAndContinue メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.ApplyEditAndContinue
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::ApplyEditAndContinue
helpviewer_keywords:
- ApplyEditAndContinue method [.NET Framework metadata]
- IMetaDataEmit::ApplyEditAndContinue method [.NET Framework metadata]
ms.assetid: 35991289-f389-495d-8caa-a6384fb1d557
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: faa9bc412e67e0e49ee969bd8b246a424fe628a0
ms.sourcegitcommit: 2eb5ca4956231c1a0efd34b6a9cab6153a5438af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2018
ms.locfileid: "49086271"
---
# <a name="imetadataemitapplyeditandcontinue-method"></a><span data-ttu-id="2f65a-102">IMetaDataEmit::ApplyEditAndContinue メソッド</span><span class="sxs-lookup"><span data-stu-id="2f65a-102">IMetaDataEmit::ApplyEditAndContinue Method</span></span>
<span data-ttu-id="2f65a-103">指定したメタデータで行われた変更では、現在のアセンブリのスコープを更新します。</span><span class="sxs-lookup"><span data-stu-id="2f65a-103">Updates the current assembly scope with the changes made in the specified metadata.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f65a-104">構文</span><span class="sxs-lookup"><span data-stu-id="2f65a-104">Syntax</span></span>  
  
```  
HRESULT ApplyEditAndContinue (   
    [in]  IUnknown    *pImport  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2f65a-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2f65a-105">Parameters</span></span>  
 `pImport`  
 <span data-ttu-id="2f65a-106">\[\]へのポインター、 [IUnknown](/cpp/atl/iunknown)ポータブル実行可能 (PE) ファイルからデルタ メタデータを表すオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="2f65a-106">\[in\] Pointer to an [IUnknown](/cpp/atl/iunknown) object that represents the delta metadata from the portable executable (PE) file.</span></span>
  
 <span data-ttu-id="2f65a-107">デルタのメタデータは、モジュールの実際のメタデータのコピーに加えられた変更を含むメタデータのブロックです。</span><span class="sxs-lookup"><span data-stu-id="2f65a-107">The delta metadata is the block of metadata that includes the changes that were made to the copy of the module's actual metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2f65a-108">要件</span><span class="sxs-lookup"><span data-stu-id="2f65a-108">Requirements</span></span>  
 <span data-ttu-id="2f65a-109">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f65a-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2f65a-110">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="2f65a-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="2f65a-111">**ライブラリ:** MSCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="2f65a-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2f65a-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2f65a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f65a-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f65a-113">See Also</span></span>  
 [<span data-ttu-id="2f65a-114">IMetaDataEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="2f65a-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="2f65a-115">IMetaDataEmit2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="2f65a-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
