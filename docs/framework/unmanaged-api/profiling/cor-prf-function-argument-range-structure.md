---
title: COR_PRF_FUNCTION_ARGUMENT_RANGE 構造体
ms.date: 03/30/2017
api_name:
- COR_PRF_FUNCTION_ARGUMENT_RANGE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_FUNCTION_ARGUMENT_RANGE
helpviewer_keywords:
- COR_PRF_FUNCTION_ARGUMENT_RANGE structure [.NET Framework profiling'
ms.assetid: 9f469eac-ac66-419b-8668-fe705bc1a51f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ddd8e86b119a3c19417306dee056e435a4f5d07a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54537908"
---
# <a name="corprffunctionargumentrange-structure"></a><span data-ttu-id="fdd92-102">COR_PRF_FUNCTION_ARGUMENT_RANGE 構造体</span><span class="sxs-lookup"><span data-stu-id="fdd92-102">COR_PRF_FUNCTION_ARGUMENT_RANGE Structure</span></span>
<span data-ttu-id="fdd92-103">メモリに左から右方向へ連続で格納される関数の引数のブロックを表します。</span><span class="sxs-lookup"><span data-stu-id="fdd92-103">Represents a block of function arguments stored contiguously in left-to-right order in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fdd92-104">構文</span><span class="sxs-lookup"><span data-stu-id="fdd92-104">Syntax</span></span>  
  
```  
typedef struct _COR_PRF_FUNCTION_ARGUMENT_RANGE {  
    UINT_PTR startAddress;  
    ULONG length;  
} COR_PRF_FUNCTION_ARGUMENT_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="fdd92-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="fdd92-105">Members</span></span>  
  
|<span data-ttu-id="fdd92-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="fdd92-106">Members</span></span>|<span data-ttu-id="fdd92-107">説明</span><span class="sxs-lookup"><span data-stu-id="fdd92-107">Description</span></span>|  
|-------------|-----------------|  
|`startAddress`|<span data-ttu-id="fdd92-108">ブロックの開始アドレス。</span><span class="sxs-lookup"><span data-stu-id="fdd92-108">The starting address of the block.</span></span>|  
|`length`|<span data-ttu-id="fdd92-109">連続するブロックの長さ。</span><span class="sxs-lookup"><span data-stu-id="fdd92-109">The length of the contiguous block.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fdd92-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="fdd92-110">Requirements</span></span>  
 <span data-ttu-id="fdd92-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdd92-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fdd92-112">**ヘッダー:** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="fdd92-112">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="fdd92-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fdd92-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fdd92-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fdd92-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fdd92-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="fdd92-115">See also</span></span>
- [<span data-ttu-id="fdd92-116">構造体のプロファイリング</span><span class="sxs-lookup"><span data-stu-id="fdd92-116">Profiling Structures</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-structures.md)
