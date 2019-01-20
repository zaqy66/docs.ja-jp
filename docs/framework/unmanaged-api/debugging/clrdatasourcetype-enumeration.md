---
title: CLRDataSourceType 列挙型
ms.date: 01/16/2019
api.name:
- CLRDataSourceType Enumeration
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDataSourceType Enumeration
helpviewer.keywords:
- CLRDataSourceType Enumeration [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 36651de5053e994103f79c9021e8e18e126f91fa
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416519"
---
# <a name="clrdatasourcetype-enumeration"></a><span data-ttu-id="9b6af-102">CLRDataSourceType 列挙型</span><span class="sxs-lookup"><span data-stu-id="9b6af-102">CLRDataSourceType Enumeration</span></span>

<span data-ttu-id="9b6af-103">CLRDATA_IL_ADDRESS_MAP 構造で使用される値を提供します。</span><span class="sxs-lookup"><span data-stu-id="9b6af-103">Provides values that are used by the CLRDATA_IL_ADDRESS_MAP structure.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="9b6af-104">構文</span><span class="sxs-lookup"><span data-stu-id="9b6af-104">Syntax</span></span>

```
typedef enum
{
    CLRDATA_SOURCE_TYPE_INVALID        = 0x00, // To indicate that nothing else applies
} CLRDataSourceType;
```

## <a name="members"></a><span data-ttu-id="9b6af-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="9b6af-105">Members</span></span>

| <span data-ttu-id="9b6af-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="9b6af-106">Member</span></span>                        | <span data-ttu-id="9b6af-107">説明</span><span class="sxs-lookup"><span data-stu-id="9b6af-107">Description</span></span>                           |
| ----------------------------- | ------------------------------------- |
| `CLRDATA_SOURCE_TYPE_INVALID` | <span data-ttu-id="9b6af-108">他に何も適用されることを示す</span><span class="sxs-lookup"><span data-stu-id="9b6af-108">To indicate that nothing else applies</span></span> |

## <a name="remarks"></a><span data-ttu-id="9b6af-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="9b6af-109">Remarks</span></span>

<span data-ttu-id="9b6af-110">この列挙体は、ランタイム内に収めるを任意のヘッダーまたはライブラリ ファイルでは公開されません。</span><span class="sxs-lookup"><span data-stu-id="9b6af-110">This enumeration lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="9b6af-111">これを使用するには、コード内に定義したよう列挙体を定義します。</span><span class="sxs-lookup"><span data-stu-id="9b6af-111">To use it, define an enumeration as defined above in your code.</span></span> <span data-ttu-id="9b6af-112">これは、エイリアスも`CLRDATA_ENUM`で説明したよう[一般的なデータ型](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md)します。</span><span class="sxs-lookup"><span data-stu-id="9b6af-112">This is also aliased to `CLRDATA_ENUM` as mentioned in [Common Data Types](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b6af-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="9b6af-113">Requirements</span></span>

<span data-ttu-id="9b6af-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b6af-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="9b6af-115">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="9b6af-115">**Header:** None</span></span>  
<span data-ttu-id="9b6af-116">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="9b6af-116">**Library:** None</span></span>  
<span data-ttu-id="9b6af-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="9b6af-117">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="9b6af-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b6af-118">See Also</span></span>

- [<span data-ttu-id="9b6af-119">デバッグ</span><span class="sxs-lookup"><span data-stu-id="9b6af-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="9b6af-120">列挙型のデバッグ</span><span class="sxs-lookup"><span data-stu-id="9b6af-120">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
