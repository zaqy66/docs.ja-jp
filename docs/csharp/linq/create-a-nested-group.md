---
title: 入れ子になったグループの作成 (C# での LINQ)
description: C# で LINQ クエリ式に入れ子になったグループを作成する方法について説明します。
ms.date: 12/1/2016
ms.assetid: e9f00708-362e-4d13-98c5-d77549347ba0
ms.openlocfilehash: c973048d0859f61596c62c294131b8c00d0039f8
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37404750"
---
# <a name="create-a-nested-group"></a><span data-ttu-id="bc11f-103">入れ子になったグループの作成</span><span class="sxs-lookup"><span data-stu-id="bc11f-103">Create a nested group</span></span>

<span data-ttu-id="bc11f-104">LINQ クエリ式で入れ子になったグループを作成する方法を次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="bc11f-104">The following example shows how to create nested groups in a LINQ query expression.</span></span> <span data-ttu-id="bc11f-105">学年レベルに基づいて作成した各グループを、さらに個人の名前に基づくグループに分割します。</span><span class="sxs-lookup"><span data-stu-id="bc11f-105">Each group that is created according to student year or grade level is then further subdivided into groups based on the individuals' names.</span></span>

## <a name="example"></a><span data-ttu-id="bc11f-106">例</span><span class="sxs-lookup"><span data-stu-id="bc11f-106">Example</span></span>

> [!NOTE]
> <span data-ttu-id="bc11f-107">この例には、「[オブジェクトのコレクションの照会](query-a-collection-of-objects.md)」のサンプル コードで定義されているオブジェクトへの参照が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bc11f-107">This example contains references to objects that are defined in the sample code in [Query a collection of objects](query-a-collection-of-objects.md).</span></span>

[!code-csharp[csProgGuideLINQ#24](~/samples/snippets/csharp/concepts/linq/how-to-create-a-nested-group_1.cs)]

<span data-ttu-id="bc11f-108">入れ子になったグループの内部要素に対して反復処理を実行するために、入れ子になった `foreach` ループが 3 つ必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="bc11f-108">Note that three nested `foreach` loops are required to iterate over the inner elements of a nested group.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc11f-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc11f-109">See also</span></span>

[<span data-ttu-id="bc11f-110">統合言語クエリ (LINQ)</span><span class="sxs-lookup"><span data-stu-id="bc11f-110">Language Integrated Query (LINQ)</span></span>](index.md)
