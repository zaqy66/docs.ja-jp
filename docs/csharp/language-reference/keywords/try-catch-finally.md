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
ms.openlocfilehash: b60a1e17f02d7a04b782c661f2b99a28403997eb
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43510099"
---
# <a name="try-catch-finally-c-reference"></a><span data-ttu-id="2b8b6-102">try-catch-finally (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="2b8b6-102">try-catch-finally (C# Reference)</span></span>
<span data-ttu-id="2b8b6-103">通常、`catch` および `finally` は、`try` ブロックのリソースを取得して使用する場合に、対で記述されます。`catch` ブロックで例外的な状況を処理し、`finally` ブロックでリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="2b8b6-103">A common usage of `catch` and `finally` together is to obtain and use resources in a `try` block, deal with exceptional circumstances in a `catch` block, and release the resources in the `finally` block.</span></span>  
  
 <span data-ttu-id="2b8b6-104">例外の再スローの使用例を含む詳細については、「[try-catch](../../../csharp/language-reference/keywords/try-catch.md)」および[例外のスロー](../../../standard/exceptions/index.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2b8b6-104">For more information and examples on re-throwing exceptions, see [try-catch](../../../csharp/language-reference/keywords/try-catch.md) and [Throwing Exceptions](../../../standard/exceptions/index.md).</span></span> <span data-ttu-id="2b8b6-105">`finally` ブロックの詳細については、「[try-finally](../../../csharp/language-reference/keywords/try-finally.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b8b6-105">For more information about the `finally` block, see [try-finally](../../../csharp/language-reference/keywords/try-finally.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2b8b6-106">例</span><span class="sxs-lookup"><span data-stu-id="2b8b6-106">Example</span></span>  
 [!code-csharp[csrefKeywordsExceptions#1](../../../csharp/language-reference/keywords/codesnippet/CSharp/try-catch-finally_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="2b8b6-107">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="2b8b6-107">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="2b8b6-108">参照</span><span class="sxs-lookup"><span data-stu-id="2b8b6-108">See Also</span></span>

- [<span data-ttu-id="2b8b6-109">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="2b8b6-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="2b8b6-110">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="2b8b6-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="2b8b6-111">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="2b8b6-111">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="2b8b6-112">try、throw、catch ステートメント (C++)</span><span class="sxs-lookup"><span data-stu-id="2b8b6-112">try, throw, and catch Statements (C++)</span></span>](/cpp/cpp/try-throw-and-catch-statements-cpp)  
- [<span data-ttu-id="2b8b6-113">例外処理ステートメント</span><span class="sxs-lookup"><span data-stu-id="2b8b6-113">Exception Handling Statements</span></span>](../../../csharp/language-reference/keywords/exception-handling-statements.md)  
- [<span data-ttu-id="2b8b6-114">throw</span><span class="sxs-lookup"><span data-stu-id="2b8b6-114">throw</span></span>](../../../csharp/language-reference/keywords/throw.md)  
- [<span data-ttu-id="2b8b6-115">方法: 例外を明示的にスローする</span><span class="sxs-lookup"><span data-stu-id="2b8b6-115">How to: Explicitly Throw Exceptions</span></span>](../../../standard/exceptions/how-to-explicitly-throw-exceptions.md)  
- [<span data-ttu-id="2b8b6-116">using ステートメント</span><span class="sxs-lookup"><span data-stu-id="2b8b6-116">using Statement</span></span>](../../../csharp/language-reference/keywords/using-statement.md)
