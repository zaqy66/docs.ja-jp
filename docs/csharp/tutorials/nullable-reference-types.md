---
title: null 許容参照型を使用して設計する
description: この高度なチュートリアルでは、null 許容参照型の概要について説明します。 参照値で null がいつ許容されるかに関する設計意図を表すことで、コンパイラで null が許容されるようにします。
ms.date: 12/03/2018
ms.custom: mvc
ms.openlocfilehash: 7e4cb423658287e5260770a680f189c227b9cd01
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53156690"
---
# <a name="tutorial-express-your-design-intent-more-clearly-with-nullable-and-non-nullable-reference-types"></a><span data-ttu-id="804ef-104">チュートリアル: null 許容参照型と null 非許容参照型を使用して設計意図をもっと明確に示す</span><span class="sxs-lookup"><span data-stu-id="804ef-104">Tutorial: Express your design intent more clearly with nullable and non-nullable reference types</span></span>

<span data-ttu-id="804ef-105">C# 8 には **null 許容参照型**が導入されています。これは、null 許容値型が値型を補完するのと同じように、参照型を補完するものです。</span><span class="sxs-lookup"><span data-stu-id="804ef-105">C# 8 introduces **nullable reference types**, which complement reference types the same way nullable value types complement value types.</span></span> <span data-ttu-id="804ef-106">型に `?` を追加することで、変数が **null 許容参照型**であることを宣言します。</span><span class="sxs-lookup"><span data-stu-id="804ef-106">You declare a variable to be a **nullable reference type** by appending a `?` to the type.</span></span> <span data-ttu-id="804ef-107">たとえば、`string?` は、null が許容される `string` を表します。</span><span class="sxs-lookup"><span data-stu-id="804ef-107">For example, `string?` represents a nullable `string`.</span></span> <span data-ttu-id="804ef-108">これらの新しい型を使用して、一部の変数では*常に値を持つ必要があり*、他の変数では*値が欠落することも可能である*という設計意図をさらに明確に示すことができます。</span><span class="sxs-lookup"><span data-stu-id="804ef-108">You can use these new types to more clearly express your design intent: some variables *must always have a value*, others *may be missing a value*.</span></span>

<span data-ttu-id="804ef-109">このチュートリアルでは、次の作業を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="804ef-109">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="804ef-110">null 許容参照型と null 非許容参照型を設計に組み込む。</span><span class="sxs-lookup"><span data-stu-id="804ef-110">Incorporate nullable and non-nullable reference types into your designs</span></span>
> * <span data-ttu-id="804ef-111">コード全体で null 許容参照型をチェックできるようにする。</span><span class="sxs-lookup"><span data-stu-id="804ef-111">Enable nullable reference type checks throughout your code.</span></span>
> * <span data-ttu-id="804ef-112">コンパイラでこれらの設計上の決定が適用されるコードを記述する。</span><span class="sxs-lookup"><span data-stu-id="804ef-112">Write code where the compiler enforces those design decisions.</span></span>
> * <span data-ttu-id="804ef-113">自分の設計の中で null 許容参照機能を使用する。</span><span class="sxs-lookup"><span data-stu-id="804ef-113">Use the nullable reference feature in your own designs</span></span>

## <a name="prerequisites"></a><span data-ttu-id="804ef-114">必須コンポーネント</span><span class="sxs-lookup"><span data-stu-id="804ef-114">Prerequisites</span></span>

<span data-ttu-id="804ef-115">お使いのコンピューターを、.NET Core が実行されるように設定する必要があります。C# 8.0 ベータ コンパイラーも実行されるようにします。</span><span class="sxs-lookup"><span data-stu-id="804ef-115">You’ll need to set up your machine to run .NET Core, including the C# 8.0 beta compiler.</span></span> <span data-ttu-id="804ef-116">C# 8 ベータ コンパイラは、[Visual Studio 2019 Preview 1](https://visualstudio.microsoft.com/vs/preview/) または [.NET Core 3.0 Preview 1](https://dotnet.microsoft.com/download/dotnet-core/3.0) で利用できます。</span><span class="sxs-lookup"><span data-stu-id="804ef-116">The C# 8 beta compiler is available with [Visual Studio 2019 preview 1](https://visualstudio.microsoft.com/vs/preview/), or [.NET Core 3.0 preview 1](https://dotnet.microsoft.com/download/dotnet-core/3.0).</span></span>

<span data-ttu-id="804ef-117">このチュートリアルでは、.NET と、C# と Visual Studio または .NET Core CLI のいずれかに精通していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="804ef-117">This tutorial assumes you're familiar with C# and .NET, including either Visual Studio or the .NET Core CLI.</span></span>

## <a name="incorporate-nullable-reference-types-into-your-designs"></a><span data-ttu-id="804ef-118">null 許容参照型と null 非許容参照型を設計に組み込む</span><span class="sxs-lookup"><span data-stu-id="804ef-118">Incorporate nullable reference types into your designs</span></span>

<span data-ttu-id="804ef-119">このチュートリアルでは、アンケートの実行をモデル化するライブラリを構築します。</span><span class="sxs-lookup"><span data-stu-id="804ef-119">In this tutorial, you'll build a library that models running a survey.</span></span> <span data-ttu-id="804ef-120">コードでは、null 許容参照型と null 非許容参照型の両方を使用して、現実世界の概念を表します。</span><span class="sxs-lookup"><span data-stu-id="804ef-120">The code uses both nullable reference types and non-nullable reference types to represent the real-world concepts.</span></span> <span data-ttu-id="804ef-121">アンケートの質問は null することはできません。</span><span class="sxs-lookup"><span data-stu-id="804ef-121">The survey questions can never be null.</span></span> <span data-ttu-id="804ef-122">回答者が質問に答えたくない場合があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-122">A respondent might prefer not to answer a question.</span></span> <span data-ttu-id="804ef-123">この場合、回答は null になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-123">The responses might be null in this case.</span></span>

<span data-ttu-id="804ef-124">このサンプルで記述するコードはそのような意図を表現し、コンパイラにその意図が適用されます。</span><span class="sxs-lookup"><span data-stu-id="804ef-124">The code you'll write for this sample expresses that intent, and the compiler enforces that intent.</span></span>

## <a name="create-the-application-and-enable-nullable-reference-types"></a><span data-ttu-id="804ef-125">アプリケーションを作成し、null 許容参照型を有効にする</span><span class="sxs-lookup"><span data-stu-id="804ef-125">Create the application and enable nullable reference types</span></span>

<span data-ttu-id="804ef-126">新しいコンソール アプリケーションを作成します。Visual Studio を使用するか、コマンド ラインで `dotnet new console` を使用します。</span><span class="sxs-lookup"><span data-stu-id="804ef-126">Create a new console application either in Visual Studio or from the command line using `dotnet new console`.</span></span> <span data-ttu-id="804ef-127">アプリケーションに `NullableIntroduction` という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="804ef-127">Name the application `NullableIntroduction`.</span></span> <span data-ttu-id="804ef-128">アプリケーションを作成したら、C# 8 ベータ機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-128">Once you've created the application, you'll need to enable C# 8 beta features.</span></span> <span data-ttu-id="804ef-129">`csproj` ファイルを開き、`LangVersion` 要素を `PropertyGroup` 要素に追加します。</span><span class="sxs-lookup"><span data-stu-id="804ef-129">Open the `csproj` file, and add a `LangVersion` element to the `PropertyGroup` element:</span></span>

```xml
<LangVersion>8.0</LangVersion>
```

<span data-ttu-id="804ef-130">または、Visual Studio プロジェクトのプロパティを使用して C# 8 を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="804ef-130">Alternatively, you can use the Visual Studio project properties to enable C# 8.</span></span> <span data-ttu-id="804ef-131">ソリューション エクスプローラーで、プロジェクト ノードを右クリックし、**[プロパティ]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="804ef-131">In Solution Explorer, right click on the project node, select **Properties**.</span></span> <span data-ttu-id="804ef-132">次に、**[ビルド]** タブを選択し、**[詳細設定]** をクリックします。言語バージョンのドロップダウンで、**[C# 8.0 (ベータ)]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="804ef-132">Then, select the **build** tab, and click **Advanced...**. In the dropdown for language version, select **C# 8.0 (beta)**.</span></span>

<span data-ttu-id="804ef-133">C# 8 プロジェクトであっても、**null 許容参照型**機能を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-133">You must opt into the **nullable reference types** feature, even in C# 8 projects.</span></span> <span data-ttu-id="804ef-134">これは、機能をオンにすると、既存の参照変数宣言が **null 非許容参照型**になるためです。</span><span class="sxs-lookup"><span data-stu-id="804ef-134">That's because once the feature is turned on, existing reference variable declarations become **non-nullable reference types**.</span></span> <span data-ttu-id="804ef-135">その決定は既存のコードで適切な null チェックが行われていない場合に問題を発見するのに役立ちますが、元の設計意図が正確に反映されない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-135">While that decision will help find issues where existing code may not have proper null-checks, it may not accurately reflect your original design intent.</span></span> <span data-ttu-id="804ef-136">この機能は、新しいプラグマを使用して有効にします。</span><span class="sxs-lookup"><span data-stu-id="804ef-136">You turn on the feature with a new pragma:</span></span>

```csharp
#nullable enable
```

<span data-ttu-id="804ef-137">ソース ファイルの任意の場所に上記のプラグマを追加でき、null 許容参照型機能はその時点からオンになります。</span><span class="sxs-lookup"><span data-stu-id="804ef-137">You can add the preceding pragma anywhere in a source file, and the nullable reference type feature is turned on from that point.</span></span> <span data-ttu-id="804ef-138">このプラグマでは、機能をオフにする `disable` 引数もサポートされています。</span><span class="sxs-lookup"><span data-stu-id="804ef-138">The pragma also supports the `disable` argument to turn off the feature.</span></span>

<span data-ttu-id="804ef-139">次の要素をご自分の .csproj ファイルに追加することで、プロジェクト全体で **null 許容参照型**を有効にすることもできます。たとえば、C# 8.0 を有効にした `LangVersion` 要素の直後に追加します。</span><span class="sxs-lookup"><span data-stu-id="804ef-139">You can also turn on **nullable reference types** for an entire project by adding the following element to your .csproj file, for example, immediately following the `LangVersion` element that enabled C# 8.0:</span></span>

```xml
<NullableReferenceTypes>true</NullableReferenceTypes>
```

### <a name="design-the-types-for-the-application"></a><span data-ttu-id="804ef-140">アプリケーション用の型を設計する</span><span class="sxs-lookup"><span data-stu-id="804ef-140">Design the types for the application</span></span>

<span data-ttu-id="804ef-141">このアンケート アプリケーションでは、いくつかのクラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-141">This survey application requires creating a number of classes:</span></span>

- <span data-ttu-id="804ef-142">質問の一覧をモデル化するクラス。</span><span class="sxs-lookup"><span data-stu-id="804ef-142">A class that models the list of questions.</span></span>
- <span data-ttu-id="804ef-143">アンケートに応じてもらうために連絡した人物の一覧をモデル化するクラス。</span><span class="sxs-lookup"><span data-stu-id="804ef-143">A class that models a list of people contacted for the survey.</span></span>
- <span data-ttu-id="804ef-144">アンケートに応じた人物から得た回答をモデル化するクラス。</span><span class="sxs-lookup"><span data-stu-id="804ef-144">A class that models the answers from a person that took the survey.</span></span>

<span data-ttu-id="804ef-145">これらの型では、null 許容参照型と null 非許容参照型の両方を利用して、必要なメンバーと省略可能なメンバーを表現します。</span><span class="sxs-lookup"><span data-stu-id="804ef-145">These types will make use of both nullable and non-nullable reference types to express which members are required and which members are optional.</span></span> <span data-ttu-id="804ef-146">null 許容参照型により、次の設計意図が明確に伝わります。</span><span class="sxs-lookup"><span data-stu-id="804ef-146">Nullable reference types communicate that design intent clearly:</span></span>

- <span data-ttu-id="804ef-147">アンケートの一部である質問を null にすることはできません。空の質問は意味がありません。</span><span class="sxs-lookup"><span data-stu-id="804ef-147">The questions that are part of the survey can never be null: It makes no sense to ask an empty question.</span></span>
- <span data-ttu-id="804ef-148">回答者を null にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="804ef-148">The respondents can never be null.</span></span> <span data-ttu-id="804ef-149">回答者が参加を辞退している場合でも、連絡した人物を追跡したいからです。</span><span class="sxs-lookup"><span data-stu-id="804ef-149">You'll want to track people you contacted, even respondents that declined to participate.</span></span>
- <span data-ttu-id="804ef-150">質問に対する回答を null にすることができます。</span><span class="sxs-lookup"><span data-stu-id="804ef-150">Any response to a question may be null.</span></span> <span data-ttu-id="804ef-151">回答者は、一部の質問またはすべての質問の回答を拒否できます。</span><span class="sxs-lookup"><span data-stu-id="804ef-151">Respondents can decline to answer some or all questions.</span></span>

<span data-ttu-id="804ef-152">これまで C# でプログラミングしている場合は、null 値を許容する参照型に慣れているため、null を許容しないインスタンスを宣言する機会がなかったかもしれません。</span><span class="sxs-lookup"><span data-stu-id="804ef-152">If you've programmed in C#, you may be so accustomed to reference types that allow null values that you may have missed other opportunities to declare non-nullable instances:</span></span>

- <span data-ttu-id="804ef-153">質問のコレクションは null を許容しないものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-153">The collection of questions should be non-nullable.</span></span>
- <span data-ttu-id="804ef-154">回答者のコレクションは null を許容しないものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-154">The collection of respondents should be non-nullable.</span></span>

<span data-ttu-id="804ef-155">コードを記述していくにつれて、参照の既定値としての null 非許容参照型によって、null 参照例外を引き起こす可能性がある一般的なミスを回避できることを理解できるでしょう。</span><span class="sxs-lookup"><span data-stu-id="804ef-155">As you write the code, you'll see that a non-nullable reference type as the default for references avoids common mistakes that could lead to null reference exceptions.</span></span> <span data-ttu-id="804ef-156">このチュートリアルから学ぶことの 1 つは、どの変数を null にすることができ、どの変数を null にすることができないかを決定することです。</span><span class="sxs-lookup"><span data-stu-id="804ef-156">One lesson from this tutorial is that you made decisions about which variables could or could not be null.</span></span> <span data-ttu-id="804ef-157">この言語には、このような決定を表現するための構文が提供されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="804ef-157">The language didn't provide syntax to express those decisions.</span></span> <span data-ttu-id="804ef-158">今、それが実現しています。</span><span class="sxs-lookup"><span data-stu-id="804ef-158">Now it does.</span></span>

<span data-ttu-id="804ef-159">ビルドするアプリでは、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="804ef-159">The app you'll build will do the following steps:</span></span>

1. <span data-ttu-id="804ef-160">アンケートを作成して質問を追加します。</span><span class="sxs-lookup"><span data-stu-id="804ef-160">Create a survey and add questions to it.</span></span>
1. <span data-ttu-id="804ef-161">アンケートの回答者の擬似乱数セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="804ef-161">Create a pseudo-random set of respondents for the survey.</span></span>
1. <span data-ttu-id="804ef-162">回答されたアンケートのサイズが目標数に達するまで、回答者に連絡します。</span><span class="sxs-lookup"><span data-stu-id="804ef-162">Contact respondents until the completed survey size reaches the goal number.</span></span>
1. <span data-ttu-id="804ef-163">アンケートの回答に関する重要な統計情報を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="804ef-163">Write out important statistics on the survey responses.</span></span>

## <a name="build-the-survey-with-nullable-and-non-nullable-types"></a><span data-ttu-id="804ef-164">null 許容型と null 非許容型を含むアンケートを作成する</span><span class="sxs-lookup"><span data-stu-id="804ef-164">Build the survey with nullable and non-nullable types</span></span>

<span data-ttu-id="804ef-165">最初に記述するコードによって、アンケートが作成されます。</span><span class="sxs-lookup"><span data-stu-id="804ef-165">The first code you'll write creates the survey.</span></span> <span data-ttu-id="804ef-166">アンケートの質問とアンケートの実行をモデル化するクラスを記述します。</span><span class="sxs-lookup"><span data-stu-id="804ef-166">You'll write classes to model a survey question and a survey run.</span></span> <span data-ttu-id="804ef-167">アンケートには、回答の形式によって区別される 3 種類の質問があります (はい/いいえで回答するもの、番号で回答するもの、およびテキストで回答するもの)。</span><span class="sxs-lookup"><span data-stu-id="804ef-167">Your survey has three types of questions, distinguished by the format of the answer: Yes/No answers, number answers, and text answers.</span></span> <span data-ttu-id="804ef-168">`public` `SurveyQuestion`クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="804ef-168">Create a `public` `SurveyQuestion` class.</span></span> <span data-ttu-id="804ef-169">`using` ステートメントの直後に `#nullable enable` プラグマを含めます。</span><span class="sxs-lookup"><span data-stu-id="804ef-169">Include the `#nullable enable` pragma immediately after the `using` statements:</span></span>

```csharp
#nullable enable
namespace NullableIntroduction
{
    public class SurveyQuestion
    {
    }
}
```

<span data-ttu-id="804ef-170">`#nullable enable` プラグマの追加は、インタープリターではすべての参照型変数の宣言が**非許容**参照型として解釈されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="804ef-170">Adding the `#nullable enable` pragma means the compiler interprets every reference type variable declaration as a **non-nullable** reference type.</span></span> <span data-ttu-id="804ef-171">次のコードに示すように、質問のテキストと質問の種類のプロパティを追加することで、最初の警告を確認できます。</span><span class="sxs-lookup"><span data-stu-id="804ef-171">You can see your first warning by adding properties for the question text and the type of question, as shown in the following code:</span></span>

```csharp
#nullable enable
namespace NullableIntroduction
{
    public enum QuestionType
    {
        YesNo,
        Number,
        Text
    }

    public class SurveyQuestion
    {
        public string QuestionText { get; }
        public QuestionType TypeOfQuestion { get; }
    }
}
```

<span data-ttu-id="804ef-172">`QuestionText` を初期化していないため、コンパイラによって、null を許容しないプロパティが初期化されていないことを示す警告が発行されます。</span><span class="sxs-lookup"><span data-stu-id="804ef-172">Because you haven't initialized `QuestionText`, the compiler issues a warning that a non-nullable property hasn't been initialized.</span></span> <span data-ttu-id="804ef-173">この設計では、質問のテキストを null 以外にする必要があるため、初期化するためのコンストラクターを追加します。`QuestionType` 値も同様にします。</span><span class="sxs-lookup"><span data-stu-id="804ef-173">Your design requires the question text to be non-null, so you add a constructor to initialize it and the `QuestionType` value as well.</span></span> <span data-ttu-id="804ef-174">完成したクラス定義は、次のコードのようになります。</span><span class="sxs-lookup"><span data-stu-id="804ef-174">The finished class definition looks like the following code:</span></span>

[!code-csharp[DefineQuestion](../../../samples/csharp/NullableIntroduction/NullableIntroduction/SurveyQuestion.cs)]

<span data-ttu-id="804ef-175">コンストラクターを追加すると、警告が解除されます。</span><span class="sxs-lookup"><span data-stu-id="804ef-175">Adding the constructor removes the warning.</span></span> <span data-ttu-id="804ef-176">コンストラクターの引数も、null 非許容参照型であるため、コンパイラによる警告は発行されません。</span><span class="sxs-lookup"><span data-stu-id="804ef-176">The constructor argument is also a non-nullable reference type, so the compiler doesn't issue any warnings.</span></span>

<span data-ttu-id="804ef-177">次に、`SurveyRun` という名前の `public` クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="804ef-177">Next, create a `public` class named `SurveyRun`.</span></span> <span data-ttu-id="804ef-178">`using` ステートメントの次に `#nullable enable` プラグマを含めます。</span><span class="sxs-lookup"><span data-stu-id="804ef-178">Include the `#nullable enable` pragma following the `using` statements.</span></span> <span data-ttu-id="804ef-179">次のコードに示すように、このクラスには、アンケートに質問を追加する `SurveyQuestion` オブジェクトとメソッドの一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="804ef-179">This class contains a list of `SurveyQuestion` objects and methods to add questions to the survey, as shown in the following code:</span></span>

```csharp
using System.Collections.Generic;

#nullable enable
namespace NullableIntroduction
{
    public class SurveyRun
    {
        private List<SurveyQuestion> surveyQuestions = new List<SurveyQuestion>();

        public void AddQuestion(QuestionType type, string question) =>
            AddQuestion(new SurveyQuestion(type, question));
        public void AddQuestion(SurveyQuestion surveyQuestion) => surveyQuestions.Add(surveyQuestion);
    }
}
```

<span data-ttu-id="804ef-180">前と同じように、この一覧オブジェクトを null 以外の値に初期化する必要があります。そうしないとコンパイラによって警告が発行されます。</span><span class="sxs-lookup"><span data-stu-id="804ef-180">As before, you must initialize the list object to a non-null value or the compiler issues a warning.</span></span> <span data-ttu-id="804ef-181">`AddQuestion` の 2 つ目のオーバーロードでは null のチェックは必要ないため、それが実行されることはありません。その変数は null 非許容であることが宣言されています。</span><span class="sxs-lookup"><span data-stu-id="804ef-181">There are no null checks in the second overload of `AddQuestion` because they aren't needed: You've declared that variable to be non-nullable.</span></span> <span data-ttu-id="804ef-182">その値は `null` になることはできません。</span><span class="sxs-lookup"><span data-stu-id="804ef-182">Its value can't be `null`.</span></span>

<span data-ttu-id="804ef-183">お使いのエディターで `Program.cs` に切り替え、`Main` の内容を次のコード行に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="804ef-183">Switch to `Program.cs` in your editor and replace the contents of `Main` with the following lines of code:</span></span>

[!code-csharp[AddQuestions](../../../samples/csharp/NullableIntroduction/NullableIntroduction/Program.cs#AddQuestions)]

<span data-ttu-id="804ef-184">ファイルの先頭に `#nullable enable` プラグマがないため、`AddQuestion` 引数のテキストとして `null` を渡しても、コンパイラによる警告は発行されません。</span><span class="sxs-lookup"><span data-stu-id="804ef-184">Without the `#nullable enable` pragma at the top of the file, the compiler doesn't issue a warning when you pass `null` as the text for the `AddQuestion` argument.</span></span> <span data-ttu-id="804ef-185">`using` ステートメントの次に `#nullable enable` を追加することで、これを修正します。</span><span class="sxs-lookup"><span data-stu-id="804ef-185">Fix that by adding `#nullable enable` following the `using` statement.</span></span> <span data-ttu-id="804ef-186">次の行を `Main` に追加して試してください。</span><span class="sxs-lookup"><span data-stu-id="804ef-186">Try it by adding the following line to `Main`:</span></span>

```csharp
surveyRun.AddQuestion(QuestionType.Text, default);
```

## <a name="create-respondents-and-get-answers-to-the-survey"></a><span data-ttu-id="804ef-187">回答者を作成し、アンケートに対する回答を取得する</span><span class="sxs-lookup"><span data-stu-id="804ef-187">Create respondents and get answers to the survey</span></span>

<span data-ttu-id="804ef-188">次に、アンケートに対する回答を生成するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="804ef-188">Next, write the code that generates answers to the survey.</span></span> <span data-ttu-id="804ef-189">これには、いくつかの小さいタスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="804ef-189">This involves several small tasks:</span></span>

1. <span data-ttu-id="804ef-190">回答者オブジェクトを生成するメソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="804ef-190">Build a method that generates respondent objects.</span></span> <span data-ttu-id="804ef-191">これらは、アンケートへの入力を求められる人物を表します。</span><span class="sxs-lookup"><span data-stu-id="804ef-191">These represent people asked to fill out the survey.</span></span>
1. <span data-ttu-id="804ef-192">回答者にアンケートを依頼し、回答を収集するか、回答者が回答しなかったことを示すデータを収集することをシミュレートするロジックを構築します。</span><span class="sxs-lookup"><span data-stu-id="804ef-192">Build logic to simulate asking the questions to a respondent and collecting answers or noting that a respondent didn't answer.</span></span>
1. <span data-ttu-id="804ef-193">十分な数の回答者がアンケートに回答するまで、これを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="804ef-193">Repeat until enough respondents have answered the survey.</span></span>

<span data-ttu-id="804ef-194">アンケートの回答を表すクラスが必要なので、ここでそれを追加します。</span><span class="sxs-lookup"><span data-stu-id="804ef-194">You'll need a class to represent a survey response, so add that now.</span></span> <span data-ttu-id="804ef-195">null 許容のサポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="804ef-195">Enable nullable support.</span></span> <span data-ttu-id="804ef-196">次のコードに示すように、`Id` プロパティとそれを初期化するコンストラクターを追加します。</span><span class="sxs-lookup"><span data-stu-id="804ef-196">Add an `Id` property and a constructor that initializes it, as shown in the following code:</span></span>

```csharp
#nullable enable
namespace NullableIntroduction
{
    public class SurveyResponse
    {
        public int Id { get; }

        public SurveyResponse(int id) => Id = id;
    }
}
```

<span data-ttu-id="804ef-197">次に、`static` メソッドを追加し、ランダム ID を生成することで新しい参加者を作成します。</span><span class="sxs-lookup"><span data-stu-id="804ef-197">Next, add a `static` method to create new participants by generating a random ID:</span></span>

[!code-csharp[GenerateRespondents](../../../samples/csharp/NullableIntroduction/NullableIntroduction/SurveyResponse.cs#Random)]

<span data-ttu-id="804ef-198">このクラスの主な役割は、アンケートの質問に対する参加者の回答を生成することです。</span><span class="sxs-lookup"><span data-stu-id="804ef-198">The main responsibility of this class is to generate the responses for a participant to the questions in the survey.</span></span> <span data-ttu-id="804ef-199">この役割には、いくつかの手順があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-199">This responsibility has a few steps:</span></span>

1. <span data-ttu-id="804ef-200">アンケートへの参加を依頼します。</span><span class="sxs-lookup"><span data-stu-id="804ef-200">Ask for participation in the survey.</span></span> <span data-ttu-id="804ef-201">回答者が同意しない場合は、応答の欠落 (つまり null) が返されます。</span><span class="sxs-lookup"><span data-stu-id="804ef-201">If the person doesn't consent, return a missing (or null) response.</span></span>
1. <span data-ttu-id="804ef-202">各質問を表示し、回答を記録します。</span><span class="sxs-lookup"><span data-stu-id="804ef-202">Ask each question and record the answer.</span></span> <span data-ttu-id="804ef-203">回答も欠落する (つまり null になる) 可能性があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-203">Each answer may also be missing (or null).</span></span>

<span data-ttu-id="804ef-204">`SurveyRespondent` クラスに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="804ef-204">Add the following code to your `SurveyRespondent` class:</span></span>

[!code-csharp[AnswerSurvey](../../../samples/csharp/NullableIntroduction/NullableIntroduction/SurveyResponse.cs#AnswerSurvey)]

<span data-ttu-id="804ef-205">アンケートの回答用のストレージは `Dictionary<int, string>?` であり、null が可能であることを示しています。</span><span class="sxs-lookup"><span data-stu-id="804ef-205">The storage for the survey answers is a `Dictionary<int, string>?`, indicating that it may be null.</span></span> <span data-ttu-id="804ef-206">新しい言語機能を使用して、コンパイラーと後日コードを読む人の両方に対して、設計意図が宣言されています。</span><span class="sxs-lookup"><span data-stu-id="804ef-206">You're using the new language feature to declare your design intent, both to the compiler and to anyone reading your code later.</span></span> <span data-ttu-id="804ef-207">先に null 値のチェックを行わずに `surveyResponses` を逆参照した場合は、コンパイラの警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="804ef-207">If you ever dereference `surveyResponses` without checking for the null value first, you'll get a compiler warning.</span></span> <span data-ttu-id="804ef-208">`AnswerSurvey` メソッドで警告が表示されないのは、上記で `surveyResponses` 変数が null 以外の値に設定されたことをコンパイラが判断できるためです。</span><span class="sxs-lookup"><span data-stu-id="804ef-208">You don't get a warning in the `AnswerSurvey` method because the compiler can determine the `surveyResponses` variable was set to a non-null value above.</span></span>

<span data-ttu-id="804ef-209">次に、`SurveyRun` クラス内に `PerformSurvey` メソッドを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-209">Next, you need to write the `PerformSurvey` method in the `SurveyRun` class.</span></span> <span data-ttu-id="804ef-210">`SurveyRun` クラスに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="804ef-210">Add the following code in the `SurveyRun` class:</span></span>

[!code-csharp[PerformSurvey](../../../samples/csharp/NullableIntroduction/NullableIntroduction/SurveyRun.cs#PerformSurvey)]

<span data-ttu-id="804ef-211">ここでも、null を許容する `List<SurveyResponse>?` の選択によって、応答で null が可能であることが示されす。</span><span class="sxs-lookup"><span data-stu-id="804ef-211">Here again, your choice of a nullable `List<SurveyResponse>?` indicates the response may be null.</span></span> <span data-ttu-id="804ef-212">これは、アンケートがまだ回答者に表示されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="804ef-212">That indicates the survey hasn't been given to any respondents yet.</span></span> <span data-ttu-id="804ef-213">十分な数の同意が得られるまで回答者が追加されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="804ef-213">Notice that respondents are added until enough have consented.</span></span>

<span data-ttu-id="804ef-214">アンケートを実行する最後の手順は、`Main` メソッドの最後にアンケートを実行する呼び出しを追加することです。</span><span class="sxs-lookup"><span data-stu-id="804ef-214">The last step to run the survey is to add a call to perform the survey at the end of the `Main` method:</span></span>

[!code-csharp[RunSurvey](../../../samples/csharp/NullableIntroduction/NullableIntroduction/Program.cs#RunSurvey)]

## <a name="examine-survey-responses"></a><span data-ttu-id="804ef-215">アンケートの回答を調べる</span><span class="sxs-lookup"><span data-stu-id="804ef-215">Examine survey responses</span></span>

<span data-ttu-id="804ef-216">最後の手順は、アンケートの結果を表示することです。</span><span class="sxs-lookup"><span data-stu-id="804ef-216">The last step is to display survey results.</span></span> <span data-ttu-id="804ef-217">記述したクラスの多くにコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="804ef-217">You'll add code to many of the classes you've written.</span></span> <span data-ttu-id="804ef-218">このコードでは、null 許容参照型と null 非許容参照型を区別する値を示します。</span><span class="sxs-lookup"><span data-stu-id="804ef-218">This code demonstrates the value of distinguishing nullable and non-nullable reference types.</span></span> <span data-ttu-id="804ef-219">`SurveyResponse` クラスに次の 2 つの式形式メンバーを追加することから始めます。</span><span class="sxs-lookup"><span data-stu-id="804ef-219">Start by adding the following two expression-bodied members to the `SurveyResponse` class:</span></span>

[!code-csharp[ReportResponses](../../../samples/csharp/NullableIntroduction/NullableIntroduction/SurveyResponse.cs#SurveyStatus)]

<span data-ttu-id="804ef-220">`surveyResponses` は null 非許容参照であるため、それを逆参照する前に型チェックは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="804ef-220">Because `surveyResponses` is a non-nullable reference, type no checks are necessary before de-referencing it.</span></span> <span data-ttu-id="804ef-221">`Answer` メソッドでは null 以外の文字列が返されるため、既定値の 2 つ目の引数を取得する `GetValueOrDefault` のオーバーロードが選択されます。</span><span class="sxs-lookup"><span data-stu-id="804ef-221">The `Answer` method returns a non-nullable string, so choose the overload of `GetValueOrDefault` that takes a second argument for the default value.</span></span>

<span data-ttu-id="804ef-222">次に、次の 3 つの式形式メンバーを `SurveyRun` クラスに追加します。</span><span class="sxs-lookup"><span data-stu-id="804ef-222">Next, add these three expression-bodied members to the `SurveyRun` class:</span></span>

[!code-csharp[ReportResults](../../../samples/csharp/NullableIntroduction/NullableIntroduction/SurveyRun.cs#RunReport)]

<span data-ttu-id="804ef-223">`AllParticipants` メンバーでは、`respondents` 変数は null の場合があるが、戻り値を null にすることはできないことを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="804ef-223">The `AllParticipants` member must take into account that the `respondents` variable might be null, but the return value can't be null.</span></span> <span data-ttu-id="804ef-224">この式を `??` とその後ろの空のシーケンスを削除することで変更すると、コンパイラーによって、メソッドで `null` が返され、その戻り値のシグネチャで null 非許容型が返される可能性があることが警告されます。</span><span class="sxs-lookup"><span data-stu-id="804ef-224">If you change that expression by removing the `??` and the empty sequence that follows, the compiler warns you the method might return `null` and its return signature returns a non-nullable type.</span></span>

<span data-ttu-id="804ef-225">最後に、次のループを `Main` メソッドの末尾に追加します。</span><span class="sxs-lookup"><span data-stu-id="804ef-225">Finally, add the following loop at the bottom of the `Main` method:</span></span>

[!code-csharp[DisplaySurveyResults](../../../samples/csharp/NullableIntroduction/NullableIntroduction/Program.cs#WriteAnswers)]

<span data-ttu-id="804ef-226">基になるインターフェースを非許容参照型を返すように設計しているため、このコードでは `null` のチェックは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="804ef-226">You don't need any `null` checks in this code because you've designed the underlying interfaces so that they all return non-nullable reference types.</span></span>

## <a name="get-the-code"></a><span data-ttu-id="804ef-227">コードを取得する</span><span class="sxs-lookup"><span data-stu-id="804ef-227">Get the code</span></span>

<span data-ttu-id="804ef-228">[csharp/IntroTonullables](https://github.com/dotnet/samples/tree/master/csharp/NullableIntroduction) フォルダーの [samples](https://github.com/dotnet/samples) リポジトリから、完成したチュートリアルのコードを取得できます。</span><span class="sxs-lookup"><span data-stu-id="804ef-228">You can get the code for the finished tutorial from our [samples](https://github.com/dotnet/samples) repository in the [csharp/IntroToNullables](https://github.com/dotnet/samples/tree/master/csharp/NullableIntroduction) folder.</span></span>

<span data-ttu-id="804ef-229">null 許容参照型と null 非許容参照型の間で型宣言を変更することで試してください。</span><span class="sxs-lookup"><span data-stu-id="804ef-229">Experiment by changing the type declarations between nullable and non-nullable reference types.</span></span> <span data-ttu-id="804ef-230">それによって生成される警告が変わることを確認して、`null` を間違って逆参照することがないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="804ef-230">See how that generates different warnings to ensure you don't accidentally dereference a `null`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="804ef-231">次の手順</span><span class="sxs-lookup"><span data-stu-id="804ef-231">Next steps</span></span>

<span data-ttu-id="804ef-232">null 許容参照型の概要を参照して理解を深めます。</span><span class="sxs-lookup"><span data-stu-id="804ef-232">Learn more by reading an overview of nullable reference types..</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="804ef-233">null 許容参照の概要</span><span class="sxs-lookup"><span data-stu-id="804ef-233">An overview of nullable references</span></span>](../nullable-references.md)
