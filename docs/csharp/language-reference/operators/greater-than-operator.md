---
title: '&gt; 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '>_CSharpKeyword'
helpviewer_keywords:
- '> operator [C#]'
- greater than operator (>) [C#]
ms.assetid: 26d3cb69-9c0b-4cc5-858b-5be1abd6659d
ms.openlocfilehash: 08fe174c7e4351edc1d1c8cdb13d736b98242795
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43510127"
---
# <a name="gt-operator-c-reference"></a><span data-ttu-id="719f7-102">&gt; 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="719f7-102">&gt; Operator (C# Reference)</span></span>
<span data-ttu-id="719f7-103">すべての数値型と列挙型で "より大きい" 関係演算子 (`>`) が定義されます。これは、最初のオペランドが 2 番目のオペランドより大きい場合に `true` を返し、それ以外の場合、`false` を返します。</span><span class="sxs-lookup"><span data-stu-id="719f7-103">All numeric and enumeration types define a "greater than" relational operator (`>`) that returns `true` if the first operand is greater than the second, `false` otherwise.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="719f7-104">コメント</span><span class="sxs-lookup"><span data-stu-id="719f7-104">Remarks</span></span>  
 <span data-ttu-id="719f7-105">ユーザー定義型は `>` 演算子をオーバーロードできます (「[演算子](../../../csharp/language-reference/keywords/operator.md)」を参照)。</span><span class="sxs-lookup"><span data-stu-id="719f7-105">User-defined types can overload the `>` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="719f7-106">`>` をオーバーロードする場合は、[<](../../../csharp/language-reference/operators/less-than-operator.md) もオーバーロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="719f7-106">If `>` is overloaded, [<](../../../csharp/language-reference/operators/less-than-operator.md) must also be overloaded.</span></span>
  
## <a name="example"></a><span data-ttu-id="719f7-107">例</span><span class="sxs-lookup"><span data-stu-id="719f7-107">Example</span></span>  
 [!code-csharp[csRefOperators#29](../../../csharp/language-reference/operators/codesnippet/CSharp/greater-than-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="719f7-108">参照</span><span class="sxs-lookup"><span data-stu-id="719f7-108">See Also</span></span>

- [<span data-ttu-id="719f7-109">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="719f7-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="719f7-110">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="719f7-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="719f7-111">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="719f7-111">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="719f7-112">explicit</span><span class="sxs-lookup"><span data-stu-id="719f7-112">explicit</span></span>](../../../csharp/language-reference/keywords/explicit.md)
