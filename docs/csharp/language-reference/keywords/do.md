---
title: do (C# リファレンス)
ms.date: 05/28/2018
f1_keywords:
- do_CSharpKeyword
- do
helpviewer_keywords:
- do keyword [C#]
ms.assetid: 50725f79-9ba6-4898-aa78-6e331568a1bb
ms.openlocfilehash: 89c13f5b547c13052e229ff6eb3a39ae5babce41
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932388"
---
# <a name="do-c-reference"></a><span data-ttu-id="844e0-102">do (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="844e0-102">do (C# Reference)</span></span>

<span data-ttu-id="844e0-103">`do` ステートメントでは、指定されたブール式が `true` と評価される間に、ステートメントまたはステートメント ブロックが実行されます。</span><span class="sxs-lookup"><span data-stu-id="844e0-103">The `do` statement executes a statement or a block of statements while a specified boolean expression evaluates to `true`.</span></span> <span data-ttu-id="844e0-104">ループの各実行の後に式が評価されるため、`do-while` ループは 1 回以上実行されます。</span><span class="sxs-lookup"><span data-stu-id="844e0-104">Because that expression is evaluated after each execution of the loop, a `do-while` loop executes one or more times.</span></span> <span data-ttu-id="844e0-105">[while](while.md) ループは、これとは異なり、0 回以上実行されます。</span><span class="sxs-lookup"><span data-stu-id="844e0-105">This differs from the [while](while.md) loop, which executes zero or more times.</span></span>

<span data-ttu-id="844e0-106">`do` ステートメント ブロック内の任意の位置で、[break](break.md) ステートメントを使用してループを抜けることができます。</span><span class="sxs-lookup"><span data-stu-id="844e0-106">At any point within the `do` statement block, you can break out of the loop by using the [break](break.md) statement.</span></span>

<span data-ttu-id="844e0-107">[continue](continue.md) ステートメントを使用すると、`while` 式の評価に直接ステップ実行できます。</span><span class="sxs-lookup"><span data-stu-id="844e0-107">You can step directly to the evaluation of the `while` expression by using the [continue](continue.md) statement.</span></span> <span data-ttu-id="844e0-108">式の評価が `true` の場合、ループの最初のステートメントから実行が続行されます。</span><span class="sxs-lookup"><span data-stu-id="844e0-108">If the expression evaluates to `true`, execution continues at the first statement in the loop.</span></span> <span data-ttu-id="844e0-109">それ以外の場合、実行は、ループの後の最初のステートメントから続行されます。</span><span class="sxs-lookup"><span data-stu-id="844e0-109">Otherwise, execution continues at the first statement after the loop.</span></span>

<span data-ttu-id="844e0-110">また、[goto](goto.md)、[return](return.md)、[throw](throw.md) ステートメントのいずれかを使って `do-while` ループを終了することもできます。</span><span class="sxs-lookup"><span data-stu-id="844e0-110">You also can exit a `do-while` loop by the [goto](goto.md), [return](return.md), or [throw](throw.md) statements.</span></span>

## <a name="example"></a><span data-ttu-id="844e0-111">例</span><span class="sxs-lookup"><span data-stu-id="844e0-111">Example</span></span>

<span data-ttu-id="844e0-112">`do` ステートメントの使用方法を次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="844e0-112">The following example shows the usage of the `do` statement.</span></span> <span data-ttu-id="844e0-113">**[実行]** を選択して、コード例を実行します。</span><span class="sxs-lookup"><span data-stu-id="844e0-113">Select **Run** to run the example code.</span></span> <span data-ttu-id="844e0-114">その後に、コードを変更し、もう一度実行することができます。</span><span class="sxs-lookup"><span data-stu-id="844e0-114">After that you can modify the code and run it again.</span></span>

[!code-csharp-interactive[do loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#4)]

## <a name="c-language-specification"></a><span data-ttu-id="844e0-115">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="844e0-115">C# language specification</span></span>

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="844e0-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="844e0-116">See also</span></span>

- [<span data-ttu-id="844e0-117">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="844e0-117">C# Reference</span></span>](../index.md)  
- [<span data-ttu-id="844e0-118">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="844e0-118">C# Programming Guide</span></span>](../../programming-guide/index.md)  
- [<span data-ttu-id="844e0-119">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="844e0-119">C# Keywords</span></span>](index.md)  
- [<span data-ttu-id="844e0-120">do-while ステートメント (C++)</span><span class="sxs-lookup"><span data-stu-id="844e0-120">do-while Statement (C++)</span></span>](/cpp/cpp/do-while-statement-cpp)  
- [<span data-ttu-id="844e0-121">繰り返しステートメント</span><span class="sxs-lookup"><span data-stu-id="844e0-121">Iteration Statements</span></span>](iteration-statements.md)  
- [<span data-ttu-id="844e0-122">while ステートメント</span><span class="sxs-lookup"><span data-stu-id="844e0-122">while statement</span></span>](while.md)  
