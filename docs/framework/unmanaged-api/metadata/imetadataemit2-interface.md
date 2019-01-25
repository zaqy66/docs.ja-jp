---
title: IMetaDataEmit2 インターフェイス
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2
helpviewer_keywords:
- IMetaDataEmit2 interface [.NET Framework metadata]
ms.assetid: 866dc96b-bbfc-4c0f-80c2-38ce93072106
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a9e0477adb4958a53289cd0a64f39259403fa7dd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54656935"
---
# <a name="imetadataemit2-interface"></a><span data-ttu-id="9ede9-102">IMetaDataEmit2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9ede9-102">IMetaDataEmit2 Interface</span></span>
<span data-ttu-id="9ede9-103">拡張、 [IMetaDataEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)主に、ジェネリック型を扱う機能を提供するインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="9ede9-103">Extends the [IMetaDataEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interface primarily to provide the ability to work with generic types.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9ede9-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="9ede9-104">Methods</span></span>  
  
|<span data-ttu-id="9ede9-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="9ede9-105">Method</span></span>|<span data-ttu-id="9ede9-106">説明</span><span class="sxs-lookup"><span data-stu-id="9ede9-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9ede9-107">DefineGenericParam メソッド</span><span class="sxs-lookup"><span data-stu-id="9ede9-107">DefineGenericParam Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definegenericparam-method.md)|<span data-ttu-id="9ede9-108">ジェネリック型パラメーターの定義を作成し、そのジェネリック型パラメーターのトークンを取得します。</span><span class="sxs-lookup"><span data-stu-id="9ede9-108">Creates a definition for a generic type parameter, and gets a token to that generic type parameter.</span></span>|  
|[<span data-ttu-id="9ede9-109">DefineMethodSpec メソッド</span><span class="sxs-lookup"><span data-stu-id="9ede9-109">DefineMethodSpec Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definemethodspec-method.md)|<span data-ttu-id="9ede9-110">メソッドのジェネリック インスタンスを作成し、定義するためのトークンを取得します。</span><span class="sxs-lookup"><span data-stu-id="9ede9-110">Creates a generic instance of a method, and gets a token to the definition.</span></span>|  
|[<span data-ttu-id="9ede9-111">GetDeltaSaveSize メソッド</span><span class="sxs-lookup"><span data-stu-id="9ede9-111">GetDeltaSaveSize Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-getdeltasavesize-method.md)|<span data-ttu-id="9ede9-112">エディット コンティニュの現在のセッションの変更を表現するために必要なデータのサイズの違いを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="9ede9-112">Gets a value indicating the difference in size of the data that is required to express the changes for the current edit-and-continue session.</span></span>|  
|[<span data-ttu-id="9ede9-113">ResetENCLog メソッド</span><span class="sxs-lookup"><span data-stu-id="9ede9-113">ResetENCLog Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-resetenclog-method.md)|<span data-ttu-id="9ede9-114">エディット コンティニュは、ログをリセットし、新しいセッションを開始します。</span><span class="sxs-lookup"><span data-stu-id="9ede9-114">Resets the edit-and-continue log and starts a new session.</span></span>|  
|[<span data-ttu-id="9ede9-115">SaveDelta メソッド</span><span class="sxs-lookup"><span data-stu-id="9ede9-115">SaveDelta Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-savedelta-method.md)|<span data-ttu-id="9ede9-116">エディット コンティニュの現在のセッションから、指定したファイルの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="9ede9-116">Saves changes from the current edit-and-continue session to the specified file.</span></span>|  
|[<span data-ttu-id="9ede9-117">SaveDeltaToMemory メソッド</span><span class="sxs-lookup"><span data-stu-id="9ede9-117">SaveDeltaToMemory Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-savedeltatomemory-method.md)|<span data-ttu-id="9ede9-118">エディット コンティニュの現在のセッションからの変更をメモリに保存します。</span><span class="sxs-lookup"><span data-stu-id="9ede9-118">Saves changes from the current edit-and-continue session to memory.</span></span>|  
|[<span data-ttu-id="9ede9-119">SaveDeltaToStream メソッド</span><span class="sxs-lookup"><span data-stu-id="9ede9-119">SaveDeltaToStream Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-savedeltatostream-method.md)|<span data-ttu-id="9ede9-120">エディット コンティニュの現在のセッションからの変更を指定したストリームに保存します。</span><span class="sxs-lookup"><span data-stu-id="9ede9-120">Saves changes from the current edit-and-continue session to the specified stream.</span></span>|  
|[<span data-ttu-id="9ede9-121">SetGenericParamProps メソッド</span><span class="sxs-lookup"><span data-stu-id="9ede9-121">SetGenericParamProps Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-setgenericparamprops-method.md)|<span data-ttu-id="9ede9-122">指定したトークンによって参照されているジェネリック パラメーターの定義のプロパティ値を設定します。</span><span class="sxs-lookup"><span data-stu-id="9ede9-122">Sets property values for the generic parameter definition referenced by the specified token.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9ede9-123">必要条件</span><span class="sxs-lookup"><span data-stu-id="9ede9-123">Requirements</span></span>  
 <span data-ttu-id="9ede9-124">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ede9-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ede9-125">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="9ede9-125">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9ede9-126">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="9ede9-126">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9ede9-127">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ede9-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ede9-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ede9-128">See also</span></span>
- [<span data-ttu-id="9ede9-129">メタデータ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9ede9-129">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [<span data-ttu-id="9ede9-130">IMetaDataEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9ede9-130">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
