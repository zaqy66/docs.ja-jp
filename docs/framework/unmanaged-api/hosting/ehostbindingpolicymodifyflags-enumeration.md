---
title: EHostBindingPolicyModifyFlags 列挙型
ms.date: 03/30/2017
api_name:
- EHostBindingPolicyModifyFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EHostBindingPolicyModifyFlags
helpviewer_keywords:
- EHostBindingPolicyModifyFlags enumeration [.NET Framework hosting]
ms.assetid: 0339af16-ee1d-48ec-837d-a79d9a9c89f8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b3aba84f1ae451ee943028d063e91ca7a6d63548
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504695"
---
# <a name="ehostbindingpolicymodifyflags-enumeration"></a><span data-ttu-id="fd53d-102">EHostBindingPolicyModifyFlags 列挙型</span><span class="sxs-lookup"><span data-stu-id="fd53d-102">EHostBindingPolicyModifyFlags Enumeration</span></span>
<span data-ttu-id="fd53d-103">により、ホストは、ターゲット アセンブリにソース アセンブリからポリシーの変更を適用するときに、共通言語ランタイム (CLR) を実行する必要がありますのリダイレクトの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd53d-103">Allows the host to specify the type of redirection the common language runtime (CLR) should perform when applying policy modifications from a source assembly to a target assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd53d-104">構文</span><span class="sxs-lookup"><span data-stu-id="fd53d-104">Syntax</span></span>  
  
```  
typedef enum _hostBindingPolicyModifyFlags {  
    HOST_BINDING_POLICY_MODIFY_DEFAULT  = 0,  
    HOST_BINDING_POLICY_MODIFY_CHAIN    = 1,  
    HOST_BINDING_POLICY_MODIFY_REMOVE   = 2,  
    HOST_BINDING_POLICY_MODIFY_MAX      = 3  
} EHostBindingPolicyModifyFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="fd53d-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="fd53d-105">Members</span></span>  
  
|<span data-ttu-id="fd53d-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="fd53d-106">Member</span></span>|<span data-ttu-id="fd53d-107">説明</span><span class="sxs-lookup"><span data-stu-id="fd53d-107">Description</span></span>|  
|------------|-----------------|  
|`HOST_BINDING_POLICY_MODIFY_CHAIN`|<span data-ttu-id="fd53d-108">CLR がターゲット アセンブリの上にソース アセンブリのポリシー値をチェーンするを指定します。</span><span class="sxs-lookup"><span data-stu-id="fd53d-108">Specifies that the CLR will chain policy values of the source assembly onto those of the target assembly.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_DEFAULT`|<span data-ttu-id="fd53d-109">CLR が既定のアクションを実行することを指定します。</span><span class="sxs-lookup"><span data-stu-id="fd53d-109">Specifies that the CLR will perform the default action.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_MAX`|<span data-ttu-id="fd53d-110">CLR が最大値にターゲット アセンブリのポリシー値を設定するを指定します。</span><span class="sxs-lookup"><span data-stu-id="fd53d-110">Specifies that the CLR will set the policy values of the target assembly to the maximum values.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_REMOVE`|<span data-ttu-id="fd53d-111">CLR がソース アセンブリのターゲット アセンブリのポリシー値を置き換えることを指定します。</span><span class="sxs-lookup"><span data-stu-id="fd53d-111">Specifies that the CLR will replace policy values of the target assembly with those of the source assembly.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fd53d-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="fd53d-112">Remarks</span></span>  
 <span data-ttu-id="fd53d-113">[Iclrhostbindingpolicymanager::modifyapplicationpolicy](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md)メソッドは、型のパラメーターを受け取る`EHostBindingPolicyModifyFlags`します。</span><span class="sxs-lookup"><span data-stu-id="fd53d-113">The [ICLRHostBindingPolicyManager::ModifyApplicationPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md) method takes a parameter of type `EHostBindingPolicyModifyFlags`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd53d-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="fd53d-114">Requirements</span></span>  
 <span data-ttu-id="fd53d-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd53d-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fd53d-116">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="fd53d-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fd53d-117">**ライブラリ:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fd53d-117">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fd53d-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd53d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd53d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd53d-119">See also</span></span>
- [<span data-ttu-id="fd53d-120">ICLRHostBindingPolicyManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fd53d-120">ICLRHostBindingPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md)
- [<span data-ttu-id="fd53d-121">ホスティングの列挙型</span><span class="sxs-lookup"><span data-stu-id="fd53d-121">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
