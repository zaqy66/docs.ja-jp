---
title: VerifyClientKey 関数 (アンマネージ API リファレンス)
description: VerifyClientKey 関数により、クライアント キーが適切なセキュリティ。
ms.date: 11/06/2017
api_name:
- VerifyClientKey
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- VerifyClientKey
helpviewer_keywords:
- VerifyClientKey function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 94d601125049f0c215b3b03bf8b13d2959872c3d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54711760"
---
# <a name="verifyclientkey-function"></a><span data-ttu-id="804d5-103">VerifyClientKey 関数</span><span class="sxs-lookup"><span data-stu-id="804d5-103">VerifyClientKey function</span></span>
<span data-ttu-id="804d5-104">クライアント キーに適切なセキュリティが確実に含められます。</span><span class="sxs-lookup"><span data-stu-id="804d5-104">Ensures that the client key has the correct security.</span></span>  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="804d5-105">構文</span><span class="sxs-lookup"><span data-stu-id="804d5-105">Syntax</span></span>  
  
```  
LONG VerifyClientKey(); 
```  

## <a name="return-value"></a><span data-ttu-id="804d5-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="804d5-106">Return value</span></span>

<span data-ttu-id="804d5-107">関数が成功した場合、戻り値は`ERROR_SUCCESS`(0)。</span><span class="sxs-lookup"><span data-stu-id="804d5-107">If the function succeeds, the return value is `ERROR_SUCCESS` (0).</span></span>

<span data-ttu-id="804d5-108">戻り値で定義されたゼロ以外のエラー コードは、関数が失敗した場合、 *WinError.h*します。</span><span class="sxs-lookup"><span data-stu-id="804d5-108">If the function fails, the return value is a non-zero error code defined in *WinError.h*.</span></span>

## <a name="requirements"></a><span data-ttu-id="804d5-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="804d5-109">Requirements</span></span>  
 <span data-ttu-id="804d5-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="804d5-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="804d5-111">**ヘッダー:** WMINet_Utils.def</span><span class="sxs-lookup"><span data-stu-id="804d5-111">**Header:** WMINet_Utils.def</span></span>  
  
 <span data-ttu-id="804d5-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="804d5-112">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="804d5-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="804d5-113">See also</span></span>
- [<span data-ttu-id="804d5-114">WMI およびパフォーマンス カウンター (アンマネージ API リファレンス)</span><span class="sxs-lookup"><span data-stu-id="804d5-114">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
