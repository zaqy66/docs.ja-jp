---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod メソッド
ms.date: 03/30/2017
ms.assetid: 4662f70d-817b-4374-8da8-e0545585939f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 38b4564aeb3c8ed4674e755e5691bb0a9d417bca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624177"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinekickoffmethod-method"></a><span data-ttu-id="7e65a-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod メソッド</span><span class="sxs-lookup"><span data-stu-id="7e65a-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod Method</span></span>
<span data-ttu-id="7e65a-103">非同期操作を開始する開始メソッドを設定します。</span><span class="sxs-lookup"><span data-stu-id="7e65a-103">Sets the starting method that initiates the async operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e65a-104">構文</span><span class="sxs-lookup"><span data-stu-id="7e65a-104">Syntax</span></span>  
  
```idl  
HRESULT DefineKickoffMethod(    [in] mdToken kickoffMethod);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7e65a-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7e65a-105">Parameters</span></span>  
  
|<span data-ttu-id="7e65a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7e65a-106">Parameter</span></span>|<span data-ttu-id="7e65a-107">説明</span><span class="sxs-lookup"><span data-stu-id="7e65a-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="7e65a-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="7e65a-108">Return Value</span></span>  
 <span data-ttu-id="7e65a-109">`HRESULT` を返します。</span><span class="sxs-lookup"><span data-stu-id="7e65a-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7e65a-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="7e65a-110">Requirements</span></span>  
 <span data-ttu-id="7e65a-111">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="7e65a-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e65a-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e65a-112">See also</span></span>
- [<span data-ttu-id="7e65a-113">ISymUnmanagedAsyncMethodPropertiesWriter インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7e65a-113">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
