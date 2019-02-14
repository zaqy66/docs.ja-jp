---
title: StrongNameErrorInfo 関数
ms.date: 03/30/2017
api_name:
- StrongNameErrorInfo
api_location:
- mscoree.dll
- mscorsn.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameErrorInfo
helpviewer_keywords:
- StrongNameErrorInfo function [.NET Framework strong naming]
ms.assetid: e91bf8c3-7c26-4732-938e-2e5b04abfc99
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b3d7555ec5b87957ff1c8e085a4c3ac44c660b0c
ms.sourcegitcommit: af0a22a4eb11bbcd33baec49150d551955b50a16
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2019
ms.locfileid: "56260817"
---
# <a name="strongnameerrorinfo-function"></a>StrongNameErrorInfo 関数
厳密な名前の関数のいずれかに基づいて最後に発生したエラー コードが取得されます。  
  
 この関数は非推奨とされました。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT StrongNameErrorInfo ();   
```  
  
## <a name="return-value"></a>戻り値  
 最終 COM エラー コードの厳密な名前の関数のいずれかによって設定します。  
  
## <a name="remarks"></a>Remarks  
 厳密な名前のメソッドのほとんどは、単純なを返す`true`または`false`が正常に完了を示す値。 使用して、`StrongNameErrorInfo`厳密な名前の関数によって生成された最後のエラーを示す HRESULT を取得します。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** StrongName.h  
  
 **ライブラリ:** MsCorEE.dll でリソースとして含まれます  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
