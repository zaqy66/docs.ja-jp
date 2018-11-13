---
title: '?: 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- ?:_CSharpKeyword
- ?_CSharpKeyword
- :_CSharpKeyword
helpviewer_keywords:
- '?: operator [C#]'
- conditional operator (?:) [C#]
ms.assetid: e83a17f1-7500-48ba-8bee-2fbc4c847af4
ms.openlocfilehash: 3e45ff6eaaefa5829c3ed9415abe1a12b7a1d069
ms.sourcegitcommit: 4bca8f7e172fd019ef437a4803bf5895c6bc4781
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "50980623"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="9df36-102">?: 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="9df36-102">?: Operator (C# Reference)</span></span>

<span data-ttu-id="9df36-103">一般に三項条件演算子として知られる、条件演算子 (`?:`) では、ブール式の値に応じて 2 つの値のいずれかが返されます。</span><span class="sxs-lookup"><span data-stu-id="9df36-103">The conditional operator (`?:`), commonly known as the ternary conditional operator, returns one of two values depending on the value of a Boolean expression.</span></span> <span data-ttu-id="9df36-104">条件演算子の構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9df36-104">Following is the syntax for the conditional operator.</span></span>  

```csharp
condition ? first_expression : second_expression;  
```

<span data-ttu-id="9df36-105">C# 7.2 より、`first_expression` と `second_expression` を [`ref` 式](https://github.com/dotnet/csharplang/blob/master/proposals/csharp-7.2/conditional-ref.md)にすることができます。</span><span class="sxs-lookup"><span data-stu-id="9df36-105">Beginning with C# 7.2, the `first_expression` and `second_expression` my be [`ref` expressions](https://github.com/dotnet/csharplang/blob/master/proposals/csharp-7.2/conditional-ref.md):</span></span>

```csharp
ref condition ? ref first_expression : ref second_expression;  
```

<span data-ttu-id="9df36-106">結果は `ref` または `ref readonly` 変数に、または何の修飾子もない変数に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9df36-106">The result may be assigned to a `ref` or `ref readonly` variable, or to a variable with neither modifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="9df36-107">コメント</span><span class="sxs-lookup"><span data-stu-id="9df36-107">Remarks</span></span>

<span data-ttu-id="9df36-108">`condition` は、`true` または `false` に評価される必要があります。</span><span class="sxs-lookup"><span data-stu-id="9df36-108">The `condition` must evaluate to `true` or `false`.</span></span> <span data-ttu-id="9df36-109">`condition` が `true` の場合、`first_expression` が評価され、これが結果となります。</span><span class="sxs-lookup"><span data-stu-id="9df36-109">If `condition` is `true`, `first_expression` is evaluated and becomes the result.</span></span> <span data-ttu-id="9df36-110">`condition` が `false` の場合、`second_expression` が評価され、これが結果となります。</span><span class="sxs-lookup"><span data-stu-id="9df36-110">If `condition` is `false`, `second_expression` is evaluated and becomes the result.</span></span> <span data-ttu-id="9df36-111">2 つの式のどちらか一方だけが評価されます。</span><span class="sxs-lookup"><span data-stu-id="9df36-111">Only one of the two expressions is evaluated.</span></span> <span data-ttu-id="9df36-112">これは、結果が `ref` となる式では次が有効になるため、特に重要です。</span><span class="sxs-lookup"><span data-stu-id="9df36-112">This is particularly important for expressions where the result is a `ref`, as the following is valid:</span></span>

```csharp
ref (storage != null) ? ref storage[3] : ref defaultValue;
```

<span data-ttu-id="9df36-113">`storage` が null である場合、`storage`の参照は評価されません。</span><span class="sxs-lookup"><span data-stu-id="9df36-113">The reference to `storage` is not evaluated when `storage` is null.</span></span>

<span data-ttu-id="9df36-114">結果が値である場合、`first_expression` の型と `second_expression` の型とは、同じ型であるか、または一方の型から他方の型への暗黙の型変換が存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="9df36-114">When the result is a value, the type of `first_expression` and `second_expression` must be the same, or there must be an implicit conversion from one type to the other.</span></span> <span data-ttu-id="9df36-115">結果が `ref` である場合は、`first_expression` と `second_expression` の型が同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9df36-115">When the result is a `ref`, the type of `first_expression` and `second_expression` must be the same.</span></span>

<span data-ttu-id="9df36-116">`if-else` の構築が必要となる場面で条件演算子を使用すると、計算をより簡潔に表現できます。</span><span class="sxs-lookup"><span data-stu-id="9df36-116">You can express calculations that might otherwise require an `if-else` construction more concisely by using the conditional operator.</span></span> <span data-ttu-id="9df36-117">たとえば、次のコードは、まず `if` ステートメントを使用し、次に条件演算子を使用して、整数を正または負に分類します。</span><span class="sxs-lookup"><span data-stu-id="9df36-117">For example, the following code uses first an `if` statement and then a conditional operator to classify an integer as positive or negative.</span></span>

```csharp
int input = Convert.ToInt32(Console.ReadLine());  
string classify;  
  
// if-else construction.  
if (input > 0)  
    classify = "positive";  
else  
    classify = "negative";  
  
// ?: conditional operator.  
classify = (input > 0) ? "positive" : "negative";  
```

<span data-ttu-id="9df36-118">条件演算子の結合規則は右から左になります。</span><span class="sxs-lookup"><span data-stu-id="9df36-118">The conditional operator is right-associative.</span></span> <span data-ttu-id="9df36-119">`a ? b : c ? d : e` という式は、`a ? b : (c ? d : e)` ではなく、`(a ? b : c) ? d : e` と評価されます。</span><span class="sxs-lookup"><span data-stu-id="9df36-119">The expression `a ? b : c ? d : e` is evaluated as `a ? b : (c ? d : e)`, not as `(a ? b : c) ? d : e`.</span></span>  
  
<span data-ttu-id="9df36-120">条件演算子は、オーバーロードできません。</span><span class="sxs-lookup"><span data-stu-id="9df36-120">The conditional operator cannot be overloaded.</span></span>
  
## <a name="example"></a><span data-ttu-id="9df36-121">例</span><span class="sxs-lookup"><span data-stu-id="9df36-121">Example</span></span>

<span data-ttu-id="9df36-122">次の例は、結果が値になる、条件演算子を示します。</span><span class="sxs-lookup"><span data-stu-id="9df36-122">The following example shows the conditional operator whose result is a value:</span></span>

[!code-csharp[csRefOperators?:](~/samples/snippets/csharp/language-reference/operators/ConditionalExamples.cs#ConditionalValue)]

<span data-ttu-id="9df36-123">もう 1 つの例は、結果が ref になる条件演算子を示します。</span><span class="sxs-lookup"><span data-stu-id="9df36-123">The following alternative shows the conditional operator where the result is a reference:</span></span>

[!code-csharp[csRefOperatorsRef?:](~/samples/snippets/csharp/language-reference/operators/ConditionalExamples.cs#ConditionalRef)]

## <a name="see-also"></a><span data-ttu-id="9df36-124">参照</span><span class="sxs-lookup"><span data-stu-id="9df36-124">See Also</span></span>

- [<span data-ttu-id="9df36-125">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="9df36-125">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="9df36-126">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="9df36-126">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="9df36-127">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="9df36-127">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="9df36-128">if-else</span><span class="sxs-lookup"><span data-stu-id="9df36-128">if-else</span></span>](../../../csharp/language-reference/keywords/if-else.md)  
- <span data-ttu-id="9df36-129">[?. 演算子と ?[] 演算子](../../../csharp/language-reference/operators/null-conditional-operators.md)</span><span class="sxs-lookup"><span data-stu-id="9df36-129">[?. and ?[] Operators](../../../csharp/language-reference/operators/null-conditional-operators.md)</span></span>  
- [<span data-ttu-id="9df36-130">??演算子</span><span class="sxs-lookup"><span data-stu-id="9df36-130">?? Operator</span></span>](../../../csharp/language-reference/operators/null-coalescing-operator.md)
