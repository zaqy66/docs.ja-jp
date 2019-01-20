---
title: IXCLRDataMethodDefinition インターフェイス
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition Interface
helpviewer.keywords:
- IXCLRDataMethodDefinition Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 4265db62b11453d9fc087928adb0cc0c05c052ca
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416609"
---
# <a name="ixclrdatamethoddefinition-interface"></a><span data-ttu-id="c6158-102">IXCLRDataMethodDefinition インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c6158-102">IXCLRDataMethodDefinition Interface</span></span>

<span data-ttu-id="c6158-103">メソッドの定義に関する情報を照会するためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="c6158-103">Provides methods for querying information about a method definition.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="c6158-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="c6158-104">Methods</span></span>

<span data-ttu-id="c6158-105">次の方法では、インターフェイスで使用可能なメソッドの一部を示します。</span><span class="sxs-lookup"><span data-stu-id="c6158-105">The following methods are some of the methods available in the interface.</span></span>

| <span data-ttu-id="c6158-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="c6158-106">Method</span></span>                                                                                                                          | <span data-ttu-id="c6158-107">説明</span><span class="sxs-lookup"><span data-stu-id="c6158-107">Description</span></span>                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="c6158-108">StartEnumInstances</span><span class="sxs-lookup"><span data-stu-id="c6158-108">StartEnumInstances</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-startenuminstances-method.md) | <span data-ttu-id="c6158-109">メソッド インスタンスの列挙体のハンドルを提供する、指定された`IXCLRDataAppDomain`します。</span><span class="sxs-lookup"><span data-stu-id="c6158-109">Provides a handle for the enumeration of method instances for a given `IXCLRDataAppDomain`.</span></span> |
| [<span data-ttu-id="c6158-110">EnumInstance</span><span class="sxs-lookup"><span data-stu-id="c6158-110">EnumInstance</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-enuminstance-method.md)             | <span data-ttu-id="c6158-111">このメソッドの定義のインスタンスを列挙します。</span><span class="sxs-lookup"><span data-stu-id="c6158-111">Enumerates the instances of this method definition.</span></span>                                         |
| [<span data-ttu-id="c6158-112">EndEnumInstances</span><span class="sxs-lookup"><span data-stu-id="c6158-112">EndEnumInstances</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-endenuminstances-method.md)     | <span data-ttu-id="c6158-113">インスタンスの列挙中に使用される内部の反復子によって使用されるリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="c6158-113">Releases the resources used by internal iterators used during instance enumeration.</span></span>         |

## <a name="remarks"></a><span data-ttu-id="c6158-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="c6158-114">Remarks</span></span>

<span data-ttu-id="c6158-115">このインターフェイスは、ランタイム内に収めるを任意のヘッダーまたはライブラリ ファイルでは公開されません。</span><span class="sxs-lookup"><span data-stu-id="c6158-115">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="c6158-116">ただし、これは COM インターフェイスから派生した`IUnknown`GUID を持つ`AAF60008-FB2C-420b-8FB1-42D244A54A97`を通常の COM メカニズムを通じて取得できます。</span><span class="sxs-lookup"><span data-stu-id="c6158-116">However, it's a COM interface that derives from `IUnknown` with GUID `AAF60008-FB2C-420b-8FB1-42D244A54A97` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6158-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="c6158-117">Requirements</span></span>

<span data-ttu-id="c6158-118">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6158-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="c6158-119">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="c6158-119">**Header:** None</span></span>  
<span data-ttu-id="c6158-120">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="c6158-120">**Library:** None</span></span>  
<span data-ttu-id="c6158-121">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="c6158-121">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="c6158-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6158-122">See Also</span></span>

- [<span data-ttu-id="c6158-123">デバッグ</span><span class="sxs-lookup"><span data-stu-id="c6158-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="c6158-124">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c6158-124">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)