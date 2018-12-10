---
title: 単体テストを記述するためのベスト プラクティス
description: コードの品質と回復性を向上させる単体テストを記述するためのベスト プラクティスについて説明します
author: jpreese
ms.author: wiwagn
ms.date: 07/28/2018
ms.openlocfilehash: 00a0b999c9a08b04cb33bcb3a332513292beb363
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53143414"
---
# <a name="unit-testing-best-practices"></a><span data-ttu-id="3c542-103">単体テストのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="3c542-103">Unit testing best practices</span></span>

<span data-ttu-id="3c542-104">著者: [John Reese](http://reesespieces.io)、協力者: [Roy Osherove](http://osherove.com/)</span><span class="sxs-lookup"><span data-stu-id="3c542-104">By [John Reese](http://reesespieces.io) with special thanks to [Roy Osherove](http://osherove.com/)</span></span>

<span data-ttu-id="3c542-105">単体テストの記述には多大な利点があります。回帰の防止に役立ち、ドキュメントを提供して、優れた設計を容易に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3c542-105">There are numerous benefits to writing unit tests; they help with regression, provide documentation, and facilitate good design.</span></span> <span data-ttu-id="3c542-106">ただし、読みにくくて不安定な単体テストは、コード ベースに打撃を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-106">However, hard to read and brittle unit tests can wreak havoc on your code base.</span></span>

<span data-ttu-id="3c542-107">このガイドでは、テストの回復性とわかりやすさを維持するよう単体テストを記述する際のいくつかのベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3c542-107">In this guide, you'll learn some best practices when writing unit tests to keep your tests resilient and easy to understand.</span></span>

## <a name="why-unit-test"></a><span data-ttu-id="3c542-108">単体テストを記述する理由</span><span class="sxs-lookup"><span data-stu-id="3c542-108">Why unit test?</span></span>

### <a name="less-time-performing-functional-tests"></a><span data-ttu-id="3c542-109">機能テストの実行時間を短縮</span><span class="sxs-lookup"><span data-stu-id="3c542-109">Less time performing functional tests</span></span>
<span data-ttu-id="3c542-110">機能テストはコストがかかります。</span><span class="sxs-lookup"><span data-stu-id="3c542-110">Functional tests are expensive.</span></span> <span data-ttu-id="3c542-111">通常、これらのテストでは、アプリケーションを開き、想定される動作を検証するためにお客様 (または他のだれか) が従う必要のある一連の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3c542-111">They typically involve opening up the application and performing a series of steps that you (or someone else), must follow in order to validate the expected behavior.</span></span> <span data-ttu-id="3c542-112">テスト担当者は、これらの手順を必ずしもが把握しているとは限りません。つまり、テストを実行するために、その領域に精通している他者に支援を求める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-112">These steps may not always be known to the tester, which means they will have to reach out to someone more knowledgeable in the area in order to carry out the test.</span></span> <span data-ttu-id="3c542-113">テスト自体は、小さな変更の場合は数秒かかり、大きな変更の場合は数分かかる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-113">Testing itself could take seconds for trivial changes, or minutes for larger changes.</span></span> <span data-ttu-id="3c542-114">最後に、システムで変更を行うたびにこのプロセスを繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-114">Lastly, this process must be repeated for every change that you make in the system.</span></span>

<span data-ttu-id="3c542-115">一方、単体テストは数ミリ秒しかかからず、ボタンを押すだけで実行でき、概してシステムの知識は必ずしも必要ありません。</span><span class="sxs-lookup"><span data-stu-id="3c542-115">Unit tests, on the other hand, take milliseconds, can be run at the press of a button and do not necessarily require any knowledge of the system at large.</span></span> <span data-ttu-id="3c542-116">テストに合格するか失敗するかは、個人ではなくテスト ランナーの責任となります。</span><span class="sxs-lookup"><span data-stu-id="3c542-116">Whether or not the test passes or fails is up to the test runner, not the individual.</span></span>

### <a name="protection-against-regression"></a><span data-ttu-id="3c542-117">回帰の防止</span><span class="sxs-lookup"><span data-stu-id="3c542-117">Protection against regression</span></span>
<span data-ttu-id="3c542-118">回帰問題は、アプリケーションに変更が行われると発生する欠陥です。</span><span class="sxs-lookup"><span data-stu-id="3c542-118">Regression defects are defects that are introduced when a change is made to the application.</span></span> <span data-ttu-id="3c542-119">一般的にテスト担当者は、新しい機能をテストするだけでなく、以前に実装されていた機能が今も想定どおりに機能していることを確認するために、事前に存在していた機能もテストします。</span><span class="sxs-lookup"><span data-stu-id="3c542-119">It is common for testers to not only test their new feature but also features that existed beforehand in order to verify that previously implemented features still function as expected.</span></span>

<span data-ttu-id="3c542-120">単体テストでは、ビルドを行うたびに、さらにはコード行を変更するたびに、テストのスイート全体を再実行できます。</span><span class="sxs-lookup"><span data-stu-id="3c542-120">With unit testing, it's possible to rerun your entire suite of tests after every build or even after you change a line of code.</span></span> <span data-ttu-id="3c542-121">これにより、新しいコードが既存の機能を損なわないことを確信できます。</span><span class="sxs-lookup"><span data-stu-id="3c542-121">Giving you confidence that your new code does not break existing functionality.</span></span>

### <a name="executable-documentation"></a><span data-ttu-id="3c542-122">実行可能なドキュメント</span><span class="sxs-lookup"><span data-stu-id="3c542-122">Executable documentation</span></span>
<span data-ttu-id="3c542-123">特定の入力によって、特定のメソッドが何を実行するか、またはそのメソッドがどのように動作するかは、必ずしも明らかではありません。</span><span class="sxs-lookup"><span data-stu-id="3c542-123">It may not always be obvious what a particular method does or how it behaves given a certain input.</span></span> <span data-ttu-id="3c542-124">空の文字列や Null を渡した場合にこのメソッドがどのように動作するか、自分自身わからないことが</span><span class="sxs-lookup"><span data-stu-id="3c542-124">You may ask yourself: How does this method behave if I pass it a blank string?</span></span> <span data-ttu-id="3c542-125">あります。</span><span class="sxs-lookup"><span data-stu-id="3c542-125">Null?</span></span>

<span data-ttu-id="3c542-126">適切な名前の単体テストのスイートがある場合、各テストは、特定の入力に対して想定される出力を明確に説明できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-126">When you have a suite of well-named unit tests, each test should be able to clearly explain the expected output for a given input.</span></span> <span data-ttu-id="3c542-127">さらに、実際に動作することを確認できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-127">In addition, it should be able to verify that it actually works.</span></span>

### <a name="less-coupled-code"></a><span data-ttu-id="3c542-128">疎結合コード</span><span class="sxs-lookup"><span data-stu-id="3c542-128">Less coupled code</span></span>
<span data-ttu-id="3c542-129">コードが密結合されている場合、単体テストは難しくなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-129">When code is tightly coupled, it can be difficult to unit test.</span></span> <span data-ttu-id="3c542-130">記述しているコードに対して単体テストを作成しないと、結合を明確に認識できません。</span><span class="sxs-lookup"><span data-stu-id="3c542-130">Without creating unit tests for the code that you're writing, coupling may be less apparent.</span></span>

<span data-ttu-id="3c542-131">したがって、コードに対するテストを記述する際には、必然的にコードを分離します。そうしないと、テストが困難になるからです。</span><span class="sxs-lookup"><span data-stu-id="3c542-131">Writing tests for your code will naturally decouple your code, because it would be more difficult to test otherwise.</span></span>

## <a name="characteristics-of-a-good-unit-test"></a><span data-ttu-id="3c542-132">適切な単体テストの特性</span><span class="sxs-lookup"><span data-stu-id="3c542-132">Characteristics of a good unit test</span></span>
- <span data-ttu-id="3c542-133">**高速**。</span><span class="sxs-lookup"><span data-stu-id="3c542-133">**Fast**.</span></span> <span data-ttu-id="3c542-134">完成度の高いプロジェクトに数千もの単体テストが含まれることは、珍しくありません。</span><span class="sxs-lookup"><span data-stu-id="3c542-134">It is not uncommon for mature projects to have thousands of unit tests.</span></span> <span data-ttu-id="3c542-135">単体テストの実行にかかる時間はごくわずかで、</span><span class="sxs-lookup"><span data-stu-id="3c542-135">Unit tests should take very little time to run.</span></span> <span data-ttu-id="3c542-136">数ミリ秒です。</span><span class="sxs-lookup"><span data-stu-id="3c542-136">Milliseconds.</span></span>
- <span data-ttu-id="3c542-137">**独立性**。</span><span class="sxs-lookup"><span data-stu-id="3c542-137">**Isolated**.</span></span> <span data-ttu-id="3c542-138">単体テストはスタンドアロンであり、独立して実行でき、ファイル システムやデータベースなどの外部要因に対する依存関係がありません。</span><span class="sxs-lookup"><span data-stu-id="3c542-138">Unit tests are standalone, can be run in isolation, and have no dependencies on any outside factors such as a file system or database.</span></span>
- <span data-ttu-id="3c542-139">**反復可能**。</span><span class="sxs-lookup"><span data-stu-id="3c542-139">**Repeatable**.</span></span> <span data-ttu-id="3c542-140">単体テストの実行では、その結果に一貫性がある必要があります。つまり、実行と実行の間で何も変更しない場合、常に同じ結果を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-140">Running a unit test should be consistent with its results, that is, it always returns the same result if you do not change anything in between runs.</span></span>
- <span data-ttu-id="3c542-141">**自己チェック**。</span><span class="sxs-lookup"><span data-stu-id="3c542-141">**Self-Checking**.</span></span> <span data-ttu-id="3c542-142">テストは人の介入なしに、合格したか失敗したかを自動的に検出できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-142">The test should be able to automatically detect if it passed or failed without any human interaction.</span></span>
- <span data-ttu-id="3c542-143">**タイムリー**。</span><span class="sxs-lookup"><span data-stu-id="3c542-143">**Timely**.</span></span> <span data-ttu-id="3c542-144">単体テストは、テスト対象のコードの記述と比較して時間がかかりすぎないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-144">A unit test should not take a disproportionally long time to write compared to the code being tested.</span></span> <span data-ttu-id="3c542-145">コードの記述と比較してコードのテストに時間がかかりすぎる場合は、よりテストしやすい設計を検討してください。</span><span class="sxs-lookup"><span data-stu-id="3c542-145">If you find testing the code taking a large amount of time compared to writing the code, consider a design that is more testable.</span></span>

## <a name="lets-speak-the-same-language"></a><span data-ttu-id="3c542-146">用語を統一する</span><span class="sxs-lookup"><span data-stu-id="3c542-146">Let's speak the same language</span></span>
<span data-ttu-id="3c542-147">テストに関して、*モック*という用語はよく誤用されます。</span><span class="sxs-lookup"><span data-stu-id="3c542-147">The term *mock* is unfortunately very misused when talking about testing.</span></span> <span data-ttu-id="3c542-148">単体テストの記述時における最も一般的な種類の*フェイク*の定義を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3c542-148">The following defines the most common types of *fakes* when writing unit tests:</span></span>

<span data-ttu-id="3c542-149">*フェイク* - フェイクは、スタブまたはモック オブジェクトのいずれかを示すのに使用できる汎用的な用語です。</span><span class="sxs-lookup"><span data-stu-id="3c542-149">*Fake* - A fake is a generic term which can be used to describe either a stub or a mock object.</span></span> <span data-ttu-id="3c542-150">スタブとモックのどちらであるかは、使用されているコンテキストによって決まります。</span><span class="sxs-lookup"><span data-stu-id="3c542-150">Whether it is a stub or a mock depends on the context in which it's used.</span></span> <span data-ttu-id="3c542-151">つまり、フェイクはスタブとモックのどちらにもなりえます。</span><span class="sxs-lookup"><span data-stu-id="3c542-151">So in other words, a fake can be a stub or a mock.</span></span>

<span data-ttu-id="3c542-152">*モック* - モック オブジェクトは、単体テストに合格したか失敗したかを判断する、システム内のフェイク オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="3c542-152">*Mock* - A mock object is a fake object in the system that decides whether or not a unit test has passed or failed.</span></span> <span data-ttu-id="3c542-153">モックは、アサートされるまでフェイクとして開始します。</span><span class="sxs-lookup"><span data-stu-id="3c542-153">A mock starts out as a Fake until it is asserted against.</span></span>

<span data-ttu-id="3c542-154">*スタブ* - スタブは、システム内の既存の依存関係 (コラボレーター) の制御可能な置換です。</span><span class="sxs-lookup"><span data-stu-id="3c542-154">*Stub* - A stub is a controllable replacement for an existing dependency (or collaborator) in the system.</span></span> <span data-ttu-id="3c542-155">スタブを使用すると、依存関係を直接処理することなく、コードをテストできます。</span><span class="sxs-lookup"><span data-stu-id="3c542-155">By using a stub, you can test your code without dealing with the dependency directly.</span></span> <span data-ttu-id="3c542-156">既定では、フェイクはスタブとして開始します。</span><span class="sxs-lookup"><span data-stu-id="3c542-156">By default, a fake starts out as a stub.</span></span>

<span data-ttu-id="3c542-157">次のコード スニペットを考えてみます。</span><span class="sxs-lookup"><span data-stu-id="3c542-157">Consider the following code snippet:</span></span>

```csharp
var mockOrder = new MockOrder();
var purchase = new Purchase(mockOrder);

purchase.ValidateOrders();

Assert.True(purchase.CanBeShipped);
```

<span data-ttu-id="3c542-158">これは、モックとして参照されるスタブの例です。</span><span class="sxs-lookup"><span data-stu-id="3c542-158">This would be an example of stub being referred to as a mock.</span></span> <span data-ttu-id="3c542-159">ここでは、実際にはスタブです。</span><span class="sxs-lookup"><span data-stu-id="3c542-159">In this case, it is a stub.</span></span> <span data-ttu-id="3c542-160">`Purchase` (テスト対象のシステム) をインスタンス化する手段として、Order を渡しているだけです。</span><span class="sxs-lookup"><span data-stu-id="3c542-160">You're just passing in the Order as a means to be able to instantiate `Purchase` (the system under test).</span></span> <span data-ttu-id="3c542-161">Order はモックでないので、名前 `MockOrder` も非常に紛らわしいものです。</span><span class="sxs-lookup"><span data-stu-id="3c542-161">The name `MockOrder` is also very misleading because again, the order is not a mock.</span></span>

<span data-ttu-id="3c542-162">より適切なアプローチを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="3c542-162">A better approach would be</span></span>

```csharp
var stubOrder = new FakeOrder();
var purchase = new Purchase(stubOrder);

purchase.ValidateOrders();

Assert.True(purchase.CanBeShipped);
```

<span data-ttu-id="3c542-163">クラスの名前を `FakeOrder` に変更して、クラスをより汎用的な名前にし、クラスをモックまたはスタブとして使用できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="3c542-163">By renaming the class to `FakeOrder`, you've made the class a lot more generic, the class can be used as a mock or a stub.</span></span> <span data-ttu-id="3c542-164">テスト ケースに適切な方をどちらでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="3c542-164">Whichever is better for the test case.</span></span> <span data-ttu-id="3c542-165">上記の例では、`FakeOrder` はスタブとして使用されています。</span><span class="sxs-lookup"><span data-stu-id="3c542-165">In the above example, `FakeOrder` is used as a stub.</span></span> <span data-ttu-id="3c542-166">アサート時には、どのような形状または形式でも `FakeOrder` を使用していません。</span><span class="sxs-lookup"><span data-stu-id="3c542-166">You're not using the `FakeOrder` in any shape or form during the assert.</span></span> <span data-ttu-id="3c542-167">`FakeOrder` は、コンストラクターの要件を満たすために `Purchase` クラスに渡されただけです。</span><span class="sxs-lookup"><span data-stu-id="3c542-167">`FakeOrder` was just passed into the `Purchase` class to satisfy the requirements of the constructor.</span></span>

<span data-ttu-id="3c542-168">これをモックとして使用するには、たとえば次のようにします。</span><span class="sxs-lookup"><span data-stu-id="3c542-168">To use it as a Mock, you could do something like this</span></span>

```csharp
var mockOrder = new FakeOrder();
var purchase = new Purchase(mockOrder);

purchase.ValidateOrders();

Assert.True(mockOrder.Validated);
```

<span data-ttu-id="3c542-169">この場合は、フェイクのプロパティをチェック (フェイクに対してアサート) しているので、上記のコード スニペット内で `mockOrder` はモックです。</span><span class="sxs-lookup"><span data-stu-id="3c542-169">In this case, you are checking a property on the Fake (asserting against it), so in the above code snippet, the `mockOrder` is a Mock.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c542-170">この用語を正確に理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="3c542-170">It's important to get this terminology correct.</span></span> <span data-ttu-id="3c542-171">スタブを "モック" と名付けた場合、他の開発者はあなたの意図を誤って解釈してしまいます。</span><span class="sxs-lookup"><span data-stu-id="3c542-171">If you call your stubs "mocks", other developers are going to make false assumptions about your intent.</span></span>

<span data-ttu-id="3c542-172">モックとスタブに関する重要な留意点として、モックとスタブはよく似ていますが、モック オブジェクトに対してはアサートを行うのに対し、スタブに対してはアサートを行いません。</span><span class="sxs-lookup"><span data-stu-id="3c542-172">The main thing to remember about mocks versus stubs is that mocks are just like stubs, but you assert against the mock object, whereas you do not assert against a stub.</span></span>

## <a name="best-practices"></a><span data-ttu-id="3c542-173">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="3c542-173">Best practices</span></span>

### <a name="naming-your-tests"></a><span data-ttu-id="3c542-174">テストの名前付け</span><span class="sxs-lookup"><span data-stu-id="3c542-174">Naming your tests</span></span>
<span data-ttu-id="3c542-175">テストの名前は、次の 3 つの部分で構成される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-175">The name of your test should consist of three parts:</span></span>
- <span data-ttu-id="3c542-176">テスト対象のメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="3c542-176">The name of the method being tested.</span></span>
- <span data-ttu-id="3c542-177">それがテストされるシナリオ。</span><span class="sxs-lookup"><span data-stu-id="3c542-177">The scenario under which it's being tested.</span></span>
- <span data-ttu-id="3c542-178">シナリオが呼び出されたときに想定される動作。</span><span class="sxs-lookup"><span data-stu-id="3c542-178">The expected behavior when the scenario is invoked.</span></span>

#### <a name="why"></a><span data-ttu-id="3c542-179">なぜでしょうか。</span><span class="sxs-lookup"><span data-stu-id="3c542-179">Why?</span></span>
- <span data-ttu-id="3c542-180">名前付け規則は、テストの目的を明示的に表すので重要です。</span><span class="sxs-lookup"><span data-stu-id="3c542-180">Naming standards are important because they explicitly express the intent of the test.</span></span>

<span data-ttu-id="3c542-181">テストは、コードが機能することを確認するだけでなく、ドキュメントも提供します。</span><span class="sxs-lookup"><span data-stu-id="3c542-181">Tests are more than just making sure your code works, they also provide documentation.</span></span> <span data-ttu-id="3c542-182">単体テストのスイートを見るだけで、コード自体を見なくても、コードの動作を推測できます。</span><span class="sxs-lookup"><span data-stu-id="3c542-182">Just by looking at the suite of unit tests, you should be able to infer the behavior of your code without even looking at the code itself.</span></span> <span data-ttu-id="3c542-183">さらに、テストが失敗した際には、どのシナリオが想定を満たしていないかを正確に判断できます。</span><span class="sxs-lookup"><span data-stu-id="3c542-183">Additionally, when tests fail, you can see exactly which scenarios do not meet your expectations.</span></span>

#### <a name="bad"></a><span data-ttu-id="3c542-184">不適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-184">Bad:</span></span>
[!code-csharp[BeforeNaming](../../../samples/csharp/unit-testing-best-practices/before/StringCalculatorTests.cs#BeforeNaming)]

#### <a name="better"></a><span data-ttu-id="3c542-185">より適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-185">Better:</span></span>
[!code-csharp[AfterNamingAndMinimallyPassing](../../../samples/csharp/unit-testing-best-practices/after/StringCalculatorTests.cs#AfterNamingAndMinimallyPassing)]

### <a name="arranging-your-tests"></a><span data-ttu-id="3c542-186">テストの配置</span><span class="sxs-lookup"><span data-stu-id="3c542-186">Arranging your tests</span></span>
<span data-ttu-id="3c542-187">**Arrange、Act、Assert** は、単体テスト時に共通するパターンです。</span><span class="sxs-lookup"><span data-stu-id="3c542-187">**Arrange, Act, Assert** is a common pattern when unit testing.</span></span> <span data-ttu-id="3c542-188">名前が示すように、これは次の 3 つの主なアクションで構成されます。</span><span class="sxs-lookup"><span data-stu-id="3c542-188">As the name implies, it consists of three main actions:</span></span>
- <span data-ttu-id="3c542-189">オブジェクトを*配置 (Arrange)* し、必要に応じて作成および設定します。</span><span class="sxs-lookup"><span data-stu-id="3c542-189">*Arrange* your objects, creating and setting them up as necessary.</span></span>
- <span data-ttu-id="3c542-190">オブジェクトを*操作 (Act)* します。</span><span class="sxs-lookup"><span data-stu-id="3c542-190">*Act* on an object.</span></span>
- <span data-ttu-id="3c542-191">何かが想定どおりであることを*アサート (Assert)* します。</span><span class="sxs-lookup"><span data-stu-id="3c542-191">*Assert* that something is as expected.</span></span>

#### <a name="why"></a><span data-ttu-id="3c542-192">なぜでしょうか。</span><span class="sxs-lookup"><span data-stu-id="3c542-192">Why?</span></span>
- <span data-ttu-id="3c542-193">*配置*と*アサート*の手順で、テストする対象を明確に区別します。</span><span class="sxs-lookup"><span data-stu-id="3c542-193">Clearly separates what is being tested from the *arrange* and *assert* steps.</span></span>
- <span data-ttu-id="3c542-194">"Act" コードにより、アサーションが混合される可能性が低くなります。</span><span class="sxs-lookup"><span data-stu-id="3c542-194">Less chance to intermix assertions with "Act" code.</span></span>

<span data-ttu-id="3c542-195">読みやすさは、テストの作成時において最も重要な側面の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="3c542-195">Readability is one of the most important aspects when writing a test.</span></span> <span data-ttu-id="3c542-196">テスト内でこれらの各アクションを分離することで、コードの呼び出しに必要な依存関係、コードを呼び出す方法、および何をアサートしようとしているかが明確に区別されます。</span><span class="sxs-lookup"><span data-stu-id="3c542-196">Separating each of these actions within the test clearly highlight the dependencies required to call your code, how your code is being called, and what you are trying to assert.</span></span> <span data-ttu-id="3c542-197">いくつかの手順を結合し、テストのサイズを小さくすることは可能ですが、主な目的はテストをできるだけ読みやすくすることにあります。</span><span class="sxs-lookup"><span data-stu-id="3c542-197">While it may be possible to combine some steps and reduce the size of your test, the primary goal is to make the test as readable as possible.</span></span>

#### <a name="bad"></a><span data-ttu-id="3c542-198">不適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-198">Bad:</span></span>
[!code-csharp[BeforeArranging](../../../samples/csharp/unit-testing-best-practices/before/StringCalculatorTests.cs#BeforeArranging)]

#### <a name="better"></a><span data-ttu-id="3c542-199">より適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-199">Better:</span></span>
[!code-csharp[AfterArranging](../../../samples/csharp/unit-testing-best-practices/after/StringCalculatorTests.cs#AfterArranging)]

### <a name="write-minimally-passing-tests"></a><span data-ttu-id="3c542-200">最小限の情報で合格するテストを記述する</span><span class="sxs-lookup"><span data-stu-id="3c542-200">Write minimally passing tests</span></span>
<span data-ttu-id="3c542-201">単体テストで使用する入力は、現在テストしている動作を検証するために、できる限り単純である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-201">The input to be used in a unit test should be the simplest possible in order to verify the behavior that you are currently testing.</span></span>

#### <a name="why"></a><span data-ttu-id="3c542-202">なぜでしょうか。</span><span class="sxs-lookup"><span data-stu-id="3c542-202">Why?</span></span>
- <span data-ttu-id="3c542-203">コードベースでの今後の変更に対して、テストの回復力が高くなります。</span><span class="sxs-lookup"><span data-stu-id="3c542-203">Tests become more resilient to future changes in the codebase.</span></span>
- <span data-ttu-id="3c542-204">実装よりもテストの動作に的が絞られます。</span><span class="sxs-lookup"><span data-stu-id="3c542-204">Closer to testing behavior over implementation.</span></span>

<span data-ttu-id="3c542-205">テストに合格するために必要以上の情報を含むテストは、テストでエラーが発生する可能性が高く、テストの目的が不明確になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-205">Tests that include more information than required to pass the test have a higher chance of introducing errors into the test and can make the intent of the test less clear.</span></span> <span data-ttu-id="3c542-206">テストの記述時には、動作に的を絞る必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-206">When writing tests you want to focus on the behavior.</span></span> <span data-ttu-id="3c542-207">モデルに追加のプロパティを設定したり、不要な場合に 0 以外の値を使用すると、証明しようとしている内容が不明瞭になるだけです。</span><span class="sxs-lookup"><span data-stu-id="3c542-207">Setting extra properties on models or using non-zero values when not required, only detracts from what you are trying to prove.</span></span>

#### <a name="bad"></a><span data-ttu-id="3c542-208">不適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-208">Bad:</span></span>
[!code-csharp[BeforeMinimallyPassing](../../../samples/csharp/unit-testing-best-practices/before/StringCalculatorTests.cs#BeforeMinimallyPassing)]

#### <a name="better"></a><span data-ttu-id="3c542-209">より適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-209">Better:</span></span>
[!code-csharp[AfterNamingAndMinimallyPassing](../../../samples/csharp/unit-testing-best-practices/after/StringCalculatorTests.cs#AfterNamingAndMinimallyPassing)]

### <a name="avoid-magic-strings"></a><span data-ttu-id="3c542-210">マジック文字列を回避する</span><span class="sxs-lookup"><span data-stu-id="3c542-210">Avoid magic strings</span></span>
<span data-ttu-id="3c542-211">単体テストにおける変数の名前付けは、より重要というわけではなくとも、運用コードにおける変数の名前付けと同等に重要です。</span><span class="sxs-lookup"><span data-stu-id="3c542-211">Naming variables in unit tests is as important, if not more important, than naming variables in production code.</span></span> <span data-ttu-id="3c542-212">単体テストにマジック文字列を含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="3c542-212">Unit tests should not contain magic strings.</span></span>

#### <a name="why"></a><span data-ttu-id="3c542-213">なぜでしょうか。</span><span class="sxs-lookup"><span data-stu-id="3c542-213">Why?</span></span>
- <span data-ttu-id="3c542-214">特殊な値となっている原因を特定するために、テストを読む人が運用コードを調べる必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="3c542-214">Prevents the need for the reader of the test to inspect the production code in order to figure out what makes the value special.</span></span>
- <span data-ttu-id="3c542-215">*実現*しようとしている内容ではなく*証明*しようとしている内容が明示的に示されます。</span><span class="sxs-lookup"><span data-stu-id="3c542-215">Explicitly shows what you're trying to *prove* rather than trying to *accomplish*.</span></span>

<span data-ttu-id="3c542-216">マジック文字列は、テストを読む人に混乱をきたす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-216">Magic strings can cause confusion to the reader of your tests.</span></span> <span data-ttu-id="3c542-217">文字列が通常からかけ離れて見えれば、パラメーターや戻り値としてその特定の値がなぜ選択されたかが気になります。</span><span class="sxs-lookup"><span data-stu-id="3c542-217">If a string looks out of the ordinary, they may wonder why a certain value was chosen for a parameter or return value.</span></span> <span data-ttu-id="3c542-218">そのような場合、テストに集中するのではなく、実装の詳細を調べようとします。</span><span class="sxs-lookup"><span data-stu-id="3c542-218">This may lead them to take a closer look at the implementation details, rather than focus on the test.</span></span>

> [!TIP] 
> <span data-ttu-id="3c542-219">テストの記述時には、その意図をできる限り表現することを目指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-219">When writing tests, you should aim to express as much intent as possible.</span></span> <span data-ttu-id="3c542-220">マジック文字列の場合の適切なアプローチとしては、これらの値を定数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3c542-220">In the case of magic strings, a good approach is to assign these values to constants.</span></span>

#### <a name="bad"></a><span data-ttu-id="3c542-221">不適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-221">Bad:</span></span>
[!code-csharp[BeforeMagicString](../../../samples/csharp/unit-testing-best-practices/before/StringCalculatorTests.cs#BeforeMagicString)]

#### <a name="better"></a><span data-ttu-id="3c542-222">より適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-222">Better:</span></span>
[!code-csharp[AfterMagicString](../../../samples/csharp/unit-testing-best-practices/after/StringCalculatorTests.cs#AfterMagicString)]

### <a name="avoid-logic-in-tests"></a><span data-ttu-id="3c542-223">テストで論理を回避する</span><span class="sxs-lookup"><span data-stu-id="3c542-223">Avoid logic in tests</span></span>
<span data-ttu-id="3c542-224">単体テストの記述時には、手動による文字列の連結、および `if`、`while`、`for`、`switch` などの論理条件を回避します。</span><span class="sxs-lookup"><span data-stu-id="3c542-224">When writing your unit tests avoid manual string concatenation and logical conditions such as `if`, `while`, `for`, `switch`, etc.</span></span>

#### <a name="why"></a><span data-ttu-id="3c542-225">なぜでしょうか。</span><span class="sxs-lookup"><span data-stu-id="3c542-225">Why?</span></span>
- <span data-ttu-id="3c542-226">テスト内にバグが発生する可能性が低くなります。</span><span class="sxs-lookup"><span data-stu-id="3c542-226">Less chance to introduce a bug inside of your tests.</span></span>
- <span data-ttu-id="3c542-227">実装の詳細ではなく、最終的な結果に的が絞られます。</span><span class="sxs-lookup"><span data-stu-id="3c542-227">Focus on the end result, rather than implementation details.</span></span>

<span data-ttu-id="3c542-228">テスト スイートに論理を導入すると、バグが発生する可能性が著しく高まります。</span><span class="sxs-lookup"><span data-stu-id="3c542-228">When you introduce logic into your test suite, the chance of introducing a bug into it increases dramatically.</span></span> <span data-ttu-id="3c542-229">テスト スイート内でバグが発見されることは避けなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3c542-229">The last place that you want to find a bug is within your test suite.</span></span> <span data-ttu-id="3c542-230">テストが機能するという高レベルの確信が持てる必要があります。そうでなければ、テストを信頼することはできません。</span><span class="sxs-lookup"><span data-stu-id="3c542-230">You should have a high level of confidence that your tests work, otherwise, you will not trust them.</span></span> <span data-ttu-id="3c542-231">信頼できないテストは、何の値も提供しません。</span><span class="sxs-lookup"><span data-stu-id="3c542-231">Tests that you do not trust, do not provide any value.</span></span> <span data-ttu-id="3c542-232">テストが失敗した場合は、コードに実際に問題があり、無視できないことを実感できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-232">When a test fails, you want to have a sense that something is actually wrong with your code and that it cannot be ignored.</span></span>

> [!TIP]
> <span data-ttu-id="3c542-233">テスト内の論理を避けられない場合は、テストを 2 つ以上の別々のテストに分割することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="3c542-233">If logic in your test seems unavoidable, consider splitting the test up into two or more different tests.</span></span>

#### <a name="bad"></a><span data-ttu-id="3c542-234">不適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-234">Bad:</span></span>
[!code-csharp[LogicInTests](../../../samples/csharp/unit-testing-best-practices/before/StringCalculatorTests.cs#LogicInTests)]

#### <a name="better"></a><span data-ttu-id="3c542-235">より適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-235">Better:</span></span>
[!code-csharp[AfterTestLogic](../../../samples/csharp/unit-testing-best-practices/after/StringCalculatorTests.cs#AfterTestLogic)]

### <a name="prefer-helper-methods-to-setup-and-teardown"></a><span data-ttu-id="3c542-236">設定と破棄よりもヘルパー メソッドを優先する</span><span class="sxs-lookup"><span data-stu-id="3c542-236">Prefer helper methods to setup and teardown</span></span>
<span data-ttu-id="3c542-237">テストに同様のオブジェクトまたは状態が必要な場合は、設定属性と破棄属性を利用する (存在する場合) よりもヘルパー メソッドを優先します。</span><span class="sxs-lookup"><span data-stu-id="3c542-237">If you require a similar object or state for your tests, prefer a helper method than leveraging Setup and Teardown attributes if they exist.</span></span>

#### <a name="why"></a><span data-ttu-id="3c542-238">なぜでしょうか。</span><span class="sxs-lookup"><span data-stu-id="3c542-238">Why?</span></span>
- <span data-ttu-id="3c542-239">各テスト内からコード全体を見ることができるので、テストを読むときに混乱が少なくなります。</span><span class="sxs-lookup"><span data-stu-id="3c542-239">Less confusion when reading the tests since all of the code is visible from within each test.</span></span>
- <span data-ttu-id="3c542-240">特定のテストに対する設定が多すぎたり少なすぎたりする可能性が低くなります。</span><span class="sxs-lookup"><span data-stu-id="3c542-240">Less chance of setting up too much or too little for the given test.</span></span>
- <span data-ttu-id="3c542-241">テスト間で状態を共有して、テスト間に不要な依存関係が生じる可能性が低くなります。</span><span class="sxs-lookup"><span data-stu-id="3c542-241">Less chance of sharing state between tests which creates unwanted dependencies between them.</span></span>

<span data-ttu-id="3c542-242">単体テスト フレームワークでは、テスト スイート内のすべての各単体テスト前に `Setup` が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3c542-242">In unit testing frameworks, `Setup` is called before each and every unit test within your test suite.</span></span> <span data-ttu-id="3c542-243">これは便利なツールとして見なされる場合もありますが、通常はテストが膨張して読みづらくなってしまいます。</span><span class="sxs-lookup"><span data-stu-id="3c542-243">While some may see this as a useful tool, it generally ends up leading to bloated and hard to read tests.</span></span> <span data-ttu-id="3c542-244">各テストには、テストが稼働するためにさまざまな要件があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-244">Each test will generally have different requirements in order to get the test up and running.</span></span> <span data-ttu-id="3c542-245">しかし、`Setup` は各テストに対してまったく同じ要件を使用することを強制します。</span><span class="sxs-lookup"><span data-stu-id="3c542-245">Unfortunately, `Setup` forces you to use the exact same requirements for each test.</span></span>

> [!NOTE] 
> <span data-ttu-id="3c542-246">xUnit では、バージョン 2.x の時点で SetUp と TearDown の両方が削除されています。</span><span class="sxs-lookup"><span data-stu-id="3c542-246">xUnit has removed both SetUp and TearDown as of version 2.x</span></span>

#### <a name="bad"></a><span data-ttu-id="3c542-247">不適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-247">Bad:</span></span>
[!code-csharp[BeforeSetup](../../../samples/csharp/unit-testing-best-practices/before/StringCalculatorTests.cs#BeforeSetup)]

```csharp
// more tests...
```

[!code-csharp[BeforeHelperMethod](../../../samples/csharp/unit-testing-best-practices/before/StringCalculatorTests.cs#BeforeHelperMethod)]

#### <a name="better"></a><span data-ttu-id="3c542-248">より適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-248">Better:</span></span>
[!code-csharp[AfterHelperMethod](../../../samples/csharp/unit-testing-best-practices/after/StringCalculatorTests.cs#AfterHelperMethod)]

```csharp
// more tests...
```

[!code-csharp[AfterSetup](../../../samples/csharp/unit-testing-best-practices/after/StringCalculatorTests.cs#AfterSetup)]

### <a name="avoid-multiple-asserts"></a><span data-ttu-id="3c542-249">複数のアサートを回避する</span><span class="sxs-lookup"><span data-stu-id="3c542-249">Avoid multiple asserts</span></span>
<span data-ttu-id="3c542-250">テストを記述する際には、テストごとにアサートを 1 つだけ含めるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="3c542-250">When writing your tests, try to only include one Assert per test.</span></span> <span data-ttu-id="3c542-251">アサートを 1 つだけ使用する一般的なアプローチには、次のものがあります。</span><span class="sxs-lookup"><span data-stu-id="3c542-251">Common approaches to using only one assert include:</span></span>
- <span data-ttu-id="3c542-252">アサートごとに別々のテストを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c542-252">Create a separate test for each assert.</span></span>
- <span data-ttu-id="3c542-253">パラメーター化されたテストを使用します。</span><span class="sxs-lookup"><span data-stu-id="3c542-253">Use parameterized tests.</span></span>

#### <a name="why"></a><span data-ttu-id="3c542-254">なぜでしょうか。</span><span class="sxs-lookup"><span data-stu-id="3c542-254">Why?</span></span>
- <span data-ttu-id="3c542-255">1 つのアサートに失敗した場合、後続のアサートは評価されません。</span><span class="sxs-lookup"><span data-stu-id="3c542-255">If one Assert fails, the subsequent Asserts will not be evaluated.</span></span>
- <span data-ttu-id="3c542-256">テストで複数のケースをアサートしないようにします。</span><span class="sxs-lookup"><span data-stu-id="3c542-256">Ensures you are not asserting multiple cases in your tests.</span></span>
- <span data-ttu-id="3c542-257">テストが失敗した理由に関する全体像をとらえることができます。</span><span class="sxs-lookup"><span data-stu-id="3c542-257">Gives you the entire picture as to why your tests are failing.</span></span> 

<span data-ttu-id="3c542-258">テスト ケースに複数のアサートを導入した場合、すべてのアサートが実行されることは保証されません。</span><span class="sxs-lookup"><span data-stu-id="3c542-258">When introducing multiple asserts into a test case, it is not guaranteed that all of the asserts will be executed.</span></span> <span data-ttu-id="3c542-259">ほとんどの単体テスト フレームワークでは、単体テストでアサーションが失敗すると、続行中のテストは自動的に失敗と見なされます。</span><span class="sxs-lookup"><span data-stu-id="3c542-259">In most unit testing frameworks, once an assertion fails in a unit test, the proceeding tests are automatically considered to be failing.</span></span> <span data-ttu-id="3c542-260">この際、実際には動作している機能が失敗として示されるので、混乱を招きます。</span><span class="sxs-lookup"><span data-stu-id="3c542-260">This can be confusing as functionality that is actually working, will be shown as failing.</span></span>

> [!NOTE]
> <span data-ttu-id="3c542-261">この規則の一般的な例外は、オブジェクトに対してアサートを行う場合です。</span><span class="sxs-lookup"><span data-stu-id="3c542-261">A common exception to this rule is when asserting against an object.</span></span> <span data-ttu-id="3c542-262">この場合、オブジェクトが想定どおりの状態にあること保証するために、通常は各プロパティに対して複数のアサートを使用することが許容されます。</span><span class="sxs-lookup"><span data-stu-id="3c542-262">In this case, it is generally acceptable to have multiple asserts against each property to ensure the object is in the state that you expect it to be in.</span></span>

#### <a name="bad"></a><span data-ttu-id="3c542-263">不適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-263">Bad:</span></span>
[!code-csharp[BeforeMultipleAsserts](../../../samples/csharp/unit-testing-best-practices/before/StringCalculatorTests.cs#BeforeMultipleAsserts)]

#### <a name="better"></a><span data-ttu-id="3c542-264">より適切な例:</span><span class="sxs-lookup"><span data-stu-id="3c542-264">Better:</span></span>
[!code-csharp[AfterMultipleAsserts](../../../samples/csharp/unit-testing-best-practices/after/StringCalculatorTests.cs#AfterMultipleAsserts)]

### <a name="validate-private-methods-by-unit-testing-public-methods"></a><span data-ttu-id="3c542-265">パブリック メソッドの単体テストを行うことでプライベート メソッドを検証する</span><span class="sxs-lookup"><span data-stu-id="3c542-265">Validate private methods by unit testing public methods</span></span>
<span data-ttu-id="3c542-266">ほとんどの場合、プライベート メソッドをテストする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3c542-266">In most cases, there should not be a need to test a private method.</span></span> <span data-ttu-id="3c542-267">プライベート メソッドは実装の詳細です。</span><span class="sxs-lookup"><span data-stu-id="3c542-267">Private methods are an implementation detail.</span></span> <span data-ttu-id="3c542-268">プライベート メソッドは独立して存在することはない、と考えることができます。</span><span class="sxs-lookup"><span data-stu-id="3c542-268">You can think of it this way: private methods never exist in isolation.</span></span> <span data-ttu-id="3c542-269">いずれかの時点で、実装の一部としてプライベート メソッドを呼び出す、パブリックに公開されたメソッドが存在することになります。</span><span class="sxs-lookup"><span data-stu-id="3c542-269">At some point, there is going to be a public facing method that calls the private method as part of its implementation.</span></span> <span data-ttu-id="3c542-270">鍵となるのは、プライベート メソッドを呼び出すパブリック メソッドの最終結果です。</span><span class="sxs-lookup"><span data-stu-id="3c542-270">What you should care about is the end result of the public method that calls into the private one.</span></span> 

<span data-ttu-id="3c542-271">次のケースを考えてみます。</span><span class="sxs-lookup"><span data-stu-id="3c542-271">Consider the following case</span></span>

```csharp
public string ParseLogLine(string input)
{
    var sanitizedInput = trimInput(input);
    return sanitizedInput;
}

private string trimInput(string input)
{
    return input.Trim();
}
```

<span data-ttu-id="3c542-272">メソッドが想定どおりに動作していることを確認する必要があるので、まずは、`trimInput` に対してテストを記述しようと考えるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="3c542-272">Your first reaction may be to start writing a test for `trimInput` because you want to make sure that the method is working as expected.</span></span> <span data-ttu-id="3c542-273">しかし、想定外の方法で `ParseLogLine` が `sanitizedInput` を操作し、`trimInput` に対するテストが無効になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-273">However, it is entirely possible that `ParseLogLine` manipulates `sanitizedInput` in such a way that you do not expect, rendering a test against `trimInput` useless.</span></span> 

<span data-ttu-id="3c542-274">実際のテストは、パブリックに公開された `ParseLogLine` メソッドに対して行う必要があります。最終的にはこのメソッドが鍵となるためです。</span><span class="sxs-lookup"><span data-stu-id="3c542-274">The real test should be done against the public facing method `ParseLogLine` because that is what you should ultimately care about.</span></span> 

```csharp
public void ParseLogLine_ByDefault_ReturnsTrimmedResult()
{
    var parser = new Parser();

    var result = parser.ParseLogLine(" a ");

    Assert.Equals("a", result);
}
```

<span data-ttu-id="3c542-275">この観点で、プライベート メソッドがある場合は、パブリック メソッドを見つけて、そのメソッドに対してテストを記述します。</span><span class="sxs-lookup"><span data-stu-id="3c542-275">With this viewpoint, if you see a private method, find the public method and write your tests against that method.</span></span> <span data-ttu-id="3c542-276">プライベート メソッドが想定どおりの結果を返すからといって、最終的にプライベート メソッドを呼び出すシステムが、結果を正しく使用するとは限りません。</span><span class="sxs-lookup"><span data-stu-id="3c542-276">Just because a private method returns the expected result, does not mean the system that eventually calls the private method uses the result correctly.</span></span>

### <a name="stub-static-references"></a><span data-ttu-id="3c542-277">スタブの静的参照</span><span class="sxs-lookup"><span data-stu-id="3c542-277">Stub static references</span></span>
<span data-ttu-id="3c542-278">単体テストの原則の 1 つは、テスト対象システムに対してフル コントロールを持つ必要があることです。</span><span class="sxs-lookup"><span data-stu-id="3c542-278">One of the principles of a unit test is that it must have full control of the system under test.</span></span> <span data-ttu-id="3c542-279">このことは、運用コードに静的参照への呼び出しが含まれる場合に問題となります (例: `DateTime.Now`)。</span><span class="sxs-lookup"><span data-stu-id="3c542-279">This can be problematic when production code includes calls to static references (e.g. `DateTime.Now`).</span></span> <span data-ttu-id="3c542-280">次のコードを考えてみます。</span><span class="sxs-lookup"><span data-stu-id="3c542-280">Consider the following code</span></span>

```csharp
public int GetDiscountedPrice(int price)
{
    if(DateTime.Now == DayOfWeek.Tuesday) 
    {
        return price / 2;
    }
    else 
    {
        return price;
    }
}
```

<span data-ttu-id="3c542-281">このコードに対して単体テストを行うには、どのようにすればよいでしょうでしょうか。</span><span class="sxs-lookup"><span data-stu-id="3c542-281">How can this code possibly be unit tested?</span></span> <span data-ttu-id="3c542-282">次のようなアプローチを試してみることができます。</span><span class="sxs-lookup"><span data-stu-id="3c542-282">You may try an approach such as</span></span>

```csharp
public void GetDiscountedPrice_ByDefault_ReturnsFullPrice()
{
    var priceCalculator = new PriceCalculator();

    var actual = priceCalculator.GetDiscountedPrice(2);

    Assert.Equals(2, actual)
}

public void GetDiscountedPrice_OnTuesday_ReturnsHalfPrice()
{
    var priceCalculator = new PriceCalculator();

    var actual = priceCalculator.GetDiscountedPrice(2);

    Assert.Equals(1, actual);
}
```

<span data-ttu-id="3c542-283">ただし、このテストにはいくつかの問題があることがすぐにわかります。</span><span class="sxs-lookup"><span data-stu-id="3c542-283">Unfortunately, you will quickly realize that there are a couple problems with your tests.</span></span> 

- <span data-ttu-id="3c542-284">テスト スイートが火曜日に実行される場合、2 番目のテストには合格しますが、最初のテストには失敗します。</span><span class="sxs-lookup"><span data-stu-id="3c542-284">If the test suite is run on a Tuesday, the second test will pass, but the first test will fail.</span></span>
- <span data-ttu-id="3c542-285">テスト スイートが他のいずれかの曜日に実行される場合、最初のテストには合格しますが、2 番目のテストには失敗します。</span><span class="sxs-lookup"><span data-stu-id="3c542-285">If the test suite is run on any other day, the first test will pass, but the second test will fail.</span></span>

<span data-ttu-id="3c542-286">こうした問題を解決するには、運用コードに*シーム*を導入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c542-286">To solve these problems, you'll need to introduce a *seam* into your production code.</span></span> <span data-ttu-id="3c542-287">1 つのアプローチとしては、インターフェイス内で制御する必要のあるコードをラップし、運用コードがそのインターフェイスに依存するようにします。</span><span class="sxs-lookup"><span data-stu-id="3c542-287">One approach is to wrap the code that you need to control in an interface and have the production code depend on that interface.</span></span>

```csharp
public interface IDateTimeProvider
{
    DayOfWeek DayOfWeek();
}

public int GetDiscountedPrice(int price, IDateTimeProvider dateTimeProvider)
{
    if(dateTimeProvider.DayOfWeek() == DayOfWeek.Tuesday) 
    {
        return price / 2;
    }
    else 
    {
        return price;
    }
}
```

<span data-ttu-id="3c542-288">この時点で、テスト スイートは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="3c542-288">Your test suite now becomes</span></span>

```csharp
public void GetDiscountedPrice_ByDefault_ReturnsFullPrice()
{
    var priceCalculator = new PriceCalculator();
    var dateTimeProviderStub = new Mock<IDateTimeProvider>();
    dateTimeProviderStub.Setup(dtp => dtp.DayOfWeek()).Returns(DayOfWeek.Monday);

    var actual = priceCalculator.GetDiscountedPrice(2, dateTimeProviderStub);

    Assert.Equals(2, actual);
}

public void GetDiscountedPrice_OnTuesday_ReturnsHalfPrice()
{
    var priceCalculator = new PriceCalculator();
    var dateTimeProviderStub = new Mock<IDateTimeProvider>();
    dateTimeProviderStub.Setup(dtp => dtp.DayOfWeek()).Returns(DayOfWeek.Tuesday);

    var actual = priceCalculator.GetDiscountedPrice(2, dateTimeProviderStub);

    Assert.Equals(1, actual);
}
```

<span data-ttu-id="3c542-289">これで、テスト スイートは `DateTime.Now` に対してフル コントロールを持ち、メソッドを呼び出すときに任意の値をスタブできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="3c542-289">Now the test suite has full control over `DateTime.Now` and can stub any value when calling into the method.</span></span>
