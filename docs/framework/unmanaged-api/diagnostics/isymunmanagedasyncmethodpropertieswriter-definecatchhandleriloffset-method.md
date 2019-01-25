---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset メソッド
ms.date: 03/30/2017
ms.assetid: 92af7896-2201-408d-8b1b-23e28001eeac
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 55d35db387d6184f68ff31a74253d3d1610c806f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54741252"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinecatchhandleriloffset-method"></a>ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset メソッド
IL オフセットの非同期メソッドをラップする catch のコンパイラによって生成されたハンドラーを設定します。  
  
 生成された catch の IL オフセットは、場合と非ユーザー コードがユーザー コード メソッドで発生した場合でも、catch を処理するために、デバッガーによって使用されます。 具体的への応答で使用される、 **CatchHandlerFound**例外イベント。  
  
## <a name="syntax"></a>構文  
  
```idl  
HRESULT DefineCatchHandlerILOffset(    [in] ULONG32 catchHandlerOffset);  
```  
  
#### <a name="parameters"></a>パラメーター  
  
|パラメーター|説明|  
|---------------|-----------------|  
|`catchHandlerOffset`||  
  
## <a name="return-value"></a>戻り値  
 `HRESULT` を返します。  
  
## <a name="requirements"></a>必要条件  
 **ヘッダー:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>関連項目
- [ISymUnmanagedAsyncMethodPropertiesWriter インターフェイス](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
