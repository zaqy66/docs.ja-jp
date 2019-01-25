---
title: ESymbolReadingPolicy 列挙型
ms.date: 03/30/2017
api_name:
- ESymbolReadingPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ESymbolReadingPolicy
helpviewer_keywords:
- ESymbolReadingPolicy enumeration [.NET Framework hosting]
ms.assetid: 4dc6c80d-b694-480b-a378-d5b18420ce17
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e17f88cf7f0d8572e65d00d8500a1fd83aa44eeb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663915"
---
# <a name="esymbolreadingpolicy-enumeration"></a><span data-ttu-id="1d235-102">ESymbolReadingPolicy 列挙型</span><span class="sxs-lookup"><span data-stu-id="1d235-102">ESymbolReadingPolicy Enumeration</span></span>
<span data-ttu-id="1d235-103">プログラム データベース (PDB) ファイルを読み取るためのポリシーを設定する値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d235-103">Contains values that set the policy for reading program database (PDB) files.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1d235-104">構文</span><span class="sxs-lookup"><span data-stu-id="1d235-104">Syntax</span></span>  
  
```  
typedef enum {  
    eSymbolReadingNever,  
    eSymbolReadingAlways,  
    eSymbolReadingFullTrustOnly  
} ESymbolReadingPolicy;  
```  
  
## <a name="members"></a><span data-ttu-id="1d235-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="1d235-105">Members</span></span>  
  
|<span data-ttu-id="1d235-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="1d235-106">Member</span></span>|<span data-ttu-id="1d235-107">説明</span><span class="sxs-lookup"><span data-stu-id="1d235-107">Description</span></span>|  
|------------|-----------------|  
|`eSymbolReadingAlways`|<span data-ttu-id="1d235-108">デバッガーが PDB ファイルを常に読み取ることを指定します。</span><span class="sxs-lookup"><span data-stu-id="1d235-108">Specifies that the debugger should always read PDB files.</span></span>|  
|`eSymbolReadingFullTrustOnly`|<span data-ttu-id="1d235-109">デバッガーが完全に信頼されたアセンブリに関連付けられた PDB ファイルのみを読み取ることを指定します。</span><span class="sxs-lookup"><span data-stu-id="1d235-109">Specifies that the debugger should read only PDB files that are associated with full-trust assemblies.</span></span>|  
|`eSymbolReadingNever`|<span data-ttu-id="1d235-110">デバッガーが PDB ファイルを読み取るしないことを指定します。</span><span class="sxs-lookup"><span data-stu-id="1d235-110">Specifies that the debugger should never read PDB files.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1d235-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="1d235-111">Remarks</span></span>  
 <span data-ttu-id="1d235-112">`ESymbolReadingPolicy`列挙で使用されますが、 [iclrdebugmanager::setsymbolreadingpolicy](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setsymbolreadingpolicy-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="1d235-112">The `ESymbolReadingPolicy` enumeration is used with the [ICLRDebugManager::SetSymbolReadingPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setsymbolreadingpolicy-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1d235-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="1d235-113">Requirements</span></span>  
 <span data-ttu-id="1d235-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d235-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1d235-115">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1d235-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1d235-116">**ライブラリ:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1d235-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1d235-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1d235-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d235-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d235-118">See also</span></span>
- [<span data-ttu-id="1d235-119">ホスティングの列挙型</span><span class="sxs-lookup"><span data-stu-id="1d235-119">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
