---
title: IAssemblyName::Finalize メソッド
ms.date: 03/30/2017
api_name:
- IAssemblyName.Finalize
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::Finalize
helpviewer_keywords:
- Finalize method [.NET Framework fusion]
- IAssemblyName::Finalize method [.NET Framework fusion]
ms.assetid: 610e792d-98ef-411f-90b0-5b9a3813f547
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dcad824ebe82e4b202a8684d4f905a7d8b90456a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54619027"
---
# <a name="iassemblynamefinalize-method"></a><span data-ttu-id="ef35a-102">IAssemblyName::Finalize メソッド</span><span class="sxs-lookup"><span data-stu-id="ef35a-102">IAssemblyName::Finalize Method</span></span>
<span data-ttu-id="ef35a-103">これにより、 [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)オブジェクト リソースを解放し、そのデストラクターが呼び出される前に、他のクリーンアップ操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="ef35a-103">Allows this [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) object to release resources and perform other cleanup operations before its destructor is called.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ef35a-104">構文</span><span class="sxs-lookup"><span data-stu-id="ef35a-104">Syntax</span></span>  
  
```  
HRESULT Finalize ();  
```  
  
## <a name="requirements"></a><span data-ttu-id="ef35a-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="ef35a-105">Requirements</span></span>  
 <span data-ttu-id="ef35a-106">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef35a-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ef35a-107">**ヘッダー:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="ef35a-107">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="ef35a-108">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ef35a-108">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef35a-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="ef35a-109">See also</span></span>
- [<span data-ttu-id="ef35a-110">IAssemblyName インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ef35a-110">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
