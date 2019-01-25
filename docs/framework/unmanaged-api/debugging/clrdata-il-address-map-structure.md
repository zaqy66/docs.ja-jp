---
title: CLRDATA_IL_ADDRESS_MAP 構造体
ms.date: 01/16/2019
api.name:
- CLRDATA_IL_ADDRESS_MAP Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDATA_IL_ADDRESS_MAP Structure
helpviewer.keywords:
- CLRDATA_IL_ADDRESS_MAP Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 3aac7e24fa9cd03350aebf5f441063bcedfaed04
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54644769"
---
# <a name="clrdatailaddressmap-structure"></a><span data-ttu-id="0e97f-102">CLRDATA_IL_ADDRESS_MAP 構造体</span><span class="sxs-lookup"><span data-stu-id="0e97f-102">CLRDATA_IL_ADDRESS_MAP Structure</span></span>

<span data-ttu-id="0e97f-103">アドレスのマッピングには、IL を定義します。</span><span class="sxs-lookup"><span data-stu-id="0e97f-103">Defines an IL to address mapping.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="0e97f-104">構文</span><span class="sxs-lookup"><span data-stu-id="0e97f-104">Syntax</span></span>

```
typedef struct
{
    ULONG32 ilOffset;
    CLRDATA_ADDRESS startAddress;
    CLRDATA_ADDRESS endAddress;
    CLRDataSourceType type;
} CLRDATA_IL_ADDRESS_MAP;
```

## <a name="members"></a><span data-ttu-id="0e97f-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="0e97f-105">Members</span></span>

| <span data-ttu-id="0e97f-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="0e97f-106">Member</span></span>         | <span data-ttu-id="0e97f-107">説明</span><span class="sxs-lookup"><span data-stu-id="0e97f-107">Description</span></span>                                            |
| -------------- | ------------------------------------------------------ |
| `ilOffset`     | <span data-ttu-id="0e97f-108">含まれているアドレスの範囲の IL オフセット</span><span class="sxs-lookup"><span data-stu-id="0e97f-108">IL offset for the contained address range</span></span>              |
| `startAddress` | <span data-ttu-id="0e97f-109">範囲の開始アドレス。</span><span class="sxs-lookup"><span data-stu-id="0e97f-109">The start address of the range.</span></span>                        |
| `endAddress`   | <span data-ttu-id="0e97f-110">範囲の終了アドレス。</span><span class="sxs-lookup"><span data-stu-id="0e97f-110">The end address of the range.</span></span>                          |
| `type`         | <span data-ttu-id="0e97f-111">データの型。</span><span class="sxs-lookup"><span data-stu-id="0e97f-111">The type of the data.</span></span> <span data-ttu-id="0e97f-112">この値が使用されません。</span><span class="sxs-lookup"><span data-stu-id="0e97f-112">This value is currently not used</span></span> |

## <a name="remarks"></a><span data-ttu-id="0e97f-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="0e97f-113">Remarks</span></span>

<span data-ttu-id="0e97f-114">この構造は、ランタイム内に収めるし、任意のヘッダーまたはライブラリ ファイルでは公開されません。</span><span class="sxs-lookup"><span data-stu-id="0e97f-114">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="0e97f-115">これを使用する構造を定義、上で指定した場所`CLRDATA_ADDRESS`は 64 ビット符号なし整数。</span><span class="sxs-lookup"><span data-stu-id="0e97f-115">To use it, define the structure as specified above, where `CLRDATA_ADDRESS` is a 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e97f-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="0e97f-116">Requirements</span></span>

<span data-ttu-id="0e97f-117">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e97f-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="0e97f-118">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="0e97f-118">**Header:** None</span></span>  
<span data-ttu-id="0e97f-119">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="0e97f-119">**Library:** None</span></span>   
<span data-ttu-id="0e97f-120">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="0e97f-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="0e97f-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e97f-121">See also</span></span>

- [<span data-ttu-id="0e97f-122">CLRDataSourceType 列挙型</span><span class="sxs-lookup"><span data-stu-id="0e97f-122">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="0e97f-123">デバッグ</span><span class="sxs-lookup"><span data-stu-id="0e97f-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="0e97f-124">デバッグ構造体</span><span class="sxs-lookup"><span data-stu-id="0e97f-124">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
