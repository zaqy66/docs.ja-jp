---
title: DOM のノード コンテンツの削除
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 615d81a7-f44f-416c-a9ab-bfe03f85e6e4
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 737766586ee920a87c25dd42896bdfb14ae69d98
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44205219"
---
# <a name="removing-node-content-in-the-dom"></a>DOM のノード コンテンツの削除
<xref:System.Xml.XmlCharacterData> を継承するノード型、つまり <xref:System.Xml.XmlComment>、<xref:System.Xml.XmlText>、<xref:System.Xml.XmlCDataSection>、<xref:System.Xml.XmlWhitespace>、および <xref:System.Xml.XmlSignificantWhitespace> ノード型では、ノードから文字範囲を削除する <xref:System.Xml.XmlCharacterData.DeleteData%2A> メソッドを使用して文字を削除できます。 コンテンツを完全に削除するには、そのコンテンツが含まれているノードを削除します。 ノードを保持する必要があり、コンテンツが正しくない場合は、そのコンテンツを変更します。 ノードのコンテンツを変更する方法については、「[XML ドキュメントのノード、コンテンツ、値の変更](../../../../docs/standard/data/xml/modifying-nodes-content-and-values-in-an-xml-document.md)」を参照してください。  
  
## <a name="see-also"></a>関連項目

- [XML ドキュメント オブジェクト モデル (DOM)](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
