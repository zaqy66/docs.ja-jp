---
title: IMetaDataImport::EnumMembers メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMembers
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMembers
helpviewer_keywords:
- IMetaDataImport::EnumMembers method [.NET Framework metadata]
- EnumMembers method [.NET Framework metadata]
ms.assetid: 3fb8e178-342b-4c89-9bcf-f7f834e6cb77
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 88b8f874400d68110fa5e8fb66ca910b8e7231e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54645965"
---
# <a name="imetadataimportenummembers-method"></a><span data-ttu-id="ebdbb-102">IMetaDataImport::EnumMembers メソッド</span><span class="sxs-lookup"><span data-stu-id="ebdbb-102">IMetaDataImport::EnumMembers Method</span></span>
<span data-ttu-id="ebdbb-103">指定した型のメンバーを表す MemberDef トークンを列挙します。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-103">Enumerates MemberDef tokens representing members of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ebdbb-104">構文</span><span class="sxs-lookup"><span data-stu-id="ebdbb-104">Syntax</span></span>  
  
```  
HRESULT EnumMembers (   
   [in, out]  HCORENUM    *phEnum,   
   [in]  mdTypeDef   cl,   
   [out] mdToken     rMembers[],   
   [in]  ULONG       cMax,   
   [out] ULONG       *pcTokens  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ebdbb-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ebdbb-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="ebdbb-106">[入力、出力]列挙子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `cl`  
 <span data-ttu-id="ebdbb-107">[in]そのメンバーが列挙型を表す TypeDef トークンです。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-107">[in] A TypeDef token representing the type whose members are to be enumerated.</span></span>  
  
 `rMembers`  
 <span data-ttu-id="ebdbb-108">[out]MemberDef トークンを保持するために使用する配列。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-108">[out] The array used to hold the MemberDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="ebdbb-109">[in] `rMembers` 配列の最大サイズ。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-109">[in] The maximum size of the `rMembers` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="ebdbb-110">[out]実際に返される MemberDef トークン数`rMembers`します。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-110">[out] The actual number of MemberDef tokens returned in `rMembers`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ebdbb-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="ebdbb-111">Return Value</span></span>  
  
|<span data-ttu-id="ebdbb-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ebdbb-112">HRESULT</span></span>|<span data-ttu-id="ebdbb-113">説明</span><span class="sxs-lookup"><span data-stu-id="ebdbb-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="ebdbb-114">`EnumMembers` 正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-114">`EnumMembers` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="ebdbb-115">MemberDef トークンを列挙することはありません。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-115">There are no MemberDef tokens to enumerate.</span></span> <span data-ttu-id="ebdbb-116">その場合は、`pcTokens`は 0 です。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-116">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ebdbb-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="ebdbb-117">Remarks</span></span>  
 <span data-ttu-id="ebdbb-118">クラスのメンバーのコレクションを列挙する場合、`EnumMembers`クラスで直接定義されているメンバーのみを返します。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-118">When enumerating collections of members for a class, `EnumMembers` returns only members defined directly on the class.</span></span> <span data-ttu-id="ebdbb-119">クラスは、継承されたメンバーの実装を提供する場合でも、クラスが継承する任意のメンバーは返されません。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-119">It does not return any members that the class inherits, even if the class provides an implementation for those inherited members.</span></span> <span data-ttu-id="ebdbb-120">継承されたメンバーを列挙するために、呼び出し元は明示的に継承チェーンを走査する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-120">To enumerate inherited members, the caller must explicitly walk the inheritance chain.</span></span> <span data-ttu-id="ebdbb-121">継承チェーンの規則は、言語や、元のメタデータを生成するコンパイラによって異なる場合がありますに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-121">Note that the rules for the inheritance chain may vary depending on the language or compiler that emitted the original metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ebdbb-122">必要条件</span><span class="sxs-lookup"><span data-stu-id="ebdbb-122">Requirements</span></span>  
 <span data-ttu-id="ebdbb-123">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebdbb-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ebdbb-124">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ebdbb-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ebdbb-125">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="ebdbb-125">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ebdbb-126">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ebdbb-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebdbb-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebdbb-127">See also</span></span>
- [<span data-ttu-id="ebdbb-128">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ebdbb-128">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="ebdbb-129">IMetaDataImport2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ebdbb-129">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
