---
title: GetRawInputDevices
ms.date: 03/30/2017
helpviewer_keywords:
- raw input [WPF]
ms.assetid: c4d37ecd-065a-4d1c-9e6c-26804ae968ca
ms.openlocfilehash: 18564e0de8f88e89f8fb71d28ee3bfeccceea4ff
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54507565"
---
# <a name="getrawinputdevices"></a><span data-ttu-id="1ad5e-102">GetRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="1ad5e-102">GetRawInputDevices</span></span>
<span data-ttu-id="1ad5e-103">PresentationHost.exe が、ホスト アプリケーションに必要な未加工入力デバイス (ヒューマン インターフェイス デバイス) を検出できるようにします。</span><span class="sxs-lookup"><span data-stu-id="1ad5e-103">Allows PresentationHost.exe to discover the raw input devices (Human Interface Devices) that the host application is interested in.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ad5e-104">構文</span><span class="sxs-lookup"><span data-stu-id="1ad5e-104">Syntax</span></span>  
  
```  
HRESULT GetRawInputDevices( [out] IEnumRAWINPUTDEVICE **ppEnum );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1ad5e-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1ad5e-105">Parameters</span></span>  
 `ppEnum`  
  
 <span data-ttu-id="1ad5e-106">[out]ポインター、 [IEnumRAWINPUTDEVICE](../../../../docs/framework/wpf/app-development/ienumrawinputdevice.md)未加工入力デバイスを列挙するためです。</span><span class="sxs-lookup"><span data-stu-id="1ad5e-106">[out] A pointer to an [IEnumRAWINPUTDEVICE](../../../../docs/framework/wpf/app-development/ienumrawinputdevice.md) for enumerating the raw input devices.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1ad5e-107">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="1ad5e-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="1ad5e-108">HRESULT:</span><span class="sxs-lookup"><span data-stu-id="1ad5e-108">HRESULT:</span></span>  
  
 <span data-ttu-id="1ad5e-109">S_OK - [IEnumRAWINPUTDEVICE](../../../../docs/framework/wpf/app-development/ienumrawinputdevice.md) S_OK が返された場合のみ PresentationHost.exe によってに使用されます。</span><span class="sxs-lookup"><span data-stu-id="1ad5e-109">S_OK - [IEnumRAWINPUTDEVICE](../../../../docs/framework/wpf/app-development/ienumrawinputdevice.md) will only be used by PresentationHost.exe if S_OK is returned.</span></span>  
  
 <span data-ttu-id="1ad5e-110">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="1ad5e-110">E_NOTIMPL</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1ad5e-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="1ad5e-111">Remarks</span></span>  
 <span data-ttu-id="1ad5e-112">未加工入力デバイスは、キーボード、マウス、およびリモート コントロールのような比較的新しいデバイスを含む入力デバイスのセットです。</span><span class="sxs-lookup"><span data-stu-id="1ad5e-112">Raw input devices are the set of input devices that includes keyboards, mice, and less traditional devices like remote controls.</span></span>  
  
 <span data-ttu-id="1ad5e-113">未加工の入力デバイスの一覧を取得すると、PresentationHost.exe は WM_INPUT 通知メッセージを受信するデバイスを登録します。</span><span class="sxs-lookup"><span data-stu-id="1ad5e-113">Once the list of raw input devices has been retrieved, PresentationHost.exe registers with the devices to receive WM_INPUT notification messages.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ad5e-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ad5e-114">See also</span></span>
- [<span data-ttu-id="1ad5e-115">GetRawInputDeviceList</span><span class="sxs-lookup"><span data-stu-id="1ad5e-115">GetRawInputDeviceList</span></span>](/windows/desktop/api/winuser/nf-winuser-getrawinputdevicelist)
- [<span data-ttu-id="1ad5e-116">FilterInputMessage</span><span class="sxs-lookup"><span data-stu-id="1ad5e-116">FilterInputMessage</span></span>](../../../../docs/framework/wpf/app-development/filterinputmessage.md)
