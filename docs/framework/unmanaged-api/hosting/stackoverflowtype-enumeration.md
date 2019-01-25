---
title: StackOverflowType 列挙型
ms.date: 03/30/2017
api_name:
- StackOverflowType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StackOverflowType
helpviewer_keywords:
- StackOverflowType enumeration [.NET Framework hosting]
ms.assetid: dab648ad-972b-479c-b129-b4c1dcbd932e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 06c9119a2b842a0efcd4af752ba72dbfda03bf13
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54653863"
---
# <a name="stackoverflowtype-enumeration"></a><span data-ttu-id="176db-102">StackOverflowType 列挙型</span><span class="sxs-lookup"><span data-stu-id="176db-102">StackOverflowType Enumeration</span></span>
<span data-ttu-id="176db-103">スタック オーバーフローのイベントの根本原因を示す値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="176db-103">Contains values that indicate the underlying cause of a stack overflow event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="176db-104">構文</span><span class="sxs-lookup"><span data-stu-id="176db-104">Syntax</span></span>  
  
```  
typedef enum {  
    SO_Managed,  
    SO_ClrEngine,  
    SO_Other  
} StackOverflowType;  
```  
  
## <a name="members"></a><span data-ttu-id="176db-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="176db-105">Members</span></span>  
  
|<span data-ttu-id="176db-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="176db-106">Member</span></span>|<span data-ttu-id="176db-107">説明</span><span class="sxs-lookup"><span data-stu-id="176db-107">Description</span></span>|  
|------------|-----------------|  
|`SO_ClrEngine`|<span data-ttu-id="176db-108">実行エンジンは、スタック オーバーフローが原因です。</span><span class="sxs-lookup"><span data-stu-id="176db-108">The stack overflow was caused by the execution engine.</span></span>|  
|`SO_Managed`|<span data-ttu-id="176db-109">マネージ コードによってスタック オーバーフローが発生しました。</span><span class="sxs-lookup"><span data-stu-id="176db-109">The stack overflow was caused by managed code.</span></span>|  
|`SO_Other`|<span data-ttu-id="176db-110">アンマネージ コードによってスタック オーバーフローが発生しました。</span><span class="sxs-lookup"><span data-stu-id="176db-110">The stack overflow was caused by unmanaged code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="176db-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="176db-111">Remarks</span></span>  
 <span data-ttu-id="176db-112">この情報を呼び出すことによって、ホストに渡される、 [iactiononclrevent::onevent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="176db-112">This information is passed to the host through a call to the [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="176db-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="176db-113">Requirements</span></span>  
 <span data-ttu-id="176db-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="176db-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="176db-115">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="176db-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="176db-116">**ライブラリ:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="176db-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="176db-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="176db-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="176db-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="176db-118">See also</span></span>
- [<span data-ttu-id="176db-119">ホスティングの列挙型</span><span class="sxs-lookup"><span data-stu-id="176db-119">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
