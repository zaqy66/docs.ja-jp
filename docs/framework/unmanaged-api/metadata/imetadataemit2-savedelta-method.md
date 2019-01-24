---
title: IMetaDataEmit2::SaveDelta メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SaveDelta
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SaveDelta
helpviewer_keywords:
- IMetaDataEmit2::SaveDelta method [.NET Framework metadata]
- SaveDelta method [.NET Framework metadata]
ms.assetid: b95739fe-d2fa-4776-ae0d-31d9707ef799
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 27d9b891475d0fb45c9ec34f3363b0d76fe394c4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54493205"
---
# <a name="imetadataemit2savedelta-method"></a><span data-ttu-id="9f4c7-102">IMetaDataEmit2::SaveDelta メソッド</span><span class="sxs-lookup"><span data-stu-id="9f4c7-102">IMetaDataEmit2::SaveDelta Method</span></span>
<span data-ttu-id="9f4c7-103">エディット コンティニュの現在のセッションから、指定したファイルの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="9f4c7-103">Saves changes from the current edit-and-continue session to the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f4c7-104">構文</span><span class="sxs-lookup"><span data-stu-id="9f4c7-104">Syntax</span></span>  
  
```  
HRESULT SaveDelta (  
    [in] LPCWSTR     szFile,   
    [in] DWORD       dwSaveFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9f4c7-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9f4c7-105">Parameters</span></span>  
 `szFile`  
 <span data-ttu-id="9f4c7-106">[in]変更を保存するファイル名。</span><span class="sxs-lookup"><span data-stu-id="9f4c7-106">[in] The file name under which to save changes.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="9f4c7-107">[in] 予約されています。</span><span class="sxs-lookup"><span data-stu-id="9f4c7-107">[in] Reserved.</span></span> <span data-ttu-id="9f4c7-108">ゼロを指定してください。</span><span class="sxs-lookup"><span data-stu-id="9f4c7-108">Must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f4c7-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="9f4c7-109">Requirements</span></span>  
 <span data-ttu-id="9f4c7-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f4c7-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9f4c7-111">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="9f4c7-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9f4c7-112">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="9f4c7-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9f4c7-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9f4c7-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f4c7-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="9f4c7-114">See also</span></span>
- [<span data-ttu-id="9f4c7-115">IMetaDataEmit2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9f4c7-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
- [<span data-ttu-id="9f4c7-116">IMetaDataEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9f4c7-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
