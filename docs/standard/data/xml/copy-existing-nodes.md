---
title: 既存のノードのコピー
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 2aa8f65c-cc62-4638-9c46-129dc15be786
author: mairaw
ms.author: mairaw
ms.openlocfilehash: eda5c9b4851b29c0a76e45414d7c47ba52252455
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44252871"
---
# <a name="copy-existing-nodes"></a>既存のノードのコピー
XML ドキュメント オブジェクト モデル (DOM) には、**SelectSingleNode**、**ChildNodes[int i]**、**Attributes[int i]** など、ノードの選択に使用できるメソッドとプロパティが多数用意されています。 ノードを選択すると、その特定のノード型で利用できる挿入メソッドを使用してツリーに挿入できます。 ノードをツリーに挿入するときの唯一の制約は、ノードを挿入した後もドキュメントが整形式になっていなければならないことです。 既存のノードを DOM ツリーに挿入すると、そのノードは元の位置から削除され、挿入先の位置に追加されます。  
  
## <a name="see-also"></a>関連項目

- [XML ドキュメント オブジェクト モデル (DOM)](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
