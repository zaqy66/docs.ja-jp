---
title: '&lt;削除&gt;要素&lt;appSettings&gt;'
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/remove
helpviewer_keywords:
- remove Element
- <remove> Element
ms.assetid: 218c4464-e007-4539-803f-7c8b0a909fd8
author: guardrex
ms.author: mairaw
ms.openlocfilehash: e9b79a8319b320289f43adac5a82ef22fa5e32b0
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50199696"
---
# <a name="remove-element-for-appsettings"></a>\<削除 > 要素の\<appSettings >

カスタム アプリケーションの設定を削除します。

[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md)   
&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md)   
&nbsp;&nbsp;&nbsp;&nbsp;**\<削除する >**

## <a name="syntax"></a>構文

```xml
<appSettings>
  <remove key="Key of custom setting" />
</appSettings>
```

### <a name="attribute"></a>属性

|         | 説明 |
| ------- | ----------- |
| **key** | 必須の属性です。<br><br>削除するキーの名前を指定します。 |

### <a name="parent-element"></a>親要素

|     | 説明 |
| --- | ----------- |
| [**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) | ファイル パス、XML Web サービス URL、またはアプリケーションのその他のカスタム構成情報など、カスタム アプリケーションの設定が含まれています。 |

## <a name="child-elements"></a>子要素

なし

## <a name="example"></a>例

次の例のカスタム構成設定を削除する方法を示しています`ApplicationName`:。

```xml
<appSettings>
  <remove key="ApplicationName" />
</appSettings>
```

## <a name="see-also"></a>関連項目

- [.NET Framework の構成ファイル スキーマ](~/docs/framework/configure-apps/file-schema/index.md)
