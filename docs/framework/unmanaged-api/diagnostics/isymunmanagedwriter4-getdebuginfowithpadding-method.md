---
title: ISymUnmanagedWriter4::GetDebugInfoWithPadding メソッド
ms.date: 03/30/2017
ms.assetid: 881e20ca-8131-4bd0-ba41-c2d6391b0fe2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1d669ae15c01a560f2cefb6e361ca32411652fbc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732974"
---
# <a name="isymunmanagedwriter4getdebuginfowithpadding-method"></a><span data-ttu-id="e9ae5-102">ISymUnmanagedWriter4::GetDebugInfoWithPadding メソッド</span><span class="sxs-lookup"><span data-stu-id="e9ae5-102">ISymUnmanagedWriter4::GetDebugInfoWithPadding Method</span></span>
<span data-ttu-id="e9ae5-103">機能と同じ[GetDebugInfo メソッド](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md)パス文字列は、文字列データの固定サイズの終端の null 文字の後に続くゼロで埋められますことを除いて`MAX_PATH`します。</span><span class="sxs-lookup"><span data-stu-id="e9ae5-103">Functions the same as [GetDebugInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) except that the path string is padded with zeros following the terminating null character to make the string data a fixed size of `MAX_PATH`.</span></span> <span data-ttu-id="e9ae5-104">自体のパス文字列の長さがある場合、余白が指定されたのみより小さい`MAX_PATH`します。</span><span class="sxs-lookup"><span data-stu-id="e9ae5-104">Padding is only given if the path string length itself is less than `MAX_PATH`.</span></span>  
  
 <span data-ttu-id="e9ae5-105">これにより、その差分 PE ファイル ツールを記述しやすくします。</span><span class="sxs-lookup"><span data-stu-id="e9ae5-105">This makes it easier to write tools that difference PE files.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e9ae5-106">構文</span><span class="sxs-lookup"><span data-stu-id="e9ae5-106">Syntax</span></span>  
  
```idl  
HRESULT GetDebugInfoWithPadding(    [in, out] IMAGE_DEBUG_DIRECTORY *pIDD,    [in] DWORD cData,    [out] DWORD *pcData,    [out, size_is(cData), length_is(*pcData)] BYTE data[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e9ae5-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9ae5-107">Parameters</span></span>  
  
|<span data-ttu-id="e9ae5-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9ae5-108">Parameter</span></span>|<span data-ttu-id="e9ae5-109">説明</span><span class="sxs-lookup"><span data-stu-id="e9ae5-109">Description</span></span>|  
|---------------|-----------------|  
|`pIDD`||  
|`cData`||  
|`pcData`||  
|`data`||  
  
## <a name="return-value"></a><span data-ttu-id="e9ae5-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9ae5-110">Return Value</span></span>  
 <span data-ttu-id="e9ae5-111">`HRESULT` を返します。</span><span class="sxs-lookup"><span data-stu-id="e9ae5-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e9ae5-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="e9ae5-112">Requirements</span></span>  
 <span data-ttu-id="e9ae5-113">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e9ae5-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e9ae5-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9ae5-114">See also</span></span>
- [<span data-ttu-id="e9ae5-115">ISymUnmanagedWriter4 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e9ae5-115">ISymUnmanagedWriter4 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-interface.md)
