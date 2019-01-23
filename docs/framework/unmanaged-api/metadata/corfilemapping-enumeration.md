---
title: CorFileMapping 列挙体
ms.date: 03/30/2017
api_name:
- CorFileMapping
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorFileMapping
helpviewer_keywords:
- CorFileMapping enumeration [.NET Framework metadata]
ms.assetid: 3ca41592-b8da-475a-8032-a15627730003
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e9b3802c9c72ec3a9302e403e55789aab8102cf1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624991"
---
# <a name="corfilemapping-enumeration"></a><span data-ttu-id="c294a-102">CorFileMapping 列挙体</span><span class="sxs-lookup"><span data-stu-id="c294a-102">CorFileMapping Enumeration</span></span>
<span data-ttu-id="c294a-103">呼び出しから返されるファイル マッピングの種類を記述する値が含まれています、 [imetadatainfo::getfilemapping](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="c294a-103">Contains values that describe the type of file mapping that is returned from a call to the [IMetaDataInfo::GetFileMapping](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c294a-104">構文</span><span class="sxs-lookup"><span data-stu-id="c294a-104">Syntax</span></span>  
  
```  
typedef enum CorFileMapping {  
  
    fmFlat                  =   0x0000,  
    fmExecutableImage       =   0x0001  
  
} CorFileMapping;  
```  
  
## <a name="members"></a><span data-ttu-id="c294a-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="c294a-105">Members</span></span>  
  
|<span data-ttu-id="c294a-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="c294a-106">Member</span></span>|<span data-ttu-id="c294a-107">説明</span><span class="sxs-lookup"><span data-stu-id="c294a-107">Description</span></span>|  
|------------|-----------------|  
|`fmFlat`|<span data-ttu-id="c294a-108">ファイルは、データ ファイルとしてマップされます。</span><span class="sxs-lookup"><span data-stu-id="c294a-108">The file is mapped as a data file.</span></span> <span data-ttu-id="c294a-109">つまり、`SEC_IMAGE`フラグは、Microsoft Win32 に渡されなかった`CreateFileMapping`関数。</span><span class="sxs-lookup"><span data-stu-id="c294a-109">That is, the `SEC_IMAGE` flag was not passed to the Microsoft Win32 `CreateFileMapping` function.</span></span>|  
|`fmExecutableImage`|<span data-ttu-id="c294a-110">いずれかを使用して、実行するため、ファイルがマップされている、`LoadLibrary`関数または`CreateFileMapping`関数と、`SEC_IMAGE`フラグ。</span><span class="sxs-lookup"><span data-stu-id="c294a-110">The file is mapped for execution, by using either the `LoadLibrary` function or the `CreateFileMapping` function with the `SEC_IMAGE` flag.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c294a-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="c294a-111">Requirements</span></span>  
 <span data-ttu-id="c294a-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c294a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c294a-113">**ヘッダー:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="c294a-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="c294a-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c294a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c294a-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="c294a-115">See also</span></span>
- [<span data-ttu-id="c294a-116">メタデータ列挙型</span><span class="sxs-lookup"><span data-stu-id="c294a-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
- [<span data-ttu-id="c294a-117">GetFileMapping メソッド</span><span class="sxs-lookup"><span data-stu-id="c294a-117">GetFileMapping Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md)
