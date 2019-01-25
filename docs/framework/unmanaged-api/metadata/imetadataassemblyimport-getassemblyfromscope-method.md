---
title: IMetaDataAssemblyImport::GetAssemblyFromScope メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetAssemblyFromScope
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetAssemblyFromScope
helpviewer_keywords:
- IMetaDataAssemblyImport::GetAssemblyFromScope method [.NET Framework metadata]
- GetAssemblyFromScope method [.NET Framework metadata]
ms.assetid: 0b437f70-561d-48c7-abe0-0cb9ace10c08
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7914257d167d0f54d3625d252076576e5e40296b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54634948"
---
# <a name="imetadataassemblyimportgetassemblyfromscope-method"></a><span data-ttu-id="32108-102">IMetaDataAssemblyImport::GetAssemblyFromScope メソッド</span><span class="sxs-lookup"><span data-stu-id="32108-102">IMetaDataAssemblyImport::GetAssemblyFromScope Method</span></span>
<span data-ttu-id="32108-103">現在のスコープ内でアセンブリへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="32108-103">Gets a pointer to the assembly in the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="32108-104">構文</span><span class="sxs-lookup"><span data-stu-id="32108-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyFromScope (  
    [out] mdAssembly  *ptkAssembly  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="32108-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="32108-105">Parameters</span></span>  
 `ptkAssembly`  
 <span data-ttu-id="32108-106">[out]取得してへのポインター`mdAssembly`アセンブリを識別するトークン。</span><span class="sxs-lookup"><span data-stu-id="32108-106">[out] A pointer to the retrieved `mdAssembly` token that identifies the assembly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="32108-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="32108-107">Requirements</span></span>  
 <span data-ttu-id="32108-108">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="32108-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="32108-109">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="32108-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="32108-110">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="32108-110">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="32108-111">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="32108-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="32108-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="32108-112">See also</span></span>
- [<span data-ttu-id="32108-113">IMetaDataAssemblyImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="32108-113">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
