---
title: CorFileFlags 列挙型
ms.date: 03/30/2017
api_name:
- CorFileFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorFileFlags
helpviewer_keywords:
- CorFileFlags enumeration [.NET Framework metadata]
ms.assetid: d16703fd-518f-412e-92cb-74433d11032e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8a614ad1bd9738c993775667ccd261a089e8b57a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624263"
---
# <a name="corfileflags-enumeration"></a><span data-ttu-id="d6f5c-102">CorFileFlags 列挙型</span><span class="sxs-lookup"><span data-stu-id="d6f5c-102">CorFileFlags Enumeration</span></span>
<span data-ttu-id="d6f5c-103">呼び出しで定義されているファイルの種類を記述する値を含む[imetadataassemblyemit::definefile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md)します。</span><span class="sxs-lookup"><span data-stu-id="d6f5c-103">Contains values that describe the type of file defined in a call to [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6f5c-104">構文</span><span class="sxs-lookup"><span data-stu-id="d6f5c-104">Syntax</span></span>  
  
```  
typedef enum CorFileFlags {  
  
    ffContainsMetaData      =   0x0000,  
    ffContainsNoMetaData    =   0x0001  
  
} CorFileFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="d6f5c-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="d6f5c-105">Members</span></span>  
  
|<span data-ttu-id="d6f5c-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="d6f5c-106">Member</span></span>|<span data-ttu-id="d6f5c-107">説明</span><span class="sxs-lookup"><span data-stu-id="d6f5c-107">Description</span></span>|  
|------------|-----------------|  
|`ffContainsMetaData`|<span data-ttu-id="d6f5c-108">ファイルがリソース ファイルではないことを示します。</span><span class="sxs-lookup"><span data-stu-id="d6f5c-108">Indicates that the file is not a resource file.</span></span>|  
|`ffContainsNoMetaData`|<span data-ttu-id="d6f5c-109">場合によっては、リソース ファイル、ファイルにメタデータが含まれていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="d6f5c-109">Indicates that the file, possibly a resource file, does not contain metadata.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d6f5c-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="d6f5c-110">Requirements</span></span>  
 <span data-ttu-id="d6f5c-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6f5c-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d6f5c-112">**ヘッダー:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="d6f5c-112">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="d6f5c-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d6f5c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6f5c-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6f5c-114">See also</span></span>
- [<span data-ttu-id="d6f5c-115">メタデータ列挙型</span><span class="sxs-lookup"><span data-stu-id="d6f5c-115">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
