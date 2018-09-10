---
title: 配列での foreach の使用 (C# プログラミング ガイド)
ms.date: 05/23/2018
helpviewer_keywords:
- arrays [C#], foreach
- foreach statement [C#], using with arrays
ms.assetid: 5f2da2a9-1f56-4de5-94cc-e07f4f7a0244
ms.openlocfilehash: 298ee915bbe11313f3b33ea7dae9353ef956a231
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43509536"
---
# <a name="using-foreach-with-arrays-c-programming-guide"></a><span data-ttu-id="e291b-102">配列での foreach の使用 (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="e291b-102">Using foreach with Arrays (C# Programming Guide)</span></span>

<span data-ttu-id="e291b-103">[foreach](../../language-reference/keywords/foreach-in.md) ステートメントでは、配列の要素の反復処理を、簡単かつ安全に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e291b-103">The [foreach](../../language-reference/keywords/foreach-in.md) statement provides a simple, clean way to iterate through the elements of an array.</span></span>

<span data-ttu-id="e291b-104">1 次元配列の場合、`foreach` ステートメントは、インデックス 0 から始まりインデックス `Length - 1` で終わるインデックスの昇順で要素を処理します。</span><span class="sxs-lookup"><span data-stu-id="e291b-104">For single-dimensional arrays, the `foreach` statement processes elements in increasing index order, starting with index 0 and ending with index `Length - 1`:</span></span>

[!code-csharp[csProgGuideArrays#28](./codesnippet/CSharp/using-foreach-with-arrays_1.cs)]

<span data-ttu-id="e291b-105">多次元配列の場合、右端の次元のインデックスが最初に加算されていき、次にその左の次元、またその左、というような方法で各要素がトラバースされます。</span><span class="sxs-lookup"><span data-stu-id="e291b-105">For multi-dimensional arrays, elements are traversed such that the indices of the rightmost dimension are increased first, then the next left dimension, and so on to the left:</span></span>

[!code-csharp[csProgGuideArrays#29](./codesnippet/CSharp/using-foreach-with-arrays_2.cs)]

<span data-ttu-id="e291b-106">ただし、多次元配列では、入れ子になった [for](../../language-reference/keywords/for.md) ループを使用した方が、配列要素を処理する順序をより厳密に制御できます。</span><span class="sxs-lookup"><span data-stu-id="e291b-106">However, with multidimensional arrays, using a nested [for](../../language-reference/keywords/for.md) loop gives you more control over the order in which to process the array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="e291b-107">参照</span><span class="sxs-lookup"><span data-stu-id="e291b-107">See Also</span></span>

- <xref:System.Array>  
- [<span data-ttu-id="e291b-108">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="e291b-108">C# Programming Guide</span></span>](../index.md)  
- [<span data-ttu-id="e291b-109">配列</span><span class="sxs-lookup"><span data-stu-id="e291b-109">Arrays</span></span>](index.md)  
- [<span data-ttu-id="e291b-110">1 次元配列</span><span class="sxs-lookup"><span data-stu-id="e291b-110">Single-Dimensional Arrays</span></span>](single-dimensional-arrays.md)  
- [<span data-ttu-id="e291b-111">多次元配列</span><span class="sxs-lookup"><span data-stu-id="e291b-111">Multidimensional Arrays</span></span>](multidimensional-arrays.md)  
- [<span data-ttu-id="e291b-112">ジャグ配列</span><span class="sxs-lookup"><span data-stu-id="e291b-112">Jagged Arrays</span></span>](jagged-arrays.md)
