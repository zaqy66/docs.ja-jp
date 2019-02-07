---
title: IXCLRDataMethodInstance::GetRepresentativeEntryAddress メソッド
ms.date: 02/01/2019
api.name:
- IXCLRDataMethodInstance::GetRepresentativeEntryAddress
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodInstance::GetRepresentativeEntryAddress
helpviewer.keywords:
- IXCLRDataMethodInstance::GetRepresentativeEntryAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 52b2fdaaefd16a49300641f44041b8352141385b
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2019
ms.locfileid: "55828676"
---
# <a name="ixclrdatamethodinstancegetrepresentativeentryaddress-method"></a><span data-ttu-id="c1780-102">IXCLRDataMethodInstance::GetRepresentativeEntryAddress メソッド</span><span class="sxs-lookup"><span data-stu-id="c1780-102">IXCLRDataMethodInstance::GetRepresentativeEntryAddress Method</span></span>

<span data-ttu-id="c1780-103">メソッドのエントリ ポイントは、すべてのネイティブ コンパイルの最も代表的なエントリ ポイントのアドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="c1780-103">Gets the most representative entry point address for the native compilation of all the possible entry points for a method.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="c1780-104">構文</span><span class="sxs-lookup"><span data-stu-id="c1780-104">Syntax</span></span>

```
HRESULT GetRepresentativeEntryAddress(
    [out] CLRDATA_ADDRESS* addr
);
```

### <a name="parameters"></a><span data-ttu-id="c1780-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c1780-105">Parameters</span></span>

<span data-ttu-id="c1780-106">`addr` [out]メソッドの最も代表的なネイティブ エントリ ポイントのアドレス。</span><span class="sxs-lookup"><span data-stu-id="c1780-106">`addr` [out] The address of the most representative native entry point for the method.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1780-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="c1780-107">Remarks</span></span>

<span data-ttu-id="c1780-108">指定されたメソッドは、 [ `IXCLRDataMethodInstance`インターフェイス](ixclrdatamethodinstance-interface.md)仮想メソッド テーブルの 19 のスロットに対応しています。</span><span class="sxs-lookup"><span data-stu-id="c1780-108">The provided method is part of the [`IXCLRDataMethodInstance` interface](ixclrdatamethodinstance-interface.md) and corresponds to the 19th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1780-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="c1780-109">Requirements</span></span>

<span data-ttu-id="c1780-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c1780-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="c1780-111">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="c1780-111">**Header:** None</span></span>  
<span data-ttu-id="c1780-112">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="c1780-112">**Library:** None</span></span>  
<span data-ttu-id="c1780-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="c1780-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="c1780-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1780-114">See also</span></span>

- [<span data-ttu-id="c1780-115">デバッグ</span><span class="sxs-lookup"><span data-stu-id="c1780-115">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="c1780-116">IXCLRDataMethodInstance インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c1780-116">IXCLRDataMethodInstance Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethodinstance-interface.md)
