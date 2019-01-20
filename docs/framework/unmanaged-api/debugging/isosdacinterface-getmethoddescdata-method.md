---
title: ISOSDacInterface::GetMethodDescData メソッド
ms.date: 01/16/2019
api.name:
- ISOSDacInterface::GetMethodDescData Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescData Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescData Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 3f22752446413c622a20340541b0ac328f63c77b
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416732"
---
# <a name="isosdacinterfacegetmethoddescdata-method"></a><span data-ttu-id="7edcd-102">ISOSDacInterface::GetMethodDescData メソッド</span><span class="sxs-lookup"><span data-stu-id="7edcd-102">ISOSDacInterface::GetMethodDescData Method</span></span>

<span data-ttu-id="7edcd-103">データを取得、指定された[MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md)します。</span><span class="sxs-lookup"><span data-stu-id="7edcd-103">Gets the data for the given [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="7edcd-104">構文</span><span class="sxs-lookup"><span data-stu-id="7edcd-104">Syntax</span></span>

```
HRESULT GetMethodDescData(
    CLRDATA_ADDRESS            methodDesc,
    CLRDATA_ADDRESS            ip,
    void                       *data,
    ULONG                      cRevertedRejitVersions,
    void                      *rgRevertedRejitData,
    void                      *pcNeededRevertedRejitData
);
```

### <a name="parameters"></a><span data-ttu-id="7edcd-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7edcd-105">Parameters</span></span>

<span data-ttu-id="7edcd-106">`methodDesc` [in]MethodDesc アドレス。</span><span class="sxs-lookup"><span data-stu-id="7edcd-106">`methodDesc` [in] The address of the MethodDesc.</span></span>

<span data-ttu-id="7edcd-107">`ip` [in]メソッドの IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="7edcd-107">`ip` [in] The IP address of the method.</span></span>

<span data-ttu-id="7edcd-108">`data` [out]関連付けられている、MethodDesc 内部 Api から返されるデータ。</span><span class="sxs-lookup"><span data-stu-id="7edcd-108">`data` [out] The data associated with the MethodDesc as returned from the internal APIs.</span></span> <span data-ttu-id="7edcd-109">構造体には、少なくとも 168 バイトが必要があります。</span><span class="sxs-lookup"><span data-stu-id="7edcd-109">The structure needs at least 168 bytes.</span></span>

<span data-ttu-id="7edcd-110">`cRevertedRejitVersions` [out]元に戻された rejit バージョンの数。</span><span class="sxs-lookup"><span data-stu-id="7edcd-110">`cRevertedRejitVersions` [out] The number of reverted rejit versions.</span></span>

<span data-ttu-id="7edcd-111">`rgRevertedRejitData` [out]内部 Api から返されるように、元に戻された rejit バージョンに関連付けられたデータ。</span><span class="sxs-lookup"><span data-stu-id="7edcd-111">`rgRevertedRejitData` [out] The data associated with the reverted rejit versions as returned from the internal APIs.</span></span> <span data-ttu-id="7edcd-112">構造体には、少なくとも 24 バイト必要があります。</span><span class="sxs-lookup"><span data-stu-id="7edcd-112">The structure needs at least 24 bytes.</span></span>

<span data-ttu-id="7edcd-113">`pcNeededRevertedRejitData` [out]元に戻された ReJit バージョンに関連付けられたデータを格納するために必要なバイト数。</span><span class="sxs-lookup"><span data-stu-id="7edcd-113">`pcNeededRevertedRejitData` [out] The number of bytes required to store the data associated with the reverted ReJit versions.</span></span>

## <a name="remarks"></a><span data-ttu-id="7edcd-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="7edcd-114">Remarks</span></span>

<span data-ttu-id="7edcd-115">指定されたメソッドは、`ISOSDacInterface`インターフェイスし、仮想メソッド テーブルの 20 のスロットに対応しています。</span><span class="sxs-lookup"><span data-stu-id="7edcd-115">The provided method is part of the `ISOSDacInterface` interface and corresponds to the 20th slot of the virtual method table.</span></span> <span data-ttu-id="7edcd-116">また、`CLRDATA_ADDRESS`は 64 ビット符号なし整数。</span><span class="sxs-lookup"><span data-stu-id="7edcd-116">Also the `CLRDATA_ADDRESS` are 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7edcd-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="7edcd-117">Requirements</span></span>

<span data-ttu-id="7edcd-118">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7edcd-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="7edcd-119">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="7edcd-119">**Header:** None</span></span>  
<span data-ttu-id="7edcd-120">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="7edcd-120">**Library:** None</span></span>  
<span data-ttu-id="7edcd-121">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7edcd-121">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="7edcd-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="7edcd-122">See Also</span></span>

- [<span data-ttu-id="7edcd-123">デバッグ</span><span class="sxs-lookup"><span data-stu-id="7edcd-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="7edcd-124">ISOSDacInterface インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7edcd-124">ISOSDacInterface Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-interface.md)
