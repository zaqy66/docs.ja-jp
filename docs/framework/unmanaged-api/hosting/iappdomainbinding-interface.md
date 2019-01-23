---
title: IAppDomainBinding インターフェイス
ms.date: 03/30/2017
api_name:
- IAppDomainBinding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IAppDomainBinding
helpviewer_keywords:
- IAppDomainBinding interface [.NET Framework hosting]
ms.assetid: 368881ab-c4ea-4731-bf22-c596aac7c66c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4be027238d676d78a3ec29e4f2696f765291f29b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504432"
---
# <a name="iappdomainbinding-interface"></a><span data-ttu-id="9d67a-102">IAppDomainBinding インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9d67a-102">IAppDomainBinding Interface</span></span>
<span data-ttu-id="9d67a-103">共通言語ランタイム (CLR) に、アプリケーション ドメインが作成されたことをホスト アプリケーションに通知するによって呼び出されるメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="9d67a-103">Provides a method that is called by the common language runtime (CLR) to notify the host application that an application domain has been created.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9d67a-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="9d67a-104">Methods</span></span>  
  
|<span data-ttu-id="9d67a-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="9d67a-105">Method</span></span>|<span data-ttu-id="9d67a-106">説明</span><span class="sxs-lookup"><span data-stu-id="9d67a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9d67a-107">OnAppDomain メソッド</span><span class="sxs-lookup"><span data-stu-id="9d67a-107">OnAppDomain Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iappdomainbinding-onappdomain-method.md)|<span data-ttu-id="9d67a-108">共通言語ランタイム (CLR) に、ホスト アプリケーション ドメインが作成されたことを通知するによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9d67a-108">Called by the common language runtime (CLR) to notify the host that an application domain has been created.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9d67a-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="9d67a-109">Requirements</span></span>  
 <span data-ttu-id="9d67a-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d67a-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9d67a-111">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="9d67a-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9d67a-112">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="9d67a-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9d67a-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9d67a-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d67a-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d67a-114">See also</span></span>
- [<span data-ttu-id="9d67a-115">ホスト インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9d67a-115">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
