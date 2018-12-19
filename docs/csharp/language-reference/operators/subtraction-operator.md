---
title: '- 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- -_CSharpKeyword
helpviewer_keywords:
- '- operator [C#]'
- subtraction operator (-) [C#]
ms.assetid: 4de7a4fa-c69d-48e6-aff1-3130af970b2d
ms.openlocfilehash: 5a467e8383d7510260ad3044976601deca7cafdb
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53242231"
---
# <a name="--operator-c-reference"></a><span data-ttu-id="02286-102">- 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="02286-102">- Operator (C# Reference)</span></span>
<span data-ttu-id="02286-103">`-` 演算子には、単項演算子としての働きと 2 項演算子としての働きとがあります。</span><span class="sxs-lookup"><span data-stu-id="02286-103">The `-` operator can function as either a unary or a binary operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="02286-104">コメント</span><span class="sxs-lookup"><span data-stu-id="02286-104">Remarks</span></span>  
 <span data-ttu-id="02286-105">すべての数値型には、単項 `-` 演算子が事前定義されています。</span><span class="sxs-lookup"><span data-stu-id="02286-105">Unary `-` operators are predefined for all numeric types.</span></span> <span data-ttu-id="02286-106">数値型に対する単項 `-` 演算の結果は、オペランドの反転の数値となります。</span><span class="sxs-lookup"><span data-stu-id="02286-106">The result of a unary `-` operation on a numeric type is the numeric negation of the operand.</span></span>  
  
 <span data-ttu-id="02286-107">最初のオペランドから 2 番目のオペランドを減算するために、すべての数値型と列挙型に 2 項 `-` 演算子が事前定義されています。</span><span class="sxs-lookup"><span data-stu-id="02286-107">Binary `-` operators are predefined for all numeric and enumeration types to subtract the second operand from the first.</span></span>  
  
 <span data-ttu-id="02286-108">2 項 `-` 演算子はデリゲート型にも備わっており、その場合、デリゲートの削除が実行されます。</span><span class="sxs-lookup"><span data-stu-id="02286-108">Delegate types also provide a binary `-` operator, which performs delegate removal.</span></span>  
  
 <span data-ttu-id="02286-109">単項 `-` 演算子と 2 項 `-` 演算子は、ユーザー定義型でオーバーロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="02286-109">User-defined types can overload the unary `-` and binary `-` operators.</span></span> <span data-ttu-id="02286-110">詳細については、「[operator (C# Reference) (operator (C# リファレンス))](../../../csharp/language-reference/keywords/operator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02286-110">For more information, see [operator (C# Reference)](../../../csharp/language-reference/keywords/operator.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="02286-111">例</span><span class="sxs-lookup"><span data-stu-id="02286-111">Example</span></span>  
 [!code-csharp[csRefOperators#40](../../../csharp/language-reference/operators/codesnippet/CSharp/subtraction-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="02286-112">参照</span><span class="sxs-lookup"><span data-stu-id="02286-112">See Also</span></span>

- [<span data-ttu-id="02286-113">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="02286-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="02286-114">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="02286-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="02286-115">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="02286-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
