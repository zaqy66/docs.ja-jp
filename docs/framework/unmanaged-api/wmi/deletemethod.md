---
title: DeleteMethod 関数 (アンマネージ API リファレンス)
description: DeleteMethod 関数では、CIM クラスの定義から、指定されたメソッドを削除します。
ms.date: 11/06/2017
api_name:
- DeleteMethod
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- DeleteMethod
helpviewer_keywords:
- DeleteMethod function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5996ce41c80cb54c4fcb9104c2993c85bcc2b466
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2018
ms.locfileid: "45510235"
---
# <a name="deletemethod-function"></a><span data-ttu-id="7abab-103">DeleteMethod 関数</span><span class="sxs-lookup"><span data-stu-id="7abab-103">DeleteMethod function</span></span>
<span data-ttu-id="7abab-104">CIM クラスの定義から、指定されたメソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="7abab-104">Deletes the specified method from a CIM class definition.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="7abab-105">構文</span><span class="sxs-lookup"><span data-stu-id="7abab-105">Syntax</span></span>  
  
```  
HRESULT Delete (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LPCWSTR           wszName 
); 
```  

## <a name="parameters"></a><span data-ttu-id="7abab-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7abab-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="7abab-107">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="7abab-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="7abab-108">[in]ポインター、 [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject)インスタンス。</span><span class="sxs-lookup"><span data-stu-id="7abab-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`wszName`  
<span data-ttu-id="7abab-109">[in]クラス テーブルから削除するメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="7abab-109">[in] The name of the method to remove from the class table.</span></span> <span data-ttu-id="7abab-110">`wszName` 有効なポインターである必要があります`LPCWSTR`します。</span><span class="sxs-lookup"><span data-stu-id="7abab-110">`wszName` must be a pointer to a valid `LPCWSTR`.</span></span>

## <a name="return-value"></a><span data-ttu-id="7abab-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="7abab-111">Return value</span></span>

<span data-ttu-id="7abab-112">この関数によって返される次の値が定義されている、 *WbemCli.h*ヘッダー ファイル、またはすることができますに定数としてコードで定義します。</span><span class="sxs-lookup"><span data-stu-id="7abab-112">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="7abab-113">定数</span><span class="sxs-lookup"><span data-stu-id="7abab-113">Constant</span></span>  |<span data-ttu-id="7abab-114">値</span><span class="sxs-lookup"><span data-stu-id="7abab-114">Value</span></span>  |<span data-ttu-id="7abab-115">説明</span><span class="sxs-lookup"><span data-stu-id="7abab-115">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_NOT_FOUND` | <span data-ttu-id="7abab-116">0x80041002</span><span class="sxs-lookup"><span data-stu-id="7abab-116">0x80041002</span></span> | <span data-ttu-id="7abab-117">指定されたメソッドが存在しません。</span><span class="sxs-lookup"><span data-stu-id="7abab-117">The specified method does not exist.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="7abab-118">0x80041006</span><span class="sxs-lookup"><span data-stu-id="7abab-118">0x80041006</span></span> | <span data-ttu-id="7abab-119">操作を完了するのに十分なメモリがありません。</span><span class="sxs-lookup"><span data-stu-id="7abab-119">There is not enough memory to complete the operation.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="7abab-120">0</span><span class="sxs-lookup"><span data-stu-id="7abab-120">0</span></span> | <span data-ttu-id="7abab-121">関数呼び出しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="7abab-121">The function call was successful.</span></span>  |

## <a name="remarks"></a><span data-ttu-id="7abab-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="7abab-122">Remarks</span></span>

<span data-ttu-id="7abab-123">この関数の呼び出しをラップする、 [IWbemClassObject::DeleteMethod](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-deletemethod)メソッド。</span><span class="sxs-lookup"><span data-stu-id="7abab-123">This function wraps a call to the [IWbemClassObject::DeleteMethod](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-deletemethod) method.</span></span>

<span data-ttu-id="7abab-124">メソッドの削除はサポートされていません[IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) CIM インスタンスを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="7abab-124">Method deletion is not supported for [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointers that point to CIM instances.</span></span>

## <a name="requirements"></a><span data-ttu-id="7abab-125">要件</span><span class="sxs-lookup"><span data-stu-id="7abab-125">Requirements</span></span>  
 <span data-ttu-id="7abab-126">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7abab-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7abab-127">**ヘッダー:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="7abab-127">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="7abab-128">**.NET Framework のバージョン:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7abab-128">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7abab-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="7abab-129">See also</span></span>  
[<span data-ttu-id="7abab-130">WMI およびパフォーマンス カウンター (アンマネージ API リファレンス)</span><span class="sxs-lookup"><span data-stu-id="7abab-130">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
