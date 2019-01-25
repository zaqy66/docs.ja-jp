---
title: ICeeGen::GetSectionCreate メソッド
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionCreate
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionCreate
helpviewer_keywords:
- ICeeGen::GetSectionCreate method [.NET Framework metadata]
- GetSectionCreate method [.NET Framework metadata]
ms.assetid: 154b2460-59ce-4874-a9f2-1b3353486ac5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 93e96e7804a3b5ecc64e9e50ce700435be83b77a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54643365"
---
# <a name="iceegengetsectioncreate-method"></a><span data-ttu-id="bf134-102">ICeeGen::GetSectionCreate メソッド</span><span class="sxs-lookup"><span data-stu-id="bf134-102">ICeeGen::GetSectionCreate Method</span></span>
<span data-ttu-id="bf134-103">生成し、指定した名前とフラグの値を使用してコードのセクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="bf134-103">Generates and gets a code section using the specified name and flag values.</span></span>  
  
 <span data-ttu-id="bf134-104">このメソッドは廃止され、使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf134-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bf134-105">構文</span><span class="sxs-lookup"><span data-stu-id="bf134-105">Syntax</span></span>  
  
```  
HRESULT GetSectionCreate (  
    [in]  const char     *name,  
    [in]  DWORD          flags,  
    [out] HCEESECTION    *section  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bf134-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bf134-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="bf134-107">[in]作成するセクションの名前を指定する文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bf134-107">[in] A pointer to a string that specifies the name of the section to be created.</span></span>  
  
 `flags`  
 <span data-ttu-id="bf134-108">[in]オプションを指定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="bf134-108">[in] Flags that specify options.</span></span>  
  
 `section`  
 <span data-ttu-id="bf134-109">[out]新しく作成されたコード セクションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bf134-109">[out] A pointer to the newly created code section.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bf134-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="bf134-110">Remarks</span></span>  
 <span data-ttu-id="bf134-111">呼び出す`GetSectionCreate`別の方法で処理されない特別なセクションの要件がある場合にのみです。</span><span class="sxs-lookup"><span data-stu-id="bf134-111">Call `GetSectionCreate` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bf134-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="bf134-112">Requirements</span></span>  
 <span data-ttu-id="bf134-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf134-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bf134-114">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="bf134-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="bf134-115">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="bf134-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="bf134-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bf134-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf134-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf134-117">See also</span></span>
- [<span data-ttu-id="bf134-118">ICeeGen インターフェイス</span><span class="sxs-lookup"><span data-stu-id="bf134-118">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
