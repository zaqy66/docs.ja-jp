---
title: C# の for ステートメント
ms.date: 06/13/2018
f1_keywords:
- for
- for_CSharpKeyword
helpviewer_keywords:
- for keyword [C#]
ms.assetid: 34041a40-2c87-467a-9ffb-a0417d8f67a8
ms.openlocfilehash: c6ef926d6fb2c79b7b7f71c3b24b86a7ab057c88
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43511729"
---
# <a name="for-c-reference"></a><span data-ttu-id="102b7-102">for (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="102b7-102">for (C# reference)</span></span>

<span data-ttu-id="102b7-103">`for` ステートメントでは、指定されたブール式が `true` と評価される間に、ステートメントまたはステートメント ブロックが実行されます。</span><span class="sxs-lookup"><span data-stu-id="102b7-103">The `for` statement executes a statement or a block of statements while a specified boolean expression evaluates to `true`.</span></span>

<span data-ttu-id="102b7-104">`for` ステートメント ブロック内の任意の位置で、[break](break.md) ステートメントを使ってループから抜けることができます。または、[continue](continue.md) ステートメントを使って、ループ内の次の繰り返しにスキップできます。</span><span class="sxs-lookup"><span data-stu-id="102b7-104">At any point within the `for` statement block, you can break out of the loop by using the [break](break.md) statement, or step to the next iteration in the loop by using the [continue](continue.md) statement.</span></span> <span data-ttu-id="102b7-105">また、[goto](goto.md)、[return](return.md)、[throw](throw.md) ステートメントのいずれかを使って `for` ループを終了することもできます。</span><span class="sxs-lookup"><span data-stu-id="102b7-105">You also can exit a `for` loop by the [goto](goto.md), [return](return.md), or [throw](throw.md) statements.</span></span>

## <a name="structure-of-the-for-statement"></a><span data-ttu-id="102b7-106">`for` ステートメントの構造</span><span class="sxs-lookup"><span data-stu-id="102b7-106">Structure of the `for` statement</span></span>

<span data-ttu-id="102b7-107">`for` ステートメントには、*initializer*、*condition*、*iterator* のセクションが定義されています。</span><span class="sxs-lookup"><span data-stu-id="102b7-107">The `for` statement defines *initializer*, *condition*, and *iterator* sections:</span></span>

```csharp
for (initializer; condition; iterator)
    body
```

<span data-ttu-id="102b7-108">3 つのセクションはすべて省略可能です。</span><span class="sxs-lookup"><span data-stu-id="102b7-108">All three sections are optional.</span></span> <span data-ttu-id="102b7-109">ループの本体は、ステートメントまたはステートメントのブロックのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="102b7-109">The body of the loop is either a statement or a block of statements.</span></span>

<span data-ttu-id="102b7-110">次の例では、`for` ステートメントと定義されているすべてのセクションが示されています。</span><span class="sxs-lookup"><span data-stu-id="102b7-110">The following example shows the `for` statement with all of the sections defined:</span></span>

[!code-csharp-interactive[for loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#5)]

### <a name="the-initializer-section"></a><span data-ttu-id="102b7-111">*initializer* セクション</span><span class="sxs-lookup"><span data-stu-id="102b7-111">The *initializer* section</span></span>

<span data-ttu-id="102b7-112">*initializer* セクション内のステートメントは、ループに入る前に 1 回だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="102b7-112">The statements in the *initializer* section are executed only once, before entering the loop.</span></span> <span data-ttu-id="102b7-113">*initializer* セクションは、次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="102b7-113">The *initializer* section is either of the following:</span></span>

- <span data-ttu-id="102b7-114">ローカル ループ変数の宣言と初期化。ループの外からアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="102b7-114">The declaration and initialization of a local loop variable, which can't be accessed from outside the loop.</span></span>

- <span data-ttu-id="102b7-115">次に列挙した 0 個以上のステートメント式 (コンマ区切り)。</span><span class="sxs-lookup"><span data-stu-id="102b7-115">Zero or more statement expressions from the following list, separated by commas:</span></span>

  - <span data-ttu-id="102b7-116">[代入](../operators/assignment-operator.md)ステートメント</span><span class="sxs-lookup"><span data-stu-id="102b7-116">[assignment](../operators/assignment-operator.md) statement</span></span>

  - <span data-ttu-id="102b7-117">メソッドの呼び出し</span><span class="sxs-lookup"><span data-stu-id="102b7-117">invocation of a method</span></span>

  - <span data-ttu-id="102b7-118">前置または後置の[インクリメント](../operators/increment-operator.md)式 (`++i`、`i++` など)</span><span class="sxs-lookup"><span data-stu-id="102b7-118">prefix or postfix [increment](../operators/increment-operator.md) expression, such as `++i` or `i++`</span></span>

  - <span data-ttu-id="102b7-119">前置または後置の[デクリメント](../operators/decrement-operator.md)式 (`--i`、`i--` など)</span><span class="sxs-lookup"><span data-stu-id="102b7-119">prefix or postfix [decrement](../operators/decrement-operator.md) expression, such as `--i` or `i--`</span></span>

  - <span data-ttu-id="102b7-120">[new](new-operator.md) キーワードを使用したオブジェクト作成</span><span class="sxs-lookup"><span data-stu-id="102b7-120">creation of an object by using [new](new-operator.md) keyword</span></span>

  - <span data-ttu-id="102b7-121">[await](await.md) 式</span><span class="sxs-lookup"><span data-stu-id="102b7-121">[await](await.md) expression</span></span>

<span data-ttu-id="102b7-122">上記の例の *initializer* セクションは、ローカル ループ変数 `i` を宣言して初期化します。</span><span class="sxs-lookup"><span data-stu-id="102b7-122">The *initializer* section in the example above declares and initializes the local loop variable `i`:</span></span>

```csharp
int i = 0
```

### <a name="the-condition-section"></a><span data-ttu-id="102b7-123">*condition* セクション</span><span class="sxs-lookup"><span data-stu-id="102b7-123">The *condition* section</span></span>

<span data-ttu-id="102b7-124">*condition* セクション (ある場合) は、ブール式にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="102b7-124">The *condition* section, if present, must be a boolean expression.</span></span> <span data-ttu-id="102b7-125">その式はループの反復の前に毎回評価されます。</span><span class="sxs-lookup"><span data-stu-id="102b7-125">That expression is evaluated before every loop iteration.</span></span> <span data-ttu-id="102b7-126">*condition* セクションが存在しないか、ブール式が `true` に評価される場合、次のループの反復が実行されます。そうでない場合は、ループが終了します。</span><span class="sxs-lookup"><span data-stu-id="102b7-126">If the *condition* section is not present or the boolean expression evaluates to `true`, the next loop iteration is executed; otherwise, the loop is exited.</span></span>

<span data-ttu-id="102b7-127">上記の例の*condition* セクションでは、ローカル ループ変数の値に基づいて、ループが終了するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="102b7-127">The *condition* section in the example above determines if the loop terminates based on the value of the local loop variable:</span></span>

```csharp
i < 5
```

### <a name="the-iterator-section"></a><span data-ttu-id="102b7-128">*iterator* セクション</span><span class="sxs-lookup"><span data-stu-id="102b7-128">The *iterator* section</span></span>

<span data-ttu-id="102b7-129">ループ本体の反復処理が終わるたびに実行される処理を *iterator* セクションで定義します。</span><span class="sxs-lookup"><span data-stu-id="102b7-129">The *iterator* section defines what happens after each iteration of the body of the loop.</span></span> <span data-ttu-id="102b7-130">*iterator* セクションには、次のステートメント式を 0 個以上、コンマで区切って記述します。</span><span class="sxs-lookup"><span data-stu-id="102b7-130">The *iterator* section contains zero or more of the following statement expressions, separated by commas:</span></span>

- <span data-ttu-id="102b7-131">[代入](../operators/assignment-operator.md)ステートメント</span><span class="sxs-lookup"><span data-stu-id="102b7-131">[assignment](../operators/assignment-operator.md) statement</span></span>

- <span data-ttu-id="102b7-132">メソッドの呼び出し</span><span class="sxs-lookup"><span data-stu-id="102b7-132">invocation of a method</span></span>

- <span data-ttu-id="102b7-133">前置または後置の[インクリメント](../operators/increment-operator.md)式 (`++i`、`i++` など)</span><span class="sxs-lookup"><span data-stu-id="102b7-133">prefix or postfix [increment](../operators/increment-operator.md) expression, such as `++i` or `i++`</span></span>

- <span data-ttu-id="102b7-134">前置または後置の[デクリメント](../operators/decrement-operator.md)式 (`--i`、`i--` など)</span><span class="sxs-lookup"><span data-stu-id="102b7-134">prefix or postfix [decrement](../operators/decrement-operator.md) expression, such as `--i` or `i--`</span></span>

- <span data-ttu-id="102b7-135">[new](new-operator.md) キーワードを使用したオブジェクト作成</span><span class="sxs-lookup"><span data-stu-id="102b7-135">creation of an object by using [new](new-operator.md) keyword</span></span>

- <span data-ttu-id="102b7-136">[await](await.md) 式</span><span class="sxs-lookup"><span data-stu-id="102b7-136">[await](await.md) expression</span></span>

<span data-ttu-id="102b7-137">上記の例の *iterator* セクションでは、ローカルのループ変数をインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="102b7-137">The *iterator* section in the example above increments the local loop variable:</span></span>

```csharp
i++
```

## <a name="examples"></a><span data-ttu-id="102b7-138">使用例</span><span class="sxs-lookup"><span data-stu-id="102b7-138">Examples</span></span>

<span data-ttu-id="102b7-139">次の例は、`for` ステートメント セクションのやや特殊な使用例です。*initializer* セクションで外部ループ変数に値を代入し、*initializer* セクションと *iterator* セクションの両方でメソッドを呼び出しています。さらに、*iterator* セクションで 2 つの変数の値を変更しています。</span><span class="sxs-lookup"><span data-stu-id="102b7-139">The following example illustrates several less common usages of the `for` statement sections: assigning a value to an external loop variable in the *initializer* section, invoking a method in both the *initializer* and the *iterator* sections, and changing the values of two variables in the *iterator* section.</span></span> <span data-ttu-id="102b7-140">**[実行]** を選択して、コード例を実行します。</span><span class="sxs-lookup"><span data-stu-id="102b7-140">Select **Run** to run the example code.</span></span> <span data-ttu-id="102b7-141">その後に、コードを変更し、もう一度実行することができます。</span><span class="sxs-lookup"><span data-stu-id="102b7-141">After that you can modify the code and run it again.</span></span>

[!code-csharp-interactive[not typical for loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#6)]

<span data-ttu-id="102b7-142">次の例では、無限 `for` ループが定義されます。</span><span class="sxs-lookup"><span data-stu-id="102b7-142">The following example defines the infinite `for` loop:</span></span>

[!code-csharp[infinite for loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#7)]

## <a name="c-language-specification"></a><span data-ttu-id="102b7-143">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="102b7-143">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="102b7-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="102b7-144">See also</span></span>

- [<span data-ttu-id="102b7-145">for ステートメント (C# 言語仕様)</span><span class="sxs-lookup"><span data-stu-id="102b7-145">The for statement (C# language specification)</span></span>](/dotnet/csharp/language-reference/language-specification/statements#the-for-statement)
- [<span data-ttu-id="102b7-146">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="102b7-146">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="102b7-147">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="102b7-147">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="102b7-148">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="102b7-148">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="102b7-149">foreach、in</span><span class="sxs-lookup"><span data-stu-id="102b7-149">foreach, in</span></span>](foreach-in.md)
- [<span data-ttu-id="102b7-150">for ステートメント (C++)</span><span class="sxs-lookup"><span data-stu-id="102b7-150">for Statement (C++)</span></span>](/cpp/cpp/for-statement-cpp)
- [<span data-ttu-id="102b7-151">繰り返しステートメント</span><span class="sxs-lookup"><span data-stu-id="102b7-151">Iteration Statements</span></span>](iteration-statements.md)
