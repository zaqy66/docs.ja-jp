---
title: スタートアップ設定スキーマ
ms.date: 03/30/2017
helpviewer_keywords:
- startup settings schema
- schema startup settings
- configuration schema [.NET Framework], startup settings
ms.assetid: 03de6972-442a-4648-9f3e-efa654e3b949
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 4cdf6a051552ab1effd9c4d9c783297a62602f7a
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47078163"
---
# <a name="startup-settings-schema"></a>スタートアップ設定スキーマ
スタートアップ設定は、アプリケーションを実行する必要のある共通言語ランタイムのバージョンを指定します。  
  
|要素|説明|  
|-------------|-----------------|  
|[\<requiredRuntime>](../../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md)|バージョン 1.0 の共通言語ランタイムのみがアプリケーションでサポートされることを指定します。 ランタイムのバージョン 1.1 でビルドされたアプリケーションは、**\<supportedRuntime >** 要素を使用します。|  
|[\<supportedRuntime>](../../../../../docs/framework/configure-apps/file-schema/startup/supportedruntime-element.md)|アプリケーションでサポートされる共通言語ランタイムのバージョンを指定します。|  
|[\<startup>](../../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)|**\<requiredRuntime>** 要素と **\<supportedRuntime>** 要素を含みます。|  
  
## <a name="see-also"></a>関連項目  
 [構成ファイル スキーマ](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [\<PaveOver> 使用するランタイム バージョンの指定](https://msdn.microsoft.com/library/c376208d-980d-42b4-865b-fbe0d9cc97c2)
