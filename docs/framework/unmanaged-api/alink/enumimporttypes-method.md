---
title: EnumImportTypes メソッド
ms.date: 03/30/2017
api_name:
- EnumImportTypes
- IALink.EnumImportTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EnumImportTypes
helpviewer_keywords:
- EnumImportTypes method
ms.assetid: 83a0e4e7-ec06-40cb-9b63-700b9695bb04
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4e437868138d7ae31d233853ecc0f709de3ee39d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54512724"
---
# <a name="enumimporttypes-method"></a><span data-ttu-id="a6fb2-102">EnumImportTypes メソッド</span><span class="sxs-lookup"><span data-stu-id="a6fb2-102">EnumImportTypes Method</span></span>
<span data-ttu-id="a6fb2-103">それぞれのスコープでは、各種類を列挙します。</span><span class="sxs-lookup"><span data-stu-id="a6fb2-103">Enumerates each type in each scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6fb2-104">構文</span><span class="sxs-lookup"><span data-stu-id="a6fb2-104">Syntax</span></span>  
  
```  
HRESULT EnumImportTypes(  
    HALINKENUM   hEnum,  
    DWORD        dwMax,  
    mdTypeDef    aTypeDefs[],  
    DWORD*       pdwCount  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a6fb2-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a6fb2-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="a6fb2-106">列挙子の処理です。</span><span class="sxs-lookup"><span data-stu-id="a6fb2-106">Handle for enumerator.</span></span>  
  
 `dwMax`  
 <span data-ttu-id="a6fb2-107">取得する型の最大数。</span><span class="sxs-lookup"><span data-stu-id="a6fb2-107">Maximum number of types to retrieve.</span></span>  
  
 `aTypeDefs`  
 <span data-ttu-id="a6fb2-108">型を超えないように、トークンを受け取ります`dwMax`します。</span><span class="sxs-lookup"><span data-stu-id="a6fb2-108">Recieves type tokens, not to exceed `dwMax`.</span></span>  
  
 `pdwCount`  
 <span data-ttu-id="a6fb2-109">型の実際の数を受け取る`aTypeDefs`します。</span><span class="sxs-lookup"><span data-stu-id="a6fb2-109">Receives actual number of type in `aTypeDefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a6fb2-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="a6fb2-110">Return Value</span></span>  
 <span data-ttu-id="a6fb2-111">メソッドが成功した場合は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="a6fb2-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a6fb2-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="a6fb2-112">Requirements</span></span>  
 <span data-ttu-id="a6fb2-113">Alink.h が必要です。</span><span class="sxs-lookup"><span data-stu-id="a6fb2-113">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6fb2-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6fb2-114">See also</span></span>
- [<span data-ttu-id="a6fb2-115">IALink インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a6fb2-115">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="a6fb2-116">IALink2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a6fb2-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="a6fb2-117">ALink API</span><span class="sxs-lookup"><span data-stu-id="a6fb2-117">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
