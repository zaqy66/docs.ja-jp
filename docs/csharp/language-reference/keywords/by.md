---
title: by コンテキスト キーワード (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- by
- by_CSharpKeyword
helpviewer_keywords:
- by keyword [C#]
ms.assetid: efe6f0e3-be40-4df2-a144-c7db968ae052
ms.openlocfilehash: b2d9b08378dd0edf37c07663b3fe37a09f8acf47
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43524503"
---
# <a name="by-c-reference"></a><span data-ttu-id="f02b4-102">by (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="f02b4-102">by (C# Reference)</span></span>

<span data-ttu-id="f02b4-103">`by` コンテキスト キーワードは、クエリ式の `group` 句で使用され、返される項目をグループ化する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="f02b4-103">The `by` contextual keyword is used in the `group` clause in a query expression to specify how the returned items should be grouped.</span></span> <span data-ttu-id="f02b4-104">詳しくは、「[group 句](../../../csharp/language-reference/keywords/group-clause.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f02b4-104">For more information, see [group clause](../../../csharp/language-reference/keywords/group-clause.md).</span></span>

## <a name="example"></a><span data-ttu-id="f02b4-105">例</span><span class="sxs-lookup"><span data-stu-id="f02b4-105">Example</span></span>

<span data-ttu-id="f02b4-106">`group` 句での `by` コンテキスト キーワードの使用例を次に示します。ここでは、各学生の姓の 1 文字目に従って学生をグループ化するように指定しています。</span><span class="sxs-lookup"><span data-stu-id="f02b4-106">The following example shows the use of the `by` contextual keyword in a `group` clause to specify that the students should be grouped according to the first letter of the last name of each student.</span></span>

[!code-csharp[csrefKeywordsContextual#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#10)]

## <a name="see-also"></a><span data-ttu-id="f02b4-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="f02b4-107">See also</span></span>

- [<span data-ttu-id="f02b4-108">LINQ クエリ式</span><span class="sxs-lookup"><span data-stu-id="f02b4-108">LINQ Query Expressions</span></span>](../../../csharp/programming-guide/linq-query-expressions/index.md)
