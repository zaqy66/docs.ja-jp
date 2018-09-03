---
title: '&lt;構成&gt;要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration
helpviewer_keywords:
- <configuration> element
- configuration element
- container tags, <configuration> element
ms.assetid: 2ec1c9dc-2e5c-4ef0-9958-81670ab88449
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: c5146ed8326b12e90d0fe6247b0c4aba3a69dd77
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43485782"
---
# <a name="configuration-element"></a>\<configuration > 要素

共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。

**\<configuration>**

## <a name="syntax"></a>構文

```xml
<configuration>
  <!-- Configuration settings -->
</configuration>
```

## <a name="attributes"></a>属性

なし

## <a name="parent-element"></a>親要素

なし

## <a name="child-elements"></a>子要素

|     | 説明 |
| --- | ----------- |
| [**\<assemblyBinding >**](~/docs/framework/configure-apps/file-schema/assemblybinding-element-for-configuration.md) | 構成レベルでのアセンブリ バインディング ポリシーを指定します。|
| [**\<スタートアップ >** 設定スキーマ](~/docs/framework/configure-apps/file-schema/startup/index.md) | スタートアップ設定スキーマのすべての要素。 |
| [**\<ランタイム >** 設定スキーマ](~/docs/framework/configure-apps/file-schema/runtime/index.md) | ランタイム設定スキーマのすべての要素。 |
| [**\<system.runtime.remoting >** 設定スキーマ](https://msdn.microsoft.com/dc2d1e62-9af7-4ca1-99fd-98b93bb4db9e) | リモート処理設定スキーマのすべての要素。 |
| [**\<system.Net >** 設定スキーマ](~/docs/framework/configure-apps/file-schema/network/index.md) | ネットワーク設定スキーマのすべての要素。 |
| [**\<cryptographySettings >** 設定スキーマ](~/docs/framework/configure-apps/file-schema/cryptography/index.md) | 暗号設定スキーマのすべての要素。 |
| [**\<configuration >** セクション スキーマ](~/docs/framework/configure-apps/file-schema/configuration-sections-schema.md) | 構成セクションの設定のスキーマのすべての要素。 |
| [トレースおよびデバッグ設定のスキーマ](~/docs/framework/configure-apps/file-schema/trace-debug/index.md) | トレースとデバッグの設定のスキーマのすべての要素。 |
| [ASP.NET 構成設定のスキーマ](https://msdn.microsoft.com/library/b5ysx397(v=vs.100).aspx) | ASP.NET Web サイトおよびアプリケーションを構成するための要素を含む、ASP.NET 構成スキーマのすべての要素。 使用される*Web.config*ファイル。 |
| [**\<webServices >** 設定スキーマ](https://msdn.microsoft.com/f84d6d55-1add-4eb7-ae46-33df5833ea2e) | Web サービス設定スキーマのすべての要素。 |
| [Web 設定スキーマ](~/docs/framework/configure-apps/file-schema/web/index.md) | IIS などのホスト アプリケーションと ASP.NET の連携を構成する要素も含め、Web 設定スキーマのすべての要素。 使用される*aspnet.config*ファイル。 |

## <a name="remarks"></a>Remarks

各構成ファイルには、1 つだけ含める必要があります**\<構成 >** 要素。

## <a name="see-also"></a>関連項目

[.NET Framework の構成ファイル スキーマ](~/docs/framework/configure-apps/file-schema/index.md)
