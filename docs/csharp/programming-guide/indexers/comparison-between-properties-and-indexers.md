---
title: プロパティとインデクサーの比較 - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- properties [C#], vs. indexers
- indexers [C#], vs. properties
ms.assetid: 3358a89f-44a0-4a4d-bf8c-07237a90af39
ms.openlocfilehash: 053eb7ee0fe9333f049e5b4f8a8e709e42aa2119
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53234462"
---
# <a name="comparison-between-properties-and-indexers-c-programming-guide"></a>プロパティとインデクサーの比較 (C# プログラミング ガイド)
インデクサーはプロパティと似ています。 次の表で示す相違点を除けば、プロパティのアクセサーに対して定義されているすべての規則が、インデクサーのアクセサーにも適用されます。  
  
|プロパティ|インデクサー|  
|--------------|-------------|  
|パブリック データ メンバーのように、メソッドを呼び出せるようにします。|オブジェクト自体で配列表記を使用して、オブジェクトの内部コレクションの要素にアクセスできるようにします。|  
|シンプルな名前でアクセスされます。|インデックスでアクセスされます。|  
|静的メンバーまたはインスタンス メンバーとして使用できます。|インスタンス メンバーである必要があります。|  
|プロパティの [get](../../../csharp/language-reference/keywords/get.md) アクセサーにはパラメーターがありません。|インデクサーの `get` アクセサーには、インデクサーと同じ仮パラメーター リストがあります。|  
|プロパティの [set](../../../csharp/language-reference/keywords/set.md) アクセサーには、暗黙の `value` パラメーターがあります。|インデクサーの `set` アクセサーには、インデクサーと同じ仮パラメーター リストのほか、[value](../../../csharp/language-reference/keywords/value.md) パラメーターがあります。|  
|[自動実装プロパティ](../../../csharp/programming-guide/classes-and-structs/auto-implemented-properties.md)を持つ簡略化された構文がサポートされます。|簡略化された構文がサポートされません。|  
  
## <a name="see-also"></a>参照

- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [インデクサー](../../../csharp/programming-guide/indexers/index.md)  
- [プロパティ](../../../csharp/programming-guide/classes-and-structs/properties.md)
