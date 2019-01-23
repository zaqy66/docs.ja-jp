---
title: AssemblyRefFlags 列挙型
ms.date: 03/30/2017
api_name:
- AssemblyRefFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- AssemblyRefFlags
helpviewer_keywords:
- AssemblyRefFlags enumeration [.NET Framework metadata]
ms.assetid: decd4f46-f3b2-466f-9501-e74f2b86b846
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b31df454c49ddccc74a7e877c09efa4f45b69d9e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491795"
---
# <a name="assemblyrefflags-enumeration"></a><span data-ttu-id="0946b-102">AssemblyRefFlags 列挙型</span><span class="sxs-lookup"><span data-stu-id="0946b-102">AssemblyRefFlags Enumeration</span></span>
<span data-ttu-id="0946b-103">アセンブリ参照の機能を記述する値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0946b-103">Contains values that describe features of an assembly reference.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0946b-104">構文</span><span class="sxs-lookup"><span data-stu-id="0946b-104">Syntax</span></span>  
  
```  
typedef enum {  
    arfFullOriginator = 0x0001  
} AssemblyRefFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="0946b-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="0946b-105">Members</span></span>  
  
|<span data-ttu-id="0946b-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="0946b-106">Member</span></span>|<span data-ttu-id="0946b-107">説明</span><span class="sxs-lookup"><span data-stu-id="0946b-107">Description</span></span>|  
|------------|-----------------|  
|`arfFullOriginator`|<span data-ttu-id="0946b-108">アセンブリ参照にはアセンブリの発行者に関する完全なハッシュされていない情報が含まれているを指定します。</span><span class="sxs-lookup"><span data-stu-id="0946b-108">Specifies that the assembly reference contains full, unhashed information about the publisher of the assembly.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0946b-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="0946b-109">Requirements</span></span>  
 <span data-ttu-id="0946b-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0946b-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0946b-111">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="0946b-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0946b-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0946b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0946b-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="0946b-113">See also</span></span>
- [<span data-ttu-id="0946b-114">メタデータ列挙型</span><span class="sxs-lookup"><span data-stu-id="0946b-114">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
- [<span data-ttu-id="0946b-115">IMetaDataAssemblyEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0946b-115">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
- [<span data-ttu-id="0946b-116">DefineAssemblyRef メソッド</span><span class="sxs-lookup"><span data-stu-id="0946b-116">DefineAssemblyRef Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassemblyref-method.md)
