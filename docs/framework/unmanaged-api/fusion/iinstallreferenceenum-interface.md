---
title: IInstallReferenceEnum インターフェイス
ms.date: 03/30/2017
api_name:
- IInstallReferenceEnum
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceEnum
helpviewer_keywords:
- IInstallReferenceEnum interface [.NET Framework fusion]
ms.assetid: 2863b33b-a541-462c-bbe8-702a2832898e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2aed89008dd2fa86b38f243c8e7cca1bdda901e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54497775"
---
# <a name="iinstallreferenceenum-interface"></a><span data-ttu-id="e5017-102">IInstallReferenceEnum インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e5017-102">IInstallReferenceEnum Interface</span></span>
<span data-ttu-id="e5017-103">グローバル アセンブリ キャッシュにインストールされている参照先アセンブリの列挙子を表します。</span><span class="sxs-lookup"><span data-stu-id="e5017-103">Represents an enumerator for the referenced assemblies installed in the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5017-104">構文</span><span class="sxs-lookup"><span data-stu-id="e5017-104">Syntax</span></span>  
  
```  
interface IInstallReferenceEnum : IUnknown {  
    HRESULT GetNextInstallReferenceItem (  
        [out] IInstallReferenceItem **ppRefItem,  
        [in]  DWORD dwFlags,  
        [in]  LPVOID pvReserved  
    );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="e5017-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="e5017-105">Methods</span></span>  
  
|<span data-ttu-id="e5017-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="e5017-106">Method</span></span>|<span data-ttu-id="e5017-107">説明</span><span class="sxs-lookup"><span data-stu-id="e5017-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e5017-108">GetNextInstallReferenceItem メソッド</span><span class="sxs-lookup"><span data-stu-id="e5017-108">GetNextInstallReferenceItem Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-getnextinstallreferenceitem-method.md)|<span data-ttu-id="e5017-109">次のポインターを取得`IInstallReferenceItem`これに含まれる`IInstallReferenceEnum`します。</span><span class="sxs-lookup"><span data-stu-id="e5017-109">Gets a pointer to the next `IInstallReferenceItem` contained in this `IInstallReferenceEnum`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e5017-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="e5017-110">Requirements</span></span>  
 <span data-ttu-id="e5017-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5017-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5017-112">**ヘッダー:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="e5017-112">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="e5017-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5017-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5017-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5017-114">See also</span></span>
- [<span data-ttu-id="e5017-115">Fusion インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e5017-115">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [<span data-ttu-id="e5017-116">IInstallReferenceItem インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e5017-116">IInstallReferenceItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md)
