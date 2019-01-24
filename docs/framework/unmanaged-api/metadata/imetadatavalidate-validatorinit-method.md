---
title: IMetaDataValidate::ValidatorInit メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataValidate.ValidatorInit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataValidate::ValidatorInit
helpviewer_keywords:
- IMetaDataValidate::ValidatorInit method [.NET Framework metadata]
- ValidatorInit method [.NET Framework metadata]
ms.assetid: 6bafd75a-e2d0-4aea-aed1-074374d5dff6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: eb5f0514cad852367365b9c8b24ef006e275f749
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54696452"
---
# <a name="imetadatavalidatevalidatorinit-method"></a><span data-ttu-id="9c0da-102">IMetaDataValidate::ValidatorInit メソッド</span><span class="sxs-lookup"><span data-stu-id="9c0da-102">IMetaDataValidate::ValidatorInit Method</span></span>
<span data-ttu-id="9c0da-103">現在のメタデータ スコープ内にあるモジュールの種類を指定するフラグを設定し、指定されたコールバック メソッドを検証エラー用に登録します。</span><span class="sxs-lookup"><span data-stu-id="9c0da-103">Sets a flag that specifies the type of the module in the current metadata scope, and registers the specified callback method for validation errors.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c0da-104">構文</span><span class="sxs-lookup"><span data-stu-id="9c0da-104">Syntax</span></span>  
  
```  
HRESULT ValidatorInit (  
   [in] DWORD       dwModuleType,  
   [in] IUnknown    *pUnk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9c0da-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9c0da-105">Parameters</span></span>  
 `dwModule`  
 <span data-ttu-id="9c0da-106">[in]値、 [CorValidatorModuleType](../../../../docs/framework/unmanaged-api/metadata/corvalidatormoduletype-enumeration.md)の現在のメタデータ スコープ内のモジュールの種類を指定する列挙体。</span><span class="sxs-lookup"><span data-stu-id="9c0da-106">[in] A value of the [CorValidatorModuleType](../../../../docs/framework/unmanaged-api/metadata/corvalidatormoduletype-enumeration.md) enumeration that specifies the type of the module in the current metadata scope.</span></span>  
  
 `pUnk`  
 <span data-ttu-id="9c0da-107">[in]ポインター、 [IUnknown](/cpp/atl/iunknown)検証エラーのコールバックで関数として機能するインスタンス。</span><span class="sxs-lookup"><span data-stu-id="9c0da-107">[in] A pointer to an [IUnknown](/cpp/atl/iunknown) instance that serves as a function callback for validation errors.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9c0da-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="9c0da-108">Requirements</span></span>  
 <span data-ttu-id="9c0da-109">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c0da-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9c0da-110">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="9c0da-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9c0da-111">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="9c0da-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9c0da-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9c0da-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c0da-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c0da-113">See also</span></span>
- [<span data-ttu-id="9c0da-114">IMetaDataValidate インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9c0da-114">IMetaDataValidate Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatavalidate-interface.md)
