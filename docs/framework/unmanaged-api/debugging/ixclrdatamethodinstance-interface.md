---
title: IXCLRDataMethodInstance インターフェイス
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodInstance Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodInstance Interface
helpviewer.keywords:
- IXCLRDataMethodInstance Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 5bf724bc76591ae59c073b5b9a788ca065f51dc0
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416529"
---
# <a name="ixclrdatamethodinstance-interface"></a><span data-ttu-id="12318-102">IXCLRDataMethodInstance インターフェイス</span><span class="sxs-lookup"><span data-stu-id="12318-102">IXCLRDataMethodInstance Interface</span></span>

<span data-ttu-id="12318-103">メソッド インスタンスの情報を照会するためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="12318-103">Provides methods for querying information about a method instance.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="12318-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="12318-104">Methods</span></span>

| <span data-ttu-id="12318-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="12318-105">Method</span></span>                                                                                                                  | <span data-ttu-id="12318-106">説明</span><span class="sxs-lookup"><span data-stu-id="12318-106">Description</span></span>                                 |
| ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| [<span data-ttu-id="12318-107">GetILAddressMap</span><span class="sxs-lookup"><span data-stu-id="12318-107">GetILAddressMap</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethodinstance-getiladdressmap-method.md) | <span data-ttu-id="12318-108">アドレスのマッピング情報の IL を取得します。</span><span class="sxs-lookup"><span data-stu-id="12318-108">Gets the IL to address mapping information.</span></span> |

## <a name="remarks"></a><span data-ttu-id="12318-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="12318-109">Remarks</span></span>

<span data-ttu-id="12318-110">このインターフェイスは、ランタイム内に収めるを任意のヘッダーまたはライブラリ ファイルでは公開されません。</span><span class="sxs-lookup"><span data-stu-id="12318-110">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="12318-111">ただし、これは COM インターフェイスから派生した`IUnknown`GUID を持つ`ECD73800-22CA-4b0d-AB55-E9BA7E6318A5`を通常の COM メカニズムを通じて取得できます。</span><span class="sxs-lookup"><span data-stu-id="12318-111">However, it's a COM interface that derives from `IUnknown` with GUID `ECD73800-22CA-4b0d-AB55-E9BA7E6318A5` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="12318-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="12318-112">Requirements</span></span>

<span data-ttu-id="12318-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="12318-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="12318-114">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="12318-114">**Header:** None</span></span>  
<span data-ttu-id="12318-115">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="12318-115">**Library:** None</span></span>  
<span data-ttu-id="12318-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="12318-116">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="12318-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="12318-117">See Also</span></span>

- [<span data-ttu-id="12318-118">デバッグ</span><span class="sxs-lookup"><span data-stu-id="12318-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="12318-119">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="12318-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
