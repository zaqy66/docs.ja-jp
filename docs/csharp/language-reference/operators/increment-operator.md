---
title: ++ 演算子 (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- ++_CSharpKeyword
helpviewer_keywords:
- increment operator (++) [C#]
- ++ operator [C#]
ms.assetid: e9dec353-070b-44fb-98ed-eb8fdf753feb
ms.openlocfilehash: a52f614ce1bbfb8e9d9be686b277c1e69f6f9d35
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45593102"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="4b4b2-102">++ 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="4b4b2-102">++ Operator (C# Reference)</span></span>
<span data-ttu-id="4b4b2-103">インクリメント演算子 (`++`) は、オペランドを 1 ずつインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="4b4b2-103">The increment operator (`++`) increments its operand by 1.</span></span> <span data-ttu-id="4b4b2-104">インクリメント演算子はそのオペランド ( `++variable` および `variable++`) の前後に指定できます。</span><span class="sxs-lookup"><span data-stu-id="4b4b2-104">The increment operator can appear before or after its operand: `++variable` and `variable++`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4b4b2-105">コメント</span><span class="sxs-lookup"><span data-stu-id="4b4b2-105">Remarks</span></span>  
 <span data-ttu-id="4b4b2-106">1 番目の形式は前置インクリメント演算です</span><span class="sxs-lookup"><span data-stu-id="4b4b2-106">The first form is a prefix increment operation.</span></span> <span data-ttu-id="4b4b2-107">この演算の結果は、インクリメント後のオペランドの値になります。</span><span class="sxs-lookup"><span data-stu-id="4b4b2-107">The result of the operation is the value of the operand after it has been incremented.</span></span>  
  
 <span data-ttu-id="4b4b2-108">2 番目の形式は後置インクリメント演算です。</span><span class="sxs-lookup"><span data-stu-id="4b4b2-108">The second form is a postfix increment operation.</span></span> <span data-ttu-id="4b4b2-109">この演算の結果は、インクリメント前のオペランドの値になります。</span><span class="sxs-lookup"><span data-stu-id="4b4b2-109">The result of the operation is the value of the operand before it has been incremented.</span></span>  
  
 <span data-ttu-id="4b4b2-110">数値型と列挙型には事前定義のインクリメント演算子があります。</span><span class="sxs-lookup"><span data-stu-id="4b4b2-110">Numeric and enumeration types have predefined increment operators.</span></span> <span data-ttu-id="4b4b2-111">ユーザー定義型は `++` 演算子をオーバーロードできます。</span><span class="sxs-lookup"><span data-stu-id="4b4b2-111">User-defined types can overload the `++` operator.</span></span> <span data-ttu-id="4b4b2-112">整数型に対する演算は、通常、列挙型で使用できます。</span><span class="sxs-lookup"><span data-stu-id="4b4b2-112">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4b4b2-113">例</span><span class="sxs-lookup"><span data-stu-id="4b4b2-113">Example</span></span>  
 [!code-csharp[csRefOperators#3](../../../csharp/language-reference/operators/codesnippet/CSharp/increment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="4b4b2-114">参照</span><span class="sxs-lookup"><span data-stu-id="4b4b2-114">See Also</span></span>

- [<span data-ttu-id="4b4b2-115">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="4b4b2-115">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="4b4b2-116">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="4b4b2-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="4b4b2-117">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="4b4b2-117">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
