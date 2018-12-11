---
title: 'ループ: while...do 式 (F#)'
description: 参照してください、... 中は式を使用して、指定したテスト条件が true の場合は、反復実行 (ループ) を実行します。
ms.date: 05/16/2016
ms.openlocfilehash: 43e2098ad6c7f103babc2471aebe987040feb989
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53127278"
---
# <a name="loops-whiledo-expression"></a><span data-ttu-id="a2be6-103">ループ: while...do 式</span><span class="sxs-lookup"><span data-stu-id="a2be6-103">Loops: while...do Expression</span></span>

<span data-ttu-id="a2be6-104">`while...do`式を使用して、指定したテスト条件が true の場合は、反復実行 (ループ) を実行します。</span><span class="sxs-lookup"><span data-stu-id="a2be6-104">The `while...do` expression is used to perform iterative execution (looping) while a specified test condition is true.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2be6-105">構文</span><span class="sxs-lookup"><span data-stu-id="a2be6-105">Syntax</span></span>

```fsharp
while test-expression do
    body-expression
```

## <a name="remarks"></a><span data-ttu-id="a2be6-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="a2be6-106">Remarks</span></span>

<span data-ttu-id="a2be6-107">*テスト式*評価; である場合は、 `true`、*式の本体*を実行し、もう一度テスト式が評価されます。</span><span class="sxs-lookup"><span data-stu-id="a2be6-107">The *test-expression* is evaluated; if it is `true`, the *body-expression* is executed and the test expression is evaluated again.</span></span> <span data-ttu-id="a2be6-108">*式の本体*型である必要があります`unit`します。</span><span class="sxs-lookup"><span data-stu-id="a2be6-108">The *body-expression* must have type `unit`.</span></span> <span data-ttu-id="a2be6-109">場合テスト式`false`イテレーションが終了します。</span><span class="sxs-lookup"><span data-stu-id="a2be6-109">If the test expression is `false`, the iteration ends.</span></span>

<span data-ttu-id="a2be6-110">次の例では、使用、`while...do`式。</span><span class="sxs-lookup"><span data-stu-id="a2be6-110">The following example illustrates the use of the `while...do` expression.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5301.fs)]

<span data-ttu-id="a2be6-111">前のコードの出力は、1 から 20 までのランダムな数値のうち、最後は 10 ストリームです。</span><span class="sxs-lookup"><span data-stu-id="a2be6-111">The output of the previous code is a stream of random numbers between 1 and 20, the last of which is 10.</span></span>

```
13 19 8 18 16 2 10
Found a 10!
```

> [!NOTE]
> <span data-ttu-id="a2be6-112">使用することができます`while...do`シーケンス式とその他のコンピュテーション式で、カスタマイズされたバージョンの場合、`while...do`式を使用します。</span><span class="sxs-lookup"><span data-stu-id="a2be6-112">You can use `while...do` in sequence expressions and other computation expressions, in which case a customized version of the `while...do` expression is used.</span></span> <span data-ttu-id="a2be6-113">詳細については、次を参照してください。[シーケンス](sequences.md)、[非同期ワークフロー](asynchronous-workflows.md)、および[コンピュテーション式](computation-expressions.md)します。</span><span class="sxs-lookup"><span data-stu-id="a2be6-113">For more information, see [Sequences](sequences.md), [Asynchronous Workflows](asynchronous-workflows.md), and [Computation Expressions](computation-expressions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a2be6-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2be6-114">See also</span></span>

- [<span data-ttu-id="a2be6-115">F# 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="a2be6-115">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="a2be6-116">ループ:`for...in` 式</span><span class="sxs-lookup"><span data-stu-id="a2be6-116">Loops: `for...in` Expression</span></span>](loops-for-in-expression.md)
- [<span data-ttu-id="a2be6-117">ループ:`for...to` 式</span><span class="sxs-lookup"><span data-stu-id="a2be6-117">Loops: `for...to` Expression</span></span>](loops-for-to-expression.md)
