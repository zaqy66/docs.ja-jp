---
title: IMetaDataTables::GetRow メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetRow
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetRow
helpviewer_keywords:
- IMetaDataTables::GetRow method [.NET Framework metadata]
- GetRow method [.NET Framework metadata]
ms.assetid: a7408d51-0bce-45a2-b58f-da4660bbc039
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d24dbcbdd8b0ed0736f7b59564cf72dffaa5a8f8
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43745958"
---
# <a name="imetadatatablesgetrow-method"></a><span data-ttu-id="ae751-102">IMetaDataTables::GetRow メソッド</span><span class="sxs-lookup"><span data-stu-id="ae751-102">IMetaDataTables::GetRow Method</span></span>
<span data-ttu-id="ae751-103">指定したテーブルのインデックス位置にある表に、指定した行インデックス位置にある行を取得します。</span><span class="sxs-lookup"><span data-stu-id="ae751-103">Gets the row at the specified row index, in the table at the specified table index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae751-104">構文</span><span class="sxs-lookup"><span data-stu-id="ae751-104">Syntax</span></span>  
  
```  
HRESULT GetRow (   
    [in]  ULONG   ixTbl,  
    [in]  ULONG   rid,  
    [out] void    **ppRow  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ae751-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae751-105">Parameters</span></span>  
 `ixTbl`  
 <span data-ttu-id="ae751-106">[in]行の取得元となるテーブルのインデックス。</span><span class="sxs-lookup"><span data-stu-id="ae751-106">[in] The index of the table from which the row will be retrieved.</span></span>  
  
 `rid`  
 <span data-ttu-id="ae751-107">[in]取得する行のインデックス。</span><span class="sxs-lookup"><span data-stu-id="ae751-107">[in] The index of the row to get.</span></span>  
  
 `ppRow`  
 <span data-ttu-id="ae751-108">[out]行へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ae751-108">[out] A pointer to a pointer to the row.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ae751-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="ae751-109">Remarks</span></span>  
 <span data-ttu-id="ae751-110">お勧めしません、このメソッドを使用して一貫性のある結果を返さないためです。</span><span class="sxs-lookup"><span data-stu-id="ae751-110">We do not recommend the use of this method, because it does not return consistent results.</span></span> <span data-ttu-id="ae751-111">GUID の表については、共通言語基盤 (CLI) のドキュメント、特に「Partition II:: メタデータ Definition and Semantics」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae751-111">For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics".</span></span> <span data-ttu-id="ae751-112">ドキュメントはオンラインで入手できます。MSDN の「[ECMA C# and Common Language Infrastructure Standards](https://go.microsoft.com/fwlink/?LinkID=99212)」 (ECMA の C# および共通言語基盤の標準規格) と、ECMA のインターナショナル Web サイトにある「[Standard ECMA-335 - Common Language Infrastructure (CLI)](https://go.microsoft.com/fwlink/?LinkID=65552)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae751-112">The documentation is available online; see [ECMA C# and Common Language Infrastructure Standards](https://go.microsoft.com/fwlink/?LinkID=99212) on MSDN and [Standard ECMA-335 - Common Language Infrastructure (CLI)](https://go.microsoft.com/fwlink/?LinkID=65552) on the Ecma International Web site.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae751-113">要件</span><span class="sxs-lookup"><span data-stu-id="ae751-113">Requirements</span></span>  
 <span data-ttu-id="ae751-114">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae751-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae751-115">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ae751-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ae751-116">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="ae751-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ae751-117">**.NET framework のバージョン**  [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae751-117">**.NET Framework Versions**  [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae751-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae751-118">See Also</span></span>  
 [<span data-ttu-id="ae751-119">IMetaDataTables インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ae751-119">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="ae751-120">IMetaDataTables2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ae751-120">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
