---
title: IAppDomainBinding::OnAppDomain メソッド
ms.date: 03/30/2017
api_name:
- IAppDomainBinding.OnAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- OnAppDomain
helpviewer_keywords:
- IAppDomainBinding::OnAppDomain method [.NET Framework hosting]
- OnAppDomain method [.NET Framework hosting]
ms.assetid: b419dcc9-e8aa-484b-af0d-0f40358edb99
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8dfd396568424c3a2300ed5d982e766afd5f925f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54725494"
---
# <a name="iappdomainbindingonappdomain-method"></a><span data-ttu-id="59fe3-102">IAppDomainBinding::OnAppDomain メソッド</span><span class="sxs-lookup"><span data-stu-id="59fe3-102">IAppDomainBinding::OnAppDomain Method</span></span>
<span data-ttu-id="59fe3-103">共通言語ランタイム (CLR) に、ホスト アプリケーション ドメインが作成されたことを通知するによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="59fe3-103">Called by the common language runtime (CLR) to notify the host that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59fe3-104">構文</span><span class="sxs-lookup"><span data-stu-id="59fe3-104">Syntax</span></span>  
  
```  
HRESULT OnAppDomain (  
    [in] IUnknown* pAppdomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="59fe3-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="59fe3-105">Parameters</span></span>  
 `pAppdomain`  
 <span data-ttu-id="59fe3-106">[in]ポインター、 [IUnknown](https://msdn.microsoft.com/library/94as6ehy(v=vs.110).aspx)新しいアプリケーション ドメインを表すインターフェイス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="59fe3-106">[in] A pointer to an [IUnknown](https://msdn.microsoft.com/library/94as6ehy(v=vs.110).aspx) interface object that represents the new application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="59fe3-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="59fe3-107">Requirements</span></span>  
 <span data-ttu-id="59fe3-108">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="59fe3-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="59fe3-109">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="59fe3-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="59fe3-110">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="59fe3-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="59fe3-111">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="59fe3-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59fe3-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="59fe3-112">See also</span></span>
- [<span data-ttu-id="59fe3-113">IAppDomainBinding インターフェイス</span><span class="sxs-lookup"><span data-stu-id="59fe3-113">IAppDomainBinding Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iappdomainbinding-interface.md)
