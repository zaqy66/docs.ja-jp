---
title: CeeSectionRelocExtra 共用体
ms.date: 03/30/2017
api_name:
- CeeSectionRelocExtra Union
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CeeSectionRelocExtra
helpviewer_keywords:
- CeeSectionRelocExtra union [.NET Framework metadata]
ms.assetid: d9568cf6-7f98-4cd6-ab36-0a2bd509afcc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9d6a5673c2aaf287131274b0c590f00a69c64fed
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54517150"
---
# <a name="ceesectionrelocextra-union"></a><span data-ttu-id="80595-102">CeeSectionRelocExtra 共用体</span><span class="sxs-lookup"><span data-stu-id="80595-102">CeeSectionRelocExtra Union</span></span>
<span data-ttu-id="80595-103">によって使用されるアドレスのオフセットを表す、 [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)セクションを再配置するインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="80595-103">Represents an address offset that is used by the [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md) interface to relocate a section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80595-104">構文</span><span class="sxs-lookup"><span data-stu-id="80595-104">Syntax</span></span>  
  
```  
typedef union  {  
    USHORT highAdj;  
} CeeSectionRelocExtra;  
```  
  
## <a name="members"></a><span data-ttu-id="80595-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="80595-105">Members</span></span>  
  
|<span data-ttu-id="80595-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="80595-106">Member</span></span>|<span data-ttu-id="80595-107">説明</span><span class="sxs-lookup"><span data-stu-id="80595-107">Description</span></span>|  
|------------|-----------------|  
|`highAdj`|<span data-ttu-id="80595-108">セクションの上位アドレスを調整します。</span><span class="sxs-lookup"><span data-stu-id="80595-108">The upper address adjustment for the section.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="80595-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="80595-109">Requirements</span></span>  
 <span data-ttu-id="80595-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="80595-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="80595-111">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="80595-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="80595-112">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="80595-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="80595-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="80595-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="80595-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="80595-114">See also</span></span>
- [<span data-ttu-id="80595-115">メタデータ共用体</span><span class="sxs-lookup"><span data-stu-id="80595-115">Metadata Unions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-unions.md)
