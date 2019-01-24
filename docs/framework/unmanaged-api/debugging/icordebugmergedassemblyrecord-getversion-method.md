---
title: ICorDebugMergedAssemblyRecord::GetVersion メソッド
ms.date: 03/30/2017
ms.assetid: c6858b06-ae26-4312-b325-ea6025016675
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4895610ba3a8e8e8eb1a1c360ecb2b707f9cee4d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54622092"
---
# <a name="icordebugmergedassemblyrecordgetversion-method"></a><span data-ttu-id="090de-102">ICorDebugMergedAssemblyRecord::GetVersion メソッド</span><span class="sxs-lookup"><span data-stu-id="090de-102">ICorDebugMergedAssemblyRecord::GetVersion Method</span></span>
<span data-ttu-id="090de-103">アセンブリのバージョン情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="090de-103">Gets the assembly's version information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="090de-104">構文</span><span class="sxs-lookup"><span data-stu-id="090de-104">Syntax</span></span>  
  
```  
HRESULT GetVersion(  
   [out] USHORT *pMajor,   
   [out] USHORT *pMinor,   
   [out] USHORT *pBuild,   
   [out] USHORT *pRevision  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="090de-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="090de-105">Parameters</span></span>  
 `pMajor`  
 <span data-ttu-id="090de-106">[out] メジャー バージョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="090de-106">[out] A pointer to the major version number.</span></span>  
  
 `pMinor`  
 <span data-ttu-id="090de-107">[out] マイナー バージョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="090de-107">[out] A pointer to the minor version number.</span></span>  
  
 `pBuild`  
 <span data-ttu-id="090de-108">[out] ビルド番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="090de-108">[out] A pointer to the build number.</span></span>  
  
 `pRevision`  
 <span data-ttu-id="090de-109">[out] リビジョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="090de-109">[out] A pointer to the revision number.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="090de-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="090de-110">Remarks</span></span>  
 <span data-ttu-id="090de-111">アセンブリのバージョン番号については、<xref:System.Version> クラスのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="090de-111">For information on assembly version numbers, see the <xref:System.Version> class topic.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="090de-112">このメソッドは .NET ネイティブでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="090de-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="090de-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="090de-113">Requirements</span></span>  
 <span data-ttu-id="090de-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="090de-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="090de-115">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="090de-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="090de-116">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="090de-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="090de-117">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="090de-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="090de-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="090de-118">See also</span></span>
- [<span data-ttu-id="090de-119">ICorDebugMergedAssemblyRecord インターフェイス</span><span class="sxs-lookup"><span data-stu-id="090de-119">ICorDebugMergedAssemblyRecord Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="090de-120">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="090de-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
