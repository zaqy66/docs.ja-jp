---
title: COINITIEE 列挙型
ms.date: 03/30/2017
api_name:
- COINITIEE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COINITIEE
helpviewer_keywords:
- COINITIEE enumeration [.NET Framework metadata]
ms.assetid: 64264238-3b68-4bac-a887-36b552426a6c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 48f15cc08167baaadc61787b8b1f7167304f0cae
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54569480"
---
# <a name="coinitiee-enumeration"></a><span data-ttu-id="d030b-102">COINITIEE 列挙型</span><span class="sxs-lookup"><span data-stu-id="d030b-102">COINITIEE Enumeration</span></span>
<span data-ttu-id="d030b-103">使用される定数を指定します[CoInitializeEE](../../../../docs/framework/unmanaged-api/hosting/coinitializeee-function.md)共通言語ランタイムを初期化するときにします。</span><span class="sxs-lookup"><span data-stu-id="d030b-103">Specifies constants used by [CoInitializeEE](../../../../docs/framework/unmanaged-api/hosting/coinitializeee-function.md) when initializing the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d030b-104">構文</span><span class="sxs-lookup"><span data-stu-id="d030b-104">Syntax</span></span>  
  
```  
typedef enum tagCOINITEE {  
   COINITEE_DEFAULT = 0x0,  
   COINITEE_DLL     = 0x1,  
   COINITEE_MAIN    = 0x2  
} COINITIEE;  
```  
  
## <a name="members"></a><span data-ttu-id="d030b-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="d030b-105">Members</span></span>  
  
|<span data-ttu-id="d030b-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="d030b-106">Member</span></span>|<span data-ttu-id="d030b-107">説明</span><span class="sxs-lookup"><span data-stu-id="d030b-107">Description</span></span>|  
|------------|-----------------|  
|`COINITEE_DEFAULT`|<span data-ttu-id="d030b-108">既定の初期化モード。</span><span class="sxs-lookup"><span data-stu-id="d030b-108">Default initialization mode.</span></span> <span data-ttu-id="d030b-109">ランタイムを初期化し、既定値を作成します。 この<xref:System.AppDomain>します。</span><span class="sxs-lookup"><span data-stu-id="d030b-109">This initializes the runtime and creates the default <xref:System.AppDomain>.</span></span>|  
|`COINITEE_DLL`|<span data-ttu-id="d030b-110">マネージ DLL を実行することを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d030b-110">Initializes to run a managed DLL.</span></span>|  
|`COINITEE_MAIN`|<span data-ttu-id="d030b-111">マネージ EXE を実行することを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d030b-111">Initializes to run a managed EXE.</span></span> <span data-ttu-id="d030b-112">これは、ランタイムを初期化しますが、既定値は作成されません<xref:System.AppDomain>、これは、exe ファイルのメイン ルーチンを入力した後に作成されます。</span><span class="sxs-lookup"><span data-stu-id="d030b-112">This initializes the runtime but does not create the default <xref:System.AppDomain>, which is created after entering the main routine of the EXE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d030b-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="d030b-113">Requirements</span></span>  
 <span data-ttu-id="d030b-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d030b-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d030b-115">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d030b-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d030b-116">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="d030b-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d030b-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d030b-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d030b-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="d030b-118">See also</span></span>
- [<span data-ttu-id="d030b-119">メタデータ列挙型</span><span class="sxs-lookup"><span data-stu-id="d030b-119">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
