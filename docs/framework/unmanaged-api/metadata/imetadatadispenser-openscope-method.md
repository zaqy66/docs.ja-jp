---
title: IMetaDataDispenser::OpenScope メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataDispenser.OpenScope
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenser::OpenScope
helpviewer_keywords:
- IMetaDataDispenser::OpenScope method [.NET Framework metadata]
- OpenScope method, IMetaDataDispenser interface [.NET Framework metadata]
ms.assetid: 65063ad5-e0d9-4c01-8f8b-9a5950109fa6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 905de2745be085391bef8ea32b8f82a5da78f3a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54681197"
---
# <a name="imetadatadispenseropenscope-method"></a><span data-ttu-id="79256-102">IMetaDataDispenser::OpenScope メソッド</span><span class="sxs-lookup"><span data-stu-id="79256-102">IMetaDataDispenser::OpenScope Method</span></span>
<span data-ttu-id="79256-103">既存のディスク上ファイルを開き、そのメタデータをメモリにマップされます。</span><span class="sxs-lookup"><span data-stu-id="79256-103">Opens an existing, on-disk file and maps its metadata into memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79256-104">構文</span><span class="sxs-lookup"><span data-stu-id="79256-104">Syntax</span></span>  
  
```  
HRESULT OpenScope (  
    [in]  LPCWSTR     szScope,   
    [in]  DWORD       dwOpenFlags,   
    [in]  REFIID      riid,   
    [out] IUnknown    **ppIUnk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="79256-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="79256-105">Parameters</span></span>  
 `szScope`  
 <span data-ttu-id="79256-106">[in]開かれるファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="79256-106">[in] The name of the file to be opened.</span></span> <span data-ttu-id="79256-107">ファイルには、共通言語ランタイム (CLR) メタデータを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="79256-107">The file must contain common language runtime (CLR) metadata.</span></span>  
  
 `dwOpenFlags`  
 <span data-ttu-id="79256-108">[in]値、 [CorOpenFlags](../../../../docs/framework/unmanaged-api/metadata/coropenflags-enumeration.md)開くのためのモード (読み取り、書き込み、およびなど) を指定する列挙体。</span><span class="sxs-lookup"><span data-stu-id="79256-108">[in] A value of the [CorOpenFlags](../../../../docs/framework/unmanaged-api/metadata/coropenflags-enumeration.md) enumeration to specify the mode (read, write, and so on) for opening.</span></span>  
  
 `riid`  
 <span data-ttu-id="79256-109">[in]返される必要なメタデータ インターフェイスの IID呼び出し元は (読み取り) をインポートまたは (書き込み) メタデータを生成するインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="79256-109">[in] The IID of the desired metadata interface to be returned; the caller will use the interface to import (read) or emit (write) metadata.</span></span>  
  
 <span data-ttu-id="79256-110">値`riid`"import"や「生成」インターフェイスのいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79256-110">The value of `riid` must specify one of the "import" or "emit" interfaces.</span></span> <span data-ttu-id="79256-111">有効な値は、IID_IMetaDataEmit、IID_IMetaDataImport、IID_IMetaDataAssemblyEmit、IID_IMetaDataAssemblyImport、IID_IMetaDataEmit2、または IID_IMetaDataImport2 は。</span><span class="sxs-lookup"><span data-stu-id="79256-111">Valid values are IID_IMetaDataEmit, IID_IMetaDataImport, IID_IMetaDataAssemblyEmit, IID_IMetaDataAssemblyImport, IID_IMetaDataEmit2, or IID_IMetaDataImport2.</span></span>  
  
 `ppIUnk`  
 <span data-ttu-id="79256-112">[out]返されたインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="79256-112">[out] The pointer to the returned interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="79256-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="79256-113">Remarks</span></span>  
 <span data-ttu-id="79256-114">メソッドを使用して、"import"インターフェイスのいずれかからまたは「生成」インターフェイスのいずれかからメソッドを使用する追加メタデータのメモリ内コピーを照会できます。</span><span class="sxs-lookup"><span data-stu-id="79256-114">The in-memory copy of the metadata can be queried using methods from one of the "import" interfaces, or added to using methods from the one of the "emit" interfaces.</span></span>  
  
 <span data-ttu-id="79256-115">ターゲット ファイルには、CLR メタデータが含まれていない場合、`OpenScope`メソッドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="79256-115">If the target file does not contain CLR metadata, the `OpenScope` method will fail.</span></span>  
  
 <span data-ttu-id="79256-116">.NET Framework バージョン 1.0 と version 1.1 の場合、スコープが開かれてで`dwOpenFlags`ofRead に設定すると、資格が共有するためです。</span><span class="sxs-lookup"><span data-stu-id="79256-116">In the .NET Framework version 1.0 and version 1.1, if a scope is opened with `dwOpenFlags` set to ofRead, it is eligible for sharing.</span></span> <span data-ttu-id="79256-117">つまり、以降の場合を呼び出す`OpenScope`以前、開かれたファイル名を渡し、既存のスコープが再利用し、データの構造体の新しいセットは作成されません。</span><span class="sxs-lookup"><span data-stu-id="79256-117">That is, if subsequent calls to `OpenScope` pass in the name of a file that was previously opened, the existing scope is reused and a new set of data structures is not created.</span></span> <span data-ttu-id="79256-118">ただし、この共有により問題が発生することができます。</span><span class="sxs-lookup"><span data-stu-id="79256-118">However, problems can arise due to this sharing.</span></span>  
  
 <span data-ttu-id="79256-119">.NET Framework version 2.0 でスコープが開かれた`dwOpenFlags`ofRead に設定が共有されなくなります。</span><span class="sxs-lookup"><span data-stu-id="79256-119">In the .NET Framework version 2.0, scopes opened with `dwOpenFlags` set to ofRead are no longer shared.</span></span> <span data-ttu-id="79256-120">共有するスコープを許可するのにには、ofReadOnly 値を使用します。</span><span class="sxs-lookup"><span data-stu-id="79256-120">Use the ofReadOnly value to allow the scope to be shared.</span></span> <span data-ttu-id="79256-121">スコープを共有すると、「読み取り/書き込み」メタデータ インターフェイスを使用するクエリは失敗します。</span><span class="sxs-lookup"><span data-stu-id="79256-121">When a scope is shared, queries that use "read/write" metadata interfaces will fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79256-122">必要条件</span><span class="sxs-lookup"><span data-stu-id="79256-122">Requirements</span></span>  
 <span data-ttu-id="79256-123">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="79256-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79256-124">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="79256-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="79256-125">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="79256-125">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="79256-126">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79256-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79256-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="79256-127">See also</span></span>
- [<span data-ttu-id="79256-128">IMetaDataDispenser インターフェイス</span><span class="sxs-lookup"><span data-stu-id="79256-128">IMetaDataDispenser Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
- [<span data-ttu-id="79256-129">IMetaDataDispenserEx インターフェイス</span><span class="sxs-lookup"><span data-stu-id="79256-129">IMetaDataDispenserEx Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)
- [<span data-ttu-id="79256-130">IMetaDataAssemblyEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="79256-130">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
- [<span data-ttu-id="79256-131">IMetaDataAssemblyImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="79256-131">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
- [<span data-ttu-id="79256-132">IMetaDataEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="79256-132">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="79256-133">IMetaDataEmit2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="79256-133">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
- [<span data-ttu-id="79256-134">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="79256-134">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="79256-135">IMetaDataImport2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="79256-135">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
