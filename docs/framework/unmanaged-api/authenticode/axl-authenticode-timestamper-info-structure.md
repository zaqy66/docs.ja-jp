---
title: AXL_AUTHENTICODE_TIMESTAMPER_INFO 構造体
ms.date: 03/30/2017
ms.assetid: 89e41a81-0f41-45ad-8f20-a120e4ff24fb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d7f4fff4f2c2b3dd04625f4cf50b8b19a0ef6f39
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43525082"
---
# <a name="axlauthenticodetimestamperinfo-structure"></a><span data-ttu-id="bf409-102">AXL_AUTHENTICODE_TIMESTAMPER_INFO 構造体</span><span class="sxs-lookup"><span data-stu-id="bf409-102">AXL_AUTHENTICODE_TIMESTAMPER_INFO Structure</span></span>
<span data-ttu-id="bf409-103">Authenticode のタイム スタンパー情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="bf409-103">Defines the Authenticode time stamper information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bf409-104">構文</span><span class="sxs-lookup"><span data-stu-id="bf409-104">Syntax</span></span>  
  
```  
typedef struct _AXL_AUTHENTICODE_SIGNER_INFO {  
    DWORD cbSize;  
    HRESULT dwError;  
    ALG_ID algHash;  
    FILETIME ftTimestamp  
    PCCERT_CHAIN_CONTEXT pChainContext;  
} AXL_AUTHENTICODE_TIMESTAMPER_INFO, * PAXL_AUTHENTICODE_TIMESTAMPER_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="bf409-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="bf409-105">Members</span></span>  
  
|<span data-ttu-id="bf409-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="bf409-106">Member</span></span>|<span data-ttu-id="bf409-107">説明</span><span class="sxs-lookup"><span data-stu-id="bf409-107">Description</span></span>|  
|------------|-----------------|  
|`cbSize`|<span data-ttu-id="bf409-108">この構造のサイズ。</span><span class="sxs-lookup"><span data-stu-id="bf409-108">The size of this structure.</span></span>|  
|`dwError`|<span data-ttu-id="bf409-109">エラー コード。</span><span class="sxs-lookup"><span data-stu-id="bf409-109">The error code.</span></span>|  
|`algHash`|<span data-ttu-id="bf409-110">ハッシュアルゴリズム。</span><span class="sxs-lookup"><span data-stu-id="bf409-110">The hash algorithm.</span></span>|  
|`ftTimestamp`|<span data-ttu-id="bf409-111">タイム スタンプの時刻。</span><span class="sxs-lookup"><span data-stu-id="bf409-111">The time of the time stamp.</span></span>|  
|`pChainContext`|<span data-ttu-id="bf409-112">タイム スタンパーのチェーン コンテキスト。</span><span class="sxs-lookup"><span data-stu-id="bf409-112">The time stamper’s chain context.</span></span>  <span data-ttu-id="bf409-113">参照してください、 [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context)構造体。</span><span class="sxs-lookup"><span data-stu-id="bf409-113">See the [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) structure.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="bf409-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf409-114">See Also</span></span>  
 [<span data-ttu-id="bf409-115">Authenticode</span><span class="sxs-lookup"><span data-stu-id="bf409-115">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
