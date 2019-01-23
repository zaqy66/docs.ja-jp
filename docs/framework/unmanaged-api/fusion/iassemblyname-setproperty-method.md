---
title: IAssemblyName::SetProperty メソッド
ms.date: 03/30/2017
api_name:
- IAssemblyName.SetProperty
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::SetProperty
helpviewer_keywords:
- IAssemblyName::SetProperty method [.NET Framework fusion]
- SetProperty method [.NET Framework fusion]
ms.assetid: 496c3add-f60b-4073-943f-d1bcf33330cb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ca2d7fe73fc749296f76e18ecce75b7fdd0795d3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585592"
---
# <a name="iassemblynamesetproperty-method"></a><span data-ttu-id="a548f-102">IAssemblyName::SetProperty メソッド</span><span class="sxs-lookup"><span data-stu-id="a548f-102">IAssemblyName::SetProperty Method</span></span>
<span data-ttu-id="a548f-103">指定したプロパティの識別子によって参照されるプロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a548f-103">Sets the value of the property referenced by the specified property identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a548f-104">構文</span><span class="sxs-lookup"><span data-stu-id="a548f-104">Syntax</span></span>  
  
```  
HRESULT SetProperty (  
    [in] DWORD  PropertyId,  
    [in] LPVOID pvProperty,  
    [in] DWORD  cbProperty  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a548f-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a548f-105">Parameters</span></span>  
 `PropertyId`  
 <span data-ttu-id="a548f-106">[in]値が設定されるプロパティの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="a548f-106">[in] The unique identifier of the property whose value will be set.</span></span>  
  
 `pvProperty`  
 <span data-ttu-id="a548f-107">[in]によって参照されるプロパティを設定する値`PropertyId`します。</span><span class="sxs-lookup"><span data-stu-id="a548f-107">[in] The value to which to set the property referenced by `PropertyId`.</span></span>  
  
 `cbProperty`  
 <span data-ttu-id="a548f-108">[in]サイズ (バイト単位) の`pvProperty`します。</span><span class="sxs-lookup"><span data-stu-id="a548f-108">[in] The size, in bytes, of `pvProperty`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a548f-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="a548f-109">Requirements</span></span>  
 <span data-ttu-id="a548f-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a548f-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a548f-111">**ヘッダー:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="a548f-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="a548f-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a548f-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a548f-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="a548f-113">See also</span></span>
- [<span data-ttu-id="a548f-114">IAssemblyName インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a548f-114">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
