---
title: IXCLRDataModule::GetMethodDefinitionByToken メソッド
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::GetMethodDefinitionByToken Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method
helpviewer.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 1371b86f30324908a639b3b1bbae0ae007ba590a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54708091"
---
# <a name="ixclrdatamodulegetmethoddefinitionbytoken-method"></a><span data-ttu-id="89a44-102">IXCLRDataModule::GetMethodDefinitionByToken メソッド</span><span class="sxs-lookup"><span data-stu-id="89a44-102">IXCLRDataModule::GetMethodDefinitionByToken Method</span></span>

<span data-ttu-id="89a44-103">指定したメタデータ トークンに対応するメソッドの定義を取得します。</span><span class="sxs-lookup"><span data-stu-id="89a44-103">Gets the method definition corresponding to a given metadata token.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="89a44-104">構文</span><span class="sxs-lookup"><span data-stu-id="89a44-104">Syntax</span></span>

```
HRESULT GetMethodDefinitionByToken(
    [in] mdMethodDef token,
    [out] IXCLRDataMethodDefinition** methodDefinition
);
```

### <a name="parameters"></a><span data-ttu-id="89a44-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89a44-105">Parameters</span></span>

<span data-ttu-id="89a44-106">`token` [in]メソッド トークンです。</span><span class="sxs-lookup"><span data-stu-id="89a44-106">`token` [in] The method token.</span></span>

<span data-ttu-id="89a44-107">`methodDefinition` [out]メソッドの定義。</span><span class="sxs-lookup"><span data-stu-id="89a44-107">`methodDefinition` [out] The method definition.</span></span>

## <a name="remarks"></a><span data-ttu-id="89a44-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="89a44-108">Remarks</span></span>

<span data-ttu-id="89a44-109">指定されたメソッドは、`IXCLRDataModule`インターフェイスし、仮想メソッド テーブルの 25 のスロットに対応しています。</span><span class="sxs-lookup"><span data-stu-id="89a44-109">The provided method is part of the `IXCLRDataModule` interface and corresponds to the 25th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="89a44-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="89a44-110">Requirements</span></span>

<span data-ttu-id="89a44-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="89a44-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="89a44-112">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="89a44-112">**Header:** None</span></span>  
<span data-ttu-id="89a44-113">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="89a44-113">**Library:** None</span></span>  
<span data-ttu-id="89a44-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="89a44-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  
 
## <a name="see-also"></a><span data-ttu-id="89a44-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="89a44-115">See also</span></span>

- [<span data-ttu-id="89a44-116">デバッグ</span><span class="sxs-lookup"><span data-stu-id="89a44-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="89a44-117">IXCLRDataModule インターフェイス</span><span class="sxs-lookup"><span data-stu-id="89a44-117">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
