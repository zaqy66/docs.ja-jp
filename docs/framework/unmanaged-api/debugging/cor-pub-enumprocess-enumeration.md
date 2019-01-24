---
title: COR_PUB_ENUMPROCESS 列挙型
ms.date: 03/30/2017
api_name:
- COR_PUB_ENUMPROCESS
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_PUB_ENUMPROCESS
helpviewer_keywords:
- COR_PUB_ENUMPROCESS enumeration [.NET Framework debugging]
ms.assetid: 5d3ada6e-feea-47da-a7ed-b664107c137f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bfc576e1b4f0bf1666dcd585a24dbfa398e9abde
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715856"
---
# <a name="corpubenumprocess-enumeration"></a><span data-ttu-id="d7954-102">COR_PUB_ENUMPROCESS 列挙型</span><span class="sxs-lookup"><span data-stu-id="d7954-102">COR_PUB_ENUMPROCESS Enumeration</span></span>
<span data-ttu-id="d7954-103">列挙するプロセスの型を識別します。</span><span class="sxs-lookup"><span data-stu-id="d7954-103">Identifies the type of process to be enumerated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d7954-104">構文</span><span class="sxs-lookup"><span data-stu-id="d7954-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PUB_MANAGEDONLY    = 0x00000001  
} COR_PUB_ENUMPROCESS;  
```  
  
## <a name="members"></a><span data-ttu-id="d7954-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="d7954-105">Members</span></span>  
  
|<span data-ttu-id="d7954-106">メンバー名</span><span class="sxs-lookup"><span data-stu-id="d7954-106">Member name</span></span>|<span data-ttu-id="d7954-107">説明</span><span class="sxs-lookup"><span data-stu-id="d7954-107">Description</span></span>|  
|-----------------|-----------------|  
|`COR_PUB_MANAGEDONLY`|<span data-ttu-id="d7954-108">管理対象のプロセス。</span><span class="sxs-lookup"><span data-stu-id="d7954-108">A managed process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d7954-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="d7954-109">Remarks</span></span>  
 <span data-ttu-id="d7954-110">アンマネージ デバッグ API の現在のバージョンでは、マネージ プロセスのみを列挙します。</span><span class="sxs-lookup"><span data-stu-id="d7954-110">The current version of the unmanaged debugging API enumerates only managed processes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d7954-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="d7954-111">Requirements</span></span>  
 <span data-ttu-id="d7954-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7954-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d7954-113">**ヘッダー:** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="d7954-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="d7954-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d7954-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d7954-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d7954-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d7954-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7954-116">See also</span></span>
- [<span data-ttu-id="d7954-117">列挙型のデバッグ</span><span class="sxs-lookup"><span data-stu-id="d7954-117">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
