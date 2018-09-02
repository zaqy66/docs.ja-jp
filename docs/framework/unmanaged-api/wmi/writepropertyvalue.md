---
title: WritePropertyValue 関数 (アンマネージ API リファレンス)
description: WritePropertyValue 関数は、プロパティにバイトを書き込みます。
ms.date: 11/06/2017
api_name:
- WritePropertyValue
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- WritePropertyValue
helpviewer_keywords:
- WritePropertyValue function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f2a4eb444967390492be33b25866de8a93a1698c
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43393908"
---
# <a name="writepropertyvalue-function"></a><span data-ttu-id="e8b1e-103">WritePropertyValue 関数</span><span class="sxs-lookup"><span data-stu-id="e8b1e-103">WritePropertyValue function</span></span>
<span data-ttu-id="e8b1e-104">プロパティのハンドルによって識別されたプロパティに指定したバイト数を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-104">Writes a specified number of bytes to a property identified by a property handle.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="e8b1e-105">構文</span><span class="sxs-lookup"><span data-stu-id="e8b1e-105">Syntax</span></span>  
  
```  
HRESULT WritePropertyValue (
   [in] int                  vFunc, 
   [in] IWbemObjectAccess*   ptr, 
   [in] long                 lHandle,
   [in] long                 lNumBytes,
   [in] byte*                aData
); 
```  

## <a name="parameters"></a><span data-ttu-id="e8b1e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e8b1e-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="e8b1e-107">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="e8b1e-108">[in]ポインター、 [IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess)インスタンス。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-108">[in] A pointer to an [IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess) instance.</span></span>

`lHandle`  
<span data-ttu-id="e8b1e-109">[in]このプロパティを識別するハンドルを格納する整数。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-109">[in] An integer that contains the handle that identifies this property.</span></span> <span data-ttu-id="e8b1e-110">呼び出すことによって、ハンドルを取得できます、 [GetPropertyHandle](getpropertyhandle.md)関数。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-110">The handle can be retrieved by calling the [GetPropertyHandle](getpropertyhandle.md) function.</span></span>   

`lNumBytes`  
<span data-ttu-id="e8b1e-111">[in]プロパティに書き込まれるバイト数。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-111">[in] The number of bytes being written to the property.</span></span> <span data-ttu-id="e8b1e-112">参照してください、[解説](#remarks)詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-112">See the [Remarks](#remarks) section for more information.</span></span>

`pHandle`   
<span data-ttu-id="e8b1e-113">[out]データを格納するバイト配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-113">[out] A pointer to the byte array that contains the data.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8b1e-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="e8b1e-114">Return value</span></span>

<span data-ttu-id="e8b1e-115">この関数によって返される次の値が定義されている、 *WbemCli.h*ヘッダー ファイル、またはすることができますに定数としてコードで定義します。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-115">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="e8b1e-116">定数</span><span class="sxs-lookup"><span data-stu-id="e8b1e-116">Constant</span></span>  |<span data-ttu-id="e8b1e-117">値</span><span class="sxs-lookup"><span data-stu-id="e8b1e-117">Value</span></span>  |<span data-ttu-id="e8b1e-118">説明</span><span class="sxs-lookup"><span data-stu-id="e8b1e-118">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="e8b1e-119">0x80041008</span><span class="sxs-lookup"><span data-stu-id="e8b1e-119">0x80041008</span></span> | <span data-ttu-id="e8b1e-120">パラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-120">A parameter is not valid.</span></span> |
|`WBEM_E_TYPE_MISMATCH` | <span data-ttu-id="e8b1e-121">0x80041005</span><span class="sxs-lookup"><span data-stu-id="e8b1e-121">0x80041005</span></span> | <span data-ttu-id="e8b1e-122">型の不一致が発生しました。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-122">A type mismatch occurred.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="e8b1e-123">0</span><span class="sxs-lookup"><span data-stu-id="e8b1e-123">0</span></span> | <span data-ttu-id="e8b1e-124">関数呼び出しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-124">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="e8b1e-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="e8b1e-125">Remarks</span></span>

<span data-ttu-id="e8b1e-126">この関数の呼び出しをラップする、 [IWbemClassObject::WritePropertyValue](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-writepropertyvalue)メソッド。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-126">This function wraps a call to the [IWbemClassObject::WritePropertyValue](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-writepropertyvalue) method.</span></span>

<span data-ttu-id="e8b1e-127">この関数を使用して、文字列およびすべて他の非設定`DWORD`以外または -`QWORD`データ。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-127">Use this function to set string and all other non-`DWORD` or non-`QWORD` data.</span></span>

<span data-ttu-id="e8b1e-128">非文字列プロパティの値の`lNumBytes`指定されたプロパティ型の適切なデータ サイズにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-128">For nonstring property values, `lNumBytes` must be the correct data size of the property type specified.</span></span> <span data-ttu-id="e8b1e-129">文字列プロパティの値、`lNumBytes`長さにする必要があります (バイト単位) で指定した文字列と文字列の偶数の長さをバイト数である必要があり、null 終端文字の後にします。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-129">For string property values, `lNumBytes` must be the length of the specified string in bytes, and the string itself must be of an even length in bytes and be followed with a null-termination character.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8b1e-130">要件</span><span class="sxs-lookup"><span data-stu-id="e8b1e-130">Requirements</span></span>  
<span data-ttu-id="e8b1e-131">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8b1e-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8b1e-132">**ヘッダー:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="e8b1e-132">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="e8b1e-133">**.NET Framework のバージョン:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="e8b1e-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8b1e-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8b1e-134">See also</span></span>  
[<span data-ttu-id="e8b1e-135">WMI およびパフォーマンス カウンター (アンマネージ API リファレンス)</span><span class="sxs-lookup"><span data-stu-id="e8b1e-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
