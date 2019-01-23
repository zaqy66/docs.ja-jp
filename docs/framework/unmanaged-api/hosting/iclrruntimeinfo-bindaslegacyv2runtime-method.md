---
title: ICLRRuntimeInfo::BindAsLegacyV2Runtime メソッド
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.BindAsLegacyV2Runtime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::BindAsLegacyV2Runtime
helpviewer_keywords:
- ICLRRuntimeInfo::BindAsLegacyV2Runtime method [.NET Framework hosting]
- BindAsLegacyV2Runtime method [.NET Framework hosting]
ms.assetid: 65fd55ac-4a24-4479-9384-a2e8013bfb2b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6c85888e9d29e7b3ae6ad76d1e534e08a4603ed2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499026"
---
# <a name="iclrruntimeinfobindaslegacyv2runtime-method"></a><span data-ttu-id="58dcb-102">ICLRRuntimeInfo::BindAsLegacyV2Runtime メソッド</span><span class="sxs-lookup"><span data-stu-id="58dcb-102">ICLRRuntimeInfo::BindAsLegacyV2Runtime Method</span></span>
<span data-ttu-id="58dcb-103">すべてレガシ共通言語ランタイム (CLR) バージョン 2 のライセンス認証ポリシーの決定の現在のランタイムをバインドします。</span><span class="sxs-lookup"><span data-stu-id="58dcb-103">Binds the current runtime for all legacy common language runtime (CLR) version 2 activation policy decisions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58dcb-104">構文</span><span class="sxs-lookup"><span data-stu-id="58dcb-104">Syntax</span></span>  
  
```  
HRESULT BindAsLegacyV2Runtime ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="58dcb-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="58dcb-105">Return Value</span></span>  
 <span data-ttu-id="58dcb-106">このメソッドは、次の特定の Hresult を返します。</span><span class="sxs-lookup"><span data-stu-id="58dcb-106">This method returns the following specific HRESULTs:</span></span>  
  
|<span data-ttu-id="58dcb-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="58dcb-107">HRESULT</span></span>|<span data-ttu-id="58dcb-108">説明</span><span class="sxs-lookup"><span data-stu-id="58dcb-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="58dcb-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="58dcb-109">S_OK</span></span>|<span data-ttu-id="58dcb-110">バインドが成功したか、このランタイムは、従来の CLR バージョン 2 のアクティブ化ポリシー ランタイムと既にバインドされています。</span><span class="sxs-lookup"><span data-stu-id="58dcb-110">Either binding succeeded, or this runtime was already bound as the legacy CLR version 2 activation policy runtime.</span></span>|  
|<span data-ttu-id="58dcb-111">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span><span class="sxs-lookup"><span data-stu-id="58dcb-111">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span></span>|<span data-ttu-id="58dcb-112">別のランタイムは、従来の CLR バージョン 2 のアクティブ化ポリシーに既にバインドされています。</span><span class="sxs-lookup"><span data-stu-id="58dcb-112">A different runtime was already bound to the legacy CLR version 2 activation policy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="58dcb-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="58dcb-113">Remarks</span></span>  
 <span data-ttu-id="58dcb-114">現在のランタイムがすべてレガシ CLR バージョン 2 のライセンス認証ポリシーの決定に既にバインドされている場合 (などを使用して、`useLegacyV2RuntimeActivationPolicy`属性を[ \<startup > 要素](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)構成ファイルで)、このメソッドエラーの結果を返しません代わりに、なりますメソッドがレガシ アクティブ化ポリシーを正常にバインドしたかどうかと同様に、結果は、s_ok を返します。</span><span class="sxs-lookup"><span data-stu-id="58dcb-114">If the current runtime is already bound for all legacy CLR version 2 activation policy decisions (for example, by using the `useLegacyV2RuntimeActivationPolicy` attribute on the [\<startup> element](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) in the configuration file), this method does not return an error result; instead, the result is S_OK, just as it would be if the method had successfully bound legacy activation policy.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="58dcb-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="58dcb-115">Requirements</span></span>  
 <span data-ttu-id="58dcb-116">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="58dcb-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58dcb-117">**ヘッダー:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="58dcb-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="58dcb-118">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="58dcb-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="58dcb-119">**.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58dcb-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58dcb-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="58dcb-120">See also</span></span>
- [<span data-ttu-id="58dcb-121">ICLRRuntimeInfo インターフェイス</span><span class="sxs-lookup"><span data-stu-id="58dcb-121">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)
- [<span data-ttu-id="58dcb-122">ホスト インターフェイス</span><span class="sxs-lookup"><span data-stu-id="58dcb-122">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="58dcb-123">ホスティング</span><span class="sxs-lookup"><span data-stu-id="58dcb-123">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
- [<span data-ttu-id="58dcb-124">\<startup> 要素</span><span class="sxs-lookup"><span data-stu-id="58dcb-124">\<startup> Element</span></span>](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)
