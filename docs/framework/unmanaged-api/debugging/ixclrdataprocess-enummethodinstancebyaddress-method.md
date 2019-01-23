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
ms.openlocfilehash: 825cb8ea94bee980f9e10b90cddf04db32c1a33f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491910"
---
# <a name="ixclrdataprocessenummethodinstancebyaddress-method"></a><span data-ttu-id="195d5-102">IXCLRDataProcess::EnumMethodInstanceByAddress メソッド</span><span class="sxs-lookup"><span data-stu-id="195d5-102">IXCLRDataProcess::EnumMethodInstanceByAddress Method</span></span>

<span data-ttu-id="195d5-103">このプロセスがアドレス オフセットから始まるのメソッドのインスタンスを列挙します。</span><span class="sxs-lookup"><span data-stu-id="195d5-103">Enumerates the method instances of this process starting at an address offset.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="195d5-104">構文</span><span class="sxs-lookup"><span data-stu-id="195d5-104">Syntax</span></span>

```
HRESULT EnumMethodInstanceByAddress(
    [in] CLRDATA_ENUM              *handle,
    [out] IXCLRDataMethodInstance **method
);
```

### <a name="parameters"></a><span data-ttu-id="195d5-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="195d5-105">Parameters</span></span>

<span data-ttu-id="195d5-106">`handle` [in]メソッド インスタンスを列挙するためのハンドル。</span><span class="sxs-lookup"><span data-stu-id="195d5-106">`handle` [in] A handle for enumerating the method instances.</span></span>

<span data-ttu-id="195d5-107">`mod` [out]列挙メソッドのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="195d5-107">`mod` [out] The enumerated method instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="195d5-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="195d5-108">Remarks</span></span>

<span data-ttu-id="195d5-109">指定されたメソッドは、`IXCLRDataProcess`インターフェイスし、仮想メソッド テーブルの 28 のスロットに対応しています。</span><span class="sxs-lookup"><span data-stu-id="195d5-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 28th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="195d5-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="195d5-110">Requirements</span></span>

<span data-ttu-id="195d5-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="195d5-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>   
<span data-ttu-id="195d5-112">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="195d5-112">**Header:** None</span></span>   
<span data-ttu-id="195d5-113">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="195d5-113">**Library:** None</span></span>   
<span data-ttu-id="195d5-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="195d5-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>   
 
## <a name="see-also"></a><span data-ttu-id="195d5-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="195d5-115">See also</span></span>
- [<span data-ttu-id="195d5-116">CLRDataSourceType 列挙型</span><span class="sxs-lookup"><span data-stu-id="195d5-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="195d5-117">デバッグ</span><span class="sxs-lookup"><span data-stu-id="195d5-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="195d5-118">IXCLRDataProcess インターフェイス</span><span class="sxs-lookup"><span data-stu-id="195d5-118">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
