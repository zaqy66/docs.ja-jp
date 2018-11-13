---
title: '条件式: if... then...else (F#)'
description: F# コードの別の分岐を実行する条件式を記述する方法について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 10e4224bef772f00520cf5a0fff2f2920147c2fc
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "44177602"
---
# <a name="conditional-expressions-ifthenelse"></a><span data-ttu-id="51db9-103">条件式: `if...then...else`</span><span class="sxs-lookup"><span data-stu-id="51db9-103">Conditional Expressions: `if...then...else`</span></span>

<span data-ttu-id="51db9-104">`if...then...else`式は、コードの別の分岐を実行し、指定されたブール式に応じて異なる値に評価されます。</span><span class="sxs-lookup"><span data-stu-id="51db9-104">The `if...then...else` expression runs different branches of code and also evaluates to a different value depending on the Boolean expression given.</span></span>

## <a name="syntax"></a><span data-ttu-id="51db9-105">構文</span><span class="sxs-lookup"><span data-stu-id="51db9-105">Syntax</span></span>

```fsharp
if boolean-expression then expression1 [ else expression2 ]
```

## <a name="remarks"></a><span data-ttu-id="51db9-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="51db9-106">Remarks</span></span>

<span data-ttu-id="51db9-107">前の構文で*expression1*ブール式を評価するときに実行される`true`、それ以外の*expression2*を実行します。</span><span class="sxs-lookup"><span data-stu-id="51db9-107">In the previous syntax, *expression1* runs when the Boolean expression evaluates to `true`; otherwise, *expression2* runs.</span></span>

<span data-ttu-id="51db9-108">異なり、他の言語で、`if...then...else`コンストラクトは式、ステートメントではありません。</span><span class="sxs-lookup"><span data-stu-id="51db9-108">Unlike in other languages, the `if...then...else` construct is an expression, not a statement.</span></span> <span data-ttu-id="51db9-109">つまり、実行する分岐の最後の式の値では、値が生成されます。</span><span class="sxs-lookup"><span data-stu-id="51db9-109">That means that it produces a value, which is the value of the last expression in the branch that executes.</span></span> <span data-ttu-id="51db9-110">各分岐で生成された値の型が一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="51db9-110">The types of the values produced in each branch must match.</span></span> <span data-ttu-id="51db9-111">明示的ながある場合`else`ブランチ、その型は、`unit`します。</span><span class="sxs-lookup"><span data-stu-id="51db9-111">If there is no explicit `else` branch, its type is `unit`.</span></span> <span data-ttu-id="51db9-112">そのため場合の種類、`then`分岐以外の任意の型は、 `unit`、必要があります、`else`ブランチと同じ戻り値の型。</span><span class="sxs-lookup"><span data-stu-id="51db9-112">Therefore, if the type of the `then` branch is any type other than `unit`, there must be an `else` branch with the same return type.</span></span> <span data-ttu-id="51db9-113">チェーンと`if...then...else`キーワードを使用することができます、併せて式`elif`の代わりに`else if`; が等しい。</span><span class="sxs-lookup"><span data-stu-id="51db9-113">When chaining `if...then...else` expressions together, you can use the keyword `elif` instead of `else if`; they are equivalent.</span></span>

## <a name="example"></a><span data-ttu-id="51db9-114">例</span><span class="sxs-lookup"><span data-stu-id="51db9-114">Example</span></span>

<span data-ttu-id="51db9-115">次の例を使用する方法を示しています、`if...then...else`式。</span><span class="sxs-lookup"><span data-stu-id="51db9-115">The following example illustrates how to use the `if...then...else` expression.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4501.fs)]

```
10 is less than 20
What is your name? John
How old are you? 9
You are only 9 years old and already learning F#? Wow!
```

## <a name="see-also"></a><span data-ttu-id="51db9-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="51db9-116">See also</span></span>

- [<span data-ttu-id="51db9-117">F# 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="51db9-117">F# Language Reference</span></span>](index.md)
