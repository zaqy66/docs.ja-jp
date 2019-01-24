---
title: IMetaDataImport::GetNameFromToken メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetNameFromToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetNameFromToken
helpviewer_keywords:
- GetNameFromToken method [.NET Framework metadata]
- IMetaDataImport::GetNameFromToken method [.NET Framework metadata]
ms.assetid: 32114ecf-8916-4ab2-a201-179c017344f1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 36218fa44f1cb49d8d0193d7c72e6feb2d121050
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54718846"
---
# <a name="imetadataimportgetnamefromtoken-method"></a><span data-ttu-id="b0765-102">IMetaDataImport::GetNameFromToken メソッド</span><span class="sxs-lookup"><span data-stu-id="b0765-102">IMetaDataImport::GetNameFromToken Method</span></span>
<span data-ttu-id="b0765-103">指定したメタデータ トークンによって参照されるオブジェクトの UTF-8 名を取得します。</span><span class="sxs-lookup"><span data-stu-id="b0765-103">Gets the UTF-8 name of the object referenced by the specified metadata token.</span></span> <span data-ttu-id="b0765-104">このメソッドは、互換性のために残されています。</span><span class="sxs-lookup"><span data-stu-id="b0765-104">This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0765-105">構文</span><span class="sxs-lookup"><span data-stu-id="b0765-105">Syntax</span></span>  
  
```  
HRESULT GetNameFromToken (  
   [in] mdToken      tk,  
   [out] MDUTF8CSTR  *pszUtf8NamePtr  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b0765-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0765-106">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="b0765-107">[in]名前を取得するオブジェクトを表すトークンです。</span><span class="sxs-lookup"><span data-stu-id="b0765-107">[in] The token representing the object to return the name for.</span></span>  
  
 `pszUtf8NamePtr`  
 <span data-ttu-id="b0765-108">[out]ヒープで utf-8 オブジェクト名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b0765-108">[out] A pointer to the UTF-8 object name in the heap.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b0765-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="b0765-109">Remarks</span></span>  
 <span data-ttu-id="b0765-110">`GetNameFromToken` は互換性のために残されています。</span><span class="sxs-lookup"><span data-stu-id="b0765-110">`GetNameFromToken` is obsolete.</span></span> <span data-ttu-id="b0765-111">代わりに、トークンを必要に応じてなどの特定の型のプロパティを取得するメソッドを呼び出す`GetFieldProps`フィールドまたは`GetMethodProps`メソッド。</span><span class="sxs-lookup"><span data-stu-id="b0765-111">As an alternative, call a method to get the properties of the particular type of token required, such as `GetFieldProps` for a field or `GetMethodProps` for a method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b0765-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="b0765-112">Requirements</span></span>  
 <span data-ttu-id="b0765-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0765-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b0765-114">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b0765-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b0765-115">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="b0765-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b0765-116">**.NET framework のバージョン:** 1</span><span class="sxs-lookup"><span data-stu-id="b0765-116">**.NET Framework Versions:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0765-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0765-117">See also</span></span>
- [<span data-ttu-id="b0765-118">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b0765-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="b0765-119">IMetaDataImport2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b0765-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
