---
title: '&lt;assemblyBinding&gt;要素&lt;構成&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/assemblyBinding
helpviewer_keywords:
- assemblyBinding Element
- <assemblyBinding> Element
ms.assetid: 6cc55983-b894-449b-8e26-b258e53939cd
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 64985d4ed2c6a82c54a7623df4b13d7ec54bff33
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54599349"
---
# <a name="assemblybinding-element-for-configuration"></a>\<assemblyBinding > 要素の\<構成 >

構成レベルでのアセンブリ バインディング ポリシーを指定します。

[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md)   
&nbsp;&nbsp;**\<assemblyBinding >**

## <a name="syntax"></a>構文

```xml
<assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
  <!-- Configuration files to include. -->
</assemblyBinding>
```

## <a name="attribute"></a>属性

|           | 説明 |
| --------- | ----------- |
| **xmlns** | 必須の属性です。<br><br>アセンブリのバインディングに必要な XML 名前空間を指定します。 値として、文字列 "urn:schemas-microsoft-com:asm.v1" を使用します。 |

## <a name="parent-element"></a>親要素

|     | 説明 |
| --- | ----------- |
| [**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) | 共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。 |

## <a name="child-element"></a>子要素

|     | 説明 |
| --- | ----------- |
| [**\<linkedConfiguration>**](~/docs/framework/configure-apps/file-schema/linkedconfiguration-element.md) | インクルードする構成ファイルを指定します。 |

## <a name="remarks"></a>Remarks

[  **\<LinkedConfiguration >** ](~/docs/framework/configure-apps/file-schema/linkedconfiguration-element.md)要素は、構成ファイルをアプリケーション構成ファイルにアセンブリを含めるようにすることでコンポーネントのアセンブリの管理を簡略化既知の場所ではなく複製アセンブリの構成設定。

> [!NOTE]
>  **\<LinkedConfiguration >** Windows サイド バイ サイドでマニフェストを使用するアプリケーションの要素がサポートされていません。

## <a name="example"></a>例

次の例では、ローカルのハード ディスク上の構成ファイルを含める方法を示します。

```xml
<configuration>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
    <linkedConfiguration href="file://c:\Program Files\Contoso\sharedConfig.xml" />
  </assemblyBinding>
</configuration>
```

## <a name="see-also"></a>関連項目

- [.NET Framework の構成ファイル スキーマ](~/docs/framework/configure-apps/file-schema/index.md)
