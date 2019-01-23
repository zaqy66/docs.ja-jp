---
title: ISOSDacInterface インターフェイス
ms.date: 01/16/2019
api.name:
- ISOSDacInterface Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface Interface
helpviewer.keywords:
- ISOSDacInterface Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 5e037cf6fb88fff4886733ff4152dca0a827e0a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491029"
---
# <a name="isosdacinterface-interface"></a><span data-ttu-id="7e958-102">ISOSDacInterface インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7e958-102">ISOSDacInterface Interface</span></span>

<span data-ttu-id="7e958-103">データにアクセスするヘルパー メソッドを提供します。`SOS`します。</span><span class="sxs-lookup"><span data-stu-id="7e958-103">Provides helper methods to access data from `SOS`.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="7e958-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="7e958-104">Methods</span></span>

| <span data-ttu-id="7e958-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="7e958-105">Method</span></span>                                                                                                               | <span data-ttu-id="7e958-106">説明</span><span class="sxs-lookup"><span data-stu-id="7e958-106">Description</span></span>                                                                                                                   |
| -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="7e958-107">GetMethodDescData</span><span class="sxs-lookup"><span data-stu-id="7e958-107">GetMethodDescData</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-getmethoddescdata-method.md) | <span data-ttu-id="7e958-108">データを取得、指定された[MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md)します。</span><span class="sxs-lookup"><span data-stu-id="7e958-108">Gets the data for the given [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span></span> |

## <a name="remarks"></a><span data-ttu-id="7e958-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="7e958-109">Remarks</span></span>

<span data-ttu-id="7e958-110">このインターフェイスは、ランタイム内に収めるを任意のヘッダーまたはライブラリ ファイルでは公開されません。</span><span class="sxs-lookup"><span data-stu-id="7e958-110">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="7e958-111">ただし、これは COM インターフェイスから派生した`IUnknown`GUID を持つ`436f00f2-b42a-4b9f-870c-e73db66ae930`を通常の COM メカニズムを通じて取得できます。</span><span class="sxs-lookup"><span data-stu-id="7e958-111">However, it's a COM interface that derives from `IUnknown` with GUID `436f00f2-b42a-4b9f-870c-e73db66ae930` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e958-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="7e958-112">Requirements</span></span>

<span data-ttu-id="7e958-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e958-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="7e958-114">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="7e958-114">**Header:** None</span></span>  
<span data-ttu-id="7e958-115">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="7e958-115">**Library:** None</span></span>  
<span data-ttu-id="7e958-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7e958-116">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="7e958-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e958-117">See also</span></span>

- [<span data-ttu-id="7e958-118">デバッグ</span><span class="sxs-lookup"><span data-stu-id="7e958-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="7e958-119">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7e958-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
