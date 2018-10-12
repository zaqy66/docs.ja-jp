---
title: C# 7.2 の新機能
description: C# 7.2 の新機能の概要。
ms.date: 08/16/2017
ms.openlocfilehash: 87fd67b37a31a02960334a2b2a325724e0cc2c73
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2018
ms.locfileid: "47400804"
---
# <a name="whats-new-in-c-72"></a><span data-ttu-id="72201-103">C# 7.2 の新機能</span><span class="sxs-lookup"><span data-stu-id="72201-103">What's new in C# 7.2</span></span>

<span data-ttu-id="72201-104">C# 7.2 は、便利な機能が多数追加された、もう 1 つのポイント リリースです。</span><span class="sxs-lookup"><span data-stu-id="72201-104">C# 7.2 is another point release that adds a number of useful features.</span></span>
<span data-ttu-id="72201-105">このリリースのテーマの 1 つは、不要なコピーや割り当てを回避して、さまざまな値の型の操作をより効率的に行うことです。</span><span class="sxs-lookup"><span data-stu-id="72201-105">One theme for this release is working more efficiently with value types by avoiding unnecessary copies or allocations.</span></span> 

<span data-ttu-id="72201-106">他の機能も、小さくても、あると助かる機能です。</span><span class="sxs-lookup"><span data-stu-id="72201-106">The remaining features are small, nice-to-have features.</span></span>

<span data-ttu-id="72201-107">C# 7.2 では[言語バージョンの選択](../language-reference/configure-language-version.md)の構成要素を使用して、コンパイラ言語バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="72201-107">C# 7.2 uses the [language version selection](../language-reference/configure-language-version.md) configuration element to select the compiler language version.</span></span>

<span data-ttu-id="72201-108">このリリースの新しい言語機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="72201-108">The new language features in this release are:</span></span>

* [<span data-ttu-id="72201-109">値の型による参照セマンティクス</span><span class="sxs-lookup"><span data-stu-id="72201-109">Reference semantics with value types</span></span>](#reference-semantics-with-value-types)
  - <span data-ttu-id="72201-110">参照セマンティクスを使用したさまざまな値の型の使用を有効にする、構文の機能強化の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="72201-110">A combination of syntax improvements that enable working with value types using reference semantics.</span></span>
* [<span data-ttu-id="72201-111">末尾以外の名前付き引数</span><span class="sxs-lookup"><span data-stu-id="72201-111">Non-trailing named arguments</span></span>](#non-trailing-named-arguments)
  - <span data-ttu-id="72201-112">名前付き引数の後ろに位置引数を続けることができます。</span><span class="sxs-lookup"><span data-stu-id="72201-112">Named arguments can be followed by positional arguments.</span></span>
* [<span data-ttu-id="72201-113">数値リテラルでの先頭のアンダースコア (_)</span><span class="sxs-lookup"><span data-stu-id="72201-113">Leading underscores in numeric literals</span></span>](#leading-underscores-in-numeric-literals)
  - <span data-ttu-id="72201-114">数値リテラルの印刷桁の前に先頭のアンダースコア(_) を含めることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="72201-114">Numeric literals can now have leading underscores before any printed digits.</span></span>
* [<span data-ttu-id="72201-115">`private protected` アクセス修飾子</span><span class="sxs-lookup"><span data-stu-id="72201-115">`private protected` access modifier</span></span>](#private-protected-access-modifier)
  - <span data-ttu-id="72201-116">`private protected` アクセス修飾子によって、同じアセンブリ内の派生クラスのアクセスが有効になります。</span><span class="sxs-lookup"><span data-stu-id="72201-116">The `private protected` access modifier enables access for derived classes in the same assembly.</span></span>

## <a name="reference-semantics-with-value-types"></a><span data-ttu-id="72201-117">値の型による参照セマンティクス</span><span class="sxs-lookup"><span data-stu-id="72201-117">Reference semantics with value types</span></span>

<span data-ttu-id="72201-118">7.2 で導入された言語機能では、参照セマンティクスを使用しているときに、さまざまな値の型を使用できます。</span><span class="sxs-lookup"><span data-stu-id="72201-118">Language features introduced in 7.2 let you work with value types while using reference semantics.</span></span> <span data-ttu-id="72201-119">これらは、参照型の使用に関連するメモリの割り当てを生じさせずに、値の型のコピーを最小限に抑えてパフォーマンスを改善するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="72201-119">They are designed to increase performance by minimizing copying value types without incurring the memory allocations associated with using reference types.</span></span> <span data-ttu-id="72201-120">次のような機能があります。</span><span class="sxs-lookup"><span data-stu-id="72201-120">The features include:</span></span>

 - <span data-ttu-id="72201-121">パラメーターの `in` 修飾子。引数が参照によって渡されるが、呼び出されたメソッドでは変更されないことを指定します。</span><span class="sxs-lookup"><span data-stu-id="72201-121">The `in` modifier on parameters, to specify that an argument is passed by reference but not modified by the called method.</span></span> <span data-ttu-id="72201-122">引数に `in` 修飾子を加えることは、[ソース互換性がある変更](version-update-considerations.md#source-compatible-changes)です。</span><span class="sxs-lookup"><span data-stu-id="72201-122">Adding the `in` modifier to an argument is a [source compatible change](version-update-considerations.md#source-compatible-changes).</span></span>
 - <span data-ttu-id="72201-123">メソッド戻りの `ref readonly` 修飾子。メソッドが参照によってその値を戻しますが、そのオブジェクトに対する書き込みを許可しないことを指定します。</span><span class="sxs-lookup"><span data-stu-id="72201-123">The `ref readonly` modifier on method returns, to indicate that a method returns its value by reference but doesn't allow writes to that object.</span></span> <span data-ttu-id="72201-124">戻り値が値に割り当てられている場合、`ref readonly` 修飾子を追加することは、[ソース互換性がある変更](version-update-considerations.md#source-compatible-changes)です。</span><span class="sxs-lookup"><span data-stu-id="72201-124">Adding the `ref readonly` modifier is a [source compatible change](version-update-considerations.md#source-compatible-changes), if the return is assigned to a value.</span></span> <span data-ttu-id="72201-125">既存の `ref` return ステートメントに `readonly` 修飾子を追加することは、[互換性がない変更](version-update-considerations.md#incompatible-changes)です。</span><span class="sxs-lookup"><span data-stu-id="72201-125">Adding the `readonly` modifer to an existing `ref` return statement is an [incompatible change](version-update-considerations.md#incompatible-changes).</span></span> <span data-ttu-id="72201-126">呼び出し元は、`readonly` 修飾子を含むように `ref` ローカル変数の宣言を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72201-126">It requires callers to update the declaration of `ref` local variables to include the `readonly` modifier.</span></span>
 - <span data-ttu-id="72201-127">`readonly struct` 宣言。変更不可の構造体で、そのメンバー メソッドの `in` パラメーターとして渡す必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="72201-127">The `readonly struct` declaration, to indicate that a struct is immutable and should be passed as an `in` parameter to its member methods.</span></span> <span data-ttu-id="72201-128">既存の構造体の宣言に `readonly` 修飾子を追加することは、[バイナリ互換性がある変更](version-update-considerations.md#binary-compatible-changes)です。</span><span class="sxs-lookup"><span data-stu-id="72201-128">Adding the `readonly` modifier to an existing struct declaration is a [binary compatible change](version-update-considerations.md#binary-compatible-changes).</span></span>
 - <span data-ttu-id="72201-129">`ref struct` 宣言。構造体型がマネージド メモリに直接アクセスし、常にスタック割り当てが必要であることを示します。</span><span class="sxs-lookup"><span data-stu-id="72201-129">The `ref struct` declaration, to indicate that a struct type accesses managed memory directly and must always be stack allocated.</span></span> <span data-ttu-id="72201-130">既存の `struct` の宣言に `ref` 修飾子を追加することは、[互換性がない変更](version-update-considerations.md#incompatible-changes)です。</span><span class="sxs-lookup"><span data-stu-id="72201-130">Adding the `ref` modifier to an existing `struct` declaration is an [incompatible change](version-update-considerations.md#incompatible-changes).</span></span> <span data-ttu-id="72201-131">`ref struct` をクラスのメンバーにすることはできません。また、ヒープ上に割り当てられている可能性がある他の場所で使用することもできません。</span><span class="sxs-lookup"><span data-stu-id="72201-131">A `ref struct` cannot be a member of a class or used in other locations where it may be allocated on the heap.</span></span>

<span data-ttu-id="72201-132">これらすべての変更の詳細については、[参照セマンティクスを持つ値の型の使用](../reference-semantics-with-value-types.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72201-132">You can read more about all these changes in [Using value types with reference semantics](../reference-semantics-with-value-types.md).</span></span>

## <a name="non-trailing-named-arguments"></a><span data-ttu-id="72201-133">末尾以外の名前付き引数</span><span class="sxs-lookup"><span data-stu-id="72201-133">Non-trailing named arguments</span></span>

<span data-ttu-id="72201-134">メソッド呼び出しで、位置引数の前に名前付き引数を使用できるようになりました。ただし、そのような名前付き引数が正しい位置にある場合です。</span><span class="sxs-lookup"><span data-stu-id="72201-134">Method calls may now use named arguments that precede positional arguments when those named arguments are in the correct positions.</span></span> <span data-ttu-id="72201-135">詳細については、「[名前付き引数と省略可能な引数](../programming-guide/classes-and-structs/named-and-optional-arguments.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72201-135">For more information see [Named and optional arguments](../programming-guide/classes-and-structs/named-and-optional-arguments.md).</span></span>

## <a name="leading-underscores-in-numeric-literals"></a><span data-ttu-id="72201-136">数値リテラルでの先頭のアンダースコア (_)</span><span class="sxs-lookup"><span data-stu-id="72201-136">Leading underscores in numeric literals</span></span>

<span data-ttu-id="72201-137">C# 7.0 の桁区切り記号のサポートの実装では、`_` をリテラル値の最初の文字にすることができませんでした。</span><span class="sxs-lookup"><span data-stu-id="72201-137">The implementation of support for digit separators in C# 7.0 didn't allow the `_` to be the first character of the literal value.</span></span> <span data-ttu-id="72201-138">16 進とバイナリの数値リテラルの先頭に `_` を使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="72201-138">Hex and binary numeric literals may now begin with an `_`.</span></span> 

<span data-ttu-id="72201-139">例:</span><span class="sxs-lookup"><span data-stu-id="72201-139">For example:</span></span>

```csharp
int binaryValue = 0b_0101_0101;
```

## <a name="private-protected-access-modifier"></a><span data-ttu-id="72201-140">_private protected_ アクセス修飾子</span><span class="sxs-lookup"><span data-stu-id="72201-140">_private protected_ access modifier</span></span>

<span data-ttu-id="72201-141">最後に、新しい複合アクセス修飾子: `private protected` は、同じアセンブリで宣言されているクラスまたは派生クラスを含むことでメンバーにアクセスできることを示しています。</span><span class="sxs-lookup"><span data-stu-id="72201-141">Finally, a new compound access modifier: `private protected` indicates that a member may be accessed by containing class or derived classes that are declared in the same assembly.</span></span> <span data-ttu-id="72201-142">`protected internal` は同じアセンブリの派生クラスまたはクラスによるアクセスを許可していますが、`private protected` は同じアセンブリで宣言された派生型へのアクセスを制限しています。</span><span class="sxs-lookup"><span data-stu-id="72201-142">While `protected internal` allows access by derived classes or classes that are in the same assembly, `private protected` limits access to derived types declared in the same assembly.</span></span>

<span data-ttu-id="72201-143">詳細については、言語リファレンスの[アクセス修飾子](../language-reference/keywords/access-modifiers.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72201-143">For more information see [access modifiers](../language-reference/keywords/access-modifiers.md) in the language reference.</span></span>
