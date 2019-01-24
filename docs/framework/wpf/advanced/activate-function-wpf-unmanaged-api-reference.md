---
title: Activate 関数 (WPF のアンマネージ API リファレンス)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- Acrivate
api_location:
- PresentationHost_v0400.dll
ms.assetid: 1400329c-b598-465f-80f2-e3dabf044811
ms.openlocfilehash: 4e79b74dc8bb7d57125c27e17e8f52d607fffcf1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54721998"
---
# <a name="activate-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="41bd3-102">Activate 関数 (WPF のアンマネージ API リファレンス)</span><span class="sxs-lookup"><span data-stu-id="41bd3-102">Activate Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="41bd3-103">この API は、Windows Presentation Foundation (WPF) インフラストラクチャをサポートしているし、コードから直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="41bd3-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="41bd3-104">Windows Presentation Foundation (WPF) インフラストラクチャによって windows の管理に使用します。</span><span class="sxs-lookup"><span data-stu-id="41bd3-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41bd3-105">構文</span><span class="sxs-lookup"><span data-stu-id="41bd3-105">Syntax</span></span>  
  
```cpp  
void Activate(  
    const ActivateParameters* pParameters,  
    __deref_out_ecount(1) LPUNKNOWN* ppInner,  
    );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="41bd3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="41bd3-106">Parameters</span></span>  
 <span data-ttu-id="41bd3-107">pParameters</span><span class="sxs-lookup"><span data-stu-id="41bd3-107">pParameters</span></span>  
 <span data-ttu-id="41bd3-108">ウィンドウのアクティブ化パラメーターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="41bd3-108">A pointer to the window's activation parameters.</span></span>  
  
 <span data-ttu-id="41bd3-109">ppInner</span><span class="sxs-lookup"><span data-stu-id="41bd3-109">ppInner</span></span>  
 <span data-ttu-id="41bd3-110">ポインターを格納している 1 つの要素のバッファーのアドレスへのポインター、<xref:Microsoft.VisualStudio.OLE.Interop.IOleDocument>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="41bd3-110">A pointer to the address of a single-element buffer that contains a pointer to an <xref:Microsoft.VisualStudio.OLE.Interop.IOleDocument> object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="41bd3-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="41bd3-111">Requirements</span></span>  
 <span data-ttu-id="41bd3-112">**プラットフォーム:** 参照してください[.NET Framework システム要件](../../../../docs/framework/get-started/system-requirements.md)します。</span><span class="sxs-lookup"><span data-stu-id="41bd3-112">**Platforms:** See [.NET Framework System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="41bd3-113">**DLL:**</span><span class="sxs-lookup"><span data-stu-id="41bd3-113">**DLL:**</span></span>  
  
 <span data-ttu-id="41bd3-114">.NET framework 3.0 および 3.5。PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="41bd3-114">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="41bd3-115">.NET framework 4 以降では。PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="41bd3-115">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="41bd3-116">**.NET framework のバージョン:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="41bd3-116">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41bd3-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="41bd3-117">See also</span></span>
- [<span data-ttu-id="41bd3-118">WPF のアンマネージ API リファレンス</span><span class="sxs-lookup"><span data-stu-id="41bd3-118">WPF Unmanaged API Reference</span></span>](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
