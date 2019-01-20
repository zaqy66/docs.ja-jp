---
title: IXCLRDataProcess::EndEnumModules メソッド
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EndEnumModules Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EndEnumModules Method
helpviewer.keywords:
- IXCLRDataProcess::EndEnumModules Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: cd49ae5fa274c577cfa3c04ec599e488384dfc64
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416659"
---
# <a name="ixclrdataprocessendenummodules-method"></a><span data-ttu-id="60ea6-102">IXCLRDataProcess::EndEnumModules メソッド</span><span class="sxs-lookup"><span data-stu-id="60ea6-102">IXCLRDataProcess::EndEnumModules Method</span></span>

<span data-ttu-id="60ea6-103">モジュールの列挙中に使用される内部の反復子によって使用されるリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="60ea6-103">Releases the resources used by internal iterators used during module enumeration.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="60ea6-104">構文</span><span class="sxs-lookup"><span data-stu-id="60ea6-104">Syntax</span></span>
```
HRESULT EndEnumModules(
    [in] CLRDATA_ENUM handle
);
```

### <a name="parameters"></a><span data-ttu-id="60ea6-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="60ea6-105">Parameters</span></span>
<span data-ttu-id="60ea6-106">`handle` [out]モジュールを列挙するためのハンドル。</span><span class="sxs-lookup"><span data-stu-id="60ea6-106">`handle` [out] A handle for enumerating the modules.</span></span>

## <a name="remarks"></a><span data-ttu-id="60ea6-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="60ea6-107">Remarks</span></span>

<span data-ttu-id="60ea6-108">指定されたメソッドは、`IXCLRDataProcess`インターフェイスし、仮想メソッド テーブルの 26 のスロットに対応しています。</span><span class="sxs-lookup"><span data-stu-id="60ea6-108">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 26th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="60ea6-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="60ea6-109">Requirements</span></span>

<span data-ttu-id="60ea6-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="60ea6-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>   
<span data-ttu-id="60ea6-111">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="60ea6-111">**Header:** None</span></span>   
<span data-ttu-id="60ea6-112">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="60ea6-112">**Library:** None</span></span>   
<span data-ttu-id="60ea6-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="60ea6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>   

## <a name="see-also"></a><span data-ttu-id="60ea6-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="60ea6-114">See Also</span></span>

- [<span data-ttu-id="60ea6-115">デバッグ</span><span class="sxs-lookup"><span data-stu-id="60ea6-115">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="60ea6-116">IXCLRDataProcess インターフェイス</span><span class="sxs-lookup"><span data-stu-id="60ea6-116">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
