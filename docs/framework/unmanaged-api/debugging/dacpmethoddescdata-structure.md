---
title: DacpMethodDescData 構造体
ms.date: 02/01/2019
api.name:
- DacpMethodDescData Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpMethodDescData Structure
helpviewer.keywords:
- DacpMethodDescData Structure [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: e9037fc035693e079e2471ad37263108656b8c01
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2019
ms.locfileid: "55828638"
---
# <a name="dacpmethoddescdata-structure"></a><span data-ttu-id="a62f2-102">DacpMethodDescData 構造体</span><span class="sxs-lookup"><span data-stu-id="a62f2-102">DacpMethodDescData Structure</span></span>

<span data-ttu-id="a62f2-103">トランスポートのバッファー、メソッドのランタイム情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="a62f2-103">Defines a transport buffer for a method's runtime information.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="a62f2-104">構文</span><span class="sxs-lookup"><span data-stu-id="a62f2-104">Syntax</span></span>

```
struct DacpMethodDescData
{
    int             bHasNativeCode;
    int             bIsDynamic;
    unsigned short  wSlotNumber;
    CLRDATA_ADDRESS NativeCodeAddr;
    CLRDATA_ADDRESS data;
    CLRDATA_ADDRESS MethodDescPtr;
    CLRDATA_ADDRESS nativeCodeInfo;
    CLRDATA_ADDRESS moduleInfo;
    mdToken         MDToken;
    CLRDATA_ADDRESS payloadGC;
    CLRDATA_ADDRESS payloadGC2;
    CLRDATA_ADDRESS managedDynamicMethodObject;
    CLRDATA_ADDRESS requestedIP;
    DacpReJitData   rejitDataCurrent;
    DacpReJitData   rejitDataRequested;
    unsigned long   cJittedRejitVersions;
};
```

## <a name="members"></a><span data-ttu-id="a62f2-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="a62f2-105">Members</span></span>

| <span data-ttu-id="a62f2-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="a62f2-106">Member</span></span>                       | <span data-ttu-id="a62f2-107">説明</span><span class="sxs-lookup"><span data-stu-id="a62f2-107">Description</span></span>                                                                                     |
| ---------------------------- | ----------------------------------------------------------------------------------------------- |
| `bHasNativeCode`             | <span data-ttu-id="a62f2-108">ランタイムがメソッドの特定のインスタンスを作成して使用可能なネイティブ コードを持つかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a62f2-108">Indicates if the runtime has native code available for the given instantiation of the method.</span></span> |
| `bIsDynamic`                 | <span data-ttu-id="a62f2-109">メソッドが、簡易コード生成を動的に生成されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a62f2-109">Indicates if the method is generated dynamically through lightweight code generation.</span></span>           |
| `wSlotNumber`                | <span data-ttu-id="a62f2-110">メソッドの表に、メソッドのスロット番号。</span><span class="sxs-lookup"><span data-stu-id="a62f2-110">The method's slot number in the method table.</span></span>                                                   |
| `NativeCodeAddr`             | <span data-ttu-id="a62f2-111">メソッドの最初のネイティブ アドレス。</span><span class="sxs-lookup"><span data-stu-id="a62f2-111">The method's initial native address.</span></span>                                                            |
| `data`                       | <span data-ttu-id="a62f2-112">ランタイムによって内部的に使用するバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a62f2-112">Pointer to a buffer used internally by the runtime.</span></span>                                             |
| `MethodDescPtr`              | <span data-ttu-id="a62f2-113">ポインター、`MethodDesc`ランタイム。</span><span class="sxs-lookup"><span data-stu-id="a62f2-113">Pointer to the `MethodDesc` in the runtime.</span></span>                                                     |
| `nativeCodeInfo`             | <span data-ttu-id="a62f2-114">メソッドを追跡するために、ランタイムによって内部的に使用するバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a62f2-114">Pointer to a buffer used internally by the runtime to track methods.</span></span>                            |
| `moduleInfo`                 | <span data-ttu-id="a62f2-115">モジュールは、ランタイムによって内部的に使用するバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a62f2-115">Pointer to a buffer used internally by the runtime for module information.</span></span>                      |
| `MDToken`                    | <span data-ttu-id="a62f2-116">指定されたメソッドに関連付けられているトークンです。</span><span class="sxs-lookup"><span data-stu-id="a62f2-116">Token associated with the given method.</span></span>                                                         |
| `payloadGC`                  | <span data-ttu-id="a62f2-117">ランタイムによって内部的に使用するガベージ コレクション バッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a62f2-117">Pointer to a garbage collection buffer used internally by the runtime.</span></span>                          |
| `payloadGC2`                 | <span data-ttu-id="a62f2-118">ランタイムによって内部的に使用するガベージ コレクション バッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a62f2-118">Pointer to a garbage collection buffer used internally by the runtime.</span></span>                          |
| `managedDynamicMethodObject` | <span data-ttu-id="a62f2-119">動的メソッドの場合、ランタイムはこのバッファー内部的に追跡情報をします。</span><span class="sxs-lookup"><span data-stu-id="a62f2-119">If the method is dynamic, the runtime uses this buffer internally for information tracking.</span></span>     |
| `requestedIP`                | <span data-ttu-id="a62f2-120">ネイティブ コードのアドレスが指定されているとき、要求につき構造体を設定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="a62f2-120">Used to populate the structure per request when given a native code address.</span></span>                    |
| `rejitDataCurrent`           | <span data-ttu-id="a62f2-121">インストルメント化された最新バージョンのメソッドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a62f2-121">Information about the latest instrumented version of the method.</span></span>                                   |
| `rejitDataRequested`         | <span data-ttu-id="a62f2-122">要求されたネイティブのアドレスの Rejit 情報。</span><span class="sxs-lookup"><span data-stu-id="a62f2-122">Rejit information for the requested native address.</span></span>                                             |
| `cJittedRejitVersions`       | <span data-ttu-id="a62f2-123">メソッドは実装を通じて rejitted された回数。</span><span class="sxs-lookup"><span data-stu-id="a62f2-123">Number of times the method has been rejitted through instrumentation.</span></span>                           |


## <a name="remarks"></a><span data-ttu-id="a62f2-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="a62f2-124">Remarks</span></span>

<span data-ttu-id="a62f2-125">この構造は、ランタイム内に収めるし、任意のヘッダーまたはライブラリ ファイルでは公開されません。</span><span class="sxs-lookup"><span data-stu-id="a62f2-125">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="a62f2-126">これを使用するには、上で指定した構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="a62f2-126">To use it, define the structure as specified above.</span></span>

## <a name="requirements"></a><span data-ttu-id="a62f2-127">必要条件</span><span class="sxs-lookup"><span data-stu-id="a62f2-127">Requirements</span></span>
<span data-ttu-id="a62f2-128">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a62f2-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="a62f2-129">**ヘッダー:** なし</span><span class="sxs-lookup"><span data-stu-id="a62f2-129">**Header:** None</span></span>  
<span data-ttu-id="a62f2-130">**ライブラリ:** なし</span><span class="sxs-lookup"><span data-stu-id="a62f2-130">**Library:** None</span></span>  
<span data-ttu-id="a62f2-131">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a62f2-131">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="a62f2-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="a62f2-132">See also</span></span>
- [<span data-ttu-id="a62f2-133">デバッグ</span><span class="sxs-lookup"><span data-stu-id="a62f2-133">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="a62f2-134">デバッグ構造体</span><span class="sxs-lookup"><span data-stu-id="a62f2-134">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="a62f2-135">共有のデータ型</span><span class="sxs-lookup"><span data-stu-id="a62f2-135">Common Data Types</span></span>](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md)
