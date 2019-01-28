---
title: class キーワード - C# リファレンス
ms.custom: seodec18
ms.date: 07/18/2017
f1_keywords:
- class_CSharpKeyword
- class
helpviewer_keywords:
- class keyword [C#]
ms.assetid: b95d8815-de18-4c3f-a8cc-a0a53bdf8690
ms.openlocfilehash: 83e7d278b38e17dac668b32687a368211399d437
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54652073"
---
# <a name="class-c-reference"></a><span data-ttu-id="be498-102">class (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="be498-102">class (C# Reference)</span></span>

<span data-ttu-id="be498-103">クラスは、次の例に示すように、キーワード `class` を使用して宣言します。</span><span class="sxs-lookup"><span data-stu-id="be498-103">Classes are declared using the keyword `class`, as shown in the following example:</span></span>

```csharp
class TestClass
{
    // Methods, properties, fields, events, delegates
    // and nested classes go here.
}
```

## <a name="remarks"></a><span data-ttu-id="be498-104">コメント</span><span class="sxs-lookup"><span data-stu-id="be498-104">Remarks</span></span>

<span data-ttu-id="be498-105">C# では、単一継承のみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="be498-105">Only single inheritance is allowed in C#.</span></span> <span data-ttu-id="be498-106">つまり、クラスは 1 つの基底クラスの実装だけを継承できます。</span><span class="sxs-lookup"><span data-stu-id="be498-106">In other words, a class can inherit implementation from one base class only.</span></span> <span data-ttu-id="be498-107">ただし、クラスは複数のインターフェイスを実装できます。</span><span class="sxs-lookup"><span data-stu-id="be498-107">However, a class can implement more than one interface.</span></span> <span data-ttu-id="be498-108">クラスの継承とインターフェイスの実装の例を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="be498-108">The following table shows examples of class inheritance and interface implementation:</span></span>

|<span data-ttu-id="be498-109">継承</span><span class="sxs-lookup"><span data-stu-id="be498-109">Inheritance</span></span>|<span data-ttu-id="be498-110">例</span><span class="sxs-lookup"><span data-stu-id="be498-110">Example</span></span>|
|-----------------|-------------|
|<span data-ttu-id="be498-111">なし</span><span class="sxs-lookup"><span data-stu-id="be498-111">None</span></span>|`class ClassA { }`|
|<span data-ttu-id="be498-112">Single</span><span class="sxs-lookup"><span data-stu-id="be498-112">Single</span></span>|`class DerivedClass: BaseClass { }`|
|<span data-ttu-id="be498-113">なし。2 つのインターフェイスを実装</span><span class="sxs-lookup"><span data-stu-id="be498-113">None, implements two interfaces</span></span>|`class ImplClass: IFace1, IFace2 { }`|
|<span data-ttu-id="be498-114">1 つ。1 つのインターフェイスを実装</span><span class="sxs-lookup"><span data-stu-id="be498-114">Single, implements one interface</span></span>|`class ImplDerivedClass: BaseClass, IFace1 { }`|

<span data-ttu-id="be498-115">名前空間内で直接宣言され、他のクラスに入れ子にされていないクラスは、[public](../../../csharp/language-reference/keywords/public.md) または [internal](../../../csharp/language-reference/keywords/internal.md) のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="be498-115">Classes that you declare directly within a namespace, not nested within other classes, can be either [public](../../../csharp/language-reference/keywords/public.md) or [internal](../../../csharp/language-reference/keywords/internal.md).</span></span> <span data-ttu-id="be498-116">クラスは既定で `internal` です。</span><span class="sxs-lookup"><span data-stu-id="be498-116">Classes are `internal` by default.</span></span>

<span data-ttu-id="be498-117">クラスのメンバー (入れ子にされているクラスを含む) は [public](public.md)、[protected internal](protected-internal.md)、[protected](protected.md)、[internal](internal.md)、[private](private.md)、または [private protected](private-protected.md) のいずれかとして宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="be498-117">Class members, including nested classes, can be [public](public.md), [protected internal](protected-internal.md), [protected](protected.md), [internal](internal.md), [private](private.md), or [private protected](private-protected.md).</span></span> <span data-ttu-id="be498-118">メンバーは既定で `private` です。</span><span class="sxs-lookup"><span data-stu-id="be498-118">Members are `private` by default.</span></span>

<span data-ttu-id="be498-119">詳細については、「[アクセス修飾子](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be498-119">For more information, see [Access Modifiers](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).</span></span>

<span data-ttu-id="be498-120">型パラメーターを持つジェネリック クラスを宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="be498-120">You can declare generic classes that have type parameters.</span></span> <span data-ttu-id="be498-121">詳細については、「[ジェネリック クラス](../../../csharp/programming-guide/generics/generic-classes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be498-121">For more information, see [Generic Classes](../../../csharp/programming-guide/generics/generic-classes.md).</span></span>

<span data-ttu-id="be498-122">クラスには、次のメンバーの宣言を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="be498-122">A class can contain declarations of the following members:</span></span>

- [<span data-ttu-id="be498-123">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="be498-123">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)

- [<span data-ttu-id="be498-124">定数</span><span class="sxs-lookup"><span data-stu-id="be498-124">Constants</span></span>](../../../csharp/programming-guide/classes-and-structs/constants.md)

- [<span data-ttu-id="be498-125">フィールド</span><span class="sxs-lookup"><span data-stu-id="be498-125">Fields</span></span>](../../../csharp/programming-guide/classes-and-structs/fields.md)

- [<span data-ttu-id="be498-126">ファイナライザー</span><span class="sxs-lookup"><span data-stu-id="be498-126">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)

- [<span data-ttu-id="be498-127">メソッド</span><span class="sxs-lookup"><span data-stu-id="be498-127">Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/methods.md)

- [<span data-ttu-id="be498-128">プロパティ</span><span class="sxs-lookup"><span data-stu-id="be498-128">Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/properties.md)

- [<span data-ttu-id="be498-129">インデクサー</span><span class="sxs-lookup"><span data-stu-id="be498-129">Indexers</span></span>](../../../csharp/programming-guide/indexers/index.md)

- [<span data-ttu-id="be498-130">演算子</span><span class="sxs-lookup"><span data-stu-id="be498-130">Operators</span></span>](../../../csharp/programming-guide/statements-expressions-operators/operators.md)

- [<span data-ttu-id="be498-131">イベント</span><span class="sxs-lookup"><span data-stu-id="be498-131">Events</span></span>](../../../csharp/programming-guide/events/index.md)

- [<span data-ttu-id="be498-132">デリゲート</span><span class="sxs-lookup"><span data-stu-id="be498-132">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)

- [<span data-ttu-id="be498-133">クラス</span><span class="sxs-lookup"><span data-stu-id="be498-133">Classes</span></span>](../../../csharp/programming-guide/classes-and-structs/classes.md)

- [<span data-ttu-id="be498-134">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="be498-134">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)

- [<span data-ttu-id="be498-135">構造体</span><span class="sxs-lookup"><span data-stu-id="be498-135">Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/structs.md)

- [<span data-ttu-id="be498-136">列挙型</span><span class="sxs-lookup"><span data-stu-id="be498-136">Enumerations</span></span>](../../../csharp/programming-guide/enumeration-types.md)

## <a name="example"></a><span data-ttu-id="be498-137">例</span><span class="sxs-lookup"><span data-stu-id="be498-137">Example</span></span>

<span data-ttu-id="be498-138">ここでは、クラスのフィールド、コンストラクター、メソッドの宣言例を示します。</span><span class="sxs-lookup"><span data-stu-id="be498-138">The following example demonstrates declaring class fields, constructors, and methods.</span></span> <span data-ttu-id="be498-139">また、オブジェクト インスタンスの作成とインスタンス データの出力の例も示します。</span><span class="sxs-lookup"><span data-stu-id="be498-139">It also demonstrates object instantiation and printing instance data.</span></span> <span data-ttu-id="be498-140">次の例では、2 つのクラスが宣言されています。</span><span class="sxs-lookup"><span data-stu-id="be498-140">In this example, two classes are declared.</span></span> <span data-ttu-id="be498-141">最初の `Child` クラスには、2 つのプライベート フィールド (`name` と `age`)、2 つのパブリック コンストラクター、および 1 つのパブリック メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="be498-141">The first class, `Child`, contains two private fields (`name` and `age`), two public constructors and one public method.</span></span> <span data-ttu-id="be498-142">2 番目のクラスである `StringTest` は、`Main`の格納に使用されます。</span><span class="sxs-lookup"><span data-stu-id="be498-142">The second class, `StringTest`, is used to contain `Main`.</span></span>

[!code-csharp[csrefKeywordsTypes#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#5)]

## <a name="comments"></a><span data-ttu-id="be498-143">コメント</span><span class="sxs-lookup"><span data-stu-id="be498-143">Comments</span></span>

<span data-ttu-id="be498-144">前の例で、プライベート フィールド (`name` および `age`) にアクセスできるのは、`Child` クラスのパブリック メソッドだけであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="be498-144">Notice that in the previous example the private fields (`name` and `age`) can only be accessed through the public method of the `Child` class.</span></span> <span data-ttu-id="be498-145">たとえば、次のステートメントを使用して `Main` メソッドから子の名前を印刷することはできません。</span><span class="sxs-lookup"><span data-stu-id="be498-145">For example, you cannot print the child's name, from the `Main` method, using a statement like this:</span></span>

```csharp
Console.Write(child1.name);   // Error
```

<span data-ttu-id="be498-146">`Main` から `Child`のプライベート メンバーへのアクセスは、`Main` がそのクラスのメンバーである場合にのみ可能です。</span><span class="sxs-lookup"><span data-stu-id="be498-146">Accessing private members of `Child` from `Main` would only be possible if `Main` were a member of the class.</span></span>

<span data-ttu-id="be498-147">アクセス修飾子を指定せずにクラス内で宣言された型は既定で `private` になります。そのため、キーワードが削除されてもこの例のデータ メンバーは `private` です。</span><span class="sxs-lookup"><span data-stu-id="be498-147">Types declared inside a class without an access modifier default to `private`, so the data members in this example would still be `private` if the keyword were removed.</span></span>

<span data-ttu-id="be498-148">最後に、既定のコンストラクターを使って作成したオブジェクト (`child3`) の `age` フィールドが、既定で 0 に初期化されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="be498-148">Finally, notice that for the object created using the default constructor (`child3`), the `age` field was initialized to zero by default.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="be498-149">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="be498-149">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="be498-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="be498-150">See also</span></span>

- [<span data-ttu-id="be498-151">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="be498-151">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="be498-152">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="be498-152">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="be498-153">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="be498-153">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
- [<span data-ttu-id="be498-154">参照型</span><span class="sxs-lookup"><span data-stu-id="be498-154">Reference Types</span></span>](../../../csharp/language-reference/keywords/reference-types.md)
