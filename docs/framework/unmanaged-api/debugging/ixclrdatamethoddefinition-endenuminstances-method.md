---
title: IXCLRDataMethodDefinition::EndEnumInstances メソッド
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::EndEnumInstances Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::EndEnumInstances Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::EndEnumInstances Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 4a7cd8850778e9bbbc7d8d67f464c7787e40bc13
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54566097"
---
# <a name="ixclrdatamethoddefinitionendenuminstances-method"></a><span data-ttu-id="f50ad-102">IXCLRDataMethodDefinition::EndEnumInstances メソッド</span><span class="sxs-lookup"><span data-stu-id="f50ad-102">IXCLRDataMethodDefinition::EndEnumInstances Method</span></span>

<span data-ttu-id="f50ad-103">インスタンスの列挙中に使用される内部の反復子によって使用されるリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="f50ad-103">Releases the resources used by internal iterators used during instance enumeration.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="f50ad-104">構文</span><span class="sxs-lookup"><span data-stu-id="f50ad-104">Syntax</span></span>

```
HRESULT EndEnumInstances(
    [in] CLRDATA_ENUM handle
);
```

### <a name="parameters"></a><span data-ttu-id="f50ad-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f50ad-105">Parameters</span></span>

<span data-ttu-id="f50ad-106">`handle` [out]インスタンスを列挙するためのハンドル。</span><span class="sxs-lookup"><span data-stu-id="f50ad-106">`handle` [out] A handle for enumerating the instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="f50ad-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="f50ad-107">Remarks</span></span>

<span data-ttu-id="f50ad-108">指定されたメソッドは、`IXCLRDataMethodDefinition`インターフェイスし、仮想メソッド テーブルの 5 番目のスロットに対応しています。</span><span class="sxs-lookup"><span data-stu-id="f50ad-108">The provided method is part of the `IXCLRDataMethodDefinition` interface and corresponds to the fifth slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="f50ad-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="f50ad-109">Requirements</span></span>

<span data-ttu-id="f50ad-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f50ad-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="f50ad-111">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="f50ad-111">**Header:** None</span></span>  
<span data-ttu-id="f50ad-112">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="f50ad-112">**Library:** None</span></span>  
<span data-ttu-id="f50ad-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="f50ad-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="f50ad-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="f50ad-114">See also</span></span>

- [<span data-ttu-id="f50ad-115">デバッグ</span><span class="sxs-lookup"><span data-stu-id="f50ad-115">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="f50ad-116">IXCLRDataMethodDefinition インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f50ad-116">IXCLRDataMethodDefinition Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-interface.md)
