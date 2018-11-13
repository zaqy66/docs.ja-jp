---
title: F# の関数型プログラミングの概要
description: 関数型プログラミングの基礎を学習F#します。
ms.date: 10/29/2018
ms.openlocfilehash: d4a9bb0cd826b41aca96e12e2bcb5aab80c18eb4
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25724479"
---
# <a name="introduction-to-functional-programming-in-f"></a><span data-ttu-id="858e8-103">F# の関数型プログラミングの概要</span><span class="sxs-lookup"><span data-stu-id="858e8-103">Introduction to Functional Programming in F#</span></span> #

<span data-ttu-id="858e8-104">関数型プログラミングは、機能と変更不可のデータの使用を重視するプログラミングのスタイルです。</span><span class="sxs-lookup"><span data-stu-id="858e8-104">Functional programming is a style of programming that emphasizes the use of functions and immutable data.</span></span> <span data-ttu-id="858e8-105">型指定された関数型プログラミングは関数型プログラミングと組み合わせると静的な型などとF#します。</span><span class="sxs-lookup"><span data-stu-id="858e8-105">Typed functional programming is when functional programming is combined with static types, such as with F#.</span></span> <span data-ttu-id="858e8-106">一般に、次の概念が関数型プログラミングで強調表示します。</span><span class="sxs-lookup"><span data-stu-id="858e8-106">In general, the following concepts are emphasized in functional programming:</span></span>

* <span data-ttu-id="858e8-107">使用する基本的な構造と機能</span><span class="sxs-lookup"><span data-stu-id="858e8-107">Functions as the primary constructs you use</span></span>
* <span data-ttu-id="858e8-108">ステートメントではなく式</span><span class="sxs-lookup"><span data-stu-id="858e8-108">Expressions instead of statements</span></span>
* <span data-ttu-id="858e8-109">変数に値を変更できません。</span><span class="sxs-lookup"><span data-stu-id="858e8-109">Immutable values over variables</span></span>
* <span data-ttu-id="858e8-110">宣言型のプログラミング命令型プログラミングの概要</span><span class="sxs-lookup"><span data-stu-id="858e8-110">Declarative programming over imperative programming</span></span>

<span data-ttu-id="858e8-111">この連載では、概念、および関数型プログラミングを使用してパターンをについて説明しますF#します。</span><span class="sxs-lookup"><span data-stu-id="858e8-111">Throughout this series, you'll explore concepts and patterns in functional programming using F#.</span></span> <span data-ttu-id="858e8-112">その過程でいくつか説明しますF#すぎます。</span><span class="sxs-lookup"><span data-stu-id="858e8-112">Along the way, you'll learn some F# too.</span></span>

## <a name="terminology"></a><span data-ttu-id="858e8-113">用語</span><span class="sxs-lookup"><span data-stu-id="858e8-113">Terminology</span></span>

<span data-ttu-id="858e8-114">その他のプログラミング パラダイムのように、関数型プログラミングを学習する必要が最終的にボキャブラリが付属します。</span><span class="sxs-lookup"><span data-stu-id="858e8-114">Functional programming, like other programming paradigms, comes with a vocabulary that you will eventually need to learn.</span></span> <span data-ttu-id="858e8-115">ここでは、いくつかの一般的な用語、時間のすべてが表示されます。</span><span class="sxs-lookup"><span data-stu-id="858e8-115">Here are some common terms you'll see all of the time:</span></span>

* <span data-ttu-id="858e8-116">**関数**-関数がコンス トラクターを指定した入力と出力を生成します。</span><span class="sxs-lookup"><span data-stu-id="858e8-116">**Function** - A function is a construct that will produce an output when given an input.</span></span> <span data-ttu-id="858e8-117">正式には、その_マップ_いずれかから項目を別のセットに設定します。</span><span class="sxs-lookup"><span data-stu-id="858e8-117">More formally, it _maps_ an item from one set to another set.</span></span> <span data-ttu-id="858e8-118">この形式は、データのコレクションを操作する関数を使用する際に特に多くの点で具象型にリフトされます。</span><span class="sxs-lookup"><span data-stu-id="858e8-118">This formalism is lifted into the concrete in many ways, especially when using functions that operate on collections of data.</span></span> <span data-ttu-id="858e8-119">これは、関数型プログラミングで最も基本的な (かつ重要な) 概念です。</span><span class="sxs-lookup"><span data-stu-id="858e8-119">It is the most basic (and important) concept in functional programming.</span></span> 
* <span data-ttu-id="858e8-120">**式**-式は、値を生成するコードでコンス トラクター。</span><span class="sxs-lookup"><span data-stu-id="858e8-120">**Expression** - An expression is a construct in code that produces a value.</span></span> <span data-ttu-id="858e8-121">F#、この値をバインドまたは明示的に無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="858e8-121">In F#, this value must be bound or explicitly ignored.</span></span> <span data-ttu-id="858e8-122">式は、関数呼び出しによって普通に交換できます。</span><span class="sxs-lookup"><span data-stu-id="858e8-122">An expression can be trivially replaced by a function call.</span></span>
* <span data-ttu-id="858e8-123">**純粋性**-純粋性のある関数のプロパティの戻り値は常に同じ引数を同じとその評価に副作用がありません。</span><span class="sxs-lookup"><span data-stu-id="858e8-123">**Purity** - Purity is a property of a function such that its return value is always the same for the same arguments, and that its evaluation has no side effects.</span></span> <span data-ttu-id="858e8-124">純粋関数は、その引数に完全に依存します。</span><span class="sxs-lookup"><span data-stu-id="858e8-124">A pure function depends entirely on its arguments.</span></span>
* <span data-ttu-id="858e8-125">**参照の透過性**-プログラムの動作に影響を与えずにその出力を交換できるように参照の透過性は式のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="858e8-125">**Referential Transparency** - Referential Transparency is a property of expressions such that they can be replaced with their output without affecting a program's behavior.</span></span>
* <span data-ttu-id="858e8-126">**不変性**の不変性という値にすることはできませんが、インプレースを変更します。</span><span class="sxs-lookup"><span data-stu-id="858e8-126">**Immutability** - Immutability means that a value cannot be changed in-place.</span></span> <span data-ttu-id="858e8-127">これは、変数で、インプレース変更できるとは対照的です。</span><span class="sxs-lookup"><span data-stu-id="858e8-127">This is in contrast with variables, which can change in place.</span></span>

## <a name="examples"></a><span data-ttu-id="858e8-128">使用例</span><span class="sxs-lookup"><span data-stu-id="858e8-128">Examples</span></span>

<span data-ttu-id="858e8-129">次の例では、これらの主要な概念を示します。</span><span class="sxs-lookup"><span data-stu-id="858e8-129">The following examples demonstrate these core concepts.</span></span>

### <a name="functions"></a><span data-ttu-id="858e8-130">関数</span><span class="sxs-lookup"><span data-stu-id="858e8-130">Functions</span></span>

<span data-ttu-id="858e8-131">関数型プログラミングの最も一般的なと基本的な構造は、関数です。</span><span class="sxs-lookup"><span data-stu-id="858e8-131">The most common and fundamental construct in functional programming is the function.</span></span> <span data-ttu-id="858e8-132">整数値に 1 を追加する単純な関数を次に示します。</span><span class="sxs-lookup"><span data-stu-id="858e8-132">Here's a simple function that adds 1 to an integer:</span></span>

```fsharp
let addOne x = x + 1
```

<span data-ttu-id="858e8-133">その型のシグネチャは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="858e8-133">Its type signature is as follows:</span></span>

```fsharp
val addOne: x:int -> int
```

<span data-ttu-id="858e8-134">として、署名を読み取ることができます"`addOne`を受け入れる、`int`という名前の`x`が生成されますと、 `int`"。</span><span class="sxs-lookup"><span data-stu-id="858e8-134">The signature can be read as, "`addOne` accepts an `int` named `x` and will produce an `int`".</span></span> <span data-ttu-id="858e8-135">正式には、`addOne`は_マッピング_一連の整数に整数のセットからの値。</span><span class="sxs-lookup"><span data-stu-id="858e8-135">More formally, `addOne` is _mapping_ a value from the set of integers to the set of integers.</span></span> <span data-ttu-id="858e8-136">`->`トークンは、このマッピングを示します。</span><span class="sxs-lookup"><span data-stu-id="858e8-136">The `->` token signifies this mapping.</span></span> <span data-ttu-id="858e8-137">F#、通常、処理の内容を把握関数のシグネチャを見てすることができます。</span><span class="sxs-lookup"><span data-stu-id="858e8-137">In F#, you can usually look at the function signature to get a sense for what it does.</span></span>

<span data-ttu-id="858e8-138">そのためが署名重要な理由ですか。</span><span class="sxs-lookup"><span data-stu-id="858e8-138">So, why is the signature important?</span></span> <span data-ttu-id="858e8-139">型指定された関数型プログラミング、関数の実装が多くの場合、小さい実際の型シグネチャよりも重要です。</span><span class="sxs-lookup"><span data-stu-id="858e8-139">In typed functional programming, the implementation of a function is often less important than the actual type signature!</span></span> <span data-ttu-id="858e8-140">という事実を`addOne`、実行時に興味深いは、整数値 1 を追加します。 という事実を受け入れて返すそのプログラムを構築する場合は、`int`はどのような通知、この関数を実際に使用する方法。</span><span class="sxs-lookup"><span data-stu-id="858e8-140">The fact that `addOne` adds the value 1 to an integer is interesting at runtime, but when you are constructing a program, the fact that it accepts and returns an `int` is what informs how you will actually use this function.</span></span> <span data-ttu-id="858e8-141">さらに、正しく (その型のシグネチャ) に関しては、この関数を使用すると、すべての問題を診断できますの本文内でのみ、`addOne`関数。</span><span class="sxs-lookup"><span data-stu-id="858e8-141">Furthermore, once you use this function correctly (with respect to its type signature), diagnosing any problems can be done only within the body of the `addOne` function.</span></span> <span data-ttu-id="858e8-142">これは、型指定された関数型プログラミングの背後にある材料です。</span><span class="sxs-lookup"><span data-stu-id="858e8-142">This is the impetus behind typed functional programming.</span></span>

### <a name="expressions"></a><span data-ttu-id="858e8-143">式</span><span class="sxs-lookup"><span data-stu-id="858e8-143">Expressions</span></span>

<span data-ttu-id="858e8-144">式は、値に評価する構成要素です。</span><span class="sxs-lookup"><span data-stu-id="858e8-144">Expressions are constructs that evaluate to a value.</span></span> <span data-ttu-id="858e8-145">ステートメントで、アクションを実行するとは対照的の値を提供するアクションを実行する式を考えることができます。</span><span class="sxs-lookup"><span data-stu-id="858e8-145">In contrast to statements, which perform an action, expressions can be thought of performing an action that gives back a value.</span></span> <span data-ttu-id="858e8-146">式は、関数型プログラミングでステートメントを優先してほとんどの場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="858e8-146">Expressions are almost always used in favor of statements in functional programming.</span></span>

<span data-ttu-id="858e8-147">前の関数について考えてみます`addOne`します。</span><span class="sxs-lookup"><span data-stu-id="858e8-147">Consider the previous function, `addOne`.</span></span> <span data-ttu-id="858e8-148">本文`addOne`式です。</span><span class="sxs-lookup"><span data-stu-id="858e8-148">The body of `addOne` is an expression:</span></span>

```fsharp
// 'x + 1' is an expression!
let addOne x = x + 1
```

<span data-ttu-id="858e8-149">結果型を定義する、この式の結果は、`addOne`関数。</span><span class="sxs-lookup"><span data-stu-id="858e8-149">It is the result of this expression that defines the result type of the `addOne` function.</span></span> <span data-ttu-id="858e8-150">たとえばなど別の種類を指定するこの関数を構成する式を変更できます、 `string`:</span><span class="sxs-lookup"><span data-stu-id="858e8-150">For example, the expression that makes up this function could be changed to be a different type, such as a `string`:</span></span>

```fsharp
let addOne x = x.ToString() + "1"
```

<span data-ttu-id="858e8-151">関数のシグネチャは、ようになりました。</span><span class="sxs-lookup"><span data-stu-id="858e8-151">The signature of the function is now:</span></span>

```fsharp
val addOne: x:'a -> string
```

<span data-ttu-id="858e8-152">以降のすべての種類F#が`ToString()`上の型と呼ばれる`x`ジェネリックが行わ (と呼ばれる[自動ジェネリック化](../language-reference/generics/automatic-generalization.md))、し、結果の型は、 `string`。</span><span class="sxs-lookup"><span data-stu-id="858e8-152">Since any type in F# can have `ToString()` called on it, the type of `x` has been made generic (called [Automatic Generalization](../language-reference/generics/automatic-generalization.md)), and the resultant type is a `string`.</span></span>

<span data-ttu-id="858e8-153">式は関数の本体だけではありません。</span><span class="sxs-lookup"><span data-stu-id="858e8-153">Expressions are not just the bodies of functions.</span></span> <span data-ttu-id="858e8-154">式が別の場所を使用する値を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="858e8-154">You can have expressions that produce a value you use elsewhere.</span></span> <span data-ttu-id="858e8-155">共通の 1 つは`if`:</span><span class="sxs-lookup"><span data-stu-id="858e8-155">A common one is `if`:</span></span>

```fsharp
// Checks if 'x' is odd by using the mod operator
let isOdd x = x % 2 <> 0

let addOneIfOdd input =
    let result =
        if isOdd input then
            input + 1
        else
            input

    result
```

<span data-ttu-id="858e8-156">`if`式と呼ばれる値を生成`result`します。</span><span class="sxs-lookup"><span data-stu-id="858e8-156">The `if` expression produces a value called `result`.</span></span> <span data-ttu-id="858e8-157">省略することに注意してください`result`完全に行う、`if`式本体の`addOneIfOdd`関数。</span><span class="sxs-lookup"><span data-stu-id="858e8-157">Note that you could omit `result` entirely, making the `if` expression the body of the `addOneIfOdd` function.</span></span> <span data-ttu-id="858e8-158">式について覚えておくべき重要な点は、値を生成することです。</span><span class="sxs-lookup"><span data-stu-id="858e8-158">The key thing to remember about expressions is that they produce a value.</span></span>

<span data-ttu-id="858e8-159">特殊な種類がある`unit`、nothing を返しますを使用する必要がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="858e8-159">There is a special type, `unit`, that is used when there is nothing to return.</span></span> <span data-ttu-id="858e8-160">たとえば、この単純な関数があるとします。</span><span class="sxs-lookup"><span data-stu-id="858e8-160">For example, consider this simple function:</span></span>

```fsharp
let printString (str: string) =
    printfn "String is: %s" s
```

<span data-ttu-id="858e8-161">署名のようになります。</span><span class="sxs-lookup"><span data-stu-id="858e8-161">The signature looks like this:</span></span>

```fsharp
val printString: str:string -> unit
```

<span data-ttu-id="858e8-162">`unit`型では、返される実際の値がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="858e8-162">The `unit` type indicates that there is no actual value being returned.</span></span> <span data-ttu-id="858e8-163">必要があるルーチンがある場合に便利ですが「作業」にもかかわらず、その作業結果として返される値を持たない。</span><span class="sxs-lookup"><span data-stu-id="858e8-163">This is useful when you have a routine that must "do work" despite having no value to return as a result of that work.</span></span>

<span data-ttu-id="858e8-164">これは、命令型プログラミングに対照的場所と同じ`if`コンストラクトとは、ステートメントと変数の変化でよく行われますが値を生成します。</span><span class="sxs-lookup"><span data-stu-id="858e8-164">This is in sharp contrast to imperative programming, where the equivalent `if` construct is a statement, and producing values is often done with mutating variables.</span></span> <span data-ttu-id="858e8-165">たとえば、 C#、このようなコードを記述する場合があります。</span><span class="sxs-lookup"><span data-stu-id="858e8-165">For example, in C#, the code might be written like this:</span></span>

```csharp
bool IsOdd(int x) => x % 2 != 0;

int AddOneIfOdd(int input)
{
    var result = input;

    if (IsOdd(input))
    {
        result = input + 1;
    }

    return result;
}
```

<span data-ttu-id="858e8-166">いることに注意がC#おり、他の C スタイル言語サポート、[三項式](../../csharp/language-reference/operators/conditional-operator.md)、式ベースの条件付きプログラミングのことができます。</span><span class="sxs-lookup"><span data-stu-id="858e8-166">It's worth noting that C# and other C-style languages do support the [ternary expression](../../csharp/language-reference/operators/conditional-operator.md), which allows for expression-based conditional programming.</span></span>

<span data-ttu-id="858e8-167">関数型プログラミングで行うことはまれステートメントで値を変更します。</span><span class="sxs-lookup"><span data-stu-id="858e8-167">In functional programming, it is rare to mutate values with statements.</span></span> <span data-ttu-id="858e8-168">ステートメントと変異をいくつかの関数型言語をサポート関数型プログラミングでこれらの概念を使用する一般的なことはありません。</span><span class="sxs-lookup"><span data-stu-id="858e8-168">Although some functional languages support statements and mutation, it is not common to use these concepts in functional programming.</span></span>

### <a name="pure-functions"></a><span data-ttu-id="858e8-169">純粋関数</span><span class="sxs-lookup"><span data-stu-id="858e8-169">Pure functions</span></span>

<span data-ttu-id="858e8-170">前に説明した、純粋関数は、関数します。</span><span class="sxs-lookup"><span data-stu-id="858e8-170">As previously mentioned, pure functions are functions that:</span></span>

* <span data-ttu-id="858e8-171">常に同じ入力に対して同じ値に評価します。</span><span class="sxs-lookup"><span data-stu-id="858e8-171">Always evaluate to the same value for the same input.</span></span>
* <span data-ttu-id="858e8-172">副作用があるありません。</span><span class="sxs-lookup"><span data-stu-id="858e8-172">Have no side effects.</span></span>

<span data-ttu-id="858e8-173">このコンテキストの数学関数と考えることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="858e8-173">It is helpful to think of mathematical functions in this context.</span></span> <span data-ttu-id="858e8-174">数学では、関数は、引数にのみ依存し、は、副作用はありません。</span><span class="sxs-lookup"><span data-stu-id="858e8-174">In mathematics, functions depend only on their arguments and do not have any side effects.</span></span> <span data-ttu-id="858e8-175">数学関数で`f(x) = x + 1`の値`f(x)`の値にのみ依存`x`します。</span><span class="sxs-lookup"><span data-stu-id="858e8-175">In the mathematical function `f(x) = x + 1`, the value of `f(x)` depends only on the value of `x`.</span></span> <span data-ttu-id="858e8-176">純粋関数型プログラミングでは、同じ方法です。</span><span class="sxs-lookup"><span data-stu-id="858e8-176">Pure functions in functional programming are the same way.</span></span>

<span data-ttu-id="858e8-177">純粋関数を記述するときに関数は引数のみに依存し、結果、副次的になる任意のアクションを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="858e8-177">When writing a pure function, the function must depend only on its arguments and not perform any action that results in a side effect.</span></span>

<span data-ttu-id="858e8-178">次のグローバルな変更可能な状態に依存するために非純粋関数の例を示します。</span><span class="sxs-lookup"><span data-stu-id="858e8-178">Here is an example of a non-pure function because it depends on global, mutable state:</span></span>

```fsharp
let mutable value = 1

let addOneToValue x = x + value
```

<span data-ttu-id="858e8-179">`addOneToValue`関数が明確に純粋なため、 `value` 1 よりも異なる値を設定するには、いつでも変更できます。</span><span class="sxs-lookup"><span data-stu-id="858e8-179">The `addOneToValue` function is clearly impure, because `value` could be changed at any time to have a different value than 1.</span></span> <span data-ttu-id="858e8-180">グローバル値に応じてのこのパターンでは、関数型プログラミングに回避されます。</span><span class="sxs-lookup"><span data-stu-id="858e8-180">This pattern of depending on a global value is to be avoided in functional programming.</span></span>

<span data-ttu-id="858e8-181">次の副作用を実行するための非純粋関数では、別の例に示します。</span><span class="sxs-lookup"><span data-stu-id="858e8-181">Here is another example of a non-pure function, because it performs a side effect:</span></span>

```fsharp
let addOneToValue x = 
    printfn "x is %d" x
    x + 1
```

<span data-ttu-id="858e8-182">値を書き込むが、この関数は、グローバルな値に依存しない、`x`プログラムの出力にします。</span><span class="sxs-lookup"><span data-stu-id="858e8-182">Although this function does not depend on a global value, it writes the value of `x` to the output of the program.</span></span> <span data-ttu-id="858e8-183">これを行うには本質的に問題はありませんが、関数が純粋でないことわけです。</span><span class="sxs-lookup"><span data-stu-id="858e8-183">Although there is nothing inherently wrong with doing this, it does mean that the function is not pure.</span></span>

<span data-ttu-id="858e8-184">削除、`printfn`ステートメント最後には、関数は、純粋な。</span><span class="sxs-lookup"><span data-stu-id="858e8-184">Removing the `printfn` statement finally makes the function pure:</span></span>

```fsharp
let addOneToValue x = x + 1
```

<span data-ttu-id="858e8-185">この機能は本質的には_優れた_で以前のバージョンよりも、`printfn`ステートメントでは、その値を返すこの関数はすべて、保証は。</span><span class="sxs-lookup"><span data-stu-id="858e8-185">Although this function is not inherently _better_ than the previous version with the `printfn` statement, it does guarantee that all this function does is return a value.</span></span> <span data-ttu-id="858e8-186">この関数を呼び出す関数の 1 回または 1 90億回は同じでも結果: 同じ値を生成します。</span><span class="sxs-lookup"><span data-stu-id="858e8-186">Calling this function once or 1 billion times will still result in the same thing: just producing a value.</span></span> <span data-ttu-id="858e8-187">この予測は、任意の純粋関数がしいものに透過的なことを意味するために関数型プログラミングで重要です。</span><span class="sxs-lookup"><span data-stu-id="858e8-187">This predictability is valuable in functional programming, as it means that any pure function is referentially transparent.</span></span>

### <a name="referential-transparency"></a><span data-ttu-id="858e8-188">参照の透過性</span><span class="sxs-lookup"><span data-stu-id="858e8-188">Referential Transparency</span></span>

<span data-ttu-id="858e8-189">参照の透過性は、式と関数のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="858e8-189">Referential transparency is a property of expressions and functions.</span></span> <span data-ttu-id="858e8-190">透明しいものである式をプログラムの動作を変更することがなく、結果の値に置き換えることがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="858e8-190">For an expression to be referentially transparent, it must be able to be replaced with its resulting value without changing the program's behavior.</span></span> <span data-ttu-id="858e8-191">すべての純粋関数では、しいもの透過的です。</span><span class="sxs-lookup"><span data-stu-id="858e8-191">All pure functions are referentially transparent.</span></span>

<span data-ttu-id="858e8-192">純粋関数と同様は数学的な観点からは参照の透過性を考えることができます。</span><span class="sxs-lookup"><span data-stu-id="858e8-192">As with pure functions, it can be helpful to think of referential transparency from a mathematical perspective.</span></span> <span data-ttu-id="858e8-193">算術式で`y = f(x)`、`f(x)`関数の結果を置き換えと等しくあってはまだ`y`します。</span><span class="sxs-lookup"><span data-stu-id="858e8-193">In the mathematical expression `y = f(x)`, `f(x)` can be replaced by the result of the function and it will still be equal to `y`.</span></span> <span data-ttu-id="858e8-194">これは関数型プログラミングで参照の透過性を均等に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="858e8-194">This is equally true for referential transparency in functional programming.</span></span>

<span data-ttu-id="858e8-195">以前に定義されたを呼び出してください`addOneIfOdd`関数を 2 回。</span><span class="sxs-lookup"><span data-stu-id="858e8-195">Consider calling the previously defined `addOneIfOdd` function twice:</span></span>

```fsharp
// Checks if 'x' is odd by using the mod operator
let isOdd x = x % 2 <> 0

let addOneIfOdd input =
    let result =
        if isOdd input then
            input + 1
        else
            input

    result

let res1 = addOneIffOdd 1 // Produces 2
let res2 = addOneIffOdd 2 // Produces 2
```

<span data-ttu-id="858e8-196">引数の置換、関数本体の各関数呼び出しを置き換えることができます`input`個々 の値。</span><span class="sxs-lookup"><span data-stu-id="858e8-196">We can replace each function call with the function body, substituting the argument `input` with each value:</span></span>

```fsharp
// Checks if 'x' is odd by using the mod operator
let isOdd x = x % 2 <> 0

let addOneIfOdd input =
    let result =
        if isOdd input then
            input + 1
        else
            input

    result

let res1 =
    let result =
        if isOdd 1 then
            1 + 1
        else
            1

    result
let res2 =
    let result =
        if isOdd 2 then
            2 + 1
        else
            2

    result
```

<span data-ttu-id="858e8-197">両方`res1`と`res2`関数が呼び出されたことを示す場合と同じ値を持つ`addOneIfOdd`はしいものに対して透過的です。</span><span class="sxs-lookup"><span data-stu-id="858e8-197">Both `res1` and `res2` have the same value as if the function was called, indicating that `addOneIfOdd` is referentially transparent!</span></span>

<span data-ttu-id="858e8-198">さらに、関数は、純粋にも、透過的なしいものにありません。</span><span class="sxs-lookup"><span data-stu-id="858e8-198">Additionally, a function doesn't have to be pure to also be referentially transparent.</span></span> <span data-ttu-id="858e8-199">以前の定義を検討してください`addOneTovalue`:。</span><span class="sxs-lookup"><span data-stu-id="858e8-199">Consider a previous definition of  `addOneTovalue`:</span></span>

```fsharp
let addOneToValue x = 
    printfn "x is %d" x
    x + 1
```

<span data-ttu-id="858e8-200">この関数への呼び出しは、その本体で置き換えることもでき、同じ処理には、毎回が行われます。</span><span class="sxs-lookup"><span data-stu-id="858e8-200">Any call to this function can also be replaced by its body and the same things will happen each time:</span></span>

* <span data-ttu-id="858e8-201">出力に、追加される前に、値が出力されます。</span><span class="sxs-lookup"><span data-stu-id="858e8-201">The value, prior to being added to, is printed to the output</span></span>
* <span data-ttu-id="858e8-202">値が 1 の追加</span><span class="sxs-lookup"><span data-stu-id="858e8-202">The value has 1 added to it</span></span>

<span data-ttu-id="858e8-203">プログラミングするときF#、純粋性ではなく、目標は、参照の透過性がよくあります。</span><span class="sxs-lookup"><span data-stu-id="858e8-203">When programming in F#, it is often referential transparency that is the goal, rather than purity.</span></span> <span data-ttu-id="858e8-204">ただし、可能な場合に、純粋関数を記述することをおすすめなります。</span><span class="sxs-lookup"><span data-stu-id="858e8-204">However, it is still good practice to write pure functions when you can.</span></span>

### <a name="immutability"></a><span data-ttu-id="858e8-205">不変性</span><span class="sxs-lookup"><span data-stu-id="858e8-205">Immutability</span></span>

<span data-ttu-id="858e8-206">最後に、型指定された関数型プログラミングの最も基本的な概念の 1 つは不変です。</span><span class="sxs-lookup"><span data-stu-id="858e8-206">Finally, one of the most fundamental concepts of typed functional programming is immutability.</span></span> <span data-ttu-id="858e8-207">F#、すべての値は既定では変更できません。</span><span class="sxs-lookup"><span data-stu-id="858e8-207">In F#, all values are immutable by default.</span></span> <span data-ttu-id="858e8-208">つまり、明示的にマークを付ける変更可能な場合を除き、インプレースで変換をすることはできません。</span><span class="sxs-lookup"><span data-stu-id="858e8-208">That means they cannot be mutated in-place unless you explicitly mark them as mutable.</span></span>

<span data-ttu-id="858e8-209">実際には、変更不可の値の操作は、ことから、「何かを変更する必要があります」プログラミングのアプローチを変更するに"べき新しい値を生成するためを意味します。</span><span class="sxs-lookup"><span data-stu-id="858e8-209">In practice, working with immutable values means that you change your approach to programming from, "I need to change something", to "I need to produce a new value".</span></span>

<span data-ttu-id="858e8-210">たとえば、値を追加する 1 いない既存の 1 つの変化、新しい値を生成を意味します。</span><span class="sxs-lookup"><span data-stu-id="858e8-210">For example, adding 1 to a value means producing a new value, not mutating the existing one:</span></span>

```fsharp
let value = 1
let secondValue = value + 1
```

<span data-ttu-id="858e8-211">F#、コードを次に**いない**変異、`value`関数です。 は、等しいかどうかチェックを代わりに、が実行されます。</span><span class="sxs-lookup"><span data-stu-id="858e8-211">In F#, the following code does **not** mutate the `value` function; instead, it performs an equality check:</span></span>

```fsharp
let value = 1
value = value + 1 // Produces a 'bool' value!
```

<span data-ttu-id="858e8-212">いくつかの関数型プログラミング言語は変化をまったくサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="858e8-212">Some functional programming languages do not support mutation at all.</span></span> <span data-ttu-id="858e8-213">F#、可能ですが、値の既定の動作ではありません。</span><span class="sxs-lookup"><span data-stu-id="858e8-213">In F#, it is supported, but it is not the default behavior for values.</span></span>

<span data-ttu-id="858e8-214">この概念は、データ構造のさらにも拡張します。</span><span class="sxs-lookup"><span data-stu-id="858e8-214">This concept extends even further to data structures.</span></span> <span data-ttu-id="858e8-215">関数型プログラミングで不変のデータ構造セット (とさらに多く) 通常よりも最初に、さまざまな実装があるなど、期待しています。</span><span class="sxs-lookup"><span data-stu-id="858e8-215">In functional programming, immutable data structures such as sets (and many more) have a different implementation than you might initially expect.</span></span> <span data-ttu-id="858e8-216">概念的には、セットに項目を追加しても、セットが変更されないようになる、_新しい_追加された値に設定します。</span><span class="sxs-lookup"><span data-stu-id="858e8-216">Conceptually, something like adding an item to a set does not change the set, it produces a _new_ set with the added value.</span></span> <span data-ttu-id="858e8-217">実際には、これは多くの場合の結果として、データの適切な表現を指定できるように、値を効率的に追跡できるようにするさまざまなデータ構造で行います。</span><span class="sxs-lookup"><span data-stu-id="858e8-217">Under the covers, this is often accomplished by a different data structure that allows for efficiently tracking a value so that the appropriate representation of the data can be given as a result.</span></span>

<span data-ttu-id="858e8-218">値とデータ構造の操作には、このスタイルは、この操作をするの新しいバージョンを作成する場合、何か変更する操作を扱うことを強制的に、重要です。</span><span class="sxs-lookup"><span data-stu-id="858e8-218">This style of working with values and data structures is critical, as it forces you to treat any operation that modifies something as if it creates a new version of that thing.</span></span> <span data-ttu-id="858e8-219">これにより、プログラムで一貫性のあるすべき点が等しいかどうかや比較など。</span><span class="sxs-lookup"><span data-stu-id="858e8-219">This allows for things like equality and comparability to be consistent in your programs.</span></span>

## <a name="next-steps"></a><span data-ttu-id="858e8-220">次の手順</span><span class="sxs-lookup"><span data-stu-id="858e8-220">Next steps</span></span>

<span data-ttu-id="858e8-221">次のセクションは、関数、関数型プログラミングで使用することができます、さまざまな方法を調査を十分に説明します。</span><span class="sxs-lookup"><span data-stu-id="858e8-221">The next section will thoroughly cover functions, exploring different ways you can use them in functional programming.</span></span>

<span data-ttu-id="858e8-222">[ファーストクラス関数](first-class-functions.md)関数を深く、紹介さまざまなコンテキストで使用する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="858e8-222">[First-class functions](first-class-functions.md) explores functions deeply, showing how you can use them in various contexts.</span></span>

## <a name="further-reading"></a><span data-ttu-id="858e8-223">関連項目</span><span class="sxs-lookup"><span data-stu-id="858e8-223">Further reading</span></span>

<span data-ttu-id="858e8-224">[考える機能的](https://fsharpforfunandprofit.com/posts/thinking-functionally-intro/)シリーズは、関数型プログラミングの詳細については、別の優れたリソースF#します。</span><span class="sxs-lookup"><span data-stu-id="858e8-224">The [Thinking Functionally](https://fsharpforfunandprofit.com/posts/thinking-functionally-intro/) series is another great resource to learn about functional programming with F#.</span></span> <span data-ttu-id="858e8-225">関数型プログラミングの基礎について説明します、pragmatic と読みやすい方法でを使用してF#な概念を説明する機能。</span><span class="sxs-lookup"><span data-stu-id="858e8-225">It covers fundamentals of functional programming in a pragmatic and easy-to-read way, using F# features to illustrate the concepts.</span></span>