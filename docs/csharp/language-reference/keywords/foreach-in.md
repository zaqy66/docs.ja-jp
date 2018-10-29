---
title: C# foreach ステートメント
ms.date: 06/29/2018
f1_keywords:
- foreach
- foreach_CSharpKeyword
helpviewer_keywords:
- foreach keyword [C#]
- foreach statement [C#]
- in keyword [C#]
ms.assetid: 5a9c5ddc-5fd3-457a-9bb6-9abffcd874ec
ms.openlocfilehash: 675e6b7fa925fe1822c2fc321d79afd13b5e4c51
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2018
ms.locfileid: "49347684"
---
# <a name="foreach-in-c-reference"></a><span data-ttu-id="da3b7-102">foreach、in (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="da3b7-102">foreach, in (C# reference)</span></span>

<span data-ttu-id="da3b7-103">`foreach` ステートメントは、<xref:System.Collections.IEnumerable?displayProperty=nameWithType> または <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> インターフェイスを実装している型のインスタンス内の要素ごとに、ステートメントまたはステートメントのブロックを実行します。</span><span class="sxs-lookup"><span data-stu-id="da3b7-103">The `foreach` statement executes a statement or a block of statements for each element in an instance of the type that implements the <xref:System.Collections.IEnumerable?displayProperty=nameWithType> or <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> interface.</span></span> <span data-ttu-id="da3b7-104">`foreach` ステートメントはこのような型にのみ限定されるものではありません。次の条件を満たす任意の型のインスタンスに適用できます。</span><span class="sxs-lookup"><span data-stu-id="da3b7-104">The `foreach` statement is not limited to those types and can be applied to an instance of any type that satisfies the following conditions:</span></span>

- <span data-ttu-id="da3b7-105">戻り値の型がクラス、構造体、インターフェイス型のいずれかである、パラメーターなしのパブリック メソッド `GetEnumerator` を持っている。</span><span class="sxs-lookup"><span data-stu-id="da3b7-105">has the public parameterless `GetEnumerator` method whose return type is either class, struct, or interface type,</span></span>
- <span data-ttu-id="da3b7-106">`GetEnumerator` メソッドの戻り値の型が、パブリック プロパティ `Current` と、戻り値の型が <xref:System.Boolean> であるパラメーターなしのパブリック メソッド `MoveNext` を持っている。</span><span class="sxs-lookup"><span data-stu-id="da3b7-106">the return type of the `GetEnumerator` method has the public `Current` property and the public parameterless `MoveNext` method whose return type is <xref:System.Boolean>.</span></span>

<span data-ttu-id="da3b7-107">`foreach` ステートメント ブロック内の任意の位置で、[break](break.md) ステートメントを使ってループから抜けることができます。または、[continue](continue.md) ステートメントを使って、ループ内の次の繰り返しにスキップできます。</span><span class="sxs-lookup"><span data-stu-id="da3b7-107">At any point within the `foreach` statement block, you can break out of the loop by using the [break](break.md) statement, or step to the next iteration in the loop by using the [continue](continue.md) statement.</span></span> <span data-ttu-id="da3b7-108">また、[goto](goto.md)、[return](return.md)、[throw](throw.md) ステートメントのいずれかを使って `foreach` ループを終了することもできます。</span><span class="sxs-lookup"><span data-stu-id="da3b7-108">You also can exit a `foreach` loop by the [goto](goto.md), [return](return.md), or [throw](throw.md) statements.</span></span>

## <a name="examples"></a><span data-ttu-id="da3b7-109">使用例</span><span class="sxs-lookup"><span data-stu-id="da3b7-109">Examples</span></span>

[!INCLUDE[interactive-note](~/includes/csharp-interactive-note.md)]

<span data-ttu-id="da3b7-110">次の例では、<xref:System.Collections.Generic.IEnumerable%601> インターフェイスを実装する <xref:System.Collections.Generic.List%601> 型のインスタンスを使用して、`foreach` ステートメントの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="da3b7-110">The following example shows usage of the `foreach` statement with an instance of the <xref:System.Collections.Generic.List%601> type that implements the <xref:System.Collections.Generic.IEnumerable%601> interface:</span></span>

[!code-csharp-interactive[list example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#1)]

<span data-ttu-id="da3b7-111">次の例では、何のインターフェイスも実装していない <xref:System.Span%601?displayProperty=nameWithType> 型のインスタンスを使用して、`foreach` ステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="da3b7-111">The next example uses the `foreach` statement with an instance of the <xref:System.Span%601?displayProperty=nameWithType> type, which doesn't implement any interfaces:</span></span>

[!code-csharp-interactive[span example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#2)]

<span data-ttu-id="da3b7-112">C# 7.3 以降、列挙子の `Current` プロパティが、[参照戻り値](../../programming-guide/classes-and-structs/ref-returns.md) (`ref T``T` はコレクション要素の種類です) を返す場合、`ref` または `ref readonly` 修飾子を使用して繰り返し変数を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="da3b7-112">Beginning with C# 7.3, if the enumerator's `Current` property returns a [reference return value](../../programming-guide/classes-and-structs/ref-returns.md) (`ref T` where `T` is the type of the collection element), you can declare the iteration variable with the `ref` or `ref readonly` modifier.</span></span> <span data-ttu-id="da3b7-113">次の例では、stackalloc 配列内の各項目の値を設定するために、`ref` 繰り返し変数を使用します。</span><span class="sxs-lookup"><span data-stu-id="da3b7-113">The following example uses a `ref` iteration variable to set the value of each item in a stackalloc array.</span></span> <span data-ttu-id="da3b7-114">`ref readonly` バージョンは、すべての値を出力するコレクションを反復処理します。</span><span class="sxs-lookup"><span data-stu-id="da3b7-114">The `ref readonly` version iterates the collection to print all the values.</span></span> <span data-ttu-id="da3b7-115">`readonly` 宣言では、暗黙のローカル変数宣言を使用します。</span><span class="sxs-lookup"><span data-stu-id="da3b7-115">The `readonly` declaration uses an implicit local variable declaration.</span></span> <span data-ttu-id="da3b7-116">暗黙の変数宣言は、`ref` または `ref readonly` 宣言で使用でき、変数の宣言を明示的に型指定できます。</span><span class="sxs-lookup"><span data-stu-id="da3b7-116">Implicit variable declarations can be used with either `ref` or `ref readonly` declarations, as can explicitly typed variable declarations.</span></span>

[!code-csharp-interactive[ref span example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#RefSpan)]

## <a name="c-language-specification"></a><span data-ttu-id="da3b7-117">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="da3b7-117">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="da3b7-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="da3b7-118">See also</span></span>

- [<span data-ttu-id="da3b7-119">foreach ステートメント (C# 言語仕様)</span><span class="sxs-lookup"><span data-stu-id="da3b7-119">The foreach statement (C# language specification)</span></span>](~/_csharplang/spec/statements.md#the-foreach-statement)
- [<span data-ttu-id="da3b7-120">配列での foreach の使用</span><span class="sxs-lookup"><span data-stu-id="da3b7-120">Using foreach with Arrays</span></span>](../../programming-guide/arrays/using-foreach-with-arrays.md)
- [<span data-ttu-id="da3b7-121">for</span><span class="sxs-lookup"><span data-stu-id="da3b7-121">for</span></span>](for.md)
- [<span data-ttu-id="da3b7-122">繰り返しステートメント</span><span class="sxs-lookup"><span data-stu-id="da3b7-122">Iteration Statements</span></span>](iteration-statements.md)
- [<span data-ttu-id="da3b7-123">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="da3b7-123">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="da3b7-124">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="da3b7-124">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="da3b7-125">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="da3b7-125">C# Programming Guide</span></span>](../../programming-guide/index.md)
