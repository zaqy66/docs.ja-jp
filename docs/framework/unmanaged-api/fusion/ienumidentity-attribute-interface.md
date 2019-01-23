---
title: IEnumIDENTITY_ATTRIBUTE インターフェイス
ms.date: 03/30/2017
api_name:
- IEnumIDENTITY_ATTRIBUTE
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumIDENTITY_ATTRIBUTE
helpviewer_keywords:
- IEnumIDENTITY_ATTRIBUTE interface [.NET Framework fusion]
ms.assetid: c2ec2748-e9ae-4e1b-80db-6fcec5cb81a1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8ae940946c56cbc858690cccce61597d0016e40c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571809"
---
# <a name="ienumidentityattribute-interface"></a><span data-ttu-id="a177f-102">IEnumIDENTITY_ATTRIBUTE インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a177f-102">IEnumIDENTITY_ATTRIBUTE Interface</span></span>
<span data-ttu-id="a177f-103">現在のスコープ内のコード オブジェクトの属性の列挙子として機能します。</span><span class="sxs-lookup"><span data-stu-id="a177f-103">Serves as an enumerator for the attributes of the code object in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a177f-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="a177f-104">Methods</span></span>  
  
|<span data-ttu-id="a177f-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="a177f-105">Method</span></span>|<span data-ttu-id="a177f-106">説明</span><span class="sxs-lookup"><span data-stu-id="a177f-106">Description</span></span>|  
|------------|-----------------|  
|`IEnumIDENTITY_ATTRIBUTE::Clone`|<span data-ttu-id="a177f-107">新しいインターフェイス ポインターを取得`IEnumIDENTITY_ATTRIBUTE`これと同じメンバーを格納している`IEnumIDENTITY_ATTRIBUTE`します。</span><span class="sxs-lookup"><span data-stu-id="a177f-107">Gets an interface pointer to a new `IEnumIDENTITY_ATTRIBUTE` that contains the same members as this `IEnumIDENTITY_ATTRIBUTE`.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::CurrentIntoBuffer`|<span data-ttu-id="a177f-108">この要素に含まれるデータを書き込みます`IEnumIDENTITY_ATTRIBUTE`に指定されたデータ バッファー。</span><span class="sxs-lookup"><span data-stu-id="a177f-108">Writes the data contained in the elements of this `IEnumIDENTITY_ATTRIBUTE` to the specified data buffer.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Next`|<span data-ttu-id="a177f-109">指定した数の現在位置から始まり、属性を取得します。</span><span class="sxs-lookup"><span data-stu-id="a177f-109">Gets the specified number of attributes, starting at the current position.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Reset`|<span data-ttu-id="a177f-110">これの先頭に、命令ポインターを移動`IEnumIDENTITY_ATTRIBUTE`します。</span><span class="sxs-lookup"><span data-stu-id="a177f-110">Moves the instruction pointer to the beginning of this `IEnumIDENTITY_ATTRIBUTE`.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Skip`|<span data-ttu-id="a177f-111">指定数の要素を現在の位置からでは、転送、命令ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="a177f-111">Moves the instruction pointer forward by the specified number of elements, starting at the current position.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a177f-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="a177f-112">Requirements</span></span>  
 <span data-ttu-id="a177f-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a177f-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a177f-114">**ヘッダー:** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="a177f-114">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="a177f-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a177f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a177f-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="a177f-116">See also</span></span>
- [<span data-ttu-id="a177f-117">Fusion インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a177f-117">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
