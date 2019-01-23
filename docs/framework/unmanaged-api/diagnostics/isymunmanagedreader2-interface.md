---
title: ISymUnmanagedReader2 インターフェイス
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2
helpviewer_keywords:
- ISymUnmanagedReader2 interface [.NET Framework debugging]
ms.assetid: a01a881b-82a3-4b3e-a3a9-9dc305c2e5f7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a08695c4e5df6aaa63bedecf68b741302e5ddd8e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54524943"
---
# <a name="isymunmanagedreader2-interface"></a><span data-ttu-id="d6a82-102">ISymUnmanagedReader2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d6a82-102">ISymUnmanagedReader2 Interface</span></span>
<span data-ttu-id="d6a82-103">ドキュメント、メソッド、およびシンボル ストア内の変数へのアクセスを提供するためのシンボル リーダーを表します。</span><span class="sxs-lookup"><span data-stu-id="d6a82-103">Represents a symbol reader that provides access to documents, methods, and variables within a symbol store.</span></span> <span data-ttu-id="d6a82-104">このインターフェイスは、拡張、 [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="d6a82-104">This interface extends the [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d6a82-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="d6a82-105">Methods</span></span>  
  
|<span data-ttu-id="d6a82-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d6a82-106">Method</span></span>|<span data-ttu-id="d6a82-107">説明</span><span class="sxs-lookup"><span data-stu-id="d6a82-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d6a82-108">GetMethodByVersionPreRemap メソッド</span><span class="sxs-lookup"><span data-stu-id="d6a82-108">GetMethodByVersionPreRemap Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-getmethodbyversionpreremap-method.md)|<span data-ttu-id="d6a82-109">メソッドのトークンとエディット コンティニュ バージョン番号を指定して、シンボル リーダー メソッドを取得します。</span><span class="sxs-lookup"><span data-stu-id="d6a82-109">Get a symbol reader method, given a method token and an edit-and-continue version number.</span></span>|  
|[<span data-ttu-id="d6a82-110">GetMethodsInDocument メソッド</span><span class="sxs-lookup"><span data-stu-id="d6a82-110">GetMethodsInDocument Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-getmethodsindocument-method.md)|<span data-ttu-id="d6a82-111">指定されたドキュメント内の行情報を持つすべてのメソッドを取得します。</span><span class="sxs-lookup"><span data-stu-id="d6a82-111">Gets every method that has line information in the provided document.</span></span>|  
|[<span data-ttu-id="d6a82-112">GetSymAttributePreRemap メソッド</span><span class="sxs-lookup"><span data-stu-id="d6a82-112">GetSymAttributePreRemap Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-getsymattributepreremap-method.md)|<span data-ttu-id="d6a82-113">その名前に基づくカスタム属性を取得します。</span><span class="sxs-lookup"><span data-stu-id="d6a82-113">Gets a custom attribute based upon its name.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d6a82-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="d6a82-114">Requirements</span></span>  
 <span data-ttu-id="d6a82-115">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="d6a82-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6a82-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6a82-116">See also</span></span>
- [<span data-ttu-id="d6a82-117">シンボル ストア診断インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d6a82-117">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="d6a82-118">ISymUnmanagedReader インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d6a82-118">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
