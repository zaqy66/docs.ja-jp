---
title: ISymUnmanagedReader::GetUserEntryPoint メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetUserEntryPoint
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetUserEntryPoint
helpviewer_keywords:
- GetUserEntryPoint method [.NET Framework debugging]
- ISymUnmanagedReader::GetUserEntryPoint method [.NET Framework debugging]
ms.assetid: 3fd3a34c-d176-46e9-9996-fb1646cff9b0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a8519577bb2b9d3ff8fa2138ba007d04d9fde159
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730153"
---
# <a name="isymunmanagedreadergetuserentrypoint-method"></a><span data-ttu-id="7bf56-102">ISymUnmanagedReader::GetUserEntryPoint メソッド</span><span class="sxs-lookup"><span data-stu-id="7bf56-102">ISymUnmanagedReader::GetUserEntryPoint Method</span></span>
<span data-ttu-id="7bf56-103">存在する場合は、モジュールのユーザー エントリ ポイントとして指定されたメソッドを返します。</span><span class="sxs-lookup"><span data-stu-id="7bf56-103">Returns the method that was specified as the user entry point for the module, if any.</span></span> <span data-ttu-id="7bf56-104">たとえば、このメソッドでは、メイン メソッドの前に、コンパイラによって生成されたスタブではなく、ユーザーのメイン メソッドに可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7bf56-104">For example, this method could be the user's main method rather than compiler-generated stubs before the main method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7bf56-105">構文</span><span class="sxs-lookup"><span data-stu-id="7bf56-105">Syntax</span></span>  
  
```  
HRESULT GetUserEntryPoint (  
    [out, retval]  mdMethodDef  *pToken);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7bf56-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7bf56-106">Parameters</span></span>  
 `pToken`  
 <span data-ttu-id="7bf56-107">[out]エントリ ポイントを受け取る変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7bf56-107">[out] A pointer to a variable that receives the entry point.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7bf56-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="7bf56-108">Return Value</span></span>  
 <span data-ttu-id="7bf56-109">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="7bf56-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7bf56-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="7bf56-110">Requirements</span></span>  
 <span data-ttu-id="7bf56-111">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="7bf56-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bf56-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="7bf56-112">See also</span></span>
- [<span data-ttu-id="7bf56-113">ISymUnmanagedReader インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7bf56-113">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
