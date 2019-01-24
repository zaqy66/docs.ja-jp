---
title: IXCLRDataProcess::EndEnumMethodInstancesByAddress メソッド
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 67978e49a8c23c4b25234ecbb3639c696c7232f4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54655648"
---
# <a name="ixclrdataprocessendenummethodinstancesbyaddress-method"></a><span data-ttu-id="1a531-102">IXCLRDataProcess::EndEnumMethodInstancesByAddress メソッド</span><span class="sxs-lookup"><span data-stu-id="1a531-102">IXCLRDataProcess::EndEnumMethodInstancesByAddress Method</span></span>

<span data-ttu-id="1a531-103">インスタンスの列挙中に使用される内部の反復子によって使用されるリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="1a531-103">Releases the resources used by internal iterators used during instance enumeration.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="1a531-104">構文</span><span class="sxs-lookup"><span data-stu-id="1a531-104">Syntax</span></span>

```
HRESULT EndEnumMethodInstancesByAddress(
    [in] CLRDATA_ENUM handle
);
```

### <a name="parameters"></a><span data-ttu-id="1a531-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1a531-105">Parameters</span></span>

<span data-ttu-id="1a531-106">`handle` [out]メソッド インスタンスを列挙するためのハンドル。</span><span class="sxs-lookup"><span data-stu-id="1a531-106">`handle` [out] A handle for enumerating the method instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a531-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="1a531-107">Remarks</span></span>

<span data-ttu-id="1a531-108">指定されたメソッドは、`IXCLRDataProcess`インターフェイスし、仮想メソッド テーブルの 29 のスロットに対応しています。</span><span class="sxs-lookup"><span data-stu-id="1a531-108">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 29th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a531-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="1a531-109">Requirements</span></span>

<span data-ttu-id="1a531-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1a531-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="1a531-111">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="1a531-111">**Header:** None</span></span>  
<span data-ttu-id="1a531-112">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="1a531-112">**Library:** None</span></span>  
<span data-ttu-id="1a531-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="1a531-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="1a531-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a531-114">See also</span></span>

- [<span data-ttu-id="1a531-115">CLRDataSourceType 列挙型</span><span class="sxs-lookup"><span data-stu-id="1a531-115">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="1a531-116">デバッグ</span><span class="sxs-lookup"><span data-stu-id="1a531-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="1a531-117">IXCLRDataProcess インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1a531-117">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
