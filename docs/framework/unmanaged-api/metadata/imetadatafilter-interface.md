---
title: IMetaDataFilter インターフェイス
ms.date: 03/30/2017
api_name:
- IMetaDataFilter
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataFilter
helpviewer_keywords:
- IMetaDataFilter interface [.NET Framework metadata]
ms.assetid: ec0856ef-8c56-40ba-bf60-86e0ce8b337f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0e1975a5063217299ddbcdce6f625d5a1285d5b4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642556"
---
# <a name="imetadatafilter-interface"></a><span data-ttu-id="09d21-102">IMetaDataFilter インターフェイス</span><span class="sxs-lookup"><span data-stu-id="09d21-102">IMetaDataFilter Interface</span></span>
<span data-ttu-id="09d21-103">メタデータ トークンにマークを付け、フィルター処理をして、既に実行されたアクションが繰り返し行われないようにするメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="09d21-103">Provides methods for marking and filtering metadata tokens to avoid repeating actions that have already been taken.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="09d21-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="09d21-104">Methods</span></span>  
  
|<span data-ttu-id="09d21-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="09d21-105">Method</span></span>|<span data-ttu-id="09d21-106">説明</span><span class="sxs-lookup"><span data-stu-id="09d21-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="09d21-107">IsTokenMarked メソッド</span><span class="sxs-lookup"><span data-stu-id="09d21-107">IsTokenMarked Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatafilter-istokenmarked-method.md)|<span data-ttu-id="09d21-108">指定したメタデータ トークンが処理されたかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="09d21-108">Gets a value indicating whether the specified metadata token has been processed.</span></span>|  
|[<span data-ttu-id="09d21-109">MarkToken メソッド</span><span class="sxs-lookup"><span data-stu-id="09d21-109">MarkToken Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatafilter-marktoken-method.md)|<span data-ttu-id="09d21-110">指定したメタデータ トークンが処理されたことを示す値を設定します。</span><span class="sxs-lookup"><span data-stu-id="09d21-110">Sets a value indicating that the specified metadata token has been processed.</span></span>|  
|[<span data-ttu-id="09d21-111">UnmarkAll メソッド</span><span class="sxs-lookup"><span data-stu-id="09d21-111">UnmarkAll Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatafilter-unmarkall-method.md)|<span data-ttu-id="09d21-112">現在のメタデータ スコープ内のすべてのトークンから処理のマークを削除します。</span><span class="sxs-lookup"><span data-stu-id="09d21-112">Removes the processing marks from all the tokens in the current metadata scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="09d21-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="09d21-113">Requirements</span></span>  
 <span data-ttu-id="09d21-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="09d21-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="09d21-115">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="09d21-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="09d21-116">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="09d21-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="09d21-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="09d21-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09d21-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="09d21-118">See also</span></span>
- [<span data-ttu-id="09d21-119">メタデータ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="09d21-119">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
