---
title: IAssemblyName::GetProperty メソッド
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetProperty
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetProperty
helpviewer_keywords:
- IAssemblyName::GetProperty method [.NET Framework fusion]
- GetProperty method [.NET Framework fusion]
ms.assetid: e59fda62-77d5-4e37-89cb-ce7ae4627975
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5d131e9d8c7a1a2b4e4def75ecfb65bb8235a65e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54550670"
---
# <a name="iassemblynamegetproperty-method"></a><span data-ttu-id="f2cd5-102">IAssemblyName::GetProperty メソッド</span><span class="sxs-lookup"><span data-stu-id="f2cd5-102">IAssemblyName::GetProperty Method</span></span>
<span data-ttu-id="f2cd5-103">指定したプロパティの識別子によって参照されるプロパティにポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="f2cd5-103">Gets a pointer to the property referenced by the specified property identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2cd5-104">構文</span><span class="sxs-lookup"><span data-stu-id="f2cd5-104">Syntax</span></span>  
  
```  
HRESULT GetProperty (  
    [in]      DWORD    PropertyId,  
    [out]     LPVOID   pvProperty,  
    [in, out] LPDWORD  pcbProperty  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f2cd5-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f2cd5-105">Parameters</span></span>  
 `PropertyId`  
 <span data-ttu-id="f2cd5-106">[in]要求されたプロパティの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="f2cd5-106">[in] The unique identifier for the requested property.</span></span>  
  
 `pvProperty`  
 <span data-ttu-id="f2cd5-107">[out]返されたプロパティのデータ。</span><span class="sxs-lookup"><span data-stu-id="f2cd5-107">[out] The returned property data.</span></span>  
  
 `pcbProperty`  
 <span data-ttu-id="f2cd5-108">[入力、出力]サイズ (バイト単位) の`pvProperty`します。</span><span class="sxs-lookup"><span data-stu-id="f2cd5-108">[in, out] The size, in bytes, of `pvProperty`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2cd5-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="f2cd5-109">Requirements</span></span>  
 <span data-ttu-id="f2cd5-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2cd5-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2cd5-111">**ヘッダー:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="f2cd5-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="f2cd5-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2cd5-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2cd5-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2cd5-113">See also</span></span>
- [<span data-ttu-id="f2cd5-114">IAssemblyName インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f2cd5-114">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
