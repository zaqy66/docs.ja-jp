---
title: CorParamAttr 列挙型
ms.date: 03/30/2017
api_name:
- CorParamAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorParamAttr
helpviewer_keywords:
- CorParamAttr enumeration [.NET Framework metadata]
ms.assetid: a7ff90ad-dad8-48e8-917d-4aa9a118cbc8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7d07c6de47038d5c52d76ad8ca8e0a5684551d59
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491468"
---
# <a name="corparamattr-enumeration"></a><span data-ttu-id="07b47-102">CorParamAttr 列挙型</span><span class="sxs-lookup"><span data-stu-id="07b47-102">CorParamAttr Enumeration</span></span>
<span data-ttu-id="07b47-103">メソッド パラメーターのメタデータを記述する値が格納されます。</span><span class="sxs-lookup"><span data-stu-id="07b47-103">Contains values that describe the metadata of a method parameter.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07b47-104">構文</span><span class="sxs-lookup"><span data-stu-id="07b47-104">Syntax</span></span>  
  
```  
typedef enum CorParamAttr {  
  
    pdIn                        =   0x0001,  
    pdOut                       =   0x0002,  
    pdOptional                  =   0x0010,  
  
    pdReservedMask              =   0xf000,  
    pdHasDefault                =   0x1000,  
    pdHasFieldMarshal           =   0x2000,  
  
    pdUnused                    =   0xcfe0  
  
} CorParamAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="07b47-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="07b47-105">Members</span></span>  
  
|<span data-ttu-id="07b47-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="07b47-106">Member</span></span>|<span data-ttu-id="07b47-107">説明</span><span class="sxs-lookup"><span data-stu-id="07b47-107">Description</span></span>|  
|------------|-----------------|  
|`pdIn`|<span data-ttu-id="07b47-108">パラメーターがメソッドの呼び出しに渡されることを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b47-108">Specifies that the parameter is passed into the method call.</span></span>|  
|`pdOut`|<span data-ttu-id="07b47-109">パラメーターが渡されること、メソッドから戻り値を指定します。</span><span class="sxs-lookup"><span data-stu-id="07b47-109">Specifies that the parameter is passed from the method return.</span></span>|  
|`pdOptional`|<span data-ttu-id="07b47-110">パラメーターが省略可能なことを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b47-110">Specifies that the parameter is optional.</span></span>|  
|`pdReservedMask`|<span data-ttu-id="07b47-111">共通言語ランタイムでは、内部使用のため予約されています。</span><span class="sxs-lookup"><span data-stu-id="07b47-111">Reserved for internal use by the common language runtime.</span></span>|  
|`pdHasDefault`|<span data-ttu-id="07b47-112">パラメーターの既定値を指定します。</span><span class="sxs-lookup"><span data-stu-id="07b47-112">Specifies that the parameter has a default value.</span></span>|  
|`pdHasFieldMarshal`|<span data-ttu-id="07b47-113">パラメーターがマーシャ リング情報を使用することを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b47-113">Specifies that the parameter has marshaling information.</span></span>|  
|`pdUnused`|<span data-ttu-id="07b47-114">使用されません。</span><span class="sxs-lookup"><span data-stu-id="07b47-114">Unused.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="07b47-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="07b47-115">Requirements</span></span>  
 <span data-ttu-id="07b47-116">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="07b47-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="07b47-117">**ヘッダー:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="07b47-117">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="07b47-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="07b47-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07b47-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="07b47-119">See also</span></span>
- [<span data-ttu-id="07b47-120">メタデータ列挙型</span><span class="sxs-lookup"><span data-stu-id="07b47-120">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
