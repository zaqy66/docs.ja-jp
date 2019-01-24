---
title: IEnumDefinitionIdentity インターフェイス
ms.date: 03/30/2017
api_name:
- IEnumDefinitionIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumDefinitionIdentity
helpviewer_keywords:
- IEnumDefinitionIdentity interface [.NET Framework fusion]
ms.assetid: 8263e75d-251b-4abc-8a1a-c62884142232
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a3ff37acd9b4dffe80112f0a0ebe9c9cd86ae66f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668448"
---
# <a name="ienumdefinitionidentity-interface"></a><span data-ttu-id="608e0-102">IEnumDefinitionIdentity インターフェイス</span><span class="sxs-lookup"><span data-stu-id="608e0-102">IEnumDefinitionIdentity Interface</span></span>
<span data-ttu-id="608e0-103">コレクションの列挙子として機能`IDefinitionIdentity`オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="608e0-103">Serves as the enumerator for a collection of `IDefinitionIdentity` objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="608e0-104">構文</span><span class="sxs-lookup"><span data-stu-id="608e0-104">Syntax</span></span>  
  
```  
IEnumDefinitionIdentity : IUnknown {  
  
    HRESULT Clone (  
        [out] IEnumDefinitionIdentity **ppIEnumDefinitionIdentity  
    );  
  
    HRESULT Next (  
        [in]  ULONG               celt,  
        [out, length_is(celt), size_is(*pceltWritten)]  
              IDefinitionIdentity *rgpIDefinitionIdentity[],  
        [out] ULONG               *pceltWritten  
    );  
  
    HRESULT Reset ();  
  
    HRESULT Skip (  
        [in] ULONG celt  
    );  
  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="608e0-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="608e0-105">Methods</span></span>  
  
|<span data-ttu-id="608e0-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="608e0-106">Method</span></span>|<span data-ttu-id="608e0-107">説明</span><span class="sxs-lookup"><span data-stu-id="608e0-107">Description</span></span>|  
|------------|-----------------|  
|`IEnumDefinitionIdentity::Clone`|<span data-ttu-id="608e0-108">新しいインターフェイス ポインターを取得`IEnumDefinitionIdentity`これと同じメンバーを含むオブジェクト`IEnumDefinitionIdentity`します。</span><span class="sxs-lookup"><span data-stu-id="608e0-108">Gets an interface pointer to a new `IEnumDefinitionIdentity` object that contains the same members as this `IEnumDefinitionIdentity`.</span></span>|  
|`IEnumDefinitionIdentity::Next`|<span data-ttu-id="608e0-109">指定した数を取得`IDefinitionIdentity`オブジェクト、現在の位置で開始します。</span><span class="sxs-lookup"><span data-stu-id="608e0-109">Gets the specified number of `IDefinitionIdentity` objects, starting at the current position.</span></span>|  
|`IEnumDefinitionIdentity::Reset`|<span data-ttu-id="608e0-110">これの先頭に、命令ポインターを移動`IEnumDefinitionIdentity`します。</span><span class="sxs-lookup"><span data-stu-id="608e0-110">Moves the instruction pointer to the beginning of this `IEnumDefinitionIdentity`.</span></span>|  
|`IEnumDefinitionIdentity::Skip`|<span data-ttu-id="608e0-111">指定数の要素を現在の位置からでは、転送、命令ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="608e0-111">Moves the instruction pointer forward by the specified number of elements, starting at the current position.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="608e0-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="608e0-112">Requirements</span></span>  
 <span data-ttu-id="608e0-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="608e0-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="608e0-114">**ヘッダー:** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="608e0-114">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="608e0-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="608e0-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="608e0-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="608e0-116">See also</span></span>
- [<span data-ttu-id="608e0-117">Fusion インターフェイス</span><span class="sxs-lookup"><span data-stu-id="608e0-117">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [<span data-ttu-id="608e0-118">IDefinitionIdentity インターフェイス</span><span class="sxs-lookup"><span data-stu-id="608e0-118">IDefinitionIdentity Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md)
