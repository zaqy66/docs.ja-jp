---
title: SaveToHistory 関数 (WPF のアンマネージ API リファレンス)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- SaveToHistory
api_location:
- PresentationHost_v0400.dll
ms.assetid: 6dd101a3-44ad-4143-b228-772156f9b8ff
ms.openlocfilehash: 680c63548482c413a7ceff24a4f38eed589f4682
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745273"
---
# <a name="savetohistory-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="3ed77-102">SaveToHistory 関数 (WPF のアンマネージ API リファレンス)</span><span class="sxs-lookup"><span data-stu-id="3ed77-102">SaveToHistory Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="3ed77-103">この API は、Windows Presentation Foundation (WPF) インフラストラクチャをサポートしているし、コードから直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="3ed77-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="3ed77-104">Windows Presentation Foundation (WPF) インフラストラクチャによって windows の管理に使用します。</span><span class="sxs-lookup"><span data-stu-id="3ed77-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3ed77-105">構文</span><span class="sxs-lookup"><span data-stu-id="3ed77-105">Syntax</span></span>  
  
```cpp  
HRESULT SaveToHistory(  
   __in_ecount(1) IStream* pHistoryStream  
)  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3ed77-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3ed77-106">Parameters</span></span>  
 <span data-ttu-id="3ed77-107">pHistoryStream</span><span class="sxs-lookup"><span data-stu-id="3ed77-107">pHistoryStream</span></span>  
 <span data-ttu-id="3ed77-108">履歴のストリームへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3ed77-108">A pointer to the history stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3ed77-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="3ed77-109">Requirements</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3ed77-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="3ed77-110">Requirements</span></span>  
 <span data-ttu-id="3ed77-111">**プラットフォーム:** 参照してください[.NET Framework システム要件](../../../../docs/framework/get-started/system-requirements.md)します。</span><span class="sxs-lookup"><span data-stu-id="3ed77-111">**Platforms:** See [.NET Framework System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3ed77-112">**DLL:**</span><span class="sxs-lookup"><span data-stu-id="3ed77-112">**DLL:**</span></span>  
  
 <span data-ttu-id="3ed77-113">.NET framework 3.0 および 3.5。PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="3ed77-113">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="3ed77-114">.NET framework 4 以降では。PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="3ed77-114">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="3ed77-115">**.NET framework のバージョン:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3ed77-115">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ed77-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ed77-116">See also</span></span>
- [<span data-ttu-id="3ed77-117">WPF のアンマネージ API リファレンス</span><span class="sxs-lookup"><span data-stu-id="3ed77-117">WPF Unmanaged API Reference</span></span>](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
