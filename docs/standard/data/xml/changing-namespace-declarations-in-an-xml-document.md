---
title: XML ドキュメントの名前空間宣言の変更
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
ms.assetid: a2758f40-e497-4964-8d8d-1bb68af14dcd
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4a6b80a885f43facf4b3d4dd1dcb56d937d4f8de
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44188801"
---
# <a name="changing-namespace-declarations-in-an-xml-document"></a>XML ドキュメントの名前空間宣言の変更
**XmlDocument** は、名前空間宣言と **xmlns** 属性をドキュメント オブジェクト モデルの一部として公開します。 名前空間宣言と xmlns 属性は **XmlDocument** に格納されるため、ドキュメントの保存時にはこれらの属性の場所を保持できます。 これらの属性を変更しても、ツリーに既に存在する別のノードの **Name**、**NamespaceURI**、**Prefix** プロパティは影響を受けません。 たとえば、次のドキュメントを読み込むと、`test` 要素の **NamespaceURI** は `123.` になります。  
  
```xml  
<test xmlns="123"/>  
```  
  
 その後、次のように `xmlns` 要素を削除しても、`test` 要素の **NamespaceURI** は `123` のまま変わりません。  
  
```vb  
doc.documentElement.RemoveAttribute("xmlns")  
```  
  
```csharp  
doc.documentElement.RemoveAttribute("xmlns");  
```  
  
 同様に、次のように別の `xmlns` 属性を `doc` 要素に追加しても、`test` 要素の **NamespaceURI** は `123` のまま変わりません。  
  
```vb  
doc.documentElement.SetAttribute("xmlns","456");  
```  
  
```csharp  
doc.documentElement.SetAttribute("xmlns","456");  
```  
  
 つまり、`xmlns` 属性を変更しても、**XmlDocument** オブジェクトを保存して再び読み込むまで、プロパティは影響を受けません。  
  
## <a name="see-also"></a>関連項目

- [XML ドキュメント オブジェクト モデル (DOM)](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
