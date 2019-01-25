---
title: CorThreadSafetyOptions 列挙型
ms.date: 03/30/2017
api_name:
- CorThreadSafetyOptions
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorThreadSafetyOptions
helpviewer_keywords:
- CorThreadSafetyOptions enumeration [.NET Framework metadata]
ms.assetid: dae07d9b-df51-488c-b17e-52d6e48217bd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b460c2c4b0d38ec46ee9d7341de9b320a2ecaa7e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54594643"
---
# <a name="corthreadsafetyoptions-enumeration"></a><span data-ttu-id="3fe65-102">CorThreadSafetyOptions 列挙型</span><span class="sxs-lookup"><span data-stu-id="3fe65-102">CorThreadSafetyOptions Enumeration</span></span>
<span data-ttu-id="3fe65-103">スレッド セーフのオプションを選択するためのフラグを指定します。</span><span class="sxs-lookup"><span data-stu-id="3fe65-103">Specifies flags to select options for thread safety.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3fe65-104">構文</span><span class="sxs-lookup"><span data-stu-id="3fe65-104">Syntax</span></span>  
  
```  
typedef enum CorThreadSafetyOptions {  
    MDThreadSafetyDefault       = 0x00000000,  
    MDThreadSafetyOff           = 0x00000000,  
    MDThreadSafetyOn            = 0x00000001,  
} CorThreadSafetyOptions;  
```  
  
## <a name="members"></a><span data-ttu-id="3fe65-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="3fe65-105">Members</span></span>  
  
|<span data-ttu-id="3fe65-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="3fe65-106">Member</span></span>|<span data-ttu-id="3fe65-107">説明</span><span class="sxs-lookup"><span data-stu-id="3fe65-107">Description</span></span>|  
|------------|-----------------|  
|`MDThreadSatetyDefault`|<span data-ttu-id="3fe65-108">既定値です。</span><span class="sxs-lookup"><span data-stu-id="3fe65-108">Default value.</span></span> <span data-ttu-id="3fe65-109">`MDThreadSatetyOff` と同じ。</span><span class="sxs-lookup"><span data-stu-id="3fe65-109">Same as `MDThreadSatetyOff`.</span></span>|  
|`MDThreadSatetyOff`|<span data-ttu-id="3fe65-110">読み取り/書き込みロックを設定できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="3fe65-110">Indicates that a reader/writer lock cannot be set.</span></span>|  
|`MDThreadSatetyOn`|<span data-ttu-id="3fe65-111">読み取り/書き込みロックを設定できることを示します。</span><span class="sxs-lookup"><span data-stu-id="3fe65-111">Indicates that a reader/writer lock can be set.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3fe65-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="3fe65-112">Requirements</span></span>  
 <span data-ttu-id="3fe65-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3fe65-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3fe65-114">**ヘッダー:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="3fe65-114">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="3fe65-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3fe65-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3fe65-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="3fe65-116">See also</span></span>
- [<span data-ttu-id="3fe65-117">メタデータ列挙型</span><span class="sxs-lookup"><span data-stu-id="3fe65-117">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
