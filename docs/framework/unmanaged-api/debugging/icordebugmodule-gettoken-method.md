---
title: ICorDebugModule::GetToken メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetToken
helpviewer_keywords:
- ICorDebugModule::GetToken method [.NET Framework debugging]
- GetToken method, ICorDebugModule interface [.NET Framework debugging]
ms.assetid: f759f87a-18ae-4c1a-8300-29b803432d0a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4f87724bda78c1948ae7e1ddfa3d586fe5b7e14e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54575737"
---
# <a name="icordebugmodulegettoken-method"></a><span data-ttu-id="e1101-102">ICorDebugModule::GetToken メソッド</span><span class="sxs-lookup"><span data-stu-id="e1101-102">ICorDebugModule::GetToken Method</span></span>
<span data-ttu-id="e1101-103">このモジュールのテーブルのエントリのトークンを取得します。</span><span class="sxs-lookup"><span data-stu-id="e1101-103">Gets the token for the table entry for this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e1101-104">構文</span><span class="sxs-lookup"><span data-stu-id="e1101-104">Syntax</span></span>  
  
```  
HRESULT GetToken(  
    [out] mdModule *pToken  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e1101-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e1101-105">Parameters</span></span>  
 `pToken`  
 <span data-ttu-id="e1101-106">[out]ポインター、`mdModule`モジュールのメタデータを参照するトークン。</span><span class="sxs-lookup"><span data-stu-id="e1101-106">[out] A pointer to the `mdModule` token that references the module's metadata.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e1101-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="e1101-107">Remarks</span></span>  
 <span data-ttu-id="e1101-108">トークンを渡すことができます、 [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)、 [IMetaDataImport2](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)、および[IMetaDataAssemblyImport](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)メタデータ インポート インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="e1101-108">The token can be passed to the [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md), [IMetaDataImport2](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md), and [IMetaDataAssemblyImport](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) metadata import interfaces.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e1101-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="e1101-109">Requirements</span></span>  
 <span data-ttu-id="e1101-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1101-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e1101-111">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e1101-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e1101-112">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e1101-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e1101-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e1101-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1101-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1101-114">See also</span></span>
- [<span data-ttu-id="e1101-115">メタデータ</span><span class="sxs-lookup"><span data-stu-id="e1101-115">Metadata</span></span>](../../../../docs/framework/unmanaged-api/metadata/index.md)
