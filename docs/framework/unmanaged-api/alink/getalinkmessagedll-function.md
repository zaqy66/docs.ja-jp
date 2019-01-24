---
title: GetALinkMessageDll 関数
ms.date: 03/30/2017
api_name:
- GetALinkMessageDll
api_location:
- alink.dll
api_type:
- DLLExport
f1_keywords:
- GetALinkMessageDll
helpviewer_keywords:
- Alink API, GetALinkMessageDll function
- GetALinkMessageDll function
ms.assetid: 67985a22-88a2-4c54-8d99-4bcde9d6213e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 632f19e0ead57d5508265fece578bb22f18ba54a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722726"
---
# <a name="getalinkmessagedll-function"></a>GetALinkMessageDll 関数
検索し、メッセージ DLL を読み込みます。 メッセージ DLL が発見または読み込まれた場合は、0 を返します。 メッセージ DLL は、言語 ID の名前を持つサブディレクトリまたは現在のディレクトリ内のいずれかになります。  
  
## <a name="syntax"></a>構文  
  
```  
HINSTANCE WINAPI GetALinkMessageDll();  
```  
  
## <a name="requirements"></a>必要条件  
 **ヘッダー:** alink.h  
  
 **ライブラリ**: alink.dll  
  
## <a name="see-also"></a>関連項目
- [Al.exe (アセンブリ リンカー)](../../../../docs/framework/tools/al-exe-assembly-linker.md)
