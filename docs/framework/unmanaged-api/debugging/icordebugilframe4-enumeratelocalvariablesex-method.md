---
title: ICorDebugILFrame4::EnumerateLocalVariablesEx メソッド
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugILFrame4.EnumerateLocalVariablesEx
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 6f60aae6-70ec-4c4c-963a-138df98c4668
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f770182ef8489d503ed092bb4c6cf43ae5b9ce10
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663350"
---
# <a name="icordebugilframe4enumeratelocalvariablesex-method"></a><span data-ttu-id="09420-102">ICorDebugILFrame4::EnumerateLocalVariablesEx メソッド</span><span class="sxs-lookup"><span data-stu-id="09420-102">ICorDebugILFrame4::EnumerateLocalVariablesEx Method</span></span>
<span data-ttu-id="09420-103">[.NET Framework 4.5.2 以降のバージョンでのみでサポート]</span><span class="sxs-lookup"><span data-stu-id="09420-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="09420-104">フレームのローカル変数の列挙子を取得し、プロファイラー ReJIT インストルメンテーションに追加される変数も含みます。</span><span class="sxs-lookup"><span data-stu-id="09420-104">Gets an enumerator for the local variable in the frame, and optionally includes variables added in profiler ReJIT instrumentation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09420-105">構文</span><span class="sxs-lookup"><span data-stu-id="09420-105">Syntax</span></span>  
  
```cpp
HRESULT EnumerateLocalVariablesEx(  
   [in] ILCodeKind flags,   
   [out] ICorDebugValueEnum **ppValueEnum  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="09420-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="09420-106">Parameters</span></span>  
 `flags`  
 <span data-ttu-id="09420-107">[in][ILCodeKind](../../../../docs/framework/unmanaged-api/debugging/ilcodekind-enumeration.md)プロファイラー ReJIT インストルメンテーションに追加された変数がフレームに含まれるかどうかを指定する列挙型メンバー。</span><span class="sxs-lookup"><span data-stu-id="09420-107">[in] An [ILCodeKind](../../../../docs/framework/unmanaged-api/debugging/ilcodekind-enumeration.md) enumeration member that specifies whether variables added in profiler ReJIT instrumentation are included in the frame.</span></span>  
  
 `ppValueEnum`  
 <span data-ttu-id="09420-108">[out]このフレームのローカル変数の列挙子である"ICorDebugValueEnum"オブジェクトのアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="09420-108">[out] A pointer to the address of an "ICorDebugValueEnum" object that is the enumerator for the local variables in this frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="09420-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="09420-109">Remarks</span></span>  
 <span data-ttu-id="09420-110">このメソッドは、 [EnumerateLocalVariables](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-enumeratelocalvariables-method.md)メソッド、点を除いて、it は、プロファイラー ReJIT インストルメンテーションに追加される変数をオプションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="09420-110">This method is similar to the [EnumerateLocalVariables](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-enumeratelocalvariables-method.md) method, except that it optionally accesses variables added in profiler ReJIT instrumentation.</span></span> <span data-ttu-id="09420-111">設定`flags`に`ILCODE_ORIGINAL_IL`呼び出しと同じですが[icordebugilframe::enumeratelocalvariables](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-enumeratelocalvariables-method.md)します。</span><span class="sxs-lookup"><span data-stu-id="09420-111">Setting `flags` to `ILCODE_ORIGINAL_IL` is equivalent to calling [ICorDebugILFrame::EnumerateLocalVariables](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-enumeratelocalvariables-method.md).</span></span> <span data-ttu-id="09420-112">`flags` を `ILCODE_REJIT_IL` に設定することにより、デバッガは プロファイラー ReJIT インストルメンテーションに追加されるローカル変数にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="09420-112">Setting `flags` to `ILCODE_REJIT_IL` allows the debugger to access the local variables added in profiler ReJIT instrumentation.</span></span> <span data-ttu-id="09420-113">中間言語 (IL) がインストルメント化されていない場合は、列挙子は空になり、メソッドは `S_OK` を返します。</span><span class="sxs-lookup"><span data-stu-id="09420-113">If the intermediate language (IL) is not instrumented, the enumeration is empty and the method returns `S_OK`.</span></span>  
  
 <span data-ttu-id="09420-114">実行中のメソッドにあるすべてのローカル変数が列挙子に含まれない場合がありますが、それは一部のローカル変数が非アクティブである可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="09420-114">The enumerator may not include all of the local variables in the running method, since some of them may not be active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="09420-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="09420-115">Requirements</span></span>  
 <span data-ttu-id="09420-116">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="09420-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="09420-117">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="09420-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="09420-118">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="09420-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="09420-119">**.NET Framework のバージョン:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="09420-119">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09420-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="09420-120">See also</span></span>
- [<span data-ttu-id="09420-121">ICorDebugILFrame4 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="09420-121">ICorDebugILFrame4 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-interface.md)
- [<span data-ttu-id="09420-122">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="09420-122">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="09420-123">ReJIT:ハウツー ガイド</span><span class="sxs-lookup"><span data-stu-id="09420-123">ReJIT: A How-To Guide</span></span>](https://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)
