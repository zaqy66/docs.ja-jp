---
title: IValidator インターフェイス
ms.date: 03/30/2017
api_name:
- IValidator
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IValidator
helpviewer_keywords:
- IValidator interface [.NET Framework hosting]
ms.assetid: b297e3b0-20f9-478f-b707-5e2eecb2b5b2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9f307ad5689602b030c609a51f6834bdbb0ec4f8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54717716"
---
# <a name="ivalidator-interface"></a><span data-ttu-id="77f29-102">IValidator インターフェイス</span><span class="sxs-lookup"><span data-stu-id="77f29-102">IValidator Interface</span></span>
<span data-ttu-id="77f29-103">ポータブル実行可能 (PE) イメージを検証し、検証エラーを報告するためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="77f29-103">Provides methods for validating portable executable (PE) images and reporting validation errors.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="77f29-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="77f29-104">Methods</span></span>  
  
|<span data-ttu-id="77f29-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="77f29-105">Method</span></span>|<span data-ttu-id="77f29-106">説明</span><span class="sxs-lookup"><span data-stu-id="77f29-106">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="77f29-107">検証</span><span class="sxs-lookup"><span data-stu-id="77f29-107">Validate</span></span>|<span data-ttu-id="77f29-108">指定された PE または Microsoft intermediate language (MSIL) ファイルを検証します。</span><span class="sxs-lookup"><span data-stu-id="77f29-108">Validates the specified PE or Microsoft intermediate language (MSIL) file.</span></span>|  
|<span data-ttu-id="77f29-109">FormatEventInfo</span><span class="sxs-lookup"><span data-stu-id="77f29-109">FormatEventInfo</span></span>|<span data-ttu-id="77f29-110">指定した検証エラーに対応するエラー メッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="77f29-110">Gets the error message corresponding to the specified validation error.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="77f29-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="77f29-111">Requirements</span></span>  
 <span data-ttu-id="77f29-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="77f29-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77f29-113">**ヘッダー:** IValidator.idl, IValidator.h</span><span class="sxs-lookup"><span data-stu-id="77f29-113">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="77f29-114">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="77f29-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="77f29-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="77f29-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77f29-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="77f29-116">See also</span></span>
- [<span data-ttu-id="77f29-117">ホスト インターフェイス</span><span class="sxs-lookup"><span data-stu-id="77f29-117">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="77f29-118">CorRuntimeHost コクラス</span><span class="sxs-lookup"><span data-stu-id="77f29-118">CorRuntimeHost Coclass</span></span>](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)
