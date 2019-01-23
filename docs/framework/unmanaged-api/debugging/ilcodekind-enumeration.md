---
title: ILCodeKind 列挙型
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ILCodeKind
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: b91765e4-82db-46f9-a6dc-6b80610276af
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0fa7d06f39dc05da6fd1657404f882c14c44ea9a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505024"
---
# <a name="ilcodekind-enumeration"></a><span data-ttu-id="2f555-102">ILCodeKind 列挙型</span><span class="sxs-lookup"><span data-stu-id="2f555-102">ILCodeKind Enumeration</span></span>
<span data-ttu-id="2f555-103">[.NET Framework 4.5.2 以降のバージョンでのみでサポート]</span><span class="sxs-lookup"><span data-stu-id="2f555-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="2f555-104">デバッガーがローカル変数またはプロファイラー ReJIT インストルメンテーションに追加されたコードにアクセスできるかどうかを指定する値を提供します。</span><span class="sxs-lookup"><span data-stu-id="2f555-104">Provides values that specify whether the debugger is able to access local variables or code added in profiler ReJIT instrumentation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f555-105">構文</span><span class="sxs-lookup"><span data-stu-id="2f555-105">Syntax</span></span>  
  
```cpp
typedef enum ILCodeKind {  
   ILCODE_ORIGINAL_IL = 0x1,  
   ILCODE_REJIT_IL = 0x2,  
} ILCodeKind;  
```  
  
## <a name="members"></a><span data-ttu-id="2f555-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="2f555-106">Members</span></span>  
  
|<span data-ttu-id="2f555-107">メンバー名</span><span class="sxs-lookup"><span data-stu-id="2f555-107">Member name</span></span>|<span data-ttu-id="2f555-108">説明</span><span class="sxs-lookup"><span data-stu-id="2f555-108">Description</span></span>|  
|-----------------|-----------------|  
|`ILCODE_ORIGINAL_IL`|<span data-ttu-id="2f555-109">デバッガーは、ReJIT インストルメンテーションからの情報に対してアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="2f555-109">The debugger does not have access to information from ReJIT instrumentation.</span></span>|  
|`ILCODE_REJIT_IL`|<span data-ttu-id="2f555-110">デバッガーは、ReJIT インストルメンテーションからの情報に対してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2f555-110">The debugger has access to information from ReJIT instrumentation.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2f555-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="2f555-111">Remarks</span></span>  
 <span data-ttu-id="2f555-112">メンバー、`ILCodeKind`に列挙体を渡すことができます、 [EnumerateLocalVariablesEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-enumeratelocalvariablesex-method.md)と[GetLocalVariableEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-getlocalvariableex-method.md)デバッガーがプロファイラーに追加される変数にアクセスできるかどうかを判断する方法ReJIT インストルメンテーションにされ、 [GetCodeEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-getcodeex-method.md)デバッガーがアクセスできるかどうかを判断するメソッドには、IL がインストルメント化されました。</span><span class="sxs-lookup"><span data-stu-id="2f555-112">A member of the `ILCodeKind` enumeration can be passed to the [EnumerateLocalVariablesEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-enumeratelocalvariablesex-method.md) and [GetLocalVariableEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-getlocalvariableex-method.md) methods to determine whether the debugger can access variables added in profiler ReJIT instrumentation, and to the [GetCodeEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-getcodeex-method.md) method to determine whether the debugger can access instrumented IL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2f555-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="2f555-113">Requirements</span></span>  
 <span data-ttu-id="2f555-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f555-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2f555-115">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2f555-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2f555-116">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2f555-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2f555-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2f555-117">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f555-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f555-118">See also</span></span>
- [<span data-ttu-id="2f555-119">列挙型のデバッグ</span><span class="sxs-lookup"><span data-stu-id="2f555-119">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
- [<span data-ttu-id="2f555-120">ICorDebugILFrame4 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="2f555-120">ICorDebugILFrame4 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-interface.md)
- [<span data-ttu-id="2f555-121">ReJIT:ハウツー ガイド</span><span class="sxs-lookup"><span data-stu-id="2f555-121">ReJIT: A How-To Guide</span></span>](https://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)
