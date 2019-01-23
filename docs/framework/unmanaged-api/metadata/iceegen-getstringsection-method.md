---
title: ICeeGen::GetStringSection メソッド
ms.date: 03/30/2017
api_name:
- ICeeGen.GetStringSection
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetStringSection
helpviewer_keywords:
- ICeeGen::GetStringSection method [.NET Framework metadata]
- GetStringSection method [.NET Framework metadata]
ms.assetid: a2267d39-69d1-4de1-bf37-f752cafacc71
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c4ccbff4a4967e7525ee4e51650a4f53e5458666
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54605519"
---
# <a name="iceegengetstringsection-method"></a><span data-ttu-id="ec4c3-102">ICeeGen::GetStringSection メソッド</span><span class="sxs-lookup"><span data-stu-id="ec4c3-102">ICeeGen::GetStringSection Method</span></span>
<span data-ttu-id="ec4c3-103">指定したハンドルによって参照されるコードのセクションの文字列表現を取得します。</span><span class="sxs-lookup"><span data-stu-id="ec4c3-103">Gets a string representation of the code section referenced by the specified handle.</span></span>  
  
 <span data-ttu-id="ec4c3-104">このメソッドは廃止され、使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec4c3-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec4c3-105">構文</span><span class="sxs-lookup"><span data-stu-id="ec4c3-105">Syntax</span></span>  
  
```  
HRESULT GetStringSection (  
    [in, out] HCEESECTION     *section  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ec4c3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ec4c3-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="ec4c3-107">[入力、出力]コード セクションへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="ec4c3-107">[in, out] The handle to the code section.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ec4c3-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="ec4c3-108">Requirements</span></span>  
 <span data-ttu-id="ec4c3-109">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec4c3-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec4c3-110">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ec4c3-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ec4c3-111">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="ec4c3-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ec4c3-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ec4c3-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec4c3-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec4c3-113">See also</span></span>
- [<span data-ttu-id="ec4c3-114">ICeeGen インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ec4c3-114">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
