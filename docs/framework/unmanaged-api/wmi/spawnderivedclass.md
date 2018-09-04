---
title: SpawnDerivedClass 関数 (アンマネージ API リファレンス)
description: SpawnDerivedClass 関数は、オブジェクトから派生した新しいオブジェクトを作成します。
ms.date: 11/06/2017
api_name:
- SpawnDerivedClass
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- SpawnDerivedClass
helpviewer_keywords:
- SpawnDerivedClass function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 04df65a29584f7e2de44389d815b915a541e38f0
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43507498"
---
# <a name="spawnderivedclass-function"></a><span data-ttu-id="fc002-103">SpawnDerivedClass 関数</span><span class="sxs-lookup"><span data-stu-id="fc002-103">SpawnDerivedClass function</span></span>
<span data-ttu-id="fc002-104">指定したオブジェクトから新たに派生するクラス オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="fc002-104">Creates a newly derived class object from a specified object.</span></span>    
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="fc002-105">構文</span><span class="sxs-lookup"><span data-stu-id="fc002-105">Syntax</span></span>  
  
```  
HRESULT SpawnDerivedClass (
   [in] int                  vFunc, 
   [in] IWbemClassObject*    ptr, 
   [in] LONG                 lFlags,
   [out] IWbemClassObject**  ppNewClass); 
```  

## <a name="parameters"></a><span data-ttu-id="fc002-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fc002-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="fc002-107">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="fc002-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="fc002-108">[in]ポインター、 [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject)インスタンス。</span><span class="sxs-lookup"><span data-stu-id="fc002-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`lFlags`  
<span data-ttu-id="fc002-109">[in]予約されています。</span><span class="sxs-lookup"><span data-stu-id="fc002-109">[in] Reserved.</span></span> <span data-ttu-id="fc002-110">このパラメーターは、0 を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc002-110">This parameter must be 0.</span></span>

`ppNewClass`  
<span data-ttu-id="fc002-111">[out]新しいクラス定義のオブジェクトへのポインターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="fc002-111">[out] Receives the pointer to the new class definition object.</span></span> <span data-ttu-id="fc002-112">新しいオブジェクトでないエラーが発生する場合、返されると`ppNewClass`は左未変更の状態します。</span><span class="sxs-lookup"><span data-stu-id="fc002-112">If an error occurs, a new object is not returned, and `ppNewClass` is left unmodified.</span></span> <span data-ttu-id="fc002-113">その値にすることはできません`null`します。</span><span class="sxs-lookup"><span data-stu-id="fc002-113">Its value cannot be `null`.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc002-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="fc002-114">Return value</span></span>

<span data-ttu-id="fc002-115">この関数によって返される次の値が定義されている、 *WbemCli.h*ヘッダー ファイル、またはすることができますに定数としてコードで定義します。</span><span class="sxs-lookup"><span data-stu-id="fc002-115">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="fc002-116">定数</span><span class="sxs-lookup"><span data-stu-id="fc002-116">Constant</span></span>  |<span data-ttu-id="fc002-117">値</span><span class="sxs-lookup"><span data-stu-id="fc002-117">Value</span></span>  |<span data-ttu-id="fc002-118">説明</span><span class="sxs-lookup"><span data-stu-id="fc002-118">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_FAILED` | <span data-ttu-id="fc002-119">0x80041001</span><span class="sxs-lookup"><span data-stu-id="fc002-119">0x80041001</span></span> | <span data-ttu-id="fc002-120">一般的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="fc002-120">There has been a general failure.</span></span> |
| `WBEM_E_INVALID_OPERATION` | <span data-ttu-id="fc002-121">0x80041016</span><span class="sxs-lookup"><span data-stu-id="fc002-121">0x80041016</span></span> | <span data-ttu-id="fc002-122">インスタンスからのクラスの生成などの無効な操作が要求されました。</span><span class="sxs-lookup"><span data-stu-id="fc002-122">An invalid operation, such as spawning a class from an instance, was requested.</span></span> |
| `WBEM_E_INCOMPLETE_CLASS` | <span data-ttu-id="fc002-123">ソース クラスが完全に定義されているか、Windows の管理を登録するため、新しい派生クラスは許可されていません。</span><span class="sxs-lookup"><span data-stu-id="fc002-123">The source class was not completely defined or registered with Windows Management, so a new derived class is not permitted.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="fc002-124">0x80041006</span><span class="sxs-lookup"><span data-stu-id="fc002-124">0x80041006</span></span> | <span data-ttu-id="fc002-125">操作を完了するのに十分なメモリがあります。</span><span class="sxs-lookup"><span data-stu-id="fc002-125">Not enough memory is available to complete the operation.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="fc002-126">0x80041008</span><span class="sxs-lookup"><span data-stu-id="fc002-126">0x80041008</span></span> | <span data-ttu-id="fc002-127">`ppNewClass` は `null` です。</span><span class="sxs-lookup"><span data-stu-id="fc002-127">`ppNewClass` is `null`.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="fc002-128">0</span><span class="sxs-lookup"><span data-stu-id="fc002-128">0</span></span> | <span data-ttu-id="fc002-129">関数呼び出しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="fc002-129">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="fc002-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="fc002-130">Remarks</span></span>

<span data-ttu-id="fc002-131">この関数の呼び出しをラップする、 [IWbemClassObject::SpawnDerivedClass](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone)メソッド。</span><span class="sxs-lookup"><span data-stu-id="fc002-131">This function wraps a call to the [IWbemClassObject::SpawnDerivedClass](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

<span data-ttu-id="fc002-132">`ptr` 生成されたオブジェクトの親クラスとなるクラス定義である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc002-132">`ptr` must be a class definition that becomes the parent class of the spawned object.</span></span> <span data-ttu-id="fc002-133">返されるオブジェクトでは、現在のオブジェクトのサブクラスになります。</span><span class="sxs-lookup"><span data-stu-id="fc002-133">The returned object becomes a subclass of the current object.</span></span>

<span data-ttu-id="fc002-134">返される新しいオブジェクト`ppNewClass`自動的に現在のオブジェクトのサブクラスになります。</span><span class="sxs-lookup"><span data-stu-id="fc002-134">The new object returned in `ppNewClass` automatically becomes a subclass of the current object.</span></span> <span data-ttu-id="fc002-135">この動作を上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="fc002-135">This behavior cannot be overridden.</span></span> <span data-ttu-id="fc002-136">サブクラス (派生クラス) を作成できる他の方法はありません。</span><span class="sxs-lookup"><span data-stu-id="fc002-136">There is no other method by which subclasses (derived classes) can be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc002-137">要件</span><span class="sxs-lookup"><span data-stu-id="fc002-137">Requirements</span></span>  
 <span data-ttu-id="fc002-138">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc002-138">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fc002-139">**ヘッダー:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="fc002-139">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="fc002-140">**.NET Framework のバージョン:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="fc002-140">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fc002-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc002-141">See also</span></span>  
[<span data-ttu-id="fc002-142">WMI およびパフォーマンス カウンター (アンマネージ API リファレンス)</span><span class="sxs-lookup"><span data-stu-id="fc002-142">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
