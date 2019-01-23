---
title: IEnumIDENTITY_ATTRIBUTE インターフェイス
ms.date: 03/30/2017
api_name:
- IEnumIDENTITY_ATTRIBUTE
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumIDENTITY_ATTRIBUTE
helpviewer_keywords:
- IEnumIDENTITY_ATTRIBUTE interface [.NET Framework fusion]
ms.assetid: c2ec2748-e9ae-4e1b-80db-6fcec5cb81a1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8ae940946c56cbc858690cccce61597d0016e40c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571809"
---
# <a name="ienumidentityattribute-interface"></a>IEnumIDENTITY_ATTRIBUTE インターフェイス
現在のスコープ内のコード オブジェクトの属性の列挙子として機能します。  
  
## <a name="methods"></a>メソッド  
  
|メソッド|説明|  
|------------|-----------------|  
|`IEnumIDENTITY_ATTRIBUTE::Clone`|新しいインターフェイス ポインターを取得`IEnumIDENTITY_ATTRIBUTE`これと同じメンバーを格納している`IEnumIDENTITY_ATTRIBUTE`します。|  
|`IEnumIDENTITY_ATTRIBUTE::CurrentIntoBuffer`|この要素に含まれるデータを書き込みます`IEnumIDENTITY_ATTRIBUTE`に指定されたデータ バッファー。|  
|`IEnumIDENTITY_ATTRIBUTE::Next`|指定した数の現在位置から始まり、属性を取得します。|  
|`IEnumIDENTITY_ATTRIBUTE::Reset`|これの先頭に、命令ポインターを移動`IEnumIDENTITY_ATTRIBUTE`します。|  
|`IEnumIDENTITY_ATTRIBUTE::Skip`|指定数の要素を現在の位置からでは、転送、命令ポインターを移動します。|  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** Isolation.h  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [Fusion インターフェイス](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
