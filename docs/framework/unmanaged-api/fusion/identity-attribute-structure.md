---
title: IDENTITY_ATTRIBUTE 構造体
ms.date: 03/30/2017
api_name:
- IDENTITY_ATTRIBUTE
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IDENTITY_ATTRIBUTE
helpviewer_keywords:
- IDENTITY_ATTRIBUTE structure [.NET Framework fusion]
ms.assetid: 1ee7c434-9681-4fa8-badd-652cb1a9742b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e26a90b6725d53774053293c04842b761da6ab12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54717676"
---
# <a name="identityattribute-structure"></a><span data-ttu-id="5d49b-102">IDENTITY_ATTRIBUTE 構造体</span><span class="sxs-lookup"><span data-stu-id="5d49b-102">IDENTITY_ATTRIBUTE Structure</span></span>
<span data-ttu-id="5d49b-103">メタデータ属性について説明する[IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md)インスタンス。</span><span class="sxs-lookup"><span data-stu-id="5d49b-103">Contains metadata attribute information about an [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5d49b-104">構文</span><span class="sxs-lookup"><span data-stu-id="5d49b-104">Syntax</span></span>  
  
```  
typedef struct _IDENTITY_ATTRIBUTE {  
    LPCWSTR  pszNamespace;  
    LPCWSTR  pszName;  
    LPCWSTR  pszValue;  
} IDENTITY_ATTRIBUTE;  
```  
  
## <a name="members"></a><span data-ttu-id="5d49b-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="5d49b-105">Members</span></span>  
  
|<span data-ttu-id="5d49b-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="5d49b-106">Member</span></span>|<span data-ttu-id="5d49b-107">説明</span><span class="sxs-lookup"><span data-stu-id="5d49b-107">Description</span></span>|  
|------------|-----------------|  
|`pszNamespace`|<span data-ttu-id="5d49b-108">属性はで、名前空間を含む null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5d49b-108">A pointer to a null-terminated character string that contains the namespace the attribute is in.</span></span>|  
|`pszName`|<span data-ttu-id="5d49b-109">属性の名前を含む null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5d49b-109">A pointer to a null-terminated character string that contains the name of the attribute.</span></span>|  
|`pszValue`|<span data-ttu-id="5d49b-110">属性の値を含む null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5d49b-110">A pointer to a null-terminated character string that contains the value of the attribute.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5d49b-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="5d49b-111">Remarks</span></span>  
 <span data-ttu-id="5d49b-112">`IDENTITY_ATTRIBUTE`構造体が null で終わる文字列への 3 つのポインターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5d49b-112">The `IDENTITY_ATTRIBUTE` structure contains three pointers to null-terminated character strings.</span></span> <span data-ttu-id="5d49b-113">これら 3 つの文字列には、1 つの属性について説明します。</span><span class="sxs-lookup"><span data-stu-id="5d49b-113">These three strings describe one attribute.</span></span>  
  
 <span data-ttu-id="5d49b-114">インスタンス、`IDENTITY_ATTRIBUTE`構造のインスタンスに関連付け、 [IDENTITY_ATTRIBUTE_BLOB](../../../../docs/framework/unmanaged-api/fusion/identity-attribute-blob-structure.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="5d49b-114">An instance of an `IDENTITY_ATTRIBUTE` structure is associated with an instance of an [IDENTITY_ATTRIBUTE_BLOB](../../../../docs/framework/unmanaged-api/fusion/identity-attribute-blob-structure.md) structure.</span></span> <span data-ttu-id="5d49b-115">`IDENTITY_ATTRIBUTE`実際の文字列と、対応する構造に含まれる`IDENTITY_ATTRIBUTE_BLOB`構造で表示されている 3 つの文字列にオフセットを一覧表示、`IDENTITY_ATTRIBUTE`構造体。</span><span class="sxs-lookup"><span data-stu-id="5d49b-115">The `IDENTITY_ATTRIBUTE` structure contains the actual strings, and the corresponding `IDENTITY_ATTRIBUTE_BLOB` structure lists the offsets to the three strings listed in the `IDENTITY_ATTRIBUTE` structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5d49b-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="5d49b-116">Requirements</span></span>  
 <span data-ttu-id="5d49b-117">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d49b-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5d49b-118">**ヘッダー:** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="5d49b-118">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="5d49b-119">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5d49b-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d49b-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d49b-120">See also</span></span>
- [<span data-ttu-id="5d49b-121">IDefinitionIdentity インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5d49b-121">IDefinitionIdentity Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md)
- [<span data-ttu-id="5d49b-122">IDENTITY_ATTRIBUTE_BLOB 構造体</span><span class="sxs-lookup"><span data-stu-id="5d49b-122">IDENTITY_ATTRIBUTE_BLOB Structure</span></span>](../../../../docs/framework/unmanaged-api/fusion/identity-attribute-blob-structure.md)
- [<span data-ttu-id="5d49b-123">Fusion 構造体</span><span class="sxs-lookup"><span data-stu-id="5d49b-123">Fusion Structures</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-structures.md)
