---
title: 自動実装するプロパティ - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- auto-implemented properties [C#]
- properties [C#], auto-implemented
ms.assetid: aa55fa97-ccec-431f-b5e9-5ac789fd32b7
ms.openlocfilehash: ef9243498f3f97e560e45c389932ff57e1e4eef7
ms.sourcegitcommit: deb9225a55485a5a6e6c7914deb30ccfceb69d3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/05/2019
ms.locfileid: "54058517"
---
# <a name="auto-implemented-properties-c-programming-guide"></a><span data-ttu-id="a6d87-102">自動実装するプロパティ (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="a6d87-102">Auto-Implemented Properties (C# Programming Guide)</span></span>
<span data-ttu-id="a6d87-103">C# 3.0 以降では、自動実装プロパティを使用することで、プロパティ アクセサーに追加のロジックが必要ない場合は、プロパティをより簡潔に宣言できます。</span><span class="sxs-lookup"><span data-stu-id="a6d87-103">In C# 3.0 and later, auto-implemented properties make property-declaration more concise when no additional logic is required in the property accessors.</span></span> <span data-ttu-id="a6d87-104">これにより、クライアント コードでオブジェクトを作成することも可能になります。</span><span class="sxs-lookup"><span data-stu-id="a6d87-104">They also enable client code to create objects.</span></span> <span data-ttu-id="a6d87-105">次の例に示すようにプロパティを宣言する場合、コンパイラによって、プロパティの `get` および `set` アクセサーを介してのみアクセスできる、プライベートの匿名バッキング フィールドが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a6d87-105">When you declare a property as shown in the following example, the compiler creates a private, anonymous backing field that can only be accessed through the property's `get` and `set` accessors.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a6d87-106">例</span><span class="sxs-lookup"><span data-stu-id="a6d87-106">Example</span></span>  
 <span data-ttu-id="a6d87-107">次の例に、自動実装プロパティを持つ簡単なクラスを示します。</span><span class="sxs-lookup"><span data-stu-id="a6d87-107">The following example shows a simple class that has some auto-implemented properties:</span></span>  
  
 [!code-csharp[csProgGuideLINQ#28](../../../csharp/programming-guide/arrays/codesnippet/CSharp/auto-implemented-properties_1.cs)]  
  
 <span data-ttu-id="a6d87-108">C# 6 以降では、フィールドと同様に自動実装プロパティを初期化することができます。</span><span class="sxs-lookup"><span data-stu-id="a6d87-108">In C# 6 and later, you can initialize auto-implemented properties similarly to fields:</span></span>  
  
```csharp  
public string FirstName { get; set; } = "Jane";  
```  
  
 <span data-ttu-id="a6d87-109">前の例に示したクラスは、変更可能です。</span><span class="sxs-lookup"><span data-stu-id="a6d87-109">The class that is shown in the previous example is mutable.</span></span> <span data-ttu-id="a6d87-110">クライアント コードは、オブジェクト内の値を作成後に変更できます。</span><span class="sxs-lookup"><span data-stu-id="a6d87-110">Client code can change the values in objects after they are created.</span></span> <span data-ttu-id="a6d87-111">データだけでなく、重要な動作 (メソッド) も含まれる複雑なクラスでは、多くの場合、パブリック プロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="a6d87-111">In complex classes that contain significant behavior (methods) as well as data, it is often necessary to have public properties.</span></span> <span data-ttu-id="a6d87-112">ただし、値 (データ) のセットをカプセル化しているだけで、動作をほとんど、またはまったく含まない小さなクラスや構造体の場合は、set アクセサーを [private](../../../csharp/language-reference/keywords/private.md) (コンシューマーからは変更できない) として宣言するか、または get アクセサー (コンストラクターを除くすべての場所で変更できない) のみを宣言することで、オブジェクトを変更不可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6d87-112">However, for small classes or structs that just encapsulate a set of values (data) and have little or no behaviors, you should either make the objects immutable by declaring the set accessor as [private](../../../csharp/language-reference/keywords/private.md) (immutable to consumers) or by declaring only a get accessor (immutable everywhere except the constructor).</span></span>  <span data-ttu-id="a6d87-113">詳細については、「[方法 :自動実装するプロパティを使用して簡易クラスを実装する](../../../csharp/programming-guide/classes-and-structs/how-to-implement-a-lightweight-class-with-auto-implemented-properties.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a6d87-113">For more information, see [How to: Implement a Lightweight Class with Auto-Implemented Properties](../../../csharp/programming-guide/classes-and-structs/how-to-implement-a-lightweight-class-with-auto-implemented-properties.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6d87-114">「</span><span class="sxs-lookup"><span data-stu-id="a6d87-114">See Also</span></span>

- [<span data-ttu-id="a6d87-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="a6d87-115">Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/properties.md)  
- [<span data-ttu-id="a6d87-116">修飾子</span><span class="sxs-lookup"><span data-stu-id="a6d87-116">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)
