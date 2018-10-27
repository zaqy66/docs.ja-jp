---
title: '&lt;オフ&gt;要素&lt;appSettings&gt;'
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/clear
helpviewer_keywords:
- clear Element
- <clear> Element
ms.assetid: 6d18c7be-27db-438b-8fb5-765d396b0b7b
author: guardrex
ms.author: mairaw
ms.openlocfilehash: bc52e3149c213925ea64a8421ee65befeea4161e
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50184219"
---
# <a name="clear-element-for-appsettings"></a>\<クリア > 要素の\<appSettings >

カスタム アプリケーションの設定をクリアします。

[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md)   
&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md)   
&nbsp;&nbsp;&nbsp;&nbsp;**\<クリア >**

## <a name="syntax"></a>構文

```xml
<appSettings>
  <clear />
</appSettings>
```

## <a name="attributes"></a>属性

なし

## <a name="parent-element"></a>親要素

|     | 説明 |
| --- | ----------- |
| [**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) | ファイル パス、XML Web サービスの Url、またはその他のカスタム アプリケーションの構成情報など、カスタム アプリケーション設定が含まれています。 |

## <a name="child-elements"></a>子要素

なし

## <a name="example"></a>例

次の例では、カスタム構成設定をクリアする方法を示します。

```xml
<appSettings>
  <clear />
</appSettings>
```

## <a name="see-also"></a>関連項目

- [.NET Framework の構成ファイル スキーマ](~/docs/framework/configure-apps/file-schema/index.md)
