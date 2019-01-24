---
title: IXCLRDataModule インターフェイス
ms.date: 01/16/2019
api.name:
- IXCLRDataModule Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule Interface
helpviewer.keywords:
- IXCLRDataModule Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: c8d6e36687fd43bbc59304eee64dd42eb78101e3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676524"
---
# <a name="ixclrdatamodule-interface"></a><span data-ttu-id="6f413-102">IXCLRDataModule インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6f413-102">IXCLRDataModule Interface</span></span>

<span data-ttu-id="6f413-103">読み込まれたモジュールに関する情報を照会するためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="6f413-103">Provides methods for querying information about a loaded module.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="6f413-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="6f413-104">Methods</span></span>

| <span data-ttu-id="6f413-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="6f413-105">Method</span></span>                                                                                                                                | <span data-ttu-id="6f413-106">説明</span><span class="sxs-lookup"><span data-stu-id="6f413-106">Description</span></span>                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="6f413-107">GetMethodDefinitionByToken</span><span class="sxs-lookup"><span data-stu-id="6f413-107">GetMethodDefinitionByToken</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getmethoddefinitionbytoken-method.md) | <span data-ttu-id="6f413-108">指定したメタデータ トークンに対応するメソッドの定義を取得します。</span><span class="sxs-lookup"><span data-stu-id="6f413-108">Gets the method definition corresponding to a given metadata token.</span></span> |
| [<span data-ttu-id="6f413-109">要求</span><span class="sxs-lookup"><span data-stu-id="6f413-109">Request</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-request-method.md)                                       | <span data-ttu-id="6f413-110">要求をモジュールのデータで指定されたバッファーを設定します。</span><span class="sxs-lookup"><span data-stu-id="6f413-110">Requests to populate the buffer given with the module's data.</span></span>       |
| [<span data-ttu-id="6f413-111">GetVersionId</span><span class="sxs-lookup"><span data-stu-id="6f413-111">GetVersionId</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getversionid-method.md)                             | <span data-ttu-id="6f413-112">モジュールのバージョンの ID を取得します</span><span class="sxs-lookup"><span data-stu-id="6f413-112">Gets the module's version ID.</span></span>                                       |

## <a name="remarks"></a><span data-ttu-id="6f413-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="6f413-113">Remarks</span></span>

<span data-ttu-id="6f413-114">このインターフェイスは、ランタイム内に収めるを任意のヘッダーまたはライブラリ ファイルでは公開されません。</span><span class="sxs-lookup"><span data-stu-id="6f413-114">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="6f413-115">ただし、これは COM インターフェイスから派生した`IUnknown`GUID を持つ`88E32849-0A0A-4cb0-9022-7CD2E9E139E2`を通常の COM メカニズムを通じて取得できます。</span><span class="sxs-lookup"><span data-stu-id="6f413-115">However, it's a COM interface that derives from `IUnknown` with GUID `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f413-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="6f413-116">Requirements</span></span>

<span data-ttu-id="6f413-117">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f413-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="6f413-118">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="6f413-118">**Header:** None</span></span>  
<span data-ttu-id="6f413-119">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="6f413-119">**Library:** None</span></span>  
<span data-ttu-id="6f413-120">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="6f413-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="6f413-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f413-121">See also</span></span>

- [<span data-ttu-id="6f413-122">デバッグ</span><span class="sxs-lookup"><span data-stu-id="6f413-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="6f413-123">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6f413-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
