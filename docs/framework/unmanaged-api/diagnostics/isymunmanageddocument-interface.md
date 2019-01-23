---
title: ISymUnmanagedDocument インターフェイス
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument
helpviewer_keywords:
- ISymUnmanagedDocument interface [.NET Framework debugging]
ms.assetid: 5c26b366-6e81-467c-9dd0-02dd26fee0a3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b14333235882efb6da1ce011c109c67a1d149bf3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54584520"
---
# <a name="isymunmanageddocument-interface"></a><span data-ttu-id="a5462-102">ISymUnmanagedDocument インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a5462-102">ISymUnmanagedDocument Interface</span></span>
<span data-ttu-id="a5462-103">シンボル ストアによって参照されるドキュメントを表します。</span><span class="sxs-lookup"><span data-stu-id="a5462-103">Represents a document referenced by a symbol store.</span></span> <span data-ttu-id="a5462-104">ドキュメントは、uniform resource locator (URL) と GUID のドキュメントの種類によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="a5462-104">A document is defined by a uniform resource locator (URL) and a document type GUID.</span></span> <span data-ttu-id="a5462-105">URL を使用して格納する方法に関係なく、ドキュメントを検索でき、ドキュメントの種類の GUID。</span><span class="sxs-lookup"><span data-stu-id="a5462-105">You can locate the document regardless of how it is stored by using the URL and document type GUID.</span></span> <span data-ttu-id="a5462-106">ドキュメントのソースをシンボル ストアに格納でき、このインターフェイスを通じて取得できます。</span><span class="sxs-lookup"><span data-stu-id="a5462-106">You can store the document source in the symbol store and retrieve it through this interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a5462-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-107">Methods</span></span>  
  
|<span data-ttu-id="a5462-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-108">Method</span></span>|<span data-ttu-id="a5462-109">説明</span><span class="sxs-lookup"><span data-stu-id="a5462-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a5462-110">FindClosestLine メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-110">FindClosestLine Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-findclosestline-method.md)|<span data-ttu-id="a5462-111">行を指定したシーケンス ポイントができない可能性がありますが、このドキュメントでは、シーケンス ポイントである最も近い行を返します。</span><span class="sxs-lookup"><span data-stu-id="a5462-111">Returns the closest line that is a sequence point, given a line in this document that may or may not be a sequence point.</span></span>|  
|[<span data-ttu-id="a5462-112">GetCheckSum メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-112">GetCheckSum Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getchecksum-method.md)|<span data-ttu-id="a5462-113">チェックサムを取得します。</span><span class="sxs-lookup"><span data-stu-id="a5462-113">Gets the checksum.</span></span>|  
|[<span data-ttu-id="a5462-114">GetCheckSumAlgorithmId メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-114">GetCheckSumAlgorithmId Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getchecksumalgorithmid-method.md)|<span data-ttu-id="a5462-115">チェックサム アルゴリズム識別子を取得またはチェックサムがない場合は、すべてゼロの GUID を返します。</span><span class="sxs-lookup"><span data-stu-id="a5462-115">Gets the checksum algorithm identifier, or returns a GUID of all zeros if there is no checksum.</span></span>|  
|[<span data-ttu-id="a5462-116">GetDocumentType メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-116">GetDocumentType Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getdocumenttype-method.md)|<span data-ttu-id="a5462-117">このドキュメントのドキュメントの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="a5462-117">Gets the document type of this document.</span></span>|  
|[<span data-ttu-id="a5462-118">GetLanguage メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-118">GetLanguage Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getlanguage-method.md)|<span data-ttu-id="a5462-119">このドキュメントの言語識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="a5462-119">Gets the language identifier of this document.</span></span>|  
|[<span data-ttu-id="a5462-120">GetLanguageVendor メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-120">GetLanguageVendor Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getlanguagevendor-method.md)|<span data-ttu-id="a5462-121">このドキュメントの言語の販売元を取得します。</span><span class="sxs-lookup"><span data-stu-id="a5462-121">Gets the language vendor of this document.</span></span>|  
|[<span data-ttu-id="a5462-122">GetSourceLength メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-122">GetSourceLength Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getsourcelength-method.md)|<span data-ttu-id="a5462-123">埋め込まれたソースの長さをバイト数で取得します。</span><span class="sxs-lookup"><span data-stu-id="a5462-123">Gets the length, in bytes, of the embedded source.</span></span>|  
|[<span data-ttu-id="a5462-124">GetSourceRange メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-124">GetSourceRange Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getsourcerange-method.md)|<span data-ttu-id="a5462-125">指定されたバッファーに埋め込みのソースの指定した範囲を返します。</span><span class="sxs-lookup"><span data-stu-id="a5462-125">Returns the specified range of the embedded source into the given buffer.</span></span>|  
|[<span data-ttu-id="a5462-126">GetURL メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-126">GetURL Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-geturl-method.md)|<span data-ttu-id="a5462-127">このドキュメントの URL を返します。</span><span class="sxs-lookup"><span data-stu-id="a5462-127">Returns the URL for this document.</span></span>|  
|[<span data-ttu-id="a5462-128">HasEmbeddedSource メソッド</span><span class="sxs-lookup"><span data-stu-id="a5462-128">HasEmbeddedSource Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-hasembeddedsource-method.md)|<span data-ttu-id="a5462-129">返します`true`ドキュメントが、デバッグのシンボルに埋め込まれたソースを返しますそれ以外の場合、`false`します。</span><span class="sxs-lookup"><span data-stu-id="a5462-129">Returns `true` if the document has source embedded in the debugging symbols; otherwise, returns `false`.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a5462-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="a5462-130">See also</span></span>
- [<span data-ttu-id="a5462-131">シンボル ストア診断インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a5462-131">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
