---
title: CorSaveSize 列挙型
ms.date: 03/30/2017
api_name:
- CorSaveSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSaveSize
helpviewer_keywords:
- CorSaveSize enumeration [.NET Framework metadata]
ms.assetid: eb95ce39-5688-43c1-a34d-578794b32faa
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f756e8688299fbe9d53822851be83703f4aa6348
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54550631"
---
# <a name="corsavesize-enumeration"></a><span data-ttu-id="d8638-102">CorSaveSize 列挙型</span><span class="sxs-lookup"><span data-stu-id="d8638-102">CorSaveSize Enumeration</span></span>
<span data-ttu-id="d8638-103">保存操作のサイズの照会で要求される精度のレベルを示す値が格納されます。</span><span class="sxs-lookup"><span data-stu-id="d8638-103">Contains values indicating the level of precision required when querying for the size of a save operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8638-104">構文</span><span class="sxs-lookup"><span data-stu-id="d8638-104">Syntax</span></span>  
  
```  
typedef enum CorSaveSize {  
    cssAccurate                = 0x0000,   
    cssQuick                   = 0x0001,   
    cssDiscardTransientCAs     = 0x0002  
} CorSaveSize;  
```  
  
## <a name="members"></a><span data-ttu-id="d8638-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="d8638-105">Members</span></span>  
  
|<span data-ttu-id="d8638-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="d8638-106">Member</span></span>|<span data-ttu-id="d8638-107">説明</span><span class="sxs-lookup"><span data-stu-id="d8638-107">Description</span></span>|  
|------------|-----------------|  
|`cssAccurate`|<span data-ttu-id="d8638-108">戻り値が正確であることを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8638-108">Specifies that the return value should be exact.</span></span>|  
|`cssQuick`|<span data-ttu-id="d8638-109">戻り値を推定することを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8638-109">Specifies that the return value should be estimated.</span></span>|  
|`cssDiscardTransientCAs`|<span data-ttu-id="d8638-110">破棄できる型を削除することを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8638-110">Specifies that discardable types should be removed.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d8638-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="d8638-111">Requirements</span></span>  
 <span data-ttu-id="d8638-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8638-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8638-113">**ヘッダー:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="d8638-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="d8638-114">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="d8638-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d8638-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8638-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8638-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8638-116">See also</span></span>
- [<span data-ttu-id="d8638-117">メタデータ列挙型</span><span class="sxs-lookup"><span data-stu-id="d8638-117">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
