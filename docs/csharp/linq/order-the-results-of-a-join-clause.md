---
title: join 句の結果の順序指定 (C# での LINQ)
description: C# で LINQ join 句の結果の順序を指定する方法について説明します。
ms.date: 12/1/2016
ms.assetid: a7458901-1201-4c25-b8d9-c04ca52e0eb9
ms.openlocfilehash: 13cd6cb202cf67def17310db6d98e368ce837646
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43516987"
---
# <a name="order-the-results-of-a-join-clause"></a><span data-ttu-id="ed626-103">join 句の結果の順序指定</span><span class="sxs-lookup"><span data-stu-id="ed626-103">Order the results of a join clause</span></span>

<span data-ttu-id="ed626-104">この例では、結合操作の結果の順序を指定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ed626-104">This example shows how to order the results of a join operation.</span></span> <span data-ttu-id="ed626-105">順序付けは結合後に実行されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ed626-105">Note that the ordering is performed after the join.</span></span> <span data-ttu-id="ed626-106">結合の前に 1 つ以上のソース シーケンスを指定した `orderby` 句を使用することもできますが、一般にこの方法は推奨されません。</span><span class="sxs-lookup"><span data-stu-id="ed626-106">Although you can use an `orderby` clause with one or more of the source sequences before the join, generally we do not recommend it.</span></span> <span data-ttu-id="ed626-107">LINQ プロバイダーによっては、結合後にその順序付けを維持しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="ed626-107">Some LINQ providers might not preserve that ordering after the join.</span></span>

## <a name="example"></a><span data-ttu-id="ed626-108">例</span><span class="sxs-lookup"><span data-stu-id="ed626-108">Example</span></span>

<span data-ttu-id="ed626-109">このクエリは、グループ結合を作成した後、スコープ内に残っているカテゴリ要素に基づいてグループを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="ed626-109">This query creates a group join, and then sorts the groups based on the category element, which is still in scope.</span></span> <span data-ttu-id="ed626-110">匿名型初期化子の内部では、結果のシーケンス内の一致するすべての要素がサブクエリによって順序付けられます。</span><span class="sxs-lookup"><span data-stu-id="ed626-110">Inside the anonymous type initializer, a sub-query orders all the matching elements from the products sequence.</span></span>

[!code-csharp[csProgGuideLINQ#81](~/samples/snippets/csharp/concepts/linq/how-to-order-the-results-of-a-join-clause_1.cs)]

## <a name="see-also"></a><span data-ttu-id="ed626-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed626-111">See also</span></span>

- [<span data-ttu-id="ed626-112">統合言語クエリ (LINQ)</span><span class="sxs-lookup"><span data-stu-id="ed626-112">Language Integrated Query (LINQ)</span></span>](index.md)  
- [<span data-ttu-id="ed626-113">orderby 句</span><span class="sxs-lookup"><span data-stu-id="ed626-113">orderby clause</span></span>](../language-reference/keywords/orderby-clause.md)  
- [<span data-ttu-id="ed626-114">join 句</span><span class="sxs-lookup"><span data-stu-id="ed626-114">join clause</span></span>](../language-reference/keywords/join-clause.md)  