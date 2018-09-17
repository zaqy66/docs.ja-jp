---
title: '方法 : コピー コンストラクターを記述する (C# プログラミング ガイド)'
ms.date: 07/20/2015
helpviewer_keywords:
- C# Language, copy constructor
- copy constructor [C#]
ms.assetid: fba899b5-fc41-428e-a745-3ebdbf37990a
ms.openlocfilehash: d6ecfc3659dcf533db0f4e7b67fdffd620a584fd
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2018
ms.locfileid: "45638111"
---
# <a name="how-to-write-a-copy-constructor-c-programming-guide"></a><span data-ttu-id="65072-102">方法 : コピー コンストラクターを記述する (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="65072-102">How to: Write a Copy Constructor (C# Programming Guide)</span></span>
<span data-ttu-id="65072-103">C# では、オブジェクトのコピー コンストラクターが提供されていませんが、独自に作成することができます。</span><span class="sxs-lookup"><span data-stu-id="65072-103">C# doesn't provide a copy constructor for objects, but you can write one yourself.</span></span>  
  
## <a name="example"></a><span data-ttu-id="65072-104">例</span><span class="sxs-lookup"><span data-stu-id="65072-104">Example</span></span>  
 <span data-ttu-id="65072-105">次の例の `Person` [クラス](../../../csharp/language-reference/keywords/class.md)では、`Person` のインスタンスを引数として受け取るコピー コンストラクターが定義されています。</span><span class="sxs-lookup"><span data-stu-id="65072-105">In the following example, the `Person`[class](../../../csharp/language-reference/keywords/class.md) defines a copy constructor that takes, as its argument, an instance of `Person`.</span></span> <span data-ttu-id="65072-106">引数のプロパティの値は、`Person`の新しいインスタンスのプロパティに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="65072-106">The values of the properties of the argument are assigned to the properties of the new instance of `Person`.</span></span> <span data-ttu-id="65072-107">このコードには、コピーするインスタンスの `Name` プロパティと `Age` プロパティをクラスのインスタンス コンストラクターに渡す代替のコピー コンストラクターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="65072-107">The code contains an alternative copy constructor that sends the `Name` and `Age` properties of the instance that you want to copy to the instance constructor of the class.</span></span>  
  
 [!code-csharp[csProgGuideObjects#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-write-a-copy-constructor_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="65072-108">参照</span><span class="sxs-lookup"><span data-stu-id="65072-108">See Also</span></span>

- <xref:System.ICloneable>  
- [<span data-ttu-id="65072-109">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="65072-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="65072-110">クラスと構造体</span><span class="sxs-lookup"><span data-stu-id="65072-110">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)  
- [<span data-ttu-id="65072-111">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="65072-111">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)  
- [<span data-ttu-id="65072-112">ファイナライザー</span><span class="sxs-lookup"><span data-stu-id="65072-112">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)
