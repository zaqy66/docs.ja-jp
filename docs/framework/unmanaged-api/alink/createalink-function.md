---
title: CreateALink 関数
ms.date: 03/30/2017
api_name:
- CreateALink
api_location:
- alink.dll
api_type:
- DLLExport
f1_keywords:
- CreateALink
helpviewer_keywords:
- CreateALink function
- Alink API, CreateALink function
ms.assetid: fc73bcb9-6af6-44d8-bc39-2f4400325dae
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f809395de68b596f769f9396da8668bf296b1aa2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54675042"
---
# <a name="createalink-function"></a><span data-ttu-id="c195b-102">CreateALink 関数</span><span class="sxs-lookup"><span data-stu-id="c195b-102">CreateALink Function</span></span>
<span data-ttu-id="c195b-103">アセンブリ リンカーのインスタンスを作成し、指定したインターフェイスへのポインターを設定します。</span><span class="sxs-lookup"><span data-stu-id="c195b-103">Creates an instance of the Assembly Linker and sets a pointer to the specified interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c195b-104">構文</span><span class="sxs-lookup"><span data-stu-id="c195b-104">Syntax</span></span>  
  
```  
HRESULT CreateALink (  
   REFIID riid,  
   IUnknown **ppInterface  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c195b-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c195b-105">Parameters</span></span>  
  
|<span data-ttu-id="c195b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c195b-106">Parameter</span></span>|<span data-ttu-id="c195b-107">説明</span><span class="sxs-lookup"><span data-stu-id="c195b-107">Description</span></span>|  
|---------------|-----------------|  
|`riid`|<span data-ttu-id="c195b-108">アセンブリ リンカー インターフェイスの 1 つの物理名。</span><span class="sxs-lookup"><span data-stu-id="c195b-108">The physical name of one of the Assembly Linker interfaces.</span></span>|  
|`ppInterface`|<span data-ttu-id="c195b-109">正常に完了へのポインターを格納する場所、`riid`インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="c195b-109">The location that on successful completion contains a pointer to the `riid` interface.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c195b-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="c195b-110">Requirements</span></span>  
 <span data-ttu-id="c195b-111">**ライブラリ**: alink.dll</span><span class="sxs-lookup"><span data-stu-id="c195b-111">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c195b-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="c195b-112">See also</span></span>
- [<span data-ttu-id="c195b-113">Al.exe (アセンブリ リンカー)</span><span class="sxs-lookup"><span data-stu-id="c195b-113">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)
