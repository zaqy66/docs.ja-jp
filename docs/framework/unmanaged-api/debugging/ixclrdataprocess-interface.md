---
title: IXCLRDataProcess インターフェイス
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess Interface
helpviewer.keywords:
- IXCLRDataProcess Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: ff74a7acb5cc84c177f083c19402cd78977aeab5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54680375"
---
# <a name="ixclrdataprocess-interface"></a><span data-ttu-id="5042a-102">IXCLRDataProcess インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5042a-102">IXCLRDataProcess Interface</span></span>

<span data-ttu-id="5042a-103">プロセスの情報を照会するためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="5042a-103">Provides methods for querying information about a process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="5042a-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="5042a-104">Methods</span></span>

| <span data-ttu-id="5042a-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="5042a-105">Method</span></span>                                                                                                                                               | <span data-ttu-id="5042a-106">説明</span><span class="sxs-lookup"><span data-stu-id="5042a-106">Description</span></span>                                                                                     |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="5042a-107">GetAppDomainByUniqueId</span><span class="sxs-lookup"><span data-stu-id="5042a-107">GetAppDomainByUniqueId</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-getappdomainbyuniqueid-method.md)                       | <span data-ttu-id="5042a-108">取得、`AppDomain`一意の id でのプロセスでします。</span><span class="sxs-lookup"><span data-stu-id="5042a-108">Gets an `AppDomain` in a process by its unique id.</span></span>                                              |
| [<span data-ttu-id="5042a-109">StartEnumModules</span><span class="sxs-lookup"><span data-stu-id="5042a-109">StartEnumModules</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-startenummodules-method.md)                                   | <span data-ttu-id="5042a-110">プロセスのモジュールを列挙するハンドルを提供します。</span><span class="sxs-lookup"><span data-stu-id="5042a-110">Provides a handle to enumerate the modules of a process.</span></span>                                        |
| [<span data-ttu-id="5042a-111">EnumModule</span><span class="sxs-lookup"><span data-stu-id="5042a-111">EnumModule</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-enummodule-method.md)                                               | <span data-ttu-id="5042a-112">このプロセスのモジュールを列挙します。</span><span class="sxs-lookup"><span data-stu-id="5042a-112">Enumerates the modules of this process.</span></span>                                                         |
| [<span data-ttu-id="5042a-113">EndEnumModules</span><span class="sxs-lookup"><span data-stu-id="5042a-113">EndEnumModules</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-endenummodules-method.md)                                       | <span data-ttu-id="5042a-114">モジュールの列挙中に使用される内部の反復子によって使用されるリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="5042a-114">Releases the resources used by internal iterators used during module enumeration.</span></span>               |
| [<span data-ttu-id="5042a-115">StartEnumMethodInstancesByAddress</span><span class="sxs-lookup"><span data-stu-id="5042a-115">StartEnumMethodInstancesByAddress</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-startenummethodinstancesbyaddress-method.md) | <span data-ttu-id="5042a-116">メソッドのインスタンスを列挙ハンドルを提供します`AppDomain`特定のアドレスで開始します。</span><span class="sxs-lookup"><span data-stu-id="5042a-116">Provides a handle to enumerate the method instances of `AppDomain` starting at a given address.</span></span> |
| [<span data-ttu-id="5042a-117">EnumMethodInstanceByAddress</span><span class="sxs-lookup"><span data-stu-id="5042a-117">EnumMethodInstanceByAddress</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-enummethodinstancebyaddress-method.md)             | <span data-ttu-id="5042a-118">このプロセスがアドレス オフセットから始まるのメソッドのインスタンスを列挙します。</span><span class="sxs-lookup"><span data-stu-id="5042a-118">Enumerates the method instances of this process starting at an address offset.</span></span>                  |
| [<span data-ttu-id="5042a-119">EndEnumMethodInstancesByAddress</span><span class="sxs-lookup"><span data-stu-id="5042a-119">EndEnumMethodInstancesByAddress</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-endenummethodinstancesbyaddress-method.md)     | <span data-ttu-id="5042a-120">インスタンスの列挙中に使用される内部の反復子によって使用されるリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="5042a-120">Releases the resources used by internal iterators used during instance enumeration.</span></span>             |

## <a name="remarks"></a><span data-ttu-id="5042a-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="5042a-121">Remarks</span></span>

<span data-ttu-id="5042a-122">このインターフェイスは、ランタイム内に収めるを任意のヘッダーまたはライブラリ ファイルでは公開されません。</span><span class="sxs-lookup"><span data-stu-id="5042a-122">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="5042a-123">ただし、これは COM インターフェイスから派生した`IUnknown`GUID を持つ`5c552ab6-fc09-4cb3-8e36-22fa03c798b7`を通常の COM メカニズムを通じて取得できます。</span><span class="sxs-lookup"><span data-stu-id="5042a-123">However, it's a COM interface that derives from `IUnknown` with GUID `5c552ab6-fc09-4cb3-8e36-22fa03c798b7` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="5042a-124">必要条件</span><span class="sxs-lookup"><span data-stu-id="5042a-124">Requirements</span></span>

<span data-ttu-id="5042a-125">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5042a-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>   
<span data-ttu-id="5042a-126">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="5042a-126">**Header:** None</span></span>  
<span data-ttu-id="5042a-127">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="5042a-127">**Library:** None</span></span>  
<span data-ttu-id="5042a-128">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="5042a-128">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="5042a-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="5042a-129">See also</span></span>

- [<span data-ttu-id="5042a-130">デバッグ</span><span class="sxs-lookup"><span data-stu-id="5042a-130">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="5042a-131">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5042a-131">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
