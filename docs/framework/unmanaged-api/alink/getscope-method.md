---
title: GetScope Method1
ms.date: 03/30/2017
api_name:
- IALink.GetScope
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetScope
helpviewer_keywords:
- GetScope method
ms.assetid: e1555328-2c71-4ece-b357-9eb6d3a8efc4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 782697536f5e01fa29830a64e47d960a47fe4eae
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663142"
---
# <a name="getscope-method1"></a><span data-ttu-id="e4dc9-102">GetScope Method1</span><span class="sxs-lookup"><span data-stu-id="e4dc9-102">GetScope Method1</span></span>
<span data-ttu-id="e4dc9-103">インポート スコープを取得します。</span><span class="sxs-lookup"><span data-stu-id="e4dc9-103">Gets an import scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4dc9-104">構文</span><span class="sxs-lookup"><span data-stu-id="e4dc9-104">Syntax</span></span>  
  
```  
HRESULT GetScope(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    IMetaDataImport** ppImportScope  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e4dc9-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e4dc9-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="e4dc9-106">インポート先のアセンブリの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="e4dc9-106">Unique ID of assembly to import to.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="e4dc9-107">インポートするファイルの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="e4dc9-107">Unique ID of the file to import from.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="e4dc9-108">インポートする 0 から始まるスコープです。</span><span class="sxs-lookup"><span data-stu-id="e4dc9-108">Zero-based scope to import.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="e4dc9-109">受信[IMetaDataImport インターフェイス](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)スコープのインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="e4dc9-109">Receives [IMetaDataImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) interface for the scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e4dc9-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="e4dc9-110">Return Value</span></span>  
 <span data-ttu-id="e4dc9-111">メソッドが成功した場合は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="e4dc9-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4dc9-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="e4dc9-112">Requirements</span></span>  
 <span data-ttu-id="e4dc9-113">Alink.h が必要です。</span><span class="sxs-lookup"><span data-stu-id="e4dc9-113">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4dc9-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4dc9-114">See also</span></span>
- [<span data-ttu-id="e4dc9-115">IALink インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e4dc9-115">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="e4dc9-116">IALink2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e4dc9-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="e4dc9-117">ALink API</span><span class="sxs-lookup"><span data-stu-id="e4dc9-117">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
