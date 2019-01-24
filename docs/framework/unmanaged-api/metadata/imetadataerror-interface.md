---
title: IMetaDataError インターフェイス
ms.date: 03/30/2017
api_name:
- IMetaDataError
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataError
helpviewer_keywords:
- IMetaDataError interface [.NET Framework metadata]
ms.assetid: 0020b62c-ea88-40c7-a9ee-16b064f81624
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fe2f683ae46d1ee6205f97536976a358e86fc53d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720380"
---
# <a name="imetadataerror-interface"></a><span data-ttu-id="dae49-102">IMetaDataError インターフェイス</span><span class="sxs-lookup"><span data-stu-id="dae49-102">IMetaDataError Interface</span></span>
<span data-ttu-id="dae49-103">メタデータのマージ中にエラーを報告するためのコールバック機構を提供します。</span><span class="sxs-lookup"><span data-stu-id="dae49-103">Provides a callback mechanism for reporting errors during the metadata merge.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="dae49-104">`IMetaDataError`クライアントによってインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dae49-104">The `IMetaDataError` interface must be implemented by the client.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="dae49-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="dae49-105">Methods</span></span>  
  
|<span data-ttu-id="dae49-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="dae49-106">Method</span></span>|<span data-ttu-id="dae49-107">説明</span><span class="sxs-lookup"><span data-stu-id="dae49-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="dae49-108">OnError メソッド</span><span class="sxs-lookup"><span data-stu-id="dae49-108">OnError Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataerror-onerror-method.md)|<span data-ttu-id="dae49-109">メタデータのマージ中に発生したエラーの通知を提供します。</span><span class="sxs-lookup"><span data-stu-id="dae49-109">Provides notification of errors that occur during the metadata merge.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="dae49-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="dae49-110">Requirements</span></span>  
 <span data-ttu-id="dae49-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dae49-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dae49-112">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="dae49-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="dae49-113">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="dae49-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="dae49-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dae49-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dae49-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="dae49-115">See also</span></span>
- [<span data-ttu-id="dae49-116">メタデータ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="dae49-116">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
