---
title: return (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- return_CSharpKeyword
- return
helpviewer_keywords:
- return statement [C#]
- return keyword [C#]
ms.assetid: 6da6e152-5b58-4448-8f3f-470dd0617ecd
ms.openlocfilehash: 29d2b8e28ae6240b9d06b82695efe1736404c5cb
ms.sourcegitcommit: 70c76a12449439bac0f7a359866be5a0311ce960
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/25/2018
ms.locfileid: "39244778"
---
# <a name="return-c-reference"></a><span data-ttu-id="da923-102">return (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="da923-102">return (C# Reference)</span></span>
<span data-ttu-id="da923-103">`return` ステートメントは、メソッドの実行を終了し、呼び出し側のメソッドに制御を戻します。</span><span class="sxs-lookup"><span data-stu-id="da923-103">The `return` statement terminates execution of the method in which it appears and returns control to the calling method.</span></span> <span data-ttu-id="da923-104">省略可能な値を返すこともできます。</span><span class="sxs-lookup"><span data-stu-id="da923-104">It can also return an optional value.</span></span> <span data-ttu-id="da923-105">メソッドが `void` 型の場合、`return` ステートメントは省略できます。</span><span class="sxs-lookup"><span data-stu-id="da923-105">If the method is a `void` type, the `return` statement can be omitted.</span></span>  
  
 <span data-ttu-id="da923-106">return ステートメントが `try` ブロック内にある場合は、制御が呼び出し側のメソッドに返される前に、`finally` ブロック (存在する場合) が実行されます。</span><span class="sxs-lookup"><span data-stu-id="da923-106">If the return statement is inside a `try` block, the `finally` block, if one exists, will be executed before control returns to the calling method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="da923-107">例</span><span class="sxs-lookup"><span data-stu-id="da923-107">Example</span></span>  
 <span data-ttu-id="da923-108">次の例では、メソッド `CalculateArea()` がローカル変数 `area` を [double](../../../csharp/language-reference/keywords/double.md) 値として返します。</span><span class="sxs-lookup"><span data-stu-id="da923-108">In the following example, the method `CalculateArea()` returns the local variable `area` as a [double](../../../csharp/language-reference/keywords/double.md) value.</span></span>  
  
 [!code-csharp[csrefKeywordsJump#6](../../../csharp/language-reference/keywords/codesnippet/CSharp/return_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="da923-109">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="da923-109">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="da923-110">参照</span><span class="sxs-lookup"><span data-stu-id="da923-110">See Also</span></span>  
 [<span data-ttu-id="da923-111">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="da923-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="da923-112">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="da923-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="da923-113">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="da923-113">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="da923-114">return ステートメント</span><span class="sxs-lookup"><span data-stu-id="da923-114">return Statement</span></span>](/cpp/cpp/return-statement-cpp)  
 [<span data-ttu-id="da923-115">ジャンプ ステートメント</span><span class="sxs-lookup"><span data-stu-id="da923-115">Jump Statements</span></span>](../../../csharp/language-reference/keywords/jump-statements.md)
