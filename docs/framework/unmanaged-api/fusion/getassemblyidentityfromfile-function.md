---
title: GetAssemblyIdentityFromFile 関数
ms.date: 03/30/2017
api_name:
- GetAssemblyIdentityFromFile
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- COM
f1_keywords:
- GetAssemblyIdentityFromFile
helpviewer_keywords:
- GetAssemblyIdentityFromFile function [.NET Framework fusion]
ms.assetid: 2c32da53-76c7-4048-84d0-d05207333004
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: feb8e5c56ee6ea766cd5f1d10af42699777db453
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654890"
---
# <a name="getassemblyidentityfromfile-function"></a><span data-ttu-id="f3d09-102">GetAssemblyIdentityFromFile 関数</span><span class="sxs-lookup"><span data-stu-id="f3d09-102">GetAssemblyIdentityFromFile Function</span></span>
<span data-ttu-id="f3d09-103">ポインターを取得、 `IUnknown` 、指定したオブジェクト`IID`のアセンブリにある指定したファイル パス。</span><span class="sxs-lookup"><span data-stu-id="f3d09-103">Gets a pointer to an `IUnknown` object with the specified `IID` in the assembly at the specified file path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3d09-104">構文</span><span class="sxs-lookup"><span data-stu-id="f3d09-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyIdentityFromFile (  
    [in]  LPCWSTR   pwzFilePath,  
    [in]  REFIID    riid,  
    [out] IUnknown  **ppIdentity  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f3d09-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f3d09-105">Parameters</span></span>  
 `pwzFilePath`  
 <span data-ttu-id="f3d09-106">[in]要求されたアセンブリへの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="f3d09-106">[in] A valid path to the requested assembly.</span></span>  
  
 `riid`  
 <span data-ttu-id="f3d09-107">[in]`IID`返すインターフェイスの。</span><span class="sxs-lookup"><span data-stu-id="f3d09-107">[in] The `IID` of the interface to return.</span></span>  
  
 `ppIdentity`  
 <span data-ttu-id="f3d09-108">[out]返されるインターフェイス ポインター。</span><span class="sxs-lookup"><span data-stu-id="f3d09-108">[out] The returned interface pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f3d09-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="f3d09-109">Requirements</span></span>  
 <span data-ttu-id="f3d09-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3d09-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f3d09-111">**ヘッダー:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="f3d09-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="f3d09-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f3d09-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3d09-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3d09-113">See also</span></span>
- [<span data-ttu-id="f3d09-114">IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3d09-114">IUnknown</span></span>](/cpp/atl/iunknown)
- [<span data-ttu-id="f3d09-115">Fusion グローバル静的関数</span><span class="sxs-lookup"><span data-stu-id="f3d09-115">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
