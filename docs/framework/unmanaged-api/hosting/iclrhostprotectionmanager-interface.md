---
title: ICLRHostProtectionManager インターフェイス
ms.date: 03/30/2017
api_name:
- ICLRHostProtectionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostProtectionManager
helpviewer_keywords:
- ICLRHostProtectionManager interface [.NET Framework hosting]
ms.assetid: ce2770ae-23d0-45d9-8bcf-46504ac5020e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1d4cb310215967a79e43e43319e107b6c42551e6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54557436"
---
# <a name="iclrhostprotectionmanager-interface"></a><span data-ttu-id="f57b0-102">ICLRHostProtectionManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f57b0-102">ICLRHostProtectionManager Interface</span></span>
<span data-ttu-id="f57b0-103">特定のマネージ クラス、メソッド、プロパティ、およびフィールドを部分的に信頼されたコードでの実行をブロックするホストを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f57b0-103">Enables the host to block specific managed classes, methods, properties, and fields from running in partially trusted code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f57b0-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="f57b0-104">Methods</span></span>  
  
|<span data-ttu-id="f57b0-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="f57b0-105">Method</span></span>|<span data-ttu-id="f57b0-106">説明</span><span class="sxs-lookup"><span data-stu-id="f57b0-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f57b0-107">SetEagerSerializeGrantSets</span><span class="sxs-lookup"><span data-stu-id="f57b0-107">SetEagerSerializeGrantSets</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-seteagerserializegrantsets-method.md)|<span data-ttu-id="f57b0-108">致命的な共通言語ランタイム (CLR) のエラーが発生する特定のまれな競合条件が発生しないことの保証を提供します。</span><span class="sxs-lookup"><span data-stu-id="f57b0-108">Provides a guarantee that certain rare race conditions that can cause fatal common language runtime (CLR) errors will never arise.</span></span>|  
|[<span data-ttu-id="f57b0-109">SetProtectedCategories メソッド</span><span class="sxs-lookup"><span data-stu-id="f57b0-109">SetProtectedCategories Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-setprotectedcategories-method.md)|<span data-ttu-id="f57b0-110">マネージ型と部分的に信頼されたコードで実行されているを禁止するメンバーのカテゴリを指定します。</span><span class="sxs-lookup"><span data-stu-id="f57b0-110">Specifies the categories of managed types and members that should be blocked from running in partially trusted code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f57b0-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="f57b0-111">Requirements</span></span>  
 <span data-ttu-id="f57b0-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f57b0-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f57b0-113">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f57b0-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f57b0-114">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="f57b0-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f57b0-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f57b0-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f57b0-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="f57b0-116">See also</span></span>
- [<span data-ttu-id="f57b0-117">EApiCategories 列挙型</span><span class="sxs-lookup"><span data-stu-id="f57b0-117">EApiCategories Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eapicategories-enumeration.md)
- [<span data-ttu-id="f57b0-118">ICLRControl インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f57b0-118">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
