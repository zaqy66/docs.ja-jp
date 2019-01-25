---
title: AXL_AUTHENTICODE_TIMESTAMPER_INFO 構造体
ms.date: 03/30/2017
ms.assetid: 89e41a81-0f41-45ad-8f20-a120e4ff24fb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d8060e95f06fd53ca985f84666cc81cfe49394fc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54659658"
---
# <a name="axlauthenticodetimestamperinfo-structure"></a><span data-ttu-id="7ff5c-102">AXL_AUTHENTICODE_TIMESTAMPER_INFO 構造体</span><span class="sxs-lookup"><span data-stu-id="7ff5c-102">AXL_AUTHENTICODE_TIMESTAMPER_INFO Structure</span></span>
<span data-ttu-id="7ff5c-103">Authenticode のタイム スタンパー情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="7ff5c-103">Defines the Authenticode time stamper information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7ff5c-104">構文</span><span class="sxs-lookup"><span data-stu-id="7ff5c-104">Syntax</span></span>  
  
```  
typedef struct _AXL_AUTHENTICODE_SIGNER_INFO {  
    DWORD cbSize;  
    HRESULT dwError;  
    ALG_ID algHash;  
    FILETIME ftTimestamp  
    PCCERT_CHAIN_CONTEXT pChainContext;  
} AXL_AUTHENTICODE_TIMESTAMPER_INFO, * PAXL_AUTHENTICODE_TIMESTAMPER_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="7ff5c-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="7ff5c-105">Members</span></span>  
  
|<span data-ttu-id="7ff5c-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="7ff5c-106">Member</span></span>|<span data-ttu-id="7ff5c-107">説明</span><span class="sxs-lookup"><span data-stu-id="7ff5c-107">Description</span></span>|  
|------------|-----------------|  
|`cbSize`|<span data-ttu-id="7ff5c-108">この構造のサイズ。</span><span class="sxs-lookup"><span data-stu-id="7ff5c-108">The size of this structure.</span></span>|  
|`dwError`|<span data-ttu-id="7ff5c-109">エラー コード。</span><span class="sxs-lookup"><span data-stu-id="7ff5c-109">The error code.</span></span>|  
|`algHash`|<span data-ttu-id="7ff5c-110">ハッシュアルゴリズム。</span><span class="sxs-lookup"><span data-stu-id="7ff5c-110">The hash algorithm.</span></span>|  
|`ftTimestamp`|<span data-ttu-id="7ff5c-111">タイム スタンプの時刻。</span><span class="sxs-lookup"><span data-stu-id="7ff5c-111">The time of the time stamp.</span></span>|  
|`pChainContext`|<span data-ttu-id="7ff5c-112">タイム スタンパーのチェーン コンテキスト。</span><span class="sxs-lookup"><span data-stu-id="7ff5c-112">The time stamper’s chain context.</span></span>  <span data-ttu-id="7ff5c-113">参照してください、 [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context)構造体。</span><span class="sxs-lookup"><span data-stu-id="7ff5c-113">See the [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) structure.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7ff5c-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="7ff5c-114">See also</span></span>
- [<span data-ttu-id="7ff5c-115">Authenticode</span><span class="sxs-lookup"><span data-stu-id="7ff5c-115">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
