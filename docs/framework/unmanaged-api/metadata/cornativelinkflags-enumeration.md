---
title: CorNativeLinkFlags 列挙型
ms.date: 03/30/2017
api_name:
- CorNativeLinkFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorNativeLinkFlags
helpviewer_keywords:
- CorNativeLinkFlags enumeration [.NET Framework metadata]
ms.assetid: 8027df7c-cfad-4724-bda0-7538d9519070
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cf0fdb1e46bfbd17505e255d539547a00eb4764c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54694556"
---
# <a name="cornativelinkflags-enumeration"></a><span data-ttu-id="ad11a-102">CorNativeLinkFlags 列挙型</span><span class="sxs-lookup"><span data-stu-id="ad11a-102">CorNativeLinkFlags Enumeration</span></span>
<span data-ttu-id="ad11a-103">ネイティブ コードをリンクするときに、リンカーが使用するフラグ値を提供します。</span><span class="sxs-lookup"><span data-stu-id="ad11a-103">Provides flag values used by the linker when linking native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad11a-104">構文</span><span class="sxs-lookup"><span data-stu-id="ad11a-104">Syntax</span></span>  
  
```  
typedef enum  
{  
    nlfNone         = 0x00,  
    nlfLastError    = 0x01,  
    nlfNoMangle     = 0x02,  
    nlfMaxValue     = 0x03  
} CorNativeLinkFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="ad11a-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="ad11a-105">Members</span></span>  
  
|<span data-ttu-id="ad11a-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="ad11a-106">Member</span></span>|<span data-ttu-id="ad11a-107">説明</span><span class="sxs-lookup"><span data-stu-id="ad11a-107">Description</span></span>|  
|------------|-----------------|  
|`nlfNone`|<span data-ttu-id="ad11a-108">フラグがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="ad11a-108">Indicates no flags.</span></span>|  
|`nlfLastError`|<span data-ttu-id="ad11a-109">示す、`setLastError`キーワード。</span><span class="sxs-lookup"><span data-stu-id="ad11a-109">Indicates a `setLastError` keyword.</span></span>|  
|`nlfNoMangle`|<span data-ttu-id="ad11a-110">示す、`nomangle`キーワード。</span><span class="sxs-lookup"><span data-stu-id="ad11a-110">Indicates a `nomangle` keyword.</span></span>|  
|`nlfMaxValue`|<span data-ttu-id="ad11a-111">使用しません。</span><span class="sxs-lookup"><span data-stu-id="ad11a-111">Not used.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ad11a-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="ad11a-112">Requirements</span></span>  
 <span data-ttu-id="ad11a-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad11a-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ad11a-114">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ad11a-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ad11a-115">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="ad11a-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ad11a-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ad11a-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad11a-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad11a-117">See also</span></span>
- [<span data-ttu-id="ad11a-118">メタデータ列挙型</span><span class="sxs-lookup"><span data-stu-id="ad11a-118">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
