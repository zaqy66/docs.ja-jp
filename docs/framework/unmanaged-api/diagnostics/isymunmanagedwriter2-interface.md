---
title: ISymUnmanagedWriter2 インターフェイス
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2
helpviewer_keywords:
- ISymUnmanagedWriter2 interface [.NET Framework debugging]
ms.assetid: 8e78faa4-cf43-44fb-a91d-94d6df692a25
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 99e8b8bbb25bc55c7d4f2f44aac8e24210d30b83
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54560550"
---
# <a name="isymunmanagedwriter2-interface"></a><span data-ttu-id="8d2df-102">ISymUnmanagedWriter2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8d2df-102">ISymUnmanagedWriter2 Interface</span></span>
<span data-ttu-id="8d2df-103">シンボル ライターを表し、ドキュメント、シーケンス ポイント、構文のスコープ、および変数を定義するメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="8d2df-103">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="8d2df-104">このインターフェイスは、拡張、 [ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="8d2df-104">This interface extends the [ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8d2df-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="8d2df-105">Methods</span></span>  
  
|<span data-ttu-id="8d2df-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="8d2df-106">Method</span></span>|<span data-ttu-id="8d2df-107">説明</span><span class="sxs-lookup"><span data-stu-id="8d2df-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8d2df-108">DefineConstant2 メソッド</span><span class="sxs-lookup"><span data-stu-id="8d2df-108">DefineConstant2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-defineconstant2-method.md)|<span data-ttu-id="8d2df-109">定数値の名前を定義します。</span><span class="sxs-lookup"><span data-stu-id="8d2df-109">Defines a name for a constant value.</span></span>|  
|[<span data-ttu-id="8d2df-110">DefineGlobalVariable2 メソッド</span><span class="sxs-lookup"><span data-stu-id="8d2df-110">DefineGlobalVariable2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-defineglobalvariable2-method.md)|<span data-ttu-id="8d2df-111">1 つのグローバル変数を定義します。</span><span class="sxs-lookup"><span data-stu-id="8d2df-111">Defines a single global variable.</span></span>|  
|[<span data-ttu-id="8d2df-112">DefineLocalVariable2 メソッド</span><span class="sxs-lookup"><span data-stu-id="8d2df-112">DefineLocalVariable2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-definelocalvariable2-method.md)|<span data-ttu-id="8d2df-113">現在の構文のスコープの変数を 1 つ定義します。</span><span class="sxs-lookup"><span data-stu-id="8d2df-113">Defines a single variable in the current lexical scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8d2df-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="8d2df-114">Requirements</span></span>  
 <span data-ttu-id="8d2df-115">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="8d2df-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8d2df-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d2df-116">See also</span></span>
- [<span data-ttu-id="8d2df-117">シンボル ストア診断インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8d2df-117">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="8d2df-118">ISymUnmanagedWriter インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8d2df-118">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="8d2df-119">ISymUnmanagedWriter3 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8d2df-119">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
