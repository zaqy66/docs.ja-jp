---
title: CorManifestResourceFlags 列挙型
ms.date: 03/30/2017
api_name:
- CorManifestResourceFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorManifestResourceFlags
helpviewer_keywords:
- CorManifestResourceFlags enumeration [.NET Framework metadata]
ms.assetid: 1b0306b7-622b-4b57-8edc-3c713bb147ae
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a3d3ef78da9dd639d0f9050a8b61d1e365cd8b42
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54650250"
---
# <a name="cormanifestresourceflags-enumeration"></a><span data-ttu-id="0bdbf-102">CorManifestResourceFlags 列挙型</span><span class="sxs-lookup"><span data-stu-id="0bdbf-102">CorManifestResourceFlags Enumeration</span></span>
<span data-ttu-id="0bdbf-103">アセンブリ マニフェストでエンコードされているリソースの可視性を示します。</span><span class="sxs-lookup"><span data-stu-id="0bdbf-103">Indicates the visibility of resources encoded in an assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0bdbf-104">構文</span><span class="sxs-lookup"><span data-stu-id="0bdbf-104">Syntax</span></span>  
  
```  
typedef enum CorManifestResourceFlags {  
  
    mrVisibilityMask        =   0x0007,  
    mrPublic                =   0x0001,  
    mrPrivate               =   0x0002  
  
} CorManifestResourceFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="0bdbf-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="0bdbf-105">Members</span></span>  
  
|<span data-ttu-id="0bdbf-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="0bdbf-106">Member</span></span>|<span data-ttu-id="0bdbf-107">説明</span><span class="sxs-lookup"><span data-stu-id="0bdbf-107">Description</span></span>|  
|------------|-----------------|  
|`mrVisibilityMask`|<span data-ttu-id="0bdbf-108">予約済み。</span><span class="sxs-lookup"><span data-stu-id="0bdbf-108">Reserved.</span></span>|  
|`mrPublic`|<span data-ttu-id="0bdbf-109">リソースはパブリックです。</span><span class="sxs-lookup"><span data-stu-id="0bdbf-109">The resources are public.</span></span>|  
|`mrPrivate`|<span data-ttu-id="0bdbf-110">リソースはプライベートです。</span><span class="sxs-lookup"><span data-stu-id="0bdbf-110">The resources are private.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0bdbf-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="0bdbf-111">Requirements</span></span>  
 <span data-ttu-id="0bdbf-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bdbf-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0bdbf-113">**ヘッダー:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="0bdbf-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="0bdbf-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0bdbf-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0bdbf-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="0bdbf-115">See also</span></span>
- [<span data-ttu-id="0bdbf-116">メタデータ列挙型</span><span class="sxs-lookup"><span data-stu-id="0bdbf-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
