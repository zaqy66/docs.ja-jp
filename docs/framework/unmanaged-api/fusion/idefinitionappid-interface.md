---
title: IDefinitionAppId インターフェイス
ms.date: 03/30/2017
api_name:
- IDefinitionAppId
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IDefinitionAppId
helpviewer_keywords:
- IDefinitionAppId interface [.NET Framework fusion]
ms.assetid: e72f2550-bdec-4a20-a2f4-2e14847266c1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4e8bb31967a6ad515761e6cd03657f2c834debe5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54545557"
---
# <a name="idefinitionappid-interface"></a><span data-ttu-id="0d81f-102">IDefinitionAppId インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0d81f-102">IDefinitionAppId Interface</span></span>
<span data-ttu-id="0d81f-103">現在のスコープ内でアプリケーションを定義するコードの一意の識別子を表します。</span><span class="sxs-lookup"><span data-stu-id="0d81f-103">Represents a unique identifier for the code that defines the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0d81f-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="0d81f-104">Methods</span></span>  
  
|<span data-ttu-id="0d81f-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="0d81f-105">Method</span></span>|<span data-ttu-id="0d81f-106">説明</span><span class="sxs-lookup"><span data-stu-id="0d81f-106">Description</span></span>|  
|------------|-----------------|  
|`IDefinitionAppId::get_Codebase`|<span data-ttu-id="0d81f-107">このコードを表す書式設定された文字列を取得します。`IDefinitionAppId`オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0d81f-107">Gets a formatted string that represents the code in this `IDefinitionAppId` object.</span></span>|  
|`IDefinitionAppId::put_Codebase`|<span data-ttu-id="0d81f-108">このコードを設定`IDefinitionAppId`を指定したオブジェクトの書式設定された文字列値。</span><span class="sxs-lookup"><span data-stu-id="0d81f-108">Sets the code of this `IDefinitionAppId` object to the specified formatted string value.</span></span>|  
|`IDefinitionAppId::EnumAppPath`|<span data-ttu-id="0d81f-109">インターフェイス ポインターを取得、 [IEnumDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/ienumdefinitionidentity-interface.md)現在のアプリケーション パス内のアセンブリを格納しているオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0d81f-109">Gets an interface pointer to an [IEnumDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/ienumdefinitionidentity-interface.md) object that contains the assemblies in the current application path.</span></span>|  
|`IDefinitionAppId::SetAppPath`|<span data-ttu-id="0d81f-110">指定したによって参照される値を現在のスコープ内のアセンブリのアプリケーション パスを設定[IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md)オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0d81f-110">Sets the application path for the assembly in the current scope to the value referenced by the specified [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) object.</span></span>|  
|`IDefinitionAppId::get_SubscriptionId`|<span data-ttu-id="0d81f-111">このサブスクリプションのトークンの識別子の文字列表現にポインターを取得します。`IDefinitionAppId`オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0d81f-111">Gets a pointer to a string representation of the token identifier for a subscription to this `IDefinitionAppId` object.</span></span>|  
|`IDefinitionAppId::put_SubscriptionId`|<span data-ttu-id="0d81f-112">このサブスクリプションのトークンの識別子を設定`IDefinitionAppId`オブジェクト指定した文字列値から。</span><span class="sxs-lookup"><span data-stu-id="0d81f-112">Sets the token identifier for a subscription to this `IDefinitionAppId` object to the specified string value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0d81f-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="0d81f-113">Requirements</span></span>  
 <span data-ttu-id="0d81f-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d81f-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0d81f-115">**ヘッダー:** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="0d81f-115">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="0d81f-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0d81f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d81f-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d81f-117">See also</span></span>
- [<span data-ttu-id="0d81f-118">Fusion インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0d81f-118">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
