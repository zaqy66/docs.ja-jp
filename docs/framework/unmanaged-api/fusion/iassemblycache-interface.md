---
title: IAssemblyCache インターフェイス
ms.date: 03/30/2017
api_name:
- IAssemblyCache
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache
helpviewer_keywords:
- IAssemblyCache interface [.NET Framework fusion]
ms.assetid: 71ea170f-872d-4fc5-81b6-27da1dec9b19
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 157cc9f5f520f376c0c055ab49b116bc7961f421
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54641071"
---
# <a name="iassemblycache-interface"></a><span data-ttu-id="d0283-102">IAssemblyCache インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d0283-102">IAssemblyCache Interface</span></span>
<span data-ttu-id="d0283-103">Fusion のテクノロジで使用するためのグローバル アセンブリ キャッシュを表します。</span><span class="sxs-lookup"><span data-stu-id="d0283-103">Represents the global assembly cache for use by the fusion technology.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d0283-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="d0283-104">Methods</span></span>  
  
|<span data-ttu-id="d0283-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="d0283-105">Method</span></span>|<span data-ttu-id="d0283-106">説明</span><span class="sxs-lookup"><span data-stu-id="d0283-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d0283-107">CreateAssemblyCacheItem メソッド</span><span class="sxs-lookup"><span data-stu-id="d0283-107">CreateAssemblyCacheItem Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-createassemblycacheitem-method.md)|<span data-ttu-id="d0283-108">新しいへの参照を取得します。 [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md)します。</span><span class="sxs-lookup"><span data-stu-id="d0283-108">Gets a reference to a new [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md).</span></span>|  
|[<span data-ttu-id="d0283-109">CreateAssemblyScavenger メソッド</span><span class="sxs-lookup"><span data-stu-id="d0283-109">CreateAssemblyScavenger Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-createassemblyscavenger-method.md)|<span data-ttu-id="d0283-110">Fusion のテクノロジでは、内部使用のため予約されています。</span><span class="sxs-lookup"><span data-stu-id="d0283-110">Reserved for internal use by the fusion technology.</span></span>|  
|[<span data-ttu-id="d0283-111">InstallAssembly メソッド</span><span class="sxs-lookup"><span data-stu-id="d0283-111">InstallAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-installassembly-method.md)|<span data-ttu-id="d0283-112">指定したアセンブリをグローバル アセンブリ キャッシュにインストールします。</span><span class="sxs-lookup"><span data-stu-id="d0283-112">Installs the specified assembly in the global assembly cache.</span></span>|  
|[<span data-ttu-id="d0283-113">QueryAssemblyInfo メソッド</span><span class="sxs-lookup"><span data-stu-id="d0283-113">QueryAssemblyInfo Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-queryassemblyinfo-method.md)|<span data-ttu-id="d0283-114">指定したアセンブリについて、要求されたデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="d0283-114">Gets the requested data about the specified assembly.</span></span>|  
|[<span data-ttu-id="d0283-115">UninstallAssembly メソッド</span><span class="sxs-lookup"><span data-stu-id="d0283-115">UninstallAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-uninstallassembly-method.md)|<span data-ttu-id="d0283-116">指定したアセンブリをグローバル アセンブリ キャッシュからアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="d0283-116">Uninstalls the specified assembly from the global assembly cache.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d0283-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="d0283-117">Requirements</span></span>  
 <span data-ttu-id="d0283-118">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0283-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0283-119">**ヘッダー:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="d0283-119">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="d0283-120">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d0283-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0283-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="d0283-121">See also</span></span>
- [<span data-ttu-id="d0283-122">Fusion インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d0283-122">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [<span data-ttu-id="d0283-123">グローバル アセンブリ キャッシュ</span><span class="sxs-lookup"><span data-stu-id="d0283-123">Global Assembly Cache</span></span>](../../../../docs/framework/app-domains/gac.md)
