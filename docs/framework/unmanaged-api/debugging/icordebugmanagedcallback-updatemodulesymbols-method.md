---
title: ICorDebugManagedCallback::UpdateModuleSymbols メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.UpdateModuleSymbols
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::UpdateModuleSymbols
helpviewer_keywords:
- UpdateModuleSymbols method [.NET Framework debugging]
- ICorDebugManagedCallback::UpdateModuleSymbols method [.NET Framework debugging]
ms.assetid: 0863f644-58e8-45a0-b0c3-a28e99b20938
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7b66cc09eda1fe5ea46a55b6239e05b5acec851c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54566906"
---
# <a name="icordebugmanagedcallbackupdatemodulesymbols-method"></a><span data-ttu-id="05f25-102">ICorDebugManagedCallback::UpdateModuleSymbols メソッド</span><span class="sxs-lookup"><span data-stu-id="05f25-102">ICorDebugManagedCallback::UpdateModuleSymbols Method</span></span>
<span data-ttu-id="05f25-103">共通言語ランタイム モジュールのシンボルが変更されたことをデバッガーに通知します。</span><span class="sxs-lookup"><span data-stu-id="05f25-103">Notifies the debugger that the symbols for a common language runtime module have changed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05f25-104">構文</span><span class="sxs-lookup"><span data-stu-id="05f25-104">Syntax</span></span>  
  
```  
HRESULT UpdateModuleSymbols (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugModule    *pModule,  
    [in] IStream            *pSymbolStream  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="05f25-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="05f25-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="05f25-106">[in]シンボルが変更されたが、モジュールを格納しているアプリケーション ドメインを表す ICorDebugAppDomain オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="05f25-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain containing the module in which the symbols have changed.</span></span>  
  
 `pModule`  
 <span data-ttu-id="05f25-107">[in]シンボルが変更されたが、モジュールを表す ICorDebugModule オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="05f25-107">[in] A pointer to an ICorDebugModule object that represents the module in which the symbols have changed.</span></span>  
  
 `pSymbolStream`  
 <span data-ttu-id="05f25-108">[in]Win32 COM へのポインター`IStream`変更されたシンボルを含むオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="05f25-108">[in] A pointer to a Win32 COM `IStream` object that contains the modified symbols.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="05f25-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="05f25-109">Remarks</span></span>  
 <span data-ttu-id="05f25-110">このメソッドは、呼び出すことによって、モジュールのシンボルのデバッガーのビューを更新する機会を提供します。 [isymunmanagedreader::updatesymbolstore](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-updatesymbolstore-method.md)または[isymunmanagedreader::replacesymbolstore](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-replacesymbolstore-method.md)します。</span><span class="sxs-lookup"><span data-stu-id="05f25-110">This method provides an opportunity to update the debugger's view of a module's symbols by calling [ISymUnmanagedReader::UpdateSymbolStore](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-updatesymbolstore-method.md) or [ISymUnmanagedReader::ReplaceSymbolStore](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-replacesymbolstore-method.md).</span></span>  
  
 <span data-ttu-id="05f25-111">このコールバックでは、同じモジュールの複数回は発生します。</span><span class="sxs-lookup"><span data-stu-id="05f25-111">This callback can occur multiple times for the same module.</span></span>  
  
 <span data-ttu-id="05f25-112">デバッガーは、ソース レベルのブレークポイントがバインドされていないをバインドしようとする必要があります。</span><span class="sxs-lookup"><span data-stu-id="05f25-112">A debugger should try to bind unbound source-level breakpoints.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05f25-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="05f25-113">Requirements</span></span>  
 <span data-ttu-id="05f25-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="05f25-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="05f25-115">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="05f25-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="05f25-116">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="05f25-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="05f25-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="05f25-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05f25-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="05f25-118">See also</span></span>
- [<span data-ttu-id="05f25-119">ICorDebugManagedCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="05f25-119">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
