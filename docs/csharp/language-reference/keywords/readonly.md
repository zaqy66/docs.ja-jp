---
title: readonly キーワード (C# リファレンス)
ms.date: 06/21/2018
f1_keywords:
- readonly_CSharpKeyword
- readonly
helpviewer_keywords:
- readonly keyword [C#]
ms.assetid: 2f8081f6-0de2-4903-898d-99696c48d2f4
ms.openlocfilehash: b50d3b571afb3128c973baaf7d7178da705382bd
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53146171"
---
# <a name="readonly-c-reference"></a><span data-ttu-id="fcb58-102">readonly (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="fcb58-102">readonly (C# Reference)</span></span>

<span data-ttu-id="fcb58-103">`readonly` キーワードは、3 つのコンテキストで使用できる修飾子です。</span><span class="sxs-lookup"><span data-stu-id="fcb58-103">The `readonly` keyword is a modifier that can be used in three contexts:</span></span>

- <span data-ttu-id="fcb58-104">[フィールドの宣言](#readonly-field-example)では、`readonly` は、フィールドへの割り当てが、宣言の一部として、または同じクラスのコンストラクター内でのみ可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="fcb58-104">In a [field declaration](#readonly-field-example), `readonly` indicates that assignment to the field can only occur as part of the declaration or in a constructor in the same class.</span></span>
- <span data-ttu-id="fcb58-105">[`readonly struct` の定義](#readonly-struct-example)では、`readonly` は `struct` が変更不可であることを示します。</span><span class="sxs-lookup"><span data-stu-id="fcb58-105">In a [`readonly struct` definition](#readonly-struct-example), `readonly` indicates that the `struct` is immutable.</span></span>
- <span data-ttu-id="fcb58-106">[`ref readonly` メソッドの戻り値](#ref-readonly-return-example)では、`readonly` 修飾子は、メソッドが参照を返し、その参照への書き込みが許可されないことを示します。</span><span class="sxs-lookup"><span data-stu-id="fcb58-106">In a [`ref readonly` method return](#ref-readonly-return-example), the `readonly` modifier indicates that method returns a reference and writes are not allowed to that reference.</span></span>

<span data-ttu-id="fcb58-107">最後の 2 つのコンテキストは、C# 7.2 で追加されました。</span><span class="sxs-lookup"><span data-stu-id="fcb58-107">The final two contexts were added in C# 7.2.</span></span>

## <a name="readonly-field-example"></a><span data-ttu-id="fcb58-108">読み取り専用フィールドの例</span><span class="sxs-lookup"><span data-stu-id="fcb58-108">Readonly field example</span></span>

<span data-ttu-id="fcb58-109">この例では、`year` フィールドの値は、クラス コンストラクターで値が割り当てられていても `ChangeYear` メソッドでは変更できません。</span><span class="sxs-lookup"><span data-stu-id="fcb58-109">In this example, the value of the field `year` cannot be changed in the method `ChangeYear`, even though it is assigned a value in the class constructor:</span></span>

[!code-csharp[Readonly Field example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#ReadonlyField)]

<span data-ttu-id="fcb58-110">`readonly` のフィールドに値を割り当てることができるのは、次のコンテキスト内に限られます。</span><span class="sxs-lookup"><span data-stu-id="fcb58-110">You can assign a value to a `readonly` field only in the following contexts:</span></span>

- <span data-ttu-id="fcb58-111">値が宣言で初期化される場合。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="fcb58-111">When the variable is initialized in the declaration, for example:</span></span>

```csharp
public readonly int y = 5;
```

- <span data-ttu-id="fcb58-112">インスタンス フィールド宣言を含むクラスのインスタンス コンストラクター内。</span><span class="sxs-lookup"><span data-stu-id="fcb58-112">In an instance constructor of the class that contains the instance field declaration.</span></span>
- <span data-ttu-id="fcb58-113">静的フィールド宣言を含むクラスの静的コンストラクター内。</span><span class="sxs-lookup"><span data-stu-id="fcb58-113">In the static constructor of the class that contains the static field declaration.</span></span>

<span data-ttu-id="fcb58-114">また、これらのコンストラクター コンテキスト内でのみ、`readonly` フィールドを [out](out-parameter-modifier.md) パラメーターまたは [ref](ref.md) パラメーターとして渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="fcb58-114">These constructor contexts are also the only contexts in which it is valid to pass a `readonly` field as an [out](out-parameter-modifier.md) or [ref](ref.md) parameter.</span></span>

> [!NOTE]
> <span data-ttu-id="fcb58-115">`readonly` キーワードは [const](const.md) キーワードとは異なります。</span><span class="sxs-lookup"><span data-stu-id="fcb58-115">The `readonly` keyword is different from the [const](const.md) keyword.</span></span> <span data-ttu-id="fcb58-116">`const` フィールドは、フィールドの宣言でしか初期化できません。</span><span class="sxs-lookup"><span data-stu-id="fcb58-116">A `const` field can only be initialized at the declaration of the field.</span></span> <span data-ttu-id="fcb58-117">`readonly` フィールドは、フィールドの宣言と任意のコンストラクターで複数回割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="fcb58-117">A `readonly` field can be assigned multiple times either in the field declaration or in any constructor.</span></span> <span data-ttu-id="fcb58-118">このため、`readonly` フィールドは、使用するコンストラクターに応じて異なる値を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="fcb58-118">Therefore, `readonly` fields can have different values depending on the constructor used.</span></span> <span data-ttu-id="fcb58-119">また、次の例のように、`const` フィールドがコンパイル時定数であるのに対し、`readonly` フィールドは実行時定数として使用できます。</span><span class="sxs-lookup"><span data-stu-id="fcb58-119">Also, while a `const` field is a compile-time constant, the `readonly` field can be used for runtime constants as in the following example:</span></span>

```csharp
public static readonly uint timeStamp = (uint)DateTime.Now.Ticks;
```

[!code-csharp[Initialize readonly Field example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#InitReadonlyField)]

<span data-ttu-id="fcb58-120">上の例で、次の例のようなステートメントを使うものとします。</span><span class="sxs-lookup"><span data-stu-id="fcb58-120">In the preceding example, if you use a statement like the following example:</span></span>

`p2.y = 66;        // Error`

<span data-ttu-id="fcb58-121">この場合、次のコンパイル エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fcb58-121">you will get the compiler error message:</span></span>

`A readonly field cannot be assigned to (except in a constructor or a variable initializer)`

## <a name="readonly-struct-example"></a><span data-ttu-id="fcb58-122">読み取り専用の構造体の例</span><span class="sxs-lookup"><span data-stu-id="fcb58-122">Readonly struct example</span></span>

<span data-ttu-id="fcb58-123">`struct` 定義での `readonly` 修飾子は、構造体が**変更不可**であることを宣言します。</span><span class="sxs-lookup"><span data-stu-id="fcb58-123">The `readonly` modifier on a `struct` definition declares that the struct is **immutable**.</span></span> <span data-ttu-id="fcb58-124">次の例のように、`struct` のすべてのインスタンス フィールドを `readonly` とマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcb58-124">Every instance field of the `struct` must be marked `readonly`, as shown in the following example:</span></span>

[!code-csharp[readonly struct example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#ReadonlyStruct)]

<span data-ttu-id="fcb58-125">前の例では、[読み取り専用の自動プロパティ](../../properties.md#read-only)を使ってその記憶域を宣言しています。</span><span class="sxs-lookup"><span data-stu-id="fcb58-125">The preceding example uses [readonly auto properties](../../properties.md#read-only) to declare its storage.</span></span> <span data-ttu-id="fcb58-126">これは、これらのプロパティに対して `readonly` バッキング フィールドを作成するようコンパイラに指示します。</span><span class="sxs-lookup"><span data-stu-id="fcb58-126">That instructs the compiler to create `readonly` backing fields for those properties.</span></span> <span data-ttu-id="fcb58-127">`readonly` フィールドを直接宣言することもできます。</span><span class="sxs-lookup"><span data-stu-id="fcb58-127">You could also declare `readonly` fields directly:</span></span>

```csharp
public readonly struct Point
{
    public readonly double X;
    public readonly double Y;

    public Point(double x, double y) => (X, Y) = (x, y);

    public override string ToString() => $"({X}, {Y})";
}
```

<span data-ttu-id="fcb58-128">`readonly` に指定されていないフィールドを追加すると、コンパイラ エラー `CS8340`: "読み取り専用の構造体のインスタンス フィールドは、読み取り専用である必要があります" が生成されます。</span><span class="sxs-lookup"><span data-stu-id="fcb58-128">Adding a field not marked `readonly` generates compiler error `CS8340`: "Instance fields of readonly structs must be readonly."</span></span>

## <a name="ref-readonly-return-example"></a><span data-ttu-id="fcb58-129">ref readonly の戻り値の例</span><span class="sxs-lookup"><span data-stu-id="fcb58-129">Ref readonly return example</span></span>

<span data-ttu-id="fcb58-130">`ref return` での `readonly` 修飾子は、返される参照を変更できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="fcb58-130">The `readonly` modifier on a `ref return` indicates that the returned reference cannot be modified.</span></span> <span data-ttu-id="fcb58-131">次の例は、origin に参照を返します。</span><span class="sxs-lookup"><span data-stu-id="fcb58-131">The following example returns a reference to the origin.</span></span> <span data-ttu-id="fcb58-132">`readonly` 修飾子を使用して、呼び出し元が origin を変更できないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="fcb58-132">It uses the `readonly` modifier to indicate that callers cannot modify the origin:</span></span>

[!code-csharp[readonly struct example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#ReadonlyReturn)]
<span data-ttu-id="fcb58-133">返される型を `readonly struct` にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fcb58-133">The type returned doesn't need to be a `readonly struct`.</span></span> <span data-ttu-id="fcb58-134">`ref` で返すことができる任意の型を、`ref readonly` で返すことができます。</span><span class="sxs-lookup"><span data-stu-id="fcb58-134">Any type that can be returned by `ref` can be returned by `ref readonly`</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="fcb58-135">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="fcb58-135">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="fcb58-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="fcb58-136">See also</span></span>

- [<span data-ttu-id="fcb58-137">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="fcb58-137">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="fcb58-138">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="fcb58-138">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="fcb58-139">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="fcb58-139">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="fcb58-140">修飾子</span><span class="sxs-lookup"><span data-stu-id="fcb58-140">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="fcb58-141">const</span><span class="sxs-lookup"><span data-stu-id="fcb58-141">const</span></span>](const.md)
- [<span data-ttu-id="fcb58-142">フィールド</span><span class="sxs-lookup"><span data-stu-id="fcb58-142">Fields</span></span>](../../programming-guide/classes-and-structs/fields.md)
