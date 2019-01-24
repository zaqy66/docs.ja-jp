---
title: ExportNestedTypeForwarder メソッド
ms.date: 03/30/2017
api_name:
- IALink.ExportNestedTypeForwarder
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ExportNestedTypeForwarder
helpviewer_keywords:
- ExportNestedTypeForwarder method
ms.assetid: 886ea6c5-6b26-4b88-8bf6-448d6d191950
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 25b7a708bb2f16433d9de9b5fc1c178cb48874a7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54658469"
---
# <a name="exportnestedtypeforwarder-method"></a>ExportNestedTypeForwarder メソッド
指定したアセンブリの型のテーブルを入れ子にされた型の型フォワーダーを追加します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT ExportNestedTypeForwarder(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    mdTypeDef       TypeToken,  
    mdExportedType  ParentType,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;  
```  
  
#### <a name="parameters"></a>パラメーター  
 `AssemblyID`  
 エクスポートするアセンブリの ID。  
  
 `FileToken`  
 ファイルの種類を定義するファイルのトークンまたはアセンブリの ID。  
  
 `TypeToken`  
 型のトークンです。  
  
 `ParentType`  
 親の種類のトークンです。  
  
 `pszTypename`  
 エクスポートする完全修飾型名。  
  
 `dwFlags`  
 `ComType` フラグなど`tdPublic`または`tdNested`します。  
  
 `pType`  
 エクスポート型のトークンを受け取ります。 これは、入れ子にされた型の生成にのみ必要です。  
  
## <a name="return-value"></a>戻り値  
 メソッドが成功した場合は、S_OK を返します。  
  
## <a name="requirements"></a>必要条件  
 Alink.h が必要です。  
  
## <a name="see-also"></a>関連項目
- [IALink インターフェイス](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [IALink2 インターフェイス](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [ALink API](../../../../docs/framework/unmanaged-api/alink/index.md)
