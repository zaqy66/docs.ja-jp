---
title: COR_GC_STAT_TYPES 列挙体
ms.date: 03/30/2017
api_name:
- COR_GC_STAT_TYPES
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_GC_STAT_TYPES
helpviewer_keywords:
- COR_GC_STAT_TYPES enumeration [.NET Framework hosting]
ms.assetid: fc51d6db-f7f8-408b-b93d-c166fc712c99
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4bd12feb47352d9bb78aa8ef056072f9bdc6fba3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710327"
---
# <a name="corgcstattypes-enumeration"></a><span data-ttu-id="85d0e-102">COR_GC_STAT_TYPES 列挙体</span><span class="sxs-lookup"><span data-stu-id="85d0e-102">COR_GC_STAT_TYPES Enumeration</span></span>
<span data-ttu-id="85d0e-103">ガベージ コレクションについて記録する統計情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="85d0e-103">Specifies the statistics to be recorded for a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85d0e-104">構文</span><span class="sxs-lookup"><span data-stu-id="85d0e-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_GC_COUNTS                 = 0x00000001  
    COR_GC_MEMORYUSAGE            = 0x00000002  
} COR_GC_STAT_TYPES;  
```  
  
## <a name="remarks"></a><span data-ttu-id="85d0e-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="85d0e-105">Remarks</span></span>  
 <span data-ttu-id="85d0e-106">この列挙体の統計情報の指定、 [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md)構造体は設定[iclrgcmanager::getstats](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-getstats-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="85d0e-106">This enumeration specifies which statistics in the [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure are to be set by [ICLRGCManager::GetStats](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-getstats-method.md) method.</span></span>  
  
## <a name="members"></a><span data-ttu-id="85d0e-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="85d0e-107">Members</span></span>  
  
|<span data-ttu-id="85d0e-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="85d0e-108">Member</span></span>|<span data-ttu-id="85d0e-109">説明</span><span class="sxs-lookup"><span data-stu-id="85d0e-109">Description</span></span>|  
|------------|-----------------|  
|`COR_GC_COUNTS`|<span data-ttu-id="85d0e-110">レコード生成ごとに実行されたガベージ コレクションの数。</span><span class="sxs-lookup"><span data-stu-id="85d0e-110">Records the number of garbage collections performed for each generation.</span></span>|  
|`COR_GC_MEMORYUSAGE`|<span data-ttu-id="85d0e-111">レコード メモリ使用量とガベージ コレクション サイズの統計情報。</span><span class="sxs-lookup"><span data-stu-id="85d0e-111">Records memory usage and garbage collection size statistics.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="85d0e-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="85d0e-112">Requirements</span></span>  
 <span data-ttu-id="85d0e-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="85d0e-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="85d0e-114">**ヘッダー:** GCHost.idl、GCHost.h</span><span class="sxs-lookup"><span data-stu-id="85d0e-114">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="85d0e-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="85d0e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85d0e-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="85d0e-116">See also</span></span>
- [<span data-ttu-id="85d0e-117">COR_GC_STATS 構造体</span><span class="sxs-lookup"><span data-stu-id="85d0e-117">COR_GC_STATS Structure</span></span>](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md)
- [<span data-ttu-id="85d0e-118">ホスティングの列挙型</span><span class="sxs-lookup"><span data-stu-id="85d0e-118">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
