---
title: try-catch-finally (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- catch-finally_CSharpKeyword
- catch-finally
helpviewer_keywords:
- finally blocks [C#]
- try-catch statement [C#]
ms.assetid: a1b443b0-ff7a-43ab-b835-0cc9bfbd15ca
ms.openlocfilehash: 18625838bd36d9d32079b7c72ded7ed660b8cf3a
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53130664"
---
# <a name="try-catch-finally-c-reference"></a><span data-ttu-id="d7e35-102">try-catch-finally (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="d7e35-102">try-catch-finally (C# Reference)</span></span>

<span data-ttu-id="d7e35-103">通常、`catch` および `finally` は、`try` ブロックのリソースを取得して使用する場合に、対で記述されます。`catch` ブロックで例外的な状況を処理し、`finally` ブロックでリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="d7e35-103">A common usage of `catch` and `finally` together is to obtain and use resources in a `try` block, deal with exceptional circumstances in a `catch` block, and release the resources in the `finally` block.</span></span>

 <span data-ttu-id="d7e35-104">例外の再スローの使用例を含む詳細については、「[try-catch](try-catch.md)」および[例外のスロー](../../../standard/exceptions/index.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d7e35-104">For more information and examples on re-throwing exceptions, see [try-catch](try-catch.md) and [Throwing Exceptions](../../../standard/exceptions/index.md).</span></span> <span data-ttu-id="d7e35-105">`finally` ブロックの詳細については、「[try-finally](try-finally.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7e35-105">For more information about the `finally` block, see [try-finally](try-finally.md).</span></span>

## <a name="example"></a><span data-ttu-id="d7e35-106">例</span><span class="sxs-lookup"><span data-stu-id="d7e35-106">Example</span></span>

[!code-csharp[csrefKeywordsExceptions#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsExceptions/CS/csrefKeywordsExceptions.cs#1)]  

## <a name="c-language-specification"></a><span data-ttu-id="d7e35-107">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="d7e35-107">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="d7e35-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7e35-108">See also</span></span>

- [<span data-ttu-id="d7e35-109">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="d7e35-109">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="d7e35-110">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="d7e35-110">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="d7e35-111">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="d7e35-111">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="d7e35-112">try、throw、catch ステートメント (C++)</span><span class="sxs-lookup"><span data-stu-id="d7e35-112">try, throw, and catch Statements (C++)</span></span>](/cpp/cpp/try-throw-and-catch-statements-cpp)
- [<span data-ttu-id="d7e35-113">例外処理ステートメント</span><span class="sxs-lookup"><span data-stu-id="d7e35-113">Exception Handling Statements</span></span>](exception-handling-statements.md)
- [<span data-ttu-id="d7e35-114">throw</span><span class="sxs-lookup"><span data-stu-id="d7e35-114">throw</span></span>](throw.md)
- [<span data-ttu-id="d7e35-115">方法: 例外を明示的にスローする</span><span class="sxs-lookup"><span data-stu-id="d7e35-115">How to: Explicitly Throw Exceptions</span></span>](../../../standard/exceptions/how-to-explicitly-throw-exceptions.md)
- [<span data-ttu-id="d7e35-116">using ステートメント</span><span class="sxs-lookup"><span data-stu-id="d7e35-116">using Statement</span></span>](using-statement.md)