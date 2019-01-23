---
title: GetHistoryFileDirectory 関数
ms.date: 03/30/2017
api_name:
- GetHistoryFileDirectory
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- GetHistoryFileDirectory
helpviewer_keywords:
- GetHistoryFileDirectory function [.NET Framework fusion]
ms.assetid: 93232222-926e-42ac-b85d-8a6d33977672
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: defe69e8d205a0c66f806e4ffacb09d5a9f63309
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54552113"
---
# <a name="gethistoryfiledirectory-function"></a><span data-ttu-id="4e675-102">GetHistoryFileDirectory 関数</span><span class="sxs-lookup"><span data-stu-id="4e675-102">GetHistoryFileDirectory Function</span></span>
<span data-ttu-id="4e675-103">アプリケーション履歴ディレクトリのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e675-103">Retrieves the path of the application history directory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e675-104">構文</span><span class="sxs-lookup"><span data-stu-id="4e675-104">Syntax</span></span>  
  
```  
HRESULT GetHistoryFileDirectory (  
    [in]      LPWSTR      wzDir,  
    [in,out]  LPCWSTR  *pdwsize,  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4e675-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4e675-105">Parameters</span></span>  
 `wzDir`  
 <span data-ttu-id="4e675-106">[out]アプリケーション履歴ディレクトリへのパスを保持するバッファー。</span><span class="sxs-lookup"><span data-stu-id="4e675-106">[out] A buffer to hold the path to the application history directory.</span></span>  
  
 `pdwSize`  
 <span data-ttu-id="4e675-107">[入力、出力]バッファーの長さ。</span><span class="sxs-lookup"><span data-stu-id="4e675-107">[in, out] The length of the buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4e675-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="4e675-108">Return Value</span></span>  
 <span data-ttu-id="4e675-109">このメソッドは、次の値だけでなく、WinError.h ファイルで定義されている標準の COM エラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="4e675-109">This method returns standard COM error codes, as defined in the WinError.h file in addition to the following values.</span></span>  
  
|<span data-ttu-id="4e675-110">リターン コード</span><span class="sxs-lookup"><span data-stu-id="4e675-110">Return code</span></span>|<span data-ttu-id="4e675-111">説明</span><span class="sxs-lookup"><span data-stu-id="4e675-111">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="4e675-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e675-112">S_OK</span></span>|<span data-ttu-id="4e675-113">メソッドは正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="4e675-113">The method completed successfully.</span></span>|  
|<span data-ttu-id="4e675-114">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4e675-114">E_INVALIDARG</span></span>|<span data-ttu-id="4e675-115">`wzDir` または`pdwSize`が null の場合、または、バージョン文字列が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="4e675-115">`wzDir` or `pdwSize` is null, or the version string is incorrect.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4e675-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="4e675-116">Remarks</span></span>  
 <span data-ttu-id="4e675-117">正常に完了、`pdwSize`引数パス文字列の長さを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e675-117">On successful completion, the `pdwSize` argument is set to the length of the path string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4e675-118">必要条件</span><span class="sxs-lookup"><span data-stu-id="4e675-118">Requirements</span></span>  
 <span data-ttu-id="4e675-119">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4e675-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4e675-120">**ヘッダー:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="4e675-120">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="4e675-121">**ライブラリ:** Fusion.dll と Mscorwks.dll します。</span><span class="sxs-lookup"><span data-stu-id="4e675-121">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="4e675-122">Mscorwks.dll のではなく Fusion.dll を使用して、正しいバージョンの .NET Framework を対象にすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4e675-122">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="4e675-123">**.NET Framework のバージョン:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4e675-123">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e675-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="4e675-124">See also</span></span>
- [<span data-ttu-id="4e675-125">CreateHistoryReader 関数</span><span class="sxs-lookup"><span data-stu-id="4e675-125">CreateHistoryReader Function</span></span>](../../../../docs/framework/unmanaged-api/fusion/createhistoryreader-function.md)
- [<span data-ttu-id="4e675-126">NukeDownloadedCache 関数</span><span class="sxs-lookup"><span data-stu-id="4e675-126">NukeDownloadedCache Function</span></span>](../../../../docs/framework/unmanaged-api/fusion/nukedownloadedcache-function.md)
- [<span data-ttu-id="4e675-127">Fusion グローバル静的関数</span><span class="sxs-lookup"><span data-stu-id="4e675-127">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
