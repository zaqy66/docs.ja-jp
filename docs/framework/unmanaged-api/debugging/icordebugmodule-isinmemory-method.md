---
title: ICorDebugModule::IsInMemory メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugModule.IsInMemory
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::IsInMemory
helpviewer_keywords:
- IsInMemory method [.NET Framework debugging]
- ICorDebugModule::IsInMemory method [.NET Framework debugging]
ms.assetid: 89940711-98e7-4aa6-bffc-5e39e91e1b7d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f7bfdcc3c8328d71146732fc4ba5664ebee9bea2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574873"
---
# <a name="icordebugmoduleisinmemory-method"></a><span data-ttu-id="2a944-102">ICorDebugModule::IsInMemory メソッド</span><span class="sxs-lookup"><span data-stu-id="2a944-102">ICorDebugModule::IsInMemory Method</span></span>
<span data-ttu-id="2a944-103">このモジュールは、メモリ内にのみ存在するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2a944-103">Gets a value that indicates whether this module exists only in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a944-104">構文</span><span class="sxs-lookup"><span data-stu-id="2a944-104">Syntax</span></span>  
  
```  
HRESULT IsInMemory(  
    [out] BOOL *pInMemory  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2a944-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2a944-105">Parameters</span></span>  
 `pInMemory`  
 <span data-ttu-id="2a944-106">[out]`true`メモリ内でのみこのモジュールが存在する場合は、それ以外の場合、`false`します。</span><span class="sxs-lookup"><span data-stu-id="2a944-106">[out] `true` if this module exists only in memory; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2a944-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="2a944-107">Remarks</span></span>  
 <span data-ttu-id="2a944-108">共通言語ランタイム (CLR) は、生のバイト ストリームからのモジュールの読み込みをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2a944-108">The common language runtime (CLR) supports the loading of modules from raw streams of bytes.</span></span> <span data-ttu-id="2a944-109">このようなモジュールが呼び出されます*メモリ内モジュール*ディスク上に存在しないとします。</span><span class="sxs-lookup"><span data-stu-id="2a944-109">Such modules are called *in-memory modules* and do not exist on disk.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2a944-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="2a944-110">Requirements</span></span>  
 <span data-ttu-id="2a944-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a944-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2a944-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2a944-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2a944-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2a944-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2a944-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2a944-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a944-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a944-115">See also</span></span>


