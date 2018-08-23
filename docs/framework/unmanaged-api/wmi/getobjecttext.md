---
title: GetObjectText 関数 (アンマネージ API リファレンス)
description: GetObjectText 関数は、MOF 構文では、オブジェクトのテキストのレンダリングを返します。
ms.date: 11/06/2017
api_name:
- GetObjectText
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetObjectText
helpviewer_keywords:
- GetObjectText function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 24ba4b37cc8221df4e018d172996c0910ec07f7d
ms.sourcegitcommit: a1e35d4e94edab384a63406c0a5438306873031b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/21/2018
ms.locfileid: "42754520"
---
# <a name="getobjecttext-function"></a><span data-ttu-id="763a6-103">GetObjectText 関数</span><span class="sxs-lookup"><span data-stu-id="763a6-103">GetObjectText function</span></span>
<span data-ttu-id="763a6-104">管理オブジェクト フォーマット (MOF) 構文では、オブジェクトのテキストのレンダリングを返します。</span><span class="sxs-lookup"><span data-stu-id="763a6-104">Returns a textual rendering of the object in the Managed Object Format (MOF) syntax.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="763a6-105">構文</span><span class="sxs-lookup"><span data-stu-id="763a6-105">Syntax</span></span>  
  
```  
HRESULT GetObjectText (
   [in] int                vFunc, 
   [in] IWbemClassObject*   ptr, 
   [in] LONG                lFlags,
   [out] BSTR*              pstrObjectText
); 
```  

## <a name="parameters"></a><span data-ttu-id="763a6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="763a6-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="763a6-107">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="763a6-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="763a6-108">[in]ポインター、 [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject)インスタンス。</span><span class="sxs-lookup"><span data-stu-id="763a6-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`lFlags`  
<span data-ttu-id="763a6-109">[in]通常は 0。</span><span class="sxs-lookup"><span data-stu-id="763a6-109">[in] Normally 0.</span></span> <span data-ttu-id="763a6-110">場合`WBEM_FLAG_NO_FLAVORS`(または 0x1) 修飾子は、伝達またはフレーバーの情報も指定します。</span><span class="sxs-lookup"><span data-stu-id="763a6-110">If `WBEM_FLAG_NO_FLAVORS` (or 0x1) is specified, qualifiers are included without propagation or flavor information.</span></span>

`pstrObjectText`   
<span data-ttu-id="763a6-111">[out]ポインターを`null`エントリ。</span><span class="sxs-lookup"><span data-stu-id="763a6-111">[out] A pointer to a `null` on entry.</span></span> <span data-ttu-id="763a6-112">戻り時に、新しく割り当てられた`BSTR`がオブジェクトの MOF 構文のレンダリングを格納しています。</span><span class="sxs-lookup"><span data-stu-id="763a6-112">On return, a newly allocated `BSTR` that contains a MOF syntax rendering of the object.</span></span>  

## <a name="return-value"></a><span data-ttu-id="763a6-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="763a6-113">Return value</span></span>

<span data-ttu-id="763a6-114">この関数によって返される次の値が定義されている、 *WbemCli.h*ヘッダー ファイル、またはすることができますに定数としてコードで定義します。</span><span class="sxs-lookup"><span data-stu-id="763a6-114">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="763a6-115">定数</span><span class="sxs-lookup"><span data-stu-id="763a6-115">Constant</span></span>  |<span data-ttu-id="763a6-116">値</span><span class="sxs-lookup"><span data-stu-id="763a6-116">Value</span></span>  |<span data-ttu-id="763a6-117">説明</span><span class="sxs-lookup"><span data-stu-id="763a6-117">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_FAILED` | <span data-ttu-id="763a6-118">0x80041001</span><span class="sxs-lookup"><span data-stu-id="763a6-118">0x80041001</span></span> | <span data-ttu-id="763a6-119">一般的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="763a6-119">There has been a general failure.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="763a6-120">0x80041008</span><span class="sxs-lookup"><span data-stu-id="763a6-120">0x80041008</span></span> | <span data-ttu-id="763a6-121">パラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="763a6-121">A parameter is not valid.</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="763a6-122">0x80041006</span><span class="sxs-lookup"><span data-stu-id="763a6-122">0x80041006</span></span> | <span data-ttu-id="763a6-123">操作を完了するのに十分なメモリがあります。</span><span class="sxs-lookup"><span data-stu-id="763a6-123">Not enough memory is available to complete the operation.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="763a6-124">0</span><span class="sxs-lookup"><span data-stu-id="763a6-124">0</span></span> | <span data-ttu-id="763a6-125">関数呼び出しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="763a6-125">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="763a6-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="763a6-126">Remarks</span></span>

<span data-ttu-id="763a6-127">この関数の呼び出しをラップする、 [IWbemClassObject::GetObjectText](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getobjecttext)メソッド。</span><span class="sxs-lookup"><span data-stu-id="763a6-127">This function wraps a call to the [IWbemClassObject::GetObjectText](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getobjecttext) method.</span></span>

<span data-ttu-id="763a6-128">オブジェクトに関するすべての情報が、元のオブジェクトを再作成できる MOF コンパイラのための十分な情報のみ、返される MOF テキストは含まれません。</span><span class="sxs-lookup"><span data-stu-id="763a6-128">The MOF text returned does not contain all the information about the object, but only enough information for the MOF compiler to be able to recreate the original object.</span></span> <span data-ttu-id="763a6-129">たとえば、伝達された修飾子または親クラスのプロパティは含まれません。</span><span class="sxs-lookup"><span data-stu-id="763a6-129">For instance, no propagated qualifiers or parent class properties are included.</span></span>

<span data-ttu-id="763a6-130">メソッドのパラメーターのテキストを再構築には、次のアルゴリズムが使用します。</span><span class="sxs-lookup"><span data-stu-id="763a6-130">The following algorithm is used to reconstruct the text of the parameters of a method:</span></span>

1. <span data-ttu-id="763a6-131">パラメーターは、その識別子の値の順序 resequenced されます。</span><span class="sxs-lookup"><span data-stu-id="763a6-131">Parameters are resequenced in the order of their identifier values.</span></span>
1. <span data-ttu-id="763a6-132">パラメーターとして指定されている`[in]`と`[out]`パラメーターを 1 つに結合されます。</span><span class="sxs-lookup"><span data-stu-id="763a6-132">Parameters that are specified as `[in]` and `[out]` are combined into a single parameter.</span></span>
 
<span data-ttu-id="763a6-133">`pstrObjectText` ポインターである必要があります、`null`ポインターが解放されないため、メソッド呼び出しの前に有効な文字列をポイントする必要がありますいない、関数が呼び出されると;。</span><span class="sxs-lookup"><span data-stu-id="763a6-133">`pstrObjectText` must be a pointer to a `null` when the function is called; it must not point to a string that is valid before the method call, because the pointer will not be deallocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="763a6-134">要件</span><span class="sxs-lookup"><span data-stu-id="763a6-134">Requirements</span></span>  
<span data-ttu-id="763a6-135">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="763a6-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="763a6-136">**ヘッダー:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="763a6-136">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="763a6-137">**.NET Framework のバージョン:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="763a6-137">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="763a6-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="763a6-138">See also</span></span>  
[<span data-ttu-id="763a6-139">WMI およびパフォーマンス カウンター (アンマネージ API リファレンス)</span><span class="sxs-lookup"><span data-stu-id="763a6-139">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
