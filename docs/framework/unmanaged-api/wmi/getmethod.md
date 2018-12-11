---
title: GetMethod 関数 (アンマネージ API リファレンス)
description: GetMethod 関数は、メソッドに関する情報を取得します。
ms.date: 11/06/2017
api_name:
- GetMethod
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetMethod
helpviewer_keywords:
- GetMethod function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 133e056663b208f2a0d12f05f31daaca95676dc5
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152319"
---
# <a name="getmethod-function"></a><span data-ttu-id="a61b9-103">GetMethod 関数</span><span class="sxs-lookup"><span data-stu-id="a61b9-103">GetMethod function</span></span>
<span data-ttu-id="a61b9-104">指定したメソッドに関する情報が取得されます。</span><span class="sxs-lookup"><span data-stu-id="a61b9-104">Retrieves information about the specified method.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="a61b9-105">構文</span><span class="sxs-lookup"><span data-stu-id="a61b9-105">Syntax</span></span>  
  
```  
HRESULT GetMethod (
   [in] int                vFunc, 
   [in] IWbemClassObject*   ptr, 
   [in] LPCWSTR             wszName,
   [in] LONG                lFlags,
   [out] IWbemClassObject** ppInSignature,
   [out] IWbemClassObject** ppOutSignature
); 
```  

## <a name="parameters"></a><span data-ttu-id="a61b9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a61b9-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="a61b9-107">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="a61b9-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="a61b9-108">[in]ポインター、 [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject)インスタンス。</span><span class="sxs-lookup"><span data-stu-id="a61b9-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`wszName`  
<span data-ttu-id="a61b9-109">[in]メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="a61b9-109">[in] The method name.</span></span> <span data-ttu-id="a61b9-110">このパラメーターにすることはできません`null`有効 をポイントする必要があります`LPCWSTR`します。</span><span class="sxs-lookup"><span data-stu-id="a61b9-110">This parameter cannot be `null` and must point to a valid `LPCWSTR`.</span></span>

`lFlags`  
<span data-ttu-id="a61b9-111">[in] 予約されています。</span><span class="sxs-lookup"><span data-stu-id="a61b9-111">[in] Reserved.</span></span> <span data-ttu-id="a61b9-112">このパラメーターは、0 を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a61b9-112">This parameter must be 0.</span></span>

`ppInSignature`   
<span data-ttu-id="a61b9-113">[out]アドレスへのポインター、 [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject)メソッドで paramteers を記述するインスタンス。</span><span class="sxs-lookup"><span data-stu-id="a61b9-113">[out] A pointer to the address of an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance that describes the in paramteers to the method.</span></span> <span data-ttu-id="a61b9-114">設定されている場合、このパラメーターは無視されます`null`します。</span><span class="sxs-lookup"><span data-stu-id="a61b9-114">This parameter is ignored if it is set to `null`.</span></span> 

`ppOutSignature`  
<span data-ttu-id="a61b9-115">[out]アドレスへのポインター、 [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject)メソッドに out パラメーターを記述するインスタンス。</span><span class="sxs-lookup"><span data-stu-id="a61b9-115">[out] A pointer to the address of an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance that describes the out parameters to the method.</span></span> <span data-ttu-id="a61b9-116">設定されている場合、このパラメーターは無視されます`null`します。</span><span class="sxs-lookup"><span data-stu-id="a61b9-116">This parameter is ignored if it is set to `null`.</span></span> 

## <a name="return-value"></a><span data-ttu-id="a61b9-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="a61b9-117">Return value</span></span>

<span data-ttu-id="a61b9-118">この関数によって返される次の値が定義されている、 *WbemCli.h*ヘッダー ファイル、またはすることができますに定数としてコードで定義します。</span><span class="sxs-lookup"><span data-stu-id="a61b9-118">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="a61b9-119">定数</span><span class="sxs-lookup"><span data-stu-id="a61b9-119">Constant</span></span>  |<span data-ttu-id="a61b9-120">値</span><span class="sxs-lookup"><span data-stu-id="a61b9-120">Value</span></span>  |<span data-ttu-id="a61b9-121">説明</span><span class="sxs-lookup"><span data-stu-id="a61b9-121">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="a61b9-122">0x80041002</span><span class="sxs-lookup"><span data-stu-id="a61b9-122">0x80041002</span></span> | <span data-ttu-id="a61b9-123">指定したプロパティが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="a61b9-123">The specified property was not found.</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="a61b9-124">0x80041006</span><span class="sxs-lookup"><span data-stu-id="a61b9-124">0x80041006</span></span> | <span data-ttu-id="a61b9-125">操作を完了するのに十分なメモリがあります。</span><span class="sxs-lookup"><span data-stu-id="a61b9-125">Not enough memory is available to complete the operation.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="a61b9-126">0</span><span class="sxs-lookup"><span data-stu-id="a61b9-126">0</span></span> | <span data-ttu-id="a61b9-127">関数呼び出しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="a61b9-127">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="a61b9-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="a61b9-128">Remarks</span></span>

<span data-ttu-id="a61b9-129">この関数の呼び出しをラップする、 [IWbemClassObject::GetMethod](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod)メソッド。</span><span class="sxs-lookup"><span data-stu-id="a61b9-129">This function wraps a call to the [IWbemClassObject::GetMethod](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod) method.</span></span>

<span data-ttu-id="a61b9-130">Windows の管理を設定できる、 [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject)へのポインター`null`メソッドにパラメーターがあるない場合。</span><span class="sxs-lookup"><span data-stu-id="a61b9-130">Windows Management can set the [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointer to `null` if the method has no in parameters.</span></span>

<span data-ttu-id="a61b9-131">`ppInSignature`と`ppOutSignature`in および out パラメーターをそれぞれのプロパティとして、説明、`IWbemClassObject`システム クラスのインスタンス[_Parameters](/windows/desktop/WmiSdk/--parameters)します。</span><span class="sxs-lookup"><span data-stu-id="a61b9-131">In `ppInSignature` and `ppOutSignature` describe in and out parameters, respectively, as properties in a `IWbemClassObject` instance of the system class [_Parameters](/windows/desktop/WmiSdk/--parameters).</span></span> <span data-ttu-id="a61b9-132">プロパティ`ppInsignature`という名前は`Param` *n*ここで、 *n*メソッド シグネチャ内のパラメーターの位置です (など`Param1`、`Param2`など。)。</span><span class="sxs-lookup"><span data-stu-id="a61b9-132">The properties in `ppInsignature` are named `Param`*n*, where *n* is the position of the parameter in the method signature (such as `Param1`, `Param2`, etc.).</span></span> <span data-ttu-id="a61b9-133">プロパティ`ppOutSignature`とも呼ば`Param` *n*、戻り値の名前は`ReturnValue`します。</span><span class="sxs-lookup"><span data-stu-id="a61b9-133">The properties in `ppOutSignature` are also named `Param`*n*, and the return value is named `ReturnValue`.</span></span> <span data-ttu-id="a61b9-134">詳細と例では、次を参照してください。 [IWbemClassObject::GetMethod メソッド](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod)します。</span><span class="sxs-lookup"><span data-stu-id="a61b9-134">For more information and an example, see [IWbemClassObject::GetMethod method](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod).</span></span>

## <a name="requirements"></a><span data-ttu-id="a61b9-135">必要条件</span><span class="sxs-lookup"><span data-stu-id="a61b9-135">Requirements</span></span>  
<span data-ttu-id="a61b9-136">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a61b9-136">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a61b9-137">**ヘッダー:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="a61b9-137">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="a61b9-138">**.NET Framework のバージョン:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a61b9-138">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a61b9-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="a61b9-139">See also</span></span>  
[<span data-ttu-id="a61b9-140">WMI およびパフォーマンス カウンター (アンマネージ API リファレンス)</span><span class="sxs-lookup"><span data-stu-id="a61b9-140">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
