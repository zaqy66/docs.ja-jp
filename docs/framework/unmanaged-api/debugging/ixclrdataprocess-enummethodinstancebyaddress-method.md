---
title: IXCLRDataProcess::EnumMethodInstanceByAddress メソッド
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: b42939e8e64e75337478ace67a9a91c6a03a94e3
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416682"
---
# <a name="ixclrdataprocessenummethodinstancebyaddress-method"></a><span data-ttu-id="6cb0f-102">IXCLRDataProcess::EnumMethodInstanceByAddress メソッド</span><span class="sxs-lookup"><span data-stu-id="6cb0f-102">IXCLRDataProcess::EnumMethodInstanceByAddress Method</span></span>

<span data-ttu-id="6cb0f-103">このプロセスがアドレス オフセットから始まるのメソッドのインスタンスを列挙します。</span><span class="sxs-lookup"><span data-stu-id="6cb0f-103">Enumerates the method instances of this process starting at an address offset.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="6cb0f-104">構文</span><span class="sxs-lookup"><span data-stu-id="6cb0f-104">Syntax</span></span>

```
HRESULT EnumMethodInstanceByAddress(
    [in] CLRDATA_ENUM              *handle,
    [out] IXCLRDataMethodInstance **method
);
```

### <a name="parameters"></a><span data-ttu-id="6cb0f-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6cb0f-105">Parameters</span></span>

<span data-ttu-id="6cb0f-106">`handle` [in]メソッド インスタンスを列挙するためのハンドル。</span><span class="sxs-lookup"><span data-stu-id="6cb0f-106">`handle` [in] A handle for enumerating the method instances.</span></span>

<span data-ttu-id="6cb0f-107">`mod` [out]列挙メソッドのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="6cb0f-107">`mod` [out] The enumerated method instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cb0f-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="6cb0f-108">Remarks</span></span>

<span data-ttu-id="6cb0f-109">指定されたメソッドは、`IXCLRDataProcess`インターフェイスし、仮想メソッド テーブルの 28 のスロットに対応しています。</span><span class="sxs-lookup"><span data-stu-id="6cb0f-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 28th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb0f-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="6cb0f-110">Requirements</span></span>

<span data-ttu-id="6cb0f-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cb0f-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>   
<span data-ttu-id="6cb0f-112">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="6cb0f-112">**Header:** None</span></span>   
<span data-ttu-id="6cb0f-113">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="6cb0f-113">**Library:** None</span></span>   
<span data-ttu-id="6cb0f-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="6cb0f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>   
 
## <a name="see-also"></a><span data-ttu-id="6cb0f-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="6cb0f-115">See Also</span></span>
- [<span data-ttu-id="6cb0f-116">CLRDataSourceType 列挙型</span><span class="sxs-lookup"><span data-stu-id="6cb0f-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="6cb0f-117">デバッグ</span><span class="sxs-lookup"><span data-stu-id="6cb0f-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="6cb0f-118">IXCLRDataProcess インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6cb0f-118">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
