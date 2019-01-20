---
title: CLRDATA_ADDRESS_RANGE 構造体
ms.date: 01/16/2019
api.name:
- CLRDATA_ADDRESS_RANGE Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDATA_ADDRESS_RANGE Structure
helpviewer.keywords:
- CLRDATA_ADDRESS_RANGE Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 3a8832a0eb173da00715bd0441b7efd337eae932
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416542"
---
# <a name="clrdataaddressrange-structure"></a><span data-ttu-id="d2263-102">CLRDATA_ADDRESS_RANGE 構造体</span><span class="sxs-lookup"><span data-stu-id="d2263-102">CLRDATA_ADDRESS_RANGE Structure</span></span>

<span data-ttu-id="d2263-103">アドレスの範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="d2263-103">Defines an address range.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="d2263-104">構文</span><span class="sxs-lookup"><span data-stu-id="d2263-104">Syntax</span></span>

```
typedef struct
{
    CLRDATA_ADDRESS startAddress;
    CLRDATA_ADDRESS endAddress;
} CLRDATA_ADDRESS_RANGE;
```

## <a name="members"></a><span data-ttu-id="d2263-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="d2263-105">Members</span></span>

| <span data-ttu-id="d2263-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="d2263-106">Member</span></span>         | <span data-ttu-id="d2263-107">説明</span><span class="sxs-lookup"><span data-stu-id="d2263-107">Description</span></span>                     |
| -------------- | ------------------------------- |
| `startAddress` | <span data-ttu-id="d2263-108">範囲の開始アドレス。</span><span class="sxs-lookup"><span data-stu-id="d2263-108">The start address of the range.</span></span> |
| `endAddress`   | <span data-ttu-id="d2263-109">範囲の終了アドレス。</span><span class="sxs-lookup"><span data-stu-id="d2263-109">The end address of the range.</span></span>   |

## <a name="remarks"></a><span data-ttu-id="d2263-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="d2263-110">Remarks</span></span>

<span data-ttu-id="d2263-111">この構造は、ランタイム内に収めるし、任意のヘッダーまたはライブラリ ファイルでは公開されません。</span><span class="sxs-lookup"><span data-stu-id="d2263-111">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="d2263-112">これを使用する構造を定義、上で指定した場所`CLRDATA_ADDRESS`は 64 ビット符号なし整数。</span><span class="sxs-lookup"><span data-stu-id="d2263-112">To use it, define the structure as specified above, where `CLRDATA_ADDRESS` is a 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2263-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="d2263-113">Requirements</span></span>

<span data-ttu-id="d2263-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2263-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="d2263-115">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="d2263-115">**Header:** None</span></span>  
<span data-ttu-id="d2263-116">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="d2263-116">**Library:** None</span></span>  
<span data-ttu-id="d2263-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d2263-117">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="d2263-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2263-118">See Also</span></span>

- [<span data-ttu-id="d2263-119">デバッグ</span><span class="sxs-lookup"><span data-stu-id="d2263-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="d2263-120">デバッグ構造体</span><span class="sxs-lookup"><span data-stu-id="d2263-120">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
