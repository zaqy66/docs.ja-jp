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
ms.openlocfilehash: e306834166051ae48fd283d51f18d9458091578f
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416662"
---
# <a name="ixclrdatamodule-interface"></a><span data-ttu-id="3e255-102">IXCLRDataModule インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3e255-102">IXCLRDataModule Interface</span></span>

<span data-ttu-id="3e255-103">読み込まれたモジュールに関する情報を照会するためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="3e255-103">Provides methods for querying information about a loaded module.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="3e255-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="3e255-104">Methods</span></span>

| <span data-ttu-id="3e255-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="3e255-105">Method</span></span>                                                                                                                                | <span data-ttu-id="3e255-106">説明</span><span class="sxs-lookup"><span data-stu-id="3e255-106">Description</span></span>                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="3e255-107">GetMethodDefinitionByToken</span><span class="sxs-lookup"><span data-stu-id="3e255-107">GetMethodDefinitionByToken</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getmethoddefinitionbytoken-method.md) | <span data-ttu-id="3e255-108">指定したメタデータ トークンに対応するメソッドの定義を取得します。</span><span class="sxs-lookup"><span data-stu-id="3e255-108">Gets the method definition corresponding to a given metadata token.</span></span> |
| [<span data-ttu-id="3e255-109">要求</span><span class="sxs-lookup"><span data-stu-id="3e255-109">Request</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-request-method.md)                                       | <span data-ttu-id="3e255-110">要求をモジュールのデータで指定されたバッファーを設定します。</span><span class="sxs-lookup"><span data-stu-id="3e255-110">Requests to populate the buffer given with the module's data.</span></span>       |
| [<span data-ttu-id="3e255-111">GetVersionId</span><span class="sxs-lookup"><span data-stu-id="3e255-111">GetVersionId</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getversionid-method.md)                             | <span data-ttu-id="3e255-112">モジュールのバージョンの ID を取得します</span><span class="sxs-lookup"><span data-stu-id="3e255-112">Gets the module's version ID.</span></span>                                       |

## <a name="remarks"></a><span data-ttu-id="3e255-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="3e255-113">Remarks</span></span>

<span data-ttu-id="3e255-114">このインターフェイスは、ランタイム内に収めるを任意のヘッダーまたはライブラリ ファイルでは公開されません。</span><span class="sxs-lookup"><span data-stu-id="3e255-114">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="3e255-115">ただし、これは COM インターフェイスから派生した`IUnknown`GUID を持つ`88E32849-0A0A-4cb0-9022-7CD2E9E139E2`を通常の COM メカニズムを通じて取得できます。</span><span class="sxs-lookup"><span data-stu-id="3e255-115">However, it's a COM interface that derives from `IUnknown` with GUID `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e255-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="3e255-116">Requirements</span></span>

<span data-ttu-id="3e255-117">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e255-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="3e255-118">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="3e255-118">**Header:** None</span></span>  
<span data-ttu-id="3e255-119">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="3e255-119">**Library:** None</span></span>  
<span data-ttu-id="3e255-120">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="3e255-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="3e255-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e255-121">See Also</span></span>

- [<span data-ttu-id="3e255-122">デバッグ</span><span class="sxs-lookup"><span data-stu-id="3e255-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="3e255-123">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3e255-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
