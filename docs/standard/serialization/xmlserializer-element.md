---
title: '&lt;xmlSerializer&gt; 要素'
ms.date: 03/30/2017
helpviewer_keywords:
- <xmlSerializer> element
- XML serialization, configuration
- xmlSerializer element
ms.assetid: d129d10c-3eb7-45d9-8098-5fa853825e47
ms.openlocfilehash: 4b511dc229c9e8321b91fbb0f9395627680e5d12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54591956"
---
# <a name="ltxmlserializergt-element"></a>&lt;xmlSerializer&gt; 要素
<xref:System.Xml.Serialization.XmlSerializer> の進行状況の追加チェックを行うかどうかを指定します。  
  
 \<configuration>  
\<system.xml.serialization>  
  
## <a name="syntax"></a>構文  
  
```xml  
<xmlSerializer checkDeserializerAdvance = "true"|"false" />  
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|**checkDeserializeAdvances**|<xref:System.Xml.Serialization.XmlSerializer> の進行状況をチェックするかどうかを指定します。 属性は "true" または "false" に設定します。 既定値は "true" です。|  
|**useLegacySerializationGeneration**|C# コードをファイルに記述し、それをアセンブリにコンパイルすることによってアセンブリを生成する従来のシリアル化の生成を、<xref:System.Xml.Serialization.XmlSerializer> で使用するかどうかを指定します。 既定値は **false** です。|  
  
### <a name="child-elements"></a>子要素  
 なし。  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<system.xml.serialization> 要素](../../../docs/standard/serialization/system-xml-serialization-element.md)|<xref:System.Xml.Serialization.XmlSerializer> クラスおよび <xref:System.Xml.Serialization.XmlSchemaImporter> クラスの構成設定を含みます。|  
  
## <a name="remarks"></a>Remarks  
 既定では、<xref:System.Xml.Serialization.XmlSerializer> は、信頼できないデータを逆シリアル化する際に、サービス拒否攻撃の可能性に対するセキュリティをさらに高めることができます。 これは、逆シリアル化中に無限ループを検出することにより行われます。 このような条件が検出された場合は、次のメッセージが、例外がスローされます。"内部エラー: 基になるストリーム化セキュリティの強化を逆シリアル化ができませんでした"。  
  
 このメッセージは、必ずしもサービス拒否攻撃を受けていることを示すわけではありません。 まれに、無限ループ検出機構で誤検出が発生し、適正な受信メッセージに対して例外がスローされる場合があります。 特定のアプリケーションにおいて、セキュリティの強化によって適正なメッセージが拒否される場合は、**checkDeserializeAdvances** 属性を "false" に設定します。  
  
## <a name="example"></a>例  
 **checkDeserializeAdvances** 属性を "false" に設定するコード例を次に示します。  
  
```xml  
<configuration>  
  <system.xml.serialization>  
    <xmlSerializer checkDeserializeAdvances="false" />  
  </system.xml.serialization>  
</configuration>  
```  
  
## <a name="see-also"></a>関連項目

- <xref:System.Xml.Serialization.XmlSerializer>
- [\<system.xml.serialization> 要素](../../../docs/standard/serialization/system-xml-serialization-element.md)
- [XML シリアル化および SOAP シリアル化](../../../docs/standard/serialization/xml-and-soap-serialization.md)
