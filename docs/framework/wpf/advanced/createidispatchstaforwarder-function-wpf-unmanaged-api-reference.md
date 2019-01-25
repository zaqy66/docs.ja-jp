---
title: CreateIDispatchSTAForwarder 関数 (WPF のアンマネージ API リファレンス)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CreateIDispatchSTAForwarder
api_location:
- PresentationHost_v0400.dll
ms.assetid: 57a02dfa-f091-4ace-9c06-1f4ab52b3527
ms.openlocfilehash: 215f6ff727b814e7e7d7c708c29a8c5221f5797f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54575983"
---
# <a name="createidispatchstaforwarder-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="b41ab-102">CreateIDispatchSTAForwarder 関数 (WPF のアンマネージ API リファレンス)</span><span class="sxs-lookup"><span data-stu-id="b41ab-102">CreateIDispatchSTAForwarder Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="b41ab-103">この API は、Windows Presentation Foundation (WPF) インフラストラクチャをサポートしているし、コードから直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="b41ab-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="b41ab-104">Windows Presentation Foundation (WPF) インフラストラクチャによってスレッドと windows の管理に使用します。</span><span class="sxs-lookup"><span data-stu-id="b41ab-104">Used by the Windows Presentation Foundation (WPF) infrastructure for thread and windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b41ab-105">構文</span><span class="sxs-lookup"><span data-stu-id="b41ab-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateIDispatchSTAForwarder(  
   __in IDispatch *pDispatchDelegate,   
   __deref_out IDispatch **ppForwarder  
)  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b41ab-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b41ab-106">Parameters</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b41ab-107">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="b41ab-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="b41ab-108">pDispatchDelegate</span><span class="sxs-lookup"><span data-stu-id="b41ab-108">pDispatchDelegate</span></span>  
 <span data-ttu-id="b41ab-109">ポインター、`IDispatch`インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="b41ab-109">A pointer to an `IDispatch` interface.</span></span>  
  
 <span data-ttu-id="b41ab-110">ppForwarder</span><span class="sxs-lookup"><span data-stu-id="b41ab-110">ppForwarder</span></span>  
 <span data-ttu-id="b41ab-111">アドレスへのポインター、`IDispatch`インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="b41ab-111">A pointer to the address of an `IDispatch` interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b41ab-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="b41ab-112">Requirements</span></span>  
 <span data-ttu-id="b41ab-113">**プラットフォーム:** 参照してください[.NET Framework システム要件](../../../../docs/framework/get-started/system-requirements.md)します。</span><span class="sxs-lookup"><span data-stu-id="b41ab-113">**Platforms:** See [.NET Framework System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b41ab-114">**DLL:**</span><span class="sxs-lookup"><span data-stu-id="b41ab-114">**DLL:**</span></span>  
  
 <span data-ttu-id="b41ab-115">.NET framework 3.0 および 3.5。PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="b41ab-115">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="b41ab-116">.NET framework 4 以降では。PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="b41ab-116">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="b41ab-117">**.NET framework のバージョン:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b41ab-117">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b41ab-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="b41ab-118">See also</span></span>
- [<span data-ttu-id="b41ab-119">WPF のアンマネージ API リファレンス</span><span class="sxs-lookup"><span data-stu-id="b41ab-119">WPF Unmanaged API Reference</span></span>](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
