---
title: CorPropertyAttr 列挙型
ms.date: 03/30/2017
api_name:
- CorPropertyAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorPropertyAttr
helpviewer_keywords:
- CorPropertyAttr enumeration [.NET Framework metadata]
ms.assetid: 58ac8202-854d-4efd-acfb-d2da8b446e12
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 713913fa046fc1bef12b8849ac82e4399a8dc534
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577581"
---
# <a name="corpropertyattr-enumeration"></a><span data-ttu-id="3486a-102">CorPropertyAttr 列挙型</span><span class="sxs-lookup"><span data-stu-id="3486a-102">CorPropertyAttr Enumeration</span></span>
<span data-ttu-id="3486a-103">プロパティのメタデータを記述する値が格納されます。</span><span class="sxs-lookup"><span data-stu-id="3486a-103">Contains values that describe the metadata of a property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3486a-104">構文</span><span class="sxs-lookup"><span data-stu-id="3486a-104">Syntax</span></span>  
  
```  
typedef enum CorPropertyAttr {  
  
    prSpecialName           =   0x0200,   
    prReservedMask          =   0xf400,  
    prRTSpecialName         =   0x0400,  
    prHasDefault            =   0x1000,  
    prUnused                =   0xe9ff  
  
} CorPropertyAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="3486a-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="3486a-105">Members</span></span>  
  
|<span data-ttu-id="3486a-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="3486a-106">Member</span></span>|<span data-ttu-id="3486a-107">説明</span><span class="sxs-lookup"><span data-stu-id="3486a-107">Description</span></span>|  
|------------|-----------------|  
|`prSpecialName`|<span data-ttu-id="3486a-108">プロパティが、特別なであると、その名前を記述しているを指定しますか。</span><span class="sxs-lookup"><span data-stu-id="3486a-108">Specifies that the property is special, and that its name describes how.</span></span>|  
|`prReservedMask`|<span data-ttu-id="3486a-109">共通言語ランタイムでは、内部使用のため予約されています。</span><span class="sxs-lookup"><span data-stu-id="3486a-109">Reserved for internal use by the common language runtime.</span></span>|  
|`prRTSpecialName`|<span data-ttu-id="3486a-110">共通言語ランタイム メタデータの内部 Api がプロパティ名のエンコードを確認する必要がありますを指定します。</span><span class="sxs-lookup"><span data-stu-id="3486a-110">Specifies that the common language runtime metadata internal APIs should check the encoding of the property name.</span></span>|  
|`prHasDefault`|<span data-ttu-id="3486a-111">既定値を持つプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="3486a-111">Specifies that the property has a default value.</span></span>|  
|`prUnused`|<span data-ttu-id="3486a-112">使用されません。</span><span class="sxs-lookup"><span data-stu-id="3486a-112">Unused.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3486a-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="3486a-113">Requirements</span></span>  
 <span data-ttu-id="3486a-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3486a-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3486a-115">**ヘッダー:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="3486a-115">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="3486a-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3486a-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3486a-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="3486a-117">See also</span></span>
- [<span data-ttu-id="3486a-118">メタデータ列挙型</span><span class="sxs-lookup"><span data-stu-id="3486a-118">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
