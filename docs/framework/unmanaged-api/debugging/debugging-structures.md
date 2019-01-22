---
title: デバッグ構造体
ms.date: 03/30/2017
helpviewer_keywords:
- unmanaged structures [.NET Framework], debugging
- debugging structures [.NET Framework]
- structures [.NET Framework debugging]
ms.assetid: 173ba2c2-ab34-49ae-b6a8-e5c49882bf05
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 23aa619d666f2e0b9eb67ab4cf8d4f92761865d3
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54415326"
---
# <a name="debugging-structures"></a>デバッグ構造体
このセクションでは、デバッグ API が使用するアンマネージ構造体について説明します。  
  
## <a name="in-this-section"></a>このセクションの内容  
 [CLR_DEBUGGING_VERSION 構造体](../../../../docs/framework/unmanaged-api/debugging/clr-debugging-version-structure.md)  
 デバッグのために共通言語ランタイム (CLR) の製品バージョンを定義します。  
  
 [CodeChunkInfo Structure1](../../../../docs/framework/unmanaged-api/debugging/codechunkinfo-structure.md)  
 メモリ内のコードの単一のチャンクを表しています。  
  
 [CorDebugBlockingObject 構造体](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md)  
 スレッドをブロックしているオブジェクトとスレッドがブロックされている理由を定義します。  
  
 [CorDebugEHClause 構造体](../../../../docs/framework/unmanaged-api/debugging/cordebugehclause-structure.md)  
 中間言語 (IL) の特定の部分の例外処理 (EH) 句を表しています。  
  
 [CorDebugExceptionObjectStackFrame 構造体](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md)  
 例外オブジェクトのスタック フレームの情報を表しています。  
  
 [CorDebugExceptionObjectStackFrame 構造体](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md)  
 マップを[!INCLUDE[wrt](../../../../includes/wrt-md.md)]を対応する GUID [ICorDebugType](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-interface.md)オブジェクト。  
  
 COR_ACTIVE_FUNCTION  
 スレッドのフレームで現在アクティブな機能に関する情報が含まれます。  
  
 [COR_ARRAY_LAYOUT 構造体](../../../../docs/framework/unmanaged-api/debugging/cor-array-layout-structure.md)  
 メモリ内の配列オブジェクトのレイアウトに関する情報が提供されます。  
  
 COR_DEBUG_IL_TO_NATIVE_MAP  
 Microsoft intermediate language (MSIL) コードをネイティブ コードにマップするために使用するオフセットが含まれます。  
  
 COR_DEBUG_STEP_RANGE  
 コードの範囲に関するオフセット情報が含まれます。  
  
 [COR_FIELD 構造体](../../../../docs/framework/unmanaged-api/debugging/cor-field-structure.md)  
 オブジェクトのフィールドに関する情報が提供されます。  
  
 [COR_GC_REFERENCE 構造体](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md)  
 ガベージ コレクトされるオブジェクトに関する情報が含まれます。  
  
 [COR_HEAPINFO 構造体](../../../../docs/framework/unmanaged-api/debugging/cor-heapinfo-structure.md)  
 列挙可能かどうかなど、ガベージ コレクション ヒープに関する情報が提供されます。  
  
 [COR_HEAPOBJECT 構造体](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md)  
 マネージド ヒープ上のオブジェクトに関する情報が提供されます。  
  
 COR_IL_MAP  
 機能の相対オフセットでの変更を指定します。  
  
 [COR_SEGMENT 構造体](../../../../docs/framework/unmanaged-api/debugging/cor-segment-structure.md)  
 マネージド ヒープのメモリ領域に関する情報が含まれます。  
  
 [COR_TYPEID 構造体](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md)  
 型識別子が含まれます。  
  
 [COR_TYPE_LAYOUT 構造体](../../../../docs/framework/unmanaged-api/debugging/cor-type-layout-structure.md)  
 メモリ内のオブジェクトのレイアウトに関する情報が提供されます。  
  
 COR_VERSION  
 共通言語ランタイムの標準の 4 つの部分のバージョン番号を保存します。  
  
 [StackTrace_SimpleContext 構造体](../../../../docs/framework/unmanaged-api/debugging/stacktrace-simplecontext-structure.md)  
 完全な `CONTEXT` 構造の代わりに使用できる単純なコンテキストを提供します。

 [CLRDATA_ADDRESS_RANGE 構造](../../../../docs/framework/unmanaged-api/debugging/clrdata-address-range-structure.md)アドレスの範囲を定義します。
 
 [CLRDATA_IL_ADDRESS_MAP 構造](../../../../docs/framework/unmanaged-api/debugging/clrdata-il-address-map-structure.md)アドレスへのマッピングから、IL を定義します。
 
 [DacpGetModuleAddress 構造](../../../../docs/framework/unmanaged-api/debugging/dacpgetmoduleaddress-structure.md)モジュール アドレス要求のコンテナーを定義します。

  
## <a name="related-sections"></a>関連項目  
 [デバッグ コクラス](../../../../docs/framework/unmanaged-api/debugging/debugging-coclasses.md)  
  
 [デバッグ インターフェイス](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
  
 [デバッグ グローバル静的関数](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)  
  
 [列挙型のデバッグ](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)  
  
 [デバッグ](../../../../docs/framework/unmanaged-api/debugging/index.md)
