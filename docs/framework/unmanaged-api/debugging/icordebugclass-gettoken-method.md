---
title: ICorDebugClass::GetToken メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugClass.GetToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass::GetToken
helpviewer_keywords:
- GetToken method, ICorDebugClass interface [.NET Framework debugging]
- ICorDebugClass::GetToken method [.NET Framework debugging]
ms.assetid: ee5c848a-eac4-4462-b07a-07ccd76a75df
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d6dc245a53c9ec7cbe56e20313abc4269e33f45c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54582319"
---
# <a name="icordebugclassgettoken-method"></a><span data-ttu-id="9cea6-102">ICorDebugClass::GetToken メソッド</span><span class="sxs-lookup"><span data-stu-id="9cea6-102">ICorDebugClass::GetToken Method</span></span>
<span data-ttu-id="9cea6-103">取得、`TypeDef`このクラスの定義を参照するメタデータ トークン。</span><span class="sxs-lookup"><span data-stu-id="9cea6-103">Gets the `TypeDef` metadata token that references the definition of this class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9cea6-104">構文</span><span class="sxs-lookup"><span data-stu-id="9cea6-104">Syntax</span></span>  
  
```  
HRESULT GetToken (  
    [out] mdTypeDef          *pTypeDef  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9cea6-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9cea6-105">Parameters</span></span>  
 `pTypeDef`  
 <span data-ttu-id="9cea6-106">[out]ポインター、`mdTypeDef`このクラスの定義を参照するトークン。</span><span class="sxs-lookup"><span data-stu-id="9cea6-106">[out] A pointer to an `mdTypeDef` token that references the definition of this class.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9cea6-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="9cea6-107">Requirements</span></span>  
 <span data-ttu-id="9cea6-108">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9cea6-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9cea6-109">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9cea6-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9cea6-110">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9cea6-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9cea6-111">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9cea6-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9cea6-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="9cea6-112">See also</span></span>
- [<span data-ttu-id="9cea6-113">メタデータ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9cea6-113">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
