---
title: CloseAssembly メソッド
ms.date: 03/30/2017
api_name:
- IALink.CloseAssembly
- CloseAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- CloseAssembly
helpviewer_keywords:
- CloseAssembly method
ms.assetid: f66a43bc-a5c5-4190-acbe-63fd27640634
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: aa415926f4a818f697812f1a3c5531cb0ab7081b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54510170"
---
# <a name="closeassembly-method"></a><span data-ttu-id="25d7d-102">CloseAssembly メソッド</span><span class="sxs-lookup"><span data-stu-id="25d7d-102">CloseAssembly Method</span></span>
<span data-ttu-id="25d7d-103">アセンブリの操作を終了します。</span><span class="sxs-lookup"><span data-stu-id="25d7d-103">Finalizes assembly operations.</span></span> <span data-ttu-id="25d7d-104">新しいアセンブリまたはバインドされていないモジュールを開始する前に、このメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="25d7d-104">Call this method before beginning a new assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="25d7d-105">構文</span><span class="sxs-lookup"><span data-stu-id="25d7d-105">Syntax</span></span>  
  
```  
HRESULT CloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="25d7d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="25d7d-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="25d7d-107">アセンブリの ID。</span><span class="sxs-lookup"><span data-stu-id="25d7d-107">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="25d7d-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="25d7d-108">Return Value</span></span>  
 <span data-ttu-id="25d7d-109">メソッドが成功した場合は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="25d7d-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="25d7d-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="25d7d-110">Requirements</span></span>  
 <span data-ttu-id="25d7d-111">Alink.h が必要です。</span><span class="sxs-lookup"><span data-stu-id="25d7d-111">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25d7d-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="25d7d-112">See also</span></span>
- [<span data-ttu-id="25d7d-113">IALink インターフェイス</span><span class="sxs-lookup"><span data-stu-id="25d7d-113">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="25d7d-114">IALink2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="25d7d-114">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="25d7d-115">ALink API</span><span class="sxs-lookup"><span data-stu-id="25d7d-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
