---
title: 例外のスロー
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- exceptions, throwing
- explicitly throwing exceptions
- throwing exceptions, design guidelines
ms.assetid: 5388e02b-52f5-460e-a2b5-eeafe60eeebe
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9fbbe84811e3fa096b9e13c459143311bb75a198
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47077838"
---
# <a name="exception-throwing"></a><span data-ttu-id="a3b9e-102">例外のスロー</span><span class="sxs-lookup"><span data-stu-id="a3b9e-102">Exception Throwing</span></span>
<span data-ttu-id="a3b9e-103">このセクションで説明されている例外のスローのガイドラインには、実行エラーの意味を適切な定義が必要です。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-103">Exception-throwing guidelines described in this section require a good definition of the meaning of execution failure.</span></span> <span data-ttu-id="a3b9e-104">メンバーが実行できないときに、実行エラーが発生します (どのようなメンバー名を意味します) を実行するように設計します。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-104">Execution failure occurs whenever a member cannot do what it was designed to do (what the member name implies).</span></span> <span data-ttu-id="a3b9e-105">たとえば場合、`OpenFile`メソッドが呼び出し元に、開いているファイル ハンドルを返すことはできませんで実行エラーと思われることです。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-105">For example, if the `OpenFile` method cannot return an opened file handle to the caller, it would be considered an execution failure.</span></span>  
  
 <span data-ttu-id="a3b9e-106">ほとんどの開発者には、0 または null 参照による除算などの使用状況のエラーの例外の使用に慣れてになります。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-106">Most developers have become comfortable with using exceptions for usage errors such as division by zero or null references.</span></span> <span data-ttu-id="a3b9e-107">Framework では、例外は、実行エラーを含むすべてのエラー条件に対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-107">In the Framework, exceptions are used for all error conditions, including execution errors.</span></span>  
  
 <span data-ttu-id="a3b9e-108">**X DO NOT** エラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-108">**X DO NOT** return error codes.</span></span>  
  
 <span data-ttu-id="a3b9e-109">例外は、フレームワークでエラーをレポートの主要な手段です。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-109">Exceptions are the primary means of reporting errors in frameworks.</span></span>  
  
 <span data-ttu-id="a3b9e-110">**✓ DO** 例外をスローして、実行の失敗を報告します。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-110">**✓ DO** report execution failures by throwing exceptions.</span></span>  
  
 <span data-ttu-id="a3b9e-111">**✓ CONSIDER** 呼び出すことによって、プロセスを終了して`System.Environment.FailFast`(.NET Framework 2.0 の機能)、コードが安全に実行をさらにはない状況が発生すると、例外をスローする代わりにします。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-111">**✓ CONSIDER** terminating the process by calling `System.Environment.FailFast` (.NET Framework 2.0 feature) instead of throwing an exception if your code encounters a situation where it is unsafe for further execution.</span></span>  
  
 <span data-ttu-id="a3b9e-112">**X DO NOT** 可能であれば、コントロールの通常のフローの例外を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-112">**X DO NOT** use exceptions for the normal flow of control, if possible.</span></span>  
  
 <span data-ttu-id="a3b9e-113">を除き、システム障害と潜在的な競合状態の操作では、ユーザーは、例外をスローしないコードを記述できますよう、フレームワークの設計者は Api を設計する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-113">Except for system failures and operations with potential race conditions, framework designers should design APIs so users can write code that does not throw exceptions.</span></span> <span data-ttu-id="a3b9e-114">たとえば、ユーザーは、例外をスローしないコードを記述できますようにメンバーを呼び出す前に前提条件をチェックする方法を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-114">For example, you can provide a way to check preconditions before calling a member so users can write code that does not throw exceptions.</span></span>  
  
 <span data-ttu-id="a3b9e-115">別のメンバーの状態をチェックするために使用するメンバーは、テスト担当者と呼ばし、実際に作業を行うメンバーは、渡ってと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-115">The member used to check preconditions of another member is often referred to as a tester, and the member that actually does the work is called a doer.</span></span>  
  
 <span data-ttu-id="a3b9e-116">Tester-doer パターンが、許容できないパフォーマンスのオーバーヘッドを持つことができます可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-116">There are cases when the Tester-Doer Pattern can have an unacceptable performance overhead.</span></span> <span data-ttu-id="a3b9e-117">このような場合は、いわゆる Try Parse パターンを考慮する必要があります (を参照してください[例外とパフォーマンス](../../../docs/standard/design-guidelines/exceptions-and-performance.md)詳細については)。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-117">In such cases, the so-called Try-Parse Pattern should be considered (see [Exceptions and Performance](../../../docs/standard/design-guidelines/exceptions-and-performance.md) for more information).</span></span>  
  
 <span data-ttu-id="a3b9e-118">**✓ CONSIDER** パフォーマンス上の違いの例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-118">**✓ CONSIDER** the performance implications of throwing exceptions.</span></span> <span data-ttu-id="a3b9e-119">1 秒あたり 100 を超える throw レートは、ほとんどのアプリケーションのパフォーマンスに著しい影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-119">Throw rates above 100 per second are likely to noticeably impact the performance of most applications.</span></span>  
  
 <span data-ttu-id="a3b9e-120">**✓ DO** ドキュメントによって公開されている呼び出し可能なメンバー、メンバーの違反のためにスローされる例外すべてではなく、システム障害) コントラクトおよびコントラクトの一部として扱われるようにします。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-120">**✓ DO** document all exceptions thrown by publicly callable members because of a violation of the member contract (rather than a system failure) and treat them as part of your contract.</span></span>  
  
 <span data-ttu-id="a3b9e-121">コントラクトの一部である例外は、[次へ] を 1 つのバージョンから変更しないでください (つまり、例外の種類を変更しないでください、および新しい例外を追加しない必要があります)。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-121">Exceptions that are a part of the contract should not change from one version to the next (i.e., exception type should not change, and new exceptions should not be added).</span></span>  
  
 <span data-ttu-id="a3b9e-122">**X DO NOT** かどうか throw をできるパブリック メンバーに基づいてにいくつかのオプションです。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-122">**X DO NOT** have public members that can either throw or not based on some option.</span></span>  
  
 <span data-ttu-id="a3b9e-123">**X DO NOT** パブリック メンバーの戻り値として例外を返すをまたは`out`パラメーター。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-123">**X DO NOT** have public members that return exceptions as the return value or an `out` parameter.</span></span>  
  
 <span data-ttu-id="a3b9e-124">それらをスローする代わりに、パブリック Api からの例外を返すには、例外ベースのエラー報告のメリットが多数達成できないからです。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-124">Returning exceptions from public APIs instead of throwing them defeats many of the benefits of exception-based error reporting.</span></span>  
  
 <span data-ttu-id="a3b9e-125">**✓ CONSIDER** 例外ビルダー メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-125">**✓ CONSIDER** using exception builder methods.</span></span>  
  
 <span data-ttu-id="a3b9e-126">さまざまな場所から同じ例外をスローする一般的です。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-126">It is common to throw the same exception from different places.</span></span> <span data-ttu-id="a3b9e-127">コードの肥大化を回避するには、例外を作成し、そのプロパティを初期化するヘルパー メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-127">To avoid code bloat, use helper methods that create exceptions and initialize their properties.</span></span>  
  
 <span data-ttu-id="a3b9e-128">また、例外をスローするメンバーが得られないインライン化します。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-128">Also, members that throw exceptions are not getting inlined.</span></span> <span data-ttu-id="a3b9e-129">Throw ステートメント ビルダー内を移動するインライン化するメンバーを許可する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-129">Moving the throw statement inside the builder might allow the member to be inlined.</span></span>  
  
 <span data-ttu-id="a3b9e-130">**X DO NOT** 例外フィルター ブロックから例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-130">**X DO NOT** throw exceptions from exception filter blocks.</span></span>  
  
 <span data-ttu-id="a3b9e-131">例外フィルターで例外が発生、CLR で例外をキャッチし、フィルターは false を返します。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-131">When an exception filter raises an exception, the exception is caught by the CLR, and the filter returns false.</span></span> <span data-ttu-id="a3b9e-132">この動作は、フィルター実行して、明示的に false を返すことと区別することであり、デバッグが困難になります。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-132">This behavior is indistinguishable from the filter executing and returning false explicitly and is therefore very difficult to debug.</span></span>  
  
 <span data-ttu-id="a3b9e-133">**X AVOID** 明示的に finally ブロックからの例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-133">**X AVOID** explicitly throwing exceptions from finally blocks.</span></span> <span data-ttu-id="a3b9e-134">スローするメソッドの呼び出しから暗黙的にスローされた例外では、許容されます。</span><span class="sxs-lookup"><span data-stu-id="a3b9e-134">Implicitly thrown exceptions resulting from calling methods that throw are acceptable.</span></span>  
  
 <span data-ttu-id="a3b9e-135">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="a3b9e-135">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="a3b9e-136">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="a3b9e-136">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3b9e-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="a3b9e-137">See also</span></span>

- [<span data-ttu-id="a3b9e-138">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="a3b9e-138">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="a3b9e-139">例外のデザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="a3b9e-139">Design Guidelines for Exceptions</span></span>](../../../docs/standard/design-guidelines/exceptions.md)
