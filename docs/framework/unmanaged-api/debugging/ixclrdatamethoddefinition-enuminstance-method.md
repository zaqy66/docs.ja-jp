---
title: IXCLRDataMethodDefinition::EnumInstance メソッド
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::EnumInstance Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::EnumInstance Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::EnumInstance Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 420acda89858713f12ea87a8c8d3909682a3f5e3
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416729"
---
# <a name="ixclrdatamethoddefinitionenuminstance-method"></a><span data-ttu-id="d3c90-102">IXCLRDataMethodDefinition::EnumInstance メソッド</span><span class="sxs-lookup"><span data-stu-id="d3c90-102">IXCLRDataMethodDefinition::EnumInstance Method</span></span>

<span data-ttu-id="d3c90-103">このメソッドの定義のインスタンスを列挙します。</span><span class="sxs-lookup"><span data-stu-id="d3c90-103">Enumerates the instances of this method definition.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="d3c90-104">構文</span><span class="sxs-lookup"><span data-stu-id="d3c90-104">Syntax</span></span>

```
HRESULT EnumInstance(
    [in, out] CLRDATA_ENUM         *handle,
    [out] IXCLRDataMethodInstance **instance
);
```

### <a name="parameters"></a><span data-ttu-id="d3c90-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d3c90-105">Parameters</span></span>

<span data-ttu-id="d3c90-106">`handle` [入力、出力]インスタンスを列挙するためのハンドル。</span><span class="sxs-lookup"><span data-stu-id="d3c90-106">`handle` [in, out] A handle for enumerating the instances.</span></span>

<span data-ttu-id="d3c90-107">`instance` [out]列挙型のインスタンス。</span><span class="sxs-lookup"><span data-stu-id="d3c90-107">`instance` [out] The enumerated instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3c90-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="d3c90-108">Remarks</span></span>

<span data-ttu-id="d3c90-109">指定されたメソッドは、`IXCLRDataMethodDefinition`インターフェイスし、仮想メソッド テーブルの 4 番目のスロットに対応しています。</span><span class="sxs-lookup"><span data-stu-id="d3c90-109">The provided method is part of the `IXCLRDataMethodDefinition` interface and corresponds to the fourth slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c90-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="d3c90-110">Requirements</span></span>

<span data-ttu-id="d3c90-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3c90-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="d3c90-112">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="d3c90-112">**Header:** None</span></span>  
<span data-ttu-id="d3c90-113">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="d3c90-113">**Library:** None</span></span>  
<span data-ttu-id="d3c90-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d3c90-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="d3c90-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="d3c90-115">See Also</span></span>

- [<span data-ttu-id="d3c90-116">CLRDataSourceType 列挙型</span><span class="sxs-lookup"><span data-stu-id="d3c90-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="d3c90-117">デバッグ</span><span class="sxs-lookup"><span data-stu-id="d3c90-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="d3c90-118">IXCLRDataMethodDefinition インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d3c90-118">IXCLRDataMethodDefinition Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-interface.md)
- [<span data-ttu-id="d3c90-119">IXCLRDataMethodInstance インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d3c90-119">IXCLRDataMethodInstance Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethodinstance-interface.md)
