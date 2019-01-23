---
title: ISymUnmanagedAsyncMethod::IsAsyncMethod メソッド
ms.date: 03/30/2017
ms.assetid: 670a7653-dac6-4171-98ee-d669e3adf4b2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 049f8e4d04498b70533134c01765af2d996d86dc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499107"
---
# <a name="isymunmanagedasyncmethodisasyncmethod-method"></a><span data-ttu-id="f2639-102">ISymUnmanagedAsyncMethod::IsAsyncMethod メソッド</span><span class="sxs-lookup"><span data-stu-id="f2639-102">ISymUnmanagedAsyncMethod::IsAsyncMethod Method</span></span>
<span data-ttu-id="f2639-103">かどうかのかどうか、メソッドは非同期の情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="f2639-103">Checks if the method has async information or not.</span></span>  
  
 <span data-ttu-id="f2639-104">このメソッドが戻る場合`FALSE`し、このインターフェイスで、他のメソッドを呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="f2639-104">If this method returns `FALSE` then it is invalid to call any other methods in this interface.</span></span> <span data-ttu-id="f2639-105">すべての戻り値は`E_UNEXPECTED`ここでします。</span><span class="sxs-lookup"><span data-stu-id="f2639-105">They will all return `E_UNEXPECTED` in this case.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2639-106">構文</span><span class="sxs-lookup"><span data-stu-id="f2639-106">Syntax</span></span>  
  
```idl  
HRESULT IsAsyncMethod(    [out, retval] BOOL* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f2639-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f2639-107">Parameters</span></span>  
  
|<span data-ttu-id="f2639-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f2639-108">Parameter</span></span>|<span data-ttu-id="f2639-109">説明</span><span class="sxs-lookup"><span data-stu-id="f2639-109">Description</span></span>|  
|---------------|-----------------|  
|`pRetVal`||  
  
## <a name="return-value"></a><span data-ttu-id="f2639-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="f2639-110">Return Value</span></span>  
 <span data-ttu-id="f2639-111">`HRESULT` を返します。</span><span class="sxs-lookup"><span data-stu-id="f2639-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2639-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="f2639-112">Requirements</span></span>  
 <span data-ttu-id="f2639-113">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f2639-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2639-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2639-114">See also</span></span>
- [<span data-ttu-id="f2639-115">ISymUnmanagedAsyncMethod インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f2639-115">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
