---
title: オブジェクトのコレクションの照会 (C# での LINQ)
description: C# で LINQ を使用して、コレクションを照会する方法について説明します。
ms.date: 11/30/2016
ms.assetid: 87a76f8a-0b58-4791-90ea-2fe0a30416c9
ms.openlocfilehash: 87c7bbe789c165a6e189231df1979fc264a34dce
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37403922"
---
# <a name="query-a-collection-of-objects"></a><span data-ttu-id="f487f-103">オブジェクトのコレクションの照会</span><span class="sxs-lookup"><span data-stu-id="f487f-103">Query a collection of objects</span></span>

<span data-ttu-id="f487f-104">この例では、`Student` オブジェクトのリストに対してシンプルなクエリを実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f487f-104">This example shows how to perform a simple query over a list of `Student` objects.</span></span> <span data-ttu-id="f487f-105">各 `Student` オブジェクトには、生徒に関する基本情報と、4 回の試験での生徒の点数を表すリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f487f-105">Each `Student` object contains some basic information about the student, and a list that represents the student's scores on four examinations.</span></span>  
  
<span data-ttu-id="f487f-106">このアプリケーションは、同じ `students` データ ソースを使用する、このセクション内のその他多くの例のフレームワークとして機能します。</span><span class="sxs-lookup"><span data-stu-id="f487f-106">This application serves as the framework for many other examples in this section that use the same `students` data source.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f487f-107">例</span><span class="sxs-lookup"><span data-stu-id="f487f-107">Example</span></span>

<span data-ttu-id="f487f-108">次のクエリは、最初の試験で 90 点以上を取った学生を返します。</span><span class="sxs-lookup"><span data-stu-id="f487f-108">The following query returns the students who received a score of 90 or greater on their first exam.</span></span>  
  
[!code-csharp[csProgGuideLINQ#15](~/samples/snippets/csharp/concepts/linq/how-to-query-a-collection-of-objects_1.cs)]  
  
<span data-ttu-id="f487f-109">このクエリは、実験用として意図的にシンプルに記述されています。</span><span class="sxs-lookup"><span data-stu-id="f487f-109">This query is intentionally simple to enable you to experiment.</span></span> <span data-ttu-id="f487f-110">たとえば、`where` 句でより多く条件を試したり、`orderby` 句を使用して結果を並べ替えたりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f487f-110">For example, you can try more conditions in the `where` clause, or use an `orderby` clause to sort the results.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f487f-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="f487f-111">See also</span></span>

[<span data-ttu-id="f487f-112">統合言語クエリ (LINQ)</span><span class="sxs-lookup"><span data-stu-id="f487f-112">Language Integrated Query (LINQ)</span></span>](index.md)  
[<span data-ttu-id="f487f-113">文字列補間</span><span class="sxs-lookup"><span data-stu-id="f487f-113">String interpolation</span></span>](../language-reference/tokens/interpolated.md)