---
title: 遅延計算 (F#)
description: F# 遅延計算が、アプリとライブラリのパフォーマンスを向上する方法について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 8afe815f26978de96291a52973d54a9dbcc5eaf2
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44201630"
---
# <a name="lazy-computations"></a><span data-ttu-id="0f07b-103">遅延計算</span><span class="sxs-lookup"><span data-stu-id="0f07b-103">Lazy Computations</span></span>

<span data-ttu-id="0f07b-104">*遅延計算*は計算には、すぐに評価されませんが、結果が必要なときに代わりに評価されます。</span><span class="sxs-lookup"><span data-stu-id="0f07b-104">*Lazy computations* are computations that are not evaluated immediately, but are instead evaluated when the result is needed.</span></span> <span data-ttu-id="0f07b-105">これは、コードのパフォーマンスを向上させるために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0f07b-105">This can help to improve the performance of your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f07b-106">構文</span><span class="sxs-lookup"><span data-stu-id="0f07b-106">Syntax</span></span>

```fsharp
let identifier = lazy ( expression )
```

## <a name="remarks"></a><span data-ttu-id="0f07b-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="0f07b-107">Remarks</span></span>

<span data-ttu-id="0f07b-108">前の構文で*式*結果が、必要な場合にのみ評価されるコードと*識別子*は結果を格納する値です。</span><span class="sxs-lookup"><span data-stu-id="0f07b-108">In the previous syntax, *expression* is code that is evaluated only when a result is required, and *identifier* is a value that stores the result.</span></span> <span data-ttu-id="0f07b-109">型の値は、 [ `Lazy<'T>`](https://msdn.microsoft.com/library/b29d0af5-6efb-4a55-a278-2662a4ecc489)場所、実際の種類のために使用`'T`式の結果から決定されます。</span><span class="sxs-lookup"><span data-stu-id="0f07b-109">The value is of type [`Lazy<'T>`](https://msdn.microsoft.com/library/b29d0af5-6efb-4a55-a278-2662a4ecc489), where the actual type that is used for `'T` is determined from the result of the expression.</span></span>

<span data-ttu-id="0f07b-110">遅延計算を使用すると、結果が必要な場合のみ、計算の実行を制限することでパフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="0f07b-110">Lazy computations enable you to improve performance by restricting the execution of a computation to only those situations in which a result is needed.</span></span>

<span data-ttu-id="0f07b-111">メソッドを呼び出すを強制的に実行する計算、`Force`します。</span><span class="sxs-lookup"><span data-stu-id="0f07b-111">To force the computation to be performed, you call the method `Force`.</span></span> <span data-ttu-id="0f07b-112">`Force` 1 回だけ実行する実行をします。</span><span class="sxs-lookup"><span data-stu-id="0f07b-112">`Force` causes the execution to be performed only one time.</span></span> <span data-ttu-id="0f07b-113">後続の呼び出し`Force`同じが、任意のコードを実行せずに返します。</span><span class="sxs-lookup"><span data-stu-id="0f07b-113">Subsequent calls to `Force` return the same result, but do not execute any code.</span></span>

<span data-ttu-id="0f07b-114">遅延計算の使用と、使用して、次のコードを示しています`Force`します。</span><span class="sxs-lookup"><span data-stu-id="0f07b-114">The following code illustrates the use of lazy computation and the use of `Force`.</span></span> <span data-ttu-id="0f07b-115">このコードの種類で`result`は`Lazy<int>`、および`Force`メソッドを返します。、`int`します。</span><span class="sxs-lookup"><span data-stu-id="0f07b-115">In this code, the type of `result` is `Lazy<int>`, and the `Force` method returns an `int`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet73011.fs)]

<span data-ttu-id="0f07b-116">遅延評価は、ではなく、`Lazy`入力、シーケンスにも使用します。</span><span class="sxs-lookup"><span data-stu-id="0f07b-116">Lazy evaluation, but not the `Lazy` type, is also used for sequences.</span></span> <span data-ttu-id="0f07b-117">詳細については、次を参照してください。[シーケンス](sequences.md)します。</span><span class="sxs-lookup"><span data-stu-id="0f07b-117">For more information, see [Sequences](sequences.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0f07b-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f07b-118">See also</span></span>

- [<span data-ttu-id="0f07b-119">F# 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="0f07b-119">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="0f07b-120">LazyExtensions モジュール</span><span class="sxs-lookup"><span data-stu-id="0f07b-120">LazyExtensions module</span></span>](https://msdn.microsoft.com/library/86671f40-84a0-402a-867d-ae596218d948)
