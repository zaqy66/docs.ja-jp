---
title: ISymUnmanagedBinder2 インターフェイス
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder2 Interface
helpviewer_keywords:
- ISymUnmanagedBinder2 interface [.NET Framework debugging]
ms.assetid: 7a59f405-73e8-4434-8bcc-a9dc45ea08e6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 52b0f6b9d3e0ea3d6fe5f14badb8401b1a0c2c63
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50187493"
---
# <a name="isymunmanagedbinder2-interface"></a>ISymUnmanagedBinder2 インターフェイス
アンマネージ コードのシンボル バインダーを表し、拡張、 [ISymUnmanagedBinder](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)インターフェイス。  
  
> [!IMPORTANT]
>  信頼できないソースからプログラム データベース (PDB) ファイルをセキュリティ リスクになります。  
  
## <a name="methods"></a>メソッド  
  
|メソッド|説明|  
|------------|-----------------|  
|[GetReaderForFile2 メソッド](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md)|メタデータ インターフェイスおよびファイル名を指定されたを返します、正しい[ISymUnmanagedReader](isymunmanagedreader-interface.md)をモジュールに関連付けられているデバッグ シンボルを読み取る。 広範な検索の提供、 [isymunmanagedbinder::getreaderforfile](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md)メソッド。|  
  
## <a name="requirements"></a>必要条件  
 **ヘッダー:** CorSym.idl、CorSym.h  
  
## <a name="see-also"></a>関連項目  
 [シンボル ストア診断インターフェイス](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)  
 [ISymUnmanagedBinder インターフェイス](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)  
 [ISymUnmanagedBinder3 インターフェイス](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-interface.md)
