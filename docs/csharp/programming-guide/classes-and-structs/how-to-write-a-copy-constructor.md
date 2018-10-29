---
title: '方法 : コピー コンストラクターを記述する (C# プログラミング ガイド)'
ms.date: 07/20/2015
helpviewer_keywords:
- C# Language, copy constructor
- copy constructor [C#]
ms.assetid: fba899b5-fc41-428e-a745-3ebdbf37990a
ms.openlocfilehash: d6ecfc3659dcf533db0f4e7b67fdffd620a584fd
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48582334"
---
# <a name="how-to-write-a-copy-constructor-c-programming-guide"></a>方法 : コピー コンストラクターを記述する (C# プログラミング ガイド)
C# では、オブジェクトのコピー コンストラクターが提供されていませんが、独自に作成することができます。  
  
## <a name="example"></a>例  
 次の例の `Person` [クラス](../../../csharp/language-reference/keywords/class.md)では、`Person` のインスタンスを引数として受け取るコピー コンストラクターが定義されています。 引数のプロパティの値は、`Person`の新しいインスタンスのプロパティに割り当てられています。 このコードには、コピーするインスタンスの `Name` プロパティと `Age` プロパティをクラスのインスタンス コンストラクターに渡す代替のコピー コンストラクターが含まれています。  
  
 [!code-csharp[csProgGuideObjects#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-write-a-copy-constructor_1.cs)]  
  
## <a name="see-also"></a>参照

- <xref:System.ICloneable>  
- [C# プログラミングガイド](../../../csharp/programming-guide/index.md)  
- [クラスと構造体](../../../csharp/programming-guide/classes-and-structs/index.md)  
- [コンストラクター](../../../csharp/programming-guide/classes-and-structs/constructors.md)  
- [ファイナライザー](../../../csharp/programming-guide/classes-and-structs/destructors.md)
