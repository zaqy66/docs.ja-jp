---
title: ISymENCUnmanagedMethod::GetDocumentsForMethodCount メソッド
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetDocumentsForMethodCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetDocumentsForMethodCount
helpviewer_keywords:
- GetDocumentsForMethodCount method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetDocumentsForMethodCount method [.NET Framework debugging]
ms.assetid: cc1a823a-3ff3-4a33-b641-96edc93d2b17
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c13fc4270b44a2483c2e9aabaedcf8f0668d2e7c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743921"
---
# <a name="isymencunmanagedmethodgetdocumentsformethodcount-method"></a>ISymENCUnmanagedMethod::GetDocumentsForMethodCount メソッド
このメソッドの行が含まれるドキュメントの数を取得します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT GetDocumentsForMethodCount(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `pRetVal`  
 [out]ポインター、`ULONG32`ドキュメントの格納に必要なバッファーのサイズを受け取る。  
  
## <a name="return-value"></a>戻り値  
 メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。  
  
## <a name="requirements"></a>必要条件  
 **ヘッダー:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>関連項目
- [ISymENCUnmanagedMethod インターフェイス](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)
