---
title: F# コードの書式設定のガイドライン
description: F# コードの書式設定するためのガイドラインについて説明します。
ms.date: 05/14/2018
ms.openlocfilehash: 9c6e80509e9a5654e6514674d38c02e2a6b44e37
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43734643"
---
# <a name="f-code-formatting-guidelines"></a><span data-ttu-id="4e7b5-103">F# コードの書式設定のガイドライン</span><span class="sxs-lookup"><span data-stu-id="4e7b5-103">F# code formatting guidelines</span></span>

<span data-ttu-id="4e7b5-104">この記事では、f# コードが実行されるように、コードを書式設定する方法に関するガイドラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-104">This article offers guidelines for how to format your code so that your F# code is:</span></span>

* <span data-ttu-id="4e7b5-105">一般に読みやすくとして表示</span><span class="sxs-lookup"><span data-stu-id="4e7b5-105">Generally viewed as more legible</span></span>
* <span data-ttu-id="4e7b5-106">Visual Studio のツールとその他のエディターの書式設定が適用される規則に従って、します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-106">Is in accordance with conventions applied by formatting tools in Visual Studio and other editors</span></span>
* <span data-ttu-id="4e7b5-107">その他のコードをオンラインに似ています</span><span class="sxs-lookup"><span data-stu-id="4e7b5-107">Similar to other code online</span></span>

<span data-ttu-id="4e7b5-108">これらのガイドラインに基づいています[f# の書式設定規則に包括的なガイド](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md)によって[Anh 協力 Phan](https://github.com/dungpa)します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-108">These guidelines are based on [A comprehensive guide to F# Formatting Conventions](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) by [Anh-Dung Phan](https://github.com/dungpa).</span></span>

## <a name="general-rules-for-indentation"></a><span data-ttu-id="4e7b5-109">インデントの一般的な規則</span><span class="sxs-lookup"><span data-stu-id="4e7b5-109">General rules for indentation</span></span>

<span data-ttu-id="4e7b5-110">F# で既定では、有意の空白を使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-110">F# uses significant white space by default.</span></span> <span data-ttu-id="4e7b5-111">次のガイドラインはこれをかけることがいくつかの課題を使い分ける方法についてのガイダンスを提供するためのものです。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-111">The following guidelines are intended to provide guidance as to how to juggle some challenges this can impose.</span></span>

### <a name="using-spaces"></a><span data-ttu-id="4e7b5-112">スペースを使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-112">Using spaces</span></span>

<span data-ttu-id="4e7b5-113">インデントが必要な場合は、スペース、タブではなくを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-113">When indentation is required, you must use spaces, not tabs.</span></span> <span data-ttu-id="4e7b5-114">少なくとも 1 つの領域が必要です。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-114">At least one space is required.</span></span> <span data-ttu-id="4e7b5-115">組織がインデントに使用する空白文字の数を指定するコーディング規則を作成できます。各レベルのインデントを設定するインデントの 2 つ、3 つまたは 4 つのスペースが一般的です。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-115">Your organization can create coding standards to specify the number of spaces to use for indentation; two, three or four spaces of indentation at each level where indentation occurs is typical.</span></span>

<span data-ttu-id="4e7b5-116">**インデントあたり 4 つのスペースをお勧めします。**</span><span class="sxs-lookup"><span data-stu-id="4e7b5-116">**We recommend 4 spaces per indentation.**</span></span>

<span data-ttu-id="4e7b5-117">ただし、プログラムのインデントは主観的な問題。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-117">That said, indentation of programs is a subjective matter.</span></span> <span data-ttu-id="4e7b5-118">バリエーションが [ok] が最初の規則に従う必要がありますが、*インデントの一貫性*します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-118">Variations are OK, but the first rule you should follow is *consistency of indentation*.</span></span> <span data-ttu-id="4e7b5-119">インデントの一般的に受け入れられるスタイルを選択し、コードベース全体で体系的に使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-119">Choose a generally accepted style of indentation and use it systematically throughout your codebase.</span></span>

## <a name="formatting-blank-lines"></a><span data-ttu-id="4e7b5-120">空白行を書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-120">Formatting blank lines</span></span>

* <span data-ttu-id="4e7b5-121">独立したトップレベル関数やクラスの定義 2 つの空白行を含む。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-121">Separate top-level function and class definitions with two blank lines.</span></span>
* <span data-ttu-id="4e7b5-122">クラス内でメソッドの定義は、単一の空白行で区切られます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-122">Method definitions inside a class are separated by a single blank line.</span></span>
* <span data-ttu-id="4e7b5-123">余分な空白行は、関連する関数のグループを区切る (控えめ) に使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-123">Extra blank lines may be used (sparingly) to separate groups of related functions.</span></span> <span data-ttu-id="4e7b5-124">一連の関連困ら (たとえば、ダミーの実装のセット) の間の空白行は省略できます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-124">Blank lines may be omitted between a bunch of related one-liners (for example, a set of dummy implementations).</span></span>
* <span data-ttu-id="4e7b5-125">論理的なセクションを示すために、関数では、空白行を使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-125">Use blank lines in functions, sparingly, to indicate logical sections.</span></span>

## <a name="formatting-comments"></a><span data-ttu-id="4e7b5-126">コメントの書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-126">Formatting comments</span></span>

<span data-ttu-id="4e7b5-127">一般に ML スタイル ブロックのコメントを複数のコメントをダブル スラッシュを好みます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-127">Generally prefer multiple double-slash comments over ML-style block comments.</span></span>

```fsharp
// Prefer this style of comments when you want
// to express written ideas on multiple lines.

(*
    ML-style comments are fine, but not a .NET-ism.
    They are useful when needing to modify multi-line comments, though.
*)
```

<span data-ttu-id="4e7b5-128">インライン コメントは、最初の文字を大文字にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-128">Inline comments should capitalize the first letter.</span></span>

```fsharp
let f x = x + 1 // Increment by one.
```

## <a name="naming-conventions"></a><span data-ttu-id="4e7b5-129">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="4e7b5-129">Naming conventions</span></span>

### <a name="use-camelcase-for-class-bound-expression-bound-and-pattern-bound-values-and-functions"></a><span data-ttu-id="4e7b5-130">キャメル ケースを使用して、クラス バインド、バインド式とパターン バインドの値と関数</span><span class="sxs-lookup"><span data-stu-id="4e7b5-130">Use camelCase for class-bound, expression-bound and pattern-bound values and functions</span></span>

<span data-ttu-id="4e7b5-131">一般的な camelCase を使用して、すべての名前を指定できる f# スタイルには、ローカル変数として、またはパターン マッチと関数定義がバインドされています。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-131">It is common and accepted F# style to use camelCase for all names bound as local variables or in pattern matches and function definitions.</span></span>

```fsharp
// OK
let addIAndJ i j = i + j

// Bad
let addIAndJ I J = I+J

// Bad
let AddIAndJ i j = i + j
```

<span data-ttu-id="4e7b5-132">クラスのローカルにバインドされた関数は、camelCase を使用してもする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-132">Locally-bound functions in classes should also use camelCase.</span></span>

```fsharp
type MyClass() =

    let doSomething () =

    let firstResult = ...

    let secondResult = ...

    member x.Result = doSomething()
```

### <a name="use-camelcase-for-module-bound-public-functions"></a><span data-ttu-id="4e7b5-133">キャメル ケースを使用してバインド モジュールのパブリック関数</span><span class="sxs-lookup"><span data-stu-id="4e7b5-133">Use camelCase for module-bound public functions</span></span>

<span data-ttu-id="4e7b5-134">モジュール連結関数は、パブリック API の一部が、camelCase を使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-134">When a module-bound function is part of a public API, it should use camelCase:</span></span>

```fsharp
module MyAPI =
    let publicFunctionOne param1 param2 param2 = ...

    let publicFunctionTwo param1 param2 param3 = ...
```

### <a name="use-camelcase-for-internal-and-private-module-bound-values-and-functions"></a><span data-ttu-id="4e7b5-135">キャメル ケースを使用して、内部、プライベート モジュール連結値および関数</span><span class="sxs-lookup"><span data-stu-id="4e7b5-135">Use camelCase for internal and private module-bound values and functions</span></span>

<span data-ttu-id="4e7b5-136">プライベート モジュール連結値は、次のようには、camelCase を使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-136">Use camelCase for private module-bound values, including the following:</span></span>

* <span data-ttu-id="4e7b5-137">スクリプトでアドホック関数</span><span class="sxs-lookup"><span data-stu-id="4e7b5-137">Ad hoc functions in scripts</span></span>

* <span data-ttu-id="4e7b5-138">モジュールまたは型の内部実装を作成する値</span><span class="sxs-lookup"><span data-stu-id="4e7b5-138">Values making up the internal implementation of a module or type</span></span>

```fsharp
let emailMyBossTheLatestResults =
    ...
```

### <a name="use-camelcase-for-parameters"></a><span data-ttu-id="4e7b5-139">パラメーターにキャメル ケースを使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-139">Use camelCase for parameters</span></span>

<span data-ttu-id="4e7b5-140">すべてのパラメーターは、.NET の名前付け規則に従って、camelCase を使用してください。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-140">All parameters should use camelCase in accordance with .NET naming conventions.</span></span>

```fsharp
module MyModule =
    let myFunction paramOne paramTwo = ...

type MyClass() =
    member this.MyMethod(paramOne, paramTwo) = ...
```

### <a name="use-pascalcase-for-modules"></a><span data-ttu-id="4e7b5-141">PascalCase モジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-141">Use PascalCase for modules</span></span>

<span data-ttu-id="4e7b5-142">(最上位レベル、内部、プライベートの入れ子になった) のすべてのモジュールは PascalCase を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-142">All modules (top-level, internal, private, nested) should use PascalCase.</span></span>

```fsharp
module MyTopLevelModule

module Helpers =
    module private SuperHelpers =
        ...

    ...
```

### <a name="use-pascalcase-for-type-declarations-members-and-labels"></a><span data-ttu-id="4e7b5-143">PascalCase を使用して、型宣言、メンバー、およびラベル</span><span class="sxs-lookup"><span data-stu-id="4e7b5-143">Use PascalCase for type declarations, members, and labels</span></span>

<span data-ttu-id="4e7b5-144">クラス、インターフェイス、構造体、列挙、デリゲート、レコード、および判別共用体がすべての名前は PascalCase です。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-144">Classes, interfaces, structs, enumerations, delegates, records, and discriminated unions should all be named with PascalCase.</span></span> <span data-ttu-id="4e7b5-145">型およびレコード、判別共用体のラベル内のメンバーは、PascalCase を使用してもする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-145">Members within types and labels for records and discriminated unions should also use PascalCase.</span></span>

```fsharp
type IMyInterface =
    abstract Something: int

type MyClass() =
    member this.MyMethod(x, y) = x + y

type MyRecord = { IntVal: int; StringVal: string }

type SchoolPerson =
    | Professor
    | Student
    | Advisor
    | Administrator
```

### <a name="use-pascalcase-for-constructs-intrinsic-to-net"></a><span data-ttu-id="4e7b5-146">PascalCase を使用して、.NET に固有の構成要素</span><span class="sxs-lookup"><span data-stu-id="4e7b5-146">Use PascalCase for constructs intrinsic to .NET</span></span>

<span data-ttu-id="4e7b5-147">名前空間、例外、イベント、およびプロジェクト/`.dll`名も PascalCase を使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-147">Namespaces, exceptions, events, and project/`.dll` names should also use PascalCase.</span></span> <span data-ttu-id="4e7b5-148">だけでなく、これにより、コンシューマーに自然に感じられる他の .NET 言語から消費も発生する可能性がある .NET の名前付け規則と一致します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-148">Not only does this make consumption from other .NET languages feel more natural to consumers, it's also consistent with .NET naming conventions that you are likely to encounter.</span></span>

### <a name="avoid-underscores-in-names"></a><span data-ttu-id="4e7b5-149">名前にアンダー スコアを回避します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-149">Avoid underscores in names</span></span>

<span data-ttu-id="4e7b5-150">従来、一部の f# ライブラリは、名前にアンダー スコアを使用するが。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-150">Historically, some F# libraries have used underscores in names.</span></span> <span data-ttu-id="4e7b5-151">ただし、これが不要になった広く受け入れられて .NET の名前付け規則と衝突ためです。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-151">However, this is no longer widely accepted, partly because it clashes with .NET naming conventions.</span></span> <span data-ttu-id="4e7b5-152">ただし、f# プログラマによってアンダー スコアは使用頻度の高い、一部の歴史的な理由と許容範囲と点が重要です。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-152">That said, some F# programmers use underscores heavily, partly for historical reasons, and tolerance and respect is important.</span></span> <span data-ttu-id="4e7b5-153">ただし、スタイルが使用するかどうかの選択肢を持つ他のユーザーによって多くの場合、我慢しなければならないこともあります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-153">However, be aware that the style is often disliked by others who have a choice about whether to use it.</span></span>

<span data-ttu-id="4e7b5-154">いくつかの例外には、アンダー スコアが非常に一般的であるネイティブのコンポーネントとの相互運用が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-154">Some exceptions includes interoperating with native components, where underscores are very common.</span></span>

### <a name="use-standard-f-operators"></a><span data-ttu-id="4e7b5-155">標準的な f# 演算子を使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-155">Use standard F# operators</span></span>

<span data-ttu-id="4e7b5-156">次の演算子は、f# の標準ライブラリで定義され、対応を定義する代わりに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-156">The following operators are defined in the F# standard library and should be used instead of defining equivalents.</span></span> <span data-ttu-id="4e7b5-157">読みやすく、慣用コードを作成する傾向が、これらの演算子の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-157">Using these operators is recommended as it tends to make code more readable and idiomatic.</span></span> <span data-ttu-id="4e7b5-158">OCaml またはその他の関数型プログラミング言語の背景を持つ開発者は、さまざまな表現方法に慣れて可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-158">Developers with a background in OCaml or other functional programming language may be accustomed to different idioms.</span></span> <span data-ttu-id="4e7b5-159">次の一覧は、推奨の f# 演算子をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-159">The following list summarizes the recommended F# operators.</span></span>

```fsharp
x |> f // Forward pipeline
f >> g // Forward composition
x |> ignore // Discard away a value
x + y // Overloaded addition (including string concatenation)
x - y // Overloaded subtraction
x * y // Overloaded multiplication
x / y // Overloaded division
x % y // Overloaded modulus
x && y // Lazy/short-cut "and"
x || y // Lazy/short-cut "or"
x <<< y // Bitwise left shift
x >>> y // Bitwise right shift
x ||| y // Bitwise or, also for working with “flags” enumeration
x &&& y // Bitwise and, also for working with “flags” enumeration
x ^^^ y // Bitwise xor, also for working with “flags” enumeration
```

### <a name="use-prefix-syntax-for-generics-foot-in-preference-to-postfix-syntax-t-foo"></a><span data-ttu-id="4e7b5-160">ジェネリックのプレフィックスの構文を使用して (`Foo<T>`) 方が優先的後置構文 (`T Foo`)</span><span class="sxs-lookup"><span data-stu-id="4e7b5-160">Use prefix syntax for generics (`Foo<T>`) in preference to postfix syntax (`T Foo`)</span></span>

<span data-ttu-id="4e7b5-161">F# ジェネリック型の名前付けの両方、後置 ML スタイルを継承する (たとえば、 `int list`) .NET スタイルのプレフィックスと (たとえば、 `list<int>`)。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-161">F# inherits both the postfix ML style of naming generic types (for example, `int list`) as well as the prefix .NET style (for example, `list<int>`).</span></span> <span data-ttu-id="4e7b5-162">次の 4 つの特定の型を除く、.NET スタイルを優先するには。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-162">Prefer the .NET style, except for four specific types:</span></span>

1. <span data-ttu-id="4e7b5-163">F# リストは、後置形式を使用:`int list`なく`list<int>`します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-163">For F# Lists, use the postfix form: `int list` rather than `list<int>`.</span></span>
2. <span data-ttu-id="4e7b5-164">F# オプションについては、後置形式を使用:`int option`なく`option<int>`します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-164">For F# Options, use the postfix form: `int option` rather than `option<int>`.</span></span>
3. <span data-ttu-id="4e7b5-165">F# の配列、構文の名前を使用`int[]`なく`int array`または`array<int>`します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-165">For F# arrays, use the syntactic name `int[]` rather than `int array` or `array<int>`.</span></span>
4. <span data-ttu-id="4e7b5-166">参照セルを使用して`int ref`なく`ref<int>`または`Ref<int>`します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-166">For Reference Cells, use `int ref` rather than `ref<int>` or `Ref<int>`.</span></span>

<span data-ttu-id="4e7b5-167">他のすべての種類では、前置形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-167">For all other types, use the prefix form.</span></span>

## <a name="formatting-tuples"></a><span data-ttu-id="4e7b5-168">タプルの書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-168">Formatting tuples</span></span>

<span data-ttu-id="4e7b5-169">タプル インスタンス化はかっこで囲まれた、する必要があり、内で使用する区切りコンマをたとえば、1 つのスペースで従う必要が: `(1, 2)`、`(x, y, z)`します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-169">A tuple instantiation should be parenthesized, and the delimiting commas within should be followed by a single space, for example: `(1, 2)`, `(x, y, z)`.</span></span>

<span data-ttu-id="4e7b5-170">タプルのパターン マッチングでは、かっこを省略することがよく受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-170">It is commonly accepted to omit parentheses in pattern matching of tuples:</span></span>

```fsharp
let (x, y) = z // Destructuring
let x, y = z // OK

// OK
match x, y with
| 1, _ -> 0
| x, 1 -> 0
| x, y -> 1
```

## <a name="formatting-discriminated-union-declarations"></a><span data-ttu-id="4e7b5-171">判別共用体の宣言の書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-171">Formatting discriminated union declarations</span></span>

<span data-ttu-id="4e7b5-172">インデント`|`によって 4 つのスペースの種類の定義。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-172">Indent `|` in type definition by 4 spaces:</span></span>

```fsharp
// OK
type Volume =
    | Liter of float
    | FluidOunce of float
    | ImperialPint of float

// Not OK
type Volume =
| Liter of float
| USPint of float
| ImperialPint of float
```

## <a name="formatting-discriminated-unions"></a><span data-ttu-id="4e7b5-173">判別共用体の書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-173">Formatting discriminated unions</span></span>

<span data-ttu-id="4e7b5-174">複数行にわたって判別の共用体はインスタンス化されたはインデントで新しいスコープに含まれているデータを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-174">Instantiated Discriminated Unions that split across multiple lines should give contained data a new scope with indentation:</span></span>

```fsharp
let tree1 =
    BinaryNode
        (BinaryNode(BinaryValue 1, BinaryValue 2),
         BinaryNode(BinaryValue 3, BinaryValue 4))
```

<span data-ttu-id="4e7b5-175">新しい行の終わりかっこのこともできます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-175">The closing parenthesis can also be on a new line:</span></span>

```fsharp
let tree1 =
    BinaryNode(
        BinaryNode(BinaryValue 1, BinaryValue 2),
        BinaryNode(BinaryValue 3, BinaryValue 4)
    )
```

## <a name="formatting-record-declarations"></a><span data-ttu-id="4e7b5-176">レコードの宣言を書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-176">Formatting record declarations</span></span>

<span data-ttu-id="4e7b5-177">インデント`{`4 で定義型で空白し、同じ行にフィールド リストの先頭します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-177">Indent `{` in type definition by 4 spaces and start the field list on the same line:</span></span>

```fsharp
// OK
type PostalAddress =
    { Address : string
      City : string
      Zip : string }
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City

// Not OK
type PostalAddress =
  { Address : string
    City : string
    Zip : string }
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City
    
// Unusual in F#
type PostalAddress =
    { 
        Address : string
        City : string
        Zip : string
    }
```

<span data-ttu-id="4e7b5-178">問題でも、同じ行で、新しい行に終了トークン開始トークンを配置することですを使用する必要があることに注意してください、[冗語構文](../language-reference/verbose-syntax.md)メンバーを定義する (、`with`キーワード)。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-178">Placing the opening token on the same line and the closing token on a new line is also fine, but be aware that you need to use the [verbose syntax](../language-reference/verbose-syntax.md) to define members (the `with` keyword):</span></span>

```fsharp
//  OK, but verbose syntax required
type PostalAddress = { 
    Address : string
    City : string
    Zip : string
} with
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City
```

## <a name="formatting-records"></a><span data-ttu-id="4e7b5-179">レコードを書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-179">Formatting records</span></span>

<span data-ttu-id="4e7b5-180">1 行では、短いレコードを記述することができます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-180">Short records can be written in one line:</span></span>

```fsharp
let point = { X = 1.0; Y = 0.0 }
```

<span data-ttu-id="4e7b5-181">長いレコードは、新しい行を使用して、ラベルの必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-181">Records that are longer should use new lines for labels:</span></span>

```fsharp
let rainbow =
    { Boss = "Jeffrey"
      Lackeys = ["Zippy"; "George"; "Bungle"] }
```

<span data-ttu-id="4e7b5-182">開始トークンを同じ行で、新しい行に終了トークン配置することは問題もです。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-182">Placing the opening token on the same line and the closing token on a new line is also fine:</span></span>

```fsharp
let rainbow = {
    Boss1 = "Jeffrey"
    Boss2 = "Jeffrey"
    Boss3 = "Jeffrey"
    Boss4 = "Jeffrey"
    Boss5 = "Jeffrey"
    Boss6 = "Jeffrey"
    Boss7 = "Jeffrey"
    Boss8 = "Jeffrey"
    Lackeys = ["Zippy"; "George"; "Bungle"]
}
```

<span data-ttu-id="4e7b5-183">リストと配列の要素の場合と同じ規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-183">The same rules apply for list and array elements.</span></span>

## <a name="formatting-lists-and-arrays"></a><span data-ttu-id="4e7b5-184">書式設定のリストと配列</span><span class="sxs-lookup"><span data-stu-id="4e7b5-184">Formatting lists and arrays</span></span>

<span data-ttu-id="4e7b5-185">書き込み`x :: l`の前後のスペースで、`::`演算子 (`::`が空白で囲まれたため、挿入演算子) と`[1; 2; 3]`(`;`はその後にスペースを区切り記号) です。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-185">Write `x :: l` with spaces around the `::` operator (`::` is an infix operator, hence surrounded by spaces) and `[1; 2; 3]` (`;` is a delimiter, hence followed by a space).</span></span>

<span data-ttu-id="4e7b5-186">常に 2 つの個別の中かっこのような演算子の間に少なくとも 1 つの領域を使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-186">Always use at least one space between two distinct brace-like operators.</span></span> <span data-ttu-id="4e7b5-187">たとえば、間に空白のままに、`[`と`{`します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-187">For example, leave a space between a `[` and a `{`.</span></span>

```fsharp
// OK
[ { IngredientName = "Green beans"; Quantity = 250 }
  { IngredientName = "Pine nuts"; Quantity = 250 }
  { IngredientName = "Feta cheese"; Quantity = 250 }
  { IngredientName = "Olive oil"; Quantity = 10 }
  { IngredientName = "Lemon"; Quantity = 1 } ]

// Not OK
[{ IngredientName = "Green beans"; Quantity = 250 }
 { IngredientName = "Pine nuts"; Quantity = 250 }
 { IngredientName = "Feta cheese"; Quantity = 250 }
 { IngredientName = "Olive oil"; Quantity = 10 }
 { IngredientName = "Lemon"; Quantity = 1 }]
```

<span data-ttu-id="4e7b5-188">リストと複数行にわたって配列は、同様のルール、レコードと同様に従います。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-188">Lists and arrays that split across multiple lines follow a similar rule as records do:</span></span>

```fsharp
let pascalsTriangle = [|
    [|1|]
    [|1; 1|]
    [|1; 2; 1|]
    [|1; 3; 3; 1|]
    [|1; 4; 6; 4; 1|]
    [|1; 5; 10; 10; 5; 1|]
    [|1; 6; 15; 20; 15; 6; 1|]
    [|1; 7; 21; 35; 35; 21; 7; 1|]
    [|1; 8; 28; 56; 70; 56; 28; 8; 1|]
|]
```

## <a name="formatting-if-expressions"></a><span data-ttu-id="4e7b5-189">書式設定の if 式</span><span class="sxs-lookup"><span data-stu-id="4e7b5-189">Formatting if expressions</span></span>

<span data-ttu-id="4e7b5-190">条件文のインデントは、それらを構成する式のサイズによって異なります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-190">Indentation of conditionals depends on the sizes of the expressions that make them up.</span></span> <span data-ttu-id="4e7b5-191">場合`cond`、`e1`と`e2`短く、単純に 1 行に書き込むには。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-191">If `cond`, `e1` and `e2` are short, simply write them on one line:</span></span>

```fsharp
if cond then e1 else e2
```

<span data-ttu-id="4e7b5-192">いずれか`cond`、`e1`または`e2`は長くなりますが、複数行にありません。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-192">If either `cond`, `e1` or `e2` are longer, but not multi-line:</span></span>

```fsharp
if cond
then e1
else e2
```

<span data-ttu-id="4e7b5-193">複数行の式のいずれかの場合。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-193">If any of the expressions are multi-line:</span></span>

```fsharp
if cond then
    e1
else
    e2
```

<span data-ttu-id="4e7b5-194">複数の条件で`elif`と`else`と同じスコープでインデントは、 `if`:</span><span class="sxs-lookup"><span data-stu-id="4e7b5-194">Multiple conditionals with `elif` and `else` are indented at the same scope as the `if`:</span></span>

```fsharp
if cond1 then e1
elif cond2 then e2
elif cond3 then e3
else e4
```

### <a name="pattern-matching-constructs"></a><span data-ttu-id="4e7b5-195">パターン マッチング</span><span class="sxs-lookup"><span data-stu-id="4e7b5-195">Pattern matching constructs</span></span>

<span data-ttu-id="4e7b5-196">使用して、`|`インデントなしの一致の各句。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-196">Use a `|` for each clause of a match with no indentation.</span></span> <span data-ttu-id="4e7b5-197">式が短い場合は、各部分式が単純でもある場合は、1 行を使用を検討できます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-197">If the expression is short, you can consider using a single line if each subexpression is also simple.</span></span>

```fsharp
// OK
match l with
| { him = x; her = "Posh" } :: tail -> _
| _ :: tail -> findDavid tail
| [] -> failwith "Couldn't find David"

// Not OK
match l with
    | { him = x; her = "Posh" } :: tail -> _
    | _ :: tail -> findDavid tail
    | [] -> failwith "Couldn't find David"
```

<span data-ttu-id="4e7b5-198">パターン マッチングの矢印の右側の式が大きすぎる場合は、次の行のインデントが設定された 1 つの手順に移動、 `match` /`|`します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-198">If the expression on the right of the pattern matching arrow is too large, move it to the following line, indented one step from the `match`/`|`.</span></span>

```fsharp
match lam with
| Var v -> 1
| Abs(x, body) ->
    1 + sizeLambda body
| App(lam1, lam2) ->
    sizeLambda lam1 + sizeLambda lam2

```

<span data-ttu-id="4e7b5-199">パターン マッチングして以降、匿名関数の`function`、遠すぎていないインデントする必要があります一般にします。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-199">Pattern matching of anonymous functions, starting by `function`, should generally not indent too far.</span></span> <span data-ttu-id="4e7b5-200">たとえば、次のように 1 つのスコープをインデントも可能です。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-200">For example, indenting one scope as follows is fine:</span></span>

```fsharp
lambdaList
|> List.map (function
    | Abs(x, body) -> 1 + sizeLambda 0 body
    | App(lam1, lam2) -> sizeLambda (sizeLambda 0 lam1) lam2
    | Var v -> 1)
```

<span data-ttu-id="4e7b5-201">パターン マッチングで定義されている関数に`let`または`let rec`の開始後にインデントが設定された 4 つのスペースにする必要があります`let`場合でも、`function`キーワードの使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-201">Pattern matching in functions defined by `let` or `let rec` should be indented 4 spaces after starting of `let`, even if `function` keyword is used:</span></span>

```fsharp
let rec sizeLambda acc = function
    | Abs(x, body) -> sizeLambda (succ acc) body
    | App(lam1, lam2) -> sizeLambda (sizeLambda acc lam1) lam2
    | Var v -> succ acc
```

<span data-ttu-id="4e7b5-202">矢印の整列はお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-202">We do not recommend aligning arrows.</span></span>

## <a name="formatting-trywith-expressions"></a><span data-ttu-id="4e7b5-203">書式設定してみてください/式を</span><span class="sxs-lookup"><span data-stu-id="4e7b5-203">Formatting try/with expressions</span></span>

<span data-ttu-id="4e7b5-204">例外の種類に一致するパターンと同じレベルでインデントする`with`します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-204">Pattern matching on the exception type should be indented at the same level as `with`.</span></span>

```fsharp
try
    if System.DateTime.Now.Second % 3 = 0 then
        raise (new System.Exception())
    else
        raise (new System.ApplicationException())
with
| :? System.ApplicationException ->
    printfn "A second that was not a multiple of 3"
| _ ->
    printfn "A second that was a multiple of 3"
```

## <a name="formatting-function-parameter-application"></a><span data-ttu-id="4e7b5-205">関数パラメーターのアプリケーションを書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-205">Formatting function parameter application</span></span>

<span data-ttu-id="4e7b5-206">一般に、関数パラメーターのほとんどのアプリケーションは、同じ行に行われます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-206">In general, most function parameter application is done on the same line.</span></span>

<span data-ttu-id="4e7b5-207">新しい行に関数にパラメーターを適用する場合は、1 つのスコープでインデントします。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-207">If you wish to apply parameters to a function on a new line, indent them by one scope.</span></span>

```fsharp
// OK
sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
sprintf
     "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
let printVolumes x =
    printf "Volume in liters = %f, in us pints = %f, in imperial = %f"
        (convertVolumeToLiter x)
        (convertVolumeUSPint x)
        (convertVolumeImperialPint x)
```

<span data-ttu-id="4e7b5-208">関数の引数としてラムダ式と同じガイドラインが適用されます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-208">The same guidelines apply for lambda expressions as function arguments.</span></span> <span data-ttu-id="4e7b5-209">ラムダ式の本体の本文には別の行を設定できる場合は、1 つのスコープでインデント</span><span class="sxs-lookup"><span data-stu-id="4e7b5-209">If the body of a lambda expression, the body can have another line, indented by one scope</span></span>

```fsharp
let printListWithOffset a list1 =
    List.iter
        (fun elem -> printfn "%d" (a + elem))
        list1

// OK if lambda body is long enough
let printListWithOffset a list1 =
    List.iter
        (fun elem ->
            printfn "%d" (a + elem))
        list1
```

<span data-ttu-id="4e7b5-210">ただし、ラムダ式の本体が 1 つ以上の行の場合は、別の関数にファクタリング アウトを検討してくださいではなく 1 つの引数として関数に適用される複数行の構築します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-210">However, if the body of a lambda expression is more than one line, consider factoring it out into a separate function rather than have a multi-line construct applied as a single argument to a function.</span></span>

### <a name="formatting-infix-operators"></a><span data-ttu-id="4e7b5-211">挿入演算子を書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-211">Formatting infix operators</span></span>

<span data-ttu-id="4e7b5-212">スペースで別の演算子。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-212">Separate operators by spaces.</span></span> <span data-ttu-id="4e7b5-213">このルールの明確な例外は、`!`と`.`演算子。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-213">Obvious exceptions to this rule are the `!` and `.` operators.</span></span>

<span data-ttu-id="4e7b5-214">挿入辞の式では、[ok] を同じ列に編成します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-214">Infix expressions are OK to lineup on same column:</span></span>

```fsharp
acc +
(sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity)

let function1 arg1 arg2 arg3 arg4 =
    arg1 + arg2 +
    arg3 + arg4
```

### <a name="formatting-pipeline-operators"></a><span data-ttu-id="4e7b5-215">パイプライン演算子を書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-215">Formatting pipeline operators</span></span>

<span data-ttu-id="4e7b5-216">パイプライン`|>`演算子は、上で動作する式の下に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-216">Pipeline `|>` operators should go underneath the expressions they operate on.</span></span>

```fsharp
// Preferred approach
let methods2 =
    System.AppDomain.CurrentDomain.GetAssemblies()
    |> List.ofArray
    |> List.map (fun assm -> assm.GetTypes())
    |> Array.concat
    |> List.ofArray
    |> List.map (fun t -> t.GetMethods())
    |> Array.concat

// Not OK
let methods2 = System.AppDomain.CurrentDomain.GetAssemblies()
            |> List.ofArray
            |> List.map (fun assm -> assm.GetTypes())
            |> Array.concat
            |> List.ofArray
            |> List.map (fun t -> t.GetMethods())
            |> Array.concat
```

### <a name="formatting-modules"></a><span data-ttu-id="4e7b5-217">モジュールの書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-217">Formatting modules</span></span>

<span data-ttu-id="4e7b5-218">モジュールの基準としたローカル モジュール内のコードのインデントを設定する必要がありますが、最上位レベルのモジュール内のコードはインデントされませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-218">Code in a local module must be indented relative to the module, but code in a top-level module should not be indented.</span></span> <span data-ttu-id="4e7b5-219">Namespace 要素は、インデントを設定するのにはありません。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-219">Namespace elements do not have to be indented.</span></span>

```fsharp
// A is a top-level module.
module A

let function1 a b = a - b * b
```

```fsharp
// A1 and A2 are local modules.
module A1 =
    let function1 a b = a*a + b*b

module A2 =
    let function2 a b = a*a - b*b
```

### <a name="formatting-object-expressions-and-interfaces"></a><span data-ttu-id="4e7b5-220">オブジェクトの式とインターフェイスの書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-220">Formatting object expressions and interfaces</span></span>

<span data-ttu-id="4e7b5-221">同じ方法では、オブジェクトの式とインターフェイスを配置する必要があります`member`される 4 つのスペース後の分だけインデントされます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-221">Object expressions and interfaces should be aligned in the same way with `member` being indented after 4 spaces.</span></span>

```fsharp
let comparer =
    { new IComparer<string> with
          member x.Compare(s1, s2) =
              let rev (s : String) =
                  new String (Array.rev (s.ToCharArray()))
              let reversed = rev s1
              reversed.CompareTo (rev s2) }
```

### <a name="formatting-white-space-in-expressions"></a><span data-ttu-id="4e7b5-222">式内の空白の書式設定</span><span class="sxs-lookup"><span data-stu-id="4e7b5-222">Formatting white space in expressions</span></span>

<span data-ttu-id="4e7b5-223">F# の式で余分な空白文字を避けてください。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-223">Avoid extraneous white space in F# expressions.</span></span>

```fsharp
// OK
spam (ham.[1])

// Not OK
spam ( ham.[ 1 ] )
```

<span data-ttu-id="4e7b5-224">名前付き引数も必要はありません領域を囲む、 `=`:</span><span class="sxs-lookup"><span data-stu-id="4e7b5-224">Named arguments should also not have space surrounding the `=`:</span></span>

```fsharp
// OK
let makeStreamReader x = new System.IO.StreamReader(path=x)

// Not OK
let makeStreamReader x = new System.IO.StreamReader(path = x)
```
