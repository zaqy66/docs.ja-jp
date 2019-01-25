---
title: ISymUnmanagedBinder3 インターフェイス
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder3 Interface
helpviewer_keywords:
- ISymUnmanagedBinder3 interface [.NET Framework debugging]
ms.assetid: 37527a84-4b03-4f08-8135-94d898599089
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: be91591bfbbe4531c5518b90e560bc05457c92da
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730166"
---
# <a name="isymunmanagedbinder3-interface"></a><span data-ttu-id="5080e-102">ISymUnmanagedBinder3 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5080e-102">ISymUnmanagedBinder3 Interface</span></span>
<span data-ttu-id="5080e-103">シンボル バインダー インターフェイスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="5080e-103">Extends the symbol binder interface.</span></span> <span data-ttu-id="5080e-104">このインターフェイスを呼び出すことによって取得`QueryInterface`を実装するオブジェクトで、`ISymUnmanagedBinder`インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="5080e-104">Obtain this interface by calling `QueryInterface` on an object that implements the `ISymUnmanagedBinder` interface.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="5080e-105">信頼できないソースからプログラム データベース (PDB) ファイルをセキュリティ リスクになります。</span><span class="sxs-lookup"><span data-stu-id="5080e-105">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5080e-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="5080e-106">Methods</span></span>  
  
|<span data-ttu-id="5080e-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="5080e-107">Method</span></span>|<span data-ttu-id="5080e-108">説明</span><span class="sxs-lookup"><span data-stu-id="5080e-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5080e-109">GetReaderFromCallback メソッド</span><span class="sxs-lookup"><span data-stu-id="5080e-109">GetReaderFromCallback Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-getreaderfromcallback-method.md)|<span data-ttu-id="5080e-110">ユーザーに実装するか、コールバックを使用して指定できるように、`IID_IDiaReadExeAtRVACallback`または`IID_IDiaReadExeAtOffsetCallback`メモリからデバッグ ディレクトリ情報を取得するには</span><span class="sxs-lookup"><span data-stu-id="5080e-110">Allows the user to implement or supply via callback either an `IID_IDiaReadExeAtRVACallback` or `IID_IDiaReadExeAtOffsetCallback` to obtain the Debug directory information from memory</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5080e-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="5080e-111">Requirements</span></span>  
 <span data-ttu-id="5080e-112">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="5080e-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5080e-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="5080e-113">See also</span></span>
- [<span data-ttu-id="5080e-114">シンボル ストア診断インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5080e-114">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="5080e-115">ISymUnmanagedBinder インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5080e-115">ISymUnmanagedBinder Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)
- [<span data-ttu-id="5080e-116">ISymUnmanagedBinder2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5080e-116">ISymUnmanagedBinder2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-interface.md)
