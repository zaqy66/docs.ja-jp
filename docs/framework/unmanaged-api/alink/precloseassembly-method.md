---
title: PreCloseAssembly メソッド
ms.date: 03/30/2017
api_name:
- IALink.PreCloseAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- PreCloseAssembly
helpviewer_keywords:
- PreCloseAssembly method
ms.assetid: 6d23ac54-15ea-4027-a172-9ebef43e8f56
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6fab522adbdb1b50448dfabfd23d663fb223c6da
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499198"
---
# <a name="precloseassembly-method"></a><span data-ttu-id="6d439-102">PreCloseAssembly メソッド</span><span class="sxs-lookup"><span data-stu-id="6d439-102">PreCloseAssembly Method</span></span>
<span data-ttu-id="6d439-103">アセンブリ ファイルを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6d439-103">Closes the assembly file.</span></span> <span data-ttu-id="6d439-104">その他のすべてのファイルを閉じた後がアセンブリ ファイルを閉じる前に、このメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6d439-104">Call this method after closing all other files, but before closing the assembly file.</span></span> <span data-ttu-id="6d439-105">非バインド モジュールのこのメソッドを呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="6d439-105">Do not call this method for unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6d439-106">構文</span><span class="sxs-lookup"><span data-stu-id="6d439-106">Syntax</span></span>  
  
```  
HRESULT PreCloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6d439-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6d439-107">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="6d439-108">アセンブリの ID。</span><span class="sxs-lookup"><span data-stu-id="6d439-108">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6d439-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="6d439-109">Return Value</span></span>  
 <span data-ttu-id="6d439-110">メソッドが成功した場合は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="6d439-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6d439-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="6d439-111">Requirements</span></span>  
 <span data-ttu-id="6d439-112">Alink.h が必要です。</span><span class="sxs-lookup"><span data-stu-id="6d439-112">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d439-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="6d439-113">See also</span></span>
- [<span data-ttu-id="6d439-114">IALink インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6d439-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="6d439-115">IALink2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6d439-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="6d439-116">ALink API</span><span class="sxs-lookup"><span data-stu-id="6d439-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
