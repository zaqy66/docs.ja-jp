---
title: IEnumRAWINPUTDEVIC:Next
ms.date: 03/30/2017
helpviewer_keywords:
- Next method [WPF]
ms.assetid: 3698b44d-510e-4d18-b32b-85f17188ee26
ms.openlocfilehash: 329a2cd96346e199ee834856dd6dbfac6175b722
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43515318"
---
# <a name="ienumrawinputdevicnext"></a>IEnumRAWINPUTDEVIC:Next
次の列挙`celt` [RAWINPUTDEVICE](https://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp)構造体、列挙子の一覧で、それらを返す`rgelt`で列挙された要素の実際の数とともに`pceltFetched`します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT Next(  
      [in] ULONG celt,  
      [out, size_is(celt), length_is(*pceltFetched)] RAWINPUTDEVICE *rgelt,  
      [out] ULONG *pceltFetched);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `celt`  
  
 [in]数[RAWINPUTDEVICE](https://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp)構造体で返される`rgelt`します。  
  
 `rgelt`  
  
 [out] 列挙された RAWINPUTDEVICE 構造体を受け取る size celt (またはそれ以上) の配列。  
  
 `pceltFetched`  
  
 [out] `rgelt` に実際に指定された要素の数へのポインター。 `NULL` が 1 の場合、呼び出し元は `rgelt` に渡すことができます。  
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値  
 指定された要素の数が `celt` の場合は HRESULT: S_OK。それ以外の場合は S_FALSE。
