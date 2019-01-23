---
title: ISymUnmanagedSymbolSearchInfo インターフェイス
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo
helpviewer_keywords:
- ISymUnmanagedSymbolSearchInfo interface [.NET Framework debugging]
ms.assetid: 30817373-0a21-49c1-a0c4-8e8daeecb8db
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8f5fc951b629a3158fc2c2d6047234fb661f3741
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54494900"
---
# <a name="isymunmanagedsymbolsearchinfo-interface"></a><span data-ttu-id="5765a-102">ISymUnmanagedSymbolSearchInfo インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5765a-102">ISymUnmanagedSymbolSearchInfo Interface</span></span>
<span data-ttu-id="5765a-103">検索パスに関する情報を取得するメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="5765a-103">Provides methods that get information about the search path.</span></span> <span data-ttu-id="5765a-104">このインターフェイスを呼び出すことによって取得`QueryInterface`を実装するオブジェクトで、 [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="5765a-104">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5765a-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="5765a-105">Methods</span></span>  
  
|<span data-ttu-id="5765a-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="5765a-106">Method</span></span>|<span data-ttu-id="5765a-107">説明</span><span class="sxs-lookup"><span data-stu-id="5765a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5765a-108">GetHRESULT メソッド</span><span class="sxs-lookup"><span data-stu-id="5765a-108">GetHRESULT Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-gethresult-method.md)|<span data-ttu-id="5765a-109">HRESULT を取得します。</span><span class="sxs-lookup"><span data-stu-id="5765a-109">Gets the HRESULT.</span></span>|  
|[<span data-ttu-id="5765a-110">GetSearchPath メソッド</span><span class="sxs-lookup"><span data-stu-id="5765a-110">GetSearchPath Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-getsearchpath-method.md)|<span data-ttu-id="5765a-111">検索パスを取得します。</span><span class="sxs-lookup"><span data-stu-id="5765a-111">Gets the search path.</span></span>|  
|[<span data-ttu-id="5765a-112">GetSearchPathLength メソッド</span><span class="sxs-lookup"><span data-stu-id="5765a-112">GetSearchPathLength Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-getsearchpathlength-method.md)|<span data-ttu-id="5765a-113">検索パスの長さを取得します。</span><span class="sxs-lookup"><span data-stu-id="5765a-113">Gets the search path length.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5765a-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="5765a-114">Requirements</span></span>  
 <span data-ttu-id="5765a-115">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="5765a-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5765a-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="5765a-116">See also</span></span>
- [<span data-ttu-id="5765a-117">シンボル ストア診断インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5765a-117">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
