---
title: IMetaDataTables::GetNextUserString メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNextUserString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNextUserString
helpviewer_keywords:
- GetNextUserString method [.NET Framework metadata]
- IMetaDataTables::GetNextUserString method [.NET Framework metadata]
ms.assetid: b7cb40ee-67b7-4f4e-8dcc-ee7ac8bc986b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 01b326765e792bf97658d951a2d5590d22eff546
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44513888"
---
# <a name="imetadatatablesgetnextuserstring-method"></a><span data-ttu-id="e0a09-102">IMetaDataTables::GetNextUserString メソッド</span><span class="sxs-lookup"><span data-stu-id="e0a09-102">IMetaDataTables::GetNextUserString Method</span></span>
<span data-ttu-id="e0a09-103">現在のテーブル列で [次へ]、ハード コーディングされた文字列を含む行のインデックスを取得します。</span><span class="sxs-lookup"><span data-stu-id="e0a09-103">Gets the index of the row that contains the next hard-coded string in the current table column.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0a09-104">構文</span><span class="sxs-lookup"><span data-stu-id="e0a09-104">Syntax</span></span>  
  
```  
HRESULT GetNextUserString (  
    [in]  ULONG   ixUserString,  
    [out] ULONG   *pNext  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e0a09-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e0a09-105">Parameters</span></span>  
 `ixUserString`  
 <span data-ttu-id="e0a09-106">[in]現在の文字列の列からインデックス値。</span><span class="sxs-lookup"><span data-stu-id="e0a09-106">[in] An index value from the current string column.</span></span>  
  
 `pNext`  
 <span data-ttu-id="e0a09-107">[out]列には、次の文字列の行インデックスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e0a09-107">[out] A pointer to the row index of the next string in the column.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e0a09-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="e0a09-108">Remarks</span></span>  
 <span data-ttu-id="e0a09-109">お勧めしません、このメソッドを使用して一貫性のある結果を返さないためです。</span><span class="sxs-lookup"><span data-stu-id="e0a09-109">We do not recommend the use of this method, because it does not return consistent results.</span></span> <span data-ttu-id="e0a09-110">GUID の表については、共通言語基盤 (CLI) のドキュメント、特に「Partition II:: メタデータ Definition and Semantics」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0a09-110">For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics".</span></span> <span data-ttu-id="e0a09-111">ドキュメントはオンラインで入手できます。MSDN の「[ECMA C# and Common Language Infrastructure Standards](https://go.microsoft.com/fwlink/?LinkID=99212)」 (ECMA の C# および共通言語基盤の標準規格) と、ECMA のインターナショナル Web サイトにある「[Standard ECMA-335 - Common Language Infrastructure (CLI)](https://go.microsoft.com/fwlink/?LinkID=65552)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0a09-111">The documentation is available online; see [ECMA C# and Common Language Infrastructure Standards](https://go.microsoft.com/fwlink/?LinkID=99212) on MSDN and [Standard ECMA-335 - Common Language Infrastructure (CLI)](https://go.microsoft.com/fwlink/?LinkID=65552) on the Ecma International Web site.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e0a09-112">要件</span><span class="sxs-lookup"><span data-stu-id="e0a09-112">Requirements</span></span>  
 <span data-ttu-id="e0a09-113">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0a09-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e0a09-114">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e0a09-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e0a09-115">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="e0a09-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e0a09-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e0a09-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0a09-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="e0a09-117">See Also</span></span>  
 [<span data-ttu-id="e0a09-118">IMetaDataTables インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e0a09-118">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="e0a09-119">IMetaDataTables2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e0a09-119">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
