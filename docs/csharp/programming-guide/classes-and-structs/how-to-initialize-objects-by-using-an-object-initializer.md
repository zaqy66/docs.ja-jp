---
title: '方法: オブジェクト初期化子を使用してオブジェクトを初期化する - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 12/20/2018
helpviewer_keywords:
- object initializers [C#], how to use
- objects [C#], initializing
ms.assetid: 4b75ebb2-2e29-43de-929c-d736a8f27ce6
ms.openlocfilehash: 29987b9ba1f1f18f4e768766bd2391ebb5862f97
ms.sourcegitcommit: d09c77414e9e4fc72c79b04deee7a756a120674e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/08/2019
ms.locfileid: "54084876"
---
# <a name="how-to-initialize-objects-by-using-an-object-initializer-c-programming-guide"></a>方法: オブジェクト初期化子を使用してオブジェクトを初期化する (C# プログラミング ガイド)

オブジェクト初期化子を使用すると、型のコンストラクターを明示的に呼び出さずに、宣言的な方法で型オブジェクトを初期化できます。  
  
次の例は、指定したオブジェクトでオブジェクト初期化子を使用する方法を示しています。 コンパイラは、最初に既定のインスタンス コンストラクターにアクセスし、メンバーの初期化を処理することで、オブジェクト初期化子を処理します。 そのため、クラスで既定のコンストラクターが `private` として宣言されている場合、パブリック アクセスを必要とするオブジェクト初期化子は失敗します。
  
匿名型を定義する場合は、オブジェクト初期化子を使用する必要があります。 詳細については、「[方法 :クエリで要素のプロパティのサブセットを返す](how-to-return-subsets-of-element-properties-in-a-query.md)」をご覧ください。  
  
## <a name="example"></a>例  

次の例は、オブジェクト初期化子を使用して、新しい `StudentName` 型を初期化する方法を示しています。 この例では `StudentName` 型でプロパティが設定されます。
  
[!code-csharp-interactive[InitializerObjectExample](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/object-collection-initializers/HowToObjectInitializers.cs#HowToObjectInitializers)]  

オブジェクト初期化子を使用し、オブジェクトにインデクサーを設定できます。 次の例では、インデクサーを使用する `BaseballTeam` クラスを定義し、選手を取得し、さまざまなポジションに据えます。 初期化子によって、ポジションの省略形 (野球のスコアカードに使用される各ポジションの番号) に基づき、選手を割り当てることができます。

[!code-csharp-interactive[InitializerIndexerExample](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/object-collection-initializers/HowToIndexInitializer.cs#HowToIndexInitializer)]  

## <a name="see-also"></a>「

- [C# プログラミング ガイド](../index.md)  
- [オブジェクト初期化子とコレクション初期化子](object-and-collection-initializers.md)
