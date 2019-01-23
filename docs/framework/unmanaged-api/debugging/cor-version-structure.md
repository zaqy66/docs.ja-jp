---
title: COR_VERSION 構造体
ms.date: 03/30/2017
api_name:
- COR_VERSION
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_VERSION
helpviewer_keywords:
- COR_VERSION structure [.NET Framework debugging]
ms.assetid: 5efaee1c-a001-4c73-9525-4160f4c71567
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e07487f536454d9d2dcfff15eb871124112d250e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54634961"
---
# <a name="corversion-structure"></a><span data-ttu-id="066e2-102">COR_VERSION 構造体</span><span class="sxs-lookup"><span data-stu-id="066e2-102">COR_VERSION Structure</span></span>
<span data-ttu-id="066e2-103">共通言語ランタイムの標準の 4 つの部分のバージョン番号を保存します。</span><span class="sxs-lookup"><span data-stu-id="066e2-103">Stores the standard four-part version number of the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="066e2-104">構文</span><span class="sxs-lookup"><span data-stu-id="066e2-104">Syntax</span></span>  
  
```  
typedef struct _COR_VERSION {  
    DWORD dwMajor;  
    DWORD dwMinor;  
    DWORD dwBuild;  
    DWORD dwSubBuild;  
} COR_VERSION;  
```  
  
## <a name="members"></a><span data-ttu-id="066e2-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="066e2-105">Members</span></span>  
  
|<span data-ttu-id="066e2-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="066e2-106">Member</span></span>|<span data-ttu-id="066e2-107">説明</span><span class="sxs-lookup"><span data-stu-id="066e2-107">Description</span></span>|  
|------------|-----------------|  
|`dwMajor`|<span data-ttu-id="066e2-108">メジャー バージョン番号。</span><span class="sxs-lookup"><span data-stu-id="066e2-108">The major version number.</span></span>|  
|`dwMinor`|<span data-ttu-id="066e2-109">マイナー バージョン番号。</span><span class="sxs-lookup"><span data-stu-id="066e2-109">The minor version number.</span></span>|  
|`dwBuild`|<span data-ttu-id="066e2-110">ビルド番号。</span><span class="sxs-lookup"><span data-stu-id="066e2-110">The build number.</span></span>|  
|`dwSubBuild`|<span data-ttu-id="066e2-111">サブ ビルド番号。</span><span class="sxs-lookup"><span data-stu-id="066e2-111">The sub-build number.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="066e2-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="066e2-112">Remarks</span></span>  
 <span data-ttu-id="066e2-113">1.0.3705.288 をバージョン番号には、1 はメジャー バージョン番号、マイナー バージョン番号が 0 には 3705 はビルド番号、および 288 はサブ ビルド番号。</span><span class="sxs-lookup"><span data-stu-id="066e2-113">If the version number is 1.0.3705.288, 1 is the major version number, 0 is the minor version number, 3705 is the build number, and 288 is the sub-build number.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="066e2-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="066e2-114">Requirements</span></span>  
 <span data-ttu-id="066e2-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="066e2-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="066e2-116">**ヘッダー:** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="066e2-116">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="066e2-117">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="066e2-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="066e2-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="066e2-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="066e2-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="066e2-119">See also</span></span>
- [<span data-ttu-id="066e2-120">デバッグ構造体</span><span class="sxs-lookup"><span data-stu-id="066e2-120">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="066e2-121">デバッグ</span><span class="sxs-lookup"><span data-stu-id="066e2-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
