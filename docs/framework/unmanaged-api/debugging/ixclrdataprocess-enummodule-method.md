---
title: IXCLRDataProcess::EnumModule メソッド
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumModule Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumModule Method
helpviewer.keywords:
- IXCLRDataProcess::EnumModule Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 1648e53df5f36f7615831b425d2b5d764731c5c4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54738132"
---
# <a name="ixclrdataprocessenummodule-method"></a><span data-ttu-id="d9f2c-102">IXCLRDataProcess::EnumModule メソッド</span><span class="sxs-lookup"><span data-stu-id="d9f2c-102">IXCLRDataProcess::EnumModule Method</span></span>

<span data-ttu-id="d9f2c-103">このプロセスのモジュールを列挙します。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-103">Enumerates the modules of this process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="d9f2c-104">構文</span><span class="sxs-lookup"><span data-stu-id="d9f2c-104">Syntax</span></span>

```
HRESULT EnumModule(
    [in, out] CLRDATA_ENUM  *handle,
    [out] IXCLRDataModule  **mod
);
```

### <a name="parameters"></a><span data-ttu-id="d9f2c-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9f2c-105">Parameters</span></span>

<span data-ttu-id="d9f2c-106">`handle` [入力、出力]モジュールを列挙するためのハンドル。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-106">`handle` [in, out] A handle for enumerating the modules.</span></span>

<span data-ttu-id="d9f2c-107">`mod` [out]列挙されたモジュール。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-107">`mod` [out] The enumerated module.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9f2c-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="d9f2c-108">Remarks</span></span>

<span data-ttu-id="d9f2c-109">指定されたメソッドは、`IXCLRDataProcess`インターフェイスし、仮想メソッド テーブルの 25 のスロットに対応しています。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 25th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f2c-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="d9f2c-110">Requirements</span></span>

<span data-ttu-id="d9f2c-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="d9f2c-112">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="d9f2c-112">**Header:** None</span></span>  
<span data-ttu-id="d9f2c-113">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="d9f2c-113">**Library:** None</span></span>  
<span data-ttu-id="d9f2c-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d9f2c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="d9f2c-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9f2c-115">See also</span></span>

- [<span data-ttu-id="d9f2c-116">CLRDataSourceType 列挙型</span><span class="sxs-lookup"><span data-stu-id="d9f2c-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="d9f2c-117">デバッグ</span><span class="sxs-lookup"><span data-stu-id="d9f2c-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="d9f2c-118">IXCLRDataModule インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d9f2c-118">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
- [<span data-ttu-id="d9f2c-119">IXCLRDataProcess インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d9f2c-119">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
