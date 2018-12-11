---
title: Visual Studio Code での F# の概要します。
description: Visual Studio Code および ionide の概要のプラグインのスイートで F# を使用する方法について説明します。
ms.date: 05/28/2018
ms.openlocfilehash: 2db587b5614c5a7ca9285cad9b719970d53afd55
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53129793"
---
# <a name="get-started-with-f-in-visual-studio-code"></a><span data-ttu-id="33587-103">Visual Studio Code での F# の概要します。</span><span class="sxs-lookup"><span data-stu-id="33587-103">Get Started with F# in Visual Studio Code</span></span>

<span data-ttu-id="33587-104">書き込めるF#で[Visual Studio Code](https://code.visualstudio.com)で、 [Ionide プラグイン](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp)クロス プラットフォームの軽量な統合開発環境 (IDE) ですばらしい体験を IntelliSense および基本的なコードを取得するにはリファクタリング。</span><span class="sxs-lookup"><span data-stu-id="33587-104">You can write F# in [Visual Studio Code](https://code.visualstudio.com) with the [Ionide plugin](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp) to get a great cross-platform, lightweight Integrated Development Environment (IDE) experience with IntelliSense and basic code refactorings.</span></span> <span data-ttu-id="33587-105">参照してください[Ionide.io](http://ionide.io)プラグインの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="33587-105">Visit [Ionide.io](http://ionide.io) to learn more about the plugin.</span></span>

<span data-ttu-id="33587-106">作業を開始できることを確認します。 [F# および ionide の概要プラグインが正しくインストールされている](install-fsharp.md#install-f-with-visual-studio-code)します。</span><span class="sxs-lookup"><span data-stu-id="33587-106">To begin, ensure that you have [F# and the Ionide plugin correctly installed](install-fsharp.md#install-f-with-visual-studio-code).</span></span>

## <a name="creating-your-first-project-with-ionide"></a><span data-ttu-id="33587-107">Ionide の概要と、最初のプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="33587-107">Creating your first project with Ionide</span></span>

<span data-ttu-id="33587-108">新しい F# プロジェクトを作成するには、新しいフォルダー (することができます、どのような名前) に Visual Studio Code を開きます。</span><span class="sxs-lookup"><span data-stu-id="33587-108">To create a new F# project, open Visual Studio Code in a new folder (you can name it whatever you like).</span></span>

<span data-ttu-id="33587-109">次に、コマンド パレットを開いて (**ビュー > コマンド パレット**) と入力します。</span><span class="sxs-lookup"><span data-stu-id="33587-109">Next, open the command palette (**View > Command Palette**) and type the following:</span></span>

```
> F# new project
```

<span data-ttu-id="33587-110">これで電源がオン、[偽造](https://github.com/fsharp-editing/Forge)プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="33587-110">This is powered by the [FORGE](https://github.com/fsharp-editing/Forge) project.</span></span>

> [!NOTE]
> <span data-ttu-id="33587-111">テンプレート オプションが表示されない場合は、コマンド パレットで、次のコマンドを実行してテンプレートを更新してください:`>F#: Refresh Project Templates`します。</span><span class="sxs-lookup"><span data-stu-id="33587-111">If you don't see template options, try refreshing templates by running the following command in the Command Palette: `>F#: Refresh Project Templates`.</span></span>

<span data-ttu-id="33587-112">選択"F#:新しいプロジェクト を押して**Enter**します。</span><span class="sxs-lookup"><span data-stu-id="33587-112">Select "F#: New Project" by hitting **Enter**.</span></span> <span data-ttu-id="33587-113">プロジェクト テンプレートを選択するためには、次の手順に移動します。</span><span class="sxs-lookup"><span data-stu-id="33587-113">This takes you to the next step, which is for selecting a project template.</span></span>

<span data-ttu-id="33587-114">選択、`classlib`テンプレートとヒット**Enter**します。</span><span class="sxs-lookup"><span data-stu-id="33587-114">Pick the `classlib` template and hit **Enter**.</span></span>

<span data-ttu-id="33587-115">次でプロジェクトを作成するディレクトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="33587-115">Next, pick a directory to create the project in.</span></span> <span data-ttu-id="33587-116">空のまま、現在のディレクトリを使用します。</span><span class="sxs-lookup"><span data-stu-id="33587-116">If you leave it blank, it uses the current directory.</span></span>

<span data-ttu-id="33587-117">最後に、最後の手順で、プロジェクトの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="33587-117">Finally, name your project in the final step.</span></span> <span data-ttu-id="33587-118">F#使用して[パスカル ケース](http://c2.com/cgi/wiki?PascalCase)プロジェクト名にします。</span><span class="sxs-lookup"><span data-stu-id="33587-118">F# uses [Pascal case](http://c2.com/cgi/wiki?PascalCase) for project names.</span></span> <span data-ttu-id="33587-119">この記事では`ClassLibraryDemo`名として。</span><span class="sxs-lookup"><span data-stu-id="33587-119">This article uses `ClassLibraryDemo` as the name.</span></span> <span data-ttu-id="33587-120">プロジェクトの名前を入力したら後のヒット**Enter**します。</span><span class="sxs-lookup"><span data-stu-id="33587-120">Once you've entered the name you want for your project, hit **Enter**.</span></span>

<span data-ttu-id="33587-121">前の手順を実行する場合に次のように表示される、左側にある Visual Studio コード ワークスペースを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33587-121">If you followed the previous step, you should get the Visual Studio Code Workspace on the left-hand side to appear with the following:</span></span>

1. <span data-ttu-id="33587-122">F#プロジェクト自体の下に、`ClassLibraryDemo`フォルダー。</span><span class="sxs-lookup"><span data-stu-id="33587-122">The F# project itself, underneath the `ClassLibraryDemo` folder.</span></span>
2. <span data-ttu-id="33587-123">使用してパッケージを追加するための適切なディレクトリ構造[ `Paket`](https://fsprojects.github.io/Paket/)します。</span><span class="sxs-lookup"><span data-stu-id="33587-123">The correct directory structure for adding packages via [`Paket`](https://fsprojects.github.io/Paket/).</span></span>
3. <span data-ttu-id="33587-124">クロス プラットフォーム ビルド スクリプトを[ `FAKE`](https://fsharp.github.io/FAKE/)します。</span><span class="sxs-lookup"><span data-stu-id="33587-124">A cross-platform build script with [`FAKE`](https://fsharp.github.io/FAKE/).</span></span>
4. <span data-ttu-id="33587-125">`paket.exe`実行可能ファイルをパッケージのフェッチし、の依存関係を解決することができます。</span><span class="sxs-lookup"><span data-stu-id="33587-125">The `paket.exe` executable that can fetch packages and resolve dependencies for you.</span></span>
5. <span data-ttu-id="33587-126">A`.gitignore`ファイルを Git ベースのソース管理にこのプロジェクトを追加する場合。</span><span class="sxs-lookup"><span data-stu-id="33587-126">A `.gitignore` file if you wish to add this project to Git-based source control.</span></span>

## <a name="writing-some-code"></a><span data-ttu-id="33587-127">コードの作成</span><span class="sxs-lookup"><span data-stu-id="33587-127">Writing some code</span></span>

<span data-ttu-id="33587-128">開く、 *ClassLibraryDemo*フォルダー。</span><span class="sxs-lookup"><span data-stu-id="33587-128">Open the *ClassLibraryDemo* folder.</span></span>  <span data-ttu-id="33587-129">次のファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="33587-129">You should see the following files:</span></span>

1. <span data-ttu-id="33587-130">`ClassLibraryDemo.fs`で定義されているクラスを使用して F# 実装ファイルです。</span><span class="sxs-lookup"><span data-stu-id="33587-130">`ClassLibraryDemo.fs`, an F# implementation file with a class defined.</span></span>
2. <span data-ttu-id="33587-131">`ClassLibraryDemo.fsproj`、F# プロジェクト ファイルをこのプロジェクトをビルドするために使用します。</span><span class="sxs-lookup"><span data-stu-id="33587-131">`ClassLibraryDemo.fsproj`, an F# project file used to build this project.</span></span>
3. <span data-ttu-id="33587-132">`Script.fsx`、ソース ファイルを読み込む F# スクリプト ファイル。</span><span class="sxs-lookup"><span data-stu-id="33587-132">`Script.fsx`, an F# script file that loads the source file.</span></span>
4. <span data-ttu-id="33587-133">`paket.references`、パケット ファイルをプロジェクトの依存関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="33587-133">`paket.references`, a Paket file that specifies the project dependencies.</span></span>

<span data-ttu-id="33587-134">開いている`Script.fsx`の末尾に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="33587-134">Open `Script.fsx`, and add the following code at the end of it:</span></span>

[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx)]

<span data-ttu-id="33587-135">この関数は、単語の形式に変換します[Pig Latin](https://en.wikipedia.org/wiki/Pig_Latin)します。</span><span class="sxs-lookup"><span data-stu-id="33587-135">This function converts a word to a form of [Pig Latin](https://en.wikipedia.org/wiki/Pig_Latin).</span></span> <span data-ttu-id="33587-136">次の手順では、F# Interactive (FSI) を使用して評価です。</span><span class="sxs-lookup"><span data-stu-id="33587-136">The next step is to evaluate it using F# Interactive (FSI).</span></span>

<span data-ttu-id="33587-137">(11 行である必要があります) 関数全体を強調表示します。</span><span class="sxs-lookup"><span data-stu-id="33587-137">Highlight the entire function (it should be 11 lines long).</span></span> <span data-ttu-id="33587-138">強調表示され後の保持、 **Alt**キーとヒット **」と入力**します。</span><span class="sxs-lookup"><span data-stu-id="33587-138">Once it is highlighted, hold the **Alt** key and hit **Enter**.</span></span> <span data-ttu-id="33587-139">以下に、ポップアップ ウィンドウがわかり、このようなものが表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33587-139">You'll notice a window pop up below, and it should show something like this:</span></span>

![Ionide の概要で F# Interactive の出力の例](media/getting-started-vscode/vscode-fsi.png)

<span data-ttu-id="33587-141">これは、次の 3 つを行いました。</span><span class="sxs-lookup"><span data-stu-id="33587-141">This did three things:</span></span>

1. <span data-ttu-id="33587-142">FSI プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="33587-142">It started the FSI process.</span></span>
2. <span data-ttu-id="33587-143">強調表示したコードは、FSI プロセス上で送信します。</span><span class="sxs-lookup"><span data-stu-id="33587-143">It sent the code you highlighted over the FSI process.</span></span>
3. <span data-ttu-id="33587-144">FSI プロセス経由で送信するコードを評価します。</span><span class="sxs-lookup"><span data-stu-id="33587-144">The FSI process evaluated the code you sent over.</span></span>

<span data-ttu-id="33587-145">経由で送信するため、[関数](../language-reference/functions/index.md)FSI でその関数を呼び出すようになりましたことができます。</span><span class="sxs-lookup"><span data-stu-id="33587-145">Because what you sent over was a [function](../language-reference/functions/index.md), you can now call that function with FSI!</span></span> <span data-ttu-id="33587-146">対話型のウィンドウで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="33587-146">In the interactive window, type the following:</span></span>

```fsharp
toPigLatin "banana";;
```

<span data-ttu-id="33587-147">次の結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="33587-147">You should see the following result:</span></span>

```fsharp
val it : string = "ananabay"
```

<span data-ttu-id="33587-148">ここで、最初の文字としての母音を試してみましょう。</span><span class="sxs-lookup"><span data-stu-id="33587-148">Now, let's try with a vowel as the first letter.</span></span> <span data-ttu-id="33587-149">次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="33587-149">Enter the following:</span></span>

```fsharp
toPigLatin "apple";;
```

<span data-ttu-id="33587-150">次の結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="33587-150">You should see the following result:</span></span>

```fsharp
val it : string = "appleyay"
```

<span data-ttu-id="33587-151">関数は、想定どおりに動作するが表示されます。</span><span class="sxs-lookup"><span data-stu-id="33587-151">The function appears to be working as expected.</span></span> <span data-ttu-id="33587-152">これで、先ほど Visual Studio Code で初めての F# 関数を記述し、FSI を使用して評価すること。</span><span class="sxs-lookup"><span data-stu-id="33587-152">Congratulations, you just wrote your first F# function in Visual Studio Code and evaluated it with FSI!</span></span>

> [!NOTE]
> <span data-ttu-id="33587-153">FSI の明細行がで終了しましたように気付き、`;;`します。</span><span class="sxs-lookup"><span data-stu-id="33587-153">As you may have noticed, the lines in FSI are terminated with `;;`.</span></span> <span data-ttu-id="33587-154">これは、FSI では、複数の行を入力できるためです。</span><span class="sxs-lookup"><span data-stu-id="33587-154">This is because FSI allows you to enter multiple lines.</span></span> <span data-ttu-id="33587-155">`;;`により FSI 確認コードが完了すると、最後にします。</span><span class="sxs-lookup"><span data-stu-id="33587-155">The `;;` at the end lets FSI know when the code is finished.</span></span>

## <a name="explaining-the-code"></a><span data-ttu-id="33587-156">コードの説明</span><span class="sxs-lookup"><span data-stu-id="33587-156">Explaining the code</span></span>

<span data-ttu-id="33587-157">コードが実際に何のことを確認していない場合は、次に、順を追って示します。</span><span class="sxs-lookup"><span data-stu-id="33587-157">If you're not sure about what the code is actually doing, here's a step-by-step.</span></span>

<span data-ttu-id="33587-158">ご覧のとおり、`toPigLatin`関数は、単語の入力として受け取り、その単語の Pig Latin 表現に変換します。</span><span class="sxs-lookup"><span data-stu-id="33587-158">As you can see, `toPigLatin` is a function that takes a word as its input and converts it to a Pig-Latin representation of that word.</span></span> <span data-ttu-id="33587-159">このルールは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="33587-159">The rules for this are as follows:</span></span>

<span data-ttu-id="33587-160">単語の最初の文字が母音で始まる場合は、単語の末尾に"yay"を追加します。</span><span class="sxs-lookup"><span data-stu-id="33587-160">If the first character in a word starts with a vowel, add "yay" to the end of the word.</span></span> <span data-ttu-id="33587-161">、母音で開始しない場合は、その最初の文字を単語の末尾に移動し、を「なります」に追加します。</span><span class="sxs-lookup"><span data-stu-id="33587-161">If it doesn't start with a vowel, move that first character to the end of the word and add "ay" to it.</span></span>

<span data-ttu-id="33587-162">FSI では、次お気付きかもしれません。</span><span class="sxs-lookup"><span data-stu-id="33587-162">You may have noticed the following in FSI:</span></span>

```fsharp
val toPigLatin : word:string -> string
```

<span data-ttu-id="33587-163">示すこの`toPigLatin`で受け取る関数には、`string`入力として (と呼ばれる`word`)、戻って別`string`。</span><span class="sxs-lookup"><span data-stu-id="33587-163">This states that `toPigLatin` is a function that takes in a `string` as input (called `word`), and returns another `string`.</span></span> <span data-ttu-id="33587-164">呼ばれます、[関数の型シグネチャ](https://fsharpforfunandprofit.com/posts/function-signatures/)、基本的な F# コードを理解する鍵は、F# です。</span><span class="sxs-lookup"><span data-stu-id="33587-164">This is known as the [type signature of the function](https://fsharpforfunandprofit.com/posts/function-signatures/), a fundamental piece of F# that's key to understanding F# code.</span></span> <span data-ttu-id="33587-165">また、この場合、Visual Studio Code で関数ポインターを合わせます。</span><span class="sxs-lookup"><span data-stu-id="33587-165">You'll also notice this if you hover over the function in Visual Studio Code.</span></span>

<span data-ttu-id="33587-166">関数の本文で、2 つの異なる部分がわかります。</span><span class="sxs-lookup"><span data-stu-id="33587-166">In the body of the function, you'll notice two distinct parts:</span></span>

1. <span data-ttu-id="33587-167">呼ばれる、内部関数`isVowel`、特定の文字を決定する (`c`) を使用して指定されたパターンのいずれかと一致する場合にチェックして、母音は、[パターン マッチング](../language-reference/pattern-matching.md):</span><span class="sxs-lookup"><span data-stu-id="33587-167">An inner function, called `isVowel`, that determines if a given character (`c`) is a vowel by checking if it matches one of the provided patterns via [Pattern Matching](../language-reference/pattern-matching.md):</span></span>

   [!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx#L2-L6)]

2. <span data-ttu-id="33587-168">[ `if..then..else` ](../language-reference/conditional-expressions-if-then-else.md)かどうかは、最初の文字は、母音と場合、最初の文字ベースの構造は、入力文字列からの戻り値をチェックする式、母音であるか。</span><span class="sxs-lookup"><span data-stu-id="33587-168">An [`if..then..else`](../language-reference/conditional-expressions-if-then-else.md) expression that checks if the first character is a vowel, and constructs a return value out of the input characters based on if the first character was a vowel or not:</span></span>

   [!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx#L8-L11)]

<span data-ttu-id="33587-169">フローの`toPigLatin`なります。</span><span class="sxs-lookup"><span data-stu-id="33587-169">The flow of `toPigLatin` is thus:</span></span>

<span data-ttu-id="33587-170">入力の単語の最初の文字の母音であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="33587-170">Check if the first character of the input word is a vowel.</span></span> <span data-ttu-id="33587-171">場合は、"yay"という単語の末尾にアタッチします。</span><span class="sxs-lookup"><span data-stu-id="33587-171">If it is, attach "yay" to the end of the word.</span></span> <span data-ttu-id="33587-172">それ以外の場合、その最初の文字を単語の末尾に移動し、それを「なります」に追加します。</span><span class="sxs-lookup"><span data-stu-id="33587-172">Otherwise, move that first character to the end of the word and add "ay" to it.</span></span>

<span data-ttu-id="33587-173">1 つの最後にこれに関する注意: その他の多くの言語とは異なり、関数から返される明示的な命令はありません。</span><span class="sxs-lookup"><span data-stu-id="33587-173">There's one final thing to notice about this: there's no explicit instruction to return from the function, unlike many other languages out there.</span></span> <span data-ttu-id="33587-174">これは、ためF#が式に基づいて、関数の本体の最後の式は、戻り値。</span><span class="sxs-lookup"><span data-stu-id="33587-174">This is because F# is Expression-based, and the last expression in the body of a function is the return value.</span></span> <span data-ttu-id="33587-175">`if..then..else`自体、式の本体では、`then`ブロックまたはの本文、`else`ブロックが入力値によって返されます。</span><span class="sxs-lookup"><span data-stu-id="33587-175">Because `if..then..else` is itself an expression, the body of the `then` block or the body of the `else` block will be returned depending on the input value.</span></span>

## <a name="moving-your-script-code-into-the-implementation-file"></a><span data-ttu-id="33587-176">スクリプト コードを実装ファイルに移動</span><span class="sxs-lookup"><span data-stu-id="33587-176">Moving your script code into the implementation file</span></span>

<span data-ttu-id="33587-177">この記事では、前のセクションには、F# コードの記述の一般的な最初の手順が示されています。 最初の関数の記述と、FSI 使用して対話的に実行します。</span><span class="sxs-lookup"><span data-stu-id="33587-177">The previous sections in this article demonstrated a common first step in writing F# code: writing an initial function and executing it interactively with FSI.</span></span> <span data-ttu-id="33587-178">これは、REPL 駆動型開発と呼ばれます、 [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) 「読み取り評価印刷ループ」を意味します。</span><span class="sxs-lookup"><span data-stu-id="33587-178">This is known as REPL-driven development, where [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) stands for "Read-Evaluate-Print Loop".</span></span> <span data-ttu-id="33587-179">機能を試して動作ものがある場合する優れた方法です。</span><span class="sxs-lookup"><span data-stu-id="33587-179">It's a great way to experiment with functionality until you have something working.</span></span>

<span data-ttu-id="33587-180">REPL 駆動型開発の次の手順では、作業コード F# 実装ファイルに移動します。</span><span class="sxs-lookup"><span data-stu-id="33587-180">The next step in REPL-driven development is to move working code into an F# implementation file.</span></span> <span data-ttu-id="33587-181">これは、実行可能なアセンブリの F# コンパイラによってコンパイルできます。</span><span class="sxs-lookup"><span data-stu-id="33587-181">It can then be compiled by the F# compiler into an assembly that can be executed.</span></span>

<span data-ttu-id="33587-182">まず、開きます`ClassLibraryDemo.fs`します。</span><span class="sxs-lookup"><span data-stu-id="33587-182">To begin, open `ClassLibraryDemo.fs`.</span></span>  <span data-ttu-id="33587-183">いくつかのコードが既にに存在することがわかります。</span><span class="sxs-lookup"><span data-stu-id="33587-183">You'll notice that some code is already in there.</span></span> <span data-ttu-id="33587-184">前方に移動し、クラス定義を削除しますがのままにすることを確認、 [ `namespace` ](../language-reference/namespaces.md)上部にある宣言します。</span><span class="sxs-lookup"><span data-stu-id="33587-184">Go ahead and delete the class definition, but make sure to leave the [`namespace`](../language-reference/namespaces.md) declaration at the top.</span></span>

<span data-ttu-id="33587-185">次に、作成、新しい[ `module` ](../language-reference/modules.md)と呼ばれる`PigLatin`をコピーし、`toPigLatin`ように関数。</span><span class="sxs-lookup"><span data-stu-id="33587-185">Next, create a new [`module`](../language-reference/modules.md) called `PigLatin` and copy the `toPigLatin` function into it as such:</span></span>

[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]

<span data-ttu-id="33587-186">次に、開く、`Script.fsx`ファイルを再び、および全体を削除`toPigLatin`ファイルに次の 2 つの行を保持することを確認しますが、機能します。</span><span class="sxs-lookup"><span data-stu-id="33587-186">Next, open the `Script.fsx` file again, and delete the entire `toPigLatin` function, but make sure to keep the following two lines in the file:</span></span>

```fsharp
#load "ClassLibraryDemo.fs"
open ClassLibraryDemo
```

<span data-ttu-id="33587-187">FSI を読み込むスクリプトの最初の行が必要な`ClassLibraryDemo.fs`します。</span><span class="sxs-lookup"><span data-stu-id="33587-187">The first line is needed for FSI scripting to load `ClassLibraryDemo.fs`.</span></span> <span data-ttu-id="33587-188">2 行目、便利なのです。 省略することは省略可能では、入力する必要があります`open ClassLibraryDemo`FSI ウィンドウを表示する場合に、`ToPigLatin`モジュールをスコープに。</span><span class="sxs-lookup"><span data-stu-id="33587-188">The second line is a convenience: omitting it is optional, but you will need to type `open ClassLibraryDemo` in an FSI window if you wish to bring the `ToPigLatin` module into scope.</span></span>

<span data-ttu-id="33587-189">次に、FSI ウィンドウで、使用して、関数を呼び出して、`PigLatin`前に定義したモジュール。</span><span class="sxs-lookup"><span data-stu-id="33587-189">Next, in the FSI window, call the function with the `PigLatin` module that you defined earlier:</span></span>

```
> PigLatin.toPigLatin "banana";;
val it : string = "ananabay"
> PigLatin.toPigLatin "apple";;
val it : string = "appleyay"
```

<span data-ttu-id="33587-190">正常に完了</span><span class="sxs-lookup"><span data-stu-id="33587-190">Success!</span></span> <span data-ttu-id="33587-191">取得する前に、同じ結果が、F# 実装ファイルから読み込まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="33587-191">You get the same results as before, but now loaded from an F# implementation file.</span></span> <span data-ttu-id="33587-192">ここでの主な違いは、F# ソース ファイルが FSI 内だけでなく、どこにでも実行できるアセンブリにコンパイルされます。</span><span class="sxs-lookup"><span data-stu-id="33587-192">The major difference here is that F# source files are compiled into assemblies that can be executed anywhere, not just in FSI.</span></span>

## <a name="summary"></a><span data-ttu-id="33587-193">まとめ</span><span class="sxs-lookup"><span data-stu-id="33587-193">Summary</span></span>

<span data-ttu-id="33587-194">この記事では、次の学習できました。</span><span class="sxs-lookup"><span data-stu-id="33587-194">In this article, you've learned:</span></span>

1. <span data-ttu-id="33587-195">Ionide の概要を使用して Visual Studio Code を設定する方法。</span><span class="sxs-lookup"><span data-stu-id="33587-195">How to set up Visual Studio Code with Ionide.</span></span>
2. <span data-ttu-id="33587-196">Ionide の概要で初めての F# プロジェクトを作成する方法。</span><span class="sxs-lookup"><span data-stu-id="33587-196">How to create your first F# project with Ionide.</span></span>
3. <span data-ttu-id="33587-197">F# スクリプトを使用して、ionide の概要で初めての F# 関数を記述し、FSI で実行する方法。</span><span class="sxs-lookup"><span data-stu-id="33587-197">How to use F# Scripting to write your first F# function in Ionide and then execute it in FSI.</span></span>
4. <span data-ttu-id="33587-198">スクリプトを移行する方法を使用して、F# ソース コード、FSI からそのコードを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="33587-198">How to migrate your script code to F# source and then call that code from FSI.</span></span>

<span data-ttu-id="33587-199">コードより F# Visual Studio Code および ionide の概要を使用して書き込むが組み込まれました。</span><span class="sxs-lookup"><span data-stu-id="33587-199">You're now equipped to write much more F# code using Visual Studio Code and Ionide.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="33587-200">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="33587-200">Troubleshooting</span></span>

<span data-ttu-id="33587-201">次に遭遇する可能性のある特定の問題のトラブルシューティングを行うことがいくつかの方法を示します。</span><span class="sxs-lookup"><span data-stu-id="33587-201">Here are a few ways you can troubleshoot certain problems that you might run into:</span></span>

1. <span data-ttu-id="33587-202">Ionide の概要の編集機能をコードを取得するには、F# ファイルはディスク、および Visual Studio Code ワークスペースで開いているフォルダー内に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33587-202">To get the code editing features of Ionide, your F# files need to be saved to disk and inside of a folder that is open in the Visual Studio Code workspace.</span></span>
2. <span data-ttu-id="33587-203">場合は、システムを変更または開いている Visual Studio のコードと共に ionide の概要の前提条件をインストールしたら、Visual Studio Code を再起動します。</span><span class="sxs-lookup"><span data-stu-id="33587-203">If you've made changes to your system or installed Ionide prerequisites with Visual Studio Code open, restart Visual Studio Code.</span></span>
3. <span data-ttu-id="33587-204">使用できることを確認、F#コンパイラとF#完全修飾パスを使用せずにコマンドラインから対話型です。</span><span class="sxs-lookup"><span data-stu-id="33587-204">Check that you can use the F# compiler and F# interactive from the command line without a fully-qualified path.</span></span> <span data-ttu-id="33587-205">」と入力して行うことができます`fsc`、F# コンパイラのコマンドラインで、`fsi`または`fsharpi`の Visual F# ツールの Windows、Mac または Linux での Mono でそれぞれします。</span><span class="sxs-lookup"><span data-stu-id="33587-205">You can do so by typing `fsc` in a command line for the F# compiler, and `fsi` or `fsharpi` for the Visual F# tools on Windows and Mono on Mac/Linux, respectively.</span></span>
4. <span data-ttu-id="33587-206">プロジェクトのディレクトリで無効な文字があれば、ionide の概要が動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="33587-206">If you have invalid characters in your project directories, Ionide might not work.</span></span>  <span data-ttu-id="33587-207">これに該当する場合、プロジェクト ディレクトリの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="33587-207">Rename your project directories if this is the case.</span></span>
5. <span data-ttu-id="33587-208">Ionide コマンドのいずれも作業している場合、 [Visual Studio Code の keybindings](https://code.visualstudio.com/docs/customization/keybindings#_customizing-shortcuts)を誤って上書きしているかどうかを参照してください。</span><span class="sxs-lookup"><span data-stu-id="33587-208">If none of the Ionide commands are working, check your [Visual Studio Code keybindings](https://code.visualstudio.com/docs/customization/keybindings#_customizing-shortcuts) to see if you're overriding them by accident.</span></span>
6. <span data-ttu-id="33587-209">Ionide の概要は、コンピューターに分割すると、上記のいずれが問題を修正、削除してみてください、`ionide-fsharp`コンピューターにディレクトリ プラグイン スイートを再インストールします。</span><span class="sxs-lookup"><span data-stu-id="33587-209">If Ionide is broken on your machine and none of the above has fixed your problem, try removing the `ionide-fsharp` directory on your machine and reinstall the plugin suite.</span></span>

<span data-ttu-id="33587-210">Ionide の概要とは、構築および F# コミュニティのメンバーによって管理されるオープン ソース プロジェクトです。</span><span class="sxs-lookup"><span data-stu-id="33587-210">Ionide is an open source project built and maintained by members of the F# community.</span></span> <span data-ttu-id="33587-211">問題を報告し、気軽に投稿にしてください、 [Ionide VSCode:FSharp GitHub リポジトリ](https://github.com/ionide/ionide-vscode-fsharp)します。</span><span class="sxs-lookup"><span data-stu-id="33587-211">Please report issues and feel free to contribute at the [Ionide-VSCode: FSharp GitHub repository](https://github.com/ionide/ionide-vscode-fsharp).</span></span>

<span data-ttu-id="33587-212">レポートに問題がある場合に従ってください[問題を報告するときに使用するログを取得するための指示](https://github.com/ionide/ionide-vscode-fsharp#how-to-get-logs-for-debugging--issue-reporting)します。</span><span class="sxs-lookup"><span data-stu-id="33587-212">If you have an issue to report, please follow [the instructions for getting logs to use when reporting an issue](https://github.com/ionide/ionide-vscode-fsharp#how-to-get-logs-for-debugging--issue-reporting).</span></span>

<span data-ttu-id="33587-213">Ionide の概要開発者および F# コミュニティからさらにヘルプを求めることも、 [Ionide Gitter チャネル](https://gitter.im/ionide/ionide-project)します。</span><span class="sxs-lookup"><span data-stu-id="33587-213">You can also ask for further help from the Ionide developers and F# community in the [Ionide Gitter channel](https://gitter.im/ionide/ionide-project).</span></span>

## <a name="next-steps"></a><span data-ttu-id="33587-214">次の手順</span><span class="sxs-lookup"><span data-stu-id="33587-214">Next steps</span></span>

<span data-ttu-id="33587-215">F# と言語の機能の詳細については、チェック アウト[F# のツアー](../tour.md)します。</span><span class="sxs-lookup"><span data-stu-id="33587-215">To learn more about F# and the features of the language, check out [Tour of F#](../tour.md).</span></span>
