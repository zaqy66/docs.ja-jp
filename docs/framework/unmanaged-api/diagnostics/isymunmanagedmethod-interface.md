---
title: ISymUnmanagedMethod インターフェイス
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod
helpviewer_keywords:
- ISymUnmanagedMethod interface [.NET Framework debugging]
ms.assetid: f204d74c-cc79-4092-83bb-60654be95649
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b19e5ce88ea34188b2757d2a0c313341fbf1e7e6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604259"
---
# <a name="isymunmanagedmethod-interface"></a><span data-ttu-id="df242-102">ISymUnmanagedMethod インターフェイス</span><span class="sxs-lookup"><span data-stu-id="df242-102">ISymUnmanagedMethod Interface</span></span>
<span data-ttu-id="df242-103">シンボル ストア内のメソッドを表します。</span><span class="sxs-lookup"><span data-stu-id="df242-103">Represents a method within the symbol store.</span></span> <span data-ttu-id="df242-104">このインターフェイスは、型に関連する属性ではなく、メソッドのシンボルに関連する属性のみへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="df242-104">This interface provides access to only the symbol-related attributes of a method, instead of the type-related attributes.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="df242-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-105">Methods</span></span>  
  
|<span data-ttu-id="df242-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-106">Method</span></span>|<span data-ttu-id="df242-107">説明</span><span class="sxs-lookup"><span data-stu-id="df242-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="df242-108">GetNamespace メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-108">GetNamespace Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getnamespace-method.md)|<span data-ttu-id="df242-109">このメソッドを定義する名前空間を取得します。</span><span class="sxs-lookup"><span data-stu-id="df242-109">Gets the namespace within which this method is defined.</span></span>|  
|[<span data-ttu-id="df242-110">GetOffset メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-110">GetOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getoffset-method.md)|<span data-ttu-id="df242-111">ドキュメント内の位置を指定するには、対応するこのメソッド内のオフセットを返します。</span><span class="sxs-lookup"><span data-stu-id="df242-111">Returns the offset within this method that corresponds to a given position within a document.</span></span>|  
|[<span data-ttu-id="df242-112">GetParameters メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-112">GetParameters Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getparameters-method.md)|<span data-ttu-id="df242-113">このメソッドのパラメーターを取得します。</span><span class="sxs-lookup"><span data-stu-id="df242-113">Gets the parameters for this method.</span></span>|  
|[<span data-ttu-id="df242-114">GetRanges メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-114">GetRanges Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getranges-method.md)|<span data-ttu-id="df242-115">指定されたドキュメント内の位置には、Microsoft intermediate language (MSIL をこのメソッド内の位置に含まれる) の範囲に先頭と末尾オフセットのペアの対応する配列を返します。</span><span class="sxs-lookup"><span data-stu-id="df242-115">Given a position in a document, returns an array of start and end offset pairs that correspond to the ranges of Microsoft intermediate language (MSIL) that the position covers within this method.</span></span>|  
|[<span data-ttu-id="df242-116">GetRootScope メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-116">GetRootScope Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getrootscope-method.md)|<span data-ttu-id="df242-117">このメソッド内でルート構文スコープを取得します。</span><span class="sxs-lookup"><span data-stu-id="df242-117">Gets the root lexical scope within this method.</span></span> <span data-ttu-id="df242-118">このスコープはメソッド全体を囲みます。</span><span class="sxs-lookup"><span data-stu-id="df242-118">This scope encloses the entire method.</span></span>|  
|[<span data-ttu-id="df242-119">GetScopeFromOffSet メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-119">GetScopeFromOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getscopefromoffset-method.md)|<span data-ttu-id="df242-120">このメソッドを指定したオフセットを囲む内で最も外側の構文のスコープを取得します。</span><span class="sxs-lookup"><span data-stu-id="df242-120">Gets the most enclosing lexical scope within this method that encloses the given offset.</span></span>|  
|[<span data-ttu-id="df242-121">GetSequencePointCount メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-121">GetSequencePointCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getsequencepointcount-method.md)|<span data-ttu-id="df242-122">このメソッド内のシーケンス ポイントの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="df242-122">Gets the count of sequence points within this method.</span></span>|  
|[<span data-ttu-id="df242-123">GetSequencePoints メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-123">GetSequencePoints Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getsequencepoints-method.md)|<span data-ttu-id="df242-124">このメソッド内のすべてのシーケンス ポイントを取得します。</span><span class="sxs-lookup"><span data-stu-id="df242-124">Gets all the sequence points within this method.</span></span>|  
|[<span data-ttu-id="df242-125">GetSourceStartEnd メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-125">GetSourceStartEnd Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getsourcestartend-method.md)|<span data-ttu-id="df242-126">このメソッドのソースの先頭と末尾のドキュメントの位置を取得します。</span><span class="sxs-lookup"><span data-stu-id="df242-126">Gets the start and end document positions for the source of this method.</span></span>|  
|[<span data-ttu-id="df242-127">GetToken メソッド</span><span class="sxs-lookup"><span data-stu-id="df242-127">GetToken Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-gettoken-method.md)|<span data-ttu-id="df242-128">このメソッドのメタデータ トークンを返します。</span><span class="sxs-lookup"><span data-stu-id="df242-128">Returns the metadata token for this method.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="df242-129">必要条件</span><span class="sxs-lookup"><span data-stu-id="df242-129">Requirements</span></span>  
 <span data-ttu-id="df242-130">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="df242-130">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df242-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="df242-131">See also</span></span>
- [<span data-ttu-id="df242-132">シンボル ストア診断インターフェイス</span><span class="sxs-lookup"><span data-stu-id="df242-132">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
