---
title: IXCLRDataProcess::GetAppDomainByUniqueId メソッド
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
helpviewer.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 83e7d4e1a4ff3c2e6f573d6c097c7cdb9c5f3c54
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416699"
---
# <a name="ixclrdataprocessgetappdomainbyuniqueid-method"></a><span data-ttu-id="501e4-102">IXCLRDataProcess::GetAppDomainByUniqueId メソッド</span><span class="sxs-lookup"><span data-stu-id="501e4-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span></span>

<span data-ttu-id="501e4-103">取得、`AppDomain`の一意の識別子に基づくプロセスにします。</span><span class="sxs-lookup"><span data-stu-id="501e4-103">Gets an `AppDomain` in a process based on its unique identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="501e4-104">構文</span><span class="sxs-lookup"><span data-stu-id="501e4-104">Syntax</span></span>
```
HRESULT GetAppDomainByUniqueID(
    [in] ULONG64               id,
    [out] IXCLRDataAppDomain **appDomain
);
```

### <a name="parameters"></a><span data-ttu-id="501e4-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="501e4-105">Parameters</span></span>
<span data-ttu-id="501e4-106">`id` [in]AppDomain の一意の識別子</span><span class="sxs-lookup"><span data-stu-id="501e4-106">`id` [in] The unique identifier of the AppDomain</span></span>

<span data-ttu-id="501e4-107">`appDomain` [out]AppDomain</span><span class="sxs-lookup"><span data-stu-id="501e4-107">`appDomain` [out] The AppDomain</span></span>

## <a name="remarks"></a><span data-ttu-id="501e4-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="501e4-108">Remarks</span></span>

<span data-ttu-id="501e4-109">指定されたメソッドは、`IXCLRDataProcess`インターフェイスし、仮想メソッド テーブルの 20 のスロットに対応しています。</span><span class="sxs-lookup"><span data-stu-id="501e4-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 20th slot of the virtual method table.</span></span> <span data-ttu-id="501e4-110">`IXCLRDataAppDomain*`返されるその他の Api との対話のために使用します。</span><span class="sxs-lookup"><span data-stu-id="501e4-110">The `IXCLRDataAppDomain*` returned is used for interaction with other APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="501e4-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="501e4-111">Requirements</span></span>
<span data-ttu-id="501e4-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="501e4-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="501e4-113">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="501e4-113">**Header:** None</span></span>  
<span data-ttu-id="501e4-114">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="501e4-114">**Library:** None</span></span>  
<span data-ttu-id="501e4-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="501e4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="501e4-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="501e4-116">See Also</span></span>
- [<span data-ttu-id="501e4-117">デバッグ</span><span class="sxs-lookup"><span data-stu-id="501e4-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="501e4-118">IXCLRDataProcess インターフェイス</span><span class="sxs-lookup"><span data-stu-id="501e4-118">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
